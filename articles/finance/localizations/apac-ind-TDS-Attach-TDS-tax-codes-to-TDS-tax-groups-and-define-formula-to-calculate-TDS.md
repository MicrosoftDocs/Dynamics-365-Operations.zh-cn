---
title: 将 TDS 税码附加到 TDS 税组并定义用于计算 TDS 的公式
description: 本主题说明如何设置从源扣缴税款 (TDS) 税组以及将 TDS 税码附加到 TDS 税组。 若要计算 TDS 税组的 TDS，必须定义附加到它的 TDS 税码的公式。
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
ms.openlocfilehash: ec0d683153bd5ab731035159d32881fbdb352d70
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023067"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a><span data-ttu-id="ebdd1-104">将 TDS 税码附加到 TDS 税组并定义用于计算 TDS 的公式</span><span class="sxs-lookup"><span data-stu-id="ebdd1-104">Attach TDS tax codes to TDS tax groups and define the formula for calculating TDS</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ebdd1-105">本主题说明如何设置从源扣缴税款 (TDS) 税组以及将 TDS 税码附加到 TDS 税组。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-105">This topic explains how to set up Tax Deducted at Source (TDS) tax groups and attach TDS tax codes to TDS tax groups.</span></span> <span data-ttu-id="ebdd1-106">若要计算 TDS 税组的 TDS，必须定义附加到它的 TDS 税码的公式。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-106">To calculate TDS for a TDS tax group, you must define the formula for TDS tax codes that are attached to it.</span></span>

<span data-ttu-id="ebdd1-107">按照以下步骤设置 TDS 税组，将 TDS 税码附加到它，并定义用于计算 TDS 的公式。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-107">Follow these steps to set up a TDS tax group, attach TDS tax codes to it, and define the formula for calculating TDS.</span></span>

