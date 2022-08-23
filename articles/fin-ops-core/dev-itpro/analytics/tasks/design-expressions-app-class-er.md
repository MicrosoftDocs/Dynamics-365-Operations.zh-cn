---
title: 设计 ER 表达式以调用应用类方法
description: 本文介绍如何通过调用必需的应用程序类方法来在电子报告配置中重用现有的应用程序逻辑。
author: kfend
ms.date: 11/02/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21c24cee15e9a0fd11838b5b8fd816e4aaed9a93
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267833"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>设计 ER 表达式以调用应用类方法

[!include [banner](../../includes/banner.md)]

本文介绍如何通过在 ER 表达式中调用必需的应用类方法来在[电子报告 (ER)](../general-electronic-reporting.md) 配置中重用现有应用程序逻辑。 调用类的参数值可以在运行时动态定义。 例如，值可以基于解析文档中的信息，以确保其正确性。

对于本文中的示例，您将设计一个流程来分析传入的银行对帐单以更新应用程序数据。 您将收到包含国际银行帐号 (IBAN) 代码的文本 (.txt) 文件形式的传入银行对帐单。 作为导入银行对帐单过程的一部分，您必须使用已经提供的逻辑验证 IBAN 代码的正确性。

## <a name="prerequisites"></a>先决条件

本文中的过程适用于已被分配了 **系统管理员** 或 **电子报告开发人员** 角色的用户。

可使用任何数据集完成这些过程。

