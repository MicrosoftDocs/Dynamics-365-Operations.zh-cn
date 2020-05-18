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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 5b51c4beac0ddf1e2b53fe300e10c0f608e5d1e1
ms.sourcegitcommit: 153bb33722c02501bf7bcfd56ac887602d5dfbd3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/29/2020
ms.locfileid: "3318658"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a><span data-ttu-id="41887-103">调试已执行 ER 格式的数据源以分析数据流和转换</span><span class="sxs-lookup"><span data-stu-id="41887-103">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="41887-104">当您将电子申报 (ER) 解决方案[配置](tasks/er-format-configuration-2016-11.md)为生成出站文档时，您将定义用于从应用程序中获取数据并在生成的输出中输入这些数据的方法。</span><span class="sxs-lookup"><span data-stu-id="41887-104">When you [configure](tasks/er-format-configuration-2016-11.md) an Electronic reporting (ER) solution to generate outbound documents, you define the methods that are used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="41887-105">为了使对 ER 解决方案的生命周期支持更加有效，您的解决方案应包括一个 ER [数据模型](general-electronic-reporting.md#DataModelComponent)及其[映射](general-electronic-reporting.md#ModelMappingComponent)组件，还应包括 ER [格式](general-electronic-reporting.md#FormatComponentOutbound)及其映射组件，以便模型映射特定于应用程序，而其他组件则与应用程序无关。</span><span class="sxs-lookup"><span data-stu-id="41887-105">To make the life cycle support of the ER solution more efficient, your solution should consist of an ER [data model](general-electronic-reporting.md#DataModelComponent) and its [mapping](general-electronic-reporting.md#ModelMappingComponent) components, and also an ER [format](general-electronic-reporting.md#FormatComponentOutbound) and its mapping components, so that the model mapping is application-specific, whereas other components remain application-agnostic.</span></span> <span data-ttu-id="41887-106">因此，一些 ER 组件可能会[影响](general-electronic-reporting.md#FormatComponentOutbound)在生成的输出中输入数据的过程。</span><span class="sxs-lookup"><span data-stu-id="41887-106">Therefore, several ER components might [affect](general-electronic-reporting.md#FormatComponentOutbound) the process of entering data in the generated output.</span></span>

<span data-ttu-id="41887-107">有时，生成的输出的数据看起来与应用程序数据库中的相同数据不同。</span><span class="sxs-lookup"><span data-stu-id="41887-107">Sometimes, the data of the generated output looks different than the same data in the application database.</span></span> <span data-ttu-id="41887-108">在这些情况下，您将需要确定哪个 ER 组件负责数据转换。</span><span class="sxs-lookup"><span data-stu-id="41887-108">In these cases, you will want to determine which ER component is responsible for the data transformation.</span></span> <span data-ttu-id="41887-109">ER 数据源调试器功能大大减少了此调查所涉及的时间和成本。</span><span class="sxs-lookup"><span data-stu-id="41887-109">The ER data source debugger feature significantly reduces the time and cost that are involved in this investigation.</span></span> <span data-ttu-id="41887-110">您可以中断 ER 格式的执行并打开数据源调试器接口。</span><span class="sxs-lookup"><span data-stu-id="41887-110">You can interrupt the execution of an ER format and open the data source debugger interface.</span></span> <span data-ttu-id="41887-111">在那里，您可以浏览可用的数据源并选择一个单独的数据源来执行。</span><span class="sxs-lookup"><span data-stu-id="41887-111">There, you can browse the available data sources and select an individual data source for execution.</span></span> <span data-ttu-id="41887-112">该手动执行将模拟实际运行 ER 格式期间数据源的执行操作。</span><span class="sxs-lookup"><span data-stu-id="41887-112">This manual execution simulates the execution of the data source during the real run of an ER format.</span></span> <span data-ttu-id="41887-113">结果显示在页面上，您可以在其中分析接收到的数据。</span><span class="sxs-lookup"><span data-stu-id="41887-113">The result is presented on a page where you can analyze the data that is received.</span></span>

<span data-ttu-id="41887-114">要打开数据源调试功能，请在 ER 用户参数中将**在格式运行时启用数据调试**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="41887-114">To turn on the data source debugging feature, set the **Enable data debugging at format run** option to **Yes** in the ER user parameters.</span></span> <span data-ttu-id="41887-115">然后，您可以在运行 ER 格式以生成出站文档时启动数据源调试。</span><span class="sxs-lookup"><span data-stu-id="41887-115">You can then start data source debugging while you run an ER format to generate outbound documents.</span></span> <span data-ttu-id="41887-116">您还可以使用**开始调试**选项来启动 [ER 操作设计器](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document)中配置的 ER 格式数据源调试。</span><span class="sxs-lookup"><span data-stu-id="41887-116">You can also use the **Start debugging** option to initiate data source debugging for an ER format that is configured in the [ER Operation designer](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span></span>

<span data-ttu-id="41887-117">本主题提供了针对已执行 ER 格式启动数据源调试的准则。</span><span class="sxs-lookup"><span data-stu-id="41887-117">This topic provides guidelines for initiating data source debugging for executed ER formats.</span></span> <span data-ttu-id="41887-118">它解释了这些信息如何帮助您理解数据流和数据转换。</span><span class="sxs-lookup"><span data-stu-id="41887-118">It explains how the information can help you understand the data flow and data transformations.</span></span> <span data-ttu-id="41887-119">本主题中的示例使用业务流程进行供应商付款处理。</span><span class="sxs-lookup"><span data-stu-id="41887-119">The examples in this topic use the business process for vendor payments processing.</span></span>

## <a name="limitations"></a><span data-ttu-id="41887-120">限制</span><span class="sxs-lookup"><span data-stu-id="41887-120">Limitations</span></span>

<span data-ttu-id="41887-121">数据源调试器可用于访问数据源的数据，这些数据源用于为生成出站文档而运行的 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="41887-121">The data source debugger can be used to access the data of data sources that are used in ER formats that are run to generate outbound documents.</span></span> <span data-ttu-id="41887-122">它不能用于调试旨在解析入站文档的 ER 格式的数据源。</span><span class="sxs-lookup"><span data-stu-id="41887-122">It can't be used to debug data sources of ER formats that are designed to parse inbound documents.</span></span>

<span data-ttu-id="41887-123">目前无法为进行数据源调试而访问以下 ER 格式设置：</span><span class="sxs-lookup"><span data-stu-id="41887-123">The following settings of ER formats aren't currently accessible for data source debugging:</span></span>

- <span data-ttu-id="41887-124">格式转换</span><span class="sxs-lookup"><span data-stu-id="41887-124">Format transformations</span></span>
- <span data-ttu-id="41887-125">格式和映射验证规则</span><span class="sxs-lookup"><span data-stu-id="41887-125">Format and mapping validation rules</span></span>
- <span data-ttu-id="41887-126">启用表达式</span><span class="sxs-lookup"><span data-stu-id="41887-126">Enabling expressions</span></span>
- <span data-ttu-id="41887-127">内存中数据收集的详细信息</span><span class="sxs-lookup"><span data-stu-id="41887-127">Details of in-memory data collection</span></span>

## <a name="prerequisites"></a><span data-ttu-id="41887-128">先决条件</span><span class="sxs-lookup"><span data-stu-id="41887-128">Prerequisites</span></span>

- <span data-ttu-id="41887-129">要完成本主题中的示例，您必须具有以下其中一个[角色](../sysadmin/tasks/assign-users-security-roles.md)的访问权限：</span><span class="sxs-lookup"><span data-stu-id="41887-129">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="41887-130">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="41887-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="41887-131">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="41887-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="41887-132">系统管理员</span><span class="sxs-lookup"><span data-stu-id="41887-132">System administrator</span></span>

- <span data-ttu-id="41887-133">公司必须设置为 **DEMF**。</span><span class="sxs-lookup"><span data-stu-id="41887-133">The company must be set to **DEMF**.</span></span>

- <span data-ttu-id="41887-134">执行本主题的[附录 1](#appendix1) 中的步骤，以下载处理供应商付款所需的 Microsoft ER 解决方案的组件。</span><span class="sxs-lookup"><span data-stu-id="41887-134">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the Microsoft ER solution that are required to process vendor payments.</span></span>
- <span data-ttu-id="41887-135">执行本主题的[附录 2](#appendix2) 中的步骤以准备应付帐款，从而使用您将下载的 ER 解决方案处理供应商付款。</span><span class="sxs-lookup"><span data-stu-id="41887-135">Follow the steps in [Appendix 2](#appendix2) of this topic to prepare Accounts payable for vendor payment processing by using the ER solution that you will download.</span></span>

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a><span data-ttu-id="41887-136">处理供应商付款以获取付款文件</span><span class="sxs-lookup"><span data-stu-id="41887-136">Process a vendor payment to get a payment file</span></span>

1. <span data-ttu-id="41887-137">执行本主题的[附录 3](#appendix3) 中的步骤以处理供应商付款。</span><span class="sxs-lookup"><span data-stu-id="41887-137">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>

    ![供应商付款处理正在进行中](./media/er-data-debugger-process-payment.png)

2. <span data-ttu-id="41887-139">下载 zip 文件并将其保存到本地计算机上。</span><span class="sxs-lookup"><span data-stu-id="41887-139">Download and save the zip file to your local computer.</span></span>
3. <span data-ttu-id="41887-140">从 zip 文件解压 **ISO20022 Credit transfer.xml** 付款文件。</span><span class="sxs-lookup"><span data-stu-id="41887-140">Extract the **ISO20022 Credit transfer.xml** payment file from the zip file.</span></span>
4. <span data-ttu-id="41887-141">使用 XML 文件查看器打开解压缩的付款文件。</span><span class="sxs-lookup"><span data-stu-id="41887-141">Open the extracted payment file by using the XML file viewer.</span></span>

    <span data-ttu-id="41887-142">在付款文件中，供应商银行帐户的国际银行帐号 (IBAN) 代码不包含空格。</span><span class="sxs-lookup"><span data-stu-id="41887-142">In the payment file, the International Bank Account Number (IBAN) code of the vendor bank account contains no spaces.</span></span> <span data-ttu-id="41887-143">因此，它不同于**银行帐户**页面上[输入](#enteredIBANcode)的值。</span><span class="sxs-lookup"><span data-stu-id="41887-143">Therefore, it differs from the value that was [entered](#enteredIBANcode) on the **Bank accounts** page.</span></span>

    ![不含空格的 IBAN 代码](./media/er-data-debugger-payment-file.png)

    <span data-ttu-id="41887-145">您可以使用 ER 数据源调试器来了解 ER 解决方案的哪个组件用于截断 IBAN 代码中的空格。</span><span class="sxs-lookup"><span data-stu-id="41887-145">You can use the ER data source debugger to learn which component of the ER solution is used to truncate spaces in the IBAN code.</span></span>

## <a name="turn-on-data-source-debugging"></a><span data-ttu-id="41887-146">打开数据源调试</span><span class="sxs-lookup"><span data-stu-id="41887-146">Turn on data source debugging</span></span>

1. <span data-ttu-id="41887-147">转到**组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="41887-147">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="41887-148">在**配置**页操作窗格中**配置**选项卡的**高级设置**组中，选择**用户参数**。</span><span class="sxs-lookup"><span data-stu-id="41887-148">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="41887-149">将**在格式运行时启用数据调试**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="41887-149">Set the **Enable data debugging at format run** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="41887-150">此参数特定于用户并且特定于公司。</span><span class="sxs-lookup"><span data-stu-id="41887-150">This parameter is user-specific and company-specific.</span></span>

    ![“用户参数”选项卡](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a><span data-ttu-id="41887-152">处理供应商付款以进行调试</span><span class="sxs-lookup"><span data-stu-id="41887-152">Process a vendor payment for debugging</span></span>

1. <span data-ttu-id="41887-153">执行本主题的[附录 3](#appendix3) 中的步骤以处理供应商付款。</span><span class="sxs-lookup"><span data-stu-id="41887-153">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>
2. <span data-ttu-id="41887-154">在消息框中，选择**是**以确认您要中断供应商付款处理，并改为在**调试数据源**页面上启动数据源调试。</span><span class="sxs-lookup"><span data-stu-id="41887-154">In the message box, select **Yes** to confirm that you want to interrupt vendor payment processing and instead start data source debugging on the **Debug Datasources** page.</span></span>

    ![确认消息框](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a><span data-ttu-id="41887-156">调试付款处理中使用的数据源</span><span class="sxs-lookup"><span data-stu-id="41887-156">Debug data sources that are used in payment processing</span></span>

### <a name="debug-the-model-mapping"></a><span data-ttu-id="41887-157">调试模型映射</span><span class="sxs-lookup"><span data-stu-id="41887-157">Debug the model mapping</span></span>

1. <span data-ttu-id="41887-158">在**调试数据源**页面中的操作窗格上，选择**模型映射**以开始从此 ER 组件进行调试。</span><span class="sxs-lookup"><span data-stu-id="41887-158">On the **Debug Datasources** page, on the Action Pane, select **Model mapping** to start to debug from this ER component.</span></span>
2. <span data-ttu-id="41887-159">在左侧的数据源窗格中，选择 **\$notSentTransactions** 数据源，然后选择**读取所有记录**。</span><span class="sxs-lookup"><span data-stu-id="41887-159">In the data source pane on the left, select the **\$notSentTransactions** data source, and then select **Read all records**.</span></span>

    <span data-ttu-id="41887-160">您可以选择**读取 1 条记录**、**读取 10 条记录**、**读取 100 条记录**或**读取所有记录**，以从所选数据源中强制读取适当数目的记录。</span><span class="sxs-lookup"><span data-stu-id="41887-160">You can select **Read 1 record**, **Read 10 records**, **Read 100 records**, or **Read all records** to force the appropriate number of records to be read from the selected data source.</span></span> <span data-ttu-id="41887-161">这样，您可以模拟从正在运行的 ER 格式访问此数据源。</span><span class="sxs-lookup"><span data-stu-id="41887-161">In this way, you can simulate access to the data source from the running ER format.</span></span>

3. <span data-ttu-id="41887-162">在右侧的数据窗格中，选择**全部展开**。</span><span class="sxs-lookup"><span data-stu-id="41887-162">In the data pane on the right, select **Expand all**.</span></span>

    <span data-ttu-id="41887-163">您可以看到**记录列表**类型的所选数据源包含单个记录。</span><span class="sxs-lookup"><span data-stu-id="41887-163">You can see that the selected data source of the **Record list** type contains a single record.</span></span>

4. <span data-ttu-id="41887-164">展开 **\$notSentTransactions** 数据源，然后选择嵌套的 **vendBankAccountInTransactionCompany()** 方法。</span><span class="sxs-lookup"><span data-stu-id="41887-164">Expand the **\$notSentTransactions** data source, and select the nested **vendBankAccountInTransactionCompany()** method.</span></span>
5. <span data-ttu-id="41887-165">展开 **vendBankAccountInTransactionCompany()** 方法，然后选择嵌套的 **IBAN** 字段。</span><span class="sxs-lookup"><span data-stu-id="41887-165">Expand the **vendBankAccountInTransactionCompany()** method, and select the nested **IBAN** field.</span></span>
6. <span data-ttu-id="41887-166">选择**获取值**。 </span><span class="sxs-lookup"><span data-stu-id="41887-166">Select **Get value**.</span></span>

    <span data-ttu-id="41887-167">您可以选择**获取值**以强制读取所选数据源中所选字段的值。</span><span class="sxs-lookup"><span data-stu-id="41887-167">You can select **Get value** to force the value of a selected field of the selected data source to be read.</span></span> <span data-ttu-id="41887-168">这样，您可以模拟从正在运行的 ER 格式访问此字段。</span><span class="sxs-lookup"><span data-stu-id="41887-168">In this way, you can simulate access to this field from the running ER format.</span></span>

7. <span data-ttu-id="41887-169">选择**全部展开**。</span><span class="sxs-lookup"><span data-stu-id="41887-169">Select **Expand all**.</span></span>

    ![模型映射中 IBAN 字段的值](./media/er-data-debugger-debugging-model-mapping.png)

    <span data-ttu-id="41887-171">如您所见，模型映射不负责截断空格，因为它为供应商银行帐户返回的 IBAN 代码包含空格。</span><span class="sxs-lookup"><span data-stu-id="41887-171">As you can see, the model mapping isn't responsible for the truncated spaces, because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="41887-172">因此，您必须继续进行数据源调试。</span><span class="sxs-lookup"><span data-stu-id="41887-172">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format-mapping"></a><span data-ttu-id="41887-173">调试格式映射</span><span class="sxs-lookup"><span data-stu-id="41887-173">Debug the format mapping</span></span>

1. <span data-ttu-id="41887-174">在**调试数据源**页面中的操作窗格上，选择**格式映射**以继续从此 ER 组件进行调试。</span><span class="sxs-lookup"><span data-stu-id="41887-174">On the **Debug Datasources** page, on the Action Pane, select **Format mapping** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="41887-175">选择 **\$PaymentByDebtor** 数据源，然后选择**读取所有记录**。</span><span class="sxs-lookup"><span data-stu-id="41887-175">Select the **\$PaymentByDebtor** data source, and then select **Read all records**.</span></span>
3. <span data-ttu-id="41887-176">展开 **\$PaymentByDebtor**。</span><span class="sxs-lookup"><span data-stu-id="41887-176">Expand **\$PaymentByDebtor**.</span></span>
4. <span data-ttu-id="41887-177">展开 **\$PaymentByDebtor.Lines**，然后选择**读取所有记录**。</span><span class="sxs-lookup"><span data-stu-id="41887-177">Expand **\$PaymentByDebtor.Lines**, and then select **Read all records**.</span></span>
5. <span data-ttu-id="41887-178">展开 **\$PaymentByDebtor.Lines.CreditorAccount**。</span><span class="sxs-lookup"><span data-stu-id="41887-178">Expand **\$PaymentByDebtor.Lines.CreditorAccount**.</span></span>
6. <span data-ttu-id="41887-179">展开 **\$PaymentByDebtor.Lines.CreditorAccount.Identification**，然后选择 **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**。</span><span class="sxs-lookup"><span data-stu-id="41887-179">Expand **\$PaymentByDebtor.Lines.CreditorAccount.Identification**, and then select **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span></span>
7. <span data-ttu-id="41887-180">选择**获取值**。 </span><span class="sxs-lookup"><span data-stu-id="41887-180">Select **Get value**.</span></span>
8. <span data-ttu-id="41887-181">选择**全部展开**。</span><span class="sxs-lookup"><span data-stu-id="41887-181">Select **Expand all**.</span></span>

    ![格式映射中 IBAN 字段的值](./media/er-data-debugger-debugging-format-mapping.png)

    <span data-ttu-id="41887-183">如您所见，格式映射的数据源不负责截断空格，因为它们为供应商银行帐户返回的 IBAN 代码包含空格。</span><span class="sxs-lookup"><span data-stu-id="41887-183">As you can see, the data sources of the format mapping aren't responsible for the truncated spaces, because the IBAN code that they return for the vendor bank account includes spaces.</span></span> <span data-ttu-id="41887-184">因此，您必须继续进行数据源调试。</span><span class="sxs-lookup"><span data-stu-id="41887-184">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format"></a><span data-ttu-id="41887-185">调试格式</span><span class="sxs-lookup"><span data-stu-id="41887-185">Debug the format</span></span>

1. <span data-ttu-id="41887-186">在**调试数据源**页面中的操作窗格上，选择**格式**以继续从此 ER 组件进行调试。</span><span class="sxs-lookup"><span data-stu-id="41887-186">On the **Debug Datasources** page, on the Action Pane, select **Format** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="41887-187">展开格式元素以选择 **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf**，然后选择**读取所有记录**。</span><span class="sxs-lookup"><span data-stu-id="41887-187">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf**, and then select **Read all records**.</span></span>
3. <span data-ttu-id="41887-188">展开格式元素以选择 **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**，然后选择**读取所有记录**。</span><span class="sxs-lookup"><span data-stu-id="41887-188">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, and then select **Read all records**.</span></span>
4. <span data-ttu-id="41887-189">展开格式元素以选择 **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**，然后选择**获取值**。</span><span class="sxs-lookup"><span data-stu-id="41887-189">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, and then select **Get value**.</span></span>
5. <span data-ttu-id="41887-190">选择**全部展开**。</span><span class="sxs-lookup"><span data-stu-id="41887-190">Select **Expand all**.</span></span>

    ![格式中 IBAN 字段的值](./media/er-data-debugger-debugging-format.png)

   <span data-ttu-id="41887-192">如您所见，格式绑定不负责截断空格，因为它为供应商银行帐户返回的 IBAN 代码包含空格。</span><span class="sxs-lookup"><span data-stu-id="41887-192">As you can see, the format binding isn't responsible for the truncated spaces because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="41887-193">因此，**BankIBAN** 元素被配置为使用截断空格的格式转换。</span><span class="sxs-lookup"><span data-stu-id="41887-193">Therefore, the **BankIBAN** element is configured to use a format transformation that truncates spaces.</span></span>

6. <span data-ttu-id="41887-194">关闭数据源调试器。</span><span class="sxs-lookup"><span data-stu-id="41887-194">Close the data source debugger.</span></span>

### <a name="review-the-format-transformations"></a><span data-ttu-id="41887-195">查看格式转换</span><span class="sxs-lookup"><span data-stu-id="41887-195">Review the format transformations</span></span>

1. <span data-ttu-id="41887-196">转到**组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="41887-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="41887-197">在**配置**页上，选择**付款模型** \> **ISO20022 信用转帐**。</span><span class="sxs-lookup"><span data-stu-id="41887-197">On the **Configurations** page, select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="41887-198">选择**设计器**，然后展开元素以选择 **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**。</span><span class="sxs-lookup"><span data-stu-id="41887-198">Select **Designer**, and then expand the elements to select **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.</span></span>

    ![格式设计器页面上的 BankIBAN 元素](./media/er-data-debugger-referred-transformation.png)

    <span data-ttu-id="41887-200">如您所见，**BankIBAN** 元素被配置为使用**删除非字母数字**转换。</span><span class="sxs-lookup"><span data-stu-id="41887-200">As you can see, the **BankIBAN** element is configured to use the **remove not alphanumeric** transformation.</span></span>

4. <span data-ttu-id="41887-201">选择**转换**选项卡。</span><span class="sxs-lookup"><span data-stu-id="41887-201">Select the **Transformations** tab.</span></span>

    ![BankIBAN 元素的“转换”选项卡](./media/er-data-debugger-transformation.png)

    <span data-ttu-id="41887-203">如您所见，**删除非字母数字**转换被配置为使用从提供的文本字符串中截断空格的表达式。</span><span class="sxs-lookup"><span data-stu-id="41887-203">As you can see, the **remove not alphanumeric** transformation is configured to use an expression that truncates spaces from the text string that is provided.</span></span>

## <a name="start-to-debug-in-the-operation-designer"></a><span data-ttu-id="41887-204">开始在操作设计器中进行调试</span><span class="sxs-lookup"><span data-stu-id="41887-204">Start to debug in the Operation designer</span></span>

<span data-ttu-id="41887-205">当您配置可以直接从操作设计器运行的 ER 格式的草稿版本时，可以通过在操作窗格中选择**开始调试**来访问数据源调试器。</span><span class="sxs-lookup"><span data-stu-id="41887-205">When you configure a draft version of the ER format that can be run directly from the Operation designer, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![格式设计器页面上的“开始调试”按钮](./media/er-data-debugger-run-from-designer.png)

<span data-ttu-id="41887-207">正在被编辑的 ER 格式的格式映射和格式组件可用于调试。</span><span class="sxs-lookup"><span data-stu-id="41887-207">The format mapping and format components of the ER format that is being edited are available for debugging.</span></span>

## <a name="start-to-debug-in-the-model-mapping-designer"></a><span data-ttu-id="41887-208">开始在模型映射设计器中进行调试</span><span class="sxs-lookup"><span data-stu-id="41887-208">Start to debug in the Model mapping designer</span></span>

<span data-ttu-id="41887-209">当您配置可以从**模型映射**页面运行的 ER 模型映射时，可以通过在操作窗格中选择**开始调试**来访问数据源调试器。</span><span class="sxs-lookup"><span data-stu-id="41887-209">When you configure an ER model mapping that can be run from the **Model mapping** page, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![模型映射设计器页面上的“开始调试”按钮](./media/er-data-debugger-run-from-designer-mapping.png)

<span data-ttu-id="41887-211">正在被编辑的 ER 映射的模型映射组件可用于调试。</span><span class="sxs-lookup"><span data-stu-id="41887-211">The model mapping component of the ER mapping that is being edited is available for debugging.</span></span>

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a><span data-ttu-id="41887-212">附录 1：获取 ER 解决方案</span><span class="sxs-lookup"><span data-stu-id="41887-212">Appendix 1: Get an ER solution</span></span>

### <a name="download-an-er-solution"></a><span data-ttu-id="41887-213">下载 ER 解决方案</span><span class="sxs-lookup"><span data-stu-id="41887-213">Download an ER solution</span></span>

<span data-ttu-id="41887-214">如果要使用 ER 解决方案为处理的供应商付款生成电子付款文件，则可以[下载](download-electronic-reporting-configuration-lcs.md) **ISO20022 信用转帐** ER 付款格式文件，可从 Microsoft Dynamics Lifecycle Services (LCS) 的共享资产库或从全局存储库中获得此格式文件。</span><span class="sxs-lookup"><span data-stu-id="41887-214">If you want to use an ER solution to generate an electronic payment file for a vendor payment that is processed, you can [download](download-electronic-reporting-configuration-lcs.md) the **ISO20022 Credit transfer** ER payment format that is available from the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) or from the Global repository.</span></span>

![在“配置存储库”页面上导入 ER 付款格式](./media/er-data-debugger-import-from-repo.png)

<span data-ttu-id="41887-216">除了所选的 ER 格式外，还必须将以下[配置](general-electronic-reporting.md#Configuration)自动导入到 Microsoft Dynamics 365 Finance 实例中，作为 **ISO20022 信用转帐** ER 解决方案的一部分：</span><span class="sxs-lookup"><span data-stu-id="41887-216">In addition to the selected ER format, the following [configurations](general-electronic-reporting.md#Configuration) must be automatically imported into your Microsoft Dynamics 365 Finance instance as part of the **ISO20022 Credit transfer** ER solution:</span></span>

- <span data-ttu-id="41887-217">**付款模型** [ER 数据模型配置](general-electronic-reporting.md#DataModelComponent)</span><span class="sxs-lookup"><span data-stu-id="41887-217">**Payment model** [ER data model configuration](general-electronic-reporting.md#DataModelComponent)</span></span>
- <span data-ttu-id="41887-218">**ISO20022 信用转帐** [ER 格式配置](general-electronic-reporting.md#FormatComponentOutbound)</span><span class="sxs-lookup"><span data-stu-id="41887-218">**ISO20022 Credit transfer** [ER format configuration](general-electronic-reporting.md#FormatComponentOutbound)</span></span>
- <span data-ttu-id="41887-219">**付款模型映射 1611** [ER 模型映射配置](general-electronic-reporting.md#ModelMappingComponent)</span><span class="sxs-lookup"><span data-stu-id="41887-219">**Payment model mapping 1611** [ER model mapping configuration](general-electronic-reporting.md#ModelMappingComponent)</span></span>
- <span data-ttu-id="41887-220">**付款模型到目标的映射 ISO20022** ER 模型映射配置</span><span class="sxs-lookup"><span data-stu-id="41887-220">**Payment model mapping to destination ISO20022** ER model mapping configuration</span></span>

<span data-ttu-id="41887-221">您可以在 ER 框架的**配置**页面（**组织管理** \> **电子申报** \> **配置**）上找到这些配置。</span><span class="sxs-lookup"><span data-stu-id="41887-221">You can find these configurations on the **Configurations** page of the ER framework (**Organization administration** \> **Electronic reporting** \> **Configurations**).</span></span>

![在“配置”页面上导入的配置](./media/er-data-debugger-configurations.png)

<span data-ttu-id="41887-223">如果配置树中缺少任何先前列出的配置，则必须从 LCS 共享资产库中手动下载它们，下载方法与下载 **ISO20022 信用转帐** ER 付款格式相同。</span><span class="sxs-lookup"><span data-stu-id="41887-223">If any of the previously listed configurations are missing in the configuration tree, you must manually download them from the LCS Shared asset library in the same way that you downloaded the **ISO20022 Credit transfer** ER payment format.</span></span>

### <a name="analyze-the-downloaded-er-solution"></a><span data-ttu-id="41887-224">分析下载的 ER 解决方案</span><span class="sxs-lookup"><span data-stu-id="41887-224">Analyze the downloaded ER solution</span></span>

#### <a name="review-the-model-mapping"></a><span data-ttu-id="41887-225">查看模型映射</span><span class="sxs-lookup"><span data-stu-id="41887-225">Review the model mapping</span></span>

1. <span data-ttu-id="41887-226">转到**组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="41887-226">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="41887-227">选择**付款模型** \> **付款模型映射 1611**。</span><span class="sxs-lookup"><span data-stu-id="41887-227">Select **Payment model** \> **Payment model mapping 1611**.</span></span>
3. <span data-ttu-id="41887-228">选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="41887-228">Select **Designer**.</span></span>
4. <span data-ttu-id="41887-229">选择**付款模型映射 ISO20022 CT** 映射记录。</span><span class="sxs-lookup"><span data-stu-id="41887-229">Select the **Payment model mapping ISO20022 CT** mapping record.</span></span>
5. <span data-ttu-id="41887-230">选择**设计器**，然后查看打开的模型映射。</span><span class="sxs-lookup"><span data-stu-id="41887-230">Select **Designer**, and then review the model mapping that is opened.</span></span>

    <span data-ttu-id="41887-231">请注意，数据模型的**付款**字段已绑定到 **\$notSentTransactions** 数据源，该数据源会返回正在处理的供应商付款行的列表。</span><span class="sxs-lookup"><span data-stu-id="41887-231">Notice that the **Payments** field of the data model is bound to the **\$notSentTransactions** data source that returns the list of vendor payment lines that are being processed.</span></span>

    ![模型映射设计器页面上的付款字段](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a><span data-ttu-id="41887-233">查看格式映射</span><span class="sxs-lookup"><span data-stu-id="41887-233">Review the format mapping</span></span>

1. <span data-ttu-id="41887-234">转到**组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="41887-234">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="41887-235">选择**付款模式** \> **ISO20022 信用转帐**。</span><span class="sxs-lookup"><span data-stu-id="41887-235">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="41887-236">选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="41887-236">Select **Designer**.</span></span>
4. <span data-ttu-id="41887-237">在**映射**选项卡上，查看打开的格式映射。</span><span class="sxs-lookup"><span data-stu-id="41887-237">On the **Mapping** tab, review the format mapping that is opened.</span></span>

    <span data-ttu-id="41887-238">请注意，**ISO20022CTReports** \> **XMLHeader** 文件的 **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** 元素已绑定到 **\$PaymentByDebtor** 数据源，该数据源被配置为对数据模型的**付款**字段的记录进行分组。</span><span class="sxs-lookup"><span data-stu-id="41887-238">Notice that the **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** element of the **ISO20022CTReports** \> **XMLHeader** file is bound to the **\$PaymentByDebtor** data source that is configured to group records of the data model's **Payments** field.</span></span>

    ![格式设计器页面上的 PmtInf 元素](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a><span data-ttu-id="41887-240">查看格式</span><span class="sxs-lookup"><span data-stu-id="41887-240">Review the format</span></span>

1. <span data-ttu-id="41887-241">转到**组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="41887-241">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="41887-242">选择**付款模式** \> **ISO20022 信用转帐**。</span><span class="sxs-lookup"><span data-stu-id="41887-242">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="41887-243">选择**设计器**，然后查看打开的格式。</span><span class="sxs-lookup"><span data-stu-id="41887-243">Select **Designer**, and then review the format that is opened.</span></span>

    <span data-ttu-id="41887-244">请注意，**Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** 下面的格式元素被配置为在付款文件中输入供应商帐户的 IBAN 代码。</span><span class="sxs-lookup"><span data-stu-id="41887-244">Notice that the format element under **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** is configured to enter the IBAN code of the vendor account in the payment file.</span></span>

    ![格式设计器页面上的 BankIBAN 元素](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a><span data-ttu-id="41887-246">附录 2：配置应付帐款</span><span class="sxs-lookup"><span data-stu-id="41887-246">Appendix 2: Configure Accounts payable</span></span>

### <a name="modify-a-vendor-property"></a><span data-ttu-id="41887-247">修改供应商属性</span><span class="sxs-lookup"><span data-stu-id="41887-247">Modify a vendor property</span></span>

1. <span data-ttu-id="41887-248">转到**应付帐款** \> **供应商** \> **所有供应商**。</span><span class="sxs-lookup"><span data-stu-id="41887-248">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="41887-249">选择供应商 **DE-01002**，然后在操作窗格内**供应商**选项卡上的**设置**组中，选择**银行帐户**。</span><span class="sxs-lookup"><span data-stu-id="41887-249">Select vendor **DE-01002**, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="41887-250">在**标识**快速选项卡上的 **IBAN** 字段中，<a name="enteredIBANcode"></a>输入 **GB33 BUKB 2020 1555 5555 55**。</span><span class="sxs-lookup"><span data-stu-id="41887-250">On the **Identification** FastTab, in the **IBAN** field, <a name="enteredIBANcode"></a>enter **GB33 BUKB 2020 1555 5555 55**.</span></span>
4. <span data-ttu-id="41887-251">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="41887-251">Select **Save**.</span></span>

![在“供应商银行帐户”页面上设置的 IBAN 字段](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a><span data-ttu-id="41887-253">设置付款方式</span><span class="sxs-lookup"><span data-stu-id="41887-253">Set up a method of payment</span></span>

1. <span data-ttu-id="41887-254">转到**应付帐款** \> **付款设置** \> **付款方式**。</span><span class="sxs-lookup"><span data-stu-id="41887-254">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="41887-255">选择 **SEPA CT** 付款方式。</span><span class="sxs-lookup"><span data-stu-id="41887-255">Select the **SEPA CT** payment method.</span></span>
3. <span data-ttu-id="41887-256">在**文件格式**快速选项卡上的**文件格式**部分中，将**通用电子导出格式**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="41887-256">On the **File formats** FastTab, in the **File formats** section, set the **Generic electronic Export format** option to **Yes**.</span></span>
4. <span data-ttu-id="41887-257">在**导出格式配置**字段中，选择 **ISO20022 信用转帐** ER 格式。</span><span class="sxs-lookup"><span data-stu-id="41887-257">In the **Export format configuration** field, select the **ISO20022 Credit transfer** ER format.</span></span>
5. <span data-ttu-id="41887-258">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="41887-258">Select **Save**.</span></span>

![“付款方式”页面上的文件格式设置](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a><span data-ttu-id="41887-260">添加供应商付款</span><span class="sxs-lookup"><span data-stu-id="41887-260">Add a vendor payment</span></span>

1. <span data-ttu-id="41887-261">转到**应付帐款** \> **付款** \> **供应商付款日记帐**。</span><span class="sxs-lookup"><span data-stu-id="41887-261">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="41887-262">添加新付款日记帐。</span><span class="sxs-lookup"><span data-stu-id="41887-262">Add a new payment journal.</span></span>
3. <span data-ttu-id="41887-263">选择**行**，然后添加新付款行。</span><span class="sxs-lookup"><span data-stu-id="41887-263">Select **Lines**, and add a new payment line.</span></span>
4. <span data-ttu-id="41887-264">在**帐户**字段中，选择供应商 **DE-01002**。</span><span class="sxs-lookup"><span data-stu-id="41887-264">In the **Account** field, select vendor **DE-01002**.</span></span>
5. <span data-ttu-id="41887-265">在**借项**字段中输入值。</span><span class="sxs-lookup"><span data-stu-id="41887-265">In the **Debit** field, enter a value.</span></span>
6. <span data-ttu-id="41887-266">在**付款方式**字段中，选择 **SEPA CT**。</span><span class="sxs-lookup"><span data-stu-id="41887-266">In the **Method of payment** field, select **SEPA CT**.</span></span>
7. <span data-ttu-id="41887-267">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="41887-267">Select **Save**.</span></span>

![在“供应商付款”页面上添加的供应商付款](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a><span data-ttu-id="41887-269">附录 3：处理供应商付款</span><span class="sxs-lookup"><span data-stu-id="41887-269">Appendix 3: Process a vendor payment</span></span>

1. <span data-ttu-id="41887-270">转到**应付帐款** \> **付款** \> **供应商付款日记帐**。</span><span class="sxs-lookup"><span data-stu-id="41887-270">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="41887-271">在**供应商付款日记帐**页面上，选择您先前创建的付款日记帐，然后选择**行**。</span><span class="sxs-lookup"><span data-stu-id="41887-271">On the **Vendor payment journal** page, select the payment journal that you previously created, and then select **Lines**.</span></span>
3. <span data-ttu-id="41887-272">选择付款行，然后选择**付款状态** \> **无**。</span><span class="sxs-lookup"><span data-stu-id="41887-272">Select the payment line, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="41887-273">选择**生成付款**。</span><span class="sxs-lookup"><span data-stu-id="41887-273">Select **Generate payments**.</span></span>
5. <span data-ttu-id="41887-274">在**付款方式**字段中，选择 **SEPA CT**。</span><span class="sxs-lookup"><span data-stu-id="41887-274">In the **Method of payment** field, select **SEPA CT**.</span></span>
6. <span data-ttu-id="41887-275">在**银行帐户**字段中，选择 **DEMF OPER**。</span><span class="sxs-lookup"><span data-stu-id="41887-275">In the **Bank account** field, select **DEMF OPER**.</span></span>
7. <span data-ttu-id="41887-276">在**生成付款**对话框中，选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="41887-276">In the **Generate payments** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="41887-277">在**电子申报参数**对话框中，选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="41887-277">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
