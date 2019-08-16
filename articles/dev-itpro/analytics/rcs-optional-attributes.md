---
title: 为 RCS 和 ER 准备应用程序特定的元数据
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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7a6fc1e54444584895aa75ae91d39143f27e34d8
ms.sourcegitcommit: d0fa7eb2166a30314205e7f70bbeaff6fbd5fb55
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/03/2019
ms.locfileid: "1726567"
---
# <a name="prepare-application-specific-metadata-for-rcs-and-er"></a><span data-ttu-id="a16b1-103">为 RCS 和 ER 准备应用程序特定的元数据</span><span class="sxs-lookup"><span data-stu-id="a16b1-103">Prepare application-specific metadata for RCS and ER</span></span>

<span data-ttu-id="a16b1-104">可以设计电子申报 (ER) 格式以分析 XML 格式的传入电子单据。</span><span class="sxs-lookup"><span data-stu-id="a16b1-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents in XML format.</span></span> <span data-ttu-id="a16b1-105">可以将所设计 ER 格式中 XML 元素的某些属性指定为可选。</span><span class="sxs-lookup"><span data-stu-id="a16b1-105">Certain attributes of XML elements can be specified in designed ER format as optional.</span></span> <span data-ttu-id="a16b1-106">这样就可以正确处理拥有此类 XML 元素和没有此类元素的传入文件。</span><span class="sxs-lookup"><span data-stu-id="a16b1-106">It will allow you to handle incoming files with and without such XML attributes properly.</span></span> <span data-ttu-id="a16b1-107">然后可以使用这些文件中的内容更新申请表数据。</span><span class="sxs-lookup"><span data-stu-id="a16b1-107">You can then use the content from these files to update application data.</span></span>

