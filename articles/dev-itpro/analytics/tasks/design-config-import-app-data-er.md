--- 
title: "设计配置以分析应用程序数据更新的传入单据 (ER)"
description: "此过程显示如何设计电子报告 (ER) 配置以分析传入电子单据。"
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: bb8477eba19b536c77296f235fc93280b9982518
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---
# <a name="design-configurations-to-parse-incoming-documents-for-application-data-updates-er"></a><span data-ttu-id="42459-103">设计配置以分析应用程序数据更新的传入单据 (ER)</span><span class="sxs-lookup"><span data-stu-id="42459-103">Design configurations to parse incoming documents for application data updates (ER)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="42459-104">此过程显示如何设计电子报告 (ER) 配置以分析传入电子单据。</span><span class="sxs-lookup"><span data-stu-id="42459-104">This procedure shows how to design Electronic reporting (ER) configurations to parse an incoming electronic document.</span></span> <span data-ttu-id="42459-105">在此过程中，将导入已为示例公司 Litware 公司创建的所需 ER 配置，并用于分析传入的电子单据。</span><span class="sxs-lookup"><span data-stu-id="42459-105">In this procedure, you will import the required ER configurations that have been created for the sample company, Litware, Inc. and use them for parsing incoming electronic documents.</span></span> <span data-ttu-id="42459-106">为了完成此过程中的步骤，您必须首先完成“ER 创建配置提供商并标记为有效”这一过程。</span><span class="sxs-lookup"><span data-stu-id="42459-106">To complete the steps in this procedure, you must first complete the procedure, “ER Create a configuration provider and mark it as active.”</span></span>

<span data-ttu-id="42459-107">此过程是为向其分配了系统管理员角色或电子申报开发人员角色的用户创建的。</span><span class="sxs-lookup"><span data-stu-id="42459-107">This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> 

<span data-ttu-id="42459-108">可使用任何数据集完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="42459-108">These steps can be completed using any dataset.</span></span> <span data-ttu-id="42459-109">首先，下载并保存主题“分析传入单据以更新应用程序数据”(https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/parse-incoming-electronic-documents) 中列出的文件。</span><span class="sxs-lookup"><span data-stu-id="42459-109">Before you begin, download and save the files listed in the topic, “Parse incoming documents to update application data” (https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/parse-incoming-electronic-documents).</span></span> <span data-ttu-id="42459-110">文件为：EFSTA model.xml、EFSTA format.xml、Response1.xml、Response2.xml、Response3.xml、Response4.xml。</span><span class="sxs-lookup"><span data-stu-id="42459-110">The files are: EFSTA model.xml, EFSTA format.xml, Response1.xml, Response2.xml, Response3.xml, Response4.xml.</span></span>

1. <span data-ttu-id="42459-111">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="42459-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="42459-112">确保示例公司 Litware 公司的配置提供程序可用且标记为“有效”。</span><span class="sxs-lookup"><span data-stu-id="42459-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="42459-113">如果没有看到此配置提供程序，请首先完成“创建配置提供程序并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="42459-113">If you don’t see this configuration provider, complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>  
2. <span data-ttu-id="42459-114">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="42459-114">Click Reporting configurations.</span></span>
    * <span data-ttu-id="42459-115">以下方案将用于显示分析 XML 格式传入电子文档的功能：ERP 应用程序 (Dynamics 365 for Finance and Operations) 从 Web 服务（如 http://efsta.org/ EFSTA fiscal service）请求数据并分析传入的响应以相应地更新应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="42459-115">The following scenario will be used to show the capabilities of parsing incoming electronic documents in XML format: ERP application (Dynamics 365 for Finance and Operations)  requests data from the web service (such as http://efsta.org/ EFSTA fiscal service) and parses the incoming responses to update application data accordingly.</span></span> <span data-ttu-id="42459-116">为实现最有效的分析方式，使用单个 ER 格式，尽管预期的 XML 格式的传入文档具有不同结构。</span><span class="sxs-lookup"><span data-stu-id="42459-116">For the most efficient way to parse, a single ER format is used despite the different structure of expected incoming documents in XML format.</span></span>   

