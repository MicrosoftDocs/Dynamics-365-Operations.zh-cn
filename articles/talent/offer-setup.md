---
title: 设置聘约管理
description: 此主题描述如何在 Talent 中设置聘约。
author: josaw
manager: AnnBe
ms.date: 02/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43cf13d96e345747e06541267d820e17de7c1763
ms.sourcegitcommit: ea17d2e35c24a141c20ab429897eebf9fa186f61
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/26/2019
ms.locfileid: "768874"
---
# <a name="set-up-offer-management"></a><span data-ttu-id="7861c-103">设置聘约管理</span><span class="sxs-lookup"><span data-stu-id="7861c-103">Set up offer management</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="7861c-104">在应聘者移到 Dynamics 365 for Talent: Attract 中的聘约的阶段时，您需要确保可以为应聘者快速创建聘约，根据需要审核，并发送给应聘者。</span><span class="sxs-lookup"><span data-stu-id="7861c-104">When a candidate is moved to the offer stage in Dynamics 365 for Talent: Attract, you need to ensure that the offers can be quickly created for the candidate, approved as necessary, and sent out to the candidate.</span></span> <span data-ttu-id="7861c-105">因为大多数聘约是标准的，因此可以从可重复使用的模板创建。</span><span class="sxs-lookup"><span data-stu-id="7861c-105">Because most offers are standard, they can be created from reusable templates.</span></span> <span data-ttu-id="7861c-106">在 Attract 中，所有聘约都汇总到一个聘约包，这是一个或多个聘约文档的集合。</span><span class="sxs-lookup"><span data-stu-id="7861c-106">In Attract, all offers are rolled into an offer package, which is a collection of one or more offer documents.</span></span> 

<span data-ttu-id="7861c-107">此主题列出了 Attract 管理员将遵循来设置不同聘约包模板的所有步骤，在 Attract 中这是聘约管理功能的一部分。</span><span class="sxs-lookup"><span data-stu-id="7861c-107">This topic lists all the steps that an Attract administrator would follow to set up different offer package templates as part of the offer management capability in Attract.</span></span> <span data-ttu-id="7861c-108">具有非管理员角色的用户不能访问这些功能。</span><span class="sxs-lookup"><span data-stu-id="7861c-108">Users with non-administrator roles will not have access to these capabilities.</span></span>

>[!NOTE]
> <span data-ttu-id="7861c-109">聘约管理功能作为综合招聘附件的一部分提供。</span><span class="sxs-lookup"><span data-stu-id="7861c-109">Offer management capabilities are available as part of the Comprehensive Hiring Add-On.</span></span>

## <a name="offer-data"></a><span data-ttu-id="7861c-110">聘约数据</span><span class="sxs-lookup"><span data-stu-id="7861c-110">Offer data</span></span> 

<span data-ttu-id="7861c-111">聘约数据在聘约包模板内是最小单位。</span><span class="sxs-lookup"><span data-stu-id="7861c-111">Offer data is the smallest unit inside the offer package template.</span></span> <span data-ttu-id="7861c-112">典型的聘约包括标准文本和一组值。</span><span class="sxs-lookup"><span data-stu-id="7861c-112">A typical offer consists of standard text and a set of values.</span></span> <span data-ttu-id="7861c-113">这些值是可以在聘约之间更改的唯一部分。</span><span class="sxs-lookup"><span data-stu-id="7861c-113">The sets of values are the only pieces that could change between offers.</span></span> <span data-ttu-id="7861c-114">在聘约创建期间，聘约创建者可以关注的最重要方面是在聘约包模板中显示的聘约数据占位符的列表。</span><span class="sxs-lookup"><span data-stu-id="7861c-114">During the offer creation, the most important aspect that the offer creator can focus on is the list of offer data placeholders present in an offer package template.</span></span> <span data-ttu-id="7861c-115">若要设置聘约数据，请执行以下操作。</span><span class="sxs-lookup"><span data-stu-id="7861c-115">To set up offer data, do the following.</span></span>

