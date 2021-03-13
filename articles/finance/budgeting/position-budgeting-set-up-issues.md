---
title: 职位预算编制疑难解答
description: 本文提供对配置职位预算时可能有的问题的解答。 其定位关于如何创建预算成本要素、薪酬组和薪酬网格的常见问题。
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: roschlom
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8211c5bd4514bffbd001f9930859f777dac7f0e1
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017609"
---
# <a name="position-budgeting-troubleshooting"></a><span data-ttu-id="4d055-104">职位预算编制疑难解答</span><span class="sxs-lookup"><span data-stu-id="4d055-104">Position budgeting troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d055-105">本文提供对配置职位预算时可能有的问题的解答。</span><span class="sxs-lookup"><span data-stu-id="4d055-105">This article provides answers to questions that you might have when you configure position budgeting.</span></span> <span data-ttu-id="4d055-106">其定位关于如何创建预算成本要素、薪酬组和薪酬网格的常见问题。</span><span class="sxs-lookup"><span data-stu-id="4d055-106">It addresses frequently asked questions about how to create budget cost elements, compensation groups, and compensation grids.</span></span> 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a><span data-ttu-id="4d055-107">为什么找不到人力资源中的预测职位页？</span><span class="sxs-lookup"><span data-stu-id="4d055-107">Why can’t I find the forecast position page in Human resources?</span></span>
---------------------------------------------------------------

<span data-ttu-id="4d055-108">预测职位已移动到“预算”。</span><span class="sxs-lookup"><span data-stu-id="4d055-108">Forecast positions have been moved to Budgeting.</span></span>

