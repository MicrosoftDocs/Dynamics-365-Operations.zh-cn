---
title: (RCS) 导入包含可选属性的 XML 格式文件
description: 本主题介绍用户如何设计 ER 格式配置以导入 XML 格式且包含可选属性的文件。
author: NickSelin
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1290598d8dbd5b72d679ccf3e642e75b6dc3215
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/04/2019
ms.locfileid: "1727067"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="1b9fa-103">(RCS) 导入包含可选属性的 XML 格式文件</span><span class="sxs-lookup"><span data-stu-id="1b9fa-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1b9fa-104">以下步骤说明系统管理员或电子报表开发人员角色的用户如何设计 ER 格式配置，以便导入包含可选属性的 XML 格式文件。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="1b9fa-105">为了完成这些步骤，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-105">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="1b9fa-106">开始之前，从 [Microsoft 下载中心](https://go.microsoft.com/fwlink/?linkid=874684)下载 IncomingDocumentToLearnHowToHandleOptionalAttributes.xml 文件并保存到本地。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.  <span data-ttu-id="1b9fa-107">转到**所有工作区** > **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.  <span data-ttu-id="1b9fa-108">确保示例公司 Litware 公司的配置提供程序可用且标记为**有效**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="1b9fa-109">如果没有看到此配置提供程序，请首先完成[创建配置提供程序并标记为当前运行的](er-configuration-provider-mark-it-active-2016-11.md)这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-109">If you don’t see this configuration provider, complete the steps in the procedure [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.  <span data-ttu-id="1b9fa-110">单击**申报配置**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="1b9fa-111">创建新的数据模型配置</span><span class="sxs-lookup"><span data-stu-id="1b9fa-111">Create a new data model configuration</span></span>
1.  <span data-ttu-id="1b9fa-112">单击**创建配置**，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-112">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="1b9fa-113">在**名称**字段中，键入“用于导入 xml 文件的模型”。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.  <span data-ttu-id="1b9fa-114">单击**创建配置**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-114">Click **Create configuration**.</span></span>
4.  <span data-ttu-id="1b9fa-115">单击**设计器**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-115">Click **Designer**.</span></span>
5.  <span data-ttu-id="1b9fa-116">单击**新建**，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-116">Click **New** to open the drop dialog.</span></span>
6.  <span data-ttu-id="1b9fa-117">在**名称**字段中，键入“根”。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-117">In the **Name** field, type 'Root'.</span></span>
7.  <span data-ttu-id="1b9fa-118">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-118">Click **Add**.</span></span>
8.  <span data-ttu-id="1b9fa-119">单击**新建**，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-119">Click **New** to open the drop dialog.</span></span>
9.  <span data-ttu-id="1b9fa-120">在**名称**字段中，键入“列表”。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-120">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="1b9fa-121">在**物料类型**字段中，选择**记录列表**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-121">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="1b9fa-122">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-122">Click **Add**.</span></span>
12. <span data-ttu-id="1b9fa-123">单击**新建**，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-123">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="1b9fa-124">在**名称**字段中，键入“代码”。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-124">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="1b9fa-125">在**物料类型**字段中，选择**字符串**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-125">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="1b9fa-126">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-126">Click **Add**.</span></span>
16. <span data-ttu-id="1b9fa-127">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-127">Click **Save**.</span></span>
17. <span data-ttu-id="1b9fa-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-128">Close the page.</span></span>
18. <span data-ttu-id="1b9fa-129">单击**更改状态**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-129">Click **Change status**.</span></span>
19. <span data-ttu-id="1b9fa-130">单击**完成**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-130">Click **Complete**.</span></span>
20. <span data-ttu-id="1b9fa-131">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="1b9fa-132">创建格式以导入数据</span><span class="sxs-lookup"><span data-stu-id="1b9fa-132">Create a format for data import</span></span>
1.  <span data-ttu-id="1b9fa-133">单击**创建配置**，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-133">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="1b9fa-134">在**新建**字段中，输入“格式基于‘用于导入 xml 文件的模型’数据模型”。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.  <span data-ttu-id="1b9fa-135">在**名称**字段中，键入“用于导入 xml 文件的格式”。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.  <span data-ttu-id="1b9fa-136">在**支持数据导入**字段中选择**是**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-136">Select **Yes** in the **Supports data import** field.</span></span>
5.  <span data-ttu-id="1b9fa-137">单击**创建配置**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="1b9fa-138">设计格式以分析 xml 格式的传入文件</span><span class="sxs-lookup"><span data-stu-id="1b9fa-138">Design a format to parse incoming file in xml format</span></span>
1.  <span data-ttu-id="1b9fa-139">单击**设计器**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-139">Click **Designer**.</span></span>
2.  <span data-ttu-id="1b9fa-140">单击**添加根**以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-140">Click **Add root** to open the drop dialog.</span></span>
3.  <span data-ttu-id="1b9fa-141">在树结构中，选择 **XML\元素**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-141">In the tree, select **XML\Element**.</span></span>
4.  <span data-ttu-id="1b9fa-142">在**名称**字段中，键入“根”。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-142">In the **Name** field, type 'root'.</span></span>
5.  <span data-ttu-id="1b9fa-143">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-143">Click **OK**.</span></span>
6.  <span data-ttu-id="1b9fa-144">单击**添加**以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-144">Click **Add** to open the drop dialog.</span></span>
7.  <span data-ttu-id="1b9fa-145">在树结构中，选择 **XML\元素**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-145">In the tree, select **XML\Element**.</span></span>
8.  <span data-ttu-id="1b9fa-146">在**名称**字段中，键入“单据”。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-146">In the **Name** field, type 'document'.</span></span>
9.  <span data-ttu-id="1b9fa-147">在**多样性**字段中，选择**一个 多个**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-147">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="1b9fa-148">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-148">Click **OK**.</span></span>
11. <span data-ttu-id="1b9fa-149">在树中，选择**根\文档**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-149">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="1b9fa-150">单击**添加**以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-150">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="1b9fa-151">在树结构中，选择 **XML\属性**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-151">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="1b9fa-152">在**名称**字段中，键入“ID”。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-152">In the **Name** field, type 'ID'.</span></span>
15. <span data-ttu-id="1b9fa-153">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-153">Click **OK**.</span></span>
16. <span data-ttu-id="1b9fa-154">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="1b9fa-155">设计格式映射以将分析的信息保存到数据模型</span><span class="sxs-lookup"><span data-stu-id="1b9fa-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="1b9fa-156">单击**将格式映射到模型**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="1b9fa-157">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-157">Click **New**.</span></span>
3. <span data-ttu-id="1b9fa-158">在**定义**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="1b9fa-159">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="1b9fa-160">在**名称**字段中，键入“映射”。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="1b9fa-161">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-161">Click **Save**.</span></span>
7. <span data-ttu-id="1b9fa-162">单击**设计器**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-162">Click **Designer**.</span></span>
8. <span data-ttu-id="1b9fa-163">在树中，展开**格式**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="1b9fa-164">在树中，展开**格式\r根: XML 元素(根)**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10. <span data-ttu-id="1b9fa-165">在树中，选择 \**格式\r根: XML 元素(根)\文档: XML 元素 1*。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="1b9fa-166">(文档)\*\*。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-166">(document)\*\*.</span></span>
11. <span data-ttu-id="1b9fa-167">单击**绑定**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-167">Click **Bind**.</span></span>
12. <span data-ttu-id="1b9fa-168">在树中，展开 \**格式\r根: XML 元素(根)\文档: XML 元素 1*。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="1b9fa-169">(文档)\*\*。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-169">(document)\*\*.</span></span>
13. <span data-ttu-id="1b9fa-170">在树中，选择 \**格式\r根: XML 元素(根)\文档: XML 元素 1*。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="1b9fa-171">(文档)\id\*\*。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-171">(document)\id\*\*.</span></span>
14. <span data-ttu-id="1b9fa-172">在树中，展开**列表 = format.root.document**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-172">In the tree, expand **List = format.root.document**.</span></span>
15. <span data-ttu-id="1b9fa-173">在树中，选择**列表 = format.root.document\代码**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-173">In the tree, select **List = format.root.document\Code**.</span></span>
16. <span data-ttu-id="1b9fa-174">单击**绑定**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-174">Click **Bind**.</span></span>
17. <span data-ttu-id="1b9fa-175">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-175">Click **Save**.</span></span>
18. <span data-ttu-id="1b9fa-176">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="1b9fa-177">运行格式映射</span><span class="sxs-lookup"><span data-stu-id="1b9fa-177">Run format mapping</span></span>
1. <span data-ttu-id="1b9fa-178">单击**运行**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-178">Click **Run**.</span></span>
2. <span data-ttu-id="1b9fa-179">单击**浏览**，然后选择 **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="1b9fa-180">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="1b9fa-181">尚未导入所选文件，因为格式设计认为“文档”元素有“id”属性，但是导入的文件中不包含此类属性。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-181">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="1b9fa-182">修改格式结构以将 xml 属性作为可选属性处理。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="1b9fa-183">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-183">Close the page.</span></span>
2. <span data-ttu-id="1b9fa-184">在树中，展开**根\文档**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="1b9fa-185">在树中，选择**根\文档\id**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="1b9fa-186">在**清空所缺少属性的字符串**字段中选择**是**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="1b9fa-187">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="1b9fa-188">运行格式映射以测试更改</span><span class="sxs-lookup"><span data-stu-id="1b9fa-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="1b9fa-189">单击**将格式映射到模型**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="1b9fa-190">单击**运行**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-190">Click **Run**.</span></span>
3. <span data-ttu-id="1b9fa-191">单击**浏览**，然后选择 **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="1b9fa-192">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-192">Click **OK**.</span></span>
5. <span data-ttu-id="1b9fa-193">检查生成的文件。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="1b9fa-194">已导入同一个文件，因为格式设计现在将“document”元素的“id”属性视为可选。</span><span class="sxs-lookup"><span data-stu-id="1b9fa-194">The same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
