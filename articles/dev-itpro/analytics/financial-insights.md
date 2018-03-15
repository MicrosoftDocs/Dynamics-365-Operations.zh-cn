---
title: "财务见解"
description: "财务见解使用 Microsoft Power BI 汇总财务关键绩效指标 (KPI)、图表和财务报表。"
author: kweekley
manager: AnnBe
ms.date: 02/28/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: d527df21e791978b41527c01c2e6b68b393861ac
ms.openlocfilehash: 90dc6214f1eb31440a3ec78a58c6a07394245cd2
ms.contentlocale: zh-cn
ms.lasthandoff: 02/28/2018

---

# <a name="financial-insights"></a><span data-ttu-id="25eab-103">财务见解</span><span class="sxs-lookup"><span data-stu-id="25eab-103">Financial Insights</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="25eab-104">**财务见解**使用 Microsoft Power BI 汇总财务关键绩效指标 (KPI)、图表和财务报表。</span><span class="sxs-lookup"><span data-stu-id="25eab-104">**Financial Insights** uses Microsoft Power BI to bring together financial key performance indicators (KPIs), charts, and financial statements.</span></span> <span data-ttu-id="25eab-105">Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中已嵌入 Power BI。</span><span class="sxs-lookup"><span data-stu-id="25eab-105">Power BI is embedded in Microsoft Dynamics 365 Finance and Operations, Enterprise edition.</span></span>
<span data-ttu-id="25eab-106">**财务见解**的主要功能是分析报告。</span><span class="sxs-lookup"><span data-stu-id="25eab-106">The focus of **Financial Insights** is analytical reporting.</span></span> <span data-ttu-id="25eab-107">组织中的人员可查看、研究、了解和采取行动。</span><span class="sxs-lookup"><span data-stu-id="25eab-107">Personas across an organization can view, research, understand, and act.</span></span> 

<span data-ttu-id="25eab-108">**财务见解**合并来自总帐和子分类帐的数据，以提供更全面的组织财务状况介绍。</span><span class="sxs-lookup"><span data-stu-id="25eab-108">**Financial Insights** combines data from the general ledger and subledgers to give a more complete picture of the financial health of an organization.</span></span>

> [!NOTE] 
> <span data-ttu-id="25eab-109">本文档使用以下 Power BI 术语：</span><span class="sxs-lookup"><span data-stu-id="25eab-109">This document uses the following Power BI terminology:</span></span>                                                                           
<span data-ttu-id="25eab-110">**报表** – 所有选项卡上的所有视觉对象保存到的单个 .pbix 文件。</span><span class="sxs-lookup"><span data-stu-id="25eab-110">**Report** – A single .pbix file that all the visuals on all tabs are saved to.</span></span>                                                          
<span data-ttu-id="25eab-111">**页面** – 单个 .pbix 文件中的一个选项卡。</span><span class="sxs-lookup"><span data-stu-id="25eab-111">**Page** – A tab in a single .pbix file.</span></span> <span data-ttu-id="25eab-112">每个页面可以包含一个或多个视觉对象。</span><span class="sxs-lookup"><span data-stu-id="25eab-112">Each page can contain one or more visuals.</span></span>                                                     
<span data-ttu-id="25eab-113">**视觉对象** – 一种数据源，如卡片、KPI、图表、图形、矩阵或财务报表。</span><span class="sxs-lookup"><span data-stu-id="25eab-113">**Visual** – A single source of data, such as a card, KPI, chart, graph, matrix, or financial statement.</span></span> <span data-ttu-id="25eab-114">因为受限于报告的数据大小，拥有一个财务报表作为视觉对象的页面不能再有其他视觉对象。</span><span class="sxs-lookup"><span data-stu-id="25eab-114">A page that has a financial statement as a visual can have no other visuals, because of the size of the data that is being reported on.</span></span>


<span data-ttu-id="25eab-115">现在，**财务见解**用于查看有效法人或所有法人的数据。</span><span class="sxs-lookup"><span data-stu-id="25eab-115">Currently, **Financial Insights** is used to view data for either the active legal entity or all legal entities.</span></span> <span data-ttu-id="25eab-116">在将来的版本中，该工作区将发展成可在其中使用 Power BI 编辑和创建视觉对象的位置。</span><span class="sxs-lookup"><span data-stu-id="25eab-116">In future releases, the workspace will evolve into the place where you can use Power BI to edit and create visuals.</span></span>

<span data-ttu-id="25eab-117">**CFO 概览**工作区与**财务见解**显示的视觉对象相同，但是侧重于供您查看和筛选现有报表中的数据。</span><span class="sxs-lookup"><span data-stu-id="25eab-117">The **CFO overview** workspace shows the same visuals as **Financial Insights**, but is focused on letting you view and filter the data on existing reports.</span></span> <span data-ttu-id="25eab-118">在将来的版本中，您可以向**财务见解**工作区添加新的视觉对象。</span><span class="sxs-lookup"><span data-stu-id="25eab-118">In future releases, you will be able to add new visuals to the **Financial Insights** workspace.</span></span> <span data-ttu-id="25eab-119">新的对象视觉也可能在侧重其他角色（如项目经理或应付帐款经理）的工作区中可用。</span><span class="sxs-lookup"><span data-stu-id="25eab-119">The new visuals might also be available in workspaces that are focused on other roles, such as project managers or accounts payable managers.</span></span> <span data-ttu-id="25eab-120">无论角色可访问哪些法人，**CFO 概览**工作区都将继续显示所有法人的数据。</span><span class="sxs-lookup"><span data-stu-id="25eab-120">The **CFO overview** workspace continues to show data for all legal entities, regardless of the legal entities that the role has access to.</span></span>

## <a name="finance-and-operations-setup"></a><span data-ttu-id="25eab-121">Finance and Operations 设置</span><span class="sxs-lookup"><span data-stu-id="25eab-121">Finance and Operations setup</span></span>
<span data-ttu-id="25eab-122">**总帐**</span><span class="sxs-lookup"><span data-stu-id="25eab-122">**General ledger**</span></span>

<span data-ttu-id="25eab-123">在**财务见解**中，将使用主科目类型和主科目类别填写**资产负债表**财务报表和各种**收入报表**财务报表中的响应相应主科目。</span><span class="sxs-lookup"><span data-stu-id="25eab-123">The main account type and the main account categories are used to fill in appropriate default main accounts on the **Balance sheet** financial statement and the various **Income statement** financial statements in **Financial Insights**.</span></span>

<span data-ttu-id="25eab-124">在**主科目**页面中，必须定义主科目，这样才能为其分配以下类型之一：</span><span class="sxs-lookup"><span data-stu-id="25eab-124">On the **Main accounts** page, you must define your main account so that one of the following types is assigned to it:</span></span>

<span data-ttu-id="25eab-125">•   收入</span><span class="sxs-lookup"><span data-stu-id="25eab-125">•   Revenue</span></span>

<span data-ttu-id="25eab-126">•   费用</span><span class="sxs-lookup"><span data-stu-id="25eab-126">•   Expense</span></span>

<span data-ttu-id="25eab-127">•   资产</span><span class="sxs-lookup"><span data-stu-id="25eab-127">•   Assets</span></span>

<span data-ttu-id="25eab-128">•   负债</span><span class="sxs-lookup"><span data-stu-id="25eab-128">•   Liabilities</span></span>

<span data-ttu-id="25eab-129">•   权益</span><span class="sxs-lookup"><span data-stu-id="25eab-129">•   Equity</span></span>