1.  <span data-ttu-id="7861c-116">转到**聘约管理**。</span><span class="sxs-lookup"><span data-stu-id="7861c-116">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="7861c-117">在左侧导航窗格中展开**库**部分，然后转到**聘约数据**。</span><span class="sxs-lookup"><span data-stu-id="7861c-117">Expand the **Library** section in the left navigation pane, then go to **Offer data**.</span></span>

    >[!NOTE]
    > <span data-ttu-id="7861c-118">**聘约数据**页上是**应聘者详细信息**和**工作详细信息**部分。</span><span class="sxs-lookup"><span data-stu-id="7861c-118">On the **Offer data** page are the **Candidate details** and **Job details** sections.</span></span> <span data-ttu-id="7861c-119">Attract 提供一些现成的聘约数据占位符。</span><span class="sxs-lookup"><span data-stu-id="7861c-119">Attract provides a few offer data placeholders out-of-the-box.</span></span>
    
    > <span data-ttu-id="7861c-120">此页面有一些部分可用于连同逻辑组中的占位符一起管理不同的聘约数据占位符。</span><span class="sxs-lookup"><span data-stu-id="7861c-120">There are sections on the page to organize different offer data placeholders together in logical groups.</span></span> <span data-ttu-id="7861c-121">这些部分可以帮助在聘约创建流程期间维护聘约数据和填充数据。</span><span class="sxs-lookup"><span data-stu-id="7861c-121">These sections can help with maintenance of offer data and population of data during the offer creation process.</span></span>

1.  <span data-ttu-id="7861c-122">若要创建新的聘约数据部分，单击**添加部分**并为部分输入一个唯一名称。</span><span class="sxs-lookup"><span data-stu-id="7861c-122">To create a new offer data section, click **Add a section** and enter a unique name for the section.</span></span>

1.  <span data-ttu-id="7861c-123">若要向任何部分添加聘约数据占位符，请单击**添加聘约数据**并为占位符输入一个唯一名称。</span><span class="sxs-lookup"><span data-stu-id="7861c-123">To add offer data placeholders to any section, click **Add offer data** and enter a unique name for the placeholder.</span></span>

1.  <span data-ttu-id="7861c-124">若要编辑任何部分人名称，悬停在部分名称上，然后更新名称。</span><span class="sxs-lookup"><span data-stu-id="7861c-124">To edit the name of any section, hover over the section name and update the name.</span></span>

1.  <span data-ttu-id="7861c-125">若要编辑任何现有聘约数据占位符的名称，请首先确保该占位符不属于任何模板。</span><span class="sxs-lookup"><span data-stu-id="7861c-125">To edit the name of any existing offer data placeholder, first make sure that the placeholder is not already part of any template.</span></span> <span data-ttu-id="7861c-126">然后，悬停在聘约数据占位符的名称上，根据需要更新名称。</span><span class="sxs-lookup"><span data-stu-id="7861c-126">Then, hover over the name of the offer data placeholder and update the name as needed.</span></span>

1. <span data-ttu-id="7861c-127">若要删除现有的聘约数据占位符，请首先确保该占位符不属于任何其他模板。</span><span class="sxs-lookup"><span data-stu-id="7861c-127">To delete an existing offer data placeholder, first make sure that the placeholder is not part of any other template.</span></span> <span data-ttu-id="7861c-128">然后，悬停在占位符上，在垃圾桶图标显示时，单击垃圾桶删除聘约数据占位符。</span><span class="sxs-lookup"><span data-stu-id="7861c-128">Then, hover over the placeholder and when the trash can icon appears, click the trash can to delete the offer data placeholder.</span></span>
    >[!NOTE]
    > <span data-ttu-id="7861c-129">您可以通过每个聘约数据旁边的数值指示符查看聘约数据占位符属于多少个模板。</span><span class="sxs-lookup"><span data-stu-id="7861c-129">You can see how many templates an offer data placeholder is part of by the number indicator next to each offer data.</span></span> 

1. <span data-ttu-id="7861c-130">若要删除任何部分，请悬停在名称上。</span><span class="sxs-lookup"><span data-stu-id="7861c-130">To delete any section, hover over the name.</span></span> <span data-ttu-id="7861c-131">如果部分内没有聘约数据占位符出现在任何模板中，您可以单击垃圾桶图标删除它。</span><span class="sxs-lookup"><span data-stu-id="7861c-131">If none of the offer data placeholders inside the section appear in any template, you can click the trash can icon to delete it.</span></span> 
    >[!NOTE]
    > <span data-ttu-id="7861c-132">删除部分还将删除该部分内的所有聘约数据占位符。</span><span class="sxs-lookup"><span data-stu-id="7861c-132">Deleting the section will also delete all the offer data placeholders inside that section.</span></span>

