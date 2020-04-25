---
title: 解决与 Finance and Operations 应用升级相关的问题
description: 本主题提供故障排除信息，可以帮助您解决与 Finance and Operations 应用升级有关的问题。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 59384d8e8d043eb14231a471c7218ced2dddf739
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172869"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a>解决与 Finance and Operations 应用升级相关的问题

[!include [banner](../../includes/banner.md)]



本主题提供 Finance and Operations 应用与 Common Data Service 之间的双写入集成的故障排除信息。 具体来说，提供可以帮助您解决与 Finance and Operations 应用升级有关的问题的信息。

> [!IMPORTANT]
> 本主题解决的某些问题可能需要系统管理员角色或 Microsoft Azure Active Directory (Azure AD) 租户管理员凭据。 介绍每个问题的每一节说明了是否需要特定角色或凭据。

## <a name="database-synchronization-errors"></a>数据库同步错误

**解决此问题所需的角色：** 系统管理员

当您尝试使用 **DualWriteProjectConfiguration** 实体将 Finance and Operations 应用更新为平台更新 30 时，您可能会收到类似于以下示例的错误消息。

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

若要解决此问题，请按照以下步骤操作。

1. 登录到 Finance and Operations 应用的虚拟机 (VM)。
2. 以管理员身份打开 Visual Studio，然后打开应用程序对象树 (AOT)。
3. 搜索 **DualWriteProjectConfiguration**。
4. 在 AOT 中，右键单击 **DualWriteProjectConfiguration**，然后选择**添加到新项目**。 选择**确定**创建使用默认选项的新项目。
5. 在解决方案资源管理器中，右键单击**项目属性**，将**在构建时同步数据库**设置为 **True**。
6. 构建项目，并确认构建成功。
7. 在 **Dynamics 365** 菜单上，选择**同步数据库**。
8. 选择**同步**进行完全数据库同步。
9. 完全数据库同步成功后，请在 Microsoft Dynamics Lifecycle Services (LCS) 中重新运行数据库同步步骤，并在适用时使用手动升级脚本，以便可以继续进行更新。

## <a name="missing-entity-fields-issue-on-maps"></a>映射中的缺少实体字段问题

**解决此问题所需的角色：** 系统管理员

在**双写入**页面上，您可能会收到类似于以下示例的错误消息：

*架构中缺少源字段\<字段名称\>。*

![缺少源字段错误消息的示例](media/error_missing_field.png)

要解决此问题，请首先执行以下步骤，以确保字段在实体中。

1. 登录到 Finance and Operations 应用的 VM。
2. 转到**工作区 \> 数据管理**，选择**框架参数**磁贴，然后在**实体设置**选项卡上，选择**刷新实体列表**刷新实体。
3. 转到**工作区 \> 数据管理**，选择**数据实体**选项卡，确保实体已列出。 如果实体未列出，登录到 Finance and Operations 应用的 VM，确保实体可用。
4. 从 Finance and Operations 应用中的**双写入**页面打开**实体映射**页面。
5. 选择**刷新实体列表**自动填充实体映射中的字段。

如果问题仍然没有解决，请按照下列步骤操作。

> [!IMPORTANT]
> 这些步骤将指导您完成删除实体然后再次添加实体的过程。 为避免出现问题，请确保严格按照以下步骤操作。

1. 在 Finance and Operations 应用中，转到**工作区 \> 数据管理**，然后选择**数据实体**磁贴。
2. 查找缺少该字段的实体。 记下目标实体、暂存表、实体名称和其他列值。
3. 如果您的任何处理组都依赖此实体，请在删除实体之前对处理组采取适当的措施。
4. 删除缺少该字段的实体。
5. 选择**新建**，然后重新添加实体。 指定在步骤 2 中记下的值。
6. 从 Finance and Operations 应用中的**双写入**页面打开**实体映射**页面。
7. 选择**刷新实体列表**自动填充实体映射中的字段。