## <a name="import-and-review-er-configurations"></a><span data-ttu-id="42459-117">导入和查看 ER 配置</span><span class="sxs-lookup"><span data-stu-id="42459-117">Import and review ER configurations</span></span>
<span data-ttu-id="42459-118">导入包含专门用于存储传入文件详细信息的示例数据模型的 ER 模型配置。</span><span class="sxs-lookup"><span data-stu-id="42459-118">Import the ER model configuration that contains the sample data model designed to store the details of the incoming file.</span></span>  
1. <span data-ttu-id="42459-119">单击“交换”。</span><span class="sxs-lookup"><span data-stu-id="42459-119">Click Exchange.</span></span>
2. <span data-ttu-id="42459-120">单击“从 XML 文件加载”。</span><span class="sxs-lookup"><span data-stu-id="42459-120">Click Load from XML file.</span></span>
    * <span data-ttu-id="42459-121">单击“浏览”并选择 EFSTA model.xml 文件。</span><span class="sxs-lookup"><span data-stu-id="42459-121">Click Browse and select the EFSTA model.xml file.</span></span>  
3. <span data-ttu-id="42459-122">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="42459-122">Click OK.</span></span>
4. <span data-ttu-id="42459-123">在树结构中，选择“EFSTA 模型”。</span><span class="sxs-lookup"><span data-stu-id="42459-123">In the tree, select 'EFSTA model'.</span></span>
5. <span data-ttu-id="42459-124">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="42459-124">Click Designer.</span></span>
    * <span data-ttu-id="42459-125">检查所导入数据模型的结构。</span><span class="sxs-lookup"><span data-stu-id="42459-125">Review the structure of the imported data model.</span></span> <span data-ttu-id="42459-126">请注意，enumType 枚举被定义为识别以下服务响应类型：获取有关交易记录提交的确认，获取有关提交的上次交易记录的信息，以及识别不支持的响应类型。</span><span class="sxs-lookup"><span data-stu-id="42459-126">Note that the enumType enumeration is defined to recognize the following types of service responses: to get confirmation about transaction’s submission, to get info about last transaction submitted, and to recognize unsupported response types.</span></span>   
6. <span data-ttu-id="42459-127">在树中，展开“Response”。</span><span class="sxs-lookup"><span data-stu-id="42459-127">In the tree, expand 'Response'.</span></span>
    * <span data-ttu-id="42459-128">请注意，定义根项目“响应”以指定必须从支持的服务响应获取哪类数据来相应地更新应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="42459-128">Note that the root item ‘Response’ is defined to specify what kind of data must be taken from a supported service response to update application data accordingly.</span></span>   
7. <span data-ttu-id="42459-129">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="42459-129">Close the page.</span></span>
    * <span data-ttu-id="42459-130">您将导入 ER 格式配置，其指定如何分析传入文档以在 ER 数据模型中存储数据。</span><span class="sxs-lookup"><span data-stu-id="42459-130">You will import the ER format configuration that specifies how the incoming documents will be parsed to store data in the ER data model.</span></span>   
8. <span data-ttu-id="42459-131">单击“交换”。</span><span class="sxs-lookup"><span data-stu-id="42459-131">Click Exchange.</span></span>
9. <span data-ttu-id="42459-132">单击“从 XML 文件加载”。</span><span class="sxs-lookup"><span data-stu-id="42459-132">Click Load from XML file.</span></span>
    * <span data-ttu-id="42459-133">单击“浏览”并选择 EFSTA format.xml 文件。</span><span class="sxs-lookup"><span data-stu-id="42459-133">Click Browse and select the EFSTA format.xml file.</span></span>  
