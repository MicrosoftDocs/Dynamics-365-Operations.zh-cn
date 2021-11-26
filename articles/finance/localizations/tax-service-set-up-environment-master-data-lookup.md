---
title: 启用税款计算配置的主数据查找
description: 本主题说明如何设置和启用税款计算主数据查找功能。
author: kai-cloud
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dafeac01aaff62cbbd5ce6ecb0af0ef111f513b2
ms.sourcegitcommit: 76fe020f9c5f4e5cc2e93f5ccb3b040f12b0363e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2021
ms.locfileid: "7749502"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>启用税款计算配置的主数据查找 

[!include [banner](../includes/banner.md)]

本主题说明如何设置和启用税款计算主数据查找功能。 可以使用下拉列表为 **供应商帐户**、**物料代码** 和 **交货期限** 等字段选择税款计算配置中的值。 这些值来自使用 Microsoft Dataverse 数据源的连接的 Microsoft Dynamics 365 Finance 环境。

1. 在 Microsoft Dynamics Lifecycle Services (LCS) 中设置 Microsoft Power Platform 集成。 有关详细信息，请参阅 [Microsoft Power Platform 集成 - 加载项概述](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)。 完成此步骤后，Microsoft Power Platform 环境的名称将显示在 **Power Platform 集成** 部分。
2. 转到 [Microsoft Power Platform 管理中心](https://admin.powerplatform.microsoft.com/environments)，选择环境名称。 将提供环境 URL。
3. 设置 Dynamics 365 Finance 和 Dataverse。 有关详细信息，请参阅[获取虚拟实体解决方案](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution)和[身份验证和授权](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization)。
4. 设置以下实体。 有关详细信息，请参阅[启用 Microsoft Dataverse 虚拟实体](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md)。

    - CompanyInfoEntity
    - CurrencyEntity
    - CustCustomerV3Entity
    - DeliveryTermsEntity
    - EcoResProductCategoryEntity
    - EcoResReleasedProductV2Entity
    - LogisticsAddressCityEntity
    - LogisticsAddressCountryRegionTranslationEntity
    - LogisticsAddressStateEntity
    - PurchProcurementChargeCDSEntity
    - SalesChargeCDSEntity
    - TaxGroupEntity
    - TaxItemGroupHeadingEntity
    - VendVendorV2Entity

5. 设置 Regulatory Configuration Service (RCS)。 打开 **功能管理** 工作区，启用以下功能：

    - 电子报告 Dataverse 数据源支持
    - 税务服务 Dataverse 数据源支持
    - 全球化功能

6. 使用租户管理员帐户登录到 RCS。
7. 转到 **电子报告** > **已连接的应用程序**。 
8. 选择 **新建** 以添加记录，然后输入以下字段信息。 

    - 在 **名称** 字段中输入名称。
    - 在 **类型** 字段中，选择 **Dataverse**。
    - 在 **应用程序** 字段中，输入 Dataverse URL。
    - 在 **租户** 字段中，输入您的租户。
    - 在 **自定义 URL** 字段中，输入您的 Dataverse URL 并向其追加“/api/data/v9.1”。

9. 选择 **检查连接**，然后完成连接流程。 

    [![检查连接按钮。](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

10. 转到 **电子报告** > **税务配置**，然后从[税务配置](https://go.microsoft.com/fwlink/?linkid=2158352)中导入税务配置。

    [![税务配置页面，税务数据模型树。](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

11. 如果您使用 Microsoft 配置，转到 **应纳税单据模型映射** 或 **Dataverse 模型映射**，然后在 **已连接的应用程序** 字段中，选择您在步骤 7 中创建的记录。
12. 将 **模型映射的默认值** 设置为 **是**。

    [![模型映射页面。](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
