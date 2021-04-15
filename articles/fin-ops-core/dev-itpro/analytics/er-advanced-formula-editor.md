---
title: 电子报告高级公式编辑器
description: 本主题描述如何使用高级公式编辑器来配置电子报告 (ER) 模型映射和格式组件中的表达式。
author: NickSelin
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: d18aeedb2f21176ffe964b926168d4bf088a093b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751200"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="09484-103">电子报告高级公式编辑器</span><span class="sxs-lookup"><span data-stu-id="09484-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09484-104">除了[电子报告](general-electronic-reporting.md)[公式编辑器](general-electronic-reporting-formula-designer.md)之外，您还可以使用高级电子报告公式编辑器来改善配置电子报告 (ER) 表达式的体验。</span><span class="sxs-lookup"><span data-stu-id="09484-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="09484-105">高级编辑器基于浏览器，由 [Monaco 编辑器](https://microsoft.github.io/monaco-editor)提供支持。</span><span class="sxs-lookup"><span data-stu-id="09484-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="09484-106">本主题介绍了最常用的高级编辑器功能：</span><span class="sxs-lookup"><span data-stu-id="09484-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="09484-107">代码自动格式化</span><span class="sxs-lookup"><span data-stu-id="09484-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="09484-108">IntelliSense</span><span class="sxs-lookup"><span data-stu-id="09484-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="09484-109">代码完成</span><span class="sxs-lookup"><span data-stu-id="09484-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="09484-110">代码导航</span><span class="sxs-lookup"><span data-stu-id="09484-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="09484-111">代码构造</span><span class="sxs-lookup"><span data-stu-id="09484-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="09484-112">查找和替换</span><span class="sxs-lookup"><span data-stu-id="09484-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="09484-113">数据粘贴</span><span class="sxs-lookup"><span data-stu-id="09484-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="09484-114">语法着色</span><span class="sxs-lookup"><span data-stu-id="09484-114">Syntax colorization</span></span>](#SyntaxColorization)

## <a name=""></a><span data-ttu-id="09484-115"><a name="ActivateAdvEditor">激活高级公式编辑器</a></span><span class="sxs-lookup"><span data-stu-id="09484-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="09484-116">完成以下步骤，开始在您的 Microsoft Dynamics 365 Finance 实例中使用高级公式编辑器。</span><span class="sxs-lookup"><span data-stu-id="09484-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="09484-117">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="09484-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="09484-118">在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。</span><span class="sxs-lookup"><span data-stu-id="09484-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="09484-119">在 **用户参数** 对话框内的 **执行跟踪** 部分中，将 **启用高级公式编辑器** 参数设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="09484-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="09484-120">[![ER 配置页](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="09484-120">[![ER configurations page](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="09484-121">请注意，此参数特定于用户和公司。</span><span class="sxs-lookup"><span data-stu-id="09484-121">Be aware that this parameter is user specific and company specific.</span></span>

## <a name=""></a><span data-ttu-id="09484-122"><a name="Autoformatting">代码自动格式化</a></span><span class="sxs-lookup"><span data-stu-id="09484-122"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="09484-123">当您编写包含多行代码的复杂表达式时，新输入行的缩进将基于前一行的缩进自动进行。</span><span class="sxs-lookup"><span data-stu-id="09484-123">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="09484-124">您可以按 **Tab** 或 **Shift+Tab** 来选择行并更改其缩进量。</span><span class="sxs-lookup"><span data-stu-id="09484-124">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="09484-125">[![ER 公式编辑器](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="09484-125">[![ER formula editor](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="09484-126">自动格式化可让整个表达式的格式保持正确，以使进一步的维护更加容易，并简化对已配置逻辑的理解。</span><span class="sxs-lookup"><span data-stu-id="09484-126">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <a name=""></a><span data-ttu-id="09484-127"><a name="IntelliSense">IntelliSense</a></span><span class="sxs-lookup"><span data-stu-id="09484-127"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="09484-128">该编辑器提供了单词补全功能，可帮助您更快地编写表达式并避免输入错误。</span><span class="sxs-lookup"><span data-stu-id="09484-128">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="09484-129">当您开始添加新文本时，编辑器会自动提供 ER 函数支持的函数列表，其中包含您输入的字符。</span><span class="sxs-lookup"><span data-stu-id="09484-129">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="09484-130">您还可以通过按 **Ctrl + 空格键** 在已配置表达式的任何位置触发 IntelliSense。</span><span class="sxs-lookup"><span data-stu-id="09484-130">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="09484-131">[![ER 公式编辑器](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="09484-131">[![ER formula editor](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <a name=""></a><span data-ttu-id="09484-132"><a name="CodeCompletion">代码完成</a></span><span class="sxs-lookup"><span data-stu-id="09484-132"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="09484-133">编辑器通过以下方式自动完成代码：</span><span class="sxs-lookup"><span data-stu-id="09484-133">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="09484-134">输入开括号时插入一个闭括号，将光标保持在括号内。</span><span class="sxs-lookup"><span data-stu-id="09484-134">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="09484-135">输入第一个引号时，插入第二个引号，使光标保持在引号内。</span><span class="sxs-lookup"><span data-stu-id="09484-135">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="09484-136">输入第一个双引号时，插入第二个双引号，使光标保持在引号内。</span><span class="sxs-lookup"><span data-stu-id="09484-136">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="09484-137">[![ER 公式编辑器](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="09484-137">[![ER formula editor](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="09484-138">当您指向键入的括号时，该括号对的第二个括号将自动突出显示以显示其支持的结构。</span><span class="sxs-lookup"><span data-stu-id="09484-138">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <a name=""></a><span data-ttu-id="09484-139"><a name="CodeNavigation">代码导航</a></span><span class="sxs-lookup"><span data-stu-id="09484-139"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="09484-140">通过使用命令面板或上下文菜单键入 **转到** 命令，您可以在表达式中找到所需的符号或行。</span><span class="sxs-lookup"><span data-stu-id="09484-140">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="09484-141">例如，要跳到第 **8** 行，请执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="09484-141">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="09484-142">按 **Ctrl+G**，输入值 **8**，然后按 **Enter**。</span><span class="sxs-lookup"><span data-stu-id="09484-142">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="09484-143">- 或者 -</span><span class="sxs-lookup"><span data-stu-id="09484-143">-or-</span></span>

- <span data-ttu-id="09484-144">按 **F1**，键入 **G**，选择 **转到行**，输入值 **8**，然后按 **Enter**。</span><span class="sxs-lookup"><span data-stu-id="09484-144">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="09484-145">[![ER 公式编辑器](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="09484-145">[![ER formula editor](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <a name=""></a><span data-ttu-id="09484-146"><a name="CodeStructuring">代码构造</a></span><span class="sxs-lookup"><span data-stu-id="09484-146"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="09484-147">某些函数（例如 [IF](er-functions-logical-if.md) 或 [CASE](er-functions-logical-case.md)）的代码是自动构建的。</span><span class="sxs-lookup"><span data-stu-id="09484-147">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="09484-148">您可以扩展和折叠此代码的任何或所有折叠区域，以减少表达式的可编辑部分，从而仅关注需要注意的那段代码。</span><span class="sxs-lookup"><span data-stu-id="09484-148">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="09484-149">切换折叠/展开命令可用于此目的。</span><span class="sxs-lookup"><span data-stu-id="09484-149">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="09484-150">例如，要折叠所有区域，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="09484-150">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="09484-151">按 **Ctrl+K**</span><span class="sxs-lookup"><span data-stu-id="09484-151">Press **Ctrl+K**</span></span>

  <span data-ttu-id="09484-152">- 或者 -</span><span class="sxs-lookup"><span data-stu-id="09484-152">-or-</span></span>

- <span data-ttu-id="09484-153">按 **F1**，按 **FO**，选择 **全部折叠**，然后按 **Enter**</span><span class="sxs-lookup"><span data-stu-id="09484-153">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="09484-154">要展开所有区域，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="09484-154">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="09484-155">按 **Ctrl+J**</span><span class="sxs-lookup"><span data-stu-id="09484-155">Press **Ctrl+J**</span></span>

  <span data-ttu-id="09484-156">- 或者 -</span><span class="sxs-lookup"><span data-stu-id="09484-156">-or-</span></span>
  
- <span data-ttu-id="09484-157">按 **F1**，键入 **UN**，选择 **全部展开**，然后按 **Enter**</span><span class="sxs-lookup"><span data-stu-id="09484-157">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="09484-158">[![ER 公式编辑器](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="09484-158">[![ER formula editor](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <a name=""></a><span data-ttu-id="09484-159"><a name="FindAndReplace">查找和替换</a></span><span class="sxs-lookup"><span data-stu-id="09484-159"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="09484-160">要查找出现的某些文本，请在表达式中选择此文本，然后执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="09484-160">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="09484-161">按 **Ctrl+F**，然后按 **F3** 查找下一处所选文本，或按 **Shift+F3** 查找上一处。</span><span class="sxs-lookup"><span data-stu-id="09484-161">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="09484-162">- 或者 -</span><span class="sxs-lookup"><span data-stu-id="09484-162">-or-</span></span>
  
- <span data-ttu-id="09484-163">按 **F1**，键入 **F**，然后选择所需的选项以查找选定的文本。</span><span class="sxs-lookup"><span data-stu-id="09484-163">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="09484-164">要替换出现的某些文本，请在表达式中选择此文本，然后执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="09484-164">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="09484-165">按 **Ctrl+H**。</span><span class="sxs-lookup"><span data-stu-id="09484-165">Press **Ctrl+H**.</span></span> <span data-ttu-id="09484-166">输入替代文本，然后选择替换选项，以替换当前表达式中的所选文本或所出现的所有此文本。</span><span class="sxs-lookup"><span data-stu-id="09484-166">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="09484-167">- 或者 -</span><span class="sxs-lookup"><span data-stu-id="09484-167">-or-</span></span>
  
- <span data-ttu-id="09484-168">按 **F1**，键入 **R**，然后选择所需的选项以替代选定的文本。</span><span class="sxs-lookup"><span data-stu-id="09484-168">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="09484-169">输入替代文本，然后选择替换选项，以替换当前表达式中的所选文本或所出现的所有此文本。</span><span class="sxs-lookup"><span data-stu-id="09484-169">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="09484-170">要更改出现的所有某些文本，请在表达式中选择此文本，然后执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="09484-170">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="09484-171">按 **Ctrl+F2**，然后输入替代文本。</span><span class="sxs-lookup"><span data-stu-id="09484-171">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="09484-172">- 或者 -</span><span class="sxs-lookup"><span data-stu-id="09484-172">-or-</span></span>
  
- <span data-ttu-id="09484-173">按 **F1**，键入 **C**，然后选择所需的选项以更改选定的文本。</span><span class="sxs-lookup"><span data-stu-id="09484-173">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="09484-174">输入替换文本。</span><span class="sxs-lookup"><span data-stu-id="09484-174">Enter the alternative text.</span></span>

<span data-ttu-id="09484-175">[![ER 公式编辑器](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="09484-175">[![ER formula editor](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <a name=""></a><span data-ttu-id="09484-176"><a name="DataPasting">数据源和函数粘贴</a></span><span class="sxs-lookup"><span data-stu-id="09484-176"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="09484-177">您可以选择 **添加数据源**，这会将当前在 **数据源** 左面板中选择的数据源粘贴到当前表达式中。</span><span class="sxs-lookup"><span data-stu-id="09484-177">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="09484-178">同样，您可以选择 **添加函数**，这会将当前在 **函数** 右面板中选择的函数粘贴到当前表达式中。</span><span class="sxs-lookup"><span data-stu-id="09484-178">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="09484-179">如果使用 ER 公式编辑器，则所选函数或所选数据源将始终粘贴到已配置表达式的末尾。</span><span class="sxs-lookup"><span data-stu-id="09484-179">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="09484-180">如果使用高级 ER 公式编辑器，则可以将所选函数或所选数据源粘贴到已配置表达式的任何部分中。</span><span class="sxs-lookup"><span data-stu-id="09484-180">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="09484-181">您将需要使用光标来指定要粘贴数据的位置。</span><span class="sxs-lookup"><span data-stu-id="09484-181">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="09484-182">[![ER 公式编辑器](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="09484-182">[![ER formula editor](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <a name=""></a><span data-ttu-id="09484-183"><a name="SyntaxColorization">语法着色</a></span><span class="sxs-lookup"><span data-stu-id="09484-183"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="09484-184">当前，使用了不同的颜色来突出显示表达式的以下部分：</span><span class="sxs-lookup"><span data-stu-id="09484-184">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="09484-185">双括号中可以表示文本常量的标签 ID 的文本。</span><span class="sxs-lookup"><span data-stu-id="09484-185">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="09484-186">[![ER 公式编辑器](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="09484-186">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="limitations"></a><span data-ttu-id="09484-187">限制</span><span class="sxs-lookup"><span data-stu-id="09484-187">Limitations</span></span>

<span data-ttu-id="09484-188">以下 Web 浏览器中现在支持此编辑器。</span><span class="sxs-lookup"><span data-stu-id="09484-188">The editor is currently supported in the following web browsers:</span></span>

- <span data-ttu-id="09484-189">Chrome</span><span class="sxs-lookup"><span data-stu-id="09484-189">Chrome</span></span>
- <span data-ttu-id="09484-190">Edge</span><span class="sxs-lookup"><span data-stu-id="09484-190">Edge</span></span>
- <span data-ttu-id="09484-191">Firefox</span><span class="sxs-lookup"><span data-stu-id="09484-191">Firefox</span></span>
- <span data-ttu-id="09484-192">Opera</span><span class="sxs-lookup"><span data-stu-id="09484-192">Opera</span></span>
- <span data-ttu-id="09484-193">Safari</span><span class="sxs-lookup"><span data-stu-id="09484-193">Safari</span></span>

## <a name="additional-resources"></a><span data-ttu-id="09484-194">其他资源</span><span class="sxs-lookup"><span data-stu-id="09484-194">Additional resources</span></span>

- [<span data-ttu-id="09484-195">电子报告 (ER) 概览</span><span class="sxs-lookup"><span data-stu-id="09484-195">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="09484-196">电子报告中的配方设计器</span><span class="sxs-lookup"><span data-stu-id="09484-196">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="09484-197">Monaco 编辑</span><span class="sxs-lookup"><span data-stu-id="09484-197">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]