<span data-ttu-id="7861c-133">在聘约数据占位符设置后，您可以在任何文档模板中使用它们。</span><span class="sxs-lookup"><span data-stu-id="7861c-133">After the offer data placeholders have been set up, you can use them across any document template.</span></span> <span data-ttu-id="7861c-134">聘约数据占位符不限制特定模板 -- 同一个集可以跨所有模板使用。</span><span class="sxs-lookup"><span data-stu-id="7861c-134">Offer data placeholders are not restricted to a specific template -- the same set can be used across all templates.</span></span>

## <a name="offer-data-rules"></a><span data-ttu-id="7861c-135">聘约数据规则</span><span class="sxs-lookup"><span data-stu-id="7861c-135">Offer data rules</span></span>

<span data-ttu-id="7861c-136">多数组织具有聘约创建必须遵守的规则。</span><span class="sxs-lookup"><span data-stu-id="7861c-136">Most organization have rules for how offers must be created.</span></span> <span data-ttu-id="7861c-137">例如，组织可能要求特定位置和资历级别组合的最大年薪聘约必须在某个范围内，或者新雇员的聘约级别只能使用一些特定的值。</span><span class="sxs-lookup"><span data-stu-id="7861c-137">For example, an organization may want to require that the maximum annual salary offer for a specific location and seniority level combination has to be within a certain range, or that there are only a few specific values possible for the offer level for the new hire.</span></span> <span data-ttu-id="7861c-138">Attract 当前支持使用 CSV 文件的所有此类数据规则。</span><span class="sxs-lookup"><span data-stu-id="7861c-138">Attract currently supports all such data rules using a CSV file.</span></span>

<span data-ttu-id="7861c-139">若要准备数据规则 CSV 文件，请执行以下操作。</span><span class="sxs-lookup"><span data-stu-id="7861c-139">To prepare the data rules CSV file, do the following.</span></span>

1.  <span data-ttu-id="7861c-140">确定规则集的聘约数据占位符。</span><span class="sxs-lookup"><span data-stu-id="7861c-140">Determine the offer data placeholder for the rule set.</span></span> <span data-ttu-id="7861c-141">例如，**年薪**。</span><span class="sxs-lookup"><span data-stu-id="7861c-141">For example, **Annual Salary**.</span></span>

1.  <span data-ttu-id="7861c-142">确定相关的聘约数据占位符值。</span><span class="sxs-lookup"><span data-stu-id="7861c-142">Identify the dependent offer data placeholder values.</span></span> <span data-ttu-id="7861c-143">例如，**工作地点**和**级别**。</span><span class="sxs-lookup"><span data-stu-id="7861c-143">For example, **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="7861c-144">指定列 1 和 2 为**工作地点**和**级别**。</span><span class="sxs-lookup"><span data-stu-id="7861c-144">Specify columns 1 and 2 as **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="7861c-145">要上载范围值，将列 3 和 4 作为**年薪**。</span><span class="sxs-lookup"><span data-stu-id="7861c-145">To upload a range value, make columns 3 and 4 **Annual Salary**.</span></span> <span data-ttu-id="7861c-146">要上载特定值而不是范围，仅将列 3 作为**年薪**。</span><span class="sxs-lookup"><span data-stu-id="7861c-146">To upload a specific value instead of a range, only make column 3 **Annual Salary**.</span></span>

1.  <span data-ttu-id="7861c-147">根据您需要的角色填充 Microsoft Excel 文件。</span><span class="sxs-lookup"><span data-stu-id="7861c-147">Populate the Microsoft Excel file based on your required roles.</span></span>

1.  <span data-ttu-id="7861c-148">确保每一行都是放在一起的所有值的唯一组合。</span><span class="sxs-lookup"><span data-stu-id="7861c-148">Ensure that each row is a unique combination of all the values put together.</span></span>

