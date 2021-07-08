---
title: 电子报告高级公式编辑器
description: 本主题描述如何使用高级公式编辑器来配置电子报告 (ER) 模型映射和格式组件中的表达式。
author: NickSelin
ms.date: 06/17/2021
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
ms.openlocfilehash: f7f80928e1d3f5d4892f72d4bd2fd09b70a26c1f
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270699"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="8eebf-103">电子报告高级公式编辑器</span><span class="sxs-lookup"><span data-stu-id="8eebf-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8eebf-104">除了[电子报告](general-electronic-reporting.md)[公式编辑器](general-electronic-reporting-formula-designer.md)之外，您还可以使用高级电子报告公式编辑器来改善配置电子报告 (ER) 表达式的体验。</span><span class="sxs-lookup"><span data-stu-id="8eebf-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="8eebf-105">高级编辑器基于浏览器，由 [Monaco 编辑器](https://microsoft.github.io/monaco-editor)提供支持。</span><span class="sxs-lookup"><span data-stu-id="8eebf-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="8eebf-106">本主题介绍了最常用的高级编辑器功能：</span><span class="sxs-lookup"><span data-stu-id="8eebf-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="8eebf-107">代码自动格式化</span><span class="sxs-lookup"><span data-stu-id="8eebf-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="8eebf-108">IntelliSense</span><span class="sxs-lookup"><span data-stu-id="8eebf-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="8eebf-109">代码完成</span><span class="sxs-lookup"><span data-stu-id="8eebf-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="8eebf-110">代码导航</span><span class="sxs-lookup"><span data-stu-id="8eebf-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="8eebf-111">代码构造</span><span class="sxs-lookup"><span data-stu-id="8eebf-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="8eebf-112">查找和替换</span><span class="sxs-lookup"><span data-stu-id="8eebf-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="8eebf-113">数据粘贴</span><span class="sxs-lookup"><span data-stu-id="8eebf-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="8eebf-114">语法着色</span><span class="sxs-lookup"><span data-stu-id="8eebf-114">Syntax colorization</span></span>](#SyntaxColorization)

## <a name=""></a><span data-ttu-id="8eebf-115"><a name="ActivateAdvEditor">激活高级公式编辑器</a></span><span class="sxs-lookup"><span data-stu-id="8eebf-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="8eebf-116">完成以下步骤，开始在您的 Microsoft Dynamics 365 Finance 实例中使用高级公式编辑器。</span><span class="sxs-lookup"><span data-stu-id="8eebf-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="8eebf-117">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="8eebf-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="8eebf-118">在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。</span><span class="sxs-lookup"><span data-stu-id="8eebf-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="8eebf-119">在 **用户参数** 对话框内的 **执行跟踪** 部分中，将 **启用高级公式编辑器** 参数设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="8eebf-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="8eebf-120">[![用户参数对话框，突出显示了启用高级公式编辑器参数](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="8eebf-120">[![User parameters dialog box, Enable advanced formula editor parameter highlighted](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="8eebf-121">请注意，此参数特定于用户和公司。</span><span class="sxs-lookup"><span data-stu-id="8eebf-121">Be aware that this parameter is user specific and company specific.</span></span>

<span data-ttu-id="8eebf-122">从 Microsoft Dynamics 365 Finance 版本 10.0.19 开始，您可以控制默认提供的 ER 公式编辑器。</span><span class="sxs-lookup"><span data-stu-id="8eebf-122">Starting in Microsoft Dynamics 365 Finance version 10.0.19, you can control what ER formula editor is offered by default.</span></span> <span data-ttu-id="8eebf-123">完成以下步骤，为当前 Finance 实例的所有用户和公司启用高级公式编辑器。</span><span class="sxs-lookup"><span data-stu-id="8eebf-123">Complete the following steps to enable the advanced formula editor for all users and companies of the current Finance instance.</span></span>

1.  <span data-ttu-id="8eebf-124">打开 **功能管理** 工作区。</span><span class="sxs-lookup"><span data-stu-id="8eebf-124">Open the **Feature management** workspace.</span></span>
2.  <span data-ttu-id="8eebf-125">在列表中查找并选择功能 **将 ER 高级公式编辑器设置为所有用户的默认编辑器**，然后选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="8eebf-125">Find and select the feature **Set the ER advanced formula editor as the default one for all users** in the list, and then select **Enable now**.</span></span>
3.  <span data-ttu-id="8eebf-126">转到 **组织管理** > **电子申报** > **配置**。</span><span class="sxs-lookup"><span data-stu-id="8eebf-126">Go to **Organization administration** > **Electronic reporting** > **Configurations**.</span></span>
4.  <span data-ttu-id="8eebf-127">在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。</span><span class="sxs-lookup"><span data-stu-id="8eebf-127">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
5.  <span data-ttu-id="8eebf-128">在 **用户参数** 对话框中，查找 **禁用高级公式编辑器** 参数，并验证它是否设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="8eebf-128">In the **User parameters** dialog box, find the **Disable advanced formula editor** parameter and verify that it is set to **No**.</span></span>

<span data-ttu-id="8eebf-129">[![用户参数对话框，突出显示了禁用高级公式编辑器参数](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)</span><span class="sxs-lookup"><span data-stu-id="8eebf-129">[![User parameters dialog box, Disable advanced formula editor parameter highlighted](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)</span></span>

> [!NOTE]
> <span data-ttu-id="8eebf-130">参数 **启用高级公式编辑器** 和 **禁用高级公式编辑器** 的值针对每个用户单独保存，并且在 **用户参数** 对话框上提供，具体取决于 **将 ER 高级公式编辑器设置为所有用户的默认编辑器** 功能的状态。</span><span class="sxs-lookup"><span data-stu-id="8eebf-130">The values of the parameters **Enable advanced formula editor** and **Disable advanced formula editor** are kept separate for each user and offered on the **User parameters** dialog box depending on the status of the **Set the ER advanced formula editor as the default one for all users** feature.</span></span>

## <a name=""></a><span data-ttu-id="8eebf-131"><a name="Autoformatting">代码自动格式化</a></span><span class="sxs-lookup"><span data-stu-id="8eebf-131"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="8eebf-132">当您编写包含多行代码的复杂表达式时，新输入行的缩进将基于前一行的缩进自动进行。</span><span class="sxs-lookup"><span data-stu-id="8eebf-132">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="8eebf-133">您可以按 **Tab** 或 **Shift+Tab** 来选择行并更改其缩进量。</span><span class="sxs-lookup"><span data-stu-id="8eebf-133">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="8eebf-134">[![ER 公式编辑器 gif，显示选择行和更改缩进](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="8eebf-134">[![ER formula editor gif showing selecting lines and changing the indentation](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="8eebf-135">自动格式化可让整个表达式的格式保持正确，以使进一步的维护更加容易，并简化对已配置逻辑的理解。</span><span class="sxs-lookup"><span data-stu-id="8eebf-135">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <a name=""></a><span data-ttu-id="8eebf-136"><a name="IntelliSense">IntelliSense</a></span><span class="sxs-lookup"><span data-stu-id="8eebf-136"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="8eebf-137">该编辑器提供了单词补全功能，可帮助您更快地编写表达式并避免输入错误。</span><span class="sxs-lookup"><span data-stu-id="8eebf-137">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="8eebf-138">当您开始添加新文本时，编辑器会自动提供 ER 函数支持的函数列表，其中包含您输入的字符。</span><span class="sxs-lookup"><span data-stu-id="8eebf-138">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="8eebf-139">您还可以通过按 **Ctrl + 空格键** 在已配置表达式的任何位置触发 IntelliSense。</span><span class="sxs-lookup"><span data-stu-id="8eebf-139">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="8eebf-140">[![ER 公式编辑器 gif，显示触发 IntelliSense](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="8eebf-140">[![ER formula editor gif showing triggering IntelliSense](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <a name=""></a><span data-ttu-id="8eebf-141"><a name="CodeCompletion">代码完成</a></span><span class="sxs-lookup"><span data-stu-id="8eebf-141"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="8eebf-142">编辑器通过以下方式自动完成代码：</span><span class="sxs-lookup"><span data-stu-id="8eebf-142">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="8eebf-143">输入开括号时插入一个闭括号，将光标保持在括号内。</span><span class="sxs-lookup"><span data-stu-id="8eebf-143">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="8eebf-144">输入第一个引号时，插入第二个引号，使光标保持在引号内。</span><span class="sxs-lookup"><span data-stu-id="8eebf-144">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="8eebf-145">输入第一个双引号时，插入第二个双引号，使光标保持在引号内。</span><span class="sxs-lookup"><span data-stu-id="8eebf-145">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="8eebf-146">[![ER 公式编辑器 gif，显示编辑器自动提供代码完成](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="8eebf-146">[![ER formula editor gif showing the editor automatically providing code completion](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="8eebf-147">当您指向键入的括号时，该括号对的第二个括号将自动突出显示以显示其支持的结构。</span><span class="sxs-lookup"><span data-stu-id="8eebf-147">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <a name=""></a><span data-ttu-id="8eebf-148"><a name="CodeNavigation">代码导航</a></span><span class="sxs-lookup"><span data-stu-id="8eebf-148"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="8eebf-149">通过使用命令面板或上下文菜单键入 **转到** 命令，您可以在表达式中找到所需的符号或行。</span><span class="sxs-lookup"><span data-stu-id="8eebf-149">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="8eebf-150">例如，要跳到第 **8** 行，请执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="8eebf-150">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="8eebf-151">按 **Ctrl+G**，输入值 **8**，然后按 **Enter**。</span><span class="sxs-lookup"><span data-stu-id="8eebf-151">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="8eebf-152">- 或者 -</span><span class="sxs-lookup"><span data-stu-id="8eebf-152">-or-</span></span>

- <span data-ttu-id="8eebf-153">按 **F1**，键入 **G**，选择 **转到行**，输入值 **8**，然后按 **Enter**。</span><span class="sxs-lookup"><span data-stu-id="8eebf-153">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="8eebf-154">[![ER 公式编辑器 gif，显示如何使用命令面板定位表达式的各个部分](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="8eebf-154">[![ER formula editor gif showing how to locate parts of an expression using the command palette](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <a name=""></a><span data-ttu-id="8eebf-155"><a name="CodeStructuring">代码构造</a></span><span class="sxs-lookup"><span data-stu-id="8eebf-155"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="8eebf-156">某些函数（例如 [IF](er-functions-logical-if.md) 或 [CASE](er-functions-logical-case.md)）的代码是自动构建的。</span><span class="sxs-lookup"><span data-stu-id="8eebf-156">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="8eebf-157">您可以扩展和折叠此代码的任何或所有折叠区域，以减少表达式的可编辑部分，从而仅关注需要注意的那段代码。</span><span class="sxs-lookup"><span data-stu-id="8eebf-157">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="8eebf-158">切换折叠/展开命令可用于此目的。</span><span class="sxs-lookup"><span data-stu-id="8eebf-158">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="8eebf-159">例如，要折叠所有区域，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="8eebf-159">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="8eebf-160">按 **Ctrl+K**</span><span class="sxs-lookup"><span data-stu-id="8eebf-160">Press **Ctrl+K**</span></span>

  <span data-ttu-id="8eebf-161">- 或者 -</span><span class="sxs-lookup"><span data-stu-id="8eebf-161">-or-</span></span>

- <span data-ttu-id="8eebf-162">按 **F1**，按 **FO**，选择 **全部折叠**，然后按 **Enter**</span><span class="sxs-lookup"><span data-stu-id="8eebf-162">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="8eebf-163">要展开所有区域，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="8eebf-163">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="8eebf-164">按 **Ctrl+J**</span><span class="sxs-lookup"><span data-stu-id="8eebf-164">Press **Ctrl+J**</span></span>

  <span data-ttu-id="8eebf-165">- 或者 -</span><span class="sxs-lookup"><span data-stu-id="8eebf-165">-or-</span></span>
  
- <span data-ttu-id="8eebf-166">按 **F1**，键入 **UN**，选择 **全部展开**，然后按 **Enter**</span><span class="sxs-lookup"><span data-stu-id="8eebf-166">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="8eebf-167">[![ER 公式编辑器 gif，显示要展开的代码](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="8eebf-167">[![ER formula editor gif showing code being unfolded](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <a name=""></a><span data-ttu-id="8eebf-168"><a name="FindAndReplace">查找和替换</a></span><span class="sxs-lookup"><span data-stu-id="8eebf-168"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="8eebf-169">要查找出现的某些文本，请在表达式中选择此文本，然后执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="8eebf-169">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="8eebf-170">按 **Ctrl+F**，然后按 **F3** 查找下一处所选文本，或按 **Shift+F3** 查找上一处。</span><span class="sxs-lookup"><span data-stu-id="8eebf-170">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="8eebf-171">- 或者 -</span><span class="sxs-lookup"><span data-stu-id="8eebf-171">-or-</span></span>
  
- <span data-ttu-id="8eebf-172">按 **F1**，键入 **F**，然后选择所需的选项以查找选定的文本。</span><span class="sxs-lookup"><span data-stu-id="8eebf-172">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="8eebf-173">要替换出现的某些文本，请在表达式中选择此文本，然后执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="8eebf-173">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="8eebf-174">按 **Ctrl+H**。</span><span class="sxs-lookup"><span data-stu-id="8eebf-174">Press **Ctrl+H**.</span></span> <span data-ttu-id="8eebf-175">输入替代文本，然后选择替换选项，以替换当前表达式中的所选文本或所出现的所有此文本。</span><span class="sxs-lookup"><span data-stu-id="8eebf-175">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="8eebf-176">- 或者 -</span><span class="sxs-lookup"><span data-stu-id="8eebf-176">-or-</span></span>
  
- <span data-ttu-id="8eebf-177">按 **F1**，键入 **R**，然后选择所需的选项以替代选定的文本。</span><span class="sxs-lookup"><span data-stu-id="8eebf-177">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="8eebf-178">输入替代文本，然后选择替换选项，以替换当前表达式中的所选文本或所出现的所有此文本。</span><span class="sxs-lookup"><span data-stu-id="8eebf-178">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="8eebf-179">要更改出现的所有某些文本，请在表达式中选择此文本，然后执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="8eebf-179">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="8eebf-180">按 **Ctrl+F2**，然后输入替代文本。</span><span class="sxs-lookup"><span data-stu-id="8eebf-180">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="8eebf-181">- 或者 -</span><span class="sxs-lookup"><span data-stu-id="8eebf-181">-or-</span></span>
  
- <span data-ttu-id="8eebf-182">按 **F1**，键入 **C**，然后选择所需的选项以更改选定的文本。</span><span class="sxs-lookup"><span data-stu-id="8eebf-182">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="8eebf-183">输入替换文本。</span><span class="sxs-lookup"><span data-stu-id="8eebf-183">Enter the alternative text.</span></span>

<span data-ttu-id="8eebf-184">[![ER 公式编辑器 gif，显示查找和替换](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="8eebf-184">[![ER formula editor gif showing find and replace](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <a name=""></a><span data-ttu-id="8eebf-185"><a name="DataPasting">数据源和函数粘贴</a></span><span class="sxs-lookup"><span data-stu-id="8eebf-185"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="8eebf-186">您可以选择 **添加数据源**，这会将当前在 **数据源** 左面板中选择的数据源粘贴到当前表达式中。</span><span class="sxs-lookup"><span data-stu-id="8eebf-186">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="8eebf-187">同样，您可以选择 **添加函数**，这会将当前在 **函数** 右面板中选择的函数粘贴到当前表达式中。</span><span class="sxs-lookup"><span data-stu-id="8eebf-187">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="8eebf-188">如果使用 ER 公式编辑器，则所选函数或所选数据源将始终粘贴到已配置表达式的末尾。</span><span class="sxs-lookup"><span data-stu-id="8eebf-188">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="8eebf-189">如果使用高级 ER 公式编辑器，则可以将所选函数或所选数据源粘贴到已配置表达式的任何部分中。</span><span class="sxs-lookup"><span data-stu-id="8eebf-189">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="8eebf-190">您将需要使用光标来指定要粘贴数据的位置。</span><span class="sxs-lookup"><span data-stu-id="8eebf-190">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="8eebf-191">[![ER 公式编辑器 gif，显示添加数据源和粘贴函数](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="8eebf-191">[![ER formula editor gif showing adding a data source and pasting a function](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <a name=""></a><span data-ttu-id="8eebf-192"><a name="SyntaxColorization">语法着色</a></span><span class="sxs-lookup"><span data-stu-id="8eebf-192"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="8eebf-193">当前，使用了不同的颜色来突出显示表达式的以下部分：</span><span class="sxs-lookup"><span data-stu-id="8eebf-193">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="8eebf-194">双括号中可以表示文本常量的标签 ID 的文本。</span><span class="sxs-lookup"><span data-stu-id="8eebf-194">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="8eebf-195">[![ER 公式编辑器](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="8eebf-195">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="limitations"></a><span data-ttu-id="8eebf-196">限制</span><span class="sxs-lookup"><span data-stu-id="8eebf-196">Limitations</span></span>

<span data-ttu-id="8eebf-197">以下 Web 浏览器中现在支持此编辑器。</span><span class="sxs-lookup"><span data-stu-id="8eebf-197">The editor is currently supported in the following web browsers:</span></span>

- <span data-ttu-id="8eebf-198">Chrome</span><span class="sxs-lookup"><span data-stu-id="8eebf-198">Chrome</span></span>
- <span data-ttu-id="8eebf-199">Edge</span><span class="sxs-lookup"><span data-stu-id="8eebf-199">Edge</span></span>
- <span data-ttu-id="8eebf-200">Firefox</span><span class="sxs-lookup"><span data-stu-id="8eebf-200">Firefox</span></span>
- <span data-ttu-id="8eebf-201">Opera</span><span class="sxs-lookup"><span data-stu-id="8eebf-201">Opera</span></span>
- <span data-ttu-id="8eebf-202">Safari</span><span class="sxs-lookup"><span data-stu-id="8eebf-202">Safari</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8eebf-203">其他资源</span><span class="sxs-lookup"><span data-stu-id="8eebf-203">Additional resources</span></span>

- [<span data-ttu-id="8eebf-204">电子报告 (ER) 概览</span><span class="sxs-lookup"><span data-stu-id="8eebf-204">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="8eebf-205">电子报告中的配方设计器</span><span class="sxs-lookup"><span data-stu-id="8eebf-205">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="8eebf-206">Monaco 编辑</span><span class="sxs-lookup"><span data-stu-id="8eebf-206">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
