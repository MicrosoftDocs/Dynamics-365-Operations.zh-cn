---
title: 电子消息
description: 此主题提供 Microsoft Dynamics 365 for Finance and Operations 中电子消息的概述和设置信息。
author: ShylaThompson
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 082ad886f40a52457900523f44158da3ed939458
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "357925"
---
# <a name="electronic-messaging"></a><span data-ttu-id="bd46b-103">电子消息</span><span class="sxs-lookup"><span data-stu-id="bd46b-103">Electronic messaging</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd46b-104">此主题提供 Microsoft Dynamics 365 for Finance and Operations 中电子消息的概述和设置信息。</span><span class="sxs-lookup"><span data-stu-id="bd46b-104">This topic provides overview and setup information for electronic messaging in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="bd46b-105">最近，全世界各个国家和地区的政府与立法机构对在这些国家或地区注册的公司实施了报告要求。</span><span class="sxs-lookup"><span data-stu-id="bd46b-105">Recently, the governments and legislative authorities of various countries and regions around the world have implemented reporting requirements for companies that are registered in those countries or regions.</span></span> <span data-ttu-id="bd46b-106">要求的目的是支持数据以电子格式从这些公司、直接从具有、存储和处理数据的系统获取。</span><span class="sxs-lookup"><span data-stu-id="bd46b-106">The purpose of the requirements is to enable data to be obtained from those companies in electronic format, directly from the systems where it was accounted, stored, and processed.</span></span>

<span data-ttu-id="bd46b-107">Finance and Operations 中的电子消息功能支持在 Finance and Operations 与政府和立法机构为报告、提交和接收官方信息提供的系统之间进行各种电子互操作流程。</span><span class="sxs-lookup"><span data-stu-id="bd46b-107">The Electronic messages functionality in Finance and Operations supports various processes for electronic interoperation between Finance and Operations and the systems that governments and legislative authorities offer for reporting, submitting, and receiving official information.</span></span>

<span data-ttu-id="bd46b-108">电子消息功能已与**电子报告** (ER) 模块集成。</span><span class="sxs-lookup"><span data-stu-id="bd46b-108">The Electronic messages functionality is integrated with the **Electronic Reporting** (ER) module.</span></span> <span data-ttu-id="bd46b-109">因此，您可以为电子消息设置 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="bd46b-109">Therefore, you can set up ER formats for electronic messages.</span></span> <span data-ttu-id="bd46b-110">有关详细信息，请参阅[电子报告 (ER)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting)。</span><span class="sxs-lookup"><span data-stu-id="bd46b-110">For more information, see [Electronic reporting (ER)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).</span></span>

<span data-ttu-id="bd46b-111">电子消息基于以下实体：</span><span class="sxs-lookup"><span data-stu-id="bd46b-111">Electronic messaging is based on the following entities:</span></span>

- <span data-ttu-id="bd46b-112">**电子消息** – 应该在内部报告和/或传输的报表或申报。</span><span class="sxs-lookup"><span data-stu-id="bd46b-112">**Electronic message** – A report or declaration that should be reported and/or transmitted internally.</span></span> <span data-ttu-id="bd46b-113">示例是发送给税务局的报表。</span><span class="sxs-lookup"><span data-stu-id="bd46b-113">An example is a report that is sent to a tax office.</span></span>
- <span data-ttu-id="bd46b-114">**电子消息项** – 应包括在报告的消息中的记录。</span><span class="sxs-lookup"><span data-stu-id="bd46b-114">**Electronic message items** – Records that should be included in the message that is reported.</span></span>
- <span data-ttu-id="bd46b-115">**电子消息处理** – 应运行以收集所需的数据、生成报表、在 Microsoft Azure Blob 存储中存储数据、在系统之外传输报表、从系统外部获取响应以及基于收到的信息更新数据库的行动链（链接或未链接）。</span><span class="sxs-lookup"><span data-stu-id="bd46b-115">**Electronic message processing** – A chain of actions, either linked or unlinked, that should be run to collect the required data, generate reports, store data in Microsoft Azure Blob storage, transmit reports outside the system, get responses from outside the system, and update the database, based on the information that is received.</span></span>

<span data-ttu-id="bd46b-116">下图显示电子消息的数据流。</span><span class="sxs-lookup"><span data-stu-id="bd46b-116">The following illustration shows the flow of data for electronic messaging.</span></span>

![电子消息数据流](media/electronic-messaging-data-flow.png)

<span data-ttu-id="bd46b-118">电子消息功能支持以下场景：</span><span class="sxs-lookup"><span data-stu-id="bd46b-118">The Electronic messages functionality supports the following scenarios:</span></span>

- <span data-ttu-id="bd46b-119">手动创建消息和生成基于不同类型的关联导出 ER 格式的报表：Microsoft Excel、XML、JavaScript Object Notation (JSON)、PDF、文本和 Microsoft Word。</span><span class="sxs-lookup"><span data-stu-id="bd46b-119">Manually create messages and generate reports that are based on associated exporting ER formats of various types: Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, text, and Microsoft Word.</span></span>
- <span data-ttu-id="bd46b-120">自动创建和处理基于通过关联导入 ER 格式从当局请求和获取的信息的消息。</span><span class="sxs-lookup"><span data-stu-id="bd46b-120">Automatically create and process messages that are based on information that was requested and obtained from an authority via an associated importing ER format.</span></span>
- <span data-ttu-id="bd46b-121">作为消息项收集和处理来自数据源（Finance and Operations 表）的信息。</span><span class="sxs-lookup"><span data-stu-id="bd46b-121">Collect and process information from a data source (Finance and Operations table) as message items.</span></span>
- <span data-ttu-id="bd46b-122">存储附加信息，并通过调用有关消息或消息项的专门定义的可执行类评估不同值。</span><span class="sxs-lookup"><span data-stu-id="bd46b-122">Store additional information, and evaluate various values by calling specifically defined executable classes in relation to messages or message items.</span></span>
- <span data-ttu-id="bd46b-123">聚合在消息项中收集的信息，按消息拆分该信息，然后生成关联导出 ER 格式的报表。</span><span class="sxs-lookup"><span data-stu-id="bd46b-123">Aggregate information that is collected in message items, split that information by message, and generate reports that are in associated exporting ER formats.</span></span>
- <span data-ttu-id="bd46b-124">传输使用存储在 Azure Key Vault 中的安全信息生成到 Web 服务的报表。</span><span class="sxs-lookup"><span data-stu-id="bd46b-124">Transmit reports that are generated to a web service by using security information that is stored in Azure Key Vault.</span></span>
- <span data-ttu-id="bd46b-125">从 Web 服务获取响应、解释响应、根据需要更新 Finance and Operations 中的数据。</span><span class="sxs-lookup"><span data-stu-id="bd46b-125">Get a response from a web service, interpret the response, and update data in Finance and Operations as appropriate.</span></span>
- <span data-ttu-id="bd46b-126">存储和查看生成的所有报表。</span><span class="sxs-lookup"><span data-stu-id="bd46b-126">Store and review all the reports that are generated.</span></span>
- <span data-ttu-id="bd46b-127">存储和查看与为消息或消息项运行的行动有关的所有日志信息。</span><span class="sxs-lookup"><span data-stu-id="bd46b-127">Store and review all the log information that is related to actions that are run for a message or message item.</span></span>
- <span data-ttu-id="bd46b-128">通过各个消息状态和消息项状态控制处理。</span><span class="sxs-lookup"><span data-stu-id="bd46b-128">Control the processing through various message statuses and message item statuses.</span></span>

## <a name="set-up-electronic-messaging"></a><span data-ttu-id="bd46b-129">设置电子消息</span><span class="sxs-lookup"><span data-stu-id="bd46b-129">Set up electronic messaging</span></span>

