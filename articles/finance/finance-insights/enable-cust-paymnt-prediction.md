---
title: 启用客户付款预测(预览)
description: 本主题说明如何在 Finance Insights 中开启和配置客户付款预测功能。
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ae957f592ad9a1237817fec5d4172295f9a53020
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222577"
---
# <a name="enable-customer-payment-predictions-preview"></a><span data-ttu-id="ef6f4-103">启用客户付款预测(预览)</span><span class="sxs-lookup"><span data-stu-id="ef6f4-103">Enable customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="ef6f4-104">本主题说明如何在 Finance Insights 中开启和配置客户付款预测功能。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-104">This topic explains how to turn on and configure the Customer payment predictions feature in Finance insights.</span></span> <span data-ttu-id="ef6f4-105">在 **功能管理** 工作区中开启功能，然后在 **Financial insights 参数** 页中输入配置设置。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-105">You turn on the feature in the **Feature management** workspace and enter configuration settings on the **Financial insights parameters** page.</span></span> <span data-ttu-id="ef6f4-106">本主题还包括可以帮助您有效使用该功能的信息。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-106">This topic also includes information that can help you effectively use the feature.</span></span>

> [!NOTE]
> <span data-ttu-id="ef6f4-107">在完成以下步骤之前，请确保完成[配置 Finance insights](configure-for-fin-insites.md) 主题中的先决步骤。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-107">Before you complete the following steps, be sure to complete the prerequisite steps in the [Configure for Finance insights](configure-for-fin-insites.md) topic.</span></span>

