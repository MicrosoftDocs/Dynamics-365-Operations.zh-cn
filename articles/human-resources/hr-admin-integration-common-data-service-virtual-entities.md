---
title: 配置 Dataverse 虚拟表
description: 本主题介绍如何为 Dynamics 365 Human Resources 配置虚拟表。 生成和更新现有虚拟表，并分析生成的实体和可用表。
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f0dac25ede6c9b9dfcfa1be1f1a5f4d7a7752112
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344706"
---
# <a name="configure-dataverse-virtual-tables"></a>配置 Dataverse 虚拟表

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Human Resources 是 Microsoft Dataverse 中的虚拟数据源。 它提供 Dataverse 和 Microsoft Power Platform 中的完全创建、读取、更新和删除 (CRUD) 操作。 虚拟表的数据未存储在 Dataverse 中，但存储在应用程序数据库中。

若要从 Dataverse 中对 Human Resources 实体启用 CRUD 操作，您必须将这些实体用作 Dataverse 中的虚拟表。 这使您可以从 Dataverse 和 Microsoft Power Platform 中对 Human Resources 中的数据执行 CRUD 操作。 这些操作还支持对 Human Resources 进行完整业务逻辑验证，以确保将数据写入实体时的数据完整性。

> [!NOTE]
> Human Resources 实体与 Dataverse 表对应。 有关 Dataverse（以前的 Common Data Service）和术语更新的详细信息，请参阅[什么是 Microsoft Dataverse？](/powerapps/maker/data-platform/data-platform-intro)

## <a name="available-virtual-tables-for-human-resources"></a>Human Resources 的可用虚拟表

Human Resources 中的所有 Open Data Protocol (OData) 实体都可用作 Dataverse 中的虚拟表。 它们在 Power Platform 中也可用。 您现在可以直接使用具有完全 CRUD 功能的 Human Resources 中的数据构建应用和体验，而无需将数据复制或同步到 Dataverse。 您可以使用 Power Apps 门户来构建面向外部的网站，以为 Human Resources 中的业务流程启用协作方案。

