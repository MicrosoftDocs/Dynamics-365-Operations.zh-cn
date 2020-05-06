---
title: 解决实时同步问题
description: 本主题提供故障排除信息，可以帮助您解决实时同步问题。
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
ms.openlocfilehash: d45b19c1e88e6a27bde4335d4a356f2173bdfcd3
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275409"
---
# <a name="troubleshoot-live-synchronization-issues"></a>解决实时同步问题

[!include [banner](../../includes/banner.md)]



本主题提供 Finance and Operations 应用与 Common Data Service 之间的双写入集成的故障排除信息。 具体来说，提供可以帮助您解决实时同步问题的信息。

> [!IMPORTANT]
> 本主题解决的某些问题可能需要系统管理员角色或 Microsoft Azure Active Directory (Azure AD) 租户管理员凭据。 介绍每个问题的每一节说明了是否需要特定角色或凭据。

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-record-in-a-finance-and-operations-app"></a>在 Finance and Operations 应用中创建记录时，实时同步会引发“403 已禁止”错误

当您在 Finance and Operations 应用中创建记录时，您可能会收到以下错误消息：

*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"此用户不是组织的成员。\\"}}\]，远程服务器返回错误：(403) 已禁止。"}}".*

要解决此问题，请按照[系统要求和先决条件](requirements-and-prerequisites.md)中的步骤操作。 要完成这些步骤，在 Common Data Service 中创建的双写入应用程序用户必须具有系统管理员角色。 默认的负责团队也必须具有系统管理员角色。

## <a name="live-synchronization-for-any-entity-consistently-throws-a-similar-error-when-you-create-a-record-in-a-finance-and-operations-app"></a>在 Finance and Operations 应用中创建记录时，任何实体的实时同步都会引发类似的错误

**解决此问题所需的角色：** 系统管理员

每次尝试在 Finance and Operations 应用中保存实体数据时，您可能会收到以下这样的错误消息：

*无法将更改保存到数据库。工作单元无法提交事务。无法将数据写入实体 uoms。写入 UnitOfMeasureEntity 失败，并显示错误消息“无法与实体 uoms 同步”。*

要解决此问题，您必须确保 Finance and Operations 应用和 Common Data Service 中都存在必备的引用数据。 例如，如果您在 Finance and Operations 应用中的客户属于特定客户组，请确保该客户组存在于 Common Data Service 中。

如果两处都存在数据，并且您已确认问题与数据无关，请按照以下步骤操作。

1. 停止相关实体。
2. 登录到 Finance and Operations 应用，并确保失败实体的记录存在于 DualWriteProjectConfiguration 和 DualWriteProjectFieldConfiguration 表中。 例如，以下是**客户**实体失败时查询将呈现的类似状态。

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. 即使停止实体映射后，如果仍有失败实体的记录，请删除与失败实体相关的记录。 记下 DualWriteProjectConfiguration 表中的 **projectname** 列，并通过使用项目名称删除记录来获取 DualWriteProjectFieldConfiguration 表中的记录。
4. 开始实体映射。 验证数据是否同步，没有任何问题。

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>在 Finance and Operations 应用中创建数据时处理读或写权限错误

在 Finance and Operations 应用中创建数据时，您可能会收到类似于以下示例的“错误请求”错误消息。

![“错误请求”错误消息的示例](media/error_record_id_source.png)

若要解决此问题，您必须为映射的 Dynamics 365 Sales 或 Dynamics 365 Customer Service 业务单位的团队分配正确的安全角色，以启用缺少的权限。

1. 在 Finance and Operations 应用中，找到在数据集成连接集中映射的业务单位。

    ![组织映射](media/mapped_business_unit.png)

2. 登录到 Dynamics 365 中的模型驱动应用内的环境，导航至**设置 \> 安全**，找到映射业务单位的团队。

    ![映射业务单位的团队](media/setting_security_page.png)

3. 打开要编辑的团队页面，然后选择**管理角色**打开**管理团队角色**对话框。

    ![管理角色按钮](media/manage_team_roles.png)

4. 为相关实体分配具有读/写权限的角色，然后选择**确定**。

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-common-data-service-environment"></a>在最近更改了 Common Data Service 环境的环境中解决同步问题

**解决此问题所需的角色：** 系统管理员

当您在 Finance and Operations 应用中创建数据时，您可能会收到以下错误消息：

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**无法为实体 CustCustomerV3Entity 生成有效负载**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"有效负载创建失败，显示错误“URI 无效：此 URI 是空的”。"}\],"isErrorCountUpdated":true}*

这是在 Dynamics 365 中的模型驱动应用中出现的错误情况：

*ISV 代码发生意外错误。(ErrorType = ClientError) 插件发生意外异常 (Execute)：Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception：无法处理实体帐户 -（连接尝试失败，因为连接方未在一段时间后正确响应，或由于连接的主机未能响应导致建立的连接失败*

当您尝试在 Finance and Operations 应用中创建数据但未正确重置 Common Data Service 环境时，将发生此错误。

若要解决此问题，请按照以下步骤操作。

1. 登录到 Finance and Operations 虚拟机 (VM)，打开 SQL Server Management Studio (SSMS)，在 DUALWRITEPROJECTCONFIGURATIONENTITY 表中查找记录，其中 **internalentityname** 等于 **客户 V3**，**externalentityname** 等于**客户**。 这是查询呈现的状态。

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. 使用上一个查询的结果中的项目名称来运行以下查询。

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. 确保 **externalenvironmentURL** 列具有正确的 Common Data Service 或应用 URL。 删除任何指向错误的 Common Data Service URL 的重复记录。 删除 DUALWRITEPROJECTFIELDCONFIGURATION 和 DUALWRITEPROJECTCONFIGURATION 表中的相应记录。
4. 停止实体映射，然后重新开始映射