1.  <span data-ttu-id="7861c-149">将文件保存为 CSV 格式。</span><span class="sxs-lookup"><span data-stu-id="7861c-149">Save the file as a CSV format.</span></span>

<span data-ttu-id="7861c-150">若要上载聘约数据规则文件，请执行以下操作。</span><span class="sxs-lookup"><span data-stu-id="7861c-150">To upload the offer data rules file, do the following.</span></span>

1.  <span data-ttu-id="7861c-151">转到**聘约管理**。</span><span class="sxs-lookup"><span data-stu-id="7861c-151">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="7861c-152">在左侧导航面板中展开**库**部分，然后转到**聘约数据规则**。</span><span class="sxs-lookup"><span data-stu-id="7861c-152">Expand the **Library** section in the left navigation panel, then go to **Offer data rules**.</span></span>

1.  <span data-ttu-id="7861c-153">单击**新建数据集**显示**上载**对话框。</span><span class="sxs-lookup"><span data-stu-id="7861c-153">Click **New data set** to display the **Upload** dialog box.</span></span>

1.  <span data-ttu-id="7861c-154">为规则集指定唯一名称，然后上载保存的 CSV 文件。</span><span class="sxs-lookup"><span data-stu-id="7861c-154">Specify a unique name for the rule set and then upload the saved CSV file.</span></span>

1.  <span data-ttu-id="7861c-155">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="7861c-155">Click **Add**.</span></span>
    <span data-ttu-id="7861c-156">规则集将在后台处理，完成后，您将在应用内或通过电子邮件收到通知。</span><span class="sxs-lookup"><span data-stu-id="7861c-156">The rule set will be processed in the background and you will be notified in-app and via email once it completes.</span></span>

    <span data-ttu-id="7861c-157">如果在处理上载时出错，您将收到通知。</span><span class="sxs-lookup"><span data-stu-id="7861c-157">You will be notified if there are errors while processing the upload.</span></span> <span data-ttu-id="7861c-158">然后，您可以下载错误日志，修复文件并将其重新上载。</span><span class="sxs-lookup"><span data-stu-id="7861c-158">You can then download the error log, fix the file, and upload it again.</span></span>

1.  <span data-ttu-id="7861c-159">如果您想要下载规则集并更新该组值，请使用省略号按钮 (**…**) 选项。</span><span class="sxs-lookup"><span data-stu-id="7861c-159">Use the ellipses button (**…**) option if you want to download the rule set and update the set of values.</span></span> <span data-ttu-id="7861c-160">在更新后，您可以再次上载文件。</span><span class="sxs-lookup"><span data-stu-id="7861c-160">After updating, you can upload the file again.</span></span>

1.  <span data-ttu-id="7861c-161">如何定义的占位符未在其他文档模板中使用，您可以删除现有的规则集上载。</span><span class="sxs-lookup"><span data-stu-id="7861c-161">You can delete an existing rule set upload if the placeholder being defined is not being used in another document template.</span></span>

>[!NOTE]
> - <span data-ttu-id="7861c-162">每个占位符只能具有与之相关的一组唯一列。</span><span class="sxs-lookup"><span data-stu-id="7861c-162">Each placeholder can only have one unique set of columns that it is dependent on.</span></span> <span data-ttu-id="7861c-163">例如，如果**年薪**与**工作地点**和**级别**相关，您则不能上载**年薪**与一组其他列相关的其他规则集。</span><span class="sxs-lookup"><span data-stu-id="7861c-163">For example, if **Annual Salary** is dependent on **Job Location** and **Level**, you can't upload another rule set where **Annual Salary** is dependent on a different set of columns.</span></span>

> - <span data-ttu-id="7861c-164">您可以在**聘约数据规则**页的**示例**选项卡下载示例聘约数据规则集。</span><span class="sxs-lookup"><span data-stu-id="7861c-164">You can download sample offer data rule sets on the **Samples** tab on the **Offer data rules** page.</span></span>

> - <span data-ttu-id="7861c-165">当聘约创建者覆盖聘约数据规则推荐的值时，聘约将被标记为非标准，并强制执行聘约审核工作流。</span><span class="sxs-lookup"><span data-stu-id="7861c-165">When an offer creator overrides the values that are recommended by the offer data rules, the offer is flagged as non-standard and offer approval workflow will be mandated.</span></span>

