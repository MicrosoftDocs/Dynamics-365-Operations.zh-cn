---
title: 运行定期 TDS 结算流程
description: 本主题说明如何结算定期从源扣缴税款 (TDS)。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: cfab08a4190bf51518bd4a9b445b229a5081e87d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023047"
---
# <a name="run-the-periodic-tds-settlement-process"></a><span data-ttu-id="fab23-103">运行定期 TDS 结算流程</span><span class="sxs-lookup"><span data-stu-id="fab23-103">Run the periodic TDS settlement process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fab23-104">本主题说明如何结算定期从源扣缴税款 (TDS)。</span><span class="sxs-lookup"><span data-stu-id="fab23-104">This topic explains how to settle periodic Tax Deducted at Source (TDS).</span></span>

1. <span data-ttu-id="fab23-105">转到 **税务 \> 申报 \> 预缴税金 \> 预缴税金付款**。</span><span class="sxs-lookup"><span data-stu-id="fab23-105">Go to **Tax \> Declarations \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="fab23-106">[![预缴税金付款对话框](./media/apac-ind-TDS-47.png)](./media/apac-ind-TDS-47.png)</span><span class="sxs-lookup"><span data-stu-id="fab23-106">[![Withholding tax payment dialog box](./media/apac-ind-TDS-47.png)](./media/apac-ind-TDS-47.png)</span></span>

2. <span data-ttu-id="fab23-107">在 **预缴税金付款** 对话框的 **税务类型** 字段中，选择 **TDS**。</span><span class="sxs-lookup"><span data-stu-id="fab23-107">In the **Withholding tax payment** dialog box, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="fab23-108">在 **税务帐号 (TAN)** 字段中，选择要对其运行结算流程的税务帐号 (TAN)。</span><span class="sxs-lookup"><span data-stu-id="fab23-108">In the **Tax Account Number (TAN)** field, select the Tax Account Number (TAN) to run the settlement process for.</span></span>
4. <span data-ttu-id="fab23-109">在 **预缴税金组分组** 字段中，选择要对其运行结算流程的 TDS 组分组。</span><span class="sxs-lookup"><span data-stu-id="fab23-109">In the **Withholding tax component group** field, select the TDS component group to run the settlement process for.</span></span>
5. <span data-ttu-id="fab23-110">在 **结算期间** 字段中，选择要对其运行结算流程的 TDS 结算期间。</span><span class="sxs-lookup"><span data-stu-id="fab23-110">In the **Settlement period** field, select the TDS settlement period to run the settlement process for.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fab23-111">针对在 **预缴税金结算期间** 页面的 **期间** 选项卡上为 TDS 结算期间设置的所有期间运行 TDS 结算流程（**税务 \> 间接税 \> 预缴税金 \> 预缴税金结算期间**）。</span><span class="sxs-lookup"><span data-stu-id="fab23-111">The TDS settlement process is run for all periods that are set up for the TDS settlement period on the **Periods** tab of the **Withholding tax settlement periods** page (**Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**).</span></span>

