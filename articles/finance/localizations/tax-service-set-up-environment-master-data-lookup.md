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
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="4c335-103">设置用于主数据查询的环境</span><span class="sxs-lookup"><span data-stu-id="4c335-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c335-104">本主题说明如何设置您的环境以使用税务计算主数据查找功能。</span><span class="sxs-lookup"><span data-stu-id="4c335-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="4c335-105">在 Lifecycle Services (LCS) 中设置 Power Platform 集成。</span><span class="sxs-lookup"><span data-stu-id="4c335-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="4c335-106">有关详细信息，请参阅 [Microsoft Power Platform 集成 - 加载项概述](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="4c335-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="4c335-107">设置 Dynamics 365 Finance 和 Microsoft Dataverse。</span><span class="sxs-lookup"><span data-stu-id="4c335-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="4c335-108">有关详细信息，请参阅[获取解决方案](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution)和[身份验证和授权](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization)。</span><span class="sxs-lookup"><span data-stu-id="4c335-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="4c335-109">设置以下实体。</span><span class="sxs-lookup"><span data-stu-id="4c335-109">Set up the following entities.</span></span> <span data-ttu-id="4c335-110">有关详细信息，请参阅[启用虚拟实体](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities)。</span><span class="sxs-lookup"><span data-stu-id="4c335-110">For more information, see [Enabling virtual entities](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span></span>
      - <span data-ttu-id="4c335-111">CompanyInfoEntity</span><span class="sxs-lookup"><span data-stu-id="4c335-111">CompanyInfoEntity</span></span>
      - <span data-ttu-id="4c335-112">CurrencyEntity</span><span class="sxs-lookup"><span data-stu-id="4c335-112">CurrencyEntity</span></span>
      - <span data-ttu-id="4c335-113">CustCustomerV3Entity</span><span class="sxs-lookup"><span data-stu-id="4c335-113">CustCustomerV3Entity</span></span>
      - <span data-ttu-id="4c335-114">DeliveryTermsEntity</span><span class="sxs-lookup"><span data-stu-id="4c335-114">DeliveryTermsEntity</span></span>
      - <span data-ttu-id="4c335-115">EcoResProductCategoryEntity</span><span class="sxs-lookup"><span data-stu-id="4c335-115">EcoResProductCategoryEntity</span></span>
      - <span data-ttu-id="4c335-116">EcoResReleasedProductV2Entity</span><span class="sxs-lookup"><span data-stu-id="4c335-116">EcoResReleasedProductV2Entity</span></span>
      - <span data-ttu-id="4c335-117">LogisticsAddressCityEntity</span><span class="sxs-lookup"><span data-stu-id="4c335-117">LogisticsAddressCityEntity</span></span>
      - <span data-ttu-id="4c335-118">LogisticsAddressCountryRegionTranslationEntity</span><span class="sxs-lookup"><span data-stu-id="4c335-118">LogisticsAddressCountryRegionTranslationEntity</span></span>
      - <span data-ttu-id="4c335-119">LogisticsAddressStateEntity</span><span class="sxs-lookup"><span data-stu-id="4c335-119">LogisticsAddressStateEntity</span></span>
      - <span data-ttu-id="4c335-120">PurchProcurementChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="4c335-120">PurchProcurementChargeCDSEntity</span></span>
      - <span data-ttu-id="4c335-121">SalesChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="4c335-121">SalesChargeCDSEntity</span></span>
      - <span data-ttu-id="4c335-122">TaxGroupEntity</span><span class="sxs-lookup"><span data-stu-id="4c335-122">TaxGroupEntity</span></span>
      - <span data-ttu-id="4c335-123">TaxItemGroupHeadingEntity</span><span class="sxs-lookup"><span data-stu-id="4c335-123">TaxItemGroupHeadingEntity</span></span>
      - <span data-ttu-id="4c335-124">VendVendorV2Entity</span><span class="sxs-lookup"><span data-stu-id="4c335-124">VendVendorV2Entity</span></span>
4. <span data-ttu-id="4c335-125">设置 Dynamics 365 Regulatory Configuration Service (RCS)。</span><span class="sxs-lookup"><span data-stu-id="4c335-125">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="4c335-126">为 Microsoft 创建服务请求以启用以下功能的外部测试：</span><span class="sxs-lookup"><span data-stu-id="4c335-126">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="4c335-127">ERCdsFeature</span><span class="sxs-lookup"><span data-stu-id="4c335-127">ERCdsFeature</span></span>
      - <span data-ttu-id="4c335-128">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="4c335-128">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="4c335-129">转到 **功能管理** 工作区，然后启用以下功能：</span><span class="sxs-lookup"><span data-stu-id="4c335-129">Go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="4c335-130">（预览）电子报告 Dataverse 数据源支持</span><span class="sxs-lookup"><span data-stu-id="4c335-130">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="4c335-131">(预览版)税务服务 Dataverse 数据源支持</span><span class="sxs-lookup"><span data-stu-id="4c335-131">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="4c335-132">(预览版)全球化功能</span><span class="sxs-lookup"><span data-stu-id="4c335-132">(Preview) Globalization features</span></span>

5. <span data-ttu-id="4c335-133">使用租户管理员帐户登录到 RCS。</span><span class="sxs-lookup"><span data-stu-id="4c335-133">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="4c335-134">转到 **电子报告** > **已连接的应用程序**。</span><span class="sxs-lookup"><span data-stu-id="4c335-134">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="4c335-135">选择 **新建** 以添加记录，然后输入以下字段信息。</span><span class="sxs-lookup"><span data-stu-id="4c335-135">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="4c335-136">在 **名称** 字段中输入名称。</span><span class="sxs-lookup"><span data-stu-id="4c335-136">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="4c335-137">在 **类型** 字段中，选择 **Dataverse**。</span><span class="sxs-lookup"><span data-stu-id="4c335-137">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="4c335-138">在 **应用程序** 字段中，输入 Dataverse URL。</span><span class="sxs-lookup"><span data-stu-id="4c335-138">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="4c335-139">在 **租户** 字段中，输入您的租户。</span><span class="sxs-lookup"><span data-stu-id="4c335-139">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="4c335-140">在 **自定义 URL** 字段中，输入您的 Dataverse URL 并向其追加“/api/data/v9.1”。</span><span class="sxs-lookup"><span data-stu-id="4c335-140">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="4c335-141">选择 **检查连接**，然后完成连接流程。</span><span class="sxs-lookup"><span data-stu-id="4c335-141">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="4c335-142">[![检查连接按钮](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="4c335-142">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="4c335-143">转到 **电子报告** > **税务配置**，然后从[税务配置](https://go.microsoft.com/fwlink/?linkid=2158352)中导入税务配置。</span><span class="sxs-lookup"><span data-stu-id="4c335-143">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="4c335-144">[![税收配置页面，税务数据模型树](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="4c335-144">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="4c335-145">如果您使用 Microsoft 配置，转到 **应纳税单据模型映射** 或 **Dataverse 模型映射**，然后在 **已连接的应用程序** 字段中，选择您在步骤 7 中创建的记录。</span><span class="sxs-lookup"><span data-stu-id="4c335-145">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="4c335-146">将 **模型映射的默认值** 设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="4c335-146">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="4c335-147">[![模型映射页面](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="4c335-147">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