1. <span data-ttu-id="ef6f4-108">按照 Microsoft Dynamics Lifecycle Services (LCS) 中环境页面内的信息连接到该环境的 Azure SQL 主实例。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-108">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="ef6f4-109">运行以下 Transact-SQL (T-SQL) 命令为沙盒环境开启外部测试版。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-109">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="ef6f4-110">（可能必须先在 LCS 中为 IP 地址开启访问权限，才能远程连接到应用程序对象服务器 \[AOS\]。）</span><span class="sxs-lookup"><span data-stu-id="ef6f4-110">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('PayPredEnableFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="ef6f4-111">如果您使用的是 10.0.20 或更高版本，或者如果您使用的是 Service Fabric 部署，请跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-111">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="ef6f4-112">Finance Insights 团队应该已经为您开启了外部测试版。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-112">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="ef6f4-113">如果在 **功能管理** 工作区中看不到此功能，或者如果在尝试打开该功能时遇到问题，请联系 <fiap@microsoft.com>。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-113">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span> 

2. <span data-ttu-id="ef6f4-114">开启客户付款见解功能：</span><span class="sxs-lookup"><span data-stu-id="ef6f4-114">Turn on the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="ef6f4-115">转到 **系统管理 \> 工作区 \> 功能管理**。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-115">Go to **System administration \> Workspaces \> Feature management**.</span></span>
    2. <span data-ttu-id="ef6f4-116">找到名称为 **客户付款见解（预览）** 的功能。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-116">Find the feature that is named **Customer payment insights (preview)**.</span></span>
    3. <span data-ttu-id="ef6f4-117">选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-117">Select **Enable now**.</span></span>

    <span data-ttu-id="ef6f4-118">现在已打开且可以配置客户付款见解功能。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-118">The Customer payment insights feature is now turned on and ready to be configured.</span></span>

3. <span data-ttu-id="ef6f4-119">配置客户付款见解功能：</span><span class="sxs-lookup"><span data-stu-id="ef6f4-119">Configure the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="ef6f4-120">转到 **信用和收款 \> 设置 \> Finance insights \> Finance insights 参数**。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-120">Go to **Credit and collections \> Setup \> Finance insights \> Finance insights parameters**.</span></span>

        <span data-ttu-id="ef6f4-121">[![配置此功能之前的“Financial insights 参数”页](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span><span class="sxs-lookup"><span data-stu-id="ef6f4-121">[![Financial insights parameters page before the feature is configured](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span></span>

    2. <span data-ttu-id="ef6f4-122">在 **Financial insights 参数** 页的 **客户付款见解** 选项卡上，选择 **查看预测模型中使用的数据字段** 链接打开 **预测模型的数据字段** 页。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-122">On the **Financial insights parameters** page, on the **Customer payment insights** tab, select the **View the data fields used in the prediction model** link to open the **Data fields for prediction model** page.</span></span> <span data-ttu-id="ef6f4-123">在那里，您可以查看用于为客户付款预测创建人工智能 (AI) 预测模型的字段的默认列表。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-123">There, you can view the default list of fields that are used to create the artificial intelligence (AI) prediction model for customer payment predictions.</span></span>

        <span data-ttu-id="ef6f4-124">要使用默认字段列表创建预测模型，请关闭 **预测模型的数据字段** 页，然后在 **Financial insights 参数** 页面上，将 **启用功能** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-124">To use the default list of fields to create the prediction model, close the **Data fields for prediction model** page, and then, on the **Financial insights parameters** page, set the **Enable feature** option to **Yes**.</span></span>

    3. <span data-ttu-id="ef6f4-125">指定“严重逾期”交易期间以定义 **严重逾期** 预测时段对您的业务的意义。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-125">Specify the "very late" transaction period to define what the **Very late** prediction bucket means for your business.</span></span>

        <span data-ttu-id="ef6f4-126">对于每个未结发票，系统将预测三个时段的付款概率：**按时**、**预期** 和 **严重逾期**。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-126">For each open invoice, the system predicts the probability of payment in three buckets: **On time**, **Late**, and **Very late**.</span></span>

        - <span data-ttu-id="ef6f4-127">**按时** – 此时段中包含预测在交易截止日期或之前支付的付款。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-127">**On time** – This bucket includes payments that are predicted to be paid on or before the transaction due date.</span></span>
        - <span data-ttu-id="ef6f4-128">**逾期** – 此时段中包含预计在交易截止日期之后，但在“严重逾期”交易期间开始之前支付的付款。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-128">**Late** – This bucket includes payments that are predicted to be paid after the transaction due date but before the start of the "very late" transaction period.</span></span>
        - <span data-ttu-id="ef6f4-129">**严重逾期** – 此时段中包含预计在“严重逾期”交易期间开始之后支付的付款。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-129">**Very late** – This bucket includes payments that are predicted to be paid after the start of the "very late" transaction period.</span></span>

        > [!NOTE]
        > <span data-ttu-id="ef6f4-130">如果更改“严重逾期”交易期间，并在创建了客户付款的 AI 预测模型之后选择 **更改逾期阈值**，将删除现有预测模型，并创建新模型。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-130">If you change the "very late" transaction period and select **Change late threshold** after the AI prediction model for customer payments has been created, the existing prediction model is deleted, and a new model is created.</span></span> <span data-ttu-id="ef6f4-131">新预测模型将根据为了定义而输入的设置把交易记录移到“严重逾期”期间。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-131">The new prediction model will move transactions into the "very late" period, based on the settings that were entered to define it.</span></span>

    4. <span data-ttu-id="ef6f4-132">定义完“严重逾期”交易期间之后，选择 **创建预测模型** 创建预测模型。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-132">After you've finished defining the "very late" transaction period, select **Create prediction model** to create the prediction model.</span></span> <span data-ttu-id="ef6f4-133">**Financial insights 参数** 页中的 **预测模型** 显示预测模型的状态。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-133">The **Prediction model** section on the **Financial insights parameters** page shows the status of the prediction model.</span></span>

        > [!NOTE]
        > <span data-ttu-id="ef6f4-134">创建预测模型期间的任何时候都可以选择 **重置模型创建** 重新开始流程。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-134">At any time while the prediction model is being created, you can select **Reset model creation** to restart the process.</span></span>

    <span data-ttu-id="ef6f4-135">该功能现已配置完毕，可以使用了。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-135">The feature has now been configured and is ready to be used.</span></span>

<span data-ttu-id="ef6f4-136">开启并配置此功能，并且预测模型已创建且正在工作之后，**Financial insights 参数** 页的 **预测模型** 部分显示模型的准确性，如下图中所示。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-136">After the feature has been turned on and configured, and the prediction model has been created and is working, the **Prediction model** section of the **Financial insights parameters** page shows the accuracy of the model, as shown in the following illustration.</span></span>

<span data-ttu-id="ef6f4-137">[![“Financial insights 参数”页的预测模型的准确性](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span><span class="sxs-lookup"><span data-stu-id="ef6f4-137">[![Accuracy of the prediction model on the Financial insights parameters page](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span></span>

## <a name="release-details"></a><span data-ttu-id="ef6f4-138">发布详细信息</span><span class="sxs-lookup"><span data-stu-id="ef6f4-138">Release details</span></span>

<span data-ttu-id="ef6f4-139">Finance insights 公开预览版可用于美国、欧洲和英国的试用部署。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-139">Finance insights public preview is available for trial deployments in the United States of America, Europe, and the United Kingdom.</span></span> <span data-ttu-id="ef6f4-140">Microsoft 将逐渐增加对更多地区的支持。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-140">Microsoft is incrementally adding support for more regions.</span></span>

<span data-ttu-id="ef6f4-141">可以并且应该仅在第 2 层沙盒环境中启用公开预览版功能。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-141">Public preview features can and should be turned on only in Tier-2 sandbox environments.</span></span> <span data-ttu-id="ef6f4-142">在沙盒环境中创建的设置和 AI 模型不能迁移到生产环境。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-142">Setup and AI models that are created in a sandbox environment can't be migrated to a production environment.</span></span> <span data-ttu-id="ef6f4-143">有关详细信息，请参阅 [Microsoft Dynamics 365 Previews 补充使用条款](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md)。</span><span class="sxs-lookup"><span data-stu-id="ef6f4-143">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