6. <span data-ttu-id="fab23-112">在 **开始日期** 字段中，选择运行 TDS 结算流程的开始日期。</span><span class="sxs-lookup"><span data-stu-id="fab23-112">In the **From date** field, select the start date to run the TDS settlement process from.</span></span>

    <span data-ttu-id="fab23-113">对于结算期间内的特定期间，将为该期间定义的开始日期视为“开始”日期。</span><span class="sxs-lookup"><span data-stu-id="fab23-113">For a specific period within the settlement period, the start date that is defined for the period is taken as the "from" date.</span></span> <span data-ttu-id="fab23-114">例如，TDS 结算期间具有两个期间：2009 年 4 月 1 日至 4 月 30 日以及 2009 年 5 月 1 日至 5 月 31 日。</span><span class="sxs-lookup"><span data-stu-id="fab23-114">For example, the TDS settlement period has two periods: April 1 through April 30, 2009, and May 1 through May 31, 2009.</span></span> <span data-ttu-id="fab23-115">如果在 **开始日期** 字段中选择 **04/06/2009**（2009 年 4 月 6 日）作为开始日期，结算流程将仍从 2009 年 4 月 1 日开始运行。</span><span class="sxs-lookup"><span data-stu-id="fab23-115">If you select **04/06/2009** (April 6, 2009) as the start date in the **From date** field, the settlement process will still run from April 1, 2009.</span></span>

    <span data-ttu-id="fab23-116">如果您在 **开始日期** 字段中输入下一期间，但没有在结算期间内设置上一期间，将不会对任何以前的期间进行结算。</span><span class="sxs-lookup"><span data-stu-id="fab23-116">If you enter a later period in the **From date** field, but without settling a previous period within the settlement period, the settlement won't occur for any previous periods.</span></span> <span data-ttu-id="fab23-117">例如，TDS 结算期间具有三个期间：2009 年 4 月 1 日至 4 月 30 日、2009 年 5 月 1 日至 5 月 31 日以及 2009 年 6 月 1 日至 6 月 30 日。</span><span class="sxs-lookup"><span data-stu-id="fab23-117">For example, the TDS settlement period has three periods: April 1 through April 30, 2009, May 1 through May 31, 2009, and June 1 through June 30, 2009.</span></span> <span data-ttu-id="fab23-118">如果在 **开始日期** 字段中选择 **05/01/2009**（2009 年 5 月 1 日）作为开始日期，结算流程将仅在 2009 年 5 月 1 日至 5 月 31 日之间运行。</span><span class="sxs-lookup"><span data-stu-id="fab23-118">If you select **05/01/2009** (May 1, 2009) as the start date in the **From date** field, the settlement process will run only from May 1 through May 31, 2009.</span></span> <span data-ttu-id="fab23-119">在 2009 年 4 月 1 日至 4 月 30 日之间将不进行结算。</span><span class="sxs-lookup"><span data-stu-id="fab23-119">The settlement won't occur for April 1 through April 30, 2009.</span></span>

7. <span data-ttu-id="fab23-120">在 **交易日期** 字段中，选择要过帐 TDS 结算交易的日期。</span><span class="sxs-lookup"><span data-stu-id="fab23-120">In the **Transaction date** field, select the date to post the TDS settlement transaction.</span></span>
8. <span data-ttu-id="fab23-121">在 **预缴税金付款版本** 字段中，选择 TDS 结算版本：</span><span class="sxs-lookup"><span data-stu-id="fab23-121">In the **Withholding tax payment version** field, select the TDS settlement version:</span></span>

     - <span data-ttu-id="fab23-122">**原始** – 使用此选项首次运行 TDS 结算流程。</span><span class="sxs-lookup"><span data-stu-id="fab23-122">**Original** – Use this option to run the TDS settlement process for the first time.</span></span> <span data-ttu-id="fab23-123">原始付款版本仅使用一次，以针对 TAN、预缴税金组分组和预缴税金结算期间的组合运行 TDS 结算流程。</span><span class="sxs-lookup"><span data-stu-id="fab23-123">The original payment version is used only one time to run the TDS settlement process for a combination of a TAN, a withholding tax component group, and a withholding tax settlement period.</span></span>
    - <span data-ttu-id="fab23-124">**最新版本** – 如果已针对指定期间运行 TDS 结算流程，请使用此选项。</span><span class="sxs-lookup"><span data-stu-id="fab23-124">**Latest versions** – Use this option if the TDS settlement process has already been run for the specified period.</span></span> <span data-ttu-id="fab23-125">包括在之前针对该期间运行结算流程之后过帐的追溯交易。</span><span class="sxs-lookup"><span data-stu-id="fab23-125">Include back-dated transactions that were posted after the settlement process was previously run for the period.</span></span> <span data-ttu-id="fab23-126">您可以使用此选项运行结算流程，次数不限。</span><span class="sxs-lookup"><span data-stu-id="fab23-126">You can use this option to run the settlement process any number of times.</span></span>