## <a name="why-cant-i-delete-a-budget-cost-element"></a><span data-ttu-id="4d055-109">为什么无法删除预算成本要素？</span><span class="sxs-lookup"><span data-stu-id="4d055-109">Why can’t I delete a budget cost element?</span></span>
<span data-ttu-id="4d055-110">您不能删除分配给预测职位的预算成本要素。</span><span class="sxs-lookup"><span data-stu-id="4d055-110">You can’t delete a budget cost element that is assigned to a forecast position.</span></span> <span data-ttu-id="4d055-111">您必须从所有预测职位中移除预算成本元素，然后才可将其删除。</span><span class="sxs-lookup"><span data-stu-id="4d055-111">Before you can delete a budget cost element, you must remove it from all forecast positions.</span></span> <span data-ttu-id="4d055-112">**提示：** 若要查找预算成本分配到的所有职位，请在 **预算成本元素** 页上选择成本元素，然后单击 **更新职位**。</span><span class="sxs-lookup"><span data-stu-id="4d055-112">**Tip:** To find all the positions that a budget cost element is assigned to, select the cost element on the **Budget cost elements** page, and then click **Update positions**.</span></span> <span data-ttu-id="4d055-113">上部网格中列出使用成本要素的职位。</span><span class="sxs-lookup"><span data-stu-id="4d055-113">The positions that use the cost element are listed in the upper grid.</span></span>

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a><span data-ttu-id="4d055-114">我如何在不打开每个职位的情况下从多个预测职位中删除成本元素？</span><span class="sxs-lookup"><span data-stu-id="4d055-114">How can I remove a cost element from multiple forecast positions without opening each one?</span></span>
<span data-ttu-id="4d055-115">您不能删除成本元素。</span><span class="sxs-lookup"><span data-stu-id="4d055-115">You can’t remove a cost element.</span></span> <span data-ttu-id="4d055-116">但是如果您更改开始日期和结束日期，以便这些日期在预算计划周期日期之外，成本元素将不再分配给该预算预测计划周期中的预测职位。</span><span class="sxs-lookup"><span data-stu-id="4d055-116">However, if you change the start and end dates so that they are outside the budget planning cycle dates, the cost element will no longer be assigned to the forecast positions in that budget planning cycle.</span></span> <span data-ttu-id="4d055-117">若要进行此更改，打开预算成本元素，然后在 **成本计算** 快速选项卡上，单击 **更改日期**，然后更改生效日期或到期日期。</span><span class="sxs-lookup"><span data-stu-id="4d055-117">To make this change, open the budget cost element, and then, on the **Cost calculation** FastTab, click **Change dates**, and change the effective date or expiration date.</span></span> <span data-ttu-id="4d055-118">然后单击 **确定** 自动更新成本元素分配到的所有预测职位。</span><span class="sxs-lookup"><span data-stu-id="4d055-118">Then click **OK** to automatically update all forecast positions that the cost element is assigned to.</span></span> <span data-ttu-id="4d055-119">**提示：** 如果您使用此方法，请注意其将从该开始日期和结束日期不再在相应范围内的 **所有** 预测职位中删除预算成本元素。</span><span class="sxs-lookup"><span data-stu-id="4d055-119">**Tip:** If you use this method, be aware that it removes the budget cost element from **all** forecast positions where the start and end dates are no longer within the appropriate range.</span></span> <span data-ttu-id="4d055-120">如果这不是您期望的效果，则必须打开每个希望从中删除预算成本元素的预测职位，并手动进行更改。</span><span class="sxs-lookup"><span data-stu-id="4d055-120">If this effect isn't what you intend, you must open each forecast position that you want to remove the budget cost element from and manually make the change.</span></span>

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a><span data-ttu-id="4d055-121">为什么在预算成本元素的“成本计算”快速选项卡中无法输入年度金额？</span><span class="sxs-lookup"><span data-stu-id="4d055-121">Why can’t I enter an annual amount on the Cost calculation FastTab for the budget cost element?</span></span>
<span data-ttu-id="4d055-122">如果 **计算基础** 快速选项卡上有预算成本元素，则您不能输入年度金额，因为，系统需要百分比来计算该值。</span><span class="sxs-lookup"><span data-stu-id="4d055-122">You can’t enter an annual amount if there are budget cost elements on the **Calculation basis** FastTab, because the system requires a percentage in order to calculate the value.</span></span> <span data-ttu-id="4d055-123">若要更改此值，从 **计算基础** 快速选项卡删除所有预算成本元素。</span><span class="sxs-lookup"><span data-stu-id="4d055-123">To change the value, remove all budget cost elements from the **Calculation basis** FastTab.</span></span>

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a><span data-ttu-id="4d055-124">为什么不能将预算成本类型从收入更改为其他预算成本类型？</span><span class="sxs-lookup"><span data-stu-id="4d055-124">Why can’t I change the budget cost type from earning to another budget cost type?</span></span>
<span data-ttu-id="4d055-125">某些预算成本要素使用收入成本要素作为计算基础。</span><span class="sxs-lookup"><span data-stu-id="4d055-125">Some budget cost elements use the earning cost element as a calculation basis.</span></span> <span data-ttu-id="4d055-126">若要更改 **预算成本类型** 字段，从所有预算成本元素的 **计算基础** 快速选项卡删除收入成本元素。</span><span class="sxs-lookup"><span data-stu-id="4d055-126">To change the **Budget cost type** field, remove the earning cost element from the **Calculation basis** FastTab of all budget cost elements.</span></span>

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a><span data-ttu-id="4d055-127">为什么无法更改某个预算成本要素的预算成本元素行上的日期？</span><span class="sxs-lookup"><span data-stu-id="4d055-127">Why can’t I change the date on budget cost element lines for a budget cost element?</span></span>
<span data-ttu-id="4d055-128">当预测职位使用某个预算成本元素时，无法更改预算成本元素行中的日期。</span><span class="sxs-lookup"><span data-stu-id="4d055-128">You can’t change the date on the budget cost element line when a budget cost element is used by a forecast position.</span></span> <span data-ttu-id="4d055-129">此限制帮助确保预测职位始终在预算成本元素的准则内。</span><span class="sxs-lookup"><span data-stu-id="4d055-129">This limitation helps guarantee that the forecast positions are always within the guidelines of the budget cost element.</span></span> <span data-ttu-id="4d055-130">若要更改该日期，在 **成本计算** 快速选项卡上，单击 **更改日期** 并输入新日期。</span><span class="sxs-lookup"><span data-stu-id="4d055-130">To change the date, on the **Cost calculation** FastTab, click **Change dates**, and enter the new dates.</span></span> <span data-ttu-id="4d055-131">然后单击 **确定** 更新成本元素分配到的职位。</span><span class="sxs-lookup"><span data-stu-id="4d055-131">Then click **OK** to update the positions that the cost element is assigned to.</span></span>

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a><span data-ttu-id="4d055-132">为什么无法更改薪酬组页中的预算成本元素的成本？</span><span class="sxs-lookup"><span data-stu-id="4d055-132">Why can’t I change the costs for a budget cost element on the Compensation group page?</span></span>
<span data-ttu-id="4d055-133">您只可以在 **预算成本元素** 页上创建和更改预算成本元素。</span><span class="sxs-lookup"><span data-stu-id="4d055-133">You can create and change budget cost elements only on the **Budget cost elements** page.</span></span>

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a><span data-ttu-id="4d055-134">当为预测职位的成本元素更改日期时为什么会收到错误消息？</span><span class="sxs-lookup"><span data-stu-id="4d055-134">Why do I receive an error message when I change the dates for a cost element on a forecast position?</span></span>
<span data-ttu-id="4d055-135">预测职位成本要素行中的日期必须属于以下范围：</span><span class="sxs-lookup"><span data-stu-id="4d055-135">The dates on the forecast position cost element line must be within the following ranges:</span></span>

-   <span data-ttu-id="4d055-136">职位的激活和报废日期。</span><span class="sxs-lookup"><span data-stu-id="4d055-136">The activation and retirement dates of the position.</span></span>
-   <span data-ttu-id="4d055-137">预算成本要素的激活日期和到期日期。</span><span class="sxs-lookup"><span data-stu-id="4d055-137">The activation and expiration dates of the budget cost element.</span></span>
-   <span data-ttu-id="4d055-138">与预测职位的预算计划流程相关的预算周期的开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="4d055-138">The start and end dates of the budget cycle that is associated with the budget planning process of the forecast position.</span></span>