10. <span data-ttu-id="42459-134">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="42459-134">Click OK.</span></span>
11. <span data-ttu-id="42459-135">在树结构中，展开“EFSTA 模型”。</span><span class="sxs-lookup"><span data-stu-id="42459-135">In the tree, expand 'EFSTA model'.</span></span>
12. <span data-ttu-id="42459-136">在树结构中，选择“EFSTA 模型\EFSTA 格式”。</span><span class="sxs-lookup"><span data-stu-id="42459-136">In the tree, select 'EFSTA model\EFSTA format'.</span></span>
13. <span data-ttu-id="42459-137">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="42459-137">Click Designer.</span></span>
14. <span data-ttu-id="42459-138">单击”展开/折叠“。</span><span class="sxs-lookup"><span data-stu-id="42459-138">Click Expand/collapse.</span></span>
    * <span data-ttu-id="42459-139">请注意，CASE 格式元素被用作根，并包含三个嵌套的 FILE 元素，也就是说，此格式被设计为分析多个格式的传入文件。</span><span class="sxs-lookup"><span data-stu-id="42459-139">Note that the CASE format element is used as the root and contains three nested FILE elements, which means that this format has been designed to parse incoming files of several formats.</span></span>  
15. <span data-ttu-id="42459-140">在树中，选择“Responses\Transaction completion\TraC”。</span><span class="sxs-lookup"><span data-stu-id="42459-140">In the tree, select 'Responses\Transaction completion\TraC'.</span></span>
    * <span data-ttu-id="42459-141">请注意，有关提交的交易记录的响应从“TraC”根元素开始。</span><span class="sxs-lookup"><span data-stu-id="42459-141">Note that the response about the submitted transaction starts from the ‘TraC’ root element.</span></span>   
16. <span data-ttu-id="42459-142">在树中，选择“Responses\Last transaction request\Tra”。</span><span class="sxs-lookup"><span data-stu-id="42459-142">In the tree, select 'Responses\Last transaction request\Tra'.</span></span>
    * <span data-ttu-id="42459-143">请注意，有关上一次提交的交易记录的响应从“Tra”根元素开始。</span><span class="sxs-lookup"><span data-stu-id="42459-143">Note that the response about the last submitted transaction starts from the ‘Tra’ root element.</span></span>   
17. <span data-ttu-id="42459-144">在树中，选择“Responses\Unexpected response\Text”。</span><span class="sxs-lookup"><span data-stu-id="42459-144">In the tree, select 'Responses\Unexpected response\Text'.</span></span>
    * <span data-ttu-id="42459-145">具有嵌套的 TEXT 元素的第三个 FILE 元素已添加，以用于识别不同于上面提到的响应的任何其他响应类型。</span><span class="sxs-lookup"><span data-stu-id="42459-145">The third FILE element with nested TEXT element has been added to recognize any other types of responses that differ from mentioned above.</span></span>   
18. <span data-ttu-id="42459-146">单击”将格式映射到模型“。</span><span class="sxs-lookup"><span data-stu-id="42459-146">Click Map format to model.</span></span>
    * <span data-ttu-id="42459-147">此模型映射包含数据流的定义以使用数据模型的项目存储分析后的传入文档的详细信息。</span><span class="sxs-lookup"><span data-stu-id="42459-147">This model mapping contains the definition of data flow to store details of the parsed incoming document with using the data model’s items.</span></span>  
19. <span data-ttu-id="42459-148">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="42459-148">Click Designer.</span></span>
20. <span data-ttu-id="42459-149">在树中，展开“格式”。</span><span class="sxs-lookup"><span data-stu-id="42459-149">In the tree, expand 'format'.</span></span>
21. <span data-ttu-id="42459-150">在树中，展开“format\Responses: Case(Responses)”。</span><span class="sxs-lookup"><span data-stu-id="42459-150">In the tree, expand 'format\Responses: Case(Responses)'.</span></span>
    * <span data-ttu-id="42459-151">检查“格式”数据源的结构。</span><span class="sxs-lookup"><span data-stu-id="42459-151">Review the structure of the ‘format’ data source.</span></span> <span data-ttu-id="42459-152">请注意，所有三个响应类型均单独提供。</span><span class="sxs-lookup"><span data-stu-id="42459-152">Note that all three response types are offered separately.</span></span>   