<span data-ttu-id="25eab-130">请勿为主科目分配其他任何主科目类型，例如**资产负债表**或**损益**。</span><span class="sxs-lookup"><span data-stu-id="25eab-130">Do not assign any other main account type, such as **Balance sheet** or **Profit and Loss**, to your main accounts.</span></span> <span data-ttu-id="25eab-131">如果分配了其他主科目类型，则报告不能确定主科目类型，因为粒状不足。</span><span class="sxs-lookup"><span data-stu-id="25eab-131">Reporting can’t determine the type of main account when other main account types are assigned, because they aren’t granular enough.</span></span> <span data-ttu-id="25eab-132">必须确定主科目类型，才能将负债和收入在财务报表上显示为正金额。</span><span class="sxs-lookup"><span data-stu-id="25eab-132">The type of main account must be determined to show liabilities and revenue as positive amounts on financial reports.</span></span>

<span data-ttu-id="25eab-133">要使各主科目在财务报表中显示和包含在其他各种视觉对象（如 KPI）中，必须将其分配给主科目类别。</span><span class="sxs-lookup"><span data-stu-id="25eab-133">To appear on the financial statements and to be included in various other visuals, such as KPIs, each main account must be assigned a main account category.</span></span> <span data-ttu-id="25eab-134">主科目类别已增强，所以现在包含显示属性。</span><span class="sxs-lookup"><span data-stu-id="25eab-134">The main account categories have been enhanced so that they include a display order.</span></span> <span data-ttu-id="25eab-135">在**财务见解**中，显示顺序专用于财务报表。</span><span class="sxs-lookup"><span data-stu-id="25eab-135">The display order is used specifically on financial statements in **Financial Insights**.</span></span> <span data-ttu-id="25eab-136">编辑或新增主科目类别之后，可更改**显示顺序**值以定义财务报表中应采用的主科目类别显示顺序。</span><span class="sxs-lookup"><span data-stu-id="25eab-136">After you edit or add a new main account category, you can change the **Display order** value to define the order that the main account categories should be shown in on a financial statement.</span></span> <span data-ttu-id="25eab-137">如果必须更改多个主科目类别的显示顺序，可使用“在 Excel 中打开”功能快速编辑并将更改发布回 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="25eab-137">If you must change the display order for many main account categories, you can use the Open in Excel feature to quickly edit and publish the changes back to Finance and Operations.</span></span>


## <a name="entity-store"></a><span data-ttu-id="25eab-138">实体商店</span><span class="sxs-lookup"><span data-stu-id="25eab-138">Entity store</span></span>
<span data-ttu-id="25eab-139">**财务见解**的数据是从实体商店（**系统管理** > **设置** > **实体商店**）提取的。</span><span class="sxs-lookup"><span data-stu-id="25eab-139">The data for **Financial Insights** is pulled from the Entity store (**System administration** > **Setup** > **Entity store**).</span></span> <span data-ttu-id="25eab-140">如果打开 **CFO 概览**或**财务见解**工作区，然后发现视觉对象中显示了以下警告消息，说明必须更新实体。</span><span class="sxs-lookup"><span data-stu-id="25eab-140">If you open the **CFO overview** or **Financial Insights** workspace, and the following warning message appears in the visuals, you must update the entities.</span></span>
 
![警告](./media/Cantdisplay.png)

<span data-ttu-id="25eab-142">必须更新以下实体，才能查看**财务见解**和 **CFO 概览**工作区中的数据：</span><span class="sxs-lookup"><span data-stu-id="25eab-142">You must update the following entities to see data in the **Financial Insights** and **CFO overview** workspaces:</span></span>

<span data-ttu-id="25eab-143">•   CustCollectionsBIMeasurements</span><span class="sxs-lookup"><span data-stu-id="25eab-143">•   CustCollectionsBIMeasurements</span></span>

<span data-ttu-id="25eab-144">•   FinancialReportingOtherData</span><span class="sxs-lookup"><span data-stu-id="25eab-144">•   FinancialReportingOtherData</span></span>

<span data-ttu-id="25eab-145">•   FinancialReportingReferenceData</span><span class="sxs-lookup"><span data-stu-id="25eab-145">•   FinancialReportingReferenceData</span></span>

<span data-ttu-id="25eab-146">•   FinancialReportingTransactionData</span><span class="sxs-lookup"><span data-stu-id="25eab-146">•   FinancialReportingTransactionData</span></span>

<span data-ttu-id="25eab-147">•   LedgerCovLiquidityMeasurement</span><span class="sxs-lookup"><span data-stu-id="25eab-147">•   LedgerCovLiquidityMeasurement</span></span>

<span data-ttu-id="25eab-148">•   采购多维数据集</span><span class="sxs-lookup"><span data-stu-id="25eab-148">•   Purchase cube</span></span>

<span data-ttu-id="25eab-149">•   销售多维数据集</span><span class="sxs-lookup"><span data-stu-id="25eab-149">•   Sales cube</span></span>

<span data-ttu-id="25eab-150">在上一个版本中，LedgerActivityMeasure 和 VendPaymentBIMeasure 实体用于 **CFO 概览**工作区中的数据。</span><span class="sxs-lookup"><span data-stu-id="25eab-150">In the previous release, the LedgerActivityMeasure and VendPaymentBIMeasure entities were used for data in the **CFO overview** workspace.</span></span> <span data-ttu-id="25eab-151">但是，当前版本中不再使用这些实体。</span><span class="sxs-lookup"><span data-stu-id="25eab-151">However, they are no longer used in the current release.</span></span>

<span data-ttu-id="25eab-152">可定义重复执行的批处理以定期更新这些实体中的数据。</span><span class="sxs-lookup"><span data-stu-id="25eab-152">You can define a recurring batch to regularly update the data in the entities.</span></span> <span data-ttu-id="25eab-153">因为更新期间将完全重建每个实体，所以请仔细选择实体的更新时间和更新频率。</span><span class="sxs-lookup"><span data-stu-id="25eab-153">Because each entity is completely rebuilt during an update, select the time and frequency of entity updates carefully.</span></span> <span data-ttu-id="25eab-154">用于财务报表的主实体为 FinancialReportingTransactionData 实体。</span><span class="sxs-lookup"><span data-stu-id="25eab-154">The primary entity that is used for financial statements is the FinancialReportingTransactionData entity.</span></span> <span data-ttu-id="25eab-155">因此，此实体的更新频率可能需要更频繁。</span><span class="sxs-lookup"><span data-stu-id="25eab-155">Therefore, you might decide to update that entity more often.</span></span>

## <a name="security"></a><span data-ttu-id="25eab-156">安全性</span><span class="sxs-lookup"><span data-stu-id="25eab-156">Security</span></span>
<span data-ttu-id="25eab-157">目前，不能将嵌入式 Power BI 报表中的数据限制为仅用户可访问的法人。</span><span class="sxs-lookup"><span data-stu-id="25eab-157">Currently, the data on embedded Power BI reports can’t be limited to the legal entities that the user has access to.</span></span> <span data-ttu-id="25eab-158">因此，通过安全设置中的职责控制嵌入式 Power BI 报表。</span><span class="sxs-lookup"><span data-stu-id="25eab-158">Therefore, the embedded Power BI reports are controlled through duties in the security setup.</span></span> <span data-ttu-id="25eab-159">定义的职责允许访问所有法人的数据或仅有效公司的数据。</span><span class="sxs-lookup"><span data-stu-id="25eab-159">The duties that are defined allow access to data for either all legal entities or only the active company.</span></span> <span data-ttu-id="25eab-160">下表显示存在的职责及将其分配给的角色。</span><span class="sxs-lookup"><span data-stu-id="25eab-160">The following table shows the duties that exist and the roles that they are assigned to.</span></span> <span data-ttu-id="25eab-161">可根据组织的需求移除职责或将职责分配给其他角色。</span><span class="sxs-lookup"><span data-stu-id="25eab-161">The duties can be removed or assigned to different roles, based on your organization’s requirements.</span></span>