要完成这些过程，您必须下载并保存以下文件：[SampleIncomingMessage.txt](https://download.microsoft.com/download/8/0/a/80adbc89-f23c-46d9-9241-e0f19125c04b/SampleIncomingMessage.txt)。

在本文中，将为示例公司 Litware 公司创建所需 ER 配置。 因此，在完成本文中的过程之前，您必须执行以下步骤。

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面，验证 **Litware, Inc.** 示例公司的配置提供程序是否可用并标记为有效。 如果没有看到此配置提供程序，您必须首先完成[创建配置提供程序并标记为有效](er-configuration-provider-mark-it-active-2016-11.md)中的步骤。

## <a name="import-a-new-er-model-configuration"></a>导入新 ER 模型配置

1. 在 **本地化配置** 页面的 **配置提供程序** 部分，选择 **Microsoft** 配置提供程序的磁贴。
2. 选择 **存储库**。
3. 在 **本地化存储库** 页面上，选择 **显示筛选器**。
4. 要选择全局存储库记录，请添加 **名称** 筛选器字段。
5. 在 **名称** 字段中，输入 **全局**。 然后选择 **contains** 筛选器运算符。
6. 选择 **应用**。
7. 选择 **[打开](../er-download-configurations-global-repo.md#open-configurations-repository)** 查看所选存储库中的 ER 配置列表。
8. 在 **配置存储库** 页的配置树中，选择 **付款模型**。
9. 在 **版本** 快速选项卡上，如果 **导入** 按钮可用，选择该按钮，然后选择 **是**。

    如果 **导入** 按钮不可用，说明您已经导入了所选版本的 **付款模型** ER 配置。

10. 关闭 **配置存储库** 页面，然后关闭 **本地化存储库** 页面。

## <a name="add-a-new-er-format-configuration"></a>添加新 ER 格式配置

添加新的 ER 格式来分析 TXT 格式的传入银行对帐单。

1. 在 **本地化配置** 页面上，选择 **报告配置** 磁贴。
2. 在 **配置** 页的左侧窗格的配置树中，选择 **付款模型**。
3. 选择 **创建配置**。 
4. 在下拉对话框中，执行以下步骤：

    1. 在 **新建** 字段中，输入 **基于数据模型付款模型的格式**。
    2. 在 **名称** 字段中，输入 **银行对帐单导入格式（示例）**。
    3. 在 **支持数据导入** 字段中，选择 **是**。
    4. 选择 **创建配置** 完成配置的创建。

## <a name="design-the-er-format-configuration--format"></a>设计 ER 格式配置 – 格式

设计一个表示 TXT 格式外部文件的预期结构的 ER 格式。

1. 对于您添加的 **银行对帐单导入格式（示例）** 格式配置，选择 **设计器**。
2. 在 **格式设计器** 页上，在左窗格中的格式结构树中，选择 **添加根**。
3. 在出现的对话框中，执行以下步骤：

    1. 在树中，选择 **文本\\序列** 添加 **序列** 格式组件。
    2. 在 **名称** 字段中，输入 **根**。
    3. 在 **特殊字符** 字段中，选择 **新行 - Windows (CR LF)**。 基于此设置，分析文件的每一行将被视为单独的记录。
    4. 选择 **确定**。

4. 选择 **添加**。
5. 在出现的对话框中，执行以下步骤：

    1. 在树中，选择 **文本\\序列**。
    2. 在 **名称** 字段中，输入 **行**。
    3. 在 **多样性** 字段中，选择 **一个 多个**。 基于此设置，预计分析文件中至少会出现一行。
    4. 选择 **确定**。

6. 在树中，选择 **根\\行**，然后选择 **添加序列**。
7. 在出现的对话框中，执行以下步骤：

    1. 在 **名称** 字段中，输入 **字段**。
    2. 在 **多样性** 字段中，选择 **正好一个**。
    3. 选择 **确定**。

8. 在树中，选择 **根\\行\\字段**，然后选择 **添加**。
9. 在出现的对话框中，执行以下步骤：

    1. 在树中，选择 **文本\\字符串**。
    2. 在 **名称** 字段中，输入 **IBAN**。
    3.. 选择 **确定**。

10. 选择 **保存**。

配置现在已设置，以使分析文件中的每一行仅包含 IBAN 代码。

![格式设计器页面上的银行对帐单导入格式（示例）格式配置。](../media/design-expressions-app-class-er-01.png)

## <a name="design-the-er-format-configuration--mapping-to-a-data-model"></a>设计 ER 格式配置 – 映射到数据模型

设计一个 ER 格式映射，该映射使用来自分析文件的信息填充数据模型。

1. 在 **格式设计器** 页面的操作窗格中，选择 **将格式映射到模型**。
2. 在 **模型到数据源映射** 页面的操作窗格中，选择 **新**。
3. 在 **定义** 字段中，选择 **BankToCustomerDebitCreditNotificationInitiation**。
4. 在 **名称** 字段中，输入 **数据模型映射**。
5. 选择 **保存**。
6. 选择 **设计器**。
7. 在 **模型映射设计器** 页的 **数据源类型** 树中，选择 **Dynamics 365 for Operations\\类**。
8. 在 **数据源** 部分，选择 **添加根** 添加一个数据源，该数据源调用现有应用程序逻辑以进行 IBAN 代码验证。
9. 在出现的对话框中，执行以下步骤：

    1. 在 **名称** 字段中，输入 **Check\_codes**。
    2. 在 **类** 字段中，输入或选择 **ISO7064**。
    3. 选择 **确定**。

10. 在 **数据源类型** 树中，执行以下步骤：

    1. 展开 **格式** 数据源。
    2. 展开 **format\\Root: Sequence(Root)**。
    3. 展开 **format\\Root: Sequence(Root)\\Rows: Sequence 1..\* (Rows)**。
    4. 展开 **format\\Root: Sequence(Root)\\Rows: Sequence 1..\* (Rows)\\Fields: Sequence 1..1 (Fields)**。

11. 在 **数据模型** 树中，执行以下步骤：

    1. 展开数据模型的 **付款** 字段。
    2. 展开 **Payments\\Creditor Account(CreditorAccount)**。
    3. 展开 **Payments\\Creditor Account(CreditorAccount)\\Identification**。
    4. 展开 **Payments\\Creditor Account(CreditorAccount)\\Identification\\IBAN**。

12. 按照以下步骤将配置格式的组件绑定到数据模型字段：

    1. 选择 **format\\Root: Sequence(Root)\\Rows: Sequence 1..\* (Rows)**。
    2. 选择 **付款**。
    3. 选择 **绑定**。 基于此设置，分析文件的每一行将被视为单笔付款。
    4. 选择 **format\\Root: Sequence(Root)\\Rows: Sequence 1..\* (Rows)\\Fields: Sequence 1..1 (Fields)\\IBAN: String(IBAN)**。
    5. 选择 **Payments\\Creditor Account(CreditorAccount)\\Identification\\IBAN**。
    6. 选择 **绑定**。 根据此设置，数据模型的 **IBAN** 字段将填充解析文件中的值。

    ![将格式组件绑定到模型映射设计器页面上的数据模型字段。](../media/design-expressions-app-class-er-02.png)

13. 在 **验证** 选项卡上，按照以下步骤添加[验证](../general-electronic-reporting-formula-designer.md#Validation)规则，该规则显示分析文件中包含无效 IBAN 代码的任何行的错误消息：

    1. 选择 **新**，然后选择 **编辑条件**。
    2. 在 **公式设计器** 页面上的 **数据源** 树中，展开表示 **ISO7064** 应用程序类的 **Check\_codes** 数据源来查看此类的可用方法。
    3. 选择 **Check\_codes\\verifyMOD1271\_36**。
    4. 选择 **添加数据源**。
    5. 在 **公式** 字段中，输入以下 [表达式](../general-electronic-reporting-formula-designer.md#Binding)：**Check\_codes.verifyMOD1271\_36(format.Root.Rows.Fields.IBAN)**。
    6. 选择 **保存**，然后关闭页面。
    7. 选择 **编辑消息**。
    8. 在 **公式设计器** 页面上的 **公式** 字段中，输入 **CONCATENATE("Invalid IBAN code has been found:&nbsp;", format.Root.Rows.Fields.IBAN)**。
    9. 选择 **保存**，然后关闭页面。

    基于这些设置，对于任何无效的 IBAN 代码，验证条件将通过调用 **ISO7064** 应用程序类的现有的 **verifyMOD1271\_36** 方法返回 *[FALSE](../er-formula-supported-data-types-primitive.md#boolean)*。 请注意，IBAN 代码的值在运行时被动态定义为基于分析文本文件的内容调用方法的参数。

    ![“模型映射设计器”页面上的验证规则。](../media/design-expressions-app-class-er-03.png)

14. 选择 **保存**。
15. 关闭 **模型映射设计器** 页面，然后关闭 **模型到数据源映射** 页面。

## <a name="run-the-format-mapping"></a>运行格式映射

为了测试，请使用以前下载的 SampleIncomingMessage.txt 文件运行格式映射。 生成的输出将包含从所选文本文件导入，并在实际导入时转移到自定义数据模型的数据。

1. 在 **模型到数据源映射** 页面上，选择 **运行**。
2. 在 **电子报表参数** 页面上，选择 **浏览**，浏览到您下载的 **SampleIncomingMessage.txt** 文件，然后选择它。
3. 选择 **确定**。
4. 请注意，**模型到数据源映射** 页面将显示有关无效 IBAN 代码的错误消息。

    ![在模型到数据源映射页面上运行格式映射的结果。](../media/design-expressions-app-class-er-04.png)

5. 检查 XML 格式的输出，该输出表示已从所选文件导入并移植到数据模型的数据。 请注意，只有三行导入的文本文件被处理，没有错误。 第 4 行的 IBAN 代码无效，已被跳过。

    ![XML 输出。](../media/design-expressions-app-class-er-05.png)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
