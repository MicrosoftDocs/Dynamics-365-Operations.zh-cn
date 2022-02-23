---
title: 调试已执行 ER 格式的数据源以分析数据流和转换
description: 本主题说明如何调试已执行 ER 格式的数据源以更好地了解已配置的数据流和转换。
author: NickSelin
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 3a486800f37dda7829aeeaa56a30285a92a61b9d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680774"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a>调试已执行 ER 格式的数据源以分析数据流和转换

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

当您将电子申报 (ER) 解决方案[配置](tasks/er-format-configuration-2016-11.md)为生成出站文档时，您将定义用于从应用程序中获取数据并在生成的输出中输入这些数据的方法。 为了使对 ER 解决方案的生命周期支持更加有效，您的解决方案应包括一个 ER [数据模型](general-electronic-reporting.md#DataModelComponent)及其[映射](general-electronic-reporting.md#ModelMappingComponent)组件，还应包括 ER [格式](general-electronic-reporting.md#FormatComponentOutbound)及其映射组件，以便模型映射特定于应用程序，而其他组件则与应用程序无关。 因此，一些 ER 组件可能会[影响](general-electronic-reporting.md#FormatComponentOutbound)在生成的输出中输入数据的过程。

有时，生成的输出的数据看起来与应用程序数据库中的相同数据不同。 在这些情况下，您将需要确定哪个 ER 组件负责数据转换。 ER 数据源调试器功能大大减少了此调查所涉及的时间和成本。 您可以中断 ER 格式的执行并打开数据源调试器接口。 在那里，您可以浏览可用的数据源并选择一个单独的数据源来执行。 该手动执行将模拟实际运行 ER 格式期间数据源的执行操作。 结果显示在页面上，您可以在其中分析接收到的数据。

要打开数据源调试功能，请在 ER 用户参数中将 **在格式运行时启用数据调试** 选项设置为 **是**。 然后，您可以在运行 ER 格式以生成出站文档时启动数据源调试。 您还可以使用 **开始调试** 选项来启动 [ER 操作设计器](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document)中配置的 ER 格式数据源调试。

本主题提供了针对已执行 ER 格式启动数据源调试的准则。 它解释了这些信息如何帮助您理解数据流和数据转换。 本主题中的示例使用业务流程进行供应商付款处理。

## <a name="limitations"></a>限制

数据源调试器可用于访问数据源的数据，这些数据源用于为生成出站文档而运行的 ER 格式。 它不能用于调试旨在解析入站文档的 ER 格式的数据源。

目前无法为进行数据源调试而访问以下 ER 格式设置：

- 格式转换
- 格式和映射验证规则
- 启用表达式
- 内存中数据收集的详细信息

## <a name="prerequisites"></a>先决条件

- 要完成本主题中的示例，您必须具有以下其中一个[角色](../sysadmin/tasks/assign-users-security-roles.md)的访问权限：

    - 电子申报开发人员
    - 电子申报功能顾问
    - 系统管理员

- 公司必须设置为 **DEMF**。

- 执行本主题的[附录 1](#appendix1) 中的步骤，以下载处理供应商付款所需的 Microsoft ER 解决方案的组件。
- 执行本主题的[附录 2](#appendix2) 中的步骤以准备应付帐款，从而使用您将下载的 ER 解决方案处理供应商付款。

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a>处理供应商付款以获取付款文件

1. 执行本主题的[附录 3](#appendix3) 中的步骤以处理供应商付款。

    ![供应商付款处理正在进行中](./media/er-data-debugger-process-payment.png)

2. 下载 zip 文件并将其保存到本地计算机上。
3. 从 zip 文件解压 **ISO20022 Credit transfer.xml** 付款文件。
4. 使用 XML 文件查看器打开解压缩的付款文件。

    在付款文件中，供应商银行帐户的国际银行帐号 (IBAN) 代码不包含空格。 因此，它不同于 **银行帐户** 页面上[输入](#enteredIBANcode)的值。

    ![不含空格的 IBAN 代码](./media/er-data-debugger-payment-file.png)

    您可以使用 ER 数据源调试器来了解 ER 解决方案的哪个组件用于截断 IBAN 代码中的空格。

## <a name="turn-on-data-source-debugging"></a>打开数据源调试

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。
3. 将 **在格式运行时启用数据调试** 选项设置为 **是**。

    > [!NOTE]
    > 此参数特定于用户并且特定于公司。

    ![“用户参数”选项卡](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a>处理供应商付款以进行调试

1. 执行本主题的[附录 3](#appendix3) 中的步骤以处理供应商付款。
2. 在消息框中，选择 **是** 以确认您要中断供应商付款处理，并改为在 **调试数据源** 页面上启动数据源调试。

    ![确认消息框](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a>调试付款处理中使用的数据源

### <a name="debug-the-model-mapping"></a>调试模型映射

1. 在 **调试数据源** 页面中的操作窗格上，选择 **模型映射** 以开始从此 ER 组件进行调试。
2. 在左侧的数据源窗格中，选择 **\$notSentTransactions** 数据源，然后选择 **读取所有记录**。

    您可以选择 **读取 1 条记录**、**读取 10 条记录**、**读取 100 条记录** 或 **读取所有记录**，以从所选数据源中强制读取适当数目的记录。 这样，您可以模拟从正在运行的 ER 格式访问此数据源。

3. 在右侧的数据窗格中，选择 **全部展开**。

    您可以看到 **记录列表** 类型的所选数据源包含单个记录。

4. 展开 **\$notSentTransactions** 数据源，然后选择嵌套的 **vendBankAccountInTransactionCompany()** 方法。
5. 展开 **vendBankAccountInTransactionCompany()** 方法，然后选择嵌套的 **IBAN** 字段。
6. 选择 **获取值**。 

    您可以选择 **获取值** 以强制读取所选数据源中所选字段的值。 这样，您可以模拟从正在运行的 ER 格式访问此字段。

7. 选择 **全部展开**。

    ![模型映射中 IBAN 字段的值](./media/er-data-debugger-debugging-model-mapping.png)

    如您所见，模型映射不负责截断空格，因为它为供应商银行帐户返回的 IBAN 代码包含空格。 因此，您必须继续进行数据源调试。

### <a name="debug-the-format-mapping"></a>调试格式映射

1. 在 **调试数据源** 页面中的操作窗格上，选择 **格式映射** 以继续从此 ER 组件进行调试。
2. 选择 **\$PaymentByDebtor** 数据源，然后选择 **读取所有记录**。
3. 展开 **\$PaymentByDebtor**。
4. 展开 **\$PaymentByDebtor.Lines**，然后选择 **读取所有记录**。
5. 展开 **\$PaymentByDebtor.Lines.CreditorAccount**。
6. 展开 **\$PaymentByDebtor.Lines.CreditorAccount.Identification**，然后选择 **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**。
7. 选择 **获取值**。 
8. 选择 **全部展开**。

    ![格式映射中 IBAN 字段的值](./media/er-data-debugger-debugging-format-mapping.png)

    如您所见，格式映射的数据源不负责截断空格，因为它们为供应商银行帐户返回的 IBAN 代码包含空格。 因此，您必须继续进行数据源调试。

### <a name="debug-the-format"></a>调试格式

1. 在 **调试数据源** 页面中的操作窗格上，选择 **格式** 以继续从此 ER 组件进行调试。
2. 展开格式元素以选择 **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf**，然后选择 **读取所有记录**。
3. 展开格式元素以选择 **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**，然后选择 **读取所有记录**。
4. 展开格式元素以选择 **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**，然后选择 **获取值**。
5. 选择 **全部展开**。

    ![格式中 IBAN 字段的值](./media/er-data-debugger-debugging-format.png)

   如您所见，格式绑定不负责截断空格，因为它为供应商银行帐户返回的 IBAN 代码包含空格。 因此，**BankIBAN** 元素被配置为使用截断空格的格式转换。

6. 关闭数据源调试器。

### <a name="review-the-format-transformations"></a>查看格式转换

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页上，选择 **付款模型** \> **ISO20022 信用转帐**。
3. 选择 **设计器**，然后展开元素以选择 **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**。

    ![格式设计器页面上的 BankIBAN 元素](./media/er-data-debugger-referred-transformation.png)

    如您所见，**BankIBAN** 元素被配置为使用 **删除非字母数字** 转换。

4. 选择 **转换** 选项卡。

    ![BankIBAN 元素的“转换”选项卡](./media/er-data-debugger-transformation.png)

    如您所见，**删除非字母数字** 转换被配置为使用从提供的文本字符串中截断空格的表达式。

## <a name="start-to-debug-in-the-operation-designer"></a>开始在操作设计器中进行调试

当您配置可以直接从操作设计器运行的 ER 格式的草稿版本时，可以通过在操作窗格中选择 **开始调试** 来访问数据源调试器。

![格式设计器页面上的“开始调试”按钮](./media/er-data-debugger-run-from-designer.png)

正在被编辑的 ER 格式的格式映射和格式组件可用于调试。

## <a name="start-to-debug-in-the-model-mapping-designer"></a>开始在模型映射设计器中进行调试

当您配置可以从 **模型映射** 页面运行的 ER 模型映射时，可以通过在操作窗格中选择 **开始调试** 来访问数据源调试器。

![模型映射设计器页面上的“开始调试”按钮](./media/er-data-debugger-run-from-designer-mapping.png)

正在被编辑的 ER 映射的模型映射组件可用于调试。

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a>附录 1：获取 ER 解决方案

### <a name="download-an-er-solution"></a>下载 ER 解决方案

如果要使用 ER 解决方案为处理的供应商付款生成电子付款文件，则可以 [下载](download-electronic-reporting-configuration-lcs.md) **ISO20022 信用转帐** ER 付款格式文件，可从 Microsoft Dynamics Lifecycle Services (LCS) 的共享资产库或从全局存储库中获得此格式文件。

![在“配置存储库”页面上导入 ER 付款格式](./media/er-data-debugger-import-from-repo.png)

除了所选的 ER 格式外，还必须将以下 [配置](general-electronic-reporting.md#Configuration)自动导入到 Microsoft Dynamics 365 Finance 实例中，作为 **ISO20022 信用转帐** ER 解决方案的一部分：

- **付款模型** [ER 数据模型配置](general-electronic-reporting.md#DataModelComponent)
- **ISO20022 信用转帐** [ER 格式配置](general-electronic-reporting.md#FormatComponentOutbound)
- **付款模型映射 1611** [ER 模型映射配置](general-electronic-reporting.md#ModelMappingComponent)
- **付款模型到目标的映射 ISO20022** ER 模型映射配置

您可以在 ER 框架的 **配置** 页面（**组织管理** \> **电子申报** \> **配置**）上找到这些配置。

![在“配置”页面上导入的配置](./media/er-data-debugger-configurations.png)

如果配置树中缺少任何先前列出的配置，则必须从 LCS 共享资产库中手动下载它们，下载方法与下载 **ISO20022 信用转帐** ER 付款格式相同。

### <a name="analyze-the-downloaded-er-solution"></a>分析下载的 ER 解决方案

#### <a name="review-the-model-mapping"></a>查看模型映射

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 选择 **付款模型** \> **付款模型映射 1611**。
3. 选择 **设计器**。
4. 选择 **付款模型映射 ISO20022 CT** 映射记录。
5. 选择 **设计器**，然后查看打开的模型映射。

    请注意，数据模型的 **付款** 字段已绑定到 **\$notSentTransactions** 数据源，该数据源会返回正在处理的供应商付款行的列表。

    ![模型映射设计器页面上的付款字段](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a>查看格式映射

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 选择 **付款模式** \> **ISO20022 信用转帐**。
3. 选择 **设计器**。
4. 在 **映射** 选项卡上，查看打开的格式映射。

    请注意，**ISO20022CTReports** \> **XMLHeader** 文件的 **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** 元素已绑定到 **\$PaymentByDebtor** 数据源，该数据源被配置为对数据模型的 **付款** 字段的记录进行分组。

    ![格式设计器页面上的 PmtInf 元素](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a>查看格式

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 选择 **付款模式** \> **ISO20022 信用转帐**。
3. 选择 **设计器**，然后查看打开的格式。

    请注意，**Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** 下面的格式元素被配置为在付款文件中输入供应商帐户的 IBAN 代码。

    ![格式设计器页面上的 BankIBAN 元素](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a>附录 2：配置应付帐款

### <a name="modify-a-vendor-property"></a>修改供应商属性

1. 转到 **应付帐款** \> **供应商** \> **所有供应商**。
2. 选择供应商 **DE-01002**，然后在操作窗格内 **供应商** 选项卡上的 **设置** 组中，选择 **银行帐户**。
3. 在 **标识** 快速选项卡上的 **IBAN** 字段中，<a name="enteredIBANcode"></a>输入 **GB33 BUKB 2020 1555 5555 55**。
4. 选择 **保存**。

![在“供应商银行帐户”页面上设置的 IBAN 字段](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a>设置付款方式

1. 转到 **应付帐款** \> **付款设置** \> **付款方式**。
2. 选择 **SEPA CT** 付款方式。
3. 在 **文件格式** 快速选项卡上的 **文件格式** 部分中，将 **通用电子导出格式** 选项设置为 **是**。
4. 在 **导出格式配置** 字段中，选择 **ISO20022 信用转帐** ER 格式。
5. 选择 **保存**。

![“付款方式”页面上的文件格式设置](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a>添加供应商付款

1. 转到 **应付帐款** \> **付款** \> **供应商付款日记帐**。
2. 添加新付款日记帐。
3. 选择 **行**，然后添加新付款行。
4. 在 **帐户** 字段中，选择供应商 **DE-01002**。
5. 在 **借项** 字段中输入值。
6. 在 **付款方式** 字段中，选择 **SEPA CT**。
7. 选择 **保存**。

![在“供应商付款”页面上添加的供应商付款](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a>附录 3：处理供应商付款

1. 转到 **应付帐款** \> **付款** \> **供应商付款日记帐**。
2. 在 **供应商付款日记帐** 页面上，选择您先前创建的付款日记帐，然后选择 **行**。
3. 选择付款行，然后选择 **付款状态** \> **无**。
4. 选择 **生成付款**。
5. 在 **付款方式** 字段中，选择 **SEPA CT**。
6. 在 **银行帐户** 字段中，选择 **DEMF OPER**。
7. 在 **生成付款** 对话框中，选择 **确定**。
8. 在 **电子申报参数** 对话框中，选择 **确定**。
