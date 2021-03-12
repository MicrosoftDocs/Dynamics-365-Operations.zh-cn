---
title: 将固定资产作为废料处置
description: 本主题介绍清除作为废料处置的固定资产交易记录的过程。
author: moaamer
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 4dee4468079a9ad500f513900cec090acf6026ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969120"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a><span data-ttu-id="7c8c5-103">将固定资产作为废料处置</span><span class="sxs-lookup"><span data-stu-id="7c8c5-103">Dispose of a fixed asset as scrap</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c8c5-104">本主题介绍清除作为废料处置的固定资产交易记录的过程。</span><span class="sxs-lookup"><span data-stu-id="7c8c5-104">The topic describes the process of eliminating transactions for a fixed asset that was disposed of as scrap.</span></span> <span data-ttu-id="7c8c5-105">可以清除的交易记录类型包括资产的购置和累计折旧交易记录以及其他固定资产交易记录。</span><span class="sxs-lookup"><span data-stu-id="7c8c5-105">The transaction types that can be eliminated include an asset's acquisition and accumulated depreciation transactions and other fixed asset transactions.</span></span> <span data-ttu-id="7c8c5-106">清除这些交易记录会影响资产负债表科目，例如购置调整、折旧调整、重估、调高和调低科目。</span><span class="sxs-lookup"><span data-stu-id="7c8c5-106">Elimination of these transactions affects balance sheet accounts, such as acquisition adjustment, depreciation adjustment, revaluation, write-up, and write-down accounts.</span></span>

| <span data-ttu-id="7c8c5-107">交易</span><span class="sxs-lookup"><span data-stu-id="7c8c5-107">Transaction</span></span>                                         | <span data-ttu-id="7c8c5-108">借记（借）</span><span class="sxs-lookup"><span data-stu-id="7c8c5-108">Debit (Dr.)</span></span> | <span data-ttu-id="7c8c5-109">贷记（贷）</span><span class="sxs-lookup"><span data-stu-id="7c8c5-109">Credit (Cr.)</span></span> |
|-----------------------------------------------------|-------------|--------------|
| <span data-ttu-id="7c8c5-110">借记累计折旧</span><span class="sxs-lookup"><span data-stu-id="7c8c5-110">Dr. Accumulated depreciation</span></span>                        | <span data-ttu-id="7c8c5-111">X</span><span class="sxs-lookup"><span data-stu-id="7c8c5-111">X</span></span>           |              |
| <span data-ttu-id="7c8c5-112">贷记固定资产损益</span><span class="sxs-lookup"><span data-stu-id="7c8c5-112">Cr. Fixed assets gain/loss</span></span>                          |             | <span data-ttu-id="7c8c5-113">X</span><span class="sxs-lookup"><span data-stu-id="7c8c5-113">X</span></span>            |
| <span data-ttu-id="7c8c5-114">借记固定资产损益</span><span class="sxs-lookup"><span data-stu-id="7c8c5-114">Dr. Fixed assets gain/loss</span></span>                          | <span data-ttu-id="7c8c5-115">X</span><span class="sxs-lookup"><span data-stu-id="7c8c5-115">X</span></span>           |              |
| <span data-ttu-id="7c8c5-116">贷记固定资产购置科目</span><span class="sxs-lookup"><span data-stu-id="7c8c5-116">Cr. Fixed asset acquisition account</span></span>                 |             | <span data-ttu-id="7c8c5-117">X</span><span class="sxs-lookup"><span data-stu-id="7c8c5-117">X</span></span>            |
| <span data-ttu-id="7c8c5-118">借记固定资产损益（帐面净值 \[NBV\]）</span><span class="sxs-lookup"><span data-stu-id="7c8c5-118">Dr. Fixed assets gain/loss (net book value \[NBV\])</span></span> | <span data-ttu-id="7c8c5-119">X</span><span class="sxs-lookup"><span data-stu-id="7c8c5-119">X</span></span>           |              |
| <span data-ttu-id="7c8c5-120">贷记固定资产损益 (NBV)</span><span class="sxs-lookup"><span data-stu-id="7c8c5-120">Cr. Fixed assets gain/loss (NBV)</span></span>                    |             | <span data-ttu-id="7c8c5-121">X</span><span class="sxs-lookup"><span data-stu-id="7c8c5-121">X</span></span>            |