您可以查看在环境中启用的虚拟表列表，然后开始使用 **Dynamics 365 HR 虚拟表** 解决方案的 [Power Apps](https://make.powerapps.com) 中的表。

![Power Apps 中的 Dynamics 365 HR 虚拟表。](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a>虚拟表与本地表

Human Resources 的虚拟表与为 Human Resources 创建的 Dataverse 本地表不同。 

Human Resources 的本地表单独生成，并在 Dataverse 的 HCM 通用解决方案中维护。 对于本地表，数据存储在 Dataverse 中并且需要与 Human Resources 应用程序数据库同步。

> [!NOTE]
> 要获取 Human Resources 的 Dataverse 本地表列表，请参阅 [Dataverse 表](./hr-developer-entities.md)。

## <a name="setup"></a>设置

请按照以下设置步骤在您的环境中启用虚拟表。

### <a name="enable-virtual-tables-in-human-resources"></a>在 Human Resources 中启用虚拟表

首先，您必须在 **功能管理** 工作区中启用虚拟表。

1. 在 Human Resources 中，选择 **系统管理**。

2. 选择 **功能管理** 磁贴。

3. 选择 **Dataverse 中的 HR 虚拟表支持**，然后选择 **启用**。

有关启用和禁用功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

### <a name="register-the-app-in-microsoft-azure"></a>在 Microsoft Azure 中注册应用

您必须在 Azure 门户中注册 Human Resources 实例，以便 Microsoft 标识平台可以为应用和用户提供身份验证和授权服务。 有关在 Azure 中注册应用的详细信息，请参阅[快速入门：向 Microsoft 标识平台注册应用程序](/azure/active-directory/develop/quickstart-register-app)。

1. 打开 [Microsoft Azure 门户](https://portal.azure.com)。

2. 在 Azure 服务中，选择 **应用注册**。

3. 选择 **新注册**。

4. 在 **名称** 字段中，输入应用的描述性名称。 例如，**Dynamics 365 Human Resources 虚拟表**。

5. 在 **重定向 URI** 字段中，输入 Human Resources 实例的命名空间 URL。

6. 选择 **注册**。

7. 注册完成后，Azure 门户显示应用注册的 **概述** 窗格，其中包括其 **应用程序（客户端）ID**。 此时，请记下 **应用程序（客户端）ID**。 您将在[配置虚拟表数据源](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source)时输入此信息。

8. 在左侧导航窗格中，选择 **证书和密码**。

9. 在页面的 **客户端密码** 部分中，选择 **新客户端密码**。

10. 提供描述，选择持续时间，然后选择 **添加**。

11. 从表的 **值** 属性中记录密码的值。 您将在[配置虚拟表数据源](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source)时输入此信息。

    > [!IMPORTANT]
    > 请确保此时记下密码的值。 离开此页面后，密码将不再显示。

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a>安装 Dynamics 365 HR 虚拟表应用

在您的 Power Apps 环境中安装 Dynamics 365 HR 虚拟表应用以将虚拟表解决方案包部署到 Dataverse。

1. 在 Human Resources 中，打开 **Microsoft Dataverse 集成** 页面。

2. 选择 **虚拟表** 选项卡。

3. 选择 **安装虚拟表应用**。

### <a name="configure-the-virtual-table-data-source"></a>配置虚拟表数据源

下一步是在 Power Apps 环境中配置虚拟表数据源。

1. 打开 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com)。

2. 在 **环境** 列表中，选择与您的 Human Resources 实例关联的 Power Apps 环境。

3. 在页面的 **详细信息** 部分中选择 **环境 URL**。

4. 在 **解决方案运行状况中心** 中，选择应用程序页面右上角的 **高级查找** 图标。

5. 在 **高级查找** 页面上的 **查找** 下拉列表中，选择 **Finance and Operations 虚拟数据源配置**。

   > [!NOTE]
   > 上一个设置步骤中安装虚拟表应用可能需要几分钟。 如果列表中没有 **Finance and Operations 虚拟数据源配置**，请稍等片刻，然后刷新列表。

6. 选择 **结果**。

7. 选择 **Microsoft HR 数据源** 记录。

8. 输入数据源配置所需的信息：

   - **目标 URL**：Human Resources 命名空间的 URL。 目标 URL 的格式为：
     
     https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/

     例如:
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     >确保在 URL 的结尾包括“**/**”字符，以避免收到错误。

   - **租户 ID**：Azure Active Directory (Azure AD) 租户 ID。

   - **AAD 应用程序 ID**：为在 Microsoft Azure 门户中注册的应用程序创建的应用程序（客户端）ID。 您在步骤[在 Microsoft Azure 中注册应用](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)的早期阶段就收到了此信息。

   - **AAD 应用程序密码**：为在 Microsoft Azure 门户中注册的应用程序创建的客户端密码。 您在步骤[在 Microsoft Azure 中注册应用](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)的早期阶段就收到了此信息。

   ![Microsoft HR 数据源。](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. 选择 **保存并关闭**。

### <a name="grant-app-permissions-in-human-resources"></a>在 Human Resources 中授予应用权限

在 Human Resources 中为两个 Azure AD 应用程序授予权限：

- 在 Microsoft Azure 门户中为您的租户创建的应用
- 在 Power Apps 环境中安装的 Dynamics 365 HR 虚拟表应用 

1. 在 Human Resources 中，打开 **Azure Active Directory 应用程序** 页面。

2. 选择 **新建** 以创建新的应用程序记录：

    - 在 **客户端 ID** 字段中，输入您在 Microsoft Azure 门户中注册的应用的客户端 ID。
    - 在 **名称** 字段中，输入您在 Microsoft Azure 门户中注册的应用的名称。
    - 在 **用户 ID** 字段中，在 Human Resources 和 Power Apps 环境中选择具有管理员权限的用户的用户 ID。

3. 选择 **新建** 以创建第二个应用程序记录：

    - **客户端 ID**：f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **名称**：Dynamics 365 HR 虚拟表
    - 在 **用户 ID** 字段中，在 Human Resources 和 Power Apps 环境中选择具有管理员权限的用户的用户 ID。

## <a name="generate-virtual-tables"></a>生成虚拟表

设置完成后，您可以选择要在 Dataverse 实例中生成和启用的虚拟表。

1. 在 Human Resources 中，打开 **Microsoft Dataverse 集成** 页面。

2. 选择 **虚拟表** 选项卡。

> [!NOTE]
> 在完成所有所需的设置后，**启用虚拟表** 切换将自动设置为 **是**。 如果切换设置为 **否**，请查看本文档前面部分中的步骤，以确保完成所有先决条件设置。

3. 选择要在 Dataverse 中生成的一个或多个表。

4. 选择 **生成/刷新**。

![Dataverse 集成。](./media/hr-admin-integration-dataverse-integration.png)

## <a name="check-table-generation-status"></a>检查表生成状态

虚拟表通过异步后台进程在 Dataverse 中生成。 有关进程的更新显示在操作中心中。 有关进程的详细信息（包括错误日志）显示在 **进程自动化** 页面中。

1. 在 Human Resources 中，打开 **进程自动化** 页面。

2. 选择 **后台进程** 选项卡。

3. 选择 **虚拟表轮询异步操作后台进程**。

4. 选择 **查看最新结果**。

滑出窗格将显示该进程的最新执行结果。 您可以查看进程的日志，包括从 Dataverse 返回的任何错误。

## <a name="see-also"></a>请参阅

[什么是 Dataverse？](/powerapps/maker/common-data-service/data-platform-intro)<br>
[Dataverse 中的表](/powerapps/maker/common-data-service/entity-overview)<br>
[表关系概述](/powerapps/maker/common-data-service/relationships-overview)<br>
[创建和编辑包含来自外部数据源的数据的虚拟表](/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[什么是 Power Apps 门户？](/powerapps/maker/portals/overview)<br>
[在 Power Apps 中创建应用概述](/powerapps/maker/)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