| <span data-ttu-id="25eab-162">**关税**</span><span class="sxs-lookup"><span data-stu-id="25eab-162">**Duty**</span></span>                     | <span data-ttu-id="25eab-163">**角色**</span><span class="sxs-lookup"><span data-stu-id="25eab-163">**Roles**</span></span>                                       | <span data-ttu-id="25eab-164">说明</span><span class="sxs-lookup"><span data-stu-id="25eab-164">Decription</span></span>                     |
|------------------------------|-------------------------------------------------|-----------------|
| <span data-ttu-id="25eab-165">查看 CFO 概述工作区</span><span class="sxs-lookup"><span data-stu-id="25eab-165">View CFO Overview workspace</span></span>  | <span data-ttu-id="25eab-166">首席财务官</span><span class="sxs-lookup"><span data-stu-id="25eab-166">Chief Financial Officer</span></span>                         | <span data-ttu-id="25eab-167">•    此职责提供对“CFO 概览”工作区的访问。</span><span class="sxs-lookup"><span data-stu-id="25eab-167">•    This duty provides access to the CFO overview workspace.</span></span> <span data-ttu-id="25eab-168">•  默认情况下，有效公司用作筛选器。</span><span class="sxs-lookup"><span data-stu-id="25eab-168">•  By default, the active company is used as a filter.</span></span> <span data-ttu-id="25eab-169">但是，无论用户是否可访问其他法人，您都可以添加所有法人。</span><span class="sxs-lookup"><span data-stu-id="25eab-169">However, you can add all legal entities, regardless of whether the user has access to the other legal entities.</span></span>               |
| <span data-ttu-id="25eab-170">查看所在公司财务见解</span><span class="sxs-lookup"><span data-stu-id="25eab-170">View financial insights current company</span></span> | <span data-ttu-id="25eab-171">•   会计师 •    会计经理 •    会计主管 • 审计员 •   预算经理 •    首席执行官 •   首席财务官 •   财务总监</span><span class="sxs-lookup"><span data-stu-id="25eab-171">•   Accountant •    Accounting manager •    Accounting supervisor • Auditor •   Budget manager •    Chief executive officer •   Chief financial officer •   Financial controller</span></span>  |   <span data-ttu-id="25eab-172">• 此职责提供对财务见解的访问。</span><span class="sxs-lookup"><span data-stu-id="25eab-172">• This duty provides access to Financial Insights.</span></span> <span data-ttu-id="25eab-173">•  默认情况下，有效公司用作筛选器。</span><span class="sxs-lookup"><span data-stu-id="25eab-173">•  By default, the active company is used as a filter.</span></span> <span data-ttu-id="25eab-174">不能添加其他法人。</span><span class="sxs-lookup"><span data-stu-id="25eab-174">You can’t add other legal entities.</span></span>            |
| <span data-ttu-id="25eab-175">查看公司间财务见解</span><span class="sxs-lookup"><span data-stu-id="25eab-175">View financial insights cross company</span></span>   | <span data-ttu-id="25eab-176">•   在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3 中，未将此职责分配给角色。</span><span class="sxs-lookup"><span data-stu-id="25eab-176">•   In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, this duty isn’t assigned to a role.</span></span> <span data-ttu-id="25eab-177">• 在下一版本中，将把此职责分配给首席财务官角色。</span><span class="sxs-lookup"><span data-stu-id="25eab-177">• In the next release, this duty will be assigned to the Chief financial officer role.</span></span> | <span data-ttu-id="25eab-178">•    此职责提供对“CFO 概览”工作区菜单项的访问。</span><span class="sxs-lookup"><span data-stu-id="25eab-178">•    This duty provides access to the menu item for the CFO overview workspace.</span></span> <span data-ttu-id="25eab-179">•    默认情况下，有效公司用作筛选器。</span><span class="sxs-lookup"><span data-stu-id="25eab-179">•    By default, the active company is used as a filter.</span></span> <span data-ttu-id="25eab-180">但是，无论用户是否可访问其他法人，您都可以添加所有法人。</span><span class="sxs-lookup"><span data-stu-id="25eab-180">However, you can add all legal entities, regardless of whether the user has access to the other legal entities.</span></span>             |


## <a name="financial-reporting-vs-finanical-insights"></a><span data-ttu-id="25eab-181">财务申报与财务见解</span><span class="sxs-lookup"><span data-stu-id="25eab-181">Financial reporting vs. Finanical insights</span></span>
<span data-ttu-id="25eab-182">尽管**财务见解**中包含财务报表，但不能取代 Finance and Operations 中的“财务申报”。</span><span class="sxs-lookup"><span data-stu-id="25eab-182">Although **Financial insights** contains financial statements, it isn’t a replacement for Financial reporting in Finance and Operations.</span></span> <span data-ttu-id="25eab-183">**财务见解**中的默认财务报表的范围受到限制，并且并非包含所有类型的财务报表。</span><span class="sxs-lookup"><span data-stu-id="25eab-183">The default financial statements in **Financial insights** are limited in scope and don’t include all types of financial statements.</span></span> <span data-ttu-id="25eab-184">“财务报告”仍然是用于设计、创建和生成法定财务报表的主要工具。</span><span class="sxs-lookup"><span data-stu-id="25eab-184">Financial reporting is still the primary tool for designing, creating, and generating statutory financial statements.</span></span>

<span data-ttu-id="25eab-185">下面的对比图可帮助区分这两个选项：</span><span class="sxs-lookup"><span data-stu-id="25eab-185">The following comparison chart will help differentiate the two options:</span></span>

<span data-ttu-id="25eab-186">|                                         | **财务申报**                            | **财务见解**             | |-----------------------------------------|----------------------------------------------------|---------- -------------------------| | **编辑默认报表**                | 是                                                | 否                                 | | **创建新报表**                  | 是                                                | 否                                 | | **打印报表**                       | 是                                                | 否                                 | | **导出到 Excel**                     | 是          | 受限制，将原始数据导出到 Excel，而不是带格式的报表       | | **支持报告层次结构/组织层次结构**   | 是                               | 否                                 | | **报告子分类帐数据**       | 是，限制为仅供应商、客户    | 是，供应商、客户、供应商/客户组、供应商/客户地址等  | | **申报币种**      | 是，核算币种，并转换为申报币种       | 否，仅限核算币种      | | **安全**                | 是，遵循 Finance and Operations 和申报树安全性 | 受限，查看所有公司（不受 Finance and Operations 安全性限制）或仅有效公司的报表 | | **支持不同会计科目表和财年** | 是                   | 否                   | | **报告外部数据**                              | 否                   | 否                                   | | **支持合并**                               | 是                          | 受限制，可报告多家公司，但是仅使用核算币种                                     |</span><span class="sxs-lookup"><span data-stu-id="25eab-186">|                                         | **Financial Reporting**                            | **Financial Insights**             | |-----------------------------------------|----------------------------------------------------|---------- -------------------------| | **Edit default reports**                | Yes                                                | No                                 | | **Create new reports**                  | Yes                                                | No                                 | | **Print reports**                       | Yes                                                | No                                 | | **Export to Excel**                     | Yes          | Limited Exports raw data to Excel, not a formatted report       | | **Support reporting hierarchy/Organization hierarchy**   | Yes                               | No                                 | | **Report on subledger data**       | Yes Limited to only vendor, customer    | Yes Vendor, customer, vendor/customer groups, vendor/customer addresses, etc.  | | **Reporting Currency**      | Yes Accounting currency and translate to reporting currency       | No Accounting currency only      | | **Security**                | Yes Adheres to Finance and Operations and reporting tree security | Limited View reports for all companies (regardless of Finance and Operations security) or only active company | | **Support different Chart of accounts and fiscal years** | Yes                   | No                   | | **report on external data**                              | No                   | No                                   | | **Support consolidations**                               | Yes                          | Limited Can report on multiple companies but use accounting currency only                                     |</span></span>