> [!NOTE]
> <span data-ttu-id="7c8c5-122">我们建议您与公司的首席财务官 (CFO) 或财务总监紧密合作，以确定每种交易记录类型应使用的正确科目，并验证处置过程及其产生的交易记录是否正确更新了这些科目。</span><span class="sxs-lookup"><span data-stu-id="7c8c5-122">We recommend that you work closely with your company's chief financial officer (CFO) or controller to identify the correct accounts that should be used for each transaction type, and also to verify that the disposal process and the transactions that it generates update those accounts correctly.</span></span>

<span data-ttu-id="7c8c5-123">在将固定资产作为废料处置之前，必须创建与资产的购置价值、当年的折旧、前一年的折旧以及资产的 NBV 关联的会计科目。</span><span class="sxs-lookup"><span data-stu-id="7c8c5-123">Before you dispose of a fixed asset as scrap, you must create ledger accounts that are associated with the asset's acquisition value, depreciation for the current year, depreciation for previous years, and the asset's NBV.</span></span> <span data-ttu-id="7c8c5-124">固定资产交易记录类型列在 **固定资产过帐模板** 页面上。</span><span class="sxs-lookup"><span data-stu-id="7c8c5-124">The fixed asset transaction types are listed on the **Fixed assets posting profile** page.</span></span> <span data-ttu-id="7c8c5-125">转到 **固定资产 \> 设置 \> 固定资产过帐模板**，然后在 **处置** 快速选项卡上，在网格上方的字段中选择 **废料**。</span><span class="sxs-lookup"><span data-stu-id="7c8c5-125">Go to **Fixed assets \> Setup \> Fixed asset posting profiles**, and then, on the **Disposal** FastTab, select **Scrap** in the field above the grid.</span></span> <span data-ttu-id="7c8c5-126">下图显示了 **固定资产过帐模板** 页面上的固定资产交易记录类型的列表。</span><span class="sxs-lookup"><span data-stu-id="7c8c5-126">The following illustration shows the list of fixed asset transaction types on the **Fixed asset posting profiles** page.</span></span>