22. <span data-ttu-id="42459-153">在树中，选择“format\Responses: Case(Responses)\aType”。</span><span class="sxs-lookup"><span data-stu-id="42459-153">In the tree, select 'format\Responses: Case(Responses)\aType'.</span></span>
    * <span data-ttu-id="42459-154">数据源项目“aType”已添加用以指示响应类型，并绑定到数据模型项目“类型”。</span><span class="sxs-lookup"><span data-stu-id="42459-154">The data source item ‘aType’ has been added to indicate the response type and is bound to the data model item ‘Type’.</span></span>  
23. <span data-ttu-id="42459-155">单击“验证”选项卡。</span><span class="sxs-lookup"><span data-stu-id="42459-155">Click the Validations tab.</span></span>
24. <span data-ttu-id="42459-156">在树中，选择“类型 = format.Responses.aType”。</span><span class="sxs-lookup"><span data-stu-id="42459-156">In the tree, select 'Type = format.Responses.aType'.</span></span>
    * <span data-ttu-id="42459-157">请注意，ER 验证已配置，用以通知用户响应结构与交易记录的提交确认或与上次提交的交易记录的信息不匹配的情况（不支持的响应案例）。</span><span class="sxs-lookup"><span data-stu-id="42459-157">Note that the ER validation has been configured to inform the user about the situation when the response structure does not match the confirmation about transaction’s submission or the information about last transaction submitted (unsupported response case).</span></span>   
25. <span data-ttu-id="42459-158">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="42459-158">Close the page.</span></span>

## <a name="run-model-mapping-of-er-format-configured-for-parsing-incoming-files"></a><span data-ttu-id="42459-159">运行为分析传入文件配置的 ER 格式的模型映射</span><span class="sxs-lookup"><span data-stu-id="42459-159">Run model mapping of ER format configured for parsing incoming files</span></span>
<span data-ttu-id="42459-160">您将为测试运行创建的模型映射，以了解配置的 ER 格式如何分析传入的服务响应。</span><span class="sxs-lookup"><span data-stu-id="42459-160">You will run the created model mapping for testing purposes to see how the configured ER format will parse incoming service responses.</span></span> <span data-ttu-id="42459-161">此步骤使用不同的 XML 文件来模拟不同的 Web 服务响应类型。</span><span class="sxs-lookup"><span data-stu-id="42459-161">This step uses different XML files to simulate different type of web service responses.</span></span>   
1. <span data-ttu-id="42459-162">在 xml 阅读器（如 web 浏览器）中打开 Response1.xml 文件。</span><span class="sxs-lookup"><span data-stu-id="42459-162">Open the Response1.xml file in an xml reader, such as a web browser.</span></span> <span data-ttu-id="42459-163">请注意，此文件包含有关已完成交易的确认详细信息（‘TraC’ 是根元素）。</span><span class="sxs-lookup"><span data-stu-id="42459-163">Note that this file contains confirmation details about the completed transaction (‘TraC’ is the root element).</span></span>   
2. <span data-ttu-id="42459-164">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="42459-164">Click Run.</span></span>
    * <span data-ttu-id="42459-165">单击“浏览”并选择 Response1.xml 文件。</span><span class="sxs-lookup"><span data-stu-id="42459-165">Click Browse and select the Response1.xml file.</span></span>  