<span data-ttu-id="25eab-187">除了来自原始 **CFO 概览**工作区的用户界面，现在还有新的 KPI、图表和财务报表可用。</span><span class="sxs-lookup"><span data-stu-id="25eab-187">In addition to the user interface in the original **CFO overview** workspace, new KPIs, charts, and financial statements are now available.</span></span> <span data-ttu-id="25eab-188">以下财务报表可用：</span><span class="sxs-lookup"><span data-stu-id="25eab-188">The following financial statements are available:</span></span>

<span data-ttu-id="25eab-189">•   试算平衡表</span><span class="sxs-lookup"><span data-stu-id="25eab-189">•   Trial balance</span></span>

<span data-ttu-id="25eab-190">•   资产负债表</span><span class="sxs-lookup"><span data-stu-id="25eab-190">•   Balance sheet</span></span>

<span data-ttu-id="25eab-191">•   按区域分类的收入报表</span><span class="sxs-lookup"><span data-stu-id="25eab-191">•   Income statement by region</span></span>

<span data-ttu-id="25eab-192">•   利润报表实际与预算</span><span class="sxs-lookup"><span data-stu-id="25eab-192">•   Income statement actual vs. budget</span></span>

<span data-ttu-id="25eab-193">•   收入报表（含差异）</span><span class="sxs-lookup"><span data-stu-id="25eab-193">•   Income statement with variances</span></span>

<span data-ttu-id="25eab-194">•   12 个月趋势收入报表</span><span class="sxs-lookup"><span data-stu-id="25eab-194">•   12-month trend income statement</span></span>

<span data-ttu-id="25eab-195">•   费用三年趋势</span><span class="sxs-lookup"><span data-stu-id="25eab-195">•   Expenses three-year trend</span></span>

<span data-ttu-id="25eab-196">•   按供应商分类的费用</span><span class="sxs-lookup"><span data-stu-id="25eab-196">•   Expenses by vendor</span></span>

<span data-ttu-id="25eab-197">•   按客户分类的销售额</span><span class="sxs-lookup"><span data-stu-id="25eab-197">•   Sales by customer</span></span>

## <a name="edit-visuals"></a><span data-ttu-id="25eab-198">编辑视觉对象</span><span class="sxs-lookup"><span data-stu-id="25eab-198">Edit visuals</span></span>
<span data-ttu-id="25eab-199">在**财务见解**初始版本中，不能编辑任何视觉对象。</span><span class="sxs-lookup"><span data-stu-id="25eab-199">In the initial release of **Financial Insights**, none of the visuals can be edited.</span></span> <span data-ttu-id="25eab-200">在将来的版本中，具有相应安全设置的用户可以新建视觉对象，复制现有视觉对象和编辑视觉对象。</span><span class="sxs-lookup"><span data-stu-id="25eab-200">In future releases, users who have the appropriate security will be able to create new visuals, copy existing visuals, and edit visuals.</span></span> <span data-ttu-id="25eab-201">尽管包含报表的 .pbix 文件以资源的形式提供，我们仍然不建议您编辑默认报表。</span><span class="sxs-lookup"><span data-stu-id="25eab-201">Although the .pbix files that contain the reports are available as resources, we don’t recommend that you edit the default reports.</span></span> <span data-ttu-id="25eab-202">将对用于创建财务报表的数据模型、默认报表和自定义财务报表视觉对象执行更多更改。</span><span class="sxs-lookup"><span data-stu-id="25eab-202">Additional changes will be made to the data model, default reports, and custom financial statement visual that are used to create the financial statements.</span></span> <span data-ttu-id="25eab-203">因此，要利用下一版本中的新功能和对数据模型的更改，必须通过 Microsoft Power BI Desktop 重新执行已对默认报表执行的任何更改。</span><span class="sxs-lookup"><span data-stu-id="25eab-203">Therefore, to take advantage of new features and changes to the data model in the next release, you will have to redo any changes that you made to the default reports through Microsoft Power BI Desktop.</span></span>


## <a name="filtering"></a><span data-ttu-id="25eab-204">筛选</span><span class="sxs-lookup"><span data-stu-id="25eab-204">Filtering</span></span>
<span data-ttu-id="25eab-205">用户可使用左侧的**筛选器**窗格筛选报表。</span><span class="sxs-lookup"><span data-stu-id="25eab-205">Users can filter the report by using the **Filter** pane on the left.</span></span> <span data-ttu-id="25eab-206">此窗格是通过 Power BI Desktop 提供的同一个窗格。</span><span class="sxs-lookup"><span data-stu-id="25eab-206">This pane is the same pane that is available through Power BI Desktop.</span></span>
<span data-ttu-id="25eab-207">有各种级别的筛选，其中一些可能不可用，具体取决于您在页面（选项卡）中选择的内容或您是否在使用钻取功能：</span><span class="sxs-lookup"><span data-stu-id="25eab-207">There are various levels of filtering, some of which might not be available, depending on what you’ve selected on a page (tab) or whether you’re using the drill-through capabilities:</span></span>

<span data-ttu-id="25eab-208">• **报表级别筛选器** – 这种筛选器应用于所有页面（选项卡）上的所有视觉对象。</span><span class="sxs-lookup"><span data-stu-id="25eab-208">•   **Report-level filters** – These filters are applied to all visuals on all pages (tabs).</span></span>

<span data-ttu-id="25eab-209">•   **页面级别筛选器** – 这种筛选器应用于活动选项卡上的所有视觉对象。这种筛选器的优先级高于报表级别筛选器。</span><span class="sxs-lookup"><span data-stu-id="25eab-209">•   **Page-level filters** – These filters are applied to all visuals on the active tab. These filters are applied on top of the report-level filters.</span></span>

<span data-ttu-id="25eab-210">•   **视觉对象级别筛选器** – 这种筛选器仅应用于所选视觉对象。</span><span class="sxs-lookup"><span data-stu-id="25eab-210">•   **Visual-level filters** – These filters are applied only to the selected visual.</span></span> <span data-ttu-id="25eab-211">这种筛选器的优先级高于页面级别筛选器。</span><span class="sxs-lookup"><span data-stu-id="25eab-211">These filters are applied on top of the page level filters.</span></span>

<span data-ttu-id="25eab-212">•   **钻取筛选器** – 从源视觉对象钻取到当前视觉对象时，此筛选器从应用于当前视觉对象的“源”视觉对象开始筛选。</span><span class="sxs-lookup"><span data-stu-id="25eab-212">•   **Drill-through filter** – This filter filters from a “source” visual that is applied to the current visual when you drill through from the source visual to the current visual.</span></span>

![筛选](./media/filter.png)


<span data-ttu-id="25eab-214">若要删除特定筛选器值，请选择其旁边的橡皮擦符号。</span><span class="sxs-lookup"><span data-stu-id="25eab-214">To remove a specific filter value, select the eraser symbol next to it.</span></span> <span data-ttu-id="25eab-215">请勿通过选择 X 移除筛选器。如果选择 X，将把正在筛选的字段作为筛选器选项移除。</span><span class="sxs-lookup"><span data-stu-id="25eab-215">Don’t remove a filter by selecting the X. If you select the X, the field that you’re filtering on is removed as a filter option.</span></span> <span data-ttu-id="25eab-216">如果从筛选器意外地删除了字段，请关闭工作区，然后重新打开它。</span><span class="sxs-lookup"><span data-stu-id="25eab-216">If you accidently remove a field from the filter, close the workspace, and then reopen it.</span></span> <span data-ttu-id="25eab-217">将重新应用默认筛选器设置。</span><span class="sxs-lookup"><span data-stu-id="25eab-217">The default filter settings will be reapplied.</span></span>

<span data-ttu-id="25eab-218">默认情况下，首次打开工作区时，将把有效法人用作报表级别筛选器。</span><span class="sxs-lookup"><span data-stu-id="25eab-218">By default, when you first open workspaces, the active legal entity is used as the report-level filter.</span></span> <span data-ttu-id="25eab-219">用户可能可以添加其他法人或更改筛选器中已选中的默认法人，具体取决于其安全设置。</span><span class="sxs-lookup"><span data-stu-id="25eab-219">Depending on their security, users might be able to add other legal entities or change the default legal entity that is selected in the filter.</span></span>

