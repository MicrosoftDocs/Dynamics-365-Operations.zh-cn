---
title: 启用现金流预测（预览）
description: 本主题说明如何在 Finance Insights 中开启现金流预测功能。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 1977dac4a3ab66cca2248dc0124d3a06d6963f40
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978756"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="e99e8-103">启用现金流预测（预览）</span><span class="sxs-lookup"><span data-stu-id="e99e8-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="e99e8-104">本主题说明如何在 Finance Insights 中开启现金流预测功能。</span><span class="sxs-lookup"><span data-stu-id="e99e8-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="e99e8-105">若要在现金流中使用付款预测，您必须按照[启用客户付款预测](enable-cust-paymnt-prediction.md)中的说明设置客户付款预测功能。</span><span class="sxs-lookup"><span data-stu-id="e99e8-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="e99e8-106">按照 Microsoft Dynamics Lifecycle Services (LCS) 中环境页面内的信息连接到该环境的 Azure SQL 主实例。</span><span class="sxs-lookup"><span data-stu-id="e99e8-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="e99e8-107">运行以下 Transact-SQL (T-SQL) 命令为沙盒环境开启外部测试版。</span><span class="sxs-lookup"><span data-stu-id="e99e8-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="e99e8-108">（可能必须先在 LCS 中为 IP 地址开启访问权限，才能远程连接到应用程序对象服务器 \[AOS\]。）</span><span class="sxs-lookup"><span data-stu-id="e99e8-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="e99e8-109">如果您的 Microsoft Dynamics 365 Finance 部署是 Service Fabric 部署，则可跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="e99e8-109">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="e99e8-110">Finance Insights 团队应该已经为您开启了外部测试版。</span><span class="sxs-lookup"><span data-stu-id="e99e8-110">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="e99e8-111">如果在 **功能管理** 工作区中看不到此功能，或者如果尝试打开该功能时遇到此问题，请联系 <fiap@microsoft.com>。</span><span class="sxs-lookup"><span data-stu-id="e99e8-111">If you don't see the features in the **Feature management** workspace, or if experience issues when you try to turn them on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="e99e8-112">打开 **功能管理** 工作区，然后执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="e99e8-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="e99e8-113">选择 **检查更新**。</span><span class="sxs-lookup"><span data-stu-id="e99e8-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="e99e8-114">开启以下功能：</span><span class="sxs-lookup"><span data-stu-id="e99e8-114">Turn on the following features:</span></span>

        - <span data-ttu-id="e99e8-115">新建网格控件</span><span class="sxs-lookup"><span data-stu-id="e99e8-115">New grid control</span></span>
        - <span data-ttu-id="e99e8-116">在网格中分组（预览）</span><span class="sxs-lookup"><span data-stu-id="e99e8-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="e99e8-117">客户付款预测(预览版)</span><span class="sxs-lookup"><span data-stu-id="e99e8-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="e99e8-118">现金流量预测(预览版)</span><span class="sxs-lookup"><span data-stu-id="e99e8-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="e99e8-119">转到 **现金和银行管理 \> 现金流与预测设置**，然后添加预测中应该包含的流动性科目。</span><span class="sxs-lookup"><span data-stu-id="e99e8-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e99e8-120">如果未设置流动性科目，则无法产生现金流。</span><span class="sxs-lookup"><span data-stu-id="e99e8-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="e99e8-121">转到 **现金和银行管理 \> 设置 \> Finance Insights（预览）\> 现金流预测（预览）**，然后执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="e99e8-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="e99e8-122">在 **现金流预测** 选项卡上，选择 **启用功能**。</span><span class="sxs-lookup"><span data-stu-id="e99e8-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="e99e8-123">选择 **创建预测模型**。</span><span class="sxs-lookup"><span data-stu-id="e99e8-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="e99e8-124">有关现金流预测功能的详细信息，请参阅[现金流预测](cash-flow-forecast-intro.md)。</span><span class="sxs-lookup"><span data-stu-id="e99e8-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="e99e8-125">隐私声明</span><span class="sxs-lookup"><span data-stu-id="e99e8-125">Privacy notice</span></span>

<span data-ttu-id="e99e8-126">预览版 (1) 采用的隐私和安全措施可能比 Dynamics 365 Finance and Operations 服务少，(2) 不包含在该服务的服务级别协议 (SLA) 中，(3) 不应用于处理应遵守法律或法规合规性要求的个人数据或其他数据，以及 (4) 享受有限支持。</span><span class="sxs-lookup"><span data-stu-id="e99e8-126">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
