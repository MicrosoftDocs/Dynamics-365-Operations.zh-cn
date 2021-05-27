---
title: 设置 TDS 税务类型的预缴税金代码
description: 本主题说明如何设置从源扣缴税款 (TDS) 的税代码。
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
ms.openlocfilehash: d56a23f7af7633e1761a8a7c48f71381d6f14df2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023070"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a><span data-ttu-id="450bb-103">设置 TDS 税务类型的预缴税金代码</span><span class="sxs-lookup"><span data-stu-id="450bb-103">Set up withholding tax codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="450bb-104">本主题说明如何设置从源扣缴税款 (TDS) 的税代码。</span><span class="sxs-lookup"><span data-stu-id="450bb-104">This topic explains how to set up tax codes for Tax Deducted at Source (TDS).</span></span>

1. <span data-ttu-id="450bb-105">转到 **税 \> 间接税 \> 预缴税金 \> 预缴税金代码**。</span><span class="sxs-lookup"><span data-stu-id="450bb-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax codes**.</span></span>

    <span data-ttu-id="450bb-106">[![预缴税金代码页面](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span><span class="sxs-lookup"><span data-stu-id="450bb-106">[![Withholding tax codes page](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span></span>

2. <span data-ttu-id="450bb-107">在操作窗格上，选择 **新建** 为 TDS 创建预缴税金代码，然后输入所需的详细信息。</span><span class="sxs-lookup"><span data-stu-id="450bb-107">On the Action Pane, select **New** to create a withholding tax code for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="450bb-108">在 **常规** 快速选项卡上，在 **税务类型** 字段中，选择 **TDS** 将税代码分类为 TDS 税代码。</span><span class="sxs-lookup"><span data-stu-id="450bb-108">On the **General** FastTab, in the **Tax type** field, select **TDS** to categorize the tax code as a TDS tax code.</span></span>
4. <span data-ttu-id="450bb-109">在 **结算期间** 字段中，选择 TDS 税代码的 TDS 结算期间。</span><span class="sxs-lookup"><span data-stu-id="450bb-109">In the **Settlement period** field, select the TDS settlement period for the TDS tax code.</span></span>
5. <span data-ttu-id="450bb-110">在 **主科目** 字段中，选择应将 TDS 金额过帐到的会计科目。</span><span class="sxs-lookup"><span data-stu-id="450bb-110">In the **Main account** field, select the ledger account that the TDS amount should be posted to.</span></span>
6. <span data-ttu-id="450bb-111">在 **应收帐款** 字段中，选择应将销售交易中扣除的 TDS 金额过帐到的应收帐款。</span><span class="sxs-lookup"><span data-stu-id="450bb-111">In the **Receivable account** field, select the receivable account that the TDS amount that is deducted in sales transactions should be posted to.</span></span>

    <span data-ttu-id="450bb-112">**源** 字段将自动设置为 **总额百分比**，此值无法更改。</span><span class="sxs-lookup"><span data-stu-id="450bb-112">The **Origin** field is automatically set to **Percentage of gross amount**, and the value can't be changed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="450bb-113">对于 TDS 税务类型的税代码，不能将来源设置为 **净额百分比**。</span><span class="sxs-lookup"><span data-stu-id="450bb-113">You can't set the origin to **Percentage of net amount** for tax codes of the TDS tax type.</span></span>

7. <span data-ttu-id="450bb-114">在 **预缴税金组分** 字段中，选择 TDS 税代码的 TDS 税种组分。</span><span class="sxs-lookup"><span data-stu-id="450bb-114">In the **Withholding tax component** field, select the TDS tax component for the TDS tax code.</span></span>
8. <span data-ttu-id="450bb-115">在操作窗格上，选择 **值** 打开 **预缴税金值** 页。</span><span class="sxs-lookup"><span data-stu-id="450bb-115">On the Action Pane, select **Values** to open the **Withholding tax values** page.</span></span>
9. <span data-ttu-id="450bb-116">在 **开始日期** 字段中，输入 TDS 值的开始日期。</span><span class="sxs-lookup"><span data-stu-id="450bb-116">In the **From date** field, enter the start date for the TDS value.</span></span> <span data-ttu-id="450bb-117">在 **结束日期** 字段中，输入结束日期。</span><span class="sxs-lookup"><span data-stu-id="450bb-117">In the **To date** field, enter the end date.</span></span>

    > [!NOTE]
    > <span data-ttu-id="450bb-118">**下限**、**上限** 和 **排除 %** 字段对 TDS 税务类型的税代码不可用。</span><span class="sxs-lookup"><span data-stu-id="450bb-118">The **Minimum limit**, **Upper limit**, and **Exclude %** fields aren't available for tax codes of the TDS tax type.</span></span>

10. <span data-ttu-id="450bb-119">在 **值** 字段中，输入 TDS 税代码的 TDS 百分比。</span><span class="sxs-lookup"><span data-stu-id="450bb-119">In the **Value** field, enter the percentage of TDS for the TDS tax code.</span></span>
11. <span data-ttu-id="450bb-120">关闭 **预缴税金值** 页返回 **预缴税金代码** 页。</span><span class="sxs-lookup"><span data-stu-id="450bb-120">Close the **Withholding tax values** page to return to the **Withholding tax codes** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="450bb-121">**预缴税金代码** 页上的 **限额** 按钮对 TDS 税务类型的税代码不可用。</span><span class="sxs-lookup"><span data-stu-id="450bb-121">The **Limits** button on the **Withholding tax codes** page isn't available for tax codes of the TDS tax type.</span></span>

12. <span data-ttu-id="450bb-122">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="450bb-122">Close the page.</span></span>
