---
title: 对跟踪所生成 ER 报表结果并与基准值比较的改进
description: 本主题介绍 Microsoft Dynamics 365 for Finance and Operations 版本 10.0.3（2019 年 6 月）中对 ER 基准功能的改进。
author: NickSelin
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 222a415f686c8028fc2a414f97eed0291d850ae7
ms.sourcegitcommit: 9917df8c0c9320955c61186cd922c8df894a4f25
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/21/2019
ms.locfileid: "1700674"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a><span data-ttu-id="0fb2a-103">对跟踪所生成 ER 报表结果并与基准值比较的改进</span><span class="sxs-lookup"><span data-stu-id="0fb2a-103">Improvements in tracing the results of generated ER reports and comparing them with baseline values</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0fb2a-104">本主题介绍已对电子申报 (ER) 框架基准功能所做的第一组改进。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-104">This topic describes the first set of improvements that have been made to the baseline feature of the Electronic reporting (ER) framework.</span></span> <span data-ttu-id="0fb2a-105">Microsoft Dynamics 365 for Finance and Operations 版本 10.0.3（2019 年 6 月）及更高版本中包含这些改进。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-105">These improvements are available in Microsoft Dynamics 365 for Finance and Operations version 10.0.3 (June 2019) and later.</span></span>

## <a name="automate-the-setting-of-baseline-rules"></a><span data-ttu-id="0fb2a-106">自动执行基准规则的设置</span><span class="sxs-lookup"><span data-stu-id="0fb2a-106">Automate the setting of baseline rules</span></span>

<span data-ttu-id="0fb2a-107">[跟踪生成的报表结果并将其与基准值进行比较](er-trace-reports-compare-baseline.md)主题介绍如何配置 ER 框架以收集有关 ER 格式执行情况的信息和评估这些执行的结果。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-107">The [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic explains how to configure the ER framework to collect information about ER format executions and evaluate the results of those executions.</span></span> <span data-ttu-id="0fb2a-108">本主题中的示例显示必须完成的步骤。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-108">The example in this topic shows the steps that must be completed.</span></span>

<span data-ttu-id="0fb2a-109">下面是其中的部分步骤：</span><span class="sxs-lookup"><span data-stu-id="0fb2a-109">Here are some of the steps:</span></span>

- <span data-ttu-id="0fb2a-110">运行 ER 格式以生成出站文件并存储在本地。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-110">Run an ER format to generate an outbound file, and store the file locally.</span></span>
- <span data-ttu-id="0fb2a-111">将本地存储的文件作为为 ER 格式添加的基准的附件添加。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-111">Add the locally stored file as an attachment of the baseline that was added for an ER format.</span></span>
- <span data-ttu-id="0fb2a-112">为添加的基准配置基准规则。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-112">Configure the baseline rule for the added baseline.</span></span> <span data-ttu-id="0fb2a-113">此配置中包含以下步骤：</span><span class="sxs-lookup"><span data-stu-id="0fb2a-113">This configuration includes the following steps:</span></span>

    - <span data-ttu-id="0fb2a-114">指定用于生成出站文件的 ER 格式元素。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-114">Specify an ER format element that is used to generate an outbound file.</span></span>
    - <span data-ttu-id="0fb2a-115">选择引用生成的出站文件的附件。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-115">Select the attachment that refers to the generated outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="0fb2a-116">这些步骤必须手动执行，即使可以使用新的 ER 功能自动执行这些步骤也不例外。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-116">These steps must be done manually, even though the new ER capabilities enable them to be automated.</span></span> <span data-ttu-id="0fb2a-117">若要了解有关此功能的详细信息，请完成以下示例。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-117">To learn more about this feature, complete the following example.</span></span>

## <a name="example-automate-the-setting-of-baseline-rules"></a><span data-ttu-id="0fb2a-118">示例：自动执行基准规则的设置</span><span class="sxs-lookup"><span data-stu-id="0fb2a-118">Example: Automate the setting of baseline rules</span></span>