<span data-ttu-id="25eab-220">需要**会计日历**筛选器，以便将正确的日历用于视觉对象。</span><span class="sxs-lookup"><span data-stu-id="25eab-220">The **Fiscal calendar** filter is required so that the correct calendar is used for the visual.</span></span> <span data-ttu-id="25eab-221">默认情况下，报表级别筛选器设置为有效法人的会计日历。</span><span class="sxs-lookup"><span data-stu-id="25eab-221">By default, the report-level filter is set to the active legal entity’s fiscal calendar.</span></span> <span data-ttu-id="25eab-222">如果将该筛选器更改为具有其他开始日期或结束日期的会计日历，将不包括期初余额。</span><span class="sxs-lookup"><span data-stu-id="25eab-222">If you change the filter to a fiscal calendar that has a different start or end date, the beginning balances won’t be included.</span></span> <span data-ttu-id="25eab-223">因此，您的**资产负债表**财务报表将不会显示正确的余额。</span><span class="sxs-lookup"><span data-stu-id="25eab-223">Therefore, your **Balance sheet** financial statements won’t show the correct balances.</span></span> <span data-ttu-id="25eab-224">如果在筛选器中再选择一个会计日历，将具有额外一组列。</span><span class="sxs-lookup"><span data-stu-id="25eab-224">If you select an additional fiscal calendar in the filter, you will have an additional set of columns.</span></span> <span data-ttu-id="25eab-225">每组额外列显示一个不同会计日历的金额。</span><span class="sxs-lookup"><span data-stu-id="25eab-225">Each additional set of columns shows the amounts for a different fiscal calendar.</span></span>

<span data-ttu-id="25eab-226">还需要**过帐层**筛选器。</span><span class="sxs-lookup"><span data-stu-id="25eab-226">The **Posting layer** filter is also required.</span></span> <span data-ttu-id="25eab-227">默认情况下，该筛选器设置为“当前”。</span><span class="sxs-lookup"><span data-stu-id="25eab-227">By default, the filter is set to Current.</span></span> <span data-ttu-id="25eab-228">可在筛选器中选择更多过帐层以显示聚合的金额。</span><span class="sxs-lookup"><span data-stu-id="25eab-228">You can select additional posting layers in the filter to show the aggregated amounts.</span></span>

<span data-ttu-id="25eab-229">**日期**和**会计年度**字段也支持筛选器。</span><span class="sxs-lookup"><span data-stu-id="25eab-229">Filters are also available for the **Date** and **Fiscal year** fields.</span></span> <span data-ttu-id="25eab-230">这些筛选器通常在页面级别应用。</span><span class="sxs-lookup"><span data-stu-id="25eab-230">Typically, these filters are applied at the page level.</span></span> <span data-ttu-id="25eab-231">默认情况下，**日期**筛选器使用您可以更改的关系日期。</span><span class="sxs-lookup"><span data-stu-id="25eab-231">By default, the **Date** filter uses a relational date that you can change.</span></span> <span data-ttu-id="25eab-232">也可以移除关系日期筛选器，改用**会计年度**筛选器。</span><span class="sxs-lookup"><span data-stu-id="25eab-232">You can also remove the relational date filter and use the **Fiscal year** filter instead.</span></span>

## <a name="currency"></a><span data-ttu-id="25eab-233">货币</span><span class="sxs-lookup"><span data-stu-id="25eab-233">Currency</span></span>

<span data-ttu-id="25eab-234">报告总帐数据的所有视觉对象都以记帐币种显示金额。</span><span class="sxs-lookup"><span data-stu-id="25eab-234">All visuals that report on general ledger data show amounts in the accounting currency.</span></span> <span data-ttu-id="25eab-235">因此，筛选法人时，必须小心地仅包含具有相同记帐币种的法人。</span><span class="sxs-lookup"><span data-stu-id="25eab-235">Therefore, when you filter on the legal entity, you must be careful to include only legal entities that have the same accounting currency.</span></span> <span data-ttu-id="25eab-236">否则，将聚合不同币种的数据。</span><span class="sxs-lookup"><span data-stu-id="25eab-236">Otherwise, you will aggregate data in different currencies.</span></span>

<span data-ttu-id="25eab-237">报告子分类帐数据的所有视觉对象（如**现金流量预测**和**前 10 位** 视觉对象）以系统币种显示金额。</span><span class="sxs-lookup"><span data-stu-id="25eab-237">All visuals that report on subledger data, such as the **Cash flow forecast** and **Top 10** visuals, show amounts in the system currency.</span></span> <span data-ttu-id="25eab-238">系统币种和系统汇率类型在**系统参数**页面中定义。</span><span class="sxs-lookup"><span data-stu-id="25eab-238">The system currency and system exchange rate type are defined on the **System parameters** page.</span></span>

<span data-ttu-id="25eab-239">**按银行帐户分类的余额**视觉对象以银行帐户的币种使用金额。</span><span class="sxs-lookup"><span data-stu-id="25eab-239">The **Balance by bank account** visual uses amounts in the bank accounts’ currency.</span></span>

## <a name="dimensions"></a><span data-ttu-id="25eab-240">维度</span><span class="sxs-lookup"><span data-stu-id="25eab-240">Dimensions</span></span>

<span data-ttu-id="25eab-241">默认财务报表中不包含任何财务维度，而是仅以主科目为重点。</span><span class="sxs-lookup"><span data-stu-id="25eab-241">The default financial statements don’t include any financial dimensions but are focused only on the main account.</span></span> <span data-ttu-id="25eab-242">报表变为可编辑时，将来的版本中将支持财务维度。</span><span class="sxs-lookup"><span data-stu-id="25eab-242">Support for financial dimensions will be available in future releases, when the reports become editable.</span></span> <span data-ttu-id="25eab-243">然后，组织就可以筛选财务维度值。</span><span class="sxs-lookup"><span data-stu-id="25eab-243">Organizations will then be able to filter on financial dimension values.</span></span>

<span data-ttu-id="25eab-244">某些财务报表中包含基于子分类帐交易记录的维度。</span><span class="sxs-lookup"><span data-stu-id="25eab-244">Some financial statements contain dimensions that are based on subledger transactions.</span></span> <span data-ttu-id="25eab-245">新财务报表的目标是对未设置为财务维度的维度启用筛选。</span><span class="sxs-lookup"><span data-stu-id="25eab-245">The goal of the new financial statements it to enable filtering on dimensions that aren’t set up as financial dimensions.</span></span> <span data-ttu-id="25eab-246">例如，默认的“按供应商分类的费用”报表可供您从主科目向下扩展，这样就可以查看按供应商细分的余额。</span><span class="sxs-lookup"><span data-stu-id="25eab-246">For example, the default Expenses by vendor report lets you expand down beyond the main account, so that you can see the balances broken down by vendor.</span></span> <span data-ttu-id="25eab-247">不会将供应商设置为财务维度。</span><span class="sxs-lookup"><span data-stu-id="25eab-247">The vendor isn’t set up as a financial dimension.</span></span> <span data-ttu-id="25eab-248">相反，系统返回到原始子分类帐交易记录以查找供应商。</span><span class="sxs-lookup"><span data-stu-id="25eab-248">Instead, the system returns to the originating subledger transaction to find the vendor.</span></span>

<span data-ttu-id="25eab-249">默认报表中使用以下维度。</span><span class="sxs-lookup"><span data-stu-id="25eab-249">The following dimensions are used on the default reports.</span></span> <span data-ttu-id="25eab-250">这些维度全部都不是财务维度。</span><span class="sxs-lookup"><span data-stu-id="25eab-250">None of these dimensions are financial dimensions.</span></span>

<span data-ttu-id="25eab-251">•   供应商</span><span class="sxs-lookup"><span data-stu-id="25eab-251">•   Vendor</span></span>

