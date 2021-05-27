---
title: 为 TDS 税务类型设置税种组分
description: 本主题说明如何为从源扣缴税款 (TDS) 税务类型设置预缴税金组分。 它还说明如何定义用于计算每个 TDS 组分的 TDS 的阈值限制。
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
ms.openlocfilehash: 6e0a6a05fcb4afb8c8965e25c3089bc1b3d98431
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023053"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a><span data-ttu-id="3d375-104">为 TDS 税务类型设置税种组分</span><span class="sxs-lookup"><span data-stu-id="3d375-104">Set up tax components for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d375-105">本主题说明如何为从源扣缴税款 (TDS) 税务类型设置预缴税金组分。</span><span class="sxs-lookup"><span data-stu-id="3d375-105">This topic explains how to set up withholding tax components for the Tax Deducted at Source (TDS) tax type.</span></span> <span data-ttu-id="3d375-106">TDS 组分是 TDS、附加费、PE-Cess 和 SHE Cess。</span><span class="sxs-lookup"><span data-stu-id="3d375-106">The TDS components are TDS, surcharge, PE-Cess, and SHE Cess.</span></span> <span data-ttu-id="3d375-107">本主题还说明如何定义用于计算每个 TDS 组分的 TDS 的阈值。</span><span class="sxs-lookup"><span data-stu-id="3d375-107">This topic also explains how to define the threshold that is used to calculate TDS for each TDS component.</span></span> <span data-ttu-id="3d375-108">此外，您可以定义一个异常阈值，用于计算每个 TDS 组分的 TDS。</span><span class="sxs-lookup"><span data-stu-id="3d375-108">Additionally, you can define an exception threshold that is used to calculate TDS for each TDS component.</span></span>

<span data-ttu-id="3d375-109">按照以下步骤设置 TDS 组分。</span><span class="sxs-lookup"><span data-stu-id="3d375-109">Follow these steps to set up TDS components.</span></span>

