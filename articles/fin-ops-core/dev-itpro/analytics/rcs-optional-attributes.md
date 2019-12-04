---
title: 导入包含可选属性的 XML 格式文件
description: 本主题提供有关设计 ER 格式以指定 XML 属性来分析 XML 格式的传入电子单据的信息。
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5e2989906c5aa3ead9e46b8ed5333e880e5cf1c6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769939"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="89987-103">导入包含可选属性的 XML 格式文件</span><span class="sxs-lookup"><span data-stu-id="89987-103">Import files in XML format with optional attributes</span></span>

<span data-ttu-id="89987-104">可以设计电子申报 (ER) 格式以分析 XML 格式的传入电子单据。</span><span class="sxs-lookup"><span data-stu-id="89987-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents in XML format.</span></span> <span data-ttu-id="89987-105">可以将所设计 ER 格式中 XML 元素的某些属性指定为可选。</span><span class="sxs-lookup"><span data-stu-id="89987-105">Certain attributes of XML elements can be specified in designed ER format as optional.</span></span> <span data-ttu-id="89987-106">这样就可以正确处理拥有此类 XML 元素和没有此类元素的传入文件。</span><span class="sxs-lookup"><span data-stu-id="89987-106">It will allow you to handle incoming files with and without such XML attributes properly.</span></span> <span data-ttu-id="89987-107">然后可以使用这些文件中的内容更新申请表数据。</span><span class="sxs-lookup"><span data-stu-id="89987-107">You can then use the content from these files to update application data.</span></span>