1. <span data-ttu-id="ebdd1-108">转到 **税务 \> 间接税 \> 预缴税金 \> 预缴税金组**。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-108">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax groups**.</span></span>

    <span data-ttu-id="ebdd1-109">[![预缴税金组页面](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span><span class="sxs-lookup"><span data-stu-id="ebdd1-109">[![Withholding tax groups page](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span></span>

2. <span data-ttu-id="ebdd1-110">在操作窗格上，选择 **新建** 以为 TDS 创建预缴税金组，然后输入所需的详细信息。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-110">On the Action Pane, select **New** to create a withholding tax group for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="ebdd1-111">在 **税务类型** 字段中，选择 **TDS**。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-111">In the **Tax type** field, select **TDS**.</span></span>
4. <span data-ttu-id="ebdd1-112">在 **设置** 快速选项卡上，选择 **添加** 以创建行。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-112">On the **Setup** FastTab, select **Add** to create a line.</span></span>
5. <span data-ttu-id="ebdd1-113">在 **预缴税金代码** 字段中，选择 TDS 税组的 TDS 税码。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-113">In the **Withholding tax code** field, select the TDS tax code for the TDS tax group.</span></span> <span data-ttu-id="ebdd1-114">**预缴税金名称** 字段显示 TDS 税码的名称，**值** 字段显示值。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-114">The **Withholding tax name** field shows the name of the TDS tax code, and the **Value** field shows the value.</span></span>
6. <span data-ttu-id="ebdd1-115">若要忽略为附加到 TDS 交易中 TDS 税码的 TDS 税种组分定义的阈值限制和异常阈值限制，请选中 **忽略阈值** 复选框。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-115">To ignore the threshold limit and exception threshold limit that are defined for the TDS tax component that is attached to the TDS tax code in TDS transactions, select the **Overlook threshold** check box.</span></span>
7. <span data-ttu-id="ebdd1-116">若要阻止在交易中计算税组，请选中 **免税** 复选框。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-116">To prevent the tax group from being calculated in transactions, select the **Exempt** check box.</span></span>
8. <span data-ttu-id="ebdd1-117">在操作窗格上，选择 **设计器** 以打开公式设计器，以便您可以定义用于计算 TDS 税组的 TDS 的公式。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-117">On the Action Pane, select **Designer** to open the formula designer, so that you can define the formula for calculating TDS for the TDS tax group.</span></span> <span data-ttu-id="ebdd1-118">在 **设计器** 页面上，**税务** 选项卡显示已为 TDS 税组选择的 TDS 税码。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-118">On the **Designer** page, the **Taxes** tab shows the TDS tax codes that have been selected for the TDS tax group.</span></span>

    <span data-ttu-id="ebdd1-119">[![设计器页面](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span><span class="sxs-lookup"><span data-stu-id="ebdd1-119">[![Designer page](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span></span>

9. <span data-ttu-id="ebdd1-120">在 **计算** 选项卡上，选择 **Alt+N** 以创建行。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-120">On the **Calculation** tab, select **Alt+N** to create a line.</span></span> <span data-ttu-id="ebdd1-121">**ID** 字段显示 TDS 计算的自动生成的优先级 ID。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-121">The **ID** field shows the automatically generated priority ID for TDS calculation.</span></span>
10. <span data-ttu-id="ebdd1-122">在 **税码** 字段中，选择要为其定义公式的 TDS 税码。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-122">In the **Tax code** field, select the TDS tax code to define the formula for.</span></span> <span data-ttu-id="ebdd1-123">可在字段中选择已为 TDS 税组选择的所有 TDS 税码。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-123">All the TDS tax codes that have been selected for the TDS tax group are available for selection in this field.</span></span>
11. <span data-ttu-id="ebdd1-124">在 **应纳税基数** 字段中，选择用于计算 TDS 的基数：</span><span class="sxs-lookup"><span data-stu-id="ebdd1-124">In the **Taxable basis** field, select the basis for calculating TDS:</span></span>

    - <span data-ttu-id="ebdd1-125">**总额** – 使用为税码定义的计算表达式，基于交易总额（即发票金额）计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-125">**Gross amount** – Calculate TDS based on the gross transaction amount (that is, the invoice amount) by using the calculation expression that is defined for the tax code.</span></span>
    - <span data-ttu-id="ebdd1-126">**不含总额** – 基于为税码定义的计算表达式计算 TDS。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-126">**Excl Gross amount** – Calculate TDS based on the calculation expression that is defined for the tax code.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ebdd1-127">对于优先级 ID 为 **1** 的 TDS 税码，**应纳税基数** 字段不能设置为 **不含总额**。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-127">The **Taxable basis** field can't be set to **Excl Gross amount** for the TDS tax code that has a priority ID of **1**.</span></span>

12. <span data-ttu-id="ebdd1-128">TDS 计算基于在 **计算表达式** 字段中为附加到 TDS 税组的每个税码定义的公式。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-128">The TDS calculation is based on the formula that is defined in the **Calculation expression** field for each tax code that is attached to the TDS tax group.</span></span> <span data-ttu-id="ebdd1-129">选择加号 (**+**)、减号 (**-**)、乘号 (**\**_) 或除号 (_*/**) 按钮，在 **计算表达式** 字段中输入选定 TDS 税码的计算表达式。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-129">Select the plus sign (**+**), minus sign (**-**), multiplication sign (**\**_), or division sign (_*/**) button to enter the calculation expression for the selected TDS tax code in the **Calculation expression** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ebdd1-130">针对优先级 ID 为 **1** 的 TDS 税码，不定义任何计算表达式。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-130">No calculation expression can be defined for the TDS tax code that has a priority ID of **1**.</span></span>

13. <span data-ttu-id="ebdd1-131">若要在 **计算表达式** 字段中定义 TDS 税码的计算表达式，请添加在 **税务** 选项卡上提供的 TDS 税码。若要在 **计算表达式** 字段中添加 TDS 税码，您可以使用以下任何方法：</span><span class="sxs-lookup"><span data-stu-id="ebdd1-131">To define the calculation expression for the TDS tax code in the **Calculation expression** field, add TDS tax codes that are available on the **Taxes** tab. To add TDS tax codes in the **Calculation expression** field, you can use any of the following methods:</span></span>

    - <span data-ttu-id="ebdd1-132">将所需税码从 **税务** 选项卡拖动到 **计算表达式** 字段。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-132">Drag the required tax code from the **Taxes** tab to the **Calculation expression** field.</span></span>
    - <span data-ttu-id="ebdd1-133">两次点击（或双击）**税务** 选项卡上的所需税码。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-133">Double-tap (or double-click) the required tax code on the **Taxes** tab.</span></span>
    - <span data-ttu-id="ebdd1-134">选择并按住（或右键单击）**税务** 选项卡上的所需税码，然后选择 **添加税码**。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-134">Select and hold (or right-click) the required tax code on the **Taxes** tab, and then select **Add tax code**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ebdd1-135">在每个 TDS 税码之前插入计算表达式。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-135">Insert a calculation expression before each TDS tax code.</span></span> <span data-ttu-id="ebdd1-136">已添加到计算表达式的 TDS 税码显示在方括号 (\[...\]) 中。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-136">The TDS tax codes that have been added to the calculation expression appear in brackets (\[...\]).</span></span>

14. <span data-ttu-id="ebdd1-137">若要清除在 **计算表达式** 字段中为税码定义的计算表达式，请选择 **C** 按钮。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-137">To clear the calculation expression that is defined for a tax code in the **Calculation expression** field, select the **C** button.</span></span>
15. <span data-ttu-id="ebdd1-138">若要删除 **计算** 选项卡上的记录，请选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-138">To delete a record on the **Calculation** tab, select **Delete**.</span></span>
16. <span data-ttu-id="ebdd1-139">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ebdd1-139">Close the page.</span></span>