## <a name="document-templates"></a><span data-ttu-id="7861c-166">文档模板</span><span class="sxs-lookup"><span data-stu-id="7861c-166">Document templates</span></span>

<span data-ttu-id="7861c-167">聘约文档模板可以帮助管理员创建录用信。</span><span class="sxs-lookup"><span data-stu-id="7861c-167">An offer document template can help administrators create offer letters.</span></span> <span data-ttu-id="7861c-168">聘约文档模板是作为聘约一部分的文本和定义的聘约数据占位符的组合。</span><span class="sxs-lookup"><span data-stu-id="7861c-168">The offer document template is a combination of the text that will be part of the offer as well as the defined offer data placeholders.</span></span> 

<span data-ttu-id="7861c-169">若要创建聘约文档模板，请执行以下操作。</span><span class="sxs-lookup"><span data-stu-id="7861c-169">To create an offer document template, do the following.</span></span>

1.  <span data-ttu-id="7861c-170">转到**聘约管理**。</span><span class="sxs-lookup"><span data-stu-id="7861c-170">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="7861c-171">在左侧导航窗格中展开**库**部分并转到**模板**。</span><span class="sxs-lookup"><span data-stu-id="7861c-171">Expand the **Library** section in the left navigation pane and go to **Templates**.</span></span>

    <span data-ttu-id="7861c-172">**模板**页将显示已定义的文档模板的列表。</span><span class="sxs-lookup"><span data-stu-id="7861c-172">The **Templates** page will display a list of document templates that have already been defined.</span></span>

1.  <span data-ttu-id="7861c-173">若要创建新的文档模板，单击**新建模板**。</span><span class="sxs-lookup"><span data-stu-id="7861c-173">To create a new document template, click **New Template**.</span></span>

1.  <span data-ttu-id="7861c-174">为模板输入一个唯一名称，然后单击**创建**。</span><span class="sxs-lookup"><span data-stu-id="7861c-174">Enter a unique name for the template and click **Create**.</span></span>

1.  <span data-ttu-id="7861c-175">使用富文本编辑器插入或编辑聘约文档内容。</span><span class="sxs-lookup"><span data-stu-id="7861c-175">Use the rich text editor to insert or edit the offer document content.</span></span> <span data-ttu-id="7861c-176">您可以使用文本编辑器顶部提供的选项插入表、图像和超链接。</span><span class="sxs-lookup"><span data-stu-id="7861c-176">You can insert tables, images, and hyperlinks using the options available at the top of the text editor.</span></span>