1. <span data-ttu-id="3d375-110">转到 **税务 \> 设置 \> 预缴税金 \> 预缴税金组分**。</span><span class="sxs-lookup"><span data-stu-id="3d375-110">Go to **Tax \> Setup \> Withholding tax \> Withholding tax components**.</span></span>

    <span data-ttu-id="3d375-111">[![预缴税金组分页面](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span><span class="sxs-lookup"><span data-stu-id="3d375-111">[![Withholding tax components page](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span></span>

2. <span data-ttu-id="3d375-112">在 **税务类型** 字段中，选择 **TDS** 以为 TDS 税务类型设置预缴税金组分。</span><span class="sxs-lookup"><span data-stu-id="3d375-112">In the **Tax type** field, select **TDS** to set up withholding tax components for the TDS tax type.</span></span>
3. <span data-ttu-id="3d375-113">在“操作窗格”中，选择 **新建** 创建一行。</span><span class="sxs-lookup"><span data-stu-id="3d375-113">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="3d375-114">在 **预缴税金组分** 字段中，为 TDS 组分输入名称。</span><span class="sxs-lookup"><span data-stu-id="3d375-114">In the **Withholding tax component** field, enter a name for the TDS component.</span></span>
5. <span data-ttu-id="3d375-115">在 **预缴税金组分组** 字段中，选择 TDS 组分要附加到的 TDS 预缴税金组分组。</span><span class="sxs-lookup"><span data-stu-id="3d375-115">In the **Withholding tax component group** field, select the TDS withholding tax component group to attach the TDS component to.</span></span>
6. <span data-ttu-id="3d375-116">在 **常规** 快速选项卡上，在 **描述** 字段中，输入 TDS 组分的描述。</span><span class="sxs-lookup"><span data-stu-id="3d375-116">On the **General** FastTab, in the **Description** field, enter a description of  the TDS component.</span></span>
7. <span data-ttu-id="3d375-117">在操作窗格上，选择 **阈值** 以打开 **阈值** 页面，以便您可以定义用于为 TDS 组分计算 TDS 的阈值。</span><span class="sxs-lookup"><span data-stu-id="3d375-117">On the Action Pane, select **Threshold** to open **Threshold** page, so that you can define the threshold that is used to calculate TDS for the TDS component.</span></span>
8. <span data-ttu-id="3d375-118">使用 **开始日期** 和 **结束日期** 字段定义阈值适用的期间。</span><span class="sxs-lookup"><span data-stu-id="3d375-118">Use the **From date** and **To date** fields to define the period that the threshold is applicable to.</span></span>
9. <span data-ttu-id="3d375-119">在 **常规** 快速选项卡上，在 **阈值** 字段中，输入用于为 TDS 组分计算 TDS 的阈值金额。</span><span class="sxs-lookup"><span data-stu-id="3d375-119">On the **General** FastTab, in the **Threshold** field, enter the threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="3d375-120">仅在累计发票金额超过阈值时，才从源扣除税款。</span><span class="sxs-lookup"><span data-stu-id="3d375-120">The tax will be deducted at the source only when the cumulative invoice amount crosses the threshold.</span></span>

    <span data-ttu-id="3d375-121">例如，如果阈值金额为 10,000，则在累计发票金额超过 10,000（换言之，当金额为 10,001 或更高）后计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="3d375-121">For example, if the threshold amount is 10,000, TDS is calculated after the cumulative invoice amount exceeds 10,000 (in other words, when it's 10,001 or more).</span></span>

10. <span data-ttu-id="3d375-122">在 **异常阈值** 字段中，输入用于为 TDS 组分计算 TDS 的异常阈值金额。</span><span class="sxs-lookup"><span data-stu-id="3d375-122">In the **Exception threshold** field, enter the exception threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="3d375-123">仅在金额超过异常阈值时，才从源扣除发票行上的税款。</span><span class="sxs-lookup"><span data-stu-id="3d375-123">The tax on an invoice line will be deducted at the source only when the amount crosses the exception threshold.</span></span>

    <span data-ttu-id="3d375-124">例如，如果异常阈值金额为 5,000，则如果发票行金额超过 5,000（换言之，如果金额为 5,001 或更高），将根据特定发票行计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="3d375-124">For example, if the exception threshold amount is 5,000, TDS is calculated on a specific invoice line if the invoice line amount exceeds 5,000 (in other words, if it's 5,001 or more).</span></span>

    <span data-ttu-id="3d375-125">[![阈值页面](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span><span class="sxs-lookup"><span data-stu-id="3d375-125">[![Threshold page](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="3d375-126">异常阈值金额必须小于或等于阈值金额。</span><span class="sxs-lookup"><span data-stu-id="3d375-126">The exception threshold amount must be less than or equal to the threshold amount.</span></span>
    >
    > <span data-ttu-id="3d375-127">如果交易金额超过异常阈值，即使累计发票金额未超过在 **阈值** 字段中指定的阈值，也扣除交易的税款。</span><span class="sxs-lookup"><span data-stu-id="3d375-127">The tax is deducted for a transaction if the transaction amount crosses the exception threshold, even if the cumulative invoice amount doesn't cross the threshold that is specified in the **Threshold** field.</span></span>

11. <span data-ttu-id="3d375-128">关闭 **阈值** 页面以返回到 **预缴税金组分** 页面。</span><span class="sxs-lookup"><span data-stu-id="3d375-128">Close the **Threshold** page to return to the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="3d375-129">在操作窗格上，选择 **复制** 以打开 **复制预缴税金组分** 对话框，以便您可以将为一个 TDS 组分组设置的 TDS 组分复制到另一个 TDS 组分组。</span><span class="sxs-lookup"><span data-stu-id="3d375-129">On the Action Pane, select **Copy** to open the **Copy withholding tax components** dialog box, so that you can copy the TDS components that were set up for one TDS component group to another TDS component group.</span></span>
13. <span data-ttu-id="3d375-130">在 **从** 字段中，选择要从中复制 TDS 组分的 TDS 组分组。</span><span class="sxs-lookup"><span data-stu-id="3d375-130">In the **From** field, select the TDS component group to copy the TDS components from.</span></span> <span data-ttu-id="3d375-131">在 **至** 字段中，选择要将 TDS 组分复制到的预缴税金组分组。</span><span class="sxs-lookup"><span data-stu-id="3d375-131">In the **To** field, select the withholding tax component group to copy the TDS components to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3d375-132">不复制附加到这两个 TDS 组分组的常见 TDS 组分。</span><span class="sxs-lookup"><span data-stu-id="3d375-132">Common TDS components that are attached to both TDS component groups aren't copied.</span></span>

14. <span data-ttu-id="3d375-133">选择 **确定** 以在 **预缴税金组分** 页面上为其他 TDS 组分组复制和创建 TDS 组分。</span><span class="sxs-lookup"><span data-stu-id="3d375-133">Select **OK** to copy and create TDS components for the other TDS component group on the **Withholding tax components** page.</span></span>

    <span data-ttu-id="3d375-134">[![复制预缴税金组分对话框](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span><span class="sxs-lookup"><span data-stu-id="3d375-134">[![Copy withholding tax components dialog box](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span></span>

15. <span data-ttu-id="3d375-135">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3d375-135">Close the page.</span></span>