<span data-ttu-id="7c8c5-127">[![作为废料处置资产，图 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span><span class="sxs-lookup"><span data-stu-id="7c8c5-127">[![Disposing of an asset as scap, Fig. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span></span>

<span data-ttu-id="7c8c5-128">对于以下示例，固定资产于 2018 年 1 月 1 日购置，将于 2019 年 3 月 31 日报废。</span><span class="sxs-lookup"><span data-stu-id="7c8c5-128">For the following example, a fixed asset was acquired on January 1, 2018, and it will be scrapped on March 31, 2019.</span></span>

- <span data-ttu-id="7c8c5-129">**购置价格：** 24,000.00 美元 (USD)</span><span class="sxs-lookup"><span data-stu-id="7c8c5-129">**Acquisition price:** 24,000.00 US dollars (USD)</span></span>
- <span data-ttu-id="7c8c5-130">**使用年限：** 两年</span><span class="sxs-lookup"><span data-stu-id="7c8c5-130">**Service life:** Two years</span></span>
- <span data-ttu-id="7c8c5-131">**折旧方法：** 直线法</span><span class="sxs-lookup"><span data-stu-id="7c8c5-131">**Depreciation method:** Straight line service life</span></span>
- <span data-ttu-id="7c8c5-132">**折旧金额：** 每月 1,000.00 美元</span><span class="sxs-lookup"><span data-stu-id="7c8c5-132">**Depreciation amount:** 1,000.00 USD per month</span></span>

<span data-ttu-id="7c8c5-133">使用以下公式计算固定资产的 NBV：</span><span class="sxs-lookup"><span data-stu-id="7c8c5-133">The NBV of a fixed asset is calculated by using the following formula:</span></span>

<span data-ttu-id="7c8c5-134">帐面净值 = 购置价格 – 折旧</span><span class="sxs-lookup"><span data-stu-id="7c8c5-134">Net book value = Acquisition price – Depreciation</span></span>

<span data-ttu-id="7c8c5-135">在此示例中，从 2018 年 1 月到 2019 年 3 月，固定资产购置和折旧为时 15 个月。</span><span class="sxs-lookup"><span data-stu-id="7c8c5-135">In this example, the fixed asset was acquired and was depreciated for 15 months, from January 2018 through March 2019.</span></span> <span data-ttu-id="7c8c5-136">因此，资产的 NBV 为 9,000.00 美元（24,000.00 美元 – 15,000.00 美元）。</span><span class="sxs-lookup"><span data-stu-id="7c8c5-136">Therefore, the asset's NBV is 9,000.00 USD (24,000.00 USD – 15,000.00 USD).</span></span>

<span data-ttu-id="7c8c5-137">[![固定资产折旧示例](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span><span class="sxs-lookup"><span data-stu-id="7c8c5-137">[![Fixed asset depreciation example](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span></span>


<span data-ttu-id="7c8c5-138">要创建处置日记帐，请转到 **固定资产 \> 日记帐分录 \> 固定资产日记帐**，然后，在“操作窗格”中，选择 **行**。</span><span class="sxs-lookup"><span data-stu-id="7c8c5-138">To create a disposal journal, go to **Fixed assets \> Journal entries \> Fixed assets journal**, and then, on the Action Pane, select **Lines**.</span></span> <span data-ttu-id="7c8c5-139">选择 **处置 – 报废**，然后选择固定资产 ID。</span><span class="sxs-lookup"><span data-stu-id="7c8c5-139">Select **Disposal – scrap**, and then select a fixed asset ID.</span></span> <span data-ttu-id="7c8c5-140">要完全处置资产，请不要在 **借记** 字段或 **贷记** 字段中输入值。</span><span class="sxs-lookup"><span data-stu-id="7c8c5-140">To fully dispose of the asset, don't enter a value in either the **Debit** field or the **Credit** field.</span></span>

<span data-ttu-id="7c8c5-141">[![固定资产日记帐](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span><span class="sxs-lookup"><span data-stu-id="7c8c5-141">[![Fixed assets journal](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span></span>

<span data-ttu-id="7c8c5-142">固定资产处置报废交易记录通过以下方式更改固定资产帐簿的字段值：</span><span class="sxs-lookup"><span data-stu-id="7c8c5-142">The fixed asset disposal scrap transaction changes the field values for the fixed asset book in the following ways:</span></span>

- <span data-ttu-id="7c8c5-143">在 **余额** 部分，**状态** 字段更新为 **已报废**。</span><span class="sxs-lookup"><span data-stu-id="7c8c5-143">In the **Balance** section, the **Status** field is updated to **Scrapped**.</span></span>
- <span data-ttu-id="7c8c5-144">在 **签发** 部分，**处置日期** 字段设置为资产报废的日期。</span><span class="sxs-lookup"><span data-stu-id="7c8c5-144">In the **Issue** section, the **Disposal date** field is set to the date when the asset was scrapped.</span></span>

<span data-ttu-id="7c8c5-145">[![固定资产日记帐明细](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span><span class="sxs-lookup"><span data-stu-id="7c8c5-145">[![Fixed assets journal detail](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span></span>

<span data-ttu-id="7c8c5-146">下图显示了固定资产余额。</span><span class="sxs-lookup"><span data-stu-id="7c8c5-146">The following illustration shows the fixed asset balance.</span></span>

<span data-ttu-id="7c8c5-147">[![固定资产余额](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span><span class="sxs-lookup"><span data-stu-id="7c8c5-147">[![Fixed asset balance](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span></span>

<span data-ttu-id="7c8c5-148">下图显示了已过帐的凭证。</span><span class="sxs-lookup"><span data-stu-id="7c8c5-148">The following illustration shows the voucher that is posted.</span></span>

<span data-ttu-id="7c8c5-149">[![帐面净值](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span><span class="sxs-lookup"><span data-stu-id="7c8c5-149">[![Net book value](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span></span>