<span data-ttu-id="25eab-252">•   供应商组</span><span class="sxs-lookup"><span data-stu-id="25eab-252">•   Vendor group</span></span>

<span data-ttu-id="25eab-253">•   客户</span><span class="sxs-lookup"><span data-stu-id="25eab-253">•   Customer</span></span>

<span data-ttu-id="25eab-254">•   客户组</span><span class="sxs-lookup"><span data-stu-id="25eab-254">•   Customer group</span></span>

<span data-ttu-id="25eab-255">•   国家/地区</span><span class="sxs-lookup"><span data-stu-id="25eab-255">•   Country/region</span></span>

<span data-ttu-id="25eab-256">•   省/直辖市/自治区</span><span class="sxs-lookup"><span data-stu-id="25eab-256">•   State/province</span></span>

<span data-ttu-id="25eab-257">•   城市</span><span class="sxs-lookup"><span data-stu-id="25eab-257">•   City</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="25eab-258">如果使用财务日记帐将多个供应商或客户的交易记录汇总到一个凭证中，数据将不正确。</span><span class="sxs-lookup"><span data-stu-id="25eab-258">If you summarize transactions for multiple vendors or customers in a single voucher by using the financial journals, the data will be incorrect.</span></span> <span data-ttu-id="25eab-259">报告不能确定哪个供应商或客户与日记帐条目中的特定会计科目有关，因为任何位置均不维护该信息。</span><span class="sxs-lookup"><span data-stu-id="25eab-259">Reporting can’t determine which vendor or customer is related to a specific ledger account in a journal entry, because that information isn’t maintained anywhere.</span></span> <span data-ttu-id="25eab-260">因此，建议不要在一个凭证中输入多个供应商、客户、固定资产或项目。</span><span class="sxs-lookup"><span data-stu-id="25eab-260">Therefore, we do not recommend that you enter multiple vendors, customers, fixed assets, or projects in a single voucher.</span></span>

## <a name="drill-on-data"></a><span data-ttu-id="25eab-261">钻取数据</span><span class="sxs-lookup"><span data-stu-id="25eab-261">Drill on data</span></span>

<span data-ttu-id="25eab-262">Power BI 提供各种级别的钻取。</span><span class="sxs-lookup"><span data-stu-id="25eab-262">Various levels of drilling are available through Power BI.</span></span> <span data-ttu-id="25eab-263">每个级别都有不同的名称和不同的功能。</span><span class="sxs-lookup"><span data-stu-id="25eab-263">Each level has a different name and different functionality.</span></span> <span data-ttu-id="25eab-264">也可以钻取行和列。</span><span class="sxs-lookup"><span data-stu-id="25eab-264">You can also drill on rows and columns.</span></span> <span data-ttu-id="25eab-265">本部分通过将**试算平衡表**财务报表用作示例并显示如何钻取行，讨论各选项。</span><span class="sxs-lookup"><span data-stu-id="25eab-265">This section discusses the various options by using the **Trial balance** financial statement as an example and showing how you can drill on the rows.</span></span> <span data-ttu-id="25eab-266">列具有相同功能。</span><span class="sxs-lookup"><span data-stu-id="25eab-266">The same functionality exists for columns.</span></span> <span data-ttu-id="25eab-267">您只需要更改**钻取**设置。</span><span class="sxs-lookup"><span data-stu-id="25eab-267">You just have to change the **Drill on** setting.</span></span>

<span data-ttu-id="25eab-268">在下图中，**试算平衡表**报表已折叠至行层次结构的最高级别，即主科目类型。</span><span class="sxs-lookup"><span data-stu-id="25eab-268">In the following illustration, the **Trial balance** statement is collapsed to the highest level of the row hierarchy, the main account type.</span></span>

![试算平衡表](./media/trial-balance.png)

 
<span data-ttu-id="25eab-270">若要查看此层次结构的下一级别（即主科目类别），可将**钻取**字段设置为**行**，然后选择**展开**按钮（“钻取”字段后的第三个按钮）。</span><span class="sxs-lookup"><span data-stu-id="25eab-270">To view the next level of the hierarchy, the main account categories, you can set the **Drill on** field to **Rows** and then select the **Expand** button (the third button after the Drill on field).</span></span> <span data-ttu-id="25eab-271">现在可以看到展开的所有主科目类别。</span><span class="sxs-lookup"><span data-stu-id="25eab-271">You now see all the main account categories expanded.</span></span> <span data-ttu-id="25eab-272">Power BI 现在不允许仅展开一行或一列，但是仍然可以看到其他所有行或列。</span><span class="sxs-lookup"><span data-stu-id="25eab-272">Currently, Power BI doesn’t let you expand only one row or column but still see all the other rows or columns.</span></span>
 
![试算平衡表](./media/trial-balance2.png)
 
  
<span data-ttu-id="25eab-274">若要展开至所有行的主科目，可以再次使用**展开**按钮。</span><span class="sxs-lookup"><span data-stu-id="25eab-274">To expand to the main accounts for all rows, you can again use the **Expand** button.</span></span> <span data-ttu-id="25eab-275">但是，若要向下钻取至仅一行的主科目，请首先选择**向下钻取**按钮（窗口右侧的单向向下箭头），然后选择要向下钻取的行。</span><span class="sxs-lookup"><span data-stu-id="25eab-275">However, to drill down to the main accounts for only one row, first select the **Drill down** button (the single downward-pointing arrow on the right side of the window), and then select the row to drill down on.</span></span> <span data-ttu-id="25eab-276">下图显示选择**向下钻取**按钮后选择**销售额**行的结果。</span><span class="sxs-lookup"><span data-stu-id="25eab-276">The following illustration shows the result when the **Sales** row is selected after the **Drill down** button is selected.</span></span>

![试算平衡表](./media/trial-balance3.png)

<span data-ttu-id="25eab-278">向下钻取一行后，需要单击多次才能返回到整个试算平衡表。</span><span class="sxs-lookup"><span data-stu-id="25eab-278">After you drill down on a single row, multiple clicks are required in order to return to the full trial balance.</span></span> <span data-ttu-id="25eab-279">**向上钻取**按钮（**钻取**字段后的第一个按钮）仅在**销售额**类别的上下文中向上钻取，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="25eab-279">The **Drill up** button (the first button after the **Drill** on field) drills up only in the context of the **Sales** category, as shown in the following illustration.</span></span>
 
![试算平衡表](./media/trial-balance4.png)
 
 
<span data-ttu-id="25eab-281">可以继续使用**向上钻取**按钮返回到行的最高级别汇总。</span><span class="sxs-lookup"><span data-stu-id="25eab-281">You can continue to use the **Drill up** button to return to the highest level of summarization for the rows.</span></span>

<span data-ttu-id="25eab-282">Power BI 也有一个按钮（**钻取**字段后的第二个按钮）用于转到层次结构中的下一级别。</span><span class="sxs-lookup"><span data-stu-id="25eab-282">Power BI also has a button that lets you go to the next level in the hierarchy (the second button after the **Drill on** field).</span></span> <span data-ttu-id="25eab-283">这个按钮的效果与**展开**按钮（**钻取**字段后的第三个按钮）的效果不同，后者用于展开层次结构。</span><span class="sxs-lookup"><span data-stu-id="25eab-283">The effect of this button differs from the effect of the **Expand** button (the third button after the **Drill on** field), which is used to expand the hierarchy.</span></span> <span data-ttu-id="25eab-284">展开层次结构时，层次结构在报表中维护。</span><span class="sxs-lookup"><span data-stu-id="25eab-284">When you expand the hierarchy, the hierarchy is maintained on the report.</span></span> <span data-ttu-id="25eab-285">例如，就像前面所显示，如果展开主科目类型，仍然可以在报表中看到主科目类型。</span><span class="sxs-lookup"><span data-stu-id="25eab-285">For example, as was shown earlier, if you expand on the main account type, you still see the main account type on the report.</span></span> <span data-ttu-id="25eab-286">但是，转至层次结构中的下一级别时，报表不再在层次结构中显示父级，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="25eab-286">However, when you go to the next level in the hierarchy, the report no longer shows the parent in the hierarchy, as shown in the following illustration.</span></span>