1.  <span data-ttu-id="7861c-177">您可以使用以下方法在聘约模板文档中插入聘约数据占位符：</span><span class="sxs-lookup"><span data-stu-id="7861c-177">You can insert offer data placeholders in the offer template document by:</span></span>

    - <span data-ttu-id="7861c-178">从右窗格拖放。</span><span class="sxs-lookup"><span data-stu-id="7861c-178">Dragging and dropping from the right pane.</span></span>

    - <span data-ttu-id="7861c-179">直接在职位中为聘约数据占位符创建标签。</span><span class="sxs-lookup"><span data-stu-id="7861c-179">Hashtag the offer data placeholder directly into position.</span></span> <span data-ttu-id="7861c-180">键入 **\#**，然后开始键入聘约数据占位符的名称。</span><span class="sxs-lookup"><span data-stu-id="7861c-180">Type **\#** and then start typing the name of the offer data placeholder.</span></span> <span data-ttu-id="7861c-181">选项将在下拉列表中显示。</span><span class="sxs-lookup"><span data-stu-id="7861c-181">Options will appear in the drop-down list.</span></span> <span data-ttu-id="7861c-182">单击或按 **Enter** 插入聘约数据占位符。</span><span class="sxs-lookup"><span data-stu-id="7861c-182">Click or press **Enter** to insert the offer data placeholder.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="7861c-183">若要将占位符与聘约文档模板关联而不向应聘者公开其值，悬停在聘约数据占位符上并单击**锁定**图标。</span><span class="sxs-lookup"><span data-stu-id="7861c-183">To associate a placeholder to the offer document template without exposing its value to the candidate, hover over the offer data placeholder and click the **Pin** icon.</span></span> <span data-ttu-id="7861c-184">这会将占位符推送到聘约文档模板的**锁定的聘约数据**部分。</span><span class="sxs-lookup"><span data-stu-id="7861c-184">This will push the placeholder to the **Pinned offer data** section of the offer document template.</span></span> <span data-ttu-id="7861c-185">若要解锁，请遵循相同的步骤，但在聘约数据占位符的列表中单击**解锁**。</span><span class="sxs-lookup"><span data-stu-id="7861c-185">To unpin, follow the same steps but click **Unpin** in the list of offer data placeholders.</span></span>

    > - <span data-ttu-id="7861c-186">若要查看可用聘约数据占位符的列表，请切换到右窗格的**可用**选项卡。</span><span class="sxs-lookup"><span data-stu-id="7861c-186">To view the list of active offer data placeholders, switch to the **Active** tab in the right pane.</span></span>

    > - <span data-ttu-id="7861c-187">如果您插入聘约数据规则集驱动的占位符，您可以看到该聘约数据占位符在其他值中的相关性。</span><span class="sxs-lookup"><span data-stu-id="7861c-187">If you insert a placeholder that is driven by an offer data rule set, you can see the dependency of that offer data placeholder on other values.</span></span>

    > - <span data-ttu-id="7861c-188">或者，您可以从本地计算机上的某个 .docx 文件**导入**内容并根据需要进行编辑。</span><span class="sxs-lookup"><span data-stu-id="7861c-188">Alternatively, you can **Import** the content from a .docx file on your local machine and edit as required.</span></span> <span data-ttu-id="7861c-189">这样，您就不必在编辑器的所有内容内键入。</span><span class="sxs-lookup"><span data-stu-id="7861c-189">That way, you don’t have to type in all the content in the editor.</span></span>

1. <span data-ttu-id="7861c-190">若要预览聘约文档，请使用页面顶部的**预览**选项。</span><span class="sxs-lookup"><span data-stu-id="7861c-190">To preview the offer document, use the **Preview** option at the top of the page.</span></span>

1. <span data-ttu-id="7861c-191">若要控制聘约创建者是否可以编辑聘约文档内容，请使用页面顶部的**管理权限**。</span><span class="sxs-lookup"><span data-stu-id="7861c-191">To control whether an offer creator can edit the offer document content, use the **Manage permission** option at the top of the page.</span></span> <span data-ttu-id="7861c-192">如果您希望聘约创建者只能插入占位符值而不编辑文本，请将权限值设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="7861c-192">If you want the offer creator to only insert placeholder values and not edit text, set the permission value to **No**.</span></span>

1. <span data-ttu-id="7861c-193">单击**保存**以保存您的进度。</span><span class="sxs-lookup"><span data-stu-id="7861c-193">Click **Save** to save your progress.</span></span> <span data-ttu-id="7861c-194">模板将保存为草稿状态。</span><span class="sxs-lookup"><span data-stu-id="7861c-194">The template will be saved in a draft state.</span></span>

1. <span data-ttu-id="7861c-195">若要完成并将文档标记为完成，请单击**完成**。</span><span class="sxs-lookup"><span data-stu-id="7861c-195">To finalize and mark the document as published, click **Finish**.</span></span>

1. <span data-ttu-id="7861c-196">您可以查看哪些文档模板（草稿模式）当前可用、已经存档或不再在文档模板库登录体验中使用。</span><span class="sxs-lookup"><span data-stu-id="7861c-196">You can see which document templates are currently active, in draft mode, and have been archived and are no longer in use on the document templates library landing experience.</span></span>

>[!NOTE]
> <span data-ttu-id="7861c-197">您可以删除不属于现有聘约包模板的任何聘约文档模板。</span><span class="sxs-lookup"><span data-stu-id="7861c-197">You can delete any offer document template that is not part of an existing offer package template.</span></span>


## <a name="offer-package-templates"></a><span data-ttu-id="7861c-198">聘约包模板</span><span class="sxs-lookup"><span data-stu-id="7861c-198">Offer package templates</span></span>

