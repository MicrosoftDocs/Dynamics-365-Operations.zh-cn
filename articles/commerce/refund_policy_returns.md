---
title: 为渠道创建和更新退货和退款政策
description: 本主题说明了如何为渠道设置退货和退款政策。
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: 89e8fe78414e73053317ebe19e3afcc89231d440
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979695"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a><span data-ttu-id="68d76-103">为渠道创建和更新退货和退款政策</span><span class="sxs-lookup"><span data-stu-id="68d76-103">Create and update a returns and refunds policy for a channel</span></span>

[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="68d76-104">概览</span><span class="sxs-lookup"><span data-stu-id="68d76-104">Overview</span></span>

<span data-ttu-id="68d76-105">利用 Dynamics 365 Commerce 中的渠道退货政策，零售商能够就使用哪些支付方式在销售点 (POS) 设备上处理退货设置强制措施。</span><span class="sxs-lookup"><span data-stu-id="68d76-105">The channel return policy in Dynamics 365 Commerce enables retailers to set enforcements on which payment tenders can be allowed for processing a return on a point of sale (POS) device.</span></span>  

<span data-ttu-id="68d76-106">本主题描述了为渠道设置退货和退款政策的步骤。</span><span class="sxs-lookup"><span data-stu-id="68d76-106">This topic describes the steps to set up a returns and refunds policy for a channel.</span></span>

<span data-ttu-id="68d76-107">目前，该政策的范围仅限于设置可以允许渠道使用的付款方式。</span><span class="sxs-lookup"><span data-stu-id="68d76-107">The scope of the policy is currently limited to setting the payment tenders that can be allowed for a channel.</span></span> <span data-ttu-id="68d76-108">“允许”列表基于用于进行购买的付款方式。</span><span class="sxs-lookup"><span data-stu-id="68d76-108">The "allowed" list is based on the payment methods used to make the purchase.</span></span> <span data-ttu-id="68d76-109">例如:</span><span class="sxs-lookup"><span data-stu-id="68d76-109">For example:</span></span>

- <span data-ttu-id="68d76-110">如果使用礼品卡进行购买，则商店政策是仅对新礼品卡处理退款或提供商店信用。</span><span class="sxs-lookup"><span data-stu-id="68d76-110">If a purchase was made using a gift card, the store policy is to process refunds only to a new gift card or to give store credit.</span></span> 
- <span data-ttu-id="68d76-111">如果使用现金进行销售，则退款可以使用的选项包括现金、礼品卡和客户帐户，而不是信用卡。</span><span class="sxs-lookup"><span data-stu-id="68d76-111">If a sale is made using cash, the options allowed for refund are cash, gift card, and customer account, but not credit card.</span></span> 


## <a name="enable-return-policy"></a><span data-ttu-id="68d76-112">启用退货政策</span><span class="sxs-lookup"><span data-stu-id="68d76-112">Enable return policy</span></span>

<span data-ttu-id="68d76-113">要启用渠道退货政策功能，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="68d76-113">To enable the channel return policy functionality, do the following:</span></span>

1. <span data-ttu-id="68d76-114">转到 Dynamics 365 Commerce 中的 **功能管理** 工作区。</span><span class="sxs-lookup"><span data-stu-id="68d76-114">Go to the **Feature Management** workspace in Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="68d76-115">在功能名称列表中搜索 **启用渠道退货政策** 功能。</span><span class="sxs-lookup"><span data-stu-id="68d76-115">Search for the **Enable channel return policies** feature in the list of feature names.</span></span>
3. <span data-ttu-id="68d76-116">选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="68d76-116">Select **Enable now**.</span></span> 

## <a name="configure-return-policy"></a><span data-ttu-id="68d76-117">配置退货政策</span><span class="sxs-lookup"><span data-stu-id="68d76-117">Configure return policy</span></span>

<span data-ttu-id="68d76-118">请按照以下步骤配置零售商店或在线零售渠道的退货政策。</span><span class="sxs-lookup"><span data-stu-id="68d76-118">Follow these steps to configure a return policy for a retail store or online retail channel.</span></span>

1. <span data-ttu-id="68d76-119">转到 **Retail 和 Commerce** \>**频道设置** \> **退货** \> **渠道退货政策**。</span><span class="sxs-lookup"><span data-stu-id="68d76-119">Go to **Retail and Commerce** \> **Channel Setup** \> **Returns** \> **Channel return policy**.</span></span>

2. <span data-ttu-id="68d76-120">选择 **新建** 以创建新的退货政策模板。</span><span class="sxs-lookup"><span data-stu-id="68d76-120">Select **New** to create a new return policy template.</span></span> <span data-ttu-id="68d76-121">若要使用现有模板，请在左窗格中选择模板。</span><span class="sxs-lookup"><span data-stu-id="68d76-121">To use an existing template, select the template in the left pane.</span></span> <span data-ttu-id="68d76-122">对于新模板，请添加名称和描述，以帮助您将政策应用于渠道时识别该政策。</span><span class="sxs-lookup"><span data-stu-id="68d76-122">For new templates, add a name and description that will help you identify the policy when it is being applied to the channel.</span></span>

   <span data-ttu-id="68d76-123">![添加新退货政策](media/Return-policy-page1.png "添加新退货政策")</span><span class="sxs-lookup"><span data-stu-id="68d76-123">![Add new return policy](media/Return-policy-page1.png "Add new return rolicy")</span></span>
     
   
3. <span data-ttu-id="68d76-124">在 **允许的退款付款方式** 部分中，定义特定于每种付款方式的 **已允许** 退货付款方式。</span><span class="sxs-lookup"><span data-stu-id="68d76-124">In the **Allowed refund payment methods** section, define **Allowed** return payment tenders that are specific to each payment method.</span></span>
   <span data-ttu-id="68d76-125">![添加付款方式](media/Return-policy-page2.PNG "设置每种付款类型允许的付款方式")</span><span class="sxs-lookup"><span data-stu-id="68d76-125">![Add payment methods](media/Return-policy-page2.PNG "Set allowed payment methods per payment type")</span></span>
   
    > [!IMPORTANT]
    > - <span data-ttu-id="68d76-126">付款方式源自为组织设置的付款方式。</span><span class="sxs-lookup"><span data-stu-id="68d76-126">The payment methods are derived from the payment methods set for the organization.</span></span>
    > - <span data-ttu-id="68d76-127">为每种列出的付款方式添加允许的退货支付方式将确保可以针对允许的退货支付方式进行退货。</span><span class="sxs-lookup"><span data-stu-id="68d76-127">Adding an allowed return tender type for each listed payment method will ensure that returns can be made to the allowed return tender type.</span></span>
    
4. <span data-ttu-id="68d76-128">将退货政策模板与其使用商店关联。</span><span class="sxs-lookup"><span data-stu-id="68d76-128">Associate the return policy template with the stores where it will be used.</span></span> <span data-ttu-id="68d76-129">选择 **零售渠道** 选项卡中的 **添加** 选项卡并关联可用渠道。</span><span class="sxs-lookup"><span data-stu-id="68d76-129">Select **Add** in the **Retail Channels** tab and associate the available channels.</span></span> 

    - <span data-ttu-id="68d76-130">在 **选择组织节点** 对话框中，选择应与模板关联的商店、地区和组织。</span><span class="sxs-lookup"><span data-stu-id="68d76-130">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>
    - <span data-ttu-id="68d76-131">只能为每个商店关联一个退货政策模板。</span><span class="sxs-lookup"><span data-stu-id="68d76-131">Only one return policy template can be associated with each store.</span></span>
    - <span data-ttu-id="68d76-132">使用箭头按钮选择商店、地区或组织。</span><span class="sxs-lookup"><span data-stu-id="68d76-132">Use the arrow buttons to select stores, regions, or organizations.</span></span>
    - <span data-ttu-id="68d76-133">政策生效日期将是将政策应用于渠道并运行渠道作业的日期。</span><span class="sxs-lookup"><span data-stu-id="68d76-133">The effective date on the policy will be the date on which the policies are applied to the channels and the channel jobs are run.</span></span> 

    <span data-ttu-id="68d76-134">![选择组织节点对话框](media/Return-policy-page3.PNG "选择组织节点对话框")</span><span class="sxs-lookup"><span data-stu-id="68d76-134">![Choose organization nodes dialog box](media/Return-policy-page3.PNG "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="68d76-135">在 **配送计划** 页面上，运行 **1070** 作业以使渠道退货政策可用于 POS。</span><span class="sxs-lookup"><span data-stu-id="68d76-135">On the **Distribution schedule** page, run the **1070** job to make the channel return policy available to the POS.</span></span>

## <a name="preview-the-channel-return-policy-in-the-pos"></a><span data-ttu-id="68d76-136">预览 POS 中的渠道退货政策</span><span class="sxs-lookup"><span data-stu-id="68d76-136">Preview the channel return policy in the POS</span></span>

<span data-ttu-id="68d76-137">请按照以下任一示例中的步骤操作，以查看 POS 中允许使用的退货支付方式。</span><span class="sxs-lookup"><span data-stu-id="68d76-137">Follow the steps in either of the following examples to view the allowed return tender types in POS.</span></span>

1. <span data-ttu-id="68d76-138">以收银员或经理身份登录到 POS。</span><span class="sxs-lookup"><span data-stu-id="68d76-138">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="68d76-139">在 **班次和银箱** 下面，选择 **显示日记帐**。</span><span class="sxs-lookup"><span data-stu-id="68d76-139">Under **Shift and Drawer**, select **Show journal**.</span></span>
3. <span data-ttu-id="68d76-140">选择属于退货的交易记录。</span><span class="sxs-lookup"><span data-stu-id="68d76-140">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="68d76-141">选择要退款的商品，然后选择付款方式。</span><span class="sxs-lookup"><span data-stu-id="68d76-141">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="68d76-142">如果所选的付款方式在允许的退货支付方式列表中，则出纳员可以完成交易。</span><span class="sxs-lookup"><span data-stu-id="68d76-142">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="68d76-143">如果不允许使用所选的付款方式，则会显示错误消息。</span><span class="sxs-lookup"><span data-stu-id="68d76-143">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="68d76-144">选择 **应付金额** 以显示所有允许的退货支付方式的列表。</span><span class="sxs-lookup"><span data-stu-id="68d76-144">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="68d76-145">- 或者 -</span><span class="sxs-lookup"><span data-stu-id="68d76-145">-or-</span></span>

1. <span data-ttu-id="68d76-146">以收银员或经理身份登录到 POS。</span><span class="sxs-lookup"><span data-stu-id="68d76-146">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="68d76-147">选择 **退货交易**，然后通过条形码扫描或手动输入来输入收据 ID。</span><span class="sxs-lookup"><span data-stu-id="68d76-147">Select **Return Transaction** and enter the receipt ID using a barcode scan or by manual entry.</span></span> 
3. <span data-ttu-id="68d76-148">选择属于退货的交易记录。</span><span class="sxs-lookup"><span data-stu-id="68d76-148">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="68d76-149">选择要退款的商品，然后选择付款方式。</span><span class="sxs-lookup"><span data-stu-id="68d76-149">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="68d76-150">如果所选的付款方式在允许的退货支付方式列表中，则出纳员可以完成交易。</span><span class="sxs-lookup"><span data-stu-id="68d76-150">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="68d76-151">如果不允许使用所选的付款方式，则会显示错误消息。</span><span class="sxs-lookup"><span data-stu-id="68d76-151">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="68d76-152">选择 **应付金额** 以显示所有允许的退货支付方式的列表。</span><span class="sxs-lookup"><span data-stu-id="68d76-152">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="68d76-153">![不允许退款](media/Return-policy-page6.png "不允许的退款类型")</span><span class="sxs-lookup"><span data-stu-id="68d76-153">![Refund not allowed](media/Return-policy-page6.png "Refund type not allowed")</span></span>



<span data-ttu-id="68d76-154">![付款方式列表](media/Return-policy-page5.PNG "允许的退款类型")</span><span class="sxs-lookup"><span data-stu-id="68d76-154">![List of payment methods](media/Return-policy-page5.PNG "Refund types allowed")</span></span>
