---
title: 将固定资产重新分类
description: 若要重新划分固定资产，您必须将固定资产转移到新的固定资产组，或者将新的固定资产编号分配给同一组内的固定资产。
author: saraschi2
manager: AnnBe
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df4a2fa3c1a38519da83391bcf1c4aa38b6504ff
ms.sourcegitcommit: 6890b5a372a18e11354003098a512685e339ddb0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/14/2019
ms.locfileid: "1541189"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="94131-103">将固定资产重新分类</span><span class="sxs-lookup"><span data-stu-id="94131-103">Reclassify fixed assets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="94131-104">若要重新划分固定资产，您必须将固定资产转移到新的固定资产组，或者将新的固定资产编号分配给同一组内的固定资产。</span><span class="sxs-lookup"><span data-stu-id="94131-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="94131-105">为某件固定资产重新分类时：</span><span class="sxs-lookup"><span data-stu-id="94131-105">When a fixed asset is reclassified:</span></span>

<span data-ttu-id="94131-106">• 为新的固定资产创建现有固定资产的所有帐簿。</span><span class="sxs-lookup"><span data-stu-id="94131-106">• All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="94131-107">为原始固定资产设置的所有信息都复制到新的固定资产。</span><span class="sxs-lookup"><span data-stu-id="94131-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="94131-108">原始固定资产的帐簿的状态为“已结算”。</span><span class="sxs-lookup"><span data-stu-id="94131-108">The status of the books for the original fixed asset is Closed.</span></span> 

<span data-ttu-id="94131-109">• 新固定资产的新帐簿将在**购置日期**字段中包含重新分类的日期。</span><span class="sxs-lookup"><span data-stu-id="94131-109">• The new books of the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="94131-110">**折旧开始日期**字段中的日期从原始资产信息复制。</span><span class="sxs-lookup"><span data-stu-id="94131-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="94131-111">如果已开始折旧，则**最近计提折旧日期**字段将显示重新分类的日期。</span><span class="sxs-lookup"><span data-stu-id="94131-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

<span data-ttu-id="94131-112">• 为新的固定资产，取消和生成原始固定资产的现有固定资产交易记录。</span><span class="sxs-lookup"><span data-stu-id="94131-112">• The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

<span data-ttu-id="94131-113">请执行以下步骤为固定资产重新分类：</span><span class="sxs-lookup"><span data-stu-id="94131-113">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="94131-114">转到**固定资产 > 定期任务 > 重新分类**。</span><span class="sxs-lookup"><span data-stu-id="94131-114">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="94131-115">在**固定资产组**字段中，选择要重新分类的组。</span><span class="sxs-lookup"><span data-stu-id="94131-115">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="94131-116">在**固定资产编号**字段中，选择要重新分类的固定资产。</span><span class="sxs-lookup"><span data-stu-id="94131-116">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="94131-117">在**新的固定资产组**字段中，选择要将固定资产转移到的组。</span><span class="sxs-lookup"><span data-stu-id="94131-117">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="94131-118">如果新固定资产组附加到编号规则，使用来自新固定资产组的编号规则的编号更新**新增固定资产的编号**字段。</span><span class="sxs-lookup"><span data-stu-id="94131-118">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="94131-119">否则，使用来自**固定资产参数**页面中设置的编号规则的编号更新**新增固定资产的编号**字段。</span><span class="sxs-lookup"><span data-stu-id="94131-119">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="94131-120">如果未在**固定资产参数**页面中设置编号规则，请在**新增固定资产的编号**字段中输入编号。</span><span class="sxs-lookup"><span data-stu-id="94131-120">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="94131-121">在**重新分类日期**字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="94131-121">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="94131-122">在**凭证系列**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="94131-122">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="94131-123">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="94131-123">Click **OK**.</span></span>