<span data-ttu-id="7861c-199">聘约包是与应聘者共享的聘约项目，包括一个或多个聘约文档模板的组合。</span><span class="sxs-lookup"><span data-stu-id="7861c-199">Offer packages are the offer artifacts that are shared with the candidate and consist of a combination of one or more offer document templates.</span></span> <span data-ttu-id="7861c-200">若要创建聘约包，请执行以下操作。</span><span class="sxs-lookup"><span data-stu-id="7861c-200">To create an offer package, do the following.</span></span>

1.  <span data-ttu-id="7861c-201">转到**聘约管理**。</span><span class="sxs-lookup"><span data-stu-id="7861c-201">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="7861c-202">从左侧导航窗格转到**包**。</span><span class="sxs-lookup"><span data-stu-id="7861c-202">Go to **Packages** from the left navigation pane.</span></span>

    <span data-ttu-id="7861c-203">可供聘约创建者使用的可用包模板的列表将显示。</span><span class="sxs-lookup"><span data-stu-id="7861c-203">A list of active package templates that are available for offer creators to use is displayed.</span></span>

1.  <span data-ttu-id="7861c-204">若要新建聘约包，单击**新建包**。</span><span class="sxs-lookup"><span data-stu-id="7861c-204">To create a new offer package, click **New Package**.</span></span>

1.  <span data-ttu-id="7861c-205">输入一个唯一名称，然后单击**创建**。</span><span class="sxs-lookup"><span data-stu-id="7861c-205">Enter a unique name and click **Create**.</span></span>

1.  <span data-ttu-id="7861c-206">单击**添加模板**。</span><span class="sxs-lookup"><span data-stu-id="7861c-206">Click **Add template**.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="7861c-207">您可以选择创建新模板或从现有模板选择。</span><span class="sxs-lookup"><span data-stu-id="7861c-207">You can choose to create a new template or choose from an existing one.</span></span>

    > - <span data-ttu-id="7861c-208">如果您选择添加现有模板，您需要确保聘约文档模板已保存、完成并且标记为可用。</span><span class="sxs-lookup"><span data-stu-id="7861c-208">If you choose to add an existing template, you need to make sure that the   offer document template was saved, finalized, and marked as   active.</span></span>
    
    > - <span data-ttu-id="7861c-209">您可以根据需要选择任意多的文档模板。</span><span class="sxs-lookup"><span data-stu-id="7861c-209">You can choose as many document templates as you want.</span></span> 
    
1.  <span data-ttu-id="7861c-210">单击**完成**返回到**包管理**。</span><span class="sxs-lookup"><span data-stu-id="7861c-210">Click **Done** to return to **Package management**.</span></span>

    <span data-ttu-id="7861c-211">您可以配置文档的顺序，还可以标记特定聘约文档是否在聘约创建时需要。</span><span class="sxs-lookup"><span data-stu-id="7861c-211">You can configure the sequence of the documents and also mark whether the specific offer document is required during offer creation.</span></span> <span data-ttu-id="7861c-212">聘约创建者可以选择删除标记为**不需要**的文档。</span><span class="sxs-lookup"><span data-stu-id="7861c-212">The offer creator will have an option to delete the documents marked as **Not required**.</span></span>

1. <span data-ttu-id="7861c-213">若要保存聘约包模板，使其可被所有聘约创建者使用，单击**保存并发布**。</span><span class="sxs-lookup"><span data-stu-id="7861c-213">To save the offer package template so that it's usable by all offer creators, click **Save and publish**.</span></span>

   <span data-ttu-id="7861c-214">若要查看草稿聘约包模板，请转到**草稿**选项卡。如果对聘约包模板进行了更改，其必须保存并重新发布。</span><span class="sxs-lookup"><span data-stu-id="7861c-214">To view draft offer package templates, go to the **Drafts** tab. If a change is made to the offer package template, it must be  saved and republished.</span></span>

## <a name="configure-an-offer-process"></a><span data-ttu-id="7861c-215">配置聘约流程</span><span class="sxs-lookup"><span data-stu-id="7861c-215">Configure an offer process</span></span>

<span data-ttu-id="7861c-216">聘约创建流程有若干个部分可由 Attract 管理员配置。</span><span class="sxs-lookup"><span data-stu-id="7861c-216">There are several parts of the offer creation process that can be configured by an Attract administrator.</span></span>