9. <span data-ttu-id="fab23-127">选中 **更新** 复选框以运行 TDS 结算流程并将金额过帐到分类帐帐户。</span><span class="sxs-lookup"><span data-stu-id="fab23-127">Select the **Update** check box to run the TDS settlement process and post the amounts to the ledger accounts.</span></span> <span data-ttu-id="fab23-128">如果清除此复选框，则不会运行结算流程，也不会生成财务分录。</span><span class="sxs-lookup"><span data-stu-id="fab23-128">If this check box is cleared, the settlement process won't be run, and the financial entries won't be generated.</span></span>
10. <span data-ttu-id="fab23-129">选择 **确定** 以运行 TDS 结算流程并生成预缴税金付款报表。</span><span class="sxs-lookup"><span data-stu-id="fab23-129">Select **OK** to run the TDS settlement process and generate the withholding tax payment report.</span></span> <span data-ttu-id="fab23-130">结算流程中包含的 TDS 交易的状态在 **结算** 页面上显示为 **已结算**（转到 **应付帐款 \> 付款 \> 供应商付款日记帐**，选择 **行**，选择 **功能**，然后选择 **结算**）。</span><span class="sxs-lookup"><span data-stu-id="fab23-130">The status of TDS transactions that are included in the settlement process is shown as **Settled** on the **Settlement** page (go to **Accounts payable \> Payments \> Vendor payment journal**, select **Lines**, select **Functions**, and then select **Settlement**).</span></span>

### <a name="important-points"></a><span data-ttu-id="fab23-131">重要事项</span><span class="sxs-lookup"><span data-stu-id="fab23-131">Important points</span></span>

- <span data-ttu-id="fab23-132">如果未在结算流程期间选择预缴税金组分组，将针对选定 TAN 和结算期间的所有预缴税金组分组进行结算。</span><span class="sxs-lookup"><span data-stu-id="fab23-132">If a withholding tax component group isn't selected during the settlement process, the settlement occurs for all the withholding tax component groups for the selected TAN and settlement period.</span></span> <span data-ttu-id="fab23-133">在 **未结交易编辑** 页面上为每个预缴税金组分组创建单独的行。</span><span class="sxs-lookup"><span data-stu-id="fab23-133">A separate line is created for each withholding tax component group on the **Open transaction editing** page.</span></span>
- <span data-ttu-id="fab23-134">结算流程基于结算期间的评估对象类别的性质。</span><span class="sxs-lookup"><span data-stu-id="fab23-134">The settlement process is based on the nature of assessee category for a settlement period.</span></span> <span data-ttu-id="fab23-135">评估对象类别的性质为 **公司** 的交易将进行结算并在 **未结交易编辑** 页面上显示为一行。</span><span class="sxs-lookup"><span data-stu-id="fab23-135">Transactions where the nature of assessee category is **Company** are settled and are shown as one line on the **Open transaction editing** page.</span></span> <span data-ttu-id="fab23-136">评估对象的性质为 **公司** 以外的其他类别的交易将进行结算并在 **未结交易编辑** 页面上显示为一行。</span><span class="sxs-lookup"><span data-stu-id="fab23-136">Transactions where the nature of assessee is something other than **Company** are settled and are shown as one line on the **Open transaction editing** page.</span></span>
- <span data-ttu-id="fab23-137">**未结交易编辑** 页面上已结算 TDS 交易行的截止日期基于在 **供应商** 页面上为 TDS 主管机构供应商定义的付款期限。</span><span class="sxs-lookup"><span data-stu-id="fab23-137">The due date for the settled TDS transaction lines on the **Open transaction editing** page is based on the terms of payment that are defined for the TDS authority vendor on the **Vendors** page.</span></span> <span data-ttu-id="fab23-138">如果没有为 TDS 主管机构供应商定义付款期限，结算期间的最后一天将显示为截止日期。</span><span class="sxs-lookup"><span data-stu-id="fab23-138">If the terms of payments aren't defined for the TDS authority vendor, the last day of the settlement period is shown as the due date.</span></span>
