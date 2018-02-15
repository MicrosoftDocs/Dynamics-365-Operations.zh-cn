---
title: "自定义字段"
description: "本主题介绍 Microsoft Dynamics 365 for Finance and Operations 如何允许用户创建自定义字段以根据业务调整应用程序。"
author: jasongre
manager: AnnBe
ms.date: 01/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: 5c66f893b0dc26b01e7c4eb024ef543f915bfe9f
ms.openlocfilehash: e272b846fba16445d3a48f9e6c33805d7b4f4d38
ms.contentlocale: zh-cn
ms.lasthandoff: 01/19/2018

---

# <a name="custom-fields"></a><span data-ttu-id="48656-103">自定义字段</span><span class="sxs-lookup"><span data-stu-id="48656-103">Custom fields</span></span>

[!include[banner](../includes/banner.md)] 

[!include[banner](../includes/pre-release.md)] 

<span data-ttu-id="48656-104">尽管 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 提供了大量的现成字段来管理各种业务流程，公司有时也需要跟踪系统中的更多信息。</span><span class="sxs-lookup"><span data-stu-id="48656-104">While Microsoft Dynamics 365 for Finance and Operations, Enterprise edition provides an extensive set of fields out-of-the-box for managing a broad range of business processes, sometimes there is a need for a company to track additional information in the system.</span></span> <span data-ttu-id="48656-105">为了满足这样的需要，Finance and Operations 允许用户创建自定义字段以根据业务调整应用程序，前提是该用户拥有此项功能的权限。</span><span class="sxs-lookup"><span data-stu-id="48656-105">To accommodate this need, Finance and Operations allows you to create custom fields to tailor the application to fit your business, provided you have permissions to the feature.</span></span>

<span data-ttu-id="48656-106">本视频体现了向页面添加自定义字段有多简单。</span><span class="sxs-lookup"><span data-stu-id="48656-106">This video shows how easy it is to add a custom field to a page.</span></span>