3. <span data-ttu-id="42459-166">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="42459-166">Click OK.</span></span>
    * <span data-ttu-id="42459-167">检查生成的输出。</span><span class="sxs-lookup"><span data-stu-id="42459-167">Review the generated output.</span></span> <span data-ttu-id="42459-168">请注意，响应类型已正确识别和分析（ERModelEnumDataSourceHandler#EFSTA model#enumType#C 意味着交易完成案例）。</span><span class="sxs-lookup"><span data-stu-id="42459-168">Note that the response type has been correctly recognized and parsed (ERModelEnumDataSourceHandler#EFSTA model#enumType#C means transaction completion case).</span></span>   
    * <span data-ttu-id="42459-169">在 XML 阅读器中打开 Response2.xml 文件。</span><span class="sxs-lookup"><span data-stu-id="42459-169">Open the Response2.xml file in an XML reader.</span></span> <span data-ttu-id="42459-170">请注意，此文件包含有关上次提交的交易记录的信息（‘Tra’是根元素）。</span><span class="sxs-lookup"><span data-stu-id="42459-170">Note that this file contains information about last transaction submitted (‘Tra’ is the root element).</span></span>   
4. <span data-ttu-id="42459-171">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="42459-171">Click Run.</span></span>
    * <span data-ttu-id="42459-172">单击“浏览”并选择 Response2.xml 文件。</span><span class="sxs-lookup"><span data-stu-id="42459-172">Click Browse and select the Response2.xml file.</span></span>  
5. <span data-ttu-id="42459-173">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="42459-173">Click OK.</span></span>
    * <span data-ttu-id="42459-174">检查生成的输出。</span><span class="sxs-lookup"><span data-stu-id="42459-174">Review the generated output.</span></span> <span data-ttu-id="42459-175">请注意，响应类型已正确识别和分析（ERModelEnumDataSourceHandler#EFSTA model#enumType#R 意味着系统重启案例）。</span><span class="sxs-lookup"><span data-stu-id="42459-175">Note that the response type has been correctly recognized and parsed (ERModelEnumDataSourceHandler#EFSTA model#enumType#R means system restart case).</span></span>   
    * <span data-ttu-id="42459-176">在 XML 阅读器中打开 Response3.xml 文件。</span><span class="sxs-lookup"><span data-stu-id="42459-176">Open the Response3.xml file in an XML reader.</span></span> <span data-ttu-id="42459-177">请注意，此文件从 TraZ 根项目开始，并且此结构不使用 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="42459-177">Note that this file starts from the TraZ root item and that this structure is not configured using ER format.</span></span>   
6. <span data-ttu-id="42459-178">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="42459-178">Click Run.</span></span>
    * <span data-ttu-id="42459-179">单击“浏览”并选择 Response3.xml 文件。</span><span class="sxs-lookup"><span data-stu-id="42459-179">Click Browse and select the Response3.xml file.</span></span>  
