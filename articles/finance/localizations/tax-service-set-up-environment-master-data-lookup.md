---
title: 设置用于主数据查询的环境
description: 本主题说明如何设置您的环境以使用税务计算主数据查找功能。
author: kai-cloud
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 9f9b385df1db60b27698d90281c43fabb574af49
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924146"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>设置用于主数据查询的环境

[!include [banner](../includes/banner.md)]

本主题说明如何设置您的环境以使用税务计算主数据查找功能。

1. 在 Lifecycle Services (LCS) 中设置 Power Platform 集成。 有关详细信息，请参阅 [Microsoft Power Platform 集成 - 加载项概述](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)。
2. 设置 Dynamics 365 Finance 和 Microsoft Dataverse。 有关详细信息，请参阅[获取解决方案](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution)和[身份验证和授权](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization)。
3. 设置以下实体。 有关详细信息，请参阅[启用虚拟实体](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities)。
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
4. 设置 Dynamics 365 Regulatory Configuration Service (RCS)。 
5. 为 Microsoft 创建服务请求以启用以下功能的外部测试：

      - ERCdsFeature
      - TaxServiceCDSFeature

6. 转到 **功能管理** 工作区，然后启用以下功能：

      - （预览）电子报告 Dataverse 数据源支持
      - (预览版)税务服务 Dataverse 数据源支持
      - (预览版)全球化功能

5. 使用租户管理员帐户登录到 RCS。
6. 转到 **电子报告** > **已连接的应用程序**。 
7. 选择 **新建** 以添加记录，然后输入以下字段信息。 

   - 在 **名称** 字段中输入名称。
   - 在 **类型** 字段中，选择 **Dataverse**。
   - 在 **应用程序** 字段中，输入 Dataverse URL。
   - 在 **租户** 字段中，输入您的租户。
   - 在 **自定义 URL** 字段中，输入您的 Dataverse URL 并向其追加“/api/data/v9.1”。

8. 选择 **检查连接**，然后完成连接流程。 

   [![检查连接按钮](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

9. 转到 **电子报告** > **税务配置**，然后从[税务配置](https://go.microsoft.com/fwlink/?linkid=2158352)中导入税务配置。

   [![税收配置页面，税务数据模型树](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

10. 如果您使用 Microsoft 配置，转到 **应纳税单据模型映射** 或 **Dataverse 模型映射**，然后在 **已连接的应用程序** 字段中，选择您在步骤 7 中创建的记录。
11. 将 **模型映射的默认值** 设置为 **是**。

   [![模型映射页面](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
