---
title: 电子报告高级公式编辑器
description: 本文描述如何使用高级公式编辑器来配置电子报告 (ER) 模型映射和格式组件中的表达式。
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
ms.openlocfilehash: f54ab248e38d87b0a9fb7a73143f56fa704a3f67
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869090"
---
# <a name="electronic-reporting-advanced-formula-editor"></a>电子报告高级公式编辑器

[!include [banner](../includes/banner.md)]

除了[电子报告](general-electronic-reporting.md)[公式编辑器](general-electronic-reporting-formula-designer.md)之外，您还可以使用高级电子报告公式编辑器来改善配置电子报告 (ER) 表达式的体验。 高级编辑器基于浏览器，由 [Monaco 编辑器](https://microsoft.github.io/monaco-editor)提供支持。 本文介绍了最常用的高级编辑器功能：

- [代码自动格式化](#Autoformatting)
- [IntelliSense](#IntelliSense)
- [代码完成](#CodeCompletion)
- [代码导航](#CodeNavigation)
- [代码构造](#CodeStructuring)
- [查找和替换](#FindAndReplace)
- [数据粘贴](#DataPasting)
- [语法着色](#SyntaxColorization)

## <a name=""></a><a name="ActivateAdvEditor">激活高级公式编辑器</a>

完成以下步骤，开始在您的 Microsoft Dynamics 365 Finance 实例中使用高级公式编辑器。

1.  转到 **组织管理** \> **电子申报** \> **配置**。
2.  在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。
3.  在 **用户参数** 对话框内的 **执行跟踪** 部分中，将 **启用高级公式编辑器** 参数设置为 **是**。

[![用户参数对话框，突出显示了启用高级公式编辑器参数。](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)

> [!NOTE]
> 请注意，此参数特定于用户和公司。

从 Microsoft Dynamics 365 Finance 版本 10.0.19 开始，您可以控制默认提供的 ER 公式编辑器。 完成以下步骤，为当前 Finance 实例的所有用户和公司启用高级公式编辑器。

1.  打开 **功能管理** 工作区。
2.  在列表中查找并选择功能 **将 ER 高级公式编辑器设置为所有用户的默认编辑器**，然后选择 **立即启用**。
3.  转到 **组织管理** > **电子申报** > **配置**。
4.  在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。
5.  在 **用户参数** 对话框中，查找 **禁用高级公式编辑器** 参数，并验证它是否设置为 **否**。

[![用户参数对话框，突出显示了禁用高级公式编辑器参数。](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)

> [!NOTE]
> 参数 **启用高级公式编辑器** 和 **禁用高级公式编辑器** 的值针对每个用户单独保存，并且在 **用户参数** 对话框上提供，具体取决于 **将 ER 高级公式编辑器设置为所有用户的默认编辑器** 功能的状态。

## <a name=""></a><a name="Autoformatting">代码自动格式化</a>

当您编写包含多行代码的复杂表达式时，新输入行的缩进将基于前一行的缩进自动进行。 您可以按 **Tab** 或 **Shift+Tab** 来选择行并更改其缩进量。

[![ER 公式编辑器 gif，显示选择行和更改缩进。](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)

自动格式化可让整个表达式的格式保持正确，以使进一步的维护更加容易，并简化对已配置逻辑的理解。

## <a name=""></a><a name="IntelliSense">IntelliSense</a>

该编辑器提供了单词补全功能，可帮助您更快地编写表达式并避免输入错误。 当您开始添加新文本时，编辑器会自动提供 ER 函数支持的函数列表，其中包含您输入的字符。 您还可以通过按 **Ctrl + 空格键** 在已配置表达式的任何位置触发 IntelliSense。

[![ER 公式编辑器 gif，显示触发 IntelliSense。](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)

## <a name=""></a><a name="CodeCompletion">代码完成</a>

编辑器通过以下方式自动完成代码：

- 输入开括号时插入一个闭括号，将光标保持在括号内。
- 输入第一个引号时，插入第二个引号，使光标保持在引号内。
- 输入第一个双引号时，插入第二个双引号，使光标保持在引号内。

[![ER 公式编辑器 gif，显示编辑器自动提供代码完成。](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)

当您指向键入的括号时，该括号对的第二个括号将自动突出显示以显示其支持的结构。

## <a name=""></a><a name="CodeNavigation">代码导航</a>

通过使用命令面板或上下文菜单键入 **转到** 命令，您可以在表达式中找到所需的符号或行。

例如，要跳到第 **8** 行，请执行下列操作：

- 按 **Ctrl+G**，输入值 **8**，然后按 **Enter**。

  - 或者 -

- 按 **F1**，键入 **G**，选择 **转到行**，输入值 **8**，然后按 **Enter**。

[![ER 公式编辑器 gif，显示如何使用命令面板定位表达式的各个部分。](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)

## <a name=""></a><a name="CodeStructuring">代码构造</a>

某些函数（例如 [IF](er-functions-logical-if.md) 或 [CASE](er-functions-logical-case.md)）的代码是自动构建的。 您可以扩展和折叠此代码的任何或所有折叠区域，以减少表达式的可编辑部分，从而仅关注需要注意的那段代码。 切换折叠/展开命令可用于此目的。

例如，要折叠所有区域，请执行以下操作：

- 按 **Ctrl+K**

  - 或者 -

- 按 **F1**，按 **FO**，选择 **全部折叠**，然后按 **Enter**

要展开所有区域，请执行以下操作：

- 按 **Ctrl+J**

  - 或者 -
  
- 按 **F1**，键入 **UN**，选择 **全部展开**，然后按 **Enter**

[![ER 公式编辑器 gif，显示要展开的代码。](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)

## <a name=""></a><a name="FindAndReplace">查找和替换</a>

要查找出现的某些文本，请在表达式中选择此文本，然后执行以下操作：

- 按 **Ctrl+F**，然后按 **F3** 查找下一处所选文本，或按 **Shift+F3** 查找上一处。

  - 或者 -
  
- 按 **F1**，键入 **F**，然后选择所需的选项以查找选定的文本。

要替换出现的某些文本，请在表达式中选择此文本，然后执行以下操作：

- 按 **Ctrl+H**。 输入替代文本，然后选择替换选项，以替换当前表达式中的所选文本或所出现的所有此文本。

  - 或者 -
  
- 按 **F1**，键入 **R**，然后选择所需的选项以替代选定的文本。 输入替代文本，然后选择替换选项，以替换当前表达式中的所选文本或所出现的所有此文本。

要更改出现的所有某些文本，请在表达式中选择此文本，然后执行以下操作：

- 按 **Ctrl+F2**，然后输入替代文本。

  - 或者 -
  
- 按 **F1**，键入 **C**，然后选择所需的选项以更改选定的文本。 输入替换文本。

[![ER 公式编辑器 gif，显示查找和替换。](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)

## <a name=""></a><a name="DataPasting">数据源和函数粘贴</a>

您可以选择 **添加数据源**，这会将当前在 **数据源** 左面板中选择的数据源粘贴到当前表达式中。 同样，您可以选择 **添加函数**，这会将当前在 **函数** 右面板中选择的函数粘贴到当前表达式中。 如果使用 ER 公式编辑器，则所选函数或所选数据源将始终粘贴到已配置表达式的末尾。 如果使用高级 ER 公式编辑器，则可以将所选函数或所选数据源粘贴到已配置表达式的任何部分中。 您将需要使用光标来指定要粘贴数据的位置。

[![ER 公式编辑器 gif，显示添加数据源和粘贴函数。](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)

## <a name=""></a><a name="SyntaxColorization">语法着色</a>

当前，使用了不同的颜色来突出显示表达式的以下部分：

- 双括号中可以表示文本常量的标签 ID 的文本。

[![ER 公式编辑器。](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)

## <a name="limitations"></a>限制

以下 Web 浏览器中现在支持此编辑器。

- Chrome
- Edge
- Firefox
- Opera
- Safari

## <a name="additional-resources"></a>其他资源

- [电子报告 (ER) 概览](general-electronic-reporting.md)
- [电子报告中的配方设计器](general-electronic-reporting-formula-designer.md)
- [Monaco 编辑](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
