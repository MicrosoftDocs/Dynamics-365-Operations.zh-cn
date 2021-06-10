---
title: 避免职位层次结构的文本截断并导出到 Visio
description: 本文说明如何解决当客户在 Microsoft Dynamics 365 Human Resources 中查看职位层次结构时出现个人和职位名称截断的问题。 文本截断可能使拍摄屏幕快照或打印层次结构很困难。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a03c8f340e8ebb2fb0440518c154ed3bdd0197f6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053243"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a><span data-ttu-id="0fdca-104">避免职位层次结构和导出到 Visio 时的文本截断</span><span class="sxs-lookup"><span data-stu-id="0fdca-104">Avoid text truncation on the position hierarchy and export to Visio</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0fdca-105">**发货**</span><span class="sxs-lookup"><span data-stu-id="0fdca-105">**Issue**</span></span>

<span data-ttu-id="0fdca-106">当客户在 Microsoft Dynamics 365 Human Resources 中查看职位层次结构时，个人和职位名称截断。</span><span class="sxs-lookup"><span data-stu-id="0fdca-106">When a customer views the position hierarchy in Microsoft Dynamics 365 Human Resources, the names of individuals and positions are truncated.</span></span> <span data-ttu-id="0fdca-107">因此，可能很难拍摄屏幕快照，或打印和分配层次结构。</span><span class="sxs-lookup"><span data-stu-id="0fdca-107">Therefore, it can be difficult to take a screenshot, or to print and distribute the hierarchy.</span></span>

![职位层次结构](media/position-h.png)

<span data-ttu-id="0fdca-109">**原因**</span><span class="sxs-lookup"><span data-stu-id="0fdca-109">**Cause**</span></span>

<span data-ttu-id="0fdca-110">此为有意行为。</span><span class="sxs-lookup"><span data-stu-id="0fdca-110">This behavior is by design.</span></span>

<span data-ttu-id="0fdca-111">**分辨率**</span><span class="sxs-lookup"><span data-stu-id="0fdca-111">**Resolution**</span></span>

<span data-ttu-id="0fdca-112">遗憾的是，用户不能轻松更改文本的大小。</span><span class="sxs-lookup"><span data-stu-id="0fdca-112">Unfortunately, users can't easily change the size of the text.</span></span> <span data-ttu-id="0fdca-113">但是，您可以将职位层次结构从 Human Resources 中导出，然后导入到 Microsoft Visio。</span><span class="sxs-lookup"><span data-stu-id="0fdca-113">However, you can export the position hierarchy out of Human Resources and then import it into Microsoft Visio.</span></span> <span data-ttu-id="0fdca-114">以下文章是为 Microsoft Dynamics AX 2012 所写，但过程也适用于 Human Resources：[导出职位层次结构到 Microsoft Visio](/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio)。</span><span class="sxs-lookup"><span data-stu-id="0fdca-114">Although the following article was written for Microsoft Dynamics AX 2012, the process still applies to Human Resources: [Export a position hierarchy to Microsoft Visio](/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span></span>

<span data-ttu-id="0fdca-115">执行以下步骤导出到 Visio。</span><span class="sxs-lookup"><span data-stu-id="0fdca-115">Follow these steps to export to Visio.</span></span>

1. <span data-ttu-id="0fdca-116">在 Human Resources 中，打开 **职位** 列表页。</span><span class="sxs-lookup"><span data-stu-id="0fdca-116">In Human Resources, open the **Positions** list page.</span></span>

    <span data-ttu-id="0fdca-117">若要在组织结构图中包括更多信息，请向 **职位** 列表添加字段，以便在您以后在此过程中使用向导时这些信息可用。</span><span class="sxs-lookup"><span data-stu-id="0fdca-117">To include more information in the organization structure diagram, add fields to the **Positions** list, so that they are available when you use the wizard later in this procedure.</span></span>

2. <span data-ttu-id="0fdca-118">在操作窗格上，选择 **在 Microsoft Office 中打开** 按钮，然后，在 **导出到 Excel** 下，选择 **职位**。</span><span class="sxs-lookup"><span data-stu-id="0fdca-118">On the Action Pane, select the **Open in Microsoft Office** button, and then, under **Export to Excel**, select **Positions**.</span></span> <span data-ttu-id="0fdca-119">或者，按 Ctrl+T。</span><span class="sxs-lookup"><span data-stu-id="0fdca-119">Alternatively, press Ctrl+T.</span></span>

    ![将职位列表页导出到 Excel](media/org-admin.png)

3. <span data-ttu-id="0fdca-121">保存导出的 Excel 文件。</span><span class="sxs-lookup"><span data-stu-id="0fdca-121">Save the Excel file that is exported.</span></span>

    ![“导出到 Excel”对话框](media/export-excel.png)