- <span data-ttu-id="7861c-217">**聘约审核** - 选择是否需要进行聘约审核才能将聘约发送给应聘者。</span><span class="sxs-lookup"><span data-stu-id="7861c-217">**Offer approvals** - Choose whether offer approvals are required before the offer can be sent to the candidate.</span></span> <span data-ttu-id="7861c-218">作为管理员，您还可以决定所有聘约审核是顺序进行，还是在并行审核工作流中进行。</span><span class="sxs-lookup"><span data-stu-id="7861c-218">As an administrator, you can also decide whether all offer approvals will happen in a sequential manner or parallel approval workflow.</span></span> <span data-ttu-id="7861c-219">您还可以强制聘约审核人是否必须随聘约审核添加备注。</span><span class="sxs-lookup"><span data-stu-id="7861c-219">You can also mandate whether offer approvers must add a comment along with their offer approval.</span></span> <span data-ttu-id="7861c-220">聘约审核对于所有非标准聘约都是必需的。</span><span class="sxs-lookup"><span data-stu-id="7861c-220">Offer approvals are mandatory for all non-standard offers.</span></span>

- <span data-ttu-id="7861c-221">**应聘者的聘约体验** - 作为管理员，您可以选择设置是否所有聘约都具有到期日期，如果有，设置到期日期的默认偏移。</span><span class="sxs-lookup"><span data-stu-id="7861c-221">**Candidate’s offer experience** - As administrator, you can choose to set whether all offers have an expiration date, and if so, what the default offset for the expiration date should be.</span></span> <span data-ttu-id="7861c-222">您还可以配置应聘者是否能够拒绝聘约。</span><span class="sxs-lookup"><span data-stu-id="7861c-222">You can also configure whether candidates can decline an offer.</span></span>

- <span data-ttu-id="7861c-223">**电子签名** - 作为管理员，您还可以选择应聘者可以用于对聘约进行签名的方法。</span><span class="sxs-lookup"><span data-stu-id="7861c-223">**e-Signatures** - As an administrator, you can also choose the method that candidates can use to sign offers.</span></span>
    - <span data-ttu-id="7861c-224">Adobe Sign - 所有聘约包都将通过 Adobe Sign 发送和签名。</span><span class="sxs-lookup"><span data-stu-id="7861c-224">Adobe Sign - All offer packages will be sent and signed via Adobe Sign.</span></span> <span data-ttu-id="7861c-225">发布聘约的每个聘约创建者都需要有连接到 Attract 的 Adobe Sign 帐户。</span><span class="sxs-lookup"><span data-stu-id="7861c-225">Each offer creator publishing the offer needs to have their Adobe Sign account connected to Attract.</span></span> <span data-ttu-id="7861c-226">对于 Adobe Sign 许可证和免费试用版，请访问此[链接](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html)。</span><span class="sxs-lookup"><span data-stu-id="7861c-226">For Adobe Sign licenses and a free Trial, please visit this [link](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span></span>

    - <span data-ttu-id="7861c-227">DocuSign - 所有聘约包都将通过 DocuSign 发送和签名。</span><span class="sxs-lookup"><span data-stu-id="7861c-227">DocuSign - All offer packages will be sent and signed via DocuSign.</span></span> <span data-ttu-id="7861c-228">发布聘约的每个聘约创建者都需要有连接到 Attract 的 DocuSign 帐户。</span><span class="sxs-lookup"><span data-stu-id="7861c-228">Each offer creator publishing the offer needs to have their DocuSign account connected to Attract.</span></span> 
    
    - <span data-ttu-id="7861c-229">ESign - 这是默认选项，现成提供，在其中，用户可以通过键入姓名和姓名首字母缩写对聘约进行签名。</span><span class="sxs-lookup"><span data-stu-id="7861c-229">ESign - This is the default option, provided out of the box, where the user can sign an offer by typing their name and initials.</span></span>


<span data-ttu-id="7861c-230">若要了解有关聘约创建流程的更多信息，请参阅[创建、审核和签署聘约](./creating-offers.md)。</span><span class="sxs-lookup"><span data-stu-id="7861c-230">To learn more about the offer creation process, see [Creating, approving, and signing offers](./creating-offers.md).</span></span>
