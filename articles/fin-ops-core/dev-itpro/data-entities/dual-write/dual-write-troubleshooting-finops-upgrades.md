---
title: 解决 Finance and Operations 应用升级存在的问题
description: 本主题提供故障排除信息，可以帮助您解决与 Finance and Operations 应用升级有关的问题。
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 97509ac662fad6181cbd60e5e0a44f674410acb9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754030"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a>解决 Finance and Operations 应用升级存在的问题

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



本主题提供 Finance and Operations 应用与 Dataverse 之间的双写入集成的故障排除信息。 具体来说，提供可以帮助您解决与 Finance and Operations 应用升级有关的问题的信息。

> [!IMPORTANT]
> 本主题解决的某些问题可能需要系统管理员角色或 Microsoft Azure Active Directory (Azure AD) 租户管理员凭据。 介绍每个问题的每一节说明了是否需要特定角色或凭据。

## <a name="database-synchronization-errors"></a>数据库同步错误

**解决此问题所需的角色：** 系统管理员

当您尝试使用 **DualWriteProjectConfiguration** 表将 Finance and Operations 应用更新为平台更新 30 时，您可能会收到类似于以下示例的错误消息。

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

若要解决此问题，请按照以下步骤操作。

1. 登录到 Finance and Operations 应用的虚拟机 (VM)。
2. 以管理员身份打开 Visual Studio，然后打开应用程序对象树 (AOT)。
3. 搜索 **DualWriteProjectConfiguration**。
4. 在 AOT 中，右键单击 **DualWriteProjectConfiguration**，然后选择 **添加到新项目**。 选择 **确定** 创建使用默认选项的新项目。
5. 在解决方案资源管理器中，右键单击 **项目属性**，将 **在构建时同步数据库** 设置为 **True**。
6. 构建项目，并确认构建成功。
7. 在 **Dynamics 365** 菜单上，选择 **同步数据库**。
8. 选择 **同步** 进行完全数据库同步。
9. 完全数据库同步成功后，请在 Microsoft Dynamics Lifecycle Services (LCS) 中重新运行数据库同步步骤，并在适用时使用手动升级脚本，以便可以继续进行更新。

## <a name="missing-table-columns-issue-on-maps"></a>映射中缺少表列问题

**解决此问题所需的角色：** 系统管理员

在 **双写入** 页面上，您可能会收到类似于以下示例的错误消息：

*架构中缺少源字段 \<field name\>。*

![缺少源列错误消息的示例](media/error_missing_field.png)

要解决此问题，请首先执行以下步骤，以确保列在表中。

1. 登录到 Finance and Operations 应用的 VM。
2. 转到 **工作区 \> 数据管理**，选择 **框架参数** 磁贴，然后在 **表设置** 选项卡上，选择 **刷新表列表** 刷新表。
3. 转到 **工作区 \> 数据管理**，选择 **数据表** 选项卡，确保表已列出。 如果表未列出，登录到 Finance and Operations 应用的 VM，确保表可用。
4. 从 Finance and Operations 应用中的 **双写入** 页面打开 **表映射** 页面。
5. 选择 **刷新表列表** 自动填充表映射中的列。

如果问题仍然没有解决，请按照下列步骤操作。

> [!IMPORTANT]
> 这些步骤将指导您完成删除表然后再次添加表的过程。 为避免出现问题，请确保严格按照以下步骤操作。

1. 在 Finance and Operations 应用中，转到 **工作区 \> 数据管理**，然后选择 **数据表** 磁贴。
2. 查找缺少该属性的表。 单击工具栏中的 **修改目标映射**。
3. 在 **将暂存映射到目标** 窗格中，单击 **生成映射**。
4. 从 Finance and Operations 应用中的 **双写入** 页面打开 **表映射** 页面。
5. 如果该属性未在映射中自动填充，请单击 **添加属性** 按钮，然后单击 **保存** 手动添加该属性。 
6. 选择映射并单击 **运行**。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]