<span data-ttu-id="0fb2a-119">若要完成此示例中的步骤，必须先完成前面的“为设计的 ER 格式添加新基准”部分[跟踪生成的报表结果并将其与基准值进行比较](er-trace-reports-compare-baseline.md)主题中的示例的步骤。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-119">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, up through the "Add a new baseline for a designed ER format" section.</span></span>

### <a name="review-added-baseline"></a><span data-ttu-id="0fb2a-120">查看添加的基准</span><span class="sxs-lookup"><span data-stu-id="0fb2a-120">Review added baseline</span></span>

1. <span data-ttu-id="0fb2a-121">转到**组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-121">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0fb2a-122">选择**基准**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-122">Select **Baselines**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0fb2a-123">仅当为当前公司开启了**以调试模式运行** ER 用户参数，操作窗格上的**基准**按钮才可用。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-123">The **Baselines** button on the Action Pane is available only when the **Run in debug mode** ER user parameter is turned on for the current company.</span></span>

<span data-ttu-id="0fb2a-124">已为所选**用于了解 ER 基准的格式**格式添加了基准，但是尚未为此基准添加基准规则。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-124">The baseline has been added for the selected **Format to learn ER baselines** format, but the baseline rules haven't yet been added for this baseline.</span></span>

<span data-ttu-id="0fb2a-125">![“电子申报格式基准”页](media/GER-BaselineSample-AddBaseline2.PNG "“电子申报格式基准”页的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="0fb2a-125">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline2.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="0fb2a-126">新建基准规则</span><span class="sxs-lookup"><span data-stu-id="0fb2a-126">Make a new baseline rule</span></span>

1. <span data-ttu-id="0fb2a-127">转到**组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-127">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0fb2a-128">在树中，展开**用于了解 ER 基准的模型**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-128">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="0fb2a-129">在树中，选择**用于了解 ER 基准的模型\\用于了解 ER 基准的格式**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-129">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="0fb2a-130">在**版本**快速选项卡上，选择**运行**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-130">On the **Versions** FastTab, select **Run**.</span></span>
5. <span data-ttu-id="0fb2a-131">在**输入 ID** 字段中，输入 **1**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-131">In the **Enter Id** field, enter **1**.</span></span>
6. <span data-ttu-id="0fb2a-132">将**创建基准文件**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-132">Set the **Make baseline files** option to **Yes**.</span></span>
7. <span data-ttu-id="0fb2a-133">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-133">Select **OK**.</span></span>

    <span data-ttu-id="0fb2a-134">![“电子报表参数”对话框](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "“电子报表参数”对话框的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="0fb2a-134">![Electronic report parameters dialog box](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "Screenshot of the Electronic report parameters dialog box")</span></span>

8. <span data-ttu-id="0fb2a-135">选择**基准**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-135">Select **Baselines**.</span></span>

    <span data-ttu-id="0fb2a-136">![“电子申报格式基准”页](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "“电子申报格式基准”页的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="0fb2a-136">![Electronic reporting format baselines page](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

    <span data-ttu-id="0fb2a-137">已将生成的出站文件自动附加到执行的 ER 格式的基准。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-137">The generated outbound file has been automatically attached to the baseline of the executed ER format.</span></span> <span data-ttu-id="0fb2a-138">基准规则已自动添加到此基准，其中还包含对附加的文件的引用。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-138">The baseline rule has been automatically added to this baseline and also contains the reference to the attached file.</span></span>

9. <span data-ttu-id="0fb2a-139">在**名称**字段中，输入**基准 1**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-139">In the **Name** field, enter **Baseline 1**.</span></span>
10. <span data-ttu-id="0fb2a-140">在**文件名掩码**字段中，输入 **.xml**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-140">In the **File name mask** field, enter **.xml**.</span></span>
11. <span data-ttu-id="0fb2a-141">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-141">Select **Save**.</span></span>

### <a name="run-the-format"></a><span data-ttu-id="0fb2a-142">运行格式</span><span class="sxs-lookup"><span data-stu-id="0fb2a-142">Run the format</span></span>

<span data-ttu-id="0fb2a-143">现在已准备就绪，可以从“运行设计的 ER 格式和检查日志以分析结果”部分开始，完成[跟踪生成的报表结果并将其与基准值进行比较](er-trace-reports-compare-baseline.md)主题中的示例中的步骤。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-143">You're now ready to complete the remaining steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, starting from the "Run the designed ER format and review the log to analyze the results" section.</span></span>

> [!NOTE]
> <span data-ttu-id="0fb2a-144">在**基准**快速选项卡上删除自动添加的基准规则时，不会自动删除引用的附件。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-144">When you delete the automatically added baseline rule on the **Baselines** FastTab, the referenced attachment isn't automatically deleted.</span></span>

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="0fb2a-145">配置基准，使其忽略持续改变的 ER 输出部分</span><span class="sxs-lookup"><span data-stu-id="0fb2a-145">Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="0fb2a-146">如果已将 ER 格式设计为包含运行该格式时更改的信息，需要此格式才能使用 ER 基准功能将生成的结果与基准值进行比较。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-146">When an ER format has been designed to contain information that is changed when the format is run, the format must be required to use the ER baseline feature to compare the generated results with baseline values.</span></span> <span data-ttu-id="0fb2a-147">例如，此信息可能是处理日期和时间，或不同格式中生成的文档的唯一标识符（全局唯一标识符 \[GUID\] 等）。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-147">For example, the information might be the processing date and time or the unique identifier of a generated document in different formats (globally unique identifier \[GUID\], and so on).</span></span> <span data-ttu-id="0fb2a-148">可通过新的 ER 功能配置基准规则，以便在为了将基准值与 ER 格式的执行结果进行比较而运行格式时忽略该格式的可更改元素。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-148">The new ER capabilities let you configure the baseline rule so that it ignores changeable elements of an ER format when the format is run with the purpose of comparing baseline values with the results of the format's execution.</span></span> <span data-ttu-id="0fb2a-149">若要了解有关此功能的详细信息，请完成以下示例。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-149">To learn more about this feature, complete the following example.</span></span>

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="0fb2a-150">示例：配置基准，使其忽略持续改变的 ER 输出部分</span><span class="sxs-lookup"><span data-stu-id="0fb2a-150">Example: Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="0fb2a-151">若要完成此示例中的步骤，必须先完成[跟踪生成的报表结果并将其与基准值进行比较](er-trace-reports-compare-baseline.md)主题中的示例的步骤。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-151">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic.</span></span>

### <a name="modify-a-configured-er-format"></a><span data-ttu-id="0fb2a-152">修改配置的 ER 格式</span><span class="sxs-lookup"><span data-stu-id="0fb2a-152">Modify a configured ER format</span></span>

1. <span data-ttu-id="0fb2a-153">转到**组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-153">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0fb2a-154">在树中，展开**用于了解 ER 基准的模型**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-154">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="0fb2a-155">在树中，选择**用于了解 ER 基准的模型\\用于了解 ER 基准的格式**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-155">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="0fb2a-156">选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-156">Select **Designer**.</span></span>
5. <span data-ttu-id="0fb2a-157">在树中，选择**输出\\文档**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-157">In the tree, select **Output\\Document**.</span></span>
6. <span data-ttu-id="0fb2a-158">选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-158">Select **Add**.</span></span>
7. <span data-ttu-id="0fb2a-159">在下拉对话框中的树中，选择 **XML\\属性**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-159">In the drop-down dialog box, in the tree, select **XML\\Attribute**.</span></span>
8. <span data-ttu-id="0fb2a-160">在**名称**字段中，输入 **ProcessingDateTime**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-160">In the **Name** field, enter **ProcessingDateTime**.</span></span>
9. <span data-ttu-id="0fb2a-161">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-161">Select **OK**.</span></span>
10. <span data-ttu-id="0fb2a-162">在**映射**选项卡上的树中，选择**输出\\文档\\ProcessingDateTime**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-162">On the **Mapping** tab, in the tree, select **Output\\Document\\ProcessingDateTime**.</span></span>
11. <span data-ttu-id="0fb2a-163">选择**编辑公式**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-163">Select **Edit formula**.</span></span>
12. <span data-ttu-id="0fb2a-164">在**公式**字段中，输入下面的表达式：**DATETIMEFORMAT(NOW(), "O")**</span><span class="sxs-lookup"><span data-stu-id="0fb2a-164">In the **Formula** field, enter the following expression: **DATETIMEFORMAT(NOW(), "O")**</span></span>
13. <span data-ttu-id="0fb2a-165">选择**保存**，然后选择**测试**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-165">Select **Save**, and then select **Test**.</span></span>
14. <span data-ttu-id="0fb2a-166">再次选择**测试**重新测试配置的表达式。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-166">Select **Test** again to retest the configured expression.</span></span>

    <span data-ttu-id="0fb2a-167">![“公式设计器”页](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "“公式设计器”页的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="0fb2a-167">![Formula designer page](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Screenshot of the Formula designer page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="0fb2a-168">**测试结果**选项卡显示配置的表达式只要被调用，都会返回不同的日期和时间值。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-168">The **Test result** tab shows that the configured expression returns a different date and time value whenever it's called.</span></span>

15. <span data-ttu-id="0fb2a-169">关闭**公式设计器**页，然后选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-169">Close the **Formula designer** page, and then select **Save**.</span></span>

    <span data-ttu-id="0fb2a-170">![“格式设计器”页](media/GER-BaselineSample-FormatMappingDesign2.PNG "“格式设计器”页的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="0fb2a-170">![Format designer page](media/GER-BaselineSample-FormatMappingDesign2.PNG "Screenshot of the Format designer page")</span></span>

16. <span data-ttu-id="0fb2a-171">关闭**格式设计器**页。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-171">Close the **Format designer** page.</span></span>

### <a name="remove-an-existing-baseline-rule"></a><span data-ttu-id="0fb2a-172">删除现有基准规则</span><span class="sxs-lookup"><span data-stu-id="0fb2a-172">Remove an existing baseline rule</span></span>

1. <span data-ttu-id="0fb2a-173">转到**组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-173">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0fb2a-174">选择**基准**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-174">Select **Baselines**.</span></span>
3. <span data-ttu-id="0fb2a-175">在基准列表中，选择为**用于了解 ER 基准的格式**格式配置的基准。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-175">In the list of baselines, select the baseline that is configured for the **Format to learn ER baselines** format.</span></span>
4. <span data-ttu-id="0fb2a-176">在**基准**快速选项卡上，选择**删除**以删除前面配置的基准规则。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-176">On the **Baselines** FastTab, select **Delete** to remove the baseline rule that you configured earlier.</span></span>

<span data-ttu-id="0fb2a-177">![“电子申报格式基准”页](media/GER-BaselineSample-AddBaseline3.PNG "“电子申报格式基准”页的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="0fb2a-177">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline3.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="define-replacements-for-bindings-of-designed-er-format"></a><span data-ttu-id="0fb2a-178">为设计的 ER 格式的绑定定义替换项</span><span class="sxs-lookup"><span data-stu-id="0fb2a-178">Define replacements for bindings of designed ER format</span></span>

1. <span data-ttu-id="0fb2a-179">在**配置**页的**替换**快速选项卡上，选择**选择组件**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-179">On the **Configurations** page, on the **Replacements** FastTab, select **Select components**.</span></span>
2. <span data-ttu-id="0fb2a-180">在格式组件树中，展开**输出**，展开**输出\\文档**，然后选中**输出\\文档\\ProcessingDateTime** 的复选框。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-180">In the format components tree, expand **Output**, expand **Output\\Document**, and then select the check box for **Output\\Document\\ProcessingDateTime**.</span></span>

    <span data-ttu-id="0fb2a-181">![“选择组件”对话框](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "“选择组件”对话框的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="0fb2a-181">![Select Components dialog box](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "Screenshot of the Select Components dialog box")</span></span>

3. <span data-ttu-id="0fb2a-182">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-182">Select **OK**.</span></span>

<span data-ttu-id="0fb2a-183">![“电子申报格式基准”页](media/GER-BaselineSample-AddBaseline4.PNG "“电子申报格式基准”页的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="0fb2a-183">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline4.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

<span data-ttu-id="0fb2a-184">已将选择的 ER 格式组件添加到了**替换**快速选项卡上的组件列表中。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-184">The selected ER format component has been added to the list of components on the **Replacements** FastTab.</span></span> <span data-ttu-id="0fb2a-185">以调试模式运行基本 ER 格式时，将把该格式每个组件的绑定替换为**绑定**列中的绑定。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-185">When the base ER format is run in debug mode, the format's binding for each component will be replaced by the binding that is shown in the **Binding** column.</span></span> <span data-ttu-id="0fb2a-186">若要更改**替换**快速选项卡上列出的组件的默认绑定，请选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-186">To change the default binding for a component that is listed on the **Replacements** FastTab, select **Edit**.</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="0fb2a-187">新建基准规则</span><span class="sxs-lookup"><span data-stu-id="0fb2a-187">Make a new baseline rule</span></span>

<span data-ttu-id="0fb2a-188">执行本主题前文“示例：自动执行基准规则的设置”部分中的步骤。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-188">Follow the steps in the "Example: Automate the setting of baseline rules" section earlier in this topic.</span></span> <span data-ttu-id="0fb2a-189">将有一个通知警告您已使用基准设置生成了出站文件，并且已强制替换了格式绑定。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-189">A notification warns you that the outbound file has been generated by using baseline settings, and that a forced replacement of the format bindings has occurred.</span></span>

<span data-ttu-id="0fb2a-190">![“配置”页上的通知](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "“配置”页上的通知的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="0fb2a-190">![Notification on the Configurations page](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Screenshot of the notification on the Configurations page")</span></span>

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a><span data-ttu-id="0fb2a-191">禁止显示有关替换格式绑定的警告</span><span class="sxs-lookup"><span data-stu-id="0fb2a-191">Suppress warnings about the replacement of format bindings</span></span>

<span data-ttu-id="0fb2a-192">通过设置特定 ER 参数，可禁止显示用于警示更换格式绑定的通知。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-192">By setting specific ER parameters, you can suppress notifications that warn about the replacement of format bindings.</span></span> <span data-ttu-id="0fb2a-193">使用 Regression Suite Automation Tool 以无人值守模式替换格式绑定时，此项禁止显示可能很有用。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-193">This suppression can be useful when format bindings are replaced in an unattended mode by using the Regression Suite Automation Tool.</span></span> <span data-ttu-id="0fb2a-194">在此情况下，可以将警告视为正在运行的测试用例失败。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-194">In this case, the warning can be considered a failure of the test case that is running.</span></span>

1. <span data-ttu-id="0fb2a-195">在**配置**页操作窗格中的**配置**选项卡上，选择**用户参数**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
2. <span data-ttu-id="0fb2a-196">将**禁止显示基准警告**选项设置为**是**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-196">Set the **Suppress baseline warnings** option to **Yes**, and then select **OK**.</span></span>

<span data-ttu-id="0fb2a-197">![“用户参数”对话框](media/GER-BaselineSample-ERUserParameters1.png "“用户参数”对话框的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="0fb2a-197">![User parameters dialog box](media/GER-BaselineSample-ERUserParameters1.png "Screenshot of the User parameters dialog box")</span></span>

### <a name="review-the-generated-baseline-file"></a><span data-ttu-id="0fb2a-198">检查生成的基准文件</span><span class="sxs-lookup"><span data-stu-id="0fb2a-198">Review the generated baseline file</span></span>

1. <span data-ttu-id="0fb2a-199">转到**组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-199">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0fb2a-200">选择**基准**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-200">Select **Baselines**.</span></span>
3. <span data-ttu-id="0fb2a-201">选择**附件**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-201">Select **Attachments**.</span></span>

    <span data-ttu-id="0fb2a-202">![“附件”页](media/GER-BaselineSample-AttachedBaselineFile.PNG "“附件”页的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="0fb2a-202">![Attachments page](media/GER-BaselineSample-AttachedBaselineFile.PNG "Screenshot of the Attachments page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="0fb2a-203">生成的文件中包含来自添加的基准规则中配置的绑定，而不是来自格式的绑定的处理日期和时间文本 (**"#"**)。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-203">The generated file contains the processing date and time text (**"#"**) from the binding that was configured in the added baseline rule, not from the format's binding.</span></span>

4. <span data-ttu-id="0fb2a-204">关闭**附件**页。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-204">Close the **Attachments** page.</span></span>

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a><span data-ttu-id="0fb2a-205">运行设计的 ER 格式和检查日志以分析结果</span><span class="sxs-lookup"><span data-stu-id="0fb2a-205">Run the designed ER format and review the log to analyze the results</span></span>

1. <span data-ttu-id="0fb2a-206">转到**组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-206">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0fb2a-207">在树中，展开**用于了解 ER 基准的模型**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-207">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="0fb2a-208">在树中，选择**用于了解 ER 基准的模型\\用于了解 ER 基准的格式**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-208">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="0fb2a-209">在**版本**快速选项卡上，选择**运行**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-209">On the **Versions** FastTab select **Run**.</span></span>
5. <span data-ttu-id="0fb2a-210">在**输入 ID** 字段中，键入 **1**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-210">In the **Enter Id** field, type **1**.</span></span>
6. <span data-ttu-id="0fb2a-211">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-211">Select **OK**.</span></span>
7. <span data-ttu-id="0fb2a-212">转到**组织管理** \> **电子申报** \> **配置调试日志**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-212">Go to **Organization administration** \> **Electronic reporting** \> **Configuration debug logs**.</span></span>

<span data-ttu-id="0fb2a-213">执行日志中包含有关所生成文件与所配置基准的比较结果的信息。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-213">The execution log contains information about the results of the comparison of the generated file with the configured baseline.</span></span> <span data-ttu-id="0fb2a-214">此日志指示生成的文件与基准相等，即使执行的格式中包含绑定以在出站文件中输入持续改变的日期和时间值。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-214">The log indicates that the generated file and the baseline are equal, even though the executed format contains the binding to enter a constantly changing date and time value in the outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="0fb2a-215">尽管已通过用于强制替换格式的绑定的基准设置生成了出站文件，您仍然不会收到有关替换的警告。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-215">Although the outbound file has been generated by using baseline settings that force the replacement of the format's bindings, you don't receive any warnings about the replacement.</span></span>

## <a name="exchange-baseline-settings-between-environments"></a><span data-ttu-id="0fb2a-216">在环境之间交换基准设置</span><span class="sxs-lookup"><span data-stu-id="0fb2a-216">Exchange baseline settings between environments</span></span>

### <a name="export-baseline-settings"></a><span data-ttu-id="0fb2a-217">导出基准设置</span><span class="sxs-lookup"><span data-stu-id="0fb2a-217">Export baseline settings</span></span>

<span data-ttu-id="0fb2a-218">可通过新的 ER 功能将所选 ER 格式的基准设置从当前 Finance and Operations 环境导出并作为 XML 文件存储。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-218">The new ER capabilities let you export baseline settings for the selected ER format from the current Finance and Operations environment and store them as XML files.</span></span> 

<span data-ttu-id="0fb2a-219">若要导出基准设置，请在**电子申报格式基准**页上选择**导出**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-219">To export baseline settings, on the **Electronic reporting format baselines** page, select **Export**.</span></span>

### <a name="import-baseline-settings"></a><span data-ttu-id="0fb2a-220">导入基线设置</span><span class="sxs-lookup"><span data-stu-id="0fb2a-220">Import baseline settings</span></span>

<span data-ttu-id="0fb2a-221">可将导出的基准设置导入到其他 Finance and Operations 环境中。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-221">Exported baseline settings can be imported into a different Finance and Operations environment.</span></span> <span data-ttu-id="0fb2a-222">首先必须将该环境作为 ER 格式导入。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-222">The environment must first be imported as an ER format.</span></span> <span data-ttu-id="0fb2a-223">然后可以导入基准设置。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-223">You can then import the baseline settings.</span></span>

<span data-ttu-id="0fb2a-224">若要从本地存储的 XML 文件导入基准设置，请在**电子申报格式基准**页上选择**导入**，然后选择**浏览**以选择该 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-224">To import baseline settings from a locally stored XML file, on the **Electronic reporting format baselines** page, select **Import**, and then select **Browse** to select the XML file.</span></span>

<span data-ttu-id="0fb2a-225">![“导入基准设置”对话框](media/GER-BaselineSample-ImportBaseline1.PNG "“导入基准设置”对话框的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="0fb2a-225">![Import baseline settings dialog box](media/GER-BaselineSample-ImportBaseline1.PNG "Screenshot of the Import baseline settings dialog box")</span></span>

<span data-ttu-id="0fb2a-226">若要基于当前文档管理设置和所选文档类型从 Microsoft SharePoint Server 中存储的 XML 文件导入基准设置，请在**电子申报格式基准**页上选择**从来源导入**。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-226">To import baseline settings from an XML file that is stored on the Microsoft SharePoint Server, based on the current Document management settings and the selected document type, on the **Electronic reporting format baselines** page, select **Import from source**.</span></span> <span data-ttu-id="0fb2a-227">然后选择文档类型和 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-227">Then select the document type and the XML file.</span></span> <span data-ttu-id="0fb2a-228">必须提前配置访问 SharePoint 文件夹所需文档类型。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-228">The required document type to access the SharePoint folder must be configured in advance.</span></span>

<span data-ttu-id="0fb2a-229">![“从来源导入”对话框](media/GER-BaselineSample-ImportBaseline2.PNG "“从来源导入”对话框的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="0fb2a-229">![Import from source dialog box](media/GER-BaselineSample-ImportBaseline2.PNG "Screenshot of the Import from source dialog box")</span></span>

> [!NOTE]
> <span data-ttu-id="0fb2a-230">可使用任务录制器录制在**从来源导入**对话框中选择所需文档类型和文件名的步骤。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-230">You can use Task recorder to record the steps for selecting the required document type and the file name in the **Import from source** dialog box.</span></span> <span data-ttu-id="0fb2a-231">这样就可以将所需基准设置保存在 SharePoint Server 上，然后在使用 Regression Suite Automation Tool 运行自动化任务时通过播放任务录制自动导入。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-231">In this way, you can keep required baseline settings on SharePoint Server and then automatically import them by playing a task recording when you run automated tests by using the Regression Suite Automation Tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0fb2a-232">其他资源</span><span class="sxs-lookup"><span data-stu-id="0fb2a-232">Additional resources</span></span>

- [<span data-ttu-id="0fb2a-233">跟踪生成的报表结果并将其与基准值进行比较。</span><span class="sxs-lookup"><span data-stu-id="0fb2a-233">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="0fb2a-234">任务录制器</span><span class="sxs-lookup"><span data-stu-id="0fb2a-234">Task recorder</span></span>](../user-interface/task-recorder.md)