![试算平衡表](./media/trial-balance5.png)

 
<span data-ttu-id="25eab-288">若要查看汇总余额背后的交易记录细节，可选择一些金额以向后钻取到 Financial and Operations 中。</span><span class="sxs-lookup"><span data-stu-id="25eab-288">To see the transaction details behind the summarized balances, you can select some amounts to drill back into Financial and Operations.</span></span>

<span data-ttu-id="25eab-289">从财务报表向后钻取将转到会计源资源管理器 (ASE)，而不是转到凭证交易记录。</span><span class="sxs-lookup"><span data-stu-id="25eab-289">The drill-back from the financial statements takes you to the Accounting source explorer (ASE), not to the voucher transactions.</span></span> <span data-ttu-id="25eab-290">ASE 不仅显示总帐中的会计条目。</span><span class="sxs-lookup"><span data-stu-id="25eab-290">The ASE doesn’t show just the accounting entries in the general ledger.</span></span> <span data-ttu-id="25eab-291">而是显示子分类帐交易记录的详细信息。</span><span class="sxs-lookup"><span data-stu-id="25eab-291">Instead, it shows the details of the subledger transaction.</span></span> <span data-ttu-id="25eab-292">因此，您可以获取有关源交易记录的多得多的详细信息，并且将其用于分析。</span><span class="sxs-lookup"><span data-stu-id="25eab-292">Therefore, you get much more detail about the originating transaction and can use it for analysis.</span></span> <span data-ttu-id="25eab-293">例如，可查看供应商或客户是谁，客户购买或供应商销售了哪些商品，甚至是交易记录中涉及哪个项目。</span><span class="sxs-lookup"><span data-stu-id="25eab-293">For example, you can see who the vendor or customer was, what the customer bought or the vendor sold, and even what project was on the transaction.</span></span>

<span data-ttu-id="25eab-294">将把财务报表中的以下筛选器发送到 ASE，以便 ASE 显示聚合的交易记录：</span><span class="sxs-lookup"><span data-stu-id="25eab-294">The following filters from the financial statements are sent to the ASE, so that the ASE shows the transactions that are aggregated:</span></span>

<span data-ttu-id="25eab-295">筛选的必需字段：</span><span class="sxs-lookup"><span data-stu-id="25eab-295">Required fields for filtering:</span></span>

  - <span data-ttu-id="25eab-296">法人</span><span class="sxs-lookup"><span data-stu-id="25eab-296">Legal entity</span></span>
 
  - <span data-ttu-id="25eab-297">会计日历</span><span class="sxs-lookup"><span data-stu-id="25eab-297">Fiscal calendar</span></span>
 
  - <span data-ttu-id="25eab-298">年</span><span class="sxs-lookup"><span data-stu-id="25eab-298">Year</span></span>
 
  - <span data-ttu-id="25eab-299">主科目 ID</span><span class="sxs-lookup"><span data-stu-id="25eab-299">Main account ID</span></span>

<span data-ttu-id="25eab-300">筛选的可选字段：</span><span class="sxs-lookup"><span data-stu-id="25eab-300">Optional fields for filtering:</span></span>

  - <span data-ttu-id="25eab-301">季度</span><span class="sxs-lookup"><span data-stu-id="25eab-301">Quarter</span></span>

  - <span data-ttu-id="25eab-302">月</span><span class="sxs-lookup"><span data-stu-id="25eab-302">Month</span></span>

  - <span data-ttu-id="25eab-303">期间余额</span><span class="sxs-lookup"><span data-stu-id="25eab-303">Period</span></span>

<span data-ttu-id="25eab-304">如果在行中向下展开的程度不足，向下钻取将不起作用。</span><span class="sxs-lookup"><span data-stu-id="25eab-304">If you don’t expand down far enough on a row, the drill-down doesn’t work.</span></span> <span data-ttu-id="25eab-305">例如，如果仅向下展开到主科目类别，则不能向下钻取到余额的 ASE 中，因为主科目是在 ASE 中进行筛选所需的字段。</span><span class="sxs-lookup"><span data-stu-id="25eab-305">For example, if you expand down only to the main account category, you can’t drill down into the ASE on the balance, because the main account is a required field for filtering in the ASE.</span></span>

<span data-ttu-id="25eab-306">如果在行中向下钻取的程度过深，将不把财务报表的额外筛选器发送到 ASE。</span><span class="sxs-lookup"><span data-stu-id="25eab-306">If you expand down too far on a row, the additional filters on the financial statements aren’t sent to the ASE.</span></span> <span data-ttu-id="25eab-307">因此，可能会发现数字有偏差。</span><span class="sxs-lookup"><span data-stu-id="25eab-307">Therefore, you might see a difference in your numbers.</span></span> <span data-ttu-id="25eab-308">例如，如果向下展开到“按地区分类的收入报表”财务报表的行中的国家或地区，则 ASE 中不将该国家或地区包含为筛选器。</span><span class="sxs-lookup"><span data-stu-id="25eab-308">For example, if you expand down to the country or region on the rows of the Income statement by region financial statement, the country or region isn’t be included as a filter in the ASE.</span></span>

> [!NOTE]
> <span data-ttu-id="25eab-309">可在财务报表行或列中继续向下钻取，超过 ASE 当前支持的筛选范围。</span><span class="sxs-lookup"><span data-stu-id="25eab-309">You can drill further down on the financial statement rows or columns than the ASE currently supports for filtering.</span></span> <span data-ttu-id="25eab-310">因此，在某些情况下，ASE 中的详细交易记录总和与您向后钻取的余额不匹配。</span><span class="sxs-lookup"><span data-stu-id="25eab-310">Therefore, in some situations, the sum of detailed transactions in the ASE won’t match the balance that you’re drilling back on.</span></span> <span data-ttu-id="25eab-311">将来将继续增强此功能。</span><span class="sxs-lookup"><span data-stu-id="25eab-311">This functionality will continue to be enhanced in the future.</span></span>

## <a name="hierarchies"></a><span data-ttu-id="25eab-312">层次结构</span><span class="sxs-lookup"><span data-stu-id="25eab-312">Hierarchies</span></span>

<span data-ttu-id="25eab-313">默认财务报表使用两个层次结构钻取和展开数据。</span><span class="sxs-lookup"><span data-stu-id="25eab-313">The default financial statements use two hierarchies to drill and expand on the data.</span></span> <span data-ttu-id="25eab-314">一个层次结构用于行，另一个层次结构用于列。</span><span class="sxs-lookup"><span data-stu-id="25eab-314">One hierarchy is for the rows, and the other hierarchy is for the columns.</span></span> <span data-ttu-id="25eab-315">两个层次结构均是在设计财务报表时预定义的。</span><span class="sxs-lookup"><span data-stu-id="25eab-315">Both hierarchies are predefined in the design of the financial statement.</span></span> <span data-ttu-id="25eab-316">对于大多数财务报表，行层次结构为**主科目类型** > **主科目类别** > **主科目**。</span><span class="sxs-lookup"><span data-stu-id="25eab-316">For most financial statements, the row hierarchy is **Main account type** > **Main account categories** > **Main account**.</span></span> <span data-ttu-id="25eab-317">但是，某些报表有更多字段，如“国家和地区”。</span><span class="sxs-lookup"><span data-stu-id="25eab-317">However, some reports have additional fields, such as Country and Region.</span></span> <span data-ttu-id="25eab-318">层次结构的这些额外节点基于各交易记录的子分类帐数据。</span><span class="sxs-lookup"><span data-stu-id="25eab-318">The additional nodes of the hierarchy are based on subledger data for each transaction.</span></span>