4. <span data-ttu-id="0fdca-123">在 Visio 中，选择 **Visio - 新建**，然后选择 **业务** 模板类别。</span><span class="sxs-lookup"><span data-stu-id="0fdca-123">In Visio, select **Visio - Create New**, and select the **Business** template category.</span></span>

    ![新建图表](media/new.png)

5. <span data-ttu-id="0fdca-125">选择 **组织结构图向导**，然后选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="0fdca-125">Select **Organization Chart Wizard**, and then select **Create**.</span></span>

    ![组织结构图向导对话框](media/orgchart-wizard.png)

6. <span data-ttu-id="0fdca-127">选择 **文件或数据库中已存储的信息**，然后选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="0fdca-127">Select **Information that's already stored in a file or database**, and then select **Next**.</span></span>

    ![组织结构图向导 1](media/orgchart-wizard7.png)

7. <span data-ttu-id="0fdca-129">选择 **文本、Org Plus (\*.txt) 或 Excel 文件**，然后选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="0fdca-129">Choose **A text, Org Plus (\*.txt), or Excel file**, and then select **Next**.</span></span>

    ![组织结构图向导 2](media/orgchart-wizard3.png)

8. <span data-ttu-id="0fdca-131">浏览选择导出的包含职位层次结构的 Excel 文件，然后选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="0fdca-131">Browse to select the exported Excel file that contains the position hierarchy, and then select **Next**.</span></span>

    ![组织结构图向导 3](media/orgchart-wizard2.png)

9. <span data-ttu-id="0fdca-133">将 **名称** 字段设置为 **职位**，将 **报告至** 字段设置为 **直接上级职位**，然后选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="0fdca-133">Set the **Name** field to **Position**, set the **Reports to** field to **Reports to position**, and then select **Next**.</span></span>

    ![组织结构图向导 4](media/orgchart-wizard1.png)

10. <span data-ttu-id="0fdca-135">选择应显示在每个节点的字段，然后选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="0fdca-135">Select the fields that should be shown on each node, and then select **Next**.</span></span>

    ![组织结构图向导 5](media/orgchart-wizard5.png)

11. <span data-ttu-id="0fdca-137">将 **职位** 列添加到 **形状数据字段** 列表，然后选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="0fdca-137">Add the **Position** column to the **Shape Data fields** list, and then select **Next**.</span></span>

    ![组织结构图向导 6](media/orgchart-wizard6.png)

12. <span data-ttu-id="0fdca-139">图片当前未提供。</span><span class="sxs-lookup"><span data-stu-id="0fdca-139">Pictures aren't currently available.</span></span> <span data-ttu-id="0fdca-140">因此，在下一页，选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="0fdca-140">Therefore, on the next page, select **Next**.</span></span>
13. <span data-ttu-id="0fdca-141">选择 **我希望向导跨各个页面自动中断我的组织结构图**。</span><span class="sxs-lookup"><span data-stu-id="0fdca-141">Select **I want the wizard to automatically break my organization chart across pages**.</span></span>

    ![组织结构图向导 7](media/orgchart-wizard4.png)

14. <span data-ttu-id="0fdca-143">选择 **完成**。</span><span class="sxs-lookup"><span data-stu-id="0fdca-143">Select **Finish**.</span></span>

    <span data-ttu-id="0fdca-144">如果有职位未在结构中，将要求您在图表中包括它们。</span><span class="sxs-lookup"><span data-stu-id="0fdca-144">If there are any positions that aren't in the structure, you're asked to include them in the diagram.</span></span>

<span data-ttu-id="0fdca-145">在 Visio 中生成的图表在单独的工作表中显示每位经理。</span><span class="sxs-lookup"><span data-stu-id="0fdca-145">The diagram that is generated in Visio shows each manager on a separate worksheet.</span></span>

<span data-ttu-id="0fdca-146">根据您选择要包括在图表中的字段，每个节点会在 Visio 文件生成时显示相应的信息。</span><span class="sxs-lookup"><span data-stu-id="0fdca-146">Based on the fields that you selected to include in the diagram, each node shows the appropriate information when the Visio file is generated.</span></span>

![层次结构图](media/hierarchy.png)

<span data-ttu-id="0fdca-148">**其他选项**</span><span class="sxs-lookup"><span data-stu-id="0fdca-148">**Additional option**</span></span>

<span data-ttu-id="0fdca-149">在 Human Resources 中，您可能还可以使用 **人员** 工作区来查看某些层次结构相关信息。</span><span class="sxs-lookup"><span data-stu-id="0fdca-149">In Human Resources, you might also be able to use the **People** workspace to view some hierarchy-related information.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]