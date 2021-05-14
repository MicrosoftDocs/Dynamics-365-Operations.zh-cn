---
title: 将固定资产重新分类
description: 若要重新划分固定资产，您必须将固定资产转移到新的固定资产组，或者将新的固定资产编号分配给同一组内的固定资产。
author: saraschi2
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fbfb754459fad1f3b1509f4f9c65c20e0385b013
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944702"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="3f6e2-103">将固定资产重新分类</span><span class="sxs-lookup"><span data-stu-id="3f6e2-103">Reclassify fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3f6e2-104">若要重新划分固定资产，您必须将固定资产转移到新的固定资产组，或者将新的固定资产编号分配给同一组内的固定资产。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="3f6e2-105">为某件固定资产重新分类时：</span><span class="sxs-lookup"><span data-stu-id="3f6e2-105">When a fixed asset is reclassified:</span></span>

- <span data-ttu-id="3f6e2-106">为新的固定资产创建现有固定资产的所有帐簿。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-106">All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="3f6e2-107">为原始固定资产设置的所有信息都复制到新的固定资产。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="3f6e2-108">原始固定资产的帐簿的状态为“已结算”。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-108">The status of the books for the original fixed asset is Closed.</span></span> 

- <span data-ttu-id="3f6e2-109">新固定资产的新帐簿将在 **购置日期** 字段中包含重新分类的日期。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-109">The new books for the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="3f6e2-110">**折旧开始日期** 字段中的日期从原始资产信息复制。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="3f6e2-111">如果已开始折旧，则 **最近计提折旧日期** 字段将显示重新分类的日期。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

- <span data-ttu-id="3f6e2-112">为新的固定资产，取消和生成原始固定资产的现有固定资产交易记录。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-112">The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

- <span data-ttu-id="3f6e2-113">重新分类具有转移交易的资产后，系统将在 **操作中心** 显示一条消息，指示在重新分类流程中转移交易未完成。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-113">When an asset that has a transfer transaction has been reclassified, the system will display a message in the **Action center** to indicate that a transfer transaction wasn't completed during the reclassification process.</span></span> <span data-ttu-id="3f6e2-114">必须完成转移交易，才能将现有的重新分类交易转移到适当的财务维度。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-114">It's necessary to complete a transfer transaction to move the existing reclassification transactions to the appropriate financial dimensions.</span></span> 

   <span data-ttu-id="3f6e2-115">在重新分类流程中，系统将运行以下操作来将资产余额从原始资产重新分类为新资产。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-115">During the reclassification process, the system runs the following actions to reclassify the asset balance from the original asset to the new asset.</span></span> 
   
   - <span data-ttu-id="3f6e2-116">重新分类流程将数据从原始固定资产帐簿复制到新固定资产帐簿。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-116">The reclassification process copies the data from the original fixed asset book to the new fixed asset book.</span></span>

   - <span data-ttu-id="3f6e2-117">重新分类交易使用原始的已过帐购置中的信息，其中包括购置交易中包含的财务维度信息。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-117">The reclassification transaction uses information from the original posted acquisition that includes financial dimension information that is included in the acquisition transaction.</span></span>  
   
   - <span data-ttu-id="3f6e2-118">同时，重新分类流程将冲销原始资产购置和资产转移交易。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-118">At the same time, the reclassification process reverses the original asset acquisition and asset transfer transaction.</span></span> 

<span data-ttu-id="3f6e2-119">下图和过程提供了重新分类流程的示例。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-119">The following diagram and procedure provide an example of the reclassification process.</span></span> 

<span data-ttu-id="3f6e2-120">[![显示重新分类流程的图](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)</span><span class="sxs-lookup"><span data-stu-id="3f6e2-120">[![Diagram showing the reclassicification process](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)</span></span>

<span data-ttu-id="3f6e2-121">请执行以下步骤为固定资产重新分类：</span><span class="sxs-lookup"><span data-stu-id="3f6e2-121">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="3f6e2-122">转到 **固定资产 > 定期任务 > 重新分类**。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-122">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="3f6e2-123">在 **固定资产组** 字段中，选择要重新分类的组。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-123">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="3f6e2-124">在 **固定资产编号** 字段中，选择要重新分类的固定资产。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-124">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="3f6e2-125">在 **新的固定资产组** 字段中，选择要将固定资产转移到的组。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-125">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="3f6e2-126">如果新固定资产组附加到编号规则，使用来自新固定资产组的编号规则的编号更新 **新增固定资产的编号** 字段。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-126">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="3f6e2-127">否则，使用来自 **固定资产参数** 页面中设置的编号规则的编号更新 **新增固定资产的编号** 字段。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-127">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="3f6e2-128">如果未在 **固定资产参数** 页面中设置编号规则，请在 **新增固定资产的编号** 字段中输入编号。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-128">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="3f6e2-129">在 **重新分类日期** 字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-129">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="3f6e2-130">在 **凭证系列** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-130">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="3f6e2-131">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="3f6e2-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