> [!Video https://www.youtube.com/embed/gWSGZI9Vtnc]

## <a name="creating-custom-fields"></a><span data-ttu-id="48656-107">创建自定义字段</span><span class="sxs-lookup"><span data-stu-id="48656-107">Creating custom fields</span></span>
<span data-ttu-id="48656-108">确定要在应用程序中跟踪的更多信息之后，可在相应表中创建自定义字段，并在页面中显示这个新字段。</span><span class="sxs-lookup"><span data-stu-id="48656-108">After you’ve identified additional information that you would like to track in the application, you can create the custom field on the appropriate table and expose that new field on a page.</span></span>   

<span data-ttu-id="48656-109">以下步骤介绍创建自定义字段并将该字段放到窗体中的流程。</span><span class="sxs-lookup"><span data-stu-id="48656-109">The following steps describe the process for creating a custom field and placing that field on a form.</span></span>  

1.   <span data-ttu-id="48656-110">导航到需要新字段的窗体。</span><span class="sxs-lookup"><span data-stu-id="48656-110">Navigate to the form where the new field is needed.</span></span> 
2.   <span data-ttu-id="48656-111">由于最终目标是在窗体中显示自定义字段，所以创建自定义字段的起点属于个性化体验。</span><span class="sxs-lookup"><span data-stu-id="48656-111">Because the end goal is to expose the custom field on a form, the entry point for creating custom fields exists inside the personalization experience.</span></span> <span data-ttu-id="48656-112">通过选择**选项**，然后选择**个性化设置此窗体**，打开个性化菜单栏。</span><span class="sxs-lookup"><span data-stu-id="48656-112">Open the personalization toolbar by selecting **Options**, and then **Personalize this form**.</span></span> 
3.   <span data-ttu-id="48656-113">单击**插入**，然后单击**字段**。</span><span class="sxs-lookup"><span data-stu-id="48656-113">Click **Insert** and then **Field**.</span></span>  
4.   <span data-ttu-id="48656-114">选择要显示新字段的窗体区域。</span><span class="sxs-lookup"><span data-stu-id="48656-114">Select the region of the form where you want to expose the new field.</span></span> <span data-ttu-id="48656-115">选择后，**插入字段**对话框将显示可插入所选窗体区域的现有字段的列表。</span><span class="sxs-lookup"><span data-stu-id="48656-115">After selection, the **Insert fields** dialog box will display a list of existing fields that can be inserted into the selected region of the form.</span></span>  
5.   <span data-ttu-id="48656-116">确保输入的字段未在该列表中。</span><span class="sxs-lookup"><span data-stu-id="48656-116">Ensure that the field you are interested in does not already exist in the list.</span></span> <span data-ttu-id="48656-117">否则，只需列表中选择该字段，然后单击**插入**。</span><span class="sxs-lookup"><span data-stu-id="48656-117">If it does, you can simply select that field in the list and click **Insert**.</span></span>   
6.   <span data-ttu-id="48656-118">单击 列表上方的**创建新字段**按钮开始创建自定义字段。</span><span class="sxs-lookup"><span data-stu-id="48656-118">Click the **Create new field** button above the list to initiate the process of creating a custom field.</span></span> <span data-ttu-id="48656-119">这将打开**创建新字段**对话框。</span><span class="sxs-lookup"><span data-stu-id="48656-119">This will open the **Create new field** dialog box.</span></span> 

     <span data-ttu-id="48656-120">如果未看到**创建新字段**按钮，说明您无权使用此功能。</span><span class="sxs-lookup"><span data-stu-id="48656-120">If you do not see the **Create new field** button, you do not have the necessary permissions to use this feature.</span></span>  
     
7.   <span data-ttu-id="48656-121">在**创建新字段**对话框中，输入以下信息。</span><span class="sxs-lookup"><span data-stu-id="48656-121">In the **Create new field** dialog box, enter the following information.</span></span>
     1.   <span data-ttu-id="48656-122">选择应在其中添加此字段的数据库表。</span><span class="sxs-lookup"><span data-stu-id="48656-122">Select the database table where this field should be added.</span></span> <span data-ttu-id="48656-123">请注意，此下拉列表中仅显示支持自定义字段的表。</span><span class="sxs-lookup"><span data-stu-id="48656-123">Note that only tables that support custom fields will appear in the drop-down list.</span></span> <span data-ttu-id="48656-124">有关支持的表的技术细节，请参阅下面的章节。</span><span class="sxs-lookup"><span data-stu-id="48656-124">See the section below for technical details on supported tables.</span></span>  
     2.   <span data-ttu-id="48656-125">选择新字段的数据类型。</span><span class="sxs-lookup"><span data-stu-id="48656-125">Select the data type for the new field.</span></span> <span data-ttu-id="48656-126">可用数据类型为复选框、日期、日期时间、小数、数字、选择列表和文本。</span><span class="sxs-lookup"><span data-stu-id="48656-126">The available data types are checkbox, date, date time, decimal, number, picklist, and text.</span></span>   
          - <span data-ttu-id="48656-127">如果选择文本数据类型，还可以指定此字段中可输入的最大文本长度。</span><span class="sxs-lookup"><span data-stu-id="48656-127">If you choose the text data type, you can also specify the maximum length of the text that can be entered in this field.</span></span> 
          - <span data-ttu-id="48656-128">如果选择选择列表数据类型，还可以为字段选择有效值集合。</span><span class="sxs-lookup"><span data-stu-id="48656-128">If you choose the picklist data type, you can also select the set of valid values for the field.</span></span>  
     3.   <span data-ttu-id="48656-129">为字段提供名称、标签和帮助文本。</span><span class="sxs-lookup"><span data-stu-id="48656-129">Provide a name, label, and help text for the field.</span></span> <span data-ttu-id="48656-130">此名称与数据库中的实际字段名称对应，而标签和帮助文本则是用于在用户界面中表示此字段的文本。</span><span class="sxs-lookup"><span data-stu-id="48656-130">The name corresponds to the physical field name in the database, whereas the label and help text are the text used to represent this field in the user interface.</span></span>  
8.   <span data-ttu-id="48656-131">如果这是需要为此窗体创建的唯一字段，请单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="48656-131">If this is the only field that you need to create for this form, click **Save**.</span></span> <span data-ttu-id="48656-132">如果需要创建更多字段，请单击**保存并新建**，然后返回到步骤 7。</span><span class="sxs-lookup"><span data-stu-id="48656-132">If you need to create additional fields, click **Save and new** and go back to step 7.</span></span> <span data-ttu-id="48656-133">请注意，目前存在**每个表 20 个自定义字段**这一限制。</span><span class="sxs-lookup"><span data-stu-id="48656-133">Note that there is currently a limit of **20 custom fields per table**.</span></span>
9.   <span data-ttu-id="48656-134">如果离开**创建新字段**对话框，将返回到**插入字段**对话框。</span><span class="sxs-lookup"><span data-stu-id="48656-134">Leaving the **Create new field** dialog box will return you to the **Insert fields** dialog box.</span></span> <span data-ttu-id="48656-135">刚才创建的所有自定义字段将在字段列表中自动标记为要插入窗体中。</span><span class="sxs-lookup"><span data-stu-id="48656-135">Any custom fields that were just added will be automatically marked in the field list to be inserted into the form.</span></span>  
10.   <span data-ttu-id="48656-136">单击**插入**将标记的字段插入窗体中的所选区域。</span><span class="sxs-lookup"><span data-stu-id="48656-136">Click **Insert** to insert the marked fields into the selected region of the form.</span></span> 
11.   <span data-ttu-id="48656-137">**可选：**从个性化工具栏启用**移动**模式，以便将新字段移动到所选区域中的所需位置。</span><span class="sxs-lookup"><span data-stu-id="48656-137">**Optional:** Enable **Move** mode from the personalization toolbar to move the new fields to their desired location in the selected region.</span></span> <span data-ttu-id="48656-138">有关如何使用各种个性化功能针对个人使用优化窗体的详细信息，请参阅[打造个性化的用户体验](personalize-user-experience.md)。</span><span class="sxs-lookup"><span data-stu-id="48656-138">See [Personalize the user experience](personalize-user-experience.md) for more information about how to use the various personalization capabilities to optimize a form for your personal usage.</span></span>  

### <a name="sharing-custom-fields-with-other-users"></a><span data-ttu-id="48656-139">与其他用户共享自定义字段</span><span class="sxs-lookup"><span data-stu-id="48656-139">Sharing custom fields with other users</span></span>
<span data-ttu-id="48656-140">创建自定义字段并在窗体中显示之后，可能需要将这个更新后的页面视图（包括新字段）共享给系统中的其他用户。</span><span class="sxs-lookup"><span data-stu-id="48656-140">After you have created a custom field and exposed it on a form, you might want to provide this updated page view that includes the new field to other users in the system.</span></span> <span data-ttu-id="48656-141">可使用本产品的个性化功能以两种不同的方法达到此目的：</span><span class="sxs-lookup"><span data-stu-id="48656-141">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

-   <span data-ttu-id="48656-142">建议的方法是通过系统管理员，因为系统管理员可以将个性化设置推送给所有用户或一小部分用户。</span><span class="sxs-lookup"><span data-stu-id="48656-142">The recommended route is through the system administrator, who can push a personalization to all users or a subset of users.</span></span> <span data-ttu-id="48656-143">有关更多详细信息，请参阅[打造个性化的用户体验](personalize-user-experience.md)。</span><span class="sxs-lookup"><span data-stu-id="48656-143">See [Personalize the user experience](personalize-user-experience.md) for more details.</span></span> 

-   <span data-ttu-id="48656-144">也可以导出更改（称为*个性化设置*），将其发送给一位或多位用户，然后请这些用户分别导入您的更改。</span><span class="sxs-lookup"><span data-stu-id="48656-144">Alternatively, you can export your changes (called *personalizations*), send them to one or more users, and have each of those users import your changes.</span></span> <span data-ttu-id="48656-145">可使用个性化工具栏上的**管理**选项导出和导入个性化设置。</span><span class="sxs-lookup"><span data-stu-id="48656-145">The **Manage** option on the personalization toolbar enables you to export and import personalizations.</span></span>

## <a name="managing-custom-fields"></a><span data-ttu-id="48656-146">管理自定义字段</span><span class="sxs-lookup"><span data-stu-id="48656-146">Managing custom fields</span></span>

<span data-ttu-id="48656-147">可通过“系统管理”模块中的**自定义字段**页面管理系统中的所有自定义字段。</span><span class="sxs-lookup"><span data-stu-id="48656-147">Management of all the custom fields in the system can be accomplished through the **Custom fields** page in the System administration module.</span></span>  <span data-ttu-id="48656-148">用户可通过此页面访问大量功能，包括：</span><span class="sxs-lookup"><span data-stu-id="48656-148">This page allows users access to many capabilities, including:</span></span> 
-   <span data-ttu-id="48656-149">查看系统中的所有自定义字段的列表。</span><span class="sxs-lookup"><span data-stu-id="48656-149">Viewing a list of all custom fields in the system.</span></span>
-   <span data-ttu-id="48656-150">对现有自定义字段进行有限编辑。</span><span class="sxs-lookup"><span data-stu-id="48656-150">Limited editing of existing custom fields.</span></span>
-   <span data-ttu-id="48656-151">删除自定义字段。</span><span class="sxs-lookup"><span data-stu-id="48656-151">Deleting custom fields.</span></span>
-   <span data-ttu-id="48656-152">在数据实体上显示自定义字段。</span><span class="sxs-lookup"><span data-stu-id="48656-152">Exposing custom fields on data entities.</span></span>
-   <span data-ttu-id="48656-153">提供自定义字段标签和帮助文本的翻译。</span><span class="sxs-lookup"><span data-stu-id="48656-153">Providing translations of custom field labels and help text.</span></span>

### <a name="viewing-all-custom-fields"></a><span data-ttu-id="48656-154">查看所有自定义字段</span><span class="sxs-lookup"><span data-stu-id="48656-154">Viewing all custom fields</span></span>
<span data-ttu-id="48656-155">**自定义字段**页面提供系统中已定义的所有自定义字段的可视性。</span><span class="sxs-lookup"><span data-stu-id="48656-155">The **Custom fields** page provides visibility to all the custom fields that have been defined in the system.</span></span> <span data-ttu-id="48656-156">只需选择您感兴趣的表，之后页面将更新以显示与该表关联的自定义字段的列表。</span><span class="sxs-lookup"><span data-stu-id="48656-156">Simply select the table that you are interested in, and the page will update to show a list of the custom fields associated with that table.</span></span> <span data-ttu-id="48656-157">可通过从列表中选择自定义字段查看有关该字段的所有详细信息。</span><span class="sxs-lookup"><span data-stu-id="48656-157">Choosing a custom field from the list will allow you to view all the details about the field.</span></span>

### <a name="editing-custom-fields"></a><span data-ttu-id="48656-158">编辑自定义字段</span><span class="sxs-lookup"><span data-stu-id="48656-158">Editing custom fields</span></span>
<span data-ttu-id="48656-159">创建自定义字段之后，**自定义字段**页面中只能修改有关该自定义字段的特定信息段。</span><span class="sxs-lookup"><span data-stu-id="48656-159">After a custom field has been created, only certain pieces of information about the custom field can be modified on the **Custom fields** page.</span></span>   

<span data-ttu-id="48656-160">*可以*修改以下属性：</span><span class="sxs-lookup"><span data-stu-id="48656-160">You *can* modify these attributes:</span></span> 
-   <span data-ttu-id="48656-161">标签</span><span class="sxs-lookup"><span data-stu-id="48656-161">Label</span></span> 
-   <span data-ttu-id="48656-162">帮助文本</span><span class="sxs-lookup"><span data-stu-id="48656-162">Help text</span></span>
-   <span data-ttu-id="48656-163">文本字段的长度</span><span class="sxs-lookup"><span data-stu-id="48656-163">Length, for Text fields</span></span>

<span data-ttu-id="48656-164">*不能*编辑以下属性：</span><span class="sxs-lookup"><span data-stu-id="48656-164">You *cannot* edit the following attributes:</span></span> 
-   <span data-ttu-id="48656-165">字段名称</span><span class="sxs-lookup"><span data-stu-id="48656-165">Field name</span></span>
-   <span data-ttu-id="48656-166">数据类型</span><span class="sxs-lookup"><span data-stu-id="48656-166">Data type</span></span>

<span data-ttu-id="48656-167">此外，对于选择列表字段，可为自定义字段的有效值集排序，但是，不能移除选择列表字段的现有值。</span><span class="sxs-lookup"><span data-stu-id="48656-167">Additionally, for picklist fields, the set of valid values for the custom field can be reordered, and new values can be added; however, existing values for the picklist field cannot be removed.</span></span> <span data-ttu-id="48656-168">编辑完特定表的字段后，请务必单击**应用更改**，以便保存更改。</span><span class="sxs-lookup"><span data-stu-id="48656-168">Remember to click **Apply changes** when you are done editing fields for a particular table so the changes are saved.</span></span> 

### <a name="exposing-custom-fields-on-data-entities"></a><span data-ttu-id="48656-169">在数据实体上显示自定义字段</span><span class="sxs-lookup"><span data-stu-id="48656-169">Exposing custom fields on data entities</span></span>
<span data-ttu-id="48656-170">允许自定义字段在数据实体上显示也可能同样重要。</span><span class="sxs-lookup"><span data-stu-id="48656-170">It may also be important to allow custom fields to be visible on data entities.</span></span> <span data-ttu-id="48656-171">数据实体用于[在 Office 中打开](../../dev-itpro/office-integration/office-integration.md)功能中，也用于数据导出/导入场景。</span><span class="sxs-lookup"><span data-stu-id="48656-171">Data entities are utilized in the [Open in Office](../../dev-itpro/office-integration/office-integration.md) feature, as well as for data import/export scenarios.</span></span>  

<span data-ttu-id="48656-172">请按照以下步骤在数据实体上显示自定义字段：</span><span class="sxs-lookup"><span data-stu-id="48656-172">Follow these steps to expose a custom field on a data entity:</span></span> 
1.   <span data-ttu-id="48656-173">在**自定义字段**窗体中选择自定义字段。</span><span class="sxs-lookup"><span data-stu-id="48656-173">Select the custom field on the **Custom fields** form.</span></span> 
2.   <span data-ttu-id="48656-174">展开**实体**部分查看相关实体集。</span><span class="sxs-lookup"><span data-stu-id="48656-174">Expand the **Entities** section to view the set of relevant entities.</span></span>  
3.   <span data-ttu-id="48656-175">单击**编辑**按钮。</span><span class="sxs-lookup"><span data-stu-id="48656-175">Click the **Edit** button.</span></span>
4.   <span data-ttu-id="48656-176">修改要为应显示此字段的各实体选择的**已启用**字段。</span><span class="sxs-lookup"><span data-stu-id="48656-176">Modify the **Enabled** field to be selected for each entity that should expose this field.</span></span>  
5.   <span data-ttu-id="48656-177">单击**应用更改**以保存您的选择。</span><span class="sxs-lookup"><span data-stu-id="48656-177">Click **Apply changes** to save your selections.</span></span>  

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a><span data-ttu-id="48656-178">允许自定义字段以其他语言显示</span><span class="sxs-lookup"><span data-stu-id="48656-178">Allowing custom fields to be displayed in other languages</span></span>
<span data-ttu-id="48656-179">因为用户可能需要使用各种语言访问自定义字段，所以**自定义字段**页面提供了一种机制来将自定义字段的标签和帮助文本翻译为其他语言。</span><span class="sxs-lookup"><span data-stu-id="48656-179">Because custom fields may need to be accessed by users in a variety of languages, the **Custom fields** page provides a mechanism to allow the label and help text for a custom field to be translated into other languages.</span></span>  

<span data-ttu-id="48656-180">以下步骤介绍将自定义字段翻译为其他语言的流程：</span><span class="sxs-lookup"><span data-stu-id="48656-180">The following steps describe the process for translating custom fields in other languages:</span></span> 
1.   <span data-ttu-id="48656-181">在**自定义字段**页面中选择自定义字段。</span><span class="sxs-lookup"><span data-stu-id="48656-181">Select the custom field on the **Custom fields** page.</span></span> 
2.   <span data-ttu-id="48656-182">选择操作窗格上的**翻译**按钮。</span><span class="sxs-lookup"><span data-stu-id="48656-182">Select the **Translations** button in the Action Pane.</span></span> <span data-ttu-id="48656-183">这将打开一个下拉菜单，其中包含该字段的现有翻译。</span><span class="sxs-lookup"><span data-stu-id="48656-183">This will open a drop-down menu with existing translations for this field.</span></span>
3.   <span data-ttu-id="48656-184">**语言**下拉菜单显示已提供了其翻译的语言的集合。</span><span class="sxs-lookup"><span data-stu-id="48656-184">The **Language** drop-down menu shows the set of languages for which translations have already been provided.</span></span> 
     1.   <span data-ttu-id="48656-185">如果要编辑现有翻译，请从菜单中选择所需语言，然后修改标签和帮助文本的值。</span><span class="sxs-lookup"><span data-stu-id="48656-185">If you want to edit an existing translation, select the desired language from the menu and modify the values for the label and help text.</span></span>  
     2.   <span data-ttu-id="48656-186">否则，单击**添加语言**按钮，从菜单中选择所需语言，然后为标签和帮助文本提供翻译后的值。</span><span class="sxs-lookup"><span data-stu-id="48656-186">Otherwise, click the **Add language** button, select the desired language from the menu, and then provide translated values for the label and help text.</span></span>  
4.   <span data-ttu-id="48656-187">完成后，单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="48656-187">Click **OK** when you are finished.</span></span>  

### <a name="deleting-custom-fields"></a><span data-ttu-id="48656-188">删除自定义字段</span><span class="sxs-lookup"><span data-stu-id="48656-188">Deleting custom fields</span></span>
<span data-ttu-id="48656-189">在很少见的情况下，您可能认为不再需要某个自定义字段。</span><span class="sxs-lookup"><span data-stu-id="48656-189">In some rare cases, you may decide that a custom field is no longer needed.</span></span> <span data-ttu-id="48656-190">在发生此情况时，系统管理员可以选择从**自定义字段**页面删除该字段。</span><span class="sxs-lookup"><span data-stu-id="48656-190">When this occurs, a system administrator can choose to delete the field from the **Custom fields** page.</span></span> <span data-ttu-id="48656-191">方法是，确保已选中正确字段，单击**删除**，单击**是**确认删除，最后单击**应用更改**。</span><span class="sxs-lookup"><span data-stu-id="48656-191">To do this, ensure the correct field is selected, click **Delete**, click **Yes** to confirm the deletion, and finally click **Apply changes**.</span></span> 

> [!Note]
> <span data-ttu-id="48656-192">此操作无法撤消，将导致从数据库永久删除与该字段关联的数据。</span><span class="sxs-lookup"><span data-stu-id="48656-192">This action cannot be undone, and will result in the data associated with the field being permanently deleted from the database.</span></span> 

## <a name="appendix"></a><span data-ttu-id="48656-193">附录</span><span class="sxs-lookup"><span data-stu-id="48656-193">Appendix</span></span> 
### <a name="who-can-create-custom-fields"></a><span data-ttu-id="48656-194">谁可以创建自定义字段？</span><span class="sxs-lookup"><span data-stu-id="48656-194">Who can create custom fields?</span></span>
<span data-ttu-id="48656-195">默认情况下，只有系统管理员这样的系统安全卫士才能创建自定义字段。</span><span class="sxs-lookup"><span data-stu-id="48656-195">As a safeguard to the system, only system administrators are able to create custom fields by default.</span></span> <span data-ttu-id="48656-196">但是，系统管理员可使用**运行时自定义高级用户**安全角色为组织认为有必要拥有创建自定义字段的权限的高级用户提供该权限。</span><span class="sxs-lookup"><span data-stu-id="48656-196">However, those power users whom the organization deems necessary can be given rights to create custom fields by a system administrator using the **Runtime customization power user** security role.</span></span> <span data-ttu-id="48656-197">不具有此安全角色的用户不能创建自定义字段，但是仍然可以查看系统中其他用户添加的自定义字段和与之交互。</span><span class="sxs-lookup"><span data-stu-id="48656-197">Users without this security role will not be able to create custom fields, but will still be able to see and interact with custom fields added by other users in the system.</span></span>    

### <a name="what-tables-support-custom-fields"></a><span data-ttu-id="48656-198">哪些表支持自定义字段？</span><span class="sxs-lookup"><span data-stu-id="48656-198">What tables support custom fields?</span></span>
<span data-ttu-id="48656-199">出于性能和技术原因，现在只有满足以下条件的表才允许添加自定义字段。</span><span class="sxs-lookup"><span data-stu-id="48656-199">For performance and technical reasons, only tables that meet the following conditions currently allow custom fields to be added.</span></span>

- <span data-ttu-id="48656-200">表必须标记为以下组之一：</span><span class="sxs-lookup"><span data-stu-id="48656-200">The table must be tagged as one of these groups:</span></span> 
     -   <span data-ttu-id="48656-201">组合</span><span class="sxs-lookup"><span data-stu-id="48656-201">Group</span></span>
     -   <span data-ttu-id="48656-202">WorksheetHeader</span><span class="sxs-lookup"><span data-stu-id="48656-202">WorksheetHeader</span></span>
     -   <span data-ttu-id="48656-203">主要</span><span class="sxs-lookup"><span data-stu-id="48656-203">Main</span></span>
     -   <span data-ttu-id="48656-204">杂项</span><span class="sxs-lookup"><span data-stu-id="48656-204">Miscellaneous</span></span>
     -   <span data-ttu-id="48656-205">参数</span><span class="sxs-lookup"><span data-stu-id="48656-205">Parameter</span></span>
     -   <span data-ttu-id="48656-206">参考</span><span class="sxs-lookup"><span data-stu-id="48656-206">Reference</span></span>
     -   <span data-ttu-id="48656-207">TransactionHeader</span><span class="sxs-lookup"><span data-stu-id="48656-207">TransactionHeader</span></span>
- <span data-ttu-id="48656-208">表不能扩展其他表。</span><span class="sxs-lookup"><span data-stu-id="48656-208">The table cannot not extend another table.</span></span>
- <span data-ttu-id="48656-209">表不能标记为系统表。</span><span class="sxs-lookup"><span data-stu-id="48656-209">The table cannot be marked as a system table.</span></span>
- <span data-ttu-id="48656-210">表不能为临时表。</span><span class="sxs-lookup"><span data-stu-id="48656-210">The table cannot be a temporary table.</span></span>

