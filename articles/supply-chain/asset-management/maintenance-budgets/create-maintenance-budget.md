---
title: 创建维护预算
description: 本主题说明如何在资产管理中创建维护预算。
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetBudgetLineAdjust, EntAssetBudget, EntAssetBudgetRecalc, EntAssetBudgetCopy, EntAssetBudgetLine, EntAssetBudgetCreate, EntAssetBudgetApprove, EntAssetBudgetCalculateActualCost
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b91b398c4ef864a92a5318b7e80f71a5a572844e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836750"
---
# <a name="create-maintenance-budgets"></a><span data-ttu-id="3ebe5-103">创建维护预算</span><span class="sxs-lookup"><span data-stu-id="3ebe5-103">Create maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 



<span data-ttu-id="3ebe5-104">维护预算用于创建预防性维护的预计成本概览。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-104">Maintenance budgets are used to provide an overview of expected costs for preventive maintenance.</span></span> <span data-ttu-id="3ebe5-105">预算行基于预计开始日期在预算期间内的维护安排行计算。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-105">Budget lines are calculated based on maintenance schedule lines that have an expected start date during the budget period.</span></span>

<span data-ttu-id="3ebe5-106">维护预算基于资产管理中使用的成本类型：**预防性**、**纠正** 和 **投资**。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-106">Maintenance budgets are based on the cost types that are used in Asset Management: **Preventive**, **Corrective**, and **Investment**.</span></span> <span data-ttu-id="3ebe5-107">将包括其更换日期在预算期间内且具有关联的更换值的有效资产的投资维护预算成本。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-107">Budget costs for investment maintenance are included for active assets that have a replacement date during the budget period and a related replacement value.</span></span> <span data-ttu-id="3ebe5-108">如果预算计算中包括过去的纠正日期，则包括纠正维护的预算成本。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-108">Budget costs for corrective maintenance are included if a past corrective date is included in the budget calculation.</span></span> <span data-ttu-id="3ebe5-109">在此情况下，将为要计算的维护成本的相同将来期间计算早期期间的纠正成本。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-109">In that case, corrective costs from an earlier period are calculated for the same future period that you calculate the maintenance budget for.</span></span>

## <a name="create-a-maintenance-budget"></a><span data-ttu-id="3ebe5-110">创建维护预算</span><span class="sxs-lookup"><span data-stu-id="3ebe5-110">Create a maintenance budget</span></span>

1. <span data-ttu-id="3ebe5-111">选择 **资产管理** \> **查询**\> **维护预算**\> **预算**。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-111">Select **Asset management** \> **Inquiries** \> **Maintenance budget** \> **Budget**.</span></span>
2. <span data-ttu-id="3ebe5-112">选择 **创建预算**。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-112">Select **Create budget**.</span></span>
3. <span data-ttu-id="3ebe5-113">在 **维护预算** 字段中，输入预算 ID。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-113">In the **Maintenance budget** field, enter a budget ID.</span></span>
4. <span data-ttu-id="3ebe5-114">在 **描述** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-114">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="3ebe5-115">在 **期间** 快速选项卡上的 **开始日期** 和 **结束日期** 字段中，输入预算期间的开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-115">On the **Period** FastTab, in the **From date** and **To date** fields, enter the start and end dates of the budget period.</span></span>
5. <span data-ttu-id="3ebe5-116">若要包括以之前期间的实际成本为基础进行计算的纠正预算成本，请在 **纠正开始日期** 字段中输入应包括这些成本的期间的开始日期。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-116">To include corrective budget costs that are calculated on the basis of actual costs from a previous period, in the **Corrective from date** field, enter the start date of the period that those costs should be included from.</span></span>
6. <span data-ttu-id="3ebe5-117">根据预算中需要的详细程度，设置五个 **分组依据** 快速选项卡上的相关选项。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-117">Depending on the level of detail that is required in the budget, set the relevant options on the five **Group by** FastTabs.</span></span>
7. <span data-ttu-id="3ebe5-118">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-118">Select **OK**.</span></span>
8. <span data-ttu-id="3ebe5-119">选择 **预算行** 打开 **维护预算行** 页，可在其中查看已经为期间创建的所有预算行。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-119">Select **Budget lines** to open **Maintenance budget lines** page, where you can view all the budget lines that have been created for the period.</span></span>
9. <span data-ttu-id="3ebe5-120">若要审核预算，请在 **维护预算** 页选择预算，然后选择 **审核**。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-120">To approve the budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="3ebe5-121">然后在 **审核预算** 对话框中选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-121">Then, in the **Approve budget** dialog box, select **OK**.</span></span> <span data-ttu-id="3ebe5-122">将把您的姓名输入到 **维护预算** 页中的 **审核人** 字段中。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-122">Your name is entered in the **Approved by** field on the **Maintenance budgets** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3ebe5-123">您审核维护预算之后，除非先删除审核，否则不能在 **维护预算行** 页中重新计算或调整关联的行。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-123">After you've approved a maintenance budget, you can't recalculate or adjust the related lines on the **Maintenance budget lines** page unless you first remove the approval.</span></span> <span data-ttu-id="3ebe5-124">若要删除维护预算的审核，请在 **维护预算** 页选择预算，然后选择 **审核**。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-124">To remove the approval of a maintenance budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="3ebe5-125">然后在 **审核预算** 对话框中选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-125">Then, in the **Approve budget** dialog box, select **OK**.</span></span>

![维护预算](media/01-maintenance-budgets.png)

<span data-ttu-id="3ebe5-127">还可以通过复制现有预算来创建新的维护预算。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-127">You can also create a new maintenance budget by copying an existing budget.</span></span> <span data-ttu-id="3ebe5-128">在 **维护预算** 页选择要复制的预算，然后选择 **复制**。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-128">On the **Maintenance budgets** page, select the budget to copy, and then select **Copy**.</span></span> <span data-ttu-id="3ebe5-129">这种方法在如下情况下非常有用：已经为一个月创建了预算，希望将其复制到其他月份。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-129">This approach is useful if, for example, you've created a budget for one month and want to copy it to other months.</span></span>

> [!NOTE]
> <span data-ttu-id="3ebe5-130">维护预算基于维护安排行仅计算预算成本。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-130">The maintenance budget calculates only budget costs based on maintenance schedule lines.</span></span> <span data-ttu-id="3ebe5-131">若要计算同一期间的实际成本，可以在 **实际成本控制** 页中执行该项计算。</span><span class="sxs-lookup"><span data-stu-id="3ebe5-131">To calculate actual costs for the same period, you can do that calculation on the **Asset cost control** page.</span></span> 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]