7. <span data-ttu-id="42459-180">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="42459-180">Click OK.</span></span>
    * <span data-ttu-id="42459-181">检查生成的输出。</span><span class="sxs-lookup"><span data-stu-id="42459-181">Review the generated output.</span></span> <span data-ttu-id="42459-182">请注意，响应类型已被正确识别为不受支持 (ERModelEnumDataSourceHandler#EFSTA model#enumType#U)。</span><span class="sxs-lookup"><span data-stu-id="42459-182">Note that the response type has been correctly recognized as not-supported (ERModelEnumDataSourceHandler#EFSTA model#enumType#U).</span></span> <span data-ttu-id="42459-183">相应的消息已放入信息日志（根据 ER 验证设置），而且大多数数据模型未填充。</span><span class="sxs-lookup"><span data-stu-id="42459-183">The corresponding message has been placed in the Infolog (according to the ER validation setting), and most of the data model has not been filled in.</span></span>   
    * <span data-ttu-id="42459-184">在 XML 阅读器中打开 Response4.xml 文件。</span><span class="sxs-lookup"><span data-stu-id="42459-184">Open the Response4.xml file in an XML reader.</span></span> <span data-ttu-id="42459-185">请注意，此文件的结构与成功分析的 Response1.xml 几乎是相同的，除了根元素“TraC”的嵌套元素的顺序。</span><span class="sxs-lookup"><span data-stu-id="42459-185">Note that the structure of this file is almost the same as the successfully parsed Response1.xml, except the sequence of nested elements of the root element ‘TraC’.</span></span>   
8. <span data-ttu-id="42459-186">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="42459-186">Click Run.</span></span>
    * <span data-ttu-id="42459-187">单击“浏览”并选择 Response4.xml 文件。</span><span class="sxs-lookup"><span data-stu-id="42459-187">Click Browse and select the Response4.xml file.</span></span>  
9. <span data-ttu-id="42459-188">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="42459-188">Click OK.</span></span>
    * <span data-ttu-id="42459-189">检查生成的输出。</span><span class="sxs-lookup"><span data-stu-id="42459-189">Review the generated output.</span></span> <span data-ttu-id="42459-190">请注意，响应类型已被正确识别为不受支持 (ERModelEnumDataSourceHandler#EFSTA model#enumType#U))。</span><span class="sxs-lookup"><span data-stu-id="42459-190">Note that the response type has been correctly recognized as not-supported (ERModelEnumDataSourceHandler#EFSTA model#enumType#U)).</span></span> <span data-ttu-id="42459-191">相应的消息已放入信息日志，并且大多数数据模型未填充。</span><span class="sxs-lookup"><span data-stu-id="42459-191">The corresponding message has been placed in the Infolog, and most of the data model has not been filled in.</span></span> <span data-ttu-id="42459-192">这是此 ER 格式的当前设置假定了某个传入文件根项目的嵌套元素的序列。</span><span class="sxs-lookup"><span data-stu-id="42459-192">This is because the current setting of this ER format assumes a certain sequence of nested elements of the root item of the incoming file.</span></span>   
10. <span data-ttu-id="42459-193">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="42459-193">Close the page.</span></span>
11. <span data-ttu-id="42459-194">在树中，选择“Responses\Transaction completion\TraC”。</span><span class="sxs-lookup"><span data-stu-id="42459-194">In the tree, select 'Responses\Transaction completion\TraC'.</span></span>
12. <span data-ttu-id="42459-195">在“分析嵌套元素的顺序”字段中，选择“任意”。</span><span class="sxs-lookup"><span data-stu-id="42459-195">In the Parsing order of nested elements field, select 'Any'.</span></span>
    * <span data-ttu-id="42459-196">在“分析嵌套元素的顺序”字段中选择“任意”以允许此根 XML 项目的任何嵌套元素顺序。</span><span class="sxs-lookup"><span data-stu-id="42459-196">Select Any in the ‘Parsing order of nested elements’ field to allow any sequence of nested elements for this root XML item.</span></span>  
13. <span data-ttu-id="42459-197">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="42459-197">Click Save.</span></span>
14. <span data-ttu-id="42459-198">单击”将格式映射到模型“。</span><span class="sxs-lookup"><span data-stu-id="42459-198">Click Map format to model.</span></span>
15. <span data-ttu-id="42459-199">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="42459-199">Click Run.</span></span>
    * <span data-ttu-id="42459-200">单击“浏览”并选择 Response4.xml 文件。</span><span class="sxs-lookup"><span data-stu-id="42459-200">Click Browse and select the Response4.xml file.</span></span>  
16. <span data-ttu-id="42459-201">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="42459-201">Click OK.</span></span>
    * <span data-ttu-id="42459-202">检查生成的输出。</span><span class="sxs-lookup"><span data-stu-id="42459-202">Review the generated output.</span></span> <span data-ttu-id="42459-203">请注意，响应类型现在已被正确识别为 Response1.xml 文件的同等项。</span><span class="sxs-lookup"><span data-stu-id="42459-203">Note that the response type has now been properly recognized as equal for Response1.xml file.</span></span>  