<span data-ttu-id="a16b1-108">若要了解有关此功能的详细信息，请完成[RCS 导入包含可选属性的 XML 格式文件](tasks/import-files-xml-format-optional-attributes.md)主题中的步骤，该主题是 7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677) 业务流程的一部分。</span><span class="sxs-lookup"><span data-stu-id="a16b1-108">To learn more about this feature, complete the steps in the topic, [RCS Import files in XML format with optional attributes](tasks/import-files-xml-format-optional-attributes.md), which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process.</span></span> <span data-ttu-id="a16b1-109">可从 [Microsoft 下载中心](https://go.microsoft.com/fwlink/?linkid=874684)下载此任务指南和关联的示例文件。</span><span class="sxs-lookup"><span data-stu-id="a16b1-109">You can download this task guide and associated sample files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>


| <span data-ttu-id="a16b1-110">内容描述</span><span class="sxs-lookup"><span data-stu-id="a16b1-110">Content description</span></span>       | <span data-ttu-id="a16b1-111">文件</span><span class="sxs-lookup"><span data-stu-id="a16b1-111">File</span></span>                                                         |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="a16b1-112">XML 格式的示例文件</span><span class="sxs-lookup"><span data-stu-id="a16b1-112">Sample file in XML format</span></span> | <span data-ttu-id="a16b1-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span><span class="sxs-lookup"><span data-stu-id="a16b1-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span></span>     |
| <span data-ttu-id="a16b1-114">任务指南</span><span class="sxs-lookup"><span data-stu-id="a16b1-114">Task guide</span></span>                | <span data-ttu-id="a16b1-115">RCS 使用可选的 attributes.axtr 导入 XML 格式的文件</span><span class="sxs-lookup"><span data-stu-id="a16b1-115">RCS Import files in XML format with optional attributes.axtr</span></span> |


<span data-ttu-id="a16b1-116">以下步骤说明系统管理员或电子报表开发人员角色的用户如何设计 ER 格式配置，以便导入包含可选属性的 XML 格式文件。</span><span class="sxs-lookup"><span data-stu-id="a16b1-116">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="a16b1-117">为了完成这些步骤，您必须首先完成[创建配置提供程序并标记为当前运行的](tasks/er-configuration-provider-mark-it-active-2016-11.md)这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="a16b1-117">To complete these steps, you must first complete the steps in the procedure, [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="a16b1-118">开始之前，从 Microsoft 下载中心 (https://go.microsoft.com/fwlink/?linkid=874684) 下载 IncomingDocumentToLearnHowToHandleOptionalAttributes.xml 文件并保存到本地。</span><span class="sxs-lookup"><span data-stu-id="a16b1-118">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span></span>

1. <span data-ttu-id="a16b1-119">转到**组织管理** > **工作区** > **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-119">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="a16b1-120">确保示例公司 Litware 公司的配置提供程序可用且标记为**有效**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-120">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="a16b1-121">如果没有看到此配置提供程序，请首先完成[创建配置提供程序并标记为当前运行的](tasks/er-configuration-provider-mark-it-active-2016-11.md)主题中的步骤。</span><span class="sxs-lookup"><span data-stu-id="a16b1-121">If you don’t see this configuration provider, complete the steps in the topic, [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="a16b1-122">单击**申报配置**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-122">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="a16b1-123">创建新的数据模型配置</span><span class="sxs-lookup"><span data-stu-id="a16b1-123">Create a new data model configuration</span></span>
1. <span data-ttu-id="a16b1-124">单击**创建配置**，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="a16b1-124">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="a16b1-125">在**名称**字段中，键入“用于导入 xml 文件的模型”。</span><span class="sxs-lookup"><span data-stu-id="a16b1-125">In the **Name** field, type 'Model to import xml file'.</span></span>
3. <span data-ttu-id="a16b1-126">单击**创建配置**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-126">Click **Create configuration**.</span></span>
4. <span data-ttu-id="a16b1-127">单击**设计器**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-127">Click **Designer**.</span></span>
5. <span data-ttu-id="a16b1-128">单击**新建**，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="a16b1-128">Click **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="a16b1-129">在**名称**字段中，键入“根”。</span><span class="sxs-lookup"><span data-stu-id="a16b1-129">In the **Name** field, type 'Root'.</span></span>
7. <span data-ttu-id="a16b1-130">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-130">Click **Add**.</span></span>
8. <span data-ttu-id="a16b1-131">单击**新建**，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="a16b1-131">Click **New** to open the drop dialog.</span></span>
9. <span data-ttu-id="a16b1-132">在**名称**字段中，键入“列表”。</span><span class="sxs-lookup"><span data-stu-id="a16b1-132">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="a16b1-133">在**物料类型**字段中，选择**记录列表**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-133">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="a16b1-134">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-134">Click **Add**.</span></span>
12. <span data-ttu-id="a16b1-135">单击**新建**，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="a16b1-135">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="a16b1-136">在**名称**字段中，键入“代码”。</span><span class="sxs-lookup"><span data-stu-id="a16b1-136">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="a16b1-137">在**物料类型**字段中，选择**字符串**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-137">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="a16b1-138">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-138">Click **Add**.</span></span>
16. <span data-ttu-id="a16b1-139">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-139">Click **Save**.</span></span>
17. <span data-ttu-id="a16b1-140">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a16b1-140">Close the page.</span></span>
18. <span data-ttu-id="a16b1-141">单击**更改状态**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-141">Click **Change status**.</span></span>
19. <span data-ttu-id="a16b1-142">单击**完成**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-142">Click **Complete**.</span></span>
20. <span data-ttu-id="a16b1-143">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-143">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="a16b1-144">创建格式以导入数据</span><span class="sxs-lookup"><span data-stu-id="a16b1-144">Create a format for data import</span></span>
1. <span data-ttu-id="a16b1-145">单击**创建配置**，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="a16b1-145">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="a16b1-146">在**新建**字段中，输入“格式基于‘用于导入 xml 文件的模型’数据模型”。</span><span class="sxs-lookup"><span data-stu-id="a16b1-146">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3. <span data-ttu-id="a16b1-147">在**名称**字段中，键入“用于导入 xml 文件的格式”。</span><span class="sxs-lookup"><span data-stu-id="a16b1-147">In the **Nam**e field, type 'Format to import xml file'.</span></span> 
4. <span data-ttu-id="a16b1-148">在**支持数据导入**字段中选择**是**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-148">Select **Yes** in the **Supports data import** field.</span></span>
5. <span data-ttu-id="a16b1-149">单击**创建配置**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-149">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="a16b1-150">设计格式以分析 xml 格式的传入文件</span><span class="sxs-lookup"><span data-stu-id="a16b1-150">Design a format to parse incoming file in xml format</span></span>
1. <span data-ttu-id="a16b1-151">单击**设计器**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-151">Click **Designer**.</span></span>
2. <span data-ttu-id="a16b1-152">单击**添加根**以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="a16b1-152">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="a16b1-153">在树结构中，选择 **XML\元素**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-153">In the tree, select **XML\Element**.</span></span>
4. <span data-ttu-id="a16b1-154">在**名称**字段中，键入“根”。</span><span class="sxs-lookup"><span data-stu-id="a16b1-154">In the **Name** field, type 'root'.</span></span>
5. <span data-ttu-id="a16b1-155">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-155">Click **OK**.</span></span>
6. <span data-ttu-id="a16b1-156">单击**添加**以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="a16b1-156">Click **Add** to open the drop dialog.</span></span>
7. <span data-ttu-id="a16b1-157">在树结构中，选择 **XML\元素**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-157">In the tree, select **XML\Element**.</span></span>
8. <span data-ttu-id="a16b1-158">在**名称**字段中，键入“单据”。</span><span class="sxs-lookup"><span data-stu-id="a16b1-158">In the **Name** field, type 'document'.</span></span>
9. <span data-ttu-id="a16b1-159">在**多样性**字段中，选择**一个 多个**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-159">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="a16b1-160">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-160">Click **OK**.</span></span>
11. <span data-ttu-id="a16b1-161">在树中，选择**根\文档**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-161">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="a16b1-162">单击**添加**以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="a16b1-162">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="a16b1-163">在树结构中，选择 **XML\属性**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-163">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="a16b1-164">在**名称**字段中，键入“Id”。</span><span class="sxs-lookup"><span data-stu-id="a16b1-164">In the **Name** field, type 'id'.</span></span>
15. <span data-ttu-id="a16b1-165">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-165">Click **OK**.</span></span>
16. <span data-ttu-id="a16b1-166">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-166">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="a16b1-167">设计格式映射以将分析的信息保存到数据模型</span><span class="sxs-lookup"><span data-stu-id="a16b1-167">Design a format mapping to save parsed information to data model</span></span>
1.  <span data-ttu-id="a16b1-168">单击**将格式映射到模型**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-168">Click **Map format to model**.</span></span>
2.  <span data-ttu-id="a16b1-169">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-169">Click **New**.</span></span>
3.  <span data-ttu-id="a16b1-170">在**定义**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="a16b1-170">In the **Definition** field, enter or select a value.</span></span>
4.  <span data-ttu-id="a16b1-171">在**名称**字段中，键入“映射”。</span><span class="sxs-lookup"><span data-stu-id="a16b1-171">In the **Name** field, type 'Mapping'.</span></span>
5.  <span data-ttu-id="a16b1-172">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-172">Click **Save**.</span></span>
6.  <span data-ttu-id="a16b1-173">单击**设计器**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-173">Click **Designer**.</span></span>
7.  <span data-ttu-id="a16b1-174">在树中，展开**格式**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-174">In the tree, expand **format**.</span></span>
8.  <span data-ttu-id="a16b1-175">在树中，展开**格式\r根: XML 元素(根)**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-175">In the tree, expand **format\root: XML Element(root)**.</span></span>
9.  <span data-ttu-id="a16b1-176">在树中，选择 \**格式\r根: XML 元素(根)\文档: XML 元素 1*。</span><span class="sxs-lookup"><span data-stu-id="a16b1-176">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="a16b1-177">(文档)\*\*。</span><span class="sxs-lookup"><span data-stu-id="a16b1-177">(document)\*\*.</span></span>
10. <span data-ttu-id="a16b1-178">单击**绑定**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-178">Click **Bind**.</span></span>
11. <span data-ttu-id="a16b1-179">在树中，展开 \**格式\r根: XML 元素(根)\文档: XML 元素 1*。</span><span class="sxs-lookup"><span data-stu-id="a16b1-179">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="a16b1-180">(文档)\*\*。</span><span class="sxs-lookup"><span data-stu-id="a16b1-180">(document)\*\*.</span></span>
12. <span data-ttu-id="a16b1-181">在树中，选择 \**格式\r根: XML 元素(根)\文档: XML 元素 1*。</span><span class="sxs-lookup"><span data-stu-id="a16b1-181">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="a16b1-182">(文档)\id\*\*。</span><span class="sxs-lookup"><span data-stu-id="a16b1-182">(document)\id\*\*.</span></span>
13. <span data-ttu-id="a16b1-183">在树中，展开**列表 = format.root.document**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-183">In the tree, expand **List = format.root.document**.</span></span>
14. <span data-ttu-id="a16b1-184">在树中，选择**列表 = format.root.document\代码**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-184">In the tree, select **List = format.root.document\Code**.</span></span>
15. <span data-ttu-id="a16b1-185">单击**绑定**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-185">Click **Bind**.</span></span>
16. <span data-ttu-id="a16b1-186">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-186">Click **Save**.</span></span>
17. <span data-ttu-id="a16b1-187">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a16b1-187">Close the page.</span></span>

## <a name="run-format-mapping"></a><span data-ttu-id="a16b1-188">运行格式映射</span><span class="sxs-lookup"><span data-stu-id="a16b1-188">Run format mapping</span></span>
1. <span data-ttu-id="a16b1-189">单击**运行**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-189">Click **Run**.</span></span>
2. <span data-ttu-id="a16b1-190">单击**浏览**，然后选择文件 **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-190">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="a16b1-191">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-191">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="a16b1-192">尚未导入所选文件，因为格式设计认为“文档”元素有“id”属性，但是导入的文件中不包含此类属性。</span><span class="sxs-lookup"><span data-stu-id="a16b1-192">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="a16b1-193">修改格式结构以将 xml 属性作为可选属性处理。</span><span class="sxs-lookup"><span data-stu-id="a16b1-193">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="a16b1-194">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a16b1-194">Close the page.</span></span>
2. <span data-ttu-id="a16b1-195">在树中，展开**根\文档**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-195">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="a16b1-196">在树中，选择**根\文档\id**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-196">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="a16b1-197">在**清空所缺少属性的字符串**字段中，选择**是**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-197">In the **Empty string for missing attribute** field, select **Yes**.</span></span>
5. <span data-ttu-id="a16b1-198">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-198">Click **Save**.</span></span>

## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="a16b1-199">运行格式映射以测试更改</span><span class="sxs-lookup"><span data-stu-id="a16b1-199">Run format mapping to test changes</span></span>
1. <span data-ttu-id="a16b1-200">单击**将格式映射到模型**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-200">Click **Map format to model**.</span></span>
2. <span data-ttu-id="a16b1-201">单击**运行**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-201">Click **Run**.</span></span>
3. <span data-ttu-id="a16b1-202">单击**浏览**，然后选择文件 **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-202">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
4. <span data-ttu-id="a16b1-203">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="a16b1-203">Click **OK**.</span></span>
5. <span data-ttu-id="a16b1-204">检查生成的文件。</span><span class="sxs-lookup"><span data-stu-id="a16b1-204">Review the generated file.</span></span> <span data-ttu-id="a16b1-205">请注意，已导入同一个文件，因为格式设计现在将“document”元素的“id”属性视为可选。</span><span class="sxs-lookup"><span data-stu-id="a16b1-205">Note that same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>