<span data-ttu-id="25eab-319">对于列，层次结构以法人和会计期间为重点。</span><span class="sxs-lookup"><span data-stu-id="25eab-319">For the columns, the hierarchy is focused on the legal entities and the fiscal periods.</span></span> <span data-ttu-id="25eab-320">对于大多数财务报表，列层次结构为**法人** > **会计日历** > **会计年度** > **季度** > **期间**。</span><span class="sxs-lookup"><span data-stu-id="25eab-320">For most financial statements, the column hierarchy is **Legal entity** > **Fiscal calendar** > **Fiscal year** > **Quarter** > **Period**.</span></span>

<span data-ttu-id="25eab-321">现在，财务报表不支持组织层次结构，这种层次结构用于聚合数据。</span><span class="sxs-lookup"><span data-stu-id="25eab-321">Currently, the financial statements don’t support the organizational hierarchies, which let you aggregate data.</span></span>

## <a name="data-limitations"></a><span data-ttu-id="25eab-322">数据限制</span><span class="sxs-lookup"><span data-stu-id="25eab-322">Data limitations</span></span>
<span data-ttu-id="25eab-323">财务报表视觉对象对可显示的行数有限制。</span><span class="sxs-lookup"><span data-stu-id="25eab-323">The financial statement visuals have a limit on the number of rows that can be shown.</span></span> <span data-ttu-id="25eab-324">现在该限制设置为 30,000。</span><span class="sxs-lookup"><span data-stu-id="25eab-324">Currently, the limit is set to 30,000.</span></span> <span data-ttu-id="25eab-325">如果超过此限制，视觉对象将显示一个警告符号，通知您此情况。</span><span class="sxs-lookup"><span data-stu-id="25eab-325">If you exceed this limit, the visual will have a warning symbol to notify you about this situation.</span></span>
 
![数据限制](./media/data-limit.png)


<span data-ttu-id="25eab-327">如果超过了最大值，财务报表中显示的总数将不正确，因为并非所有行都加载到了视觉对象中。</span><span class="sxs-lookup"><span data-stu-id="25eab-327">If the maximum is exceeded, the totals that appear on the financial statement will be incorrect, because not all the rows were loaded into the visual.</span></span>

### <a name="empty-rows"></a><span data-ttu-id="25eab-328">空行</span><span class="sxs-lookup"><span data-stu-id="25eab-328">Empty rows</span></span>
<span data-ttu-id="25eab-329">Power BI 不提供用于隐藏和显示空行的选项。</span><span class="sxs-lookup"><span data-stu-id="25eab-329">Power BI doesn’t provide an option to hide and show empty rows.</span></span> <span data-ttu-id="25eab-330">如果行中没有任何数据，视觉对象中将不显示该行。</span><span class="sxs-lookup"><span data-stu-id="25eab-330">If a row doesn’t have any data, the row won’t appear in the visual.</span></span>

## <a name="what-is-coming-in-future-releases"></a><span data-ttu-id="25eab-331">将来的版本将有哪些更新？</span><span class="sxs-lookup"><span data-stu-id="25eab-331">What is coming in future releases?</span></span>
<span data-ttu-id="25eab-332">将继续增强使用 Power BI 的新工作区和财务报表。</span><span class="sxs-lookup"><span data-stu-id="25eab-332">The new workspaces and financial statements that use Power BI will continue to be enhanced.</span></span> <span data-ttu-id="25eab-333">下面是正在考虑加入将来的版本中的部分新功能：</span><span class="sxs-lookup"><span data-stu-id="25eab-333">Here are some of the new features that are being considered for future releases:</span></span>

 - <span data-ttu-id="25eab-334">复制、编辑、删除和创建视觉对象，甚至财务报表</span><span class="sxs-lookup"><span data-stu-id="25eab-334">The ability to copy, edit, delete, and create visuals, even the financial statements</span></span>                                                  
 - <span data-ttu-id="25eab-335">更多默认报表</span><span class="sxs-lookup"><span data-stu-id="25eab-335">Additional default reports</span></span>                                                                                                            
    - <span data-ttu-id="25eab-336">支持更多子分类帐数据</span><span class="sxs-lookup"><span data-stu-id="25eab-336">Support for additional subledger data</span></span>                                                                                            
 - <span data-ttu-id="25eab-337">支持报告币种</span><span class="sxs-lookup"><span data-stu-id="25eab-337">Support for a reporting currency</span></span>                                                                                                      
 - <span data-ttu-id="25eab-338">为行和列增加自定义计算</span><span class="sxs-lookup"><span data-stu-id="25eab-338">Add custom calculations for rows and columns</span></span>                                                                                          
 - <span data-ttu-id="25eab-339">将财务报表导出到 Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="25eab-339">The ability to export the financial statements to Microsoft Excel</span></span>                                                                     
   - <span data-ttu-id="25eab-340">导出期间保留财务报表的格式。</span><span class="sxs-lookup"><span data-stu-id="25eab-340">Maintain the format of the financial statement during export.</span></span>                                                                          
   - <span data-ttu-id="25eab-341">通过创建数据透视表以使用视觉对象中的信息，在 Excel 中分析数据。</span><span class="sxs-lookup"><span data-stu-id="25eab-341">Analyze data in Excel by creating a Pivot Table that uses the information on the visual.</span></span>                                              
 - <span data-ttu-id="25eab-342">区域设置支持</span><span class="sxs-lookup"><span data-stu-id="25eab-342">Locale support</span></span>                                                                                                                        
 - <span data-ttu-id="25eab-343">可定义报告层次结构，以便定义可在财务报表中用于设计、筛选和安全设置的主科目层次结构或组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="25eab-343">The ability to define reporting hierarchies, so that you can define main account hierarchies or an organizational hierarchy that can be used on financial statements for design, filtering, and security.</span></span>                                                                    
 - <span data-ttu-id="25eab-344">支持打印</span><span class="sxs-lookup"><span data-stu-id="25eab-344">Support for printing</span></span>

<span data-ttu-id="25eab-345">开展相关工作后，将通过路线图网站传达新功能：https://roadmap.dynamics.com/。</span><span class="sxs-lookup"><span data-stu-id="25eab-345">The new features will be communicated through the roadmap website as work is started: https://roadmap.dynamics.com/.</span></span>

## <a name="additional-resources-for-power-bi"></a><span data-ttu-id="25eab-346">适用于 Power BI 的其他资源</span><span class="sxs-lookup"><span data-stu-id="25eab-346">Additional resources for Power BI</span></span>

<span data-ttu-id="25eab-347">在生产环境中，不需要以下资源中的信息即可为 **CFO 概览**或**财务见解**工作区启用嵌入式报表。</span><span class="sxs-lookup"><span data-stu-id="25eab-347">The information in the following resources isn’t required in order to enable the embedded reports for the **CFO overview** or **Financial Insights** workspace in a production environment.</span></span> <span data-ttu-id="25eab-348">不过它们对开发箱很有帮助，而您希望将自己的 Power BI 报表嵌入 Finance and Operations 中时也有帮助。</span><span class="sxs-lookup"><span data-stu-id="25eab-348">Instead, they are helpful for dev boxes and if you want to embed your own Power BI reports into Finance and Operations.</span></span>

<span data-ttu-id="25eab-349">https://blogs.msdn.microsoft.com/dynamicsaxbi/2017/07/29/accessing-analytical-workspaces-on-1box-environment/</span><span class="sxs-lookup"><span data-stu-id="25eab-349">https://blogs.msdn.microsoft.com/dynamicsaxbi/2017/07/29/accessing-analytical-workspaces-on-1box-environment/</span></span>

<span data-ttu-id="25eab-350">https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/add-analytics-tab-workspaces</span><span class="sxs-lookup"><span data-stu-id="25eab-350">https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/add-analytics-tab-workspaces</span></span>