<span data-ttu-id="bd46b-130">电子消息可以帮助您维护不同文档类型的不同电子报告流程。</span><span class="sxs-lookup"><span data-stu-id="bd46b-130">Electronic messaging can help you maintain different electronic reporting processes for different document types.</span></span> <span data-ttu-id="bd46b-131">在一些复杂的场景中，电子消息被设置为包含很多消息状态、消息项状态、行动、额外字段和可执行类的组合。</span><span class="sxs-lookup"><span data-stu-id="bd46b-131">In some complex scenarios, electronic messaging is set up to have a combination of many message statuses, message items statuses, actions, additional fields, and executable classes.</span></span> <span data-ttu-id="bd46b-132">对于这些场景，数据实体包可以导入。</span><span class="sxs-lookup"><span data-stu-id="bd46b-132">For these scenarios, packages of data entities are available for import.</span></span> <span data-ttu-id="bd46b-133">如果您使用这些数据实体包，您应使用数据管理工具将其导入到法人。</span><span class="sxs-lookup"><span data-stu-id="bd46b-133">If you use these data entity packages, you should import them to a legal entity by using the Data management tool.</span></span> <span data-ttu-id="bd46b-134">有关如何使用数据管理工具的详细信息，请参阅[数据管理](../../dev-itpro/data-entities/data-entities-data-packages.md)。</span><span class="sxs-lookup"><span data-stu-id="bd46b-134">For more information about how to use the Data management tool, see [Data management](../../dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

<span data-ttu-id="bd46b-135">如果您不导入数据实体包，您可以手动设置电子消息功能。</span><span class="sxs-lookup"><span data-stu-id="bd46b-135">If you don't import a data entity package, you can manually set up the Electronic messages functionality.</span></span> <span data-ttu-id="bd46b-136">在这种情况下，必须设置以下元素：</span><span class="sxs-lookup"><span data-stu-id="bd46b-136">In this case, you must set up the following elements:</span></span> 

- [<span data-ttu-id="bd46b-137">编号规则</span><span class="sxs-lookup"><span data-stu-id="bd46b-137">Number sequences</span></span>](#number-sequences)
- [<span data-ttu-id="bd46b-138">消息项类型和状态</span><span class="sxs-lookup"><span data-stu-id="bd46b-138">Message item types and statuses</span></span>](#message-item-types-and-statuses)
- [<span data-ttu-id="bd46b-139">消息状态</span><span class="sxs-lookup"><span data-stu-id="bd46b-139">Message statuses</span></span>](#message-statuses)
- [<span data-ttu-id="bd46b-140">附加字段</span><span class="sxs-lookup"><span data-stu-id="bd46b-140">Additional fields</span></span>](#additional-fields)
- [<span data-ttu-id="bd46b-141">可执行类设置</span><span class="sxs-lookup"><span data-stu-id="bd46b-141">Executable class settings</span></span>](#executable-class-settings)
- [<span data-ttu-id="bd46b-142">填充记录行为</span><span class="sxs-lookup"><span data-stu-id="bd46b-142">Populate records actions</span></span>](#populate-records-actions)
- [<span data-ttu-id="bd46b-143">Web 服务设置</span><span class="sxs-lookup"><span data-stu-id="bd46b-143">Web service settings</span></span>](#web-service-settings)
- [<span data-ttu-id="bd46b-144">消息处理操作</span><span class="sxs-lookup"><span data-stu-id="bd46b-144">Message processing actions</span></span>](#message-processing-actions)
- [<span data-ttu-id="bd46b-145">电子消息处理</span><span class="sxs-lookup"><span data-stu-id="bd46b-145">Electronic message processing</span></span>](#electronic-message-processing)

<span data-ttu-id="bd46b-146">以下部分提供有关每个元素的详细信息。</span><span class="sxs-lookup"><span data-stu-id="bd46b-146">The following sections provide more information about each of these elements.</span></span>

### <a name="number-sequences"></a><span data-ttu-id="bd46b-147">编号规则</span><span class="sxs-lookup"><span data-stu-id="bd46b-147">Number sequences</span></span>

<span data-ttu-id="bd46b-148">为消息和消息项设置编号规则。</span><span class="sxs-lookup"><span data-stu-id="bd46b-148">Set up number sequences for both messages and message items.</span></span> <span data-ttu-id="bd46b-149">编号规则用于自动对消息和消息项编号，分配的编号将用作系统中消息和消息项的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="bd46b-149">The number sequences are used to automatically number the messages and the message items, and the numbers that are assigned will be used as unique identifiers for the messages and message items in the system.</span></span> <span data-ttu-id="bd46b-150">您可以在**总帐参数**页（**总帐** \> **分类帐设置** \> **总帐参数**）上为电子消息设置编号规则。</span><span class="sxs-lookup"><span data-stu-id="bd46b-150">You can set up number sequences for electronic messaging on the **General ledger parameters** page (**General ledger** \> **Ledger setup** \> **General ledger parameters**).</span></span>

### <a name="message-item-types-and-statuses"></a><span data-ttu-id="bd46b-151">消息项类型和状态</span><span class="sxs-lookup"><span data-stu-id="bd46b-151">Message item types and statuses</span></span>

<span data-ttu-id="bd46b-152">消息项类型标识将在电子消息中使用的记录的类型。</span><span class="sxs-lookup"><span data-stu-id="bd46b-152">Message item types identify the types of records that will be used in electronic messages.</span></span> <span data-ttu-id="bd46b-153">您可以在**消息项类型**页（**税** \> **设置** \> **电子消息** \> **消息项类型**）设置消息项类型。</span><span class="sxs-lookup"><span data-stu-id="bd46b-153">You can set up message item types on the **Message item types** page (**Tax** \> **Setup** \> **Electronic messages** \> **Message item types**).</span></span>

<span data-ttu-id="bd46b-154">消息项状态标识将应用于您正在设置的处理中的消息项的状态。</span><span class="sxs-lookup"><span data-stu-id="bd46b-154">Message item statuses identify the statuses that will apply to message items in the processing that you're setting up.</span></span> <span data-ttu-id="bd46b-155">您可以在**消息项状态**页（**税** \> **设置** \> **电子消息** \> **消息项状态**）设置消息项类型。</span><span class="sxs-lookup"><span data-stu-id="bd46b-155">You can set up message item types on the **Message item statuses** page (**Tax** \> **Setup** \> **Electronic messages** \> **Message item statuses**).</span></span>

### <a name="message-statuses"></a><span data-ttu-id="bd46b-156">消息状态</span><span class="sxs-lookup"><span data-stu-id="bd46b-156">Message statuses</span></span>

<span data-ttu-id="bd46b-157">设置应该在消息处理中呈现的消息状态。</span><span class="sxs-lookup"><span data-stu-id="bd46b-157">Set up the message statuses that should be available in message processing.</span></span> <span data-ttu-id="bd46b-158">您可以在**消息状态**页（**税** \> **设置** \> **电子消息** \> **消息状态**）设置消息状态。</span><span class="sxs-lookup"><span data-stu-id="bd46b-158">You can set up message statuses on the **Message statuses** page (**Tax** \> **Setup** \> **Electronic messages** \> **Message statuses**).</span></span>

### <a name="additional-fields"></a><span data-ttu-id="bd46b-159">附加字段</span><span class="sxs-lookup"><span data-stu-id="bd46b-159">Additional fields</span></span>

<span data-ttu-id="bd46b-160">电子消息功能让您可以填充交易表中的记录。</span><span class="sxs-lookup"><span data-stu-id="bd46b-160">The Electronic messages functionality lets you populate records from a transactional table.</span></span> <span data-ttu-id="bd46b-161">这样，您可以为报告准备记录，然后报告它们。</span><span class="sxs-lookup"><span data-stu-id="bd46b-161">In this way, you can prepare the records for reporting and then report them.</span></span> <span data-ttu-id="bd46b-162">有时，交易表中没有足够的信息来根据报表要求报告记录。</span><span class="sxs-lookup"><span data-stu-id="bd46b-162">Sometimes, there isn't enough information in the transactional table to report a record according to the report requirements.</span></span> <span data-ttu-id="bd46b-163">您可以通过设置附加字段来填写必须为记录报告的所有信息。</span><span class="sxs-lookup"><span data-stu-id="bd46b-163">You can fill in all the information that must be reported for a record by setting up additional fields.</span></span> <span data-ttu-id="bd46b-164">附加字段可与消息和消息项关联。</span><span class="sxs-lookup"><span data-stu-id="bd46b-164">Additional fields can be associated with both messages and message items.</span></span> <span data-ttu-id="bd46b-165">您可以在**附加字段**页（**税** \> **设置** \> **电子消息** \> **附加字段**）设置附加字段。</span><span class="sxs-lookup"><span data-stu-id="bd46b-165">You can set up additional fields on the **Additional fields** page (**Tax** \> **Setup** \> **Electronic messages** \> **Additional fields**).</span></span>

<span data-ttu-id="bd46b-166">下表描述**附加字段**页的字段。</span><span class="sxs-lookup"><span data-stu-id="bd46b-166">The following table describes the fields on the **Additional fields** page.</span></span>

| <span data-ttu-id="bd46b-167">字段</span><span class="sxs-lookup"><span data-stu-id="bd46b-167">Field</span></span>                | <span data-ttu-id="bd46b-168">说明</span><span class="sxs-lookup"><span data-stu-id="bd46b-168">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="bd46b-169">字段名称</span><span class="sxs-lookup"><span data-stu-id="bd46b-169">Field name</span></span>           | <span data-ttu-id="bd46b-170">输入与此流程相关的消息项的其他属性的名称。</span><span class="sxs-lookup"><span data-stu-id="bd46b-170">Enter the name of an additional attribute of message items that are related to the process.</span></span> <span data-ttu-id="bd46b-171">在处理流程时，此名称显示在用户界面中。</span><span class="sxs-lookup"><span data-stu-id="bd46b-171">This name is shown in the user interface while you work with the process.</span></span> <span data-ttu-id="bd46b-172">它还可以用于与流程相关的 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="bd46b-172">It can also be used in ER configurations that are related to the process.</span></span> |
| <span data-ttu-id="bd46b-173">说明</span><span class="sxs-lookup"><span data-stu-id="bd46b-173">Description</span></span>          | <span data-ttu-id="bd46b-174">输入与此流程相关的消息项的其他属性的描述。</span><span class="sxs-lookup"><span data-stu-id="bd46b-174">Enter a description of the additional attribute of message items that are related to the process.</span></span> |
| <span data-ttu-id="bd46b-175">字段值</span><span class="sxs-lookup"><span data-stu-id="bd46b-175">Field value</span></span>          | <span data-ttu-id="bd46b-176">在报告过程中输入要使用的与消息项相关的字段值。</span><span class="sxs-lookup"><span data-stu-id="bd46b-176">Enter the field value to use in relation to a message item during reporting.</span></span> |
| <span data-ttu-id="bd46b-177">字段描述</span><span class="sxs-lookup"><span data-stu-id="bd46b-177">Field description</span></span>    | <span data-ttu-id="bd46b-178">在报告过程中输入要使用的与消息项相关的字段值的描述。</span><span class="sxs-lookup"><span data-stu-id="bd46b-178">Enter a description of the field value to use in relation to a message item during reporting.</span></span> |
| <span data-ttu-id="bd46b-179">科目类型</span><span class="sxs-lookup"><span data-stu-id="bd46b-179">Account type</span></span>         | <span data-ttu-id="bd46b-180">有些附加字段值可能被限制为特定科目类型。</span><span class="sxs-lookup"><span data-stu-id="bd46b-180">Some additional fields values might be limited to specific account types.</span></span> <span data-ttu-id="bd46b-181">选择以下值之一：**所有**、**客户**或**供应商**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-181">Select one of the following values: **All**, **Customer**, or **Vendor**.</span></span> |
| <span data-ttu-id="bd46b-182">帐户编码</span><span class="sxs-lookup"><span data-stu-id="bd46b-182">Account code</span></span>         | <span data-ttu-id="bd46b-183">如果您在**科目类型**字段中选择了**客户**或**供应商**，您可以进一步将字段值的使用限定为特定组或表。</span><span class="sxs-lookup"><span data-stu-id="bd46b-183">If you selected **Customer** or **Vendor** in the **Account type** field, you can further limit the use of field values to a specific group or table.</span></span> |
| <span data-ttu-id="bd46b-184">帐户/组编号</span><span class="sxs-lookup"><span data-stu-id="bd46b-184">Account/Group number</span></span> | <span data-ttu-id="bd46b-185">如果您在**科目类型**字段中选择了**客户**或**供应商**，并且如果您在**帐户编码**字段中输入了组或表，您可以在此字段中输入特定组或票务代理。</span><span class="sxs-lookup"><span data-stu-id="bd46b-185">If you selected **Customer** or **Vendor** in the **Account type** field, and if you entered a group or table in the **Account code** field, you can enter a specific group or counteragent in this field.</span></span> |
| <span data-ttu-id="bd46b-186">生效</span><span class="sxs-lookup"><span data-stu-id="bd46b-186">Effective</span></span>            | <span data-ttu-id="bd46b-187">指定应该开始考虑值的日期。</span><span class="sxs-lookup"><span data-stu-id="bd46b-187">Specify the date when the value should start to be considered.</span></span> |
| <span data-ttu-id="bd46b-188">到期</span><span class="sxs-lookup"><span data-stu-id="bd46b-188">Expiration</span></span>           | <span data-ttu-id="bd46b-189">指定应该停止考虑值的日期。</span><span class="sxs-lookup"><span data-stu-id="bd46b-189">Specify the date when the value should stop being considered.</span></span> |

### <a name="executable-class-settings"></a><span data-ttu-id="bd46b-190">可执行类设置</span><span class="sxs-lookup"><span data-stu-id="bd46b-190">Executable class settings</span></span>

<span data-ttu-id="bd46b-191">可执行类是一个 X++ 方法或类，如果流程需要一些评估，电子消息处理可以对行动调用它。</span><span class="sxs-lookup"><span data-stu-id="bd46b-191">An executable class is an X++ method or class that the electronic message processing can call in relation to an action if some evaluation is required for the process.</span></span>

<span data-ttu-id="bd46b-192">您可以在**可执行类设置**页（**税** \> **设置**\> **电子消息** \> **可执行类设置**）手动设置可执行类。</span><span class="sxs-lookup"><span data-stu-id="bd46b-192">You can manually set up an executable class on the **Executable class settings** page (**Tax** \> **Setup** \> **Electronic messages** \> **Executable class settings**).</span></span> <span data-ttu-id="bd46b-193">创建行，并设置以下字段。</span><span class="sxs-lookup"><span data-stu-id="bd46b-193">Create a line, and set the following fields.</span></span>

| <span data-ttu-id="bd46b-194">字段</span><span class="sxs-lookup"><span data-stu-id="bd46b-194">Field</span></span>                 | <span data-ttu-id="bd46b-195">说明</span><span class="sxs-lookup"><span data-stu-id="bd46b-195">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="bd46b-196">可执行类</span><span class="sxs-lookup"><span data-stu-id="bd46b-196">Executable class</span></span>      | <span data-ttu-id="bd46b-197">输入将在设置此类为其调用的消息处理行动期间使用的名称。</span><span class="sxs-lookup"><span data-stu-id="bd46b-197">Enter the name that will be used during the setup of a message processing action that this class is called in relation to.</span></span> |
| <span data-ttu-id="bd46b-198">说明</span><span class="sxs-lookup"><span data-stu-id="bd46b-198">Description</span></span>           | <span data-ttu-id="bd46b-199">输入可执行类的描述。</span><span class="sxs-lookup"><span data-stu-id="bd46b-199">Enter a description of the executable class.</span></span> |
| <span data-ttu-id="bd46b-200">可执行类名称</span><span class="sxs-lookup"><span data-stu-id="bd46b-200">Executable class name</span></span> | <span data-ttu-id="bd46b-201">选择 X++ 可执行类。</span><span class="sxs-lookup"><span data-stu-id="bd46b-201">Select an X++ executable class.</span></span> |
| <span data-ttu-id="bd46b-202">执行级别</span><span class="sxs-lookup"><span data-stu-id="bd46b-202">Execution level</span></span>       | <span data-ttu-id="bd46b-203">因为应为选择的可执行类预定义此字段，因此此字段将自动设置。</span><span class="sxs-lookup"><span data-stu-id="bd46b-203">This field is set automatically, because the value should be predefined for the selected executable class.</span></span> <span data-ttu-id="bd46b-204">此字段限制相关评估运行的级别。</span><span class="sxs-lookup"><span data-stu-id="bd46b-204">This field limits the level that related evaluation is run on.</span></span> |
| <span data-ttu-id="bd46b-205">类描述</span><span class="sxs-lookup"><span data-stu-id="bd46b-205">Class description</span></span>     | <span data-ttu-id="bd46b-206">因为应为选择的可执行类预定义此字段，因此此字段将自动设置。</span><span class="sxs-lookup"><span data-stu-id="bd46b-206">This field is set automatically, because the value should be predefined for the selected executable class.</span></span> |

### <a name="populate-records-actions"></a><span data-ttu-id="bd46b-207">填充记录行为</span><span class="sxs-lookup"><span data-stu-id="bd46b-207">Populate records actions</span></span>

<span data-ttu-id="bd46b-208">您使用填充记录操作设置将记录添加到消息项表以使其可以添加到电子消息的操作。</span><span class="sxs-lookup"><span data-stu-id="bd46b-208">You use populate records actions to set up actions that add records to the Message items table so that they can be added to an electronic message.</span></span> <span data-ttu-id="bd46b-209">例如，如果您的电子消息必须报告客户发票，则必须设置在**客户发票日记帐**表中链接的**填充记录**操作（在**数据源**字段中）。</span><span class="sxs-lookup"><span data-stu-id="bd46b-209">For example, if your electronic message must report customer invoices, you must set up a **Populate records** action that is linked on **Customer invoice journal** table (in **Data source** field).</span></span> <span data-ttu-id="bd46b-210">您可以在**填充记录行动**页（**税** \> **设置**\> **电子消息** \> **填充记录行动**）设置填充记录行动。</span><span class="sxs-lookup"><span data-stu-id="bd46b-210">You can set up populate records actions on the **Populate records action** page (**Tax** \> **Setup** \> **Electronic messages** \> **Populate records actions**).</span></span> <span data-ttu-id="bd46b-211">为应将记录添加到表的每个操作创建新记录，然后设置以下字段。</span><span class="sxs-lookup"><span data-stu-id="bd46b-211">Create a new record for every action that should add records to the table, and set the following fields.</span></span>

| <span data-ttu-id="bd46b-212">字段</span><span class="sxs-lookup"><span data-stu-id="bd46b-212">Field</span></span>       | <span data-ttu-id="bd46b-213">说明</span><span class="sxs-lookup"><span data-stu-id="bd46b-213">Description</span></span>                                                               |
|-------------|---------------------------------------------------------------------------|
| <span data-ttu-id="bd46b-214">姓名</span><span class="sxs-lookup"><span data-stu-id="bd46b-214">Name</span></span>        | <span data-ttu-id="bd46b-215">为在您的流程中填充记录的操作输入名称。</span><span class="sxs-lookup"><span data-stu-id="bd46b-215">Enter a name for the action that populates records in your process.</span></span>       |
| <span data-ttu-id="bd46b-216">说明</span><span class="sxs-lookup"><span data-stu-id="bd46b-216">Description</span></span> | <span data-ttu-id="bd46b-217">输入在您的流程中填充记录的操作的描述。</span><span class="sxs-lookup"><span data-stu-id="bd46b-217">Enter a description of the action that populates records in your process.</span></span> |

<span data-ttu-id="bd46b-218">在**数据源设置**快速选项卡上，为用于流程的每个数据源添加一个行，并设置以下字段。</span><span class="sxs-lookup"><span data-stu-id="bd46b-218">On the **Datasources setup** FastTab, add a line for every data source that is used for the process, and set the following fields.</span></span>

| <span data-ttu-id="bd46b-219">字段</span><span class="sxs-lookup"><span data-stu-id="bd46b-219">Field</span></span>                  | <span data-ttu-id="bd46b-220">说明</span><span class="sxs-lookup"><span data-stu-id="bd46b-220">Description</span></span> |
|------------------------|-------------|
| <span data-ttu-id="bd46b-221">姓名</span><span class="sxs-lookup"><span data-stu-id="bd46b-221">Name</span></span>                   | <span data-ttu-id="bd46b-222">输入数据源的名称。</span><span class="sxs-lookup"><span data-stu-id="bd46b-222">Enter a name for the data source.</span></span> |
| <span data-ttu-id="bd46b-223">消息项类型</span><span class="sxs-lookup"><span data-stu-id="bd46b-223">Message item type</span></span>      | <span data-ttu-id="bd46b-224">选择在为数据源创建记录时应使用的消息项的类型。</span><span class="sxs-lookup"><span data-stu-id="bd46b-224">Select the type of message item that should be used when records are created for the data source.</span></span> |
| <span data-ttu-id="bd46b-225">科目类型</span><span class="sxs-lookup"><span data-stu-id="bd46b-225">Account type</span></span>           | <span data-ttu-id="bd46b-226">选择应与来自数据源的记录关联的科目的类型。</span><span class="sxs-lookup"><span data-stu-id="bd46b-226">Select the type of account that should be associated with records from the data source.</span></span> |
| <span data-ttu-id="bd46b-227">主表名称</span><span class="sxs-lookup"><span data-stu-id="bd46b-227">Master table name</span></span>      | <span data-ttu-id="bd46b-228">选择应是数据源的 Finance and Operations 中的表。</span><span class="sxs-lookup"><span data-stu-id="bd46b-228">Select the table in Finance and Operations that should be a data source.</span></span> |
| <span data-ttu-id="bd46b-229">单据编号字段</span><span class="sxs-lookup"><span data-stu-id="bd46b-229">Document number field</span></span>  | <span data-ttu-id="bd46b-230">在所选表中选择应从中获取单据编号的字段。</span><span class="sxs-lookup"><span data-stu-id="bd46b-230">Select the field that the document number should be taken from in the selected table.</span></span> |
| <span data-ttu-id="bd46b-231">单据日期字段</span><span class="sxs-lookup"><span data-stu-id="bd46b-231">Document date field</span></span>    | <span data-ttu-id="bd46b-232">在所选表中选择应从中获取单据日期的字段。</span><span class="sxs-lookup"><span data-stu-id="bd46b-232">Select the field that the document date should be taken from in the selected table.</span></span> |
| <span data-ttu-id="bd46b-233">文档帐户字段</span><span class="sxs-lookup"><span data-stu-id="bd46b-233">Document account field</span></span> | <span data-ttu-id="bd46b-234">在所选表中选择应从中获取单据科目的字段。</span><span class="sxs-lookup"><span data-stu-id="bd46b-234">Select the field that the document account should be taken from in the selected table.</span></span> |
| <span data-ttu-id="bd46b-235">用户查询</span><span class="sxs-lookup"><span data-stu-id="bd46b-235">User query</span></span>             | <span data-ttu-id="bd46b-236">如果选中此复选框，则可以通过选择网格上方的**编辑查询**来设置查询。</span><span class="sxs-lookup"><span data-stu-id="bd46b-236">If this check box is selected, you can set up a query by selecting **Edit query** above the grid.</span></span> <span data-ttu-id="bd46b-237">否则，所有记录将从数据源填充。</span><span class="sxs-lookup"><span data-stu-id="bd46b-237">Otherwise, all the records will be populated from the data source.</span></span> |

### <a name="web-service-settings"></a><span data-ttu-id="bd46b-238">Web 服务设置</span><span class="sxs-lookup"><span data-stu-id="bd46b-238">Web service settings</span></span>

<span data-ttu-id="bd46b-239">您使用 Web 服务设置对传输到 Web 服务的直接数据传输进行设置。</span><span class="sxs-lookup"><span data-stu-id="bd46b-239">You use web service settings to set up direct data transmission to a web service.</span></span> <span data-ttu-id="bd46b-240">您可以在 **Web 服务设置**页（**税** \> **设置** \> **电子消息** \> **Web 服务设置**）设置 Web 服务设置。</span><span class="sxs-lookup"><span data-stu-id="bd46b-240">You can set up web service settings on the **Web service settings** page (**Tax** \> **Setup** \> **Electronic messages** \> **Web service settings**).</span></span>

<span data-ttu-id="bd46b-241">下表描述 **Web 服务设置**页的字段。</span><span class="sxs-lookup"><span data-stu-id="bd46b-241">The following table describes the fields on the **Web service settings** page.</span></span>

| <span data-ttu-id="bd46b-242">字段</span><span class="sxs-lookup"><span data-stu-id="bd46b-242">Field</span></span>                   | <span data-ttu-id="bd46b-243">说明</span><span class="sxs-lookup"><span data-stu-id="bd46b-243">Description</span></span> |
|-------------------------|-------------|
| <span data-ttu-id="bd46b-244">Web 服务</span><span class="sxs-lookup"><span data-stu-id="bd46b-244">Web service</span></span>             | <span data-ttu-id="bd46b-245">为 Web 服务输入名称。</span><span class="sxs-lookup"><span data-stu-id="bd46b-245">Enter a name for the web service.</span></span> |
| <span data-ttu-id="bd46b-246">说明</span><span class="sxs-lookup"><span data-stu-id="bd46b-246">Description</span></span>             | <span data-ttu-id="bd46b-247">输入 Web 服务的描述。</span><span class="sxs-lookup"><span data-stu-id="bd46b-247">Enter a description of the web service.</span></span> |
| <span data-ttu-id="bd46b-248">Internet 地址</span><span class="sxs-lookup"><span data-stu-id="bd46b-248">Internet address</span></span>        | <span data-ttu-id="bd46b-249">输入 Web 服务的 Internet 地址。</span><span class="sxs-lookup"><span data-stu-id="bd46b-249">Enter the internet address of the web service.</span></span> |
| <span data-ttu-id="bd46b-250">证书</span><span class="sxs-lookup"><span data-stu-id="bd46b-250">Certificate</span></span>             | <span data-ttu-id="bd46b-251">选择此前设置的密钥保管库证书。</span><span class="sxs-lookup"><span data-stu-id="bd46b-251">Select a Key Vault certificate that has previously been set up.</span></span> |
| <span data-ttu-id="bd46b-252">响应类型 - XML</span><span class="sxs-lookup"><span data-stu-id="bd46b-252">The response type – XML</span></span> | <span data-ttu-id="bd46b-253">如果响应类型是 XML，将此选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-253">Set this option to **Yes** if the response type is XML.</span></span> |
| <span data-ttu-id="bd46b-254">请求方法</span><span class="sxs-lookup"><span data-stu-id="bd46b-254">Request method</span></span>          | <span data-ttu-id="bd46b-255">指定请求的方法。</span><span class="sxs-lookup"><span data-stu-id="bd46b-255">Specify the method of the request.</span></span> <span data-ttu-id="bd46b-256">HTTP 定义指示应该为给定资源执行的操作的一组请求方法。</span><span class="sxs-lookup"><span data-stu-id="bd46b-256">HTTP defines a set of request methods that indicate the action that should be performed for a given resource.</span></span> <span data-ttu-id="bd46b-257">方法可以是 **GET**、**POST**，或其他 HTTP 方法。</span><span class="sxs-lookup"><span data-stu-id="bd46b-257">The method can be **GET**, **POST**, or another HTTP method.</span></span> |
| <span data-ttu-id="bd46b-258">请求标题</span><span class="sxs-lookup"><span data-stu-id="bd46b-258">Request headers</span></span>         | <span data-ttu-id="bd46b-259">指定请求标题。</span><span class="sxs-lookup"><span data-stu-id="bd46b-259">Specify request headers.</span></span> <span data-ttu-id="bd46b-260">请求标题是可以在 HTTP 请求中使用但与消息内容不相关的 HTTP 标题。</span><span class="sxs-lookup"><span data-stu-id="bd46b-260">A request header is an HTTP header that can be used in an HTTP request, and that isn't related to the content of the message.</span></span> |
| <span data-ttu-id="bd46b-261">接受编码</span><span class="sxs-lookup"><span data-stu-id="bd46b-261">Accept encoding</span></span>         | <span data-ttu-id="bd46b-262">指定接受编码。</span><span class="sxs-lookup"><span data-stu-id="bd46b-262">Specify the Accept-Encoding.</span></span> <span data-ttu-id="bd46b-263">接受编码请求 HTTP 标题给予客户可以了解的内容编码的建议。</span><span class="sxs-lookup"><span data-stu-id="bd46b-263">The Accept-Encoding request HTTP header advertises the content encoding that the client can understand.</span></span> <span data-ttu-id="bd46b-264">此内容编码通常是压缩算法。</span><span class="sxs-lookup"><span data-stu-id="bd46b-264">This content encoding is usually a compression algorithm.</span></span> |
| <span data-ttu-id="bd46b-265">内容类型</span><span class="sxs-lookup"><span data-stu-id="bd46b-265">Content type</span></span>            | <span data-ttu-id="bd46b-266">指定内容类型。</span><span class="sxs-lookup"><span data-stu-id="bd46b-266">Specify the content type.</span></span> <span data-ttu-id="bd46b-267">内容类型实体标题指示资源的媒体类型。</span><span class="sxs-lookup"><span data-stu-id="bd46b-267">The Content-Type entity header indicates the media type of the resource.</span></span> |

### <a name="message-processing-actions"></a><span data-ttu-id="bd46b-268">消息处理操作</span><span class="sxs-lookup"><span data-stu-id="bd46b-268">Message processing actions</span></span>

<span data-ttu-id="bd46b-269">您使用消息处理操作创建流程的操作和设置操作参数。</span><span class="sxs-lookup"><span data-stu-id="bd46b-269">You use message processing actions to create actions for your processes and set up their parameters.</span></span> <span data-ttu-id="bd46b-270">您可以在**消息处理操作**页（**税** \> **设置** \> **电子消息** \> **消息处理操作**）设置消息处理操作。</span><span class="sxs-lookup"><span data-stu-id="bd46b-270">You can set up message processing actions on the **Message processing actions** page (**Tax** \> **Setup** \> **Electronic messages** \> **Message processing actions**).</span></span>

<span data-ttu-id="bd46b-271">下表描述**消息处理操作**页的字段。</span><span class="sxs-lookup"><span data-stu-id="bd46b-271">The following tables describe the fields on the **Message processing actions** page.</span></span>

#### <a name="general-fasttab"></a><span data-ttu-id="bd46b-272">常规快速选项卡</span><span class="sxs-lookup"><span data-stu-id="bd46b-272">General FastTab</span></span>

| <span data-ttu-id="bd46b-273">字段</span><span class="sxs-lookup"><span data-stu-id="bd46b-273">Field</span></span>                   | <span data-ttu-id="bd46b-274">说明</span><span class="sxs-lookup"><span data-stu-id="bd46b-274">Description</span></span> |
|-------------------------|-------------|
| <span data-ttu-id="bd46b-275">操作类型</span><span class="sxs-lookup"><span data-stu-id="bd46b-275">Action type</span></span>             | <span data-ttu-id="bd46b-276">选择操作的类型。</span><span class="sxs-lookup"><span data-stu-id="bd46b-276">Select the type of action.</span></span> <span data-ttu-id="bd46b-277">有关可用选项的信息，请参阅[消息处理操作类型](#message-processing-action-types)部分。</span><span class="sxs-lookup"><span data-stu-id="bd46b-277">For information about the available options, see the [Message processing action types](#message-processing-action-types) section.</span></span> |
| <span data-ttu-id="bd46b-278">格式映射</span><span class="sxs-lookup"><span data-stu-id="bd46b-278">Format mapping</span></span>          | <span data-ttu-id="bd46b-279">选择应为操作调用的 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="bd46b-279">Select the ER format that should be called for the action.</span></span> <span data-ttu-id="bd46b-280">此字段仅可用于**电子报告导出**、**电子报告导入**和**电子报告导出消息**类型的操作。</span><span class="sxs-lookup"><span data-stu-id="bd46b-280">This field is available only for actions of the **Electronic reporting export**, **Electronic reporting import**, and **Electronic reporting export message** types.</span></span> |
| <span data-ttu-id="bd46b-281">消息项类型</span><span class="sxs-lookup"><span data-stu-id="bd46b-281">Message item type</span></span>       | <span data-ttu-id="bd46b-282">选择应为其评估操作的记录的类型。</span><span class="sxs-lookup"><span data-stu-id="bd46b-282">Select the type of records that the action should be evaluated for.</span></span> <span data-ttu-id="bd46b-283">此字段可用于**消息项执行级别**、**电子报告导出**和**电子报告导入**类型以及其他一些类型的操作。</span><span class="sxs-lookup"><span data-stu-id="bd46b-283">This field is available for actions of the **Message item execution level**, **Electronic reporting export**, and **Electronic reporting import** types, and also some other types.</span></span> <span data-ttu-id="bd46b-284">如果将此字段留空，为消息处理定义的所有消息项类型都将进行评估。</span><span class="sxs-lookup"><span data-stu-id="bd46b-284">If you leave this field blank, all the message item types that are defined for the message processing are evaluated.</span></span> |
| <span data-ttu-id="bd46b-285">可执行类</span><span class="sxs-lookup"><span data-stu-id="bd46b-285">Executable class</span></span>        | <span data-ttu-id="bd46b-286">选择以前创建的可执行类设置。</span><span class="sxs-lookup"><span data-stu-id="bd46b-286">Select executable class settings that were previously created.</span></span> <span data-ttu-id="bd46b-287">此字段仅可用于**消息项执行级别**和**消息项执行级别**类型的操作。</span><span class="sxs-lookup"><span data-stu-id="bd46b-287">This field is available only for actions of the **Message item execution level** and **Message item execution level** types.</span></span> |
| <span data-ttu-id="bd46b-288">填充记录行为</span><span class="sxs-lookup"><span data-stu-id="bd46b-288">Populate records action</span></span> | <span data-ttu-id="bd46b-289">选择此前设置的填充记录操作。</span><span class="sxs-lookup"><span data-stu-id="bd46b-289">Select a populate records action that was previously set up.</span></span> <span data-ttu-id="bd46b-290">此字段仅可用于**填充记录**类型的操作。</span><span class="sxs-lookup"><span data-stu-id="bd46b-290">This field is available only for actions of the **Populate records** type.</span></span> |

##### <a name="message-processing-action-types"></a><span data-ttu-id="bd46b-291">消息处理操作类型</span><span class="sxs-lookup"><span data-stu-id="bd46b-291">Message processing action types</span></span>

<span data-ttu-id="bd46b-292">**操作类型**字段中具有以下选项：</span><span class="sxs-lookup"><span data-stu-id="bd46b-292">The following options are available in the **Action type** field:</span></span>

- <span data-ttu-id="bd46b-293">**填充记录** – **填充记录**操作必须在以前设置。</span><span class="sxs-lookup"><span data-stu-id="bd46b-293">**Populate records** – A **Populate records** action must previously be set up.</span></span> <span data-ttu-id="bd46b-294">将其与**填充记录**类型的操作关联以使其包括在处理中。</span><span class="sxs-lookup"><span data-stu-id="bd46b-294">Associate it with an action of the **Populate records** type to enable it to be included in processing.</span></span> <span data-ttu-id="bd46b-295">假定此操作类型用于消息处理的第一个操作。</span><span class="sxs-lookup"><span data-stu-id="bd46b-295">It's assumed that this action type is used for the first action in message processing.</span></span> <span data-ttu-id="bd46b-296">因此，仅可以为此类型的操作设置结果状态。</span><span class="sxs-lookup"><span data-stu-id="bd46b-296">Therefore, only a result status can be set up for an action of this type.</span></span> <span data-ttu-id="bd46b-297">不能设置初始状态。</span><span class="sxs-lookup"><span data-stu-id="bd46b-297">An initial status can't be set up.</span></span>
- <span data-ttu-id="bd46b-298">**创建消息** – 使用此类型允许用户在**电子消息**页手动创建消息。</span><span class="sxs-lookup"><span data-stu-id="bd46b-298">**Create message** – Use this type to let users manually create messages on the **Electronic message** page.</span></span> <span data-ttu-id="bd46b-299">无法为此类型的操作设置初始状态。</span><span class="sxs-lookup"><span data-stu-id="bd46b-299">An initial status can't be set up for an action of this type.</span></span>
- <span data-ttu-id="bd46b-300">**消息执行级别** – 使用此类型设置应在消息级别评估的可执行类。</span><span class="sxs-lookup"><span data-stu-id="bd46b-300">**Message execution level** – Use this type to set up an executable class that should be evaluated at the message level.</span></span>
- <span data-ttu-id="bd46b-301">**消息项执行级别** – 使用此类型设置应在消息项级别评估的可执行类。</span><span class="sxs-lookup"><span data-stu-id="bd46b-301">**Message item execution level** – Use this type to set up an executable class that should be evaluated at the message item level.</span></span>
- <span data-ttu-id="bd46b-302">**电子报告导出** – 为应基于消息项级别的导出 ER 配置生成报表的操作使用此类型。</span><span class="sxs-lookup"><span data-stu-id="bd46b-302">**Electronic reporting export** – Use this type for actions that should generate a report that is based on an exporting ER configuration at the message item level.</span></span>
- <span data-ttu-id="bd46b-303">**电子报告导出消息** – 为应基于消息级别的导出 ER 配置生成报表的操作使用此类型（例如，当消息不包含任何消息项时）。</span><span class="sxs-lookup"><span data-stu-id="bd46b-303">**Electronic reporting export message** – Use this type for actions that should generate a report that is based on an exporting ER configuration at the message level (for example, when a message doesn't have any message items).</span></span>
- <span data-ttu-id="bd46b-304">**电子报告导入** – 为应基于导入 ER 配置生成报表的操作使用此类型。</span><span class="sxs-lookup"><span data-stu-id="bd46b-304">**Electronic reporting import** – Use this type for actions that should generate a report that is based on an importing ER configuration.</span></span>
- <span data-ttu-id="bd46b-305">**消息级别用户处理** – 为假定一些用户手动操作的操作使用此类型。</span><span class="sxs-lookup"><span data-stu-id="bd46b-305">**Message level user processing** – Use this type for actions that assume some manual actions by the user.</span></span> <span data-ttu-id="bd46b-306">例如，用户可能更新消息的状态。</span><span class="sxs-lookup"><span data-stu-id="bd46b-306">For example, the user might update the status of messages.</span></span>
- <span data-ttu-id="bd46b-307">**用户处理** – 为假定一些用户手动操作的操作使用此类型。</span><span class="sxs-lookup"><span data-stu-id="bd46b-307">**User processing** – Use this type for actions that assume some manual action by the user.</span></span> <span data-ttu-id="bd46b-308">例如，用户可能更新消息项的状态。</span><span class="sxs-lookup"><span data-stu-id="bd46b-308">For example, the user might update the status of messages items.</span></span>
- <span data-ttu-id="bd46b-309">**Web 服务** – 为应将生成的报表传输到 Web 服务的操作使用此类型。</span><span class="sxs-lookup"><span data-stu-id="bd46b-309">**Web service** – Use this type for actions that should transmit a generated report to a web service.</span></span> <span data-ttu-id="bd46b-310">此操作类型不用于“意大利采购和销售发票通信”报告。</span><span class="sxs-lookup"><span data-stu-id="bd46b-310">This action type isn't used for Italian Purchase and Sales Invoices Communication reporting.</span></span>
- <span data-ttu-id="bd46b-311">**请求验证** – 使用此类型从服务器请求验证。</span><span class="sxs-lookup"><span data-stu-id="bd46b-311">**Request verification** – Use this type to request verification from a server.</span></span>

#### <a name="initial-statuses-fasttab"></a><span data-ttu-id="bd46b-312">初始状态快速选项卡</span><span class="sxs-lookup"><span data-stu-id="bd46b-312">Initial statuses FastTab</span></span>

> [!NOTE]
> <span data-ttu-id="bd46b-313">**初始状态**快速选项卡不可用于具有**填充记录**或**创建消息**初始类型的操作。</span><span class="sxs-lookup"><span data-stu-id="bd46b-313">The **Initial statuses** FastTab isn't available for actions that have an initial type of **Populate records** or **Create message**.</span></span>

| <span data-ttu-id="bd46b-314">字段</span><span class="sxs-lookup"><span data-stu-id="bd46b-314">Field</span></span>               | <span data-ttu-id="bd46b-315">说明</span><span class="sxs-lookup"><span data-stu-id="bd46b-315">Description</span></span>                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd46b-316">消息项状态</span><span class="sxs-lookup"><span data-stu-id="bd46b-316">Message item status</span></span> | <span data-ttu-id="bd46b-317">选择应为其评估所选的消息处理操作的消息项状态。</span><span class="sxs-lookup"><span data-stu-id="bd46b-317">Select the message item status that the selected message processing action should be evaluated for.</span></span> |
| <span data-ttu-id="bd46b-318">说明</span><span class="sxs-lookup"><span data-stu-id="bd46b-318">Description</span></span>         | <span data-ttu-id="bd46b-319">所选消息项状态的描述。</span><span class="sxs-lookup"><span data-stu-id="bd46b-319">A description of the selected message item status.</span></span>                                                  |

#### <a name="result-statuses-fasttab"></a><span data-ttu-id="bd46b-320">结果状态快速选项卡</span><span class="sxs-lookup"><span data-stu-id="bd46b-320">Result statuses FastTab</span></span>

| <span data-ttu-id="bd46b-321">字段</span><span class="sxs-lookup"><span data-stu-id="bd46b-321">Field</span></span>               | <span data-ttu-id="bd46b-322">说明</span><span class="sxs-lookup"><span data-stu-id="bd46b-322">Description</span></span> |
|---------------------|-------------|
| <span data-ttu-id="bd46b-323">消息状态</span><span class="sxs-lookup"><span data-stu-id="bd46b-323">Message status</span></span>      | <span data-ttu-id="bd46b-324">选择应为其评估所选的消息处理操作的消息状态。</span><span class="sxs-lookup"><span data-stu-id="bd46b-324">Select the message statuses that the selected message processing action should be evaluated for.</span></span> <span data-ttu-id="bd46b-325">此字段仅可用于在消息级别评估的消息处理操作。</span><span class="sxs-lookup"><span data-stu-id="bd46b-325">This field is available only for message processing actions that are evaluated at the message level.</span></span> <span data-ttu-id="bd46b-326">例如，它不可用于**电子报告导出**和**电子报告导入**类型的操作。</span><span class="sxs-lookup"><span data-stu-id="bd46b-326">For example, it's available for actions of the **Electronic reporting export** and **Electronic reporting import** types.</span></span> <span data-ttu-id="bd46b-327">它不可用于**用户处理**和**消息项执行级别**类型的操作。</span><span class="sxs-lookup"><span data-stu-id="bd46b-327">It isn't available for actions of the **User processing** and **Message item execution level** types.</span></span> |
| <span data-ttu-id="bd46b-328">说明</span><span class="sxs-lookup"><span data-stu-id="bd46b-328">Description</span></span>         | <span data-ttu-id="bd46b-329">所选消息状态的描述。</span><span class="sxs-lookup"><span data-stu-id="bd46b-329">A description of the selected message status.</span></span> |
| <span data-ttu-id="bd46b-330">响应类型</span><span class="sxs-lookup"><span data-stu-id="bd46b-330">Response type</span></span>       | <span data-ttu-id="bd46b-331">所选消息状态的响应类型。</span><span class="sxs-lookup"><span data-stu-id="bd46b-331">The response type of the selected message status.</span></span> |
| <span data-ttu-id="bd46b-332">消息项状态</span><span class="sxs-lookup"><span data-stu-id="bd46b-332">Message item status</span></span> | <span data-ttu-id="bd46b-333">选择应在评估所选消息处理操作后可用的生成的状态。</span><span class="sxs-lookup"><span data-stu-id="bd46b-333">Select the resulting statuses that should be available after the selected message processing action is evaluated.</span></span> <span data-ttu-id="bd46b-334">此字段仅可用于在消息项级别评估的消息处理操作。</span><span class="sxs-lookup"><span data-stu-id="bd46b-334">This field is available only for message processing actions that are evaluated at the message item level.</span></span> <span data-ttu-id="bd46b-335">例如，它可用于**用户处理**和**消息项执行级别**类型的操作。</span><span class="sxs-lookup"><span data-stu-id="bd46b-335">For example, it's available for actions of the **User processing** and **Message item execution level** types.</span></span> <span data-ttu-id="bd46b-336">对于在消息级别评估的消息处理操作，此字段显示为所选消息状态设置的消息项状态。</span><span class="sxs-lookup"><span data-stu-id="bd46b-336">For message processing actions that are evaluated at the message level, this field shows the message item status that was set up for the selected message status.</span></span> |

### <a name="electronic-message-processing"></a><span data-ttu-id="bd46b-337">电子消息处理</span><span class="sxs-lookup"><span data-stu-id="bd46b-337">Electronic message processing</span></span>

<span data-ttu-id="bd46b-338">电子消息处理是电子消息功能的基本概念。</span><span class="sxs-lookup"><span data-stu-id="bd46b-338">Electronic message processing is a basic concept of the Electronic messages functionality.</span></span> <span data-ttu-id="bd46b-339">它聚合应为电子消息评估的操作。</span><span class="sxs-lookup"><span data-stu-id="bd46b-339">It aggregates actions that should be evaluated for the electronic message.</span></span> <span data-ttu-id="bd46b-340">操作可以通过初始状态和结果状态链接。</span><span class="sxs-lookup"><span data-stu-id="bd46b-340">The actions can be linked via an initial status and a result status.</span></span> <span data-ttu-id="bd46b-341">或者，**用户处理**类型的操作可以独立启动。</span><span class="sxs-lookup"><span data-stu-id="bd46b-341">Alternatively, actions of the **User processing** type can be started independently.</span></span> <span data-ttu-id="bd46b-342">在**电子消息处理**页（**税** \> **设置** \> **电子消息** \> **电子消息处理**），还可以选择应为处理支持的附加字段。</span><span class="sxs-lookup"><span data-stu-id="bd46b-342">On the **Electronic message processing** page (**Tax** \> **Setup** \> **Electronic messages** \> **Electronic message processing**), you can also select additional fields that should be supported for the processing.</span></span>

<span data-ttu-id="bd46b-343">**操作**快速选项卡让您可以将预定义的操作添加到处理。</span><span class="sxs-lookup"><span data-stu-id="bd46b-343">The **Action** FastTab lets you add predefined actions to the processing.</span></span> <span data-ttu-id="bd46b-344">您可以指定是否必须单独运行操作，或者它是否可以通过处理启动。</span><span class="sxs-lookup"><span data-stu-id="bd46b-344">You can specify whether an action must be run separately, or whether it can be initiated by the processing.</span></span> <span data-ttu-id="bd46b-345">（用户操作必须单独运行。）</span><span class="sxs-lookup"><span data-stu-id="bd46b-345">(User actions must be run separately.)</span></span>

<span data-ttu-id="bd46b-346">**消息项附加字段**快速选项卡让您可以添加与消息项相关的预定义附加字段。</span><span class="sxs-lookup"><span data-stu-id="bd46b-346">The **Message item additional fields** FastTab lets you add predefined additional fields that are related to message items.</span></span> <span data-ttu-id="bd46b-347">您必须为与字段相关的每个消息项类型添加附加字段。</span><span class="sxs-lookup"><span data-stu-id="bd46b-347">You must add additional fields for each type of message item that the fields are related to.</span></span>

<span data-ttu-id="bd46b-348">**消息附加字段**快速选项卡让您可以添加与消息相关的预定义附加字段。</span><span class="sxs-lookup"><span data-stu-id="bd46b-348">The **Message additional fields** FastTab lets you add predefined additional fields that are related to messages.</span></span>

<span data-ttu-id="bd46b-349">**安全角色**快速选项卡允许您设置在进行特定处理的系统中预定义的安全角色。</span><span class="sxs-lookup"><span data-stu-id="bd46b-349">The **Security roles** FastTab lets you set up the security roles that are predefined in the system for specific processing.</span></span> <span data-ttu-id="bd46b-350">具有特定角色的用户将只看到为该角色定义的处理。</span><span class="sxs-lookup"><span data-stu-id="bd46b-350">Users who have a specific role will see only processing that is defined for that role.</span></span>

<span data-ttu-id="bd46b-351">**批处理**快速选项卡让您可以设置在批处理制度中执行的处理。</span><span class="sxs-lookup"><span data-stu-id="bd46b-351">The **Batch** FastTab lets you set up processing to work in a batch regime.</span></span>

## <a name="work-with-electronic-messages-functionality"></a><span data-ttu-id="bd46b-352">使用电子消息功能</span><span class="sxs-lookup"><span data-stu-id="bd46b-352">Work with Electronic messages functionality</span></span>

<span data-ttu-id="bd46b-353">如果您在消息级别工作，**电子消息**页（**税** \> **查询和报表** \> **电子消息** \> **电子消息**）更有用。</span><span class="sxs-lookup"><span data-stu-id="bd46b-353">If you're working at the message level, the **Electronic messages** page (**Tax** \> **Inquiries and reports** \> **Electronic messages** \> **Electronic messages**) is more useful.</span></span> <span data-ttu-id="bd46b-354">如果您在数据收集（消息项）级别运行，**电子消息项**页（**税** \> **查询和报表** \> **电子消息** \> **电子消息项**）更有用。</span><span class="sxs-lookup"><span data-stu-id="bd46b-354">If you're operating at the data collection (message item) level, the **Electronic message items** page (**Tax** \> **Inquires and reports** \> **Electronic messages** \> **Electronic message items**) is more useful.</span></span>

### <a name="electronic-messages"></a><span data-ttu-id="bd46b-355">电子消息</span><span class="sxs-lookup"><span data-stu-id="bd46b-355">Electronic messages</span></span>

<span data-ttu-id="bd46b-356">**电子消息**页根据您的角色显示对您可用的处理。</span><span class="sxs-lookup"><span data-stu-id="bd46b-356">The **Electronic messages** page presents the processing that is available to you, based on your role.</span></span> <span data-ttu-id="bd46b-357">安全角色与该处理的设置中的处理关联。</span><span class="sxs-lookup"><span data-stu-id="bd46b-357">Security roles are associated with processing in the setup of that processing.</span></span> <span data-ttu-id="bd46b-358">对于每个您可用的处理，此页显示电子消息和与之相关的信息。</span><span class="sxs-lookup"><span data-stu-id="bd46b-358">For each processing that is available to you, the page shows electronic messages and information that is related to them.</span></span>

<span data-ttu-id="bd46b-359">**消息**快速选项卡显示所选处理的电子消息。</span><span class="sxs-lookup"><span data-stu-id="bd46b-359">The **Messages** FastTab shows electronic messages for the selected processing.</span></span> <span data-ttu-id="bd46b-360">根据所选消息和预定义处理的状态，您可以通过选择网格上方的按钮运行一些操作：</span><span class="sxs-lookup"><span data-stu-id="bd46b-360">Depending on the status of the selected message and predefined processing, you can run some actions by selecting the buttons above the grid:</span></span>

- <span data-ttu-id="bd46b-361">**新建** – 此按钮与**创建消息**类型的操作关联。</span><span class="sxs-lookup"><span data-stu-id="bd46b-361">**New** – This button is associated with actions of the **Create message** type.</span></span>
- <span data-ttu-id="bd46b-362">**删除** – 如果选择了所选消息的当前状态的**允许删除**复选框，此按钮可用。</span><span class="sxs-lookup"><span data-stu-id="bd46b-362">**Delete** – This button is available if the **Allow delete** check box is selected for the current status of the selected message.</span></span>
- <span data-ttu-id="bd46b-363">**生成报表** – 此按钮与**电子报告导出消息**类型的操作关联。</span><span class="sxs-lookup"><span data-stu-id="bd46b-363">**Generate report** – This button is associated with actions of the **Electronic reporting export message** type.</span></span>
- <span data-ttu-id="bd46b-364">**发送报表** – 此按钮与 **Web 服务**类型的操作关联。</span><span class="sxs-lookup"><span data-stu-id="bd46b-364">**Send report** – This button is associated with actions of the **Web service** type.</span></span>
- <span data-ttu-id="bd46b-365">**更新状态** – 此按钮与**消息级别用户处理**类型的操作关联。</span><span class="sxs-lookup"><span data-stu-id="bd46b-365">**Update status** – This button is associated with actions of the **Message level user processing** type.</span></span>
- <span data-ttu-id="bd46b-366">**消息项** – 打开**电子消息项**页。</span><span class="sxs-lookup"><span data-stu-id="bd46b-366">**Message items** – Open the **Electronic message items** page.</span></span>

<span data-ttu-id="bd46b-367">**操作日志**快速选项卡显示有关为所选消息运行的所有操作的信息。</span><span class="sxs-lookup"><span data-stu-id="bd46b-367">The **Action log** FastTab shows information about all the actions that have been run for the selected message.</span></span>

<span data-ttu-id="bd46b-368">**消息附加字段**快速选项卡显示为处理设置中的消息定义的所有附加字段。</span><span class="sxs-lookup"><span data-stu-id="bd46b-368">The **Message additional fields** FastTab shows all the additional fields that are defined for messages in the processing setup.</span></span> <span data-ttu-id="bd46b-369">它还显示这些附加字段的值。</span><span class="sxs-lookup"><span data-stu-id="bd46b-369">It also shows the values of those additional fields.</span></span>

<span data-ttu-id="bd46b-370">**消息项**快速选项卡显示与所选消息相关的所有消息项。</span><span class="sxs-lookup"><span data-stu-id="bd46b-370">The **Message items** FastTab shows all the message items that are related to the selected message.</span></span>

<span data-ttu-id="bd46b-371">您可以查看所选消息的所有附件。</span><span class="sxs-lookup"><span data-stu-id="bd46b-371">You can review all the attachments for the selected message.</span></span> <span data-ttu-id="bd46b-372">这些附件是已生成并接收的报表。</span><span class="sxs-lookup"><span data-stu-id="bd46b-372">These attachments are reports that have already been generated and received.</span></span> <span data-ttu-id="bd46b-373">选择要查看其附件的消息，然后选择操作窗格上的**附件**按钮。</span><span class="sxs-lookup"><span data-stu-id="bd46b-373">Select the message to review attachments for, and then select the **Attachment** button on the Action Pane.</span></span>

![“附件”按钮](media/attachment-icon.png)

<span data-ttu-id="bd46b-375">**附件**页显示与消息相关的所有附件。</span><span class="sxs-lookup"><span data-stu-id="bd46b-375">The **Attachments** page shows all the attachments that are related to the message.</span></span> <span data-ttu-id="bd46b-376">若要查看文件，请在左侧列表中选择它，然后选择操作窗格上的**打开**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-376">To view a file, select it in the list on the left, and then select **Open** on the Action Pane.</span></span>

![“打开”按钮](media/open-button.png)

<span data-ttu-id="bd46b-378">若要查看与以前为消息运行的特定操作相关的附件，请选择**电子消息**页上的消息，然后，在**操作日志**快速选项卡上，选择该操作。</span><span class="sxs-lookup"><span data-stu-id="bd46b-378">To review an attachment that is related to a specific action that was previously run for a message, select the message on the **Electronic messages** page, and then, on **Action log** FastTab, select the action.</span></span> <span data-ttu-id="bd46b-379">然后选择操作窗格上的**附件**按钮。</span><span class="sxs-lookup"><span data-stu-id="bd46b-379">Then select the **Attachment** button on the Action Pane.</span></span>

<span data-ttu-id="bd46b-380">您还可以通过选择操作窗格上的**运行处理**运行整个处理或特定操作。</span><span class="sxs-lookup"><span data-stu-id="bd46b-380">You can also run either the whole processing or just a specific action by selecting **Run processing** on the Action Pane.</span></span>

### <a name="electronic-message-items"></a><span data-ttu-id="bd46b-381">电子消息项</span><span class="sxs-lookup"><span data-stu-id="bd46b-381">Electronic message items</span></span>

<span data-ttu-id="bd46b-382">**电子消息项**页显示所有消息项，以及为每个消息项运行的操作的日志。</span><span class="sxs-lookup"><span data-stu-id="bd46b-382">The **Electronic message items** page presents all message items and a log of the actions that have been run for each message item.</span></span> <span data-ttu-id="bd46b-383">它还显示为消息项定义的附加字段，以及这些附加字段的值。</span><span class="sxs-lookup"><span data-stu-id="bd46b-383">It also shows the additional fields that are defined for the message items, and the values of those additional fields.</span></span>

<span data-ttu-id="bd46b-384">下表描述**消息项**选项卡的字段。</span><span class="sxs-lookup"><span data-stu-id="bd46b-384">The following table describes the fields on the **Message items** tab.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bd46b-385">字段</span><span class="sxs-lookup"><span data-stu-id="bd46b-385">Field</span></span></th>
<th><span data-ttu-id="bd46b-386">说明</span><span class="sxs-lookup"><span data-stu-id="bd46b-386">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd46b-387">处理中</span><span class="sxs-lookup"><span data-stu-id="bd46b-387">Processing</span></span></td>
<td><span data-ttu-id="bd46b-388">用于创建消息项的处理的名称。</span><span class="sxs-lookup"><span data-stu-id="bd46b-388">The name of the processing that was used to create the message item.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd46b-389">消息项</span><span class="sxs-lookup"><span data-stu-id="bd46b-389">Message item</span></span></td>
<td><span data-ttu-id="bd46b-390">消息项的 ID。</span><span class="sxs-lookup"><span data-stu-id="bd46b-390">The ID of the message item.</span></span> <span data-ttu-id="bd46b-391">此 ID 基于在<strong>总帐参数</strong>页定义的<strong>消息项</strong>编号规则自动分配。</span><span class="sxs-lookup"><span data-stu-id="bd46b-391">This ID is assigned automatically, based on the <strong>Message item</strong> number sequence that is defined on the <strong>General ledger parameters</strong> page.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd46b-392">消息项日期</span><span class="sxs-lookup"><span data-stu-id="bd46b-392">Message item date</span></span></td>
<td><span data-ttu-id="bd46b-393">创建消息项的日期。</span><span class="sxs-lookup"><span data-stu-id="bd46b-393">The date when the message item was created.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd46b-394">消息项类型</span><span class="sxs-lookup"><span data-stu-id="bd46b-394">Message item type</span></span></td>
<td><span data-ttu-id="bd46b-395">消息项的类型。</span><span class="sxs-lookup"><span data-stu-id="bd46b-395">The type of message item.</span></span> <span data-ttu-id="bd46b-396">可以为同一个处理设置多个消息项类型（例如，<strong>传入发票</strong>和<strong>传出发票</strong>）。</span><span class="sxs-lookup"><span data-stu-id="bd46b-396">Several types of messages items can be set up for the same processing (for example, <strong>Incoming invoices</strong> and <strong>Outgoing invoices</strong>).</span></span> <span data-ttu-id="bd46b-397">只有当发票被添加到消息项表时，此字段才会自动填充。</span><span class="sxs-lookup"><span data-stu-id="bd46b-397">This field can be filled in automatically only when an invoice is added to the Message items table.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd46b-398">消息项状态</span><span class="sxs-lookup"><span data-stu-id="bd46b-398">Message item status</span></span></td>
<td><span data-ttu-id="bd46b-399">消息项的实际状态。</span><span class="sxs-lookup"><span data-stu-id="bd46b-399">The actual status of the message item.</span></span> <span data-ttu-id="bd46b-400">可用状态随消息项类型而变化。</span><span class="sxs-lookup"><span data-stu-id="bd46b-400">The available statuses vary, depending on the type of message item.</span></span> <span data-ttu-id="bd46b-401">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="bd46b-401">Here are some examples:</span></span>
<ul>
<li><span data-ttu-id="bd46b-402"><strong>已填充</strong> – 记录已添加到消息项表中。</span><span class="sxs-lookup"><span data-stu-id="bd46b-402"><strong>Populated</strong> – A record was added to the Message items table.</span></span></li>
<li><span data-ttu-id="bd46b-403"><strong>已评估</strong> – 已为消息项计算其他属性。</span><span class="sxs-lookup"><span data-stu-id="bd46b-403"><strong>Evaluated</strong> – Additional attributes were calculated for the message item.</span></span></li>
<li><span data-ttu-id="bd46b-404"><strong>已报告</strong> – 消息项已成功添加到报表中。</span><span class="sxs-lookup"><span data-stu-id="bd46b-404"><strong>Reported</strong> – The message item was successfully added to a report.</span></span></li>
<li><span data-ttu-id="bd46b-405"><strong>已排除</strong> – 如果您必须在导出报表前从报表中排除一些消息项，此状态可能有用。</span><span class="sxs-lookup"><span data-stu-id="bd46b-405"><strong>Excluded</strong> – This status can be useful if you must exclude some message items from a report before it's exported.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="bd46b-406">传输日期</span><span class="sxs-lookup"><span data-stu-id="bd46b-406">Transmission date</span></span></td>
<td><span data-ttu-id="bd46b-407">对于在系统外自动传输生成的报表的处理，为传输消息项的日期。</span><span class="sxs-lookup"><span data-stu-id="bd46b-407">For processing that automatically transmits a generated report outside the system, the date when the message item was transmitted.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd46b-408">文档编号</span><span class="sxs-lookup"><span data-stu-id="bd46b-408">Document number</span></span></td>
<td><span data-ttu-id="bd46b-409">此字段基于填充记录操作的设置自动填充。</span><span class="sxs-lookup"><span data-stu-id="bd46b-409">This field is filled in automatically, based on the setup of the populate records action.</span></span> <span data-ttu-id="bd46b-410">只有当发票被添加到消息项表时，此字段才会自动填充。</span><span class="sxs-lookup"><span data-stu-id="bd46b-410">This field can be filled in automatically only when an invoice is added to the Message items table.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd46b-411">帐号</span><span class="sxs-lookup"><span data-stu-id="bd46b-411">Account number</span></span></td>
<td><span data-ttu-id="bd46b-412">客户或供应商的帐号（或其他字段值，根据在<strong>填充记录</strong>操作上定义的字段）。</span><span class="sxs-lookup"><span data-stu-id="bd46b-412">The account number of a customer or vendor (or another field value, depending on the field that is defined on the <strong>Populate records</strong> action).</span></span> <span data-ttu-id="bd46b-413">只有当发票被添加到消息项表时，此字段才会自动填充。</span><span class="sxs-lookup"><span data-stu-id="bd46b-413">This field can be filled in automatically only when an invoice is added to the Message items table.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd46b-414">消息</span><span class="sxs-lookup"><span data-stu-id="bd46b-414">Message</span></span></td>
<td><span data-ttu-id="bd46b-415">消息的编号。</span><span class="sxs-lookup"><span data-stu-id="bd46b-415">The number of the message.</span></span> <span data-ttu-id="bd46b-416">此编号基于在<strong>总帐参数</strong>页定义的<strong>消息</strong>编号规则自动分配。</span><span class="sxs-lookup"><span data-stu-id="bd46b-416">This number is assigned automatically, based on the <strong>Message</strong> number sequence that is defined on the <strong>General ledger parameters</strong> page.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd46b-417">消息状态</span><span class="sxs-lookup"><span data-stu-id="bd46b-417">Message status</span></span></td>
<td><span data-ttu-id="bd46b-418">电子消息的实际状态。</span><span class="sxs-lookup"><span data-stu-id="bd46b-418">The actual status of the electronic message.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd46b-419">后续操作</span><span class="sxs-lookup"><span data-stu-id="bd46b-419">Next action</span></span></td>
<td><span data-ttu-id="bd46b-420">可以为消息项的当前状态启动的下一个操作。</span><span class="sxs-lookup"><span data-stu-id="bd46b-420">The next actions that can be initiated for the current status of the message item.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd46b-421">**附加字段**选项卡显示所选消息项的附加字段及其值。</span><span class="sxs-lookup"><span data-stu-id="bd46b-421">The **Additional fields** tab shows the additional fields for the selected message item, and their values.</span></span>

#### <a name="run-processing"></a><span data-ttu-id="bd46b-422">运行处理</span><span class="sxs-lookup"><span data-stu-id="bd46b-422">Run processing</span></span>

<span data-ttu-id="bd46b-423">选择操作窗格上的**运行处理**运行消息项的处理。</span><span class="sxs-lookup"><span data-stu-id="bd46b-423">Select **Run processing** on the Action Pane to run the processing for message items.</span></span> <span data-ttu-id="bd46b-424">若要运行特定操作，在**运行处理**对话框中，将**选择操作**选项设置为**是**，然后选择操作。</span><span class="sxs-lookup"><span data-stu-id="bd46b-424">To run a specific action, in the **Run processing** dialog box, set the **Select action** option to **Yes**, and then select an action.</span></span> <span data-ttu-id="bd46b-425">若要运行整个处理，则将**选择操作**选项保留为**否**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-425">To run the whole processing, leave the **Select action** option set to **No**.</span></span>

#### <a name="generate-report"></a><span data-ttu-id="bd46b-426">生成报表</span><span class="sxs-lookup"><span data-stu-id="bd46b-426">Generate report</span></span>

<span data-ttu-id="bd46b-427">选择操作窗格上的**生成报表**生成报表。</span><span class="sxs-lookup"><span data-stu-id="bd46b-427">Select **Generate report** on the Action Pane to generate a report.</span></span> <span data-ttu-id="bd46b-428">此按钮与**电子报告导出**类型的操作关联。</span><span class="sxs-lookup"><span data-stu-id="bd46b-428">This button is associated with actions of the **Electronic reporting export** type.</span></span>

#### <a name="update-status"></a><span data-ttu-id="bd46b-429">更新状态</span><span class="sxs-lookup"><span data-stu-id="bd46b-429">Update status</span></span>

<span data-ttu-id="bd46b-430">选择操作窗格上的**更新状态**更新一个或多个消息项的状态。</span><span class="sxs-lookup"><span data-stu-id="bd46b-430">Select **Update status** on the Action Pane to update the status of one or more message items.</span></span> <span data-ttu-id="bd46b-431">在**更新状态**对话框中，使用**要包括的记录**快速选项卡选择要更新的消息项。</span><span class="sxs-lookup"><span data-stu-id="bd46b-431">In the **Update status** dialog box, use the **Records to include** FastTab to select message items for update.</span></span> <span data-ttu-id="bd46b-432">请确保正确定义选择条件，因为消息项状态将根据这些条件、所选操作的初始状态以及您设置的**新状态**更新。</span><span class="sxs-lookup"><span data-stu-id="bd46b-432">Make sure that you correctly define the selection criteria, because message item statuses will be updated according to these criteria, the initial status of the selected action, and the **New status** value that you set.</span></span> <span data-ttu-id="bd46b-433">在完成状态更新后，将很难确定更新了哪些项目。</span><span class="sxs-lookup"><span data-stu-id="bd46b-433">After a status update is completed, it will be difficult to determine which items were just updated.</span></span> <span data-ttu-id="bd46b-434">因此将很难回滚状态更新。</span><span class="sxs-lookup"><span data-stu-id="bd46b-434">Therefore, it will be difficult to roll back status updates.</span></span>

#### <a name="electronic-messages"></a><span data-ttu-id="bd46b-435">电子消息</span><span class="sxs-lookup"><span data-stu-id="bd46b-435">Electronic messages</span></span>

<span data-ttu-id="bd46b-436">选择操作窗格上的**电子消息**查看与所选消息项相关的电子消息。</span><span class="sxs-lookup"><span data-stu-id="bd46b-436">Select **Electronic message** on the Action Pane to review an electronic message that is related to the selected message item.</span></span>

<span data-ttu-id="bd46b-437">您还可以查看与该消息项对应的所有文件。</span><span class="sxs-lookup"><span data-stu-id="bd46b-437">You can also review all the files that correspond to the message item.</span></span> <span data-ttu-id="bd46b-438">选择消息项的**消息**字段，或选择操作窗格上的**电子消息**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-438">Select the **Message** field of the message item, or select **Electronic message** on the Action Pane.</span></span> <span data-ttu-id="bd46b-439">在**电子消息**页，选择要查看其报表的消息，然后选择操作窗格上的**附件**按钮。</span><span class="sxs-lookup"><span data-stu-id="bd46b-439">On the **Electronic message** page, select the message to review a report for, and then select the **Attachment** button on the Action Pane.</span></span>

![“附件”按钮](media/attachment-icon.png)

<span data-ttu-id="bd46b-441">**附件**页显示与消息相关的所有附件。</span><span class="sxs-lookup"><span data-stu-id="bd46b-441">The **Attachments** page shows all the attachments that are related to the message.</span></span> <span data-ttu-id="bd46b-442">若要查看文件，请在左侧列表中选择它，然后选择操作窗格上的**打开**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-442">To view a file, select it in the list on the left, and then select **Open** on the Action Pane.</span></span>

![“打开”按钮](media/open-button.png)

#### <a name="original-document"></a><span data-ttu-id="bd46b-444">原始凭证</span><span class="sxs-lookup"><span data-stu-id="bd46b-444">Original document</span></span>

<span data-ttu-id="bd46b-445">选择操作窗格上的**原始单据**打开所选消息项的原始单据。</span><span class="sxs-lookup"><span data-stu-id="bd46b-445">Select **Original document** on the Action Pane to open the original document for the selected message item.</span></span>

## <a name="example"></a><span data-ttu-id="bd46b-446">示例</span><span class="sxs-lookup"><span data-stu-id="bd46b-446">Example</span></span>

<span data-ttu-id="bd46b-447">在创建您的 ER 格式后，将其映射到数据源，然后完成它，您可以使用**电子报告**工作区来运行它。</span><span class="sxs-lookup"><span data-stu-id="bd46b-447">After you've created your ER format, mapped it to data sources, and completed it, you can run it by using the **Electronic reporting** workspace.</span></span> <span data-ttu-id="bd46b-448">生成一个可以保存在本地的报表。</span><span class="sxs-lookup"><span data-stu-id="bd46b-448">A report is generated that you can save locally.</span></span>

<span data-ttu-id="bd46b-449">若要控制报告流程的以下方面，必须设置电子消息处理：</span><span class="sxs-lookup"><span data-stu-id="bd46b-449">To control the following aspects of the reporting process, you must set up electronic messaging processing:</span></span>

- <span data-ttu-id="bd46b-450">记录有关生成报表人员的信息。</span><span class="sxs-lookup"><span data-stu-id="bd46b-450">Log information about who generated the report.</span></span>
- <span data-ttu-id="bd46b-451">记录报表生成时间。</span><span class="sxs-lookup"><span data-stu-id="bd46b-451">Log when the report was generated.</span></span>
- <span data-ttu-id="bd46b-452">保存为以前期间生成的报表。</span><span class="sxs-lookup"><span data-stu-id="bd46b-452">Save the reports that were generated for previous periods.</span></span>

<span data-ttu-id="bd46b-453">本部分提供显示如何设置电子消息功能来建立报告流程的示例。</span><span class="sxs-lookup"><span data-stu-id="bd46b-453">This section provides an example that shows how you might set up the Electronic messages functionality to build a reporting process.</span></span>

### <a name="set-up-and-run-processing-to-call-a-simple-er-exporting-format-to-generate-an-excel-report"></a><span data-ttu-id="bd46b-454">设置并运行处理以调用简单的 ER 导出格式来生成 Excel 报表</span><span class="sxs-lookup"><span data-stu-id="bd46b-454">Set up and run processing to call a simple ER exporting format to generate an Excel report</span></span>

<span data-ttu-id="bd46b-455">本部分提供显示如何设置电子消息以基于 Excel 的导出 ER 格式生成报表的示例。</span><span class="sxs-lookup"><span data-stu-id="bd46b-455">This section provides an example that shows how you can set up electronic messaging to generate a report that is based on an exporting ER format for Excel.</span></span> <span data-ttu-id="bd46b-456">要按此示例操作，必须已经创建了 ER Excel 导出格式，并映射到数据源并且完成。</span><span class="sxs-lookup"><span data-stu-id="bd46b-456">To follow this example, the ER Excel exporting format must already be created, mapped to data sources, and completed.</span></span> <span data-ttu-id="bd46b-457">必须为电子消息设置了编号规则。</span><span class="sxs-lookup"><span data-stu-id="bd46b-457">A number sequence must already be set up for electronic messages.</span></span>

<span data-ttu-id="bd46b-458">在您创建处理时，如果您首先定义将设置的处理操作和状态将会很有用。</span><span class="sxs-lookup"><span data-stu-id="bd46b-458">When you build processing, it's helpful if you first define the processing actions and statuses that will be set up.</span></span> <span data-ttu-id="bd46b-459">下图显示此示例的处理看起来如何。</span><span class="sxs-lookup"><span data-stu-id="bd46b-459">The following illustration shows what the processing looks like for this example.</span></span>

![处理方案](media/processing-scheme.png)

#### <a name="create-message-statuses"></a><span data-ttu-id="bd46b-461">创建消息状态</span><span class="sxs-lookup"><span data-stu-id="bd46b-461">Create message statuses</span></span>

1. <span data-ttu-id="bd46b-462">转到**税 \> 设置 \> 电子消息 \> 消息状态**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-462">Go to **Tax \> Setup \> Electronic messages \> Message statuses**.</span></span>
2. <span data-ttu-id="bd46b-463">创建以下消息状态：</span><span class="sxs-lookup"><span data-stu-id="bd46b-463">Create the following message statuses:</span></span>

    - <span data-ttu-id="bd46b-464">新建</span><span class="sxs-lookup"><span data-stu-id="bd46b-464">New</span></span>
    - <span data-ttu-id="bd46b-465">已准备</span><span class="sxs-lookup"><span data-stu-id="bd46b-465">Prepared</span></span>
    - <span data-ttu-id="bd46b-466">已生成</span><span class="sxs-lookup"><span data-stu-id="bd46b-466">Generated</span></span>

    ![消息状态](media/message-statuses.png)

3. <span data-ttu-id="bd46b-468">在**新**状态的行中，选择**允许删除**复选框以让用户可以删除此状态的消息。</span><span class="sxs-lookup"><span data-stu-id="bd46b-468">On the line for the **New** status, select the **Allow delete** check box to let users delete messages that have this status.</span></span>

#### <a name="create-additional-fields"></a><span data-ttu-id="bd46b-469">创建附加字段</span><span class="sxs-lookup"><span data-stu-id="bd46b-469">Create additional fields</span></span>

1. <span data-ttu-id="bd46b-470">转到**税 \> 设置 \> 电子消息 \> 附加字段**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-470">Go to **Tax \> Setup \> Electronic messages \> Additional fields**.</span></span>
2. <span data-ttu-id="bd46b-471">添加附加字段及其值。</span><span class="sxs-lookup"><span data-stu-id="bd46b-471">Add an additional field and its values.</span></span> <span data-ttu-id="bd46b-472">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="bd46b-472">Here is an example.</span></span>

    ![附加字段](media/additional-fields.png)

3. <span data-ttu-id="bd46b-474">将**用户编辑**选项设置为**是**以允许用户编辑此字段。</span><span class="sxs-lookup"><span data-stu-id="bd46b-474">Set the **User edit** option to **Yes** to let users edit the field.</span></span>

#### <a name="create-message-processing-actions"></a><span data-ttu-id="bd46b-475">创建消息处理操作</span><span class="sxs-lookup"><span data-stu-id="bd46b-475">Create message processing actions</span></span>

<span data-ttu-id="bd46b-476">对于本例，将创建以下操作：</span><span class="sxs-lookup"><span data-stu-id="bd46b-476">For this example, you will create the following actions:</span></span>

- <span data-ttu-id="bd46b-477">**创建消息**</span><span class="sxs-lookup"><span data-stu-id="bd46b-477">**Create message**</span></span>
- <span data-ttu-id="bd46b-478">**更新为已准备**</span><span class="sxs-lookup"><span data-stu-id="bd46b-478">**Update to Prepared**</span></span>
- <span data-ttu-id="bd46b-479">**生成报表**</span><span class="sxs-lookup"><span data-stu-id="bd46b-479">**Generate report**</span></span>
- <span data-ttu-id="bd46b-480">**更新为初始状态**（可选）</span><span class="sxs-lookup"><span data-stu-id="bd46b-480">**Update to initial status** (optional)</span></span>

1. <span data-ttu-id="bd46b-481">转到**税 \> 设置 \> 电子消息 \> 消息处理操作**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-481">Go to **Tax \> Setup \> Electronic messages \> Message processing actions**.</span></span>
2. <span data-ttu-id="bd46b-482">创建名为**创建消息**的操作。</span><span class="sxs-lookup"><span data-stu-id="bd46b-482">Create an action that is named **Create message**.</span></span> <span data-ttu-id="bd46b-483">在**常规**快速选项卡上，在**操作类型**字段中，选择**创建消息**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-483">On the **General** FastTab, in the **Action type** field, select **Create message**.</span></span>
3. <span data-ttu-id="bd46b-484">创建名为**更新为已准备**的操作，然后设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="bd46b-484">Create an action that is named **Update to Prepared**, and set the following fields:</span></span>

    - <span data-ttu-id="bd46b-485">在**常规**快速选项卡上，在**操作类型**字段中，选择**消息级别用户处理**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-485">On the **General** FastTab, in the **Action type** field, select **Message level user processing**.</span></span>
    - <span data-ttu-id="bd46b-486">在**初始状态**快速选项卡上，在**消息状态**字段中，选择**新**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-486">On the **Initial statuses** FastTab, in the **Message status** field, select **New**.</span></span>
    - <span data-ttu-id="bd46b-487">在**结果状态**快速选项卡上，在**消息状态**字段中，选择**已准备**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-487">On the **Result statuses** FastTab, in the **Message status** field, select **Prepared**.</span></span> <span data-ttu-id="bd46b-488">在**响应类型**字段中，输入**已成功执行**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-488">In the **Response type** field, enter **Successfully executed**.</span></span>

4. <span data-ttu-id="bd46b-489">创建名为**生成报表**的操作，然后设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="bd46b-489">Create an action that is named **Generate report**, and set the following fields:</span></span>

    - <span data-ttu-id="bd46b-490">在**常规**快速选项卡上，在**操作类型**字段中，选择**电子报告导出**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-490">On the **General** FastTab, in the **Action type** field, select **Electronic reporting export**.</span></span> <span data-ttu-id="bd46b-491">在**格式映射**字段中，选择导出 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="bd46b-491">In the **Format mapping** field, select the exporting ER format.</span></span> <span data-ttu-id="bd46b-492">选项有 **Excel**、**XML**、**JSON**、**文本**和**其他**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-492">The options are **Excel**, **XML**, **JSON**, **Text**, and **Other**.</span></span>
    - <span data-ttu-id="bd46b-493">在**初始状态**快速选项卡上，在**消息状态**字段中，选择**已准备**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-493">On the **Initial statuses** FastTab, in the **Message status** field, select **Prepared**.</span></span>
    - <span data-ttu-id="bd46b-494">在**结果状态**快速选项卡上，在**消息状态**字段中，选择**已生成**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-494">On the **Result statuses** FastTab, in the **Message status** field, select **Generated**.</span></span> <span data-ttu-id="bd46b-495">在**响应类型**字段中，输入**已成功执行**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-495">In the **Response type** field, enter **Successfully executed**.</span></span>

    ![生成报表操作](media/generate-report-action.png)

5. <span data-ttu-id="bd46b-497">可选：若要使用户能够多次重新生成报表，您可以创建**更新为初始状态**操作并设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="bd46b-497">Optional: To let users regenerate a report several times, you can create an **Update to initial status** action and set the following fields:</span></span>

    - <span data-ttu-id="bd46b-498">在**常规**快速选项卡上，在**操作类型**字段中，选择**消息级别用户处理**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-498">On the **General** FastTab, in the **Action type** field, select **Message level user processing**.</span></span>
    - <span data-ttu-id="bd46b-499">在**初始状态**快速选项卡上，在**消息状态**字段中，选择**已生成**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-499">On the **Initial statuses** FastTab, in the **Message status** field, select **Generated**.</span></span>
    - <span data-ttu-id="bd46b-500">在**结果状态**快速选项卡上，在**消息状态**字段中，选择**已准备**或（和）**新**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-500">On the **Result statuses** FastTab, in the **Message status** field, select **Prepared** or (and) **New**.</span></span> <span data-ttu-id="bd46b-501">在**响应类型**字段中，输入**已成功执行**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-501">In the **Response type** field, enter **Successfully executed**.</span></span>

#### <a name="electronic-message-processing"></a><span data-ttu-id="bd46b-502">电子消息处理</span><span class="sxs-lookup"><span data-stu-id="bd46b-502">Electronic message processing</span></span>

<span data-ttu-id="bd46b-503">在此示例中，应设置所有操作，以便其单独运行。</span><span class="sxs-lookup"><span data-stu-id="bd46b-503">In this example, all the actions should be set up so that they run separately.</span></span> <span data-ttu-id="bd46b-504">假定每个操作都将由用户初始化。</span><span class="sxs-lookup"><span data-stu-id="bd46b-504">The assumption is that every action will be initialized by the user.</span></span>

1. <span data-ttu-id="bd46b-505">转到**税 \> 设置 \> 电子消息 \> 电子消息处理**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-505">Go to **Tax \> Setup \> Electronic messages \> Electronic message processing**.</span></span>
2. <span data-ttu-id="bd46b-506">为您的处理添加记录，添加所有先前定义的操作和附加字段。</span><span class="sxs-lookup"><span data-stu-id="bd46b-506">Add a record for your processing, and add all previously defined actions and an additional field.</span></span>
3. <span data-ttu-id="bd46b-507">可选：在**安全角色**快速选项卡上，为您的处理定义安全角色以限制对特定报告的访问。</span><span class="sxs-lookup"><span data-stu-id="bd46b-507">Optional: On the **Security roles** FastTab, define security roles for your processing to restrict access to specific reporting.</span></span>
4. <span data-ttu-id="bd46b-508">转到**税 \> 查询和报表 \> 电子消息 \> 电子消息**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-508">Go to **Tax \> Inquires and reports \> Electronic messages \> Electronic messages**.</span></span>
5. <span data-ttu-id="bd46b-509">选择**新建**创建消息。</span><span class="sxs-lookup"><span data-stu-id="bd46b-509">Select **New** to create a message.</span></span> <span data-ttu-id="bd46b-510">此时，您可以添加日期和描述。</span><span class="sxs-lookup"><span data-stu-id="bd46b-510">At this point, you can add dates and a description.</span></span> <span data-ttu-id="bd46b-511">您还可以根据需要更新附加字段的值。</span><span class="sxs-lookup"><span data-stu-id="bd46b-511">You can also update the value of the additional field as you require.</span></span>

    ![创建电子消息](media/create-electronic-message.png)

<span data-ttu-id="bd46b-513">**操作日志**快速选项卡上的网格将自动填充为对消息执行的所有操作的日志。</span><span class="sxs-lookup"><span data-stu-id="bd46b-513">The grid on the **Action log** FastTab is automatically filled in with a log of all actions that are performed on the message.</span></span>

<span data-ttu-id="bd46b-514">您现在可以删除或更新消息状态。</span><span class="sxs-lookup"><span data-stu-id="bd46b-514">You can now either delete or update the message status.</span></span> <span data-ttu-id="bd46b-515">若要更新消息状态，选择**更新状态**，然后在**新状态**字段中，选择**已准备**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-515">To update the message status, select **Update status**, and then, in the **New status** field, select **Prepared**.</span></span> <span data-ttu-id="bd46b-516">然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="bd46b-516">Then select **OK**.</span></span>

![更新消息状态](media/update-status.png)

<span data-ttu-id="bd46b-518">消息状态更新为**已准备**，现在，您可以通过选择**生成报表**生成报表。</span><span class="sxs-lookup"><span data-stu-id="bd46b-518">The message status is updated to **Prepared**, and you can now generate the report by selecting **Generate report**.</span></span> <span data-ttu-id="bd46b-519">将生成报表，消息状态和操作日志将更新。</span><span class="sxs-lookup"><span data-stu-id="bd46b-519">The report is generated, and the message status and action log are updated.</span></span> <span data-ttu-id="bd46b-520">若要查看生成的报表，请选择操作窗格上的**附件**按钮。</span><span class="sxs-lookup"><span data-stu-id="bd46b-520">To view the generated report, select the **Attachment** button on the Action Pane.</span></span>
