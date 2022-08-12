---
title: 启用税款计算配置的主数据查找
description: 本文说明如何设置和启用税款计算主数据查找功能。
author: kai-cloud
ms.date: 07/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3642bb88d5b0570014513b64eef5fdab6d1ee9d3
ms.sourcegitcommit: 5b721f6fc1ba4350b5bd0eae457f71d80246db42
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/20/2022
ms.locfileid: "9181115"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>启用税款计算配置的主数据查找 

[!include [banner](../includes/banner.md)]

本文说明如何设置和启用税款计算主数据查找功能。 可以使用下拉列表为 **法人**、**供应商帐户**、**物料代码** 和 **交货期限** 等字段选择税款计算配置中的值。 这些值来自使用 Microsoft Dataverse 数据源的连接的 Microsoft Dynamics 365 Finance 环境。

> [!NOTE] 
> 税款计算主数据查找功能是可选功能。 如果您在 Regulatory Configuration Service (RCS) 中禁用了 **税务服务 Dataverse 数据源支持** 功能，您可以跳过以下步骤。 但是，在这种情况下，税款计算配置中将没有下拉列表。

若要在税款计算功能版本配置中启用下拉列表，请完成以下步骤。

1. [启用 Microsoft Power Platform 集成并打开 Dataverse 环境。](#enable)
2. [安装财务和运营虚拟实体。](#install)
3. [注册 Azure Active Directory (Azure AD) 应用程序。](#register)
4. [在财务和运营应用中授予应用权限。](#grant)
5. [配置虚拟实体数据源。](#configure)
6. [启用 Dataverse 虚拟实体。](#virtual)
7. [设置税款计算的连接应用程序。](#set-up)
8. [导入和设置 Dataverse 模型映射配置。](#import)

## <a name="enable-microsoft-power-platform-integration-and-open-the-dataverse-environment"></a><a name='enable'></a>启用 Microsoft Power Platform 集成并打开 Dataverse 环境

在 Microsoft Dynamics Lifecycle Services (LCS) 中创建新的财务和运营应用环境时，可以启用财务和运营应用与 Microsoft Power Platform 的集成。 有关详细信息，请参阅 [Microsoft Power Platform 集成 - 加载项概述](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)。 完成后，Microsoft Power Platform 环境的名称将显示在 **Power Platform 集成** 部分。

1. 在 LCS 内，在您的财务和运营环境中，在 **Power Platform 集成** 部分，查找并记录链接环境的 **环境名称** 值。

    [![环境名称值。](./media/tcs-dataverse-master-data-lookup-1.png)](./media/tcs-dataverse-master-data-lookup-1.png)

2. 在 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com/environments)，在 **环境** 选项卡上，选择与您所记录的 **环境名称** 值匹配的环境。
3. 在 **详细信息** 页面上，查找 Dataverse 环境的 **环境 URL** 值。 请记录此值，因为在[步骤 7. 设置税款计算的连接应用程序](#set-up)中需要用到它。
4. 通过选择 **环境 URL** 值，确保您可以在浏览器中打开 Dataverse 环境。

    [![Dataverse 环境页面。](./media/tcs-dataverse-master-data-lookup-2.png)](./media/tcs-dataverse-master-data-lookup-2.png)

    > [!NOTE]
    > 在浏览器中保持 Dataverse 环境处于打开状态。 您将需要在[步骤 5. 配置虚拟实体数据源](#configure)中使用它。

有关详细信息，请参阅[启用 Microsoft Power Platform 集成](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md)。

## <a name="install-finance-and-operations-virtual-entities"></a><a name='install'></a>安装财务和运营虚拟实体

必须从 Microsoft AppSource 虚拟实体解决方案安装财务和运营虚拟实体的 Dataverse 解决方案。

1. 在 AppSource 中，查找[财务和运营虚拟实体](https://appsource.microsoft.com/product/dynamics-365/mscrm.finance_and_operations_virtual_entity)。
2. 选择 **立即获取**。
3. 在 **选择环境** 字段中，输入您之前记录的 **环境名称** 值。
4. 选中相应的复选框，然后选择 **安装**。

安装完成后，您可以在 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com/)内 **资源** \> **Dynamics 365 应用** 下面查找 **财务和运营虚拟实体** 应用。

有关详细信息，请参阅[获取虚拟实体解决方案](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution)。

## <a name="register-an-azure-ad-application"></a><a name='register'></a>注册 Azure AD 应用程序

您必须在与财务和运营应用相同的租户上注册 Azure AD 应用程序，以便 Dataverse 可以调用它们。

1. 在 [Azure 门户](https://portal.azure.com)中，转到 **Azure Active Directory \> 应用注册**。
2. 选择 **新注册**，然后输入以下信息：

    - **名称** - 输入唯一名称。
    - **帐户类型** - 输入 **任何 Azure AD 目录**（单租户或多租户）。
    - **重定向 URI** - 保持此字段为空。

3. 选择 **注册**。
4. 记下 **应用程序（客户端）ID** 值，因为后面需要该值。

    [![Azure AD 应用程序（客户端）ID 值。](./media/tcs-dataverse-master-data-lookup-3.png)](./media/tcs-dataverse-master-data-lookup-3.png)

5. 为应用程序创建对称密钥。
6. 在新应用程序中，选择 **证书和密钥**。
7. 选择 **新客户端密码**。
8. 输入说明，选择到期日期，然后选择 **保存**。 将创建和显示密钥。 复制该值以供以后使用。

有关详细信息，请参阅[注册 Azure AD 应用程序](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#register-the-app-in-the-azure-portal)。

## <a name="grant-app-permissions-in-finance-and-operations-apps"></a><a name='grant'></a>在财务和运营应用中授予应用权限

Dataverse 使用您创建的 Azure AD 应用程序来调用财务和运营应用。 因此，应用程序必须受到财务和运营应用的信任，并与具有适当权限的用户帐户相关联。 在财务和运营应用中，您必须创建一个 **仅** 对虚拟实体功能拥有权限的特殊服务用户。 此服务用户不得具有其他权利。 完成此步骤后，任何具有您创建的 Azure AD 应用密钥的应用程序都将能够调用财务和运营应用环境并访问虚拟实体功能。

1. 在您的环境中，转到 **系统管理** \> **用户** \> **用户**。
2. 选择 **新建** 以新建用户，然后输入以下信息：

    - **用户 ID** - 输入 **dataverseintegration** 或其他值。
    - **用户名** - 输入 **dataverse 集成** 或其他值。
    - **提供程序** - 将此字段设置为 **NonAAD**。
    - **电子邮件** - 输入 **dataverseintegration** 或其他值。 （该值不必是有效的电子邮件帐户。）

3. 将 **CDS 虚拟实体应用程序** 安全角色分配给用户。
4. 删除所有其他角色，包括 **系统用户**。
5. 转到 **系统管理** \> **设置** \> **Azure Active Directory 应用程序** 以注册 Dataverse。 
6. 添加一行，然后在 **客户端 ID** 字段中输入您之前记录的 **应用程序（客户端）ID** 值。
7. 在 **名称** 字段中输入名称。 在这个例子中，输入 **Dataverse 集成**。
8. 在 **用户 ID** 字段中，输入您之前创建的用户 ID。

有关详细信息，请参阅[在财务和运营应用中授予应用权限](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#grant-app-permissions-in-finance-and-operations-apps)。

## <a name="configure-the-virtual-entity-data-source"></a><a name='configure'></a>配置虚拟实体数据源

您必须向 Dataverse 提供要连接到的财务和运营应用实例。

1. 从[步骤 1. 启用 Microsoft Power Platform 集成并打开 Dataverse 环境](#enable)开始，您的 Dataverse 环境在浏览器中仍应是一个开放环境。 选择右上角的设置按钮（齿轮符号），然后选择 **高级设置**。

    [![正在打开 Dataverse 环境中的“高级”设置。](./media/tcs-dataverse-master-data-lookup-4.png)](./media/tcs-dataverse-master-data-lookup-4.png)

2. 在 **设置** 下拉菜单上，选择 **管理**。

    [![管理。](./media/tcs-dataverse-master-data-lookup-5.png)](./media/tcs-dataverse-master-data-lookup-5.png)

3. 选择 **虚拟实体数据源**。

    [![虚拟实体数据源。](./media/tcs-dataverse-master-data-lookup-6.png)](./media/tcs-dataverse-master-data-lookup-6.png)

4. 选择名为 **财务和运营** 的数据源。

    [![财务和运营数据源。](./media/tcs-dataverse-master-data-lookup-7.png)](./media/tcs-dataverse-master-data-lookup-7.png)

5. 输入前面步骤中的以下信息：

    - **目标 URL** - 输入可用于访问财务和运营应用的 URL。
    - **OAuth URL** – 输入 `https://login.windows.net/`。
    - **租户 ID** – 指定您的租户。 此值可以是您公司电子邮件的域名（如 contoso.com）。
    - **AAD 应用程序 ID** – 输入之前创建的 **应用程序（客户端）ID** 值。
    - **AAD 应用程序密码** – 输入之前生成的密码。
    - **AAD 资源** - 输入 **00000015-0000-0000-c000-000000000000**。 此值是表示财务和运营应用的 Azure AD 应用程序。 它应始终是此相同值。

6. 保存所做的更改。
7. 关闭此页面以返回到 **管理** 页面，您将在其中开始[步骤 6. 启用 Dataverse 虚拟实体](#virtual)。

    [![关闭要编辑的实体。](./media/tcs-dataverse-master-data-lookup-8.png)](./media/tcs-dataverse-master-data-lookup-8.png)

有关详细信息，请参阅[配置虚拟实体数据源](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#configure-the-virtual-entity-data-source)。

## <a name="enable-dataverse-virtual-entities"></a><a name='virtual'></a>启用 Dataverse 虚拟实体

财务和运营应用中的虚拟实体的可见性必须设置为 **是**，然后才能通过“税款计算”配置使用它们。

> [!NOTE]
> 在[步骤 8. 设置税款计算的连接应用程序](#import)中，只需单击一次便可启用与税款计算相关的虚拟实体，从而可以跳过此步骤。 但是，我们建议您手动启用至少一个虚拟实体，以表明已正确建立财务和运营应用与 Dataverse 之间的连接。

1. 在您的 Dataverse 环境中，在 **管理** 页面上，选择右上角的筛选器按钮（漏斗符号）。

    [![筛选按钮。](./media/tcs-dataverse-master-data-lookup-9.png)](./media/tcs-dataverse-master-data-lookup-9.png)

2. 在 **高级查找** 窗口内的 **查找** 字段中，选择 **可用的财务和运营实体**。
3. 添加以下规则：**名称** - **包含** - **CompanyInfoEntity**。 然后选择 **结果**。

    [![高级查找窗口。](./media/tcs-dataverse-master-data-lookup-10.png)](./media/tcs-dataverse-master-data-lookup-10.png)

4. 在搜索结果中选择 **CompanyInfoEntity**，选中 **可见** 复选框，然后选择 **保存**。

    [![设置实体可见性。](./media/tcs-dataverse-master-data-lookup-11.png)](./media/tcs-dataverse-master-data-lookup-11.png)

5. 对税款计算配置中引用的以下实体重复上述步骤：

    - CompanyInfoEntity
    - CurrencyEntity
    - CustCustomerV3Entity
    - DeliveryTermsEntity
    - EcoResProductCategoryEntity
    - EcoResReleasedProductV2Entity
    - LogisticsAddressCountryRegionTranslationEntity
    - LogisticsAddressStateEntity
    - PurchProcurementChargeCDSEntity
    - SalesChargeCDSEntity
    - TaxGroupEntity
    - TaxItemGroupHeadingEntity
    - VendVendorV2Entity
    - InventOperationalSiteV2Entity
    - TaxExemptCodeEntity
    - InventWarehouseEntity

    > [!NOTE]
    > Dataverse 只能检索实体的前 5,000 条记录，并使其在税款计算配置的下拉列表中可用。

有关详细信息，请参阅[启用 Microsoft Dataverse 虚拟实体](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md)。

## <a name="set-up-the-connected-application-for-tax-calculation"></a><a name='set-up'></a>设置税款计算的连接应用程序。

1. 在 RCS 中，打开 **功能管理** 工作区，启用以下功能：

    - 电子报告 Dataverse 数据源支持
    - 税务服务 Dataverse 数据源支持
    - 全球化功能

2. 转到 **电子报告**，然后在 **相关链接** 部分，选择 **已连接的应用程序**。

    [![已连接的应用程序。](./media/tcs-dataverse-master-data-lookup-12.png)](./media/tcs-dataverse-master-data-lookup-12.png)

3. 选择 **新建** 以添加记录，然后输入以下信息。

    - **名称** - 输入名称。
    - **类型** – 选择 **Dataverse**。
    - **应用程序** - 输入 Dataverse 环境的 **环境 URL** 值，您在[步骤 1. 启用 Microsoft Power Platform 集成并打开 Dataverse 环境](#enable)中记录了此值。
    - **租户** - 输入您的租户。
    - **自定义 URL** - 输入您的 Dataverse URL 并向其追加 **/api/data/v9.1**。

4. 选择 **检查连接**，然后在显示的对话框中选择 **单击此处连接至所选的远程应用程序**。

    [![正在检查连接。](./media/tcs-dataverse-master-data-lookup-13.png)](./media/tcs-dataverse-master-data-lookup-13.png)
5. 确保您收到“成功！” 消息，此消息指示已成功建立连接。

    [![成功消息。](./media/tcs-dataverse-master-data-lookup-14.png)](./media/tcs-dataverse-master-data-lookup-14.png)

## <a name="import-and-set-up-the-dataverse-model-mapping-configuration"></a><a name='import'></a>导入和设置 Dataverse 模型映射配置

Microsoft 为实体提供从财务和运营应用到税款计算的默认模型映射配置。

1. 在 RCS 中，转到 **电子申报**。
2. 在 **配置提供程序** 部分中，在 **Microsoft** 提供商的磁贴上，选择 **存储库**。

    [![存储库。](./media/tcs-dataverse-master-data-lookup-15.png)](./media/tcs-dataverse-master-data-lookup-15.png)

3. 选择 **全局配置存储库** 记录，然后选择 **打开**。
4. 在 **税务数据模型** \> **税款计算数据模型** 下面，选择 **Dataverse 模型映射** 配置。
5. 在 **版本** 快速选项卡上，选择与您的财务和运营应用版本匹配的版本，然后选择 **导入**。

    [![正在导入 Dataverse 模型映射配置。](./media/tcs-dataverse-master-data-lookup-16.png)](./media/tcs-dataverse-master-data-lookup-16.png)

    > [!IMPORTANT]
    > **Dataverse 模型映射** 配置仅对其导入的最高版本有效。 因此，您导入的 **Dataverse 模型映射** 配置版本不应高于您计划实施的税款计算配置版本。 例如，如果您计划实施税款计算配置 40.50.225 版本，则应仅导入 **Dataverse 模型映射** 配置 40.50.13 版本。 您不应导入版本 40.54.14。 否则，配置中将存在数据模型不匹配。

6. 返回 **电子申报**，并选择 **税务配置** 磁贴。
7. 选择导入的 **Dataverse 模型映射** 配置，然后选择 **编辑**。
8. 将 **模型映射的默认值** 选项设置为 **是**。
9. 在 **已连接的应用程序** 字段中，选择您在[步骤 7. 设置税款计算的连接应用程序](#set-up)中设置的已连接应用程序。
10. 将 **设置虚拟表可见性** 选项设置为 **是**，以将所有与税款计算相关的虚拟实体设置为可见。

您现在已完成主数据查找功能的设置。 现在将在 **税款计算功能版本** 设置中启用字段下载列表，其中包括 Dynamics 365 Finance 中的 **法人**、**供应商帐户**、**物料代码** 和 **交货期限** 等字段。

[![法人下拉列表。](./media/tcs-dataverse-master-data-lookup-17.png)](./media/tcs-dataverse-master-data-lookup-17.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