<span data-ttu-id="89987-108">若要了解有关此功能的详细信息，请完成 [(RCS) 导入包含可选属性的 XML 格式文件](tasks/import-files-xml-format-optional-attributes.md)主题中的步骤，该主题是 7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677) 业务流程的一部分。</span><span class="sxs-lookup"><span data-stu-id="89987-108">To learn more about this feature, complete the steps in the topic, [(RCS) Import files in XML format with optional attributes](tasks/import-files-xml-format-optional-attributes.md), which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process.</span></span> <span data-ttu-id="89987-109">可从 [Microsoft 下载中心](https://go.microsoft.com/fwlink/?linkid=874684)下载此任务指南和关联的示例文件。</span><span class="sxs-lookup"><span data-stu-id="89987-109">You can download this task guide and associated sample files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>


| <span data-ttu-id="89987-110">内容描述</span><span class="sxs-lookup"><span data-stu-id="89987-110">Content description</span></span>       | <span data-ttu-id="89987-111">文件</span><span class="sxs-lookup"><span data-stu-id="89987-111">File</span></span>                                                         |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="89987-112">XML 格式的示例文件</span><span class="sxs-lookup"><span data-stu-id="89987-112">Sample file in XML format</span></span> | <span data-ttu-id="89987-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span><span class="sxs-lookup"><span data-stu-id="89987-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span></span>     |
| <span data-ttu-id="89987-114">任务指南</span><span class="sxs-lookup"><span data-stu-id="89987-114">Task guide</span></span>                | <span data-ttu-id="89987-115">RCS 使用可选的 attributes.axtr 导入 XML 格式的文件</span><span class="sxs-lookup"><span data-stu-id="89987-115">RCS Import files in XML format with optional attributes.axtr</span></span> |


<span data-ttu-id="89987-116">以下步骤说明系统管理员或电子报表开发人员角色的用户如何设计 ER 格式配置，以便导入包含可选属性的 XML 格式文件。</span><span class="sxs-lookup"><span data-stu-id="89987-116">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="89987-117">为了完成这些步骤，您必须首先完成[创建配置提供程序并标记为当前运行的](tasks/er-configuration-provider-mark-it-active-2016-11.md)过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="89987-117">To complete these steps, you must first complete the steps in the procedure, [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="89987-118">开始之前，从 Microsoft 下载中心 (https://go.microsoft.com/fwlink/?linkid=874684) 下载 IncomingDocumentToLearnHowToHandleOptionalAttributes.xml 文件并保存到本地。</span><span class="sxs-lookup"><span data-stu-id="89987-118">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span></span>

1. <span data-ttu-id="89987-119">转到**组织管理** > **工作区** > **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="89987-119">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="89987-120">确保示例公司 Litware 公司的配置提供程序可用且标记为**有效**。</span><span class="sxs-lookup"><span data-stu-id="89987-120">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="89987-121">如果没有看到此配置提供程序，请首先完成[创建配置提供程序并标记为当前运行的](tasks/er-configuration-provider-mark-it-active-2016-11.md)这一主题中的步骤。</span><span class="sxs-lookup"><span data-stu-id="89987-121">If you don’t see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="89987-122">单击**申报配置**。</span><span class="sxs-lookup"><span data-stu-id="89987-122">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="89987-123">创建新的数据模型配置</span><span class="sxs-lookup"><span data-stu-id="89987-123">Create a new data model configuration</span></span>
1. <span data-ttu-id="89987-124">单击**创建配置**，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="89987-124">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="89987-125">在**名称**字段中，键入“用于导入 xml 文件的模型”。</span><span class="sxs-lookup"><span data-stu-id="89987-125">In the **Name** field, type 'Model to import xml file'.</span></span>
3. <span data-ttu-id="89987-126">单击**创建配置**。</span><span class="sxs-lookup"><span data-stu-id="89987-126">Click **Create configuration**.</span></span>
4. <span data-ttu-id="89987-127">单击**设计器**。</span><span class="sxs-lookup"><span data-stu-id="89987-127">Click **Designer**.</span></span>
5. <span data-ttu-id="89987-128">单击**新建**，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="89987-128">Click **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="89987-129">在**名称**字段中，键入“根”。</span><span class="sxs-lookup"><span data-stu-id="89987-129">In the **Name** field, type 'Root'.</span></span>
7. <span data-ttu-id="89987-130">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="89987-130">Click **Add**.</span></span>
8. <span data-ttu-id="89987-131">单击**新建**，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="89987-131">Click **New** to open the drop dialog.</span></span>
9. <span data-ttu-id="89987-132">在**名称**字段中，键入“列表”。</span><span class="sxs-lookup"><span data-stu-id="89987-132">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="89987-133">在**物料类型**字段中，选择**记录列表**。</span><span class="sxs-lookup"><span data-stu-id="89987-133">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="89987-134">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="89987-134">Click **Add**.</span></span>
12. <span data-ttu-id="89987-135">单击**新建**，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="89987-135">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="89987-136">在**名称**字段中，键入“代码”。</span><span class="sxs-lookup"><span data-stu-id="89987-136">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="89987-137">在**物料类型**字段中，选择**字符串**。</span><span class="sxs-lookup"><span data-stu-id="89987-137">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="89987-138">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="89987-138">Click **Add**.</span></span>
16. <span data-ttu-id="89987-139">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="89987-139">Click **Save**.</span></span>
17. <span data-ttu-id="89987-140">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="89987-140">Close the page.</span></span>
18. <span data-ttu-id="89987-141">单击**更改状态**。</span><span class="sxs-lookup"><span data-stu-id="89987-141">Click **Change status**.</span></span>
19. <span data-ttu-id="89987-142">单击**完成**。</span><span class="sxs-lookup"><span data-stu-id="89987-142">Click **Complete**.</span></span>
20. <span data-ttu-id="89987-143">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="89987-143">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="89987-144">创建格式以导入数据</span><span class="sxs-lookup"><span data-stu-id="89987-144">Create a format for data import</span></span>
1. <span data-ttu-id="89987-145">单击**创建配置**，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="89987-145">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="89987-146">在**新建**字段中，输入“格式基于‘用于导入 xml 文件的模型’数据模型”。</span><span class="sxs-lookup"><span data-stu-id="89987-146">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3. <span data-ttu-id="89987-147">在**名称**字段中，键入“用于导入 xml 文件的格式”。</span><span class="sxs-lookup"><span data-stu-id="89987-147">In the **Nam**e field, type 'Format to import xml file'.</span></span> 
4. <span data-ttu-id="89987-148">在**支持数据导入**字段中选择**是**。</span><span class="sxs-lookup"><span data-stu-id="89987-148">Select **Yes** in the **Supports data import** field.</span></span>
5. <span data-ttu-id="89987-149">单击**创建配置**。</span><span class="sxs-lookup"><span data-stu-id="89987-149">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="89987-150">设计格式以分析 xml 格式的传入文件</span><span class="sxs-lookup"><span data-stu-id="89987-150">Design a format to parse incoming file in xml format</span></span>
1. <span data-ttu-id="89987-151">单击**设计器**。</span><span class="sxs-lookup"><span data-stu-id="89987-151">Click **Designer**.</span></span>
2. <span data-ttu-id="89987-152">单击**添加根**以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="89987-152">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="89987-153">在树结构中，选择 **XML\元素**。</span><span class="sxs-lookup"><span data-stu-id="89987-153">In the tree, select **XML\Element**.</span></span>
4. <span data-ttu-id="89987-154">在**名称**字段中，键入“根”。</span><span class="sxs-lookup"><span data-stu-id="89987-154">In the **Name** field, type 'root'.</span></span>
5. <span data-ttu-id="89987-155">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="89987-155">Click **OK**.</span></span>
6. <span data-ttu-id="89987-156">单击**添加**以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="89987-156">Click **Add** to open the drop dialog.</span></span>
7. <span data-ttu-id="89987-157">在树结构中，选择 **XML\元素**。</span><span class="sxs-lookup"><span data-stu-id="89987-157">In the tree, select **XML\Element**.</span></span>
8. <span data-ttu-id="89987-158">在**名称**字段中，键入“单据”。</span><span class="sxs-lookup"><span data-stu-id="89987-158">In the **Name** field, type 'document'.</span></span>
9. <span data-ttu-id="89987-159">在**多样性**字段中，选择**一个 多个**。</span><span class="sxs-lookup"><span data-stu-id="89987-159">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="89987-160">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="89987-160">Click **OK**.</span></span>
11. <span data-ttu-id="89987-161">在树中，选择**根\文档**。</span><span class="sxs-lookup"><span data-stu-id="89987-161">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="89987-162">单击**添加**以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="89987-162">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="89987-163">在树结构中，选择 **XML\属性**。</span><span class="sxs-lookup"><span data-stu-id="89987-163">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="89987-164">在**名称**字段中，键入“Id”。</span><span class="sxs-lookup"><span data-stu-id="89987-164">In the **Name** field, type 'id'.</span></span>
15. <span data-ttu-id="89987-165">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="89987-165">Click **OK**.</span></span>
16. <span data-ttu-id="89987-166">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="89987-166">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="89987-167">设计格式映射以将分析的信息保存到数据模型</span><span class="sxs-lookup"><span data-stu-id="89987-167">Design a format mapping to save parsed information to data model</span></span>
1.  <span data-ttu-id="89987-168">单击**将格式映射到模型**。</span><span class="sxs-lookup"><span data-stu-id="89987-168">Click **Map format to model**.</span></span>
2.  <span data-ttu-id="89987-169">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="89987-169">Click **New**.</span></span>
3.  <span data-ttu-id="89987-170">在**定义**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="89987-170">In the **Definition** field, enter or select a value.</span></span>
4.  <span data-ttu-id="89987-171">在**名称**字段中，键入“映射”。</span><span class="sxs-lookup"><span data-stu-id="89987-171">In the **Name** field, type 'Mapping'.</span></span>
5.  <span data-ttu-id="89987-172">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="89987-172">Click **Save**.</span></span>
6.  <span data-ttu-id="89987-173">单击**设计器**。</span><span class="sxs-lookup"><span data-stu-id="89987-173">Click **Designer**.</span></span>
7.  <span data-ttu-id="89987-174">在树中，展开**格式**。</span><span class="sxs-lookup"><span data-stu-id="89987-174">In the tree, expand **format**.</span></span>
8.  <span data-ttu-id="89987-175">在树中，展开**格式\根: XML 元素(根)**。</span><span class="sxs-lookup"><span data-stu-id="89987-175">In the tree, expand **format\root: XML Element(root)**.</span></span>
9.  <span data-ttu-id="89987-176">在树中，选择 \**格式\根: XML 元素(根)\文档: XML 元素 1*。</span><span class="sxs-lookup"><span data-stu-id="89987-176">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="89987-177">(文档)\*\*。</span><span class="sxs-lookup"><span data-stu-id="89987-177">(document)\*\*.</span></span>
10. <span data-ttu-id="89987-178">单击**绑定**。</span><span class="sxs-lookup"><span data-stu-id="89987-178">Click **Bind**.</span></span>
11. <span data-ttu-id="89987-179">在树中，展开 \**格式\根: XML 元素(根)\文档: XML 元素 1*。</span><span class="sxs-lookup"><span data-stu-id="89987-179">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="89987-180">(文档)\*\*。</span><span class="sxs-lookup"><span data-stu-id="89987-180">(document)\*\*.</span></span>
12. <span data-ttu-id="89987-181">在树中，选择 \**格式\根: XML 元素(根)\文档: XML 元素 1*。</span><span class="sxs-lookup"><span data-stu-id="89987-181">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="89987-182">(文档)\id\*\*。</span><span class="sxs-lookup"><span data-stu-id="89987-182">(document)\id\*\*.</span></span>
13. <span data-ttu-id="89987-183">在树中，展开**列表 = format.root.document**。</span><span class="sxs-lookup"><span data-stu-id="89987-183">In the tree, expand **List = format.root.document**.</span></span>
14. <span data-ttu-id="89987-184">在树中，选择**列表 = format.root.document\代码**。</span><span class="sxs-lookup"><span data-stu-id="89987-184">In the tree, select **List = format.root.document\Code**.</span></span>
15. <span data-ttu-id="89987-185">单击**绑定**。</span><span class="sxs-lookup"><span data-stu-id="89987-185">Click **Bind**.</span></span>
16. <span data-ttu-id="89987-186">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="89987-186">Click **Save**.</span></span>
17. <span data-ttu-id="89987-187">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="89987-187">Close the page.</span></span>

## <a name="run-format-mapping"></a><span data-ttu-id="89987-188">运行格式映射</span><span class="sxs-lookup"><span data-stu-id="89987-188">Run format mapping</span></span>
1. <span data-ttu-id="89987-189">单击**运行**。</span><span class="sxs-lookup"><span data-stu-id="89987-189">Click **Run**.</span></span>
2. <span data-ttu-id="89987-190">单击**浏览**，然后选择文件 **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**。</span><span class="sxs-lookup"><span data-stu-id="89987-190">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="89987-191">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="89987-191">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="89987-192">尚未导入所选文件，因为格式设计认为“文档”元素有“id”属性，但是导入的文件中不包含此类属性。</span><span class="sxs-lookup"><span data-stu-id="89987-192">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="89987-193">修改格式结构以将 xml 属性作为可选属性处理。</span><span class="sxs-lookup"><span data-stu-id="89987-193">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="89987-194">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="89987-194">Close the page.</span></span>
2. <span data-ttu-id="89987-195">在树中，展开**根\文档**。</span><span class="sxs-lookup"><span data-stu-id="89987-195">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="89987-196">在树中，选择**根\文档\id**。</span><span class="sxs-lookup"><span data-stu-id="89987-196">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="89987-197">在**清空所缺少属性的字符串**字段中，选择**是**。</span><span class="sxs-lookup"><span data-stu-id="89987-197">In the **Empty string for missing attribute** field, select **Yes**.</span></span>
5. <span data-ttu-id="89987-198">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="89987-198">Click **Save**.</span></span>

## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="89987-199">运行格式映射以测试更改</span><span class="sxs-lookup"><span data-stu-id="89987-199">Run format mapping to test changes</span></span>
1. <span data-ttu-id="89987-200">单击**将格式映射到模型**。</span><span class="sxs-lookup"><span data-stu-id="89987-200">Click **Map format to model**.</span></span>
2. <span data-ttu-id="89987-201">单击**运行**。</span><span class="sxs-lookup"><span data-stu-id="89987-201">Click **Run**.</span></span>
3. <span data-ttu-id="89987-202">单击**浏览**，然后选择文件 **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**。</span><span class="sxs-lookup"><span data-stu-id="89987-202">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
4. <span data-ttu-id="89987-203">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="89987-203">Click **OK**.</span></span>
5. <span data-ttu-id="89987-204">检查生成的文件。</span><span class="sxs-lookup"><span data-stu-id="89987-204">Review the generated file.</span></span> <span data-ttu-id="89987-205">请注意，已导入同一个文件，因为格式设计现在将“document”元素的“id”属性视为可选。</span><span class="sxs-lookup"><span data-stu-id="89987-205">Note that same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
