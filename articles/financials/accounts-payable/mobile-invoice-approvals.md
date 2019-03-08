---
title: 移动发票审核
description: 本主题旨在通过以供应商发票的移动审核为使用案例，在 Dynamics 365 for Finance and Operations 中提供移动方案的设计方法实践。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e39d81b0d600012f936865b53f8556eb3ef0a3d9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "314386"
---
# <a name="mobile-invoice-approvals"></a><span data-ttu-id="53f31-103">移动发票审核</span><span class="sxs-lookup"><span data-stu-id="53f31-103">Mobile invoice approvals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53f31-104">商业用户可通过 Microsoft Dynamics 365 for Finance and Operations 中的移动功能设计移动体验。</span><span class="sxs-lookup"><span data-stu-id="53f31-104">Mobile capabilities in Microsoft Dynamics 365 for Finance and Operations let a business user design mobile experiences.</span></span> <span data-ttu-id="53f31-105">对于高级方案，开发人员还可通过此平台根据需要扩展功能。</span><span class="sxs-lookup"><span data-stu-id="53f31-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="53f31-106">若要了解有关移动的一些新概念，最有效的方法是设计一些新方案。</span><span class="sxs-lookup"><span data-stu-id="53f31-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="53f31-107">本主题旨在通过以供应商发票的移动审核为使用案例，提供移动方案的设计方法实践。</span><span class="sxs-lookup"><span data-stu-id="53f31-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="53f31-108">本主题应该可以帮助您设计这些方案的变型，还可以适用于与供应商发票无关的其他方案。</span><span class="sxs-lookup"><span data-stu-id="53f31-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="53f31-109">必备项</span><span class="sxs-lookup"><span data-stu-id="53f31-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="53f31-110">必备项</span><span class="sxs-lookup"><span data-stu-id="53f31-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="53f31-111">说明</span><span class="sxs-lookup"><span data-stu-id="53f31-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53f31-112">移动手册预习</span><span class="sxs-lookup"><span data-stu-id="53f31-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="53f31-113">移动平台</span><span class="sxs-lookup"><span data-stu-id="53f31-113">Mobile platform</span></span>](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="53f31-114">Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="53f31-114">Dynamics 365 for Finance and Operations</span></span>                                                                             | <span data-ttu-id="53f31-115">已安装了 Microsoft Dynamics 365 for Operations 版本 1611 和 Microsoft Dynamics for Operations 平台更新 3（2016 年 11 月）的环境</span><span class="sxs-lookup"><span data-stu-id="53f31-115">An environment that has Microsoft Dynamics 365 for Operations version 1611 and Microsoft Dynamics for Operations platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="53f31-116">安装修补程序 KB 3204341。</span><span class="sxs-lookup"><span data-stu-id="53f31-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="53f31-117">任务录制器可能错误地为 Dynamics 365 for Operation 平台更新 3（2016 年 11 月更新）中的下拉对话框录制两个关闭命令。</span><span class="sxs-lookup"><span data-stu-id="53f31-117">Task recorder can erroneously record two Close commands for dropdown dialogs this is included in Dynamics 365 for Operation platform update 3 (November 2016 update)</span></span> |
| <span data-ttu-id="53f31-118">安装修补程序 KB 3207800。</span><span class="sxs-lookup"><span data-stu-id="53f31-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="53f31-119">此修补程序允许在 Dynamics 365 for Operation 平台更新 3（2016 年 11 月更新）中的移动客户端上查看附件。</span><span class="sxs-lookup"><span data-stu-id="53f31-119">This hotfix enables attachments to be viewed on the mobile client this is included in Dynamics 365 for Operation platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="53f31-120">安装修补程序 KB 3208224。</span><span class="sxs-lookup"><span data-stu-id="53f31-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="53f31-121">Microsoft Dynamics AX 应用程序 7.0.1（2016 年 5 月）中的移动供应商发票审核应用程序的应用程序代码。</span><span class="sxs-lookup"><span data-stu-id="53f31-121">Application code for the mobile vendor invoice approval application this is included in Microsoft Dynamics AX application 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="53f31-122">为 Finance and Operations 安装了此移动应用程序的 Android、iOS 或 Windows 设备</span><span class="sxs-lookup"><span data-stu-id="53f31-122">An Android or iOS or a Windows device that has the mobile app installed for Finance and Operations</span></span> | <span data-ttu-id="53f31-123">在相应的应用程序商城中搜索该应用程序。</span><span class="sxs-lookup"><span data-stu-id="53f31-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="53f31-124">简介</span><span class="sxs-lookup"><span data-stu-id="53f31-124">Introduction</span></span>
<span data-ttu-id="53f31-125">供应商发票的移动审核需要“必备条件”部分中提到的三个修补程序。</span><span class="sxs-lookup"><span data-stu-id="53f31-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="53f31-126">这些修补程序不为发票审核提供工作区。</span><span class="sxs-lookup"><span data-stu-id="53f31-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="53f31-127">若要了解移动上下文中的工作区是什么，请阅读“必备条件”部分中提到的移动手册。</span><span class="sxs-lookup"><span data-stu-id="53f31-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="53f31-128">必须设计发票审核工作区。</span><span class="sxs-lookup"><span data-stu-id="53f31-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="53f31-129">每个组织都以不同方式为供应商发票编排和定义自己的业务流程。</span><span class="sxs-lookup"><span data-stu-id="53f31-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="53f31-130">为供应商发票审核设计移动体验时，应考虑以下业务流程因素。</span><span class="sxs-lookup"><span data-stu-id="53f31-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="53f31-131">观点是尽量使用这些数据点优化设备上的用户体验。</span><span class="sxs-lookup"><span data-stu-id="53f31-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="53f31-132">用户希望在移动体验中看到发票抬头中的哪些字段？其顺序如何？</span><span class="sxs-lookup"><span data-stu-id="53f31-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="53f31-133">用户希望在移动体验中看到发票行中的哪些字段？其顺序如何？</span><span class="sxs-lookup"><span data-stu-id="53f31-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="53f31-134">一个发票中有多少个发票行？</span><span class="sxs-lookup"><span data-stu-id="53f31-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="53f31-135">在此处应用 80-20 规则，并针对 80% 进行优化。</span><span class="sxs-lookup"><span data-stu-id="53f31-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="53f31-136">用户是否希望检查期间在移动设备上显示会计分配（发票编码）？</span><span class="sxs-lookup"><span data-stu-id="53f31-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="53f31-137">如果此问题的答案为是，请注意以下问题：</span><span class="sxs-lookup"><span data-stu-id="53f31-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="53f31-138">一个发票行有多少个会计分配（延伸价格、销售税、费用、拆分等）？</span><span class="sxs-lookup"><span data-stu-id="53f31-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="53f31-139">再次应用 80-20 规则。</span><span class="sxs-lookup"><span data-stu-id="53f31-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="53f31-140">发票的发票抬头中是否也有会计分配？</span><span class="sxs-lookup"><span data-stu-id="53f31-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="53f31-141">如果有，这些会计分配在设备上是否可用？</span><span class="sxs-lookup"><span data-stu-id="53f31-141">If so, should these accounting distributions be available on the device?</span></span>

> [!NOTE]
> <span data-ttu-id="53f31-142">此主题不介绍如何编辑会计分配，因为此功能现在不支持移动方案。</span><span class="sxs-lookup"><span data-stu-id="53f31-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="53f31-143">用户是否要在设备上查看发票的附件？</span><span class="sxs-lookup"><span data-stu-id="53f31-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="53f31-144">发票审核的移动体验设计将有所不同，具体取决于这些问题的答案。</span><span class="sxs-lookup"><span data-stu-id="53f31-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="53f31-145">目标是优化组织中移动业务流程的用户体验。</span><span class="sxs-lookup"><span data-stu-id="53f31-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="53f31-146">本文的其他部分中，我们将查看两个方案变型，这两个变型基于前面问题的不同答案。</span><span class="sxs-lookup"><span data-stu-id="53f31-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="53f31-147">在使用移动设计器时，通常需要确保“发布”更改，以防丢失更新。</span><span class="sxs-lookup"><span data-stu-id="53f31-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="53f31-148">为 Contoso 设计简单发票审核方案</span><span class="sxs-lookup"><span data-stu-id="53f31-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="53f31-149">方案属性</span><span class="sxs-lookup"><span data-stu-id="53f31-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="53f31-150">答卷</span><span class="sxs-lookup"><span data-stu-id="53f31-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="53f31-151">用户希望在移动体验中看到发票抬头中的哪些字段？其顺序如何？</span><span class="sxs-lookup"><span data-stu-id="53f31-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="53f31-152">供应商名称</span><span class="sxs-lookup"><span data-stu-id="53f31-152">Vendor name</span></span></li>
<li><span data-ttu-id="53f31-153">发票合计</span><span class="sxs-lookup"><span data-stu-id="53f31-153">Invoice total</span></span></li>
<li><span data-ttu-id="53f31-154">发票帐户</span><span class="sxs-lookup"><span data-stu-id="53f31-154">Invoice account</span></span></li>
<li><span data-ttu-id="53f31-155">发票编号</span><span class="sxs-lookup"><span data-stu-id="53f31-155">Invoice number</span></span></li>
<li><span data-ttu-id="53f31-156">发票日期</span><span class="sxs-lookup"><span data-stu-id="53f31-156">Invoice date</span></span></li>
<li><span data-ttu-id="53f31-157">发票描述</span><span class="sxs-lookup"><span data-stu-id="53f31-157">Invoice description</span></span></li>
<li><span data-ttu-id="53f31-158">到期日期</span><span class="sxs-lookup"><span data-stu-id="53f31-158">Due date</span></span></li>
<li><span data-ttu-id="53f31-159">发票币种</span><span class="sxs-lookup"><span data-stu-id="53f31-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53f31-160">用户希望在移动体验中看到发票行中的哪些字段？其顺序如何？</span><span class="sxs-lookup"><span data-stu-id="53f31-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="53f31-161">采购类别</span><span class="sxs-lookup"><span data-stu-id="53f31-161">Procurement category</span></span></li>
<li><span data-ttu-id="53f31-162">数量</span><span class="sxs-lookup"><span data-stu-id="53f31-162">Quantity</span></span></li>
<li><span data-ttu-id="53f31-163">单价</span><span class="sxs-lookup"><span data-stu-id="53f31-163">Unit price</span></span></li>
<li><span data-ttu-id="53f31-164">行净额</span><span class="sxs-lookup"><span data-stu-id="53f31-164">Line net amount</span></span></li>
<li><span data-ttu-id="53f31-165">1099 金额</span><span class="sxs-lookup"><span data-stu-id="53f31-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53f31-166">一个发票中有多少个发票行？</span><span class="sxs-lookup"><span data-stu-id="53f31-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="53f31-167">在此处应用 80-20 规则，并针对 80% 进行优化。</span><span class="sxs-lookup"><span data-stu-id="53f31-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="53f31-168">1</span><span class="sxs-lookup"><span data-stu-id="53f31-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53f31-169">用户是否希望检查期间在移动设备上显示会计分配（发票编码）？</span><span class="sxs-lookup"><span data-stu-id="53f31-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="53f31-170">是</span><span class="sxs-lookup"><span data-stu-id="53f31-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53f31-171">一个发票行有多少个会计分配（延伸价格、销售税、费用等）？</span><span class="sxs-lookup"><span data-stu-id="53f31-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="53f31-172">再次应用 80-20 规则。</span><span class="sxs-lookup"><span data-stu-id="53f31-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="53f31-173">延伸价格：2，销售税：0，费用：0</span><span class="sxs-lookup"><span data-stu-id="53f31-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53f31-174">发票的发票抬头中是否也有会计分配？</span><span class="sxs-lookup"><span data-stu-id="53f31-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="53f31-175">如果有，这些会计分配在设备上是否可用？</span><span class="sxs-lookup"><span data-stu-id="53f31-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="53f31-176">未使用</span><span class="sxs-lookup"><span data-stu-id="53f31-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53f31-177">用户是否要在设备上查看发票的附件？</span><span class="sxs-lookup"><span data-stu-id="53f31-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="53f31-178">是</span><span class="sxs-lookup"><span data-stu-id="53f31-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="53f31-179">创建工作区</span><span class="sxs-lookup"><span data-stu-id="53f31-179">Create the workspace</span></span>

1.  <span data-ttu-id="53f31-180">在浏览器中，打开 Finance and Operations 并登录。</span><span class="sxs-lookup"><span data-stu-id="53f31-180">In a browser, open Finance and Operations, and sign in.</span></span>
2.  <span data-ttu-id="53f31-181">登录之后，按照以下示例所示将 **&mode=mobile** 追加到 URL，然后刷新页面：https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="53f31-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span></span>
3.  <span data-ttu-id="53f31-182">单击页面右上角的**设置**（齿轮）按钮，然后单击**移动应用程序**。</span><span class="sxs-lookup"><span data-stu-id="53f31-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="53f31-183">任务录制器显示时，移动应用程序设计器也必须显示。</span><span class="sxs-lookup"><span data-stu-id="53f31-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="53f31-184">单击**添加**以创建新工作区。</span><span class="sxs-lookup"><span data-stu-id="53f31-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="53f31-185">对于此示例，请将该工作区命名为**我的审核**。</span><span class="sxs-lookup"><span data-stu-id="53f31-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="53f31-186">输入描述。</span><span class="sxs-lookup"><span data-stu-id="53f31-186">Enter a description.</span></span>
6.  <span data-ttu-id="53f31-187">选择工作区颜色。</span><span class="sxs-lookup"><span data-stu-id="53f31-187">Select a workspace color.</span></span> <span data-ttu-id="53f31-188">此工作区颜色将用于此工作区的移动体验的整体样式。</span><span class="sxs-lookup"><span data-stu-id="53f31-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="53f31-189">为该工作区选择图标。</span><span class="sxs-lookup"><span data-stu-id="53f31-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="53f31-190">单击**完成**。</span><span class="sxs-lookup"><span data-stu-id="53f31-190">Click **Done**</span></span>
9.  <span data-ttu-id="53f31-191">单击**发布工作区**以保存更改。</span><span class="sxs-lookup"><span data-stu-id="53f31-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="53f31-192">分配给我的供应商发票</span><span class="sxs-lookup"><span data-stu-id="53f31-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="53f31-193">应设计的第一个移动页面是为用户分配以待检查的发票列表。</span><span class="sxs-lookup"><span data-stu-id="53f31-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="53f31-194">若要设计此移动页面，请使用 Finance and Operations 中的 **VendMobileInvoiceAssignedToMeListPage** 页面。</span><span class="sxs-lookup"><span data-stu-id="53f31-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page in Finance and Operations.</span></span> <span data-ttu-id="53f31-195">完成此过程，请确保为您分配至少一个供应商发票进行检查，并且发票行有两个分配。</span><span class="sxs-lookup"><span data-stu-id="53f31-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="53f31-196">此设置满足该方案的要求。</span><span class="sxs-lookup"><span data-stu-id="53f31-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="53f31-197">在 Finance and Operations URL 中，将菜单项的名称替换为 **VendMobileInvoiceAssignedToMeListPage**，以便在**应付账款**模块中打开**分配给我的待定供应商发票**列表页面的移动版本。</span><span class="sxs-lookup"><span data-stu-id="53f31-197">In the Finance and Operations URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="53f31-198">此页面根据系统中为您分配的发票数量显示这些发票。</span><span class="sxs-lookup"><span data-stu-id="53f31-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="53f31-199">若要查找特定发票，必须使用左侧的筛选器。</span><span class="sxs-lookup"><span data-stu-id="53f31-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="53f31-200">但是，此示例不需要特定发票。</span><span class="sxs-lookup"><span data-stu-id="53f31-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="53f31-201">只需要为您分配某张发票，这将允许您设计移动页面。</span><span class="sxs-lookup"><span data-stu-id="53f31-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="53f31-202">已专门为供应商发票的移动方案设计可用新页面。</span><span class="sxs-lookup"><span data-stu-id="53f31-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="53f31-203">因此，您必须使用这些页面。</span><span class="sxs-lookup"><span data-stu-id="53f31-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="53f31-204">此 URL 应类似以下 URL，并且输入该 URL 之后，必须显示下图中显示的页面：https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![“分配给我的待定供应商发票”页面](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="53f31-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
2.  <span data-ttu-id="53f31-205">单击页面右上角的**设置**（齿轮）按钮，然后单击**移动应用程序**</span><span class="sxs-lookup"><span data-stu-id="53f31-205">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="53f31-206">选择您的工作区，然后单击**编辑**</span><span class="sxs-lookup"><span data-stu-id="53f31-206">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="53f31-207">单击**添加页面**创建第一个移动页面。</span><span class="sxs-lookup"><span data-stu-id="53f31-207">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="53f31-208">输入名称（如**我的供应商发票**）和描述（如**分配给我检查的供应商发票**）。</span><span class="sxs-lookup"><span data-stu-id="53f31-208">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="53f31-209">单击**完成**。</span><span class="sxs-lookup"><span data-stu-id="53f31-209">Click **Done**.</span></span>
7.  <span data-ttu-id="53f31-210">在移动设计器中的**字段**选项卡上，单击**选择字段**。</span><span class="sxs-lookup"><span data-stu-id="53f31-210">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="53f31-211">列表页面上的列必须类似下图。</span><span class="sxs-lookup"><span data-stu-id="53f31-211">The columns on the list page must resemble the following illustration.</span></span> <span data-ttu-id="53f31-212">[![“分配给我的待定供应商发票”页面上的列](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="53f31-212">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
8.  <span data-ttu-id="53f31-213">从列表页面添加必须在移动页面中向用户显示的所需列。</span><span class="sxs-lookup"><span data-stu-id="53f31-213">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="53f31-214">添加顺序为字段向最终用户显示的顺序。</span><span class="sxs-lookup"><span data-stu-id="53f31-214">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="53f31-215">只能通过重新选择所有字段才能更改字段的顺序。</span><span class="sxs-lookup"><span data-stu-id="53f31-215">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="53f31-216">根据此方案的要求，需要下面的八个字段：</span><span class="sxs-lookup"><span data-stu-id="53f31-216">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="53f31-217">但是，某些用户可能会认为八个字段在移动设备上提供的信息太多。</span><span class="sxs-lookup"><span data-stu-id="53f31-217">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="53f31-218">因此，我们将在移动列表视图中仅显示最重要的字段。</span><span class="sxs-lookup"><span data-stu-id="53f31-218">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="53f31-219">其余字段将在我们以后将设计的详细信息视图中显示。</span><span class="sxs-lookup"><span data-stu-id="53f31-219">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="53f31-220">现在我们将仅添加以下字段。</span><span class="sxs-lookup"><span data-stu-id="53f31-220">For now, we will add the following fields.</span></span> <span data-ttu-id="53f31-221">单击这些列中的加号 (**+**) 添加到移动页面。</span><span class="sxs-lookup"><span data-stu-id="53f31-221">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="53f31-222">供应商名称</span><span class="sxs-lookup"><span data-stu-id="53f31-222">Vendor name</span></span>
    - <span data-ttu-id="53f31-223">发票合计</span><span class="sxs-lookup"><span data-stu-id="53f31-223">Invoice total</span></span>
    - <span data-ttu-id="53f31-224">发票帐户</span><span class="sxs-lookup"><span data-stu-id="53f31-224">Invoice account</span></span>
    - <span data-ttu-id="53f31-225">发票编号</span><span class="sxs-lookup"><span data-stu-id="53f31-225">Invoice number</span></span>
    - <span data-ttu-id="53f31-226">发票日期</span><span class="sxs-lookup"><span data-stu-id="53f31-226">Invoice date</span></span>

    <span data-ttu-id="53f31-227">添加字段之后，移动页面必须类似下图。</span><span class="sxs-lookup"><span data-stu-id="53f31-227">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    <span data-ttu-id="53f31-228">[![添加字段后的页面](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="53f31-228">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>
9.  <span data-ttu-id="53f31-229">还必须立即添加以下列，以便在以后启用工作流操作。</span><span class="sxs-lookup"><span data-stu-id="53f31-229">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="53f31-230">显示已完成任务</span><span class="sxs-lookup"><span data-stu-id="53f31-230">Show complete task</span></span>
    - <span data-ttu-id="53f31-231">显示委托任务</span><span class="sxs-lookup"><span data-stu-id="53f31-231">Show delegate task</span></span>
    - <span data-ttu-id="53f31-232">显示撤消任务</span><span class="sxs-lookup"><span data-stu-id="53f31-232">Show recall task</span></span>
    - <span data-ttu-id="53f31-233">显示拒绝任务</span><span class="sxs-lookup"><span data-stu-id="53f31-233">Show reject task</span></span>
    - <span data-ttu-id="53f31-234">显示请求完成任务</span><span class="sxs-lookup"><span data-stu-id="53f31-234">Show request completion task</span></span>
    - <span data-ttu-id="53f31-235">显示重新提交任务</span><span class="sxs-lookup"><span data-stu-id="53f31-235">Show resubmit task</span></span>

10. <span data-ttu-id="53f31-236">单击**完成**退出编辑模式。</span><span class="sxs-lookup"><span data-stu-id="53f31-236">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="53f31-237">单击**后退**，然后单击**完成**退出工作区</span><span class="sxs-lookup"><span data-stu-id="53f31-237">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="53f31-238">单击**发布工作区**以保存工作。</span><span class="sxs-lookup"><span data-stu-id="53f31-238">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="53f31-239">在“应付账款参数”窗体中的**发票**下，启用**在待定供应商发票列表中显示发票总计**。</span><span class="sxs-lookup"><span data-stu-id="53f31-239">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="53f31-240">请注意，只有通过启用此参数，才能计算发票总计并在待定供应商发票列表页面中显示。</span><span class="sxs-lookup"><span data-stu-id="53f31-240">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="53f31-241">这是必备修补程序 3208224 中的一项新功能。</span><span class="sxs-lookup"><span data-stu-id="53f31-241">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="53f31-242">供应商发票明细</span><span class="sxs-lookup"><span data-stu-id="53f31-242">Vendor invoice details</span></span>

<span data-ttu-id="53f31-243">若要为移动设计发票明细页面，请使用 Finance and Operations 中的 **VendMobileInvoiceHeaderDetails** 页面。</span><span class="sxs-lookup"><span data-stu-id="53f31-243">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page in Finance and Operations.</span></span> <span data-ttu-id="53f31-244">请注意，此页面根据您在系统中的发票数量，显示时间最久的发票（即最先创建的发票）。</span><span class="sxs-lookup"><span data-stu-id="53f31-244">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="53f31-245">若要查找特定发票，必须使用左侧的筛选器。</span><span class="sxs-lookup"><span data-stu-id="53f31-245">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="53f31-246">但是，此示例不需要特定发票。</span><span class="sxs-lookup"><span data-stu-id="53f31-246">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="53f31-247">我们仅需要一些发票数据，以便设计移动页面。</span><span class="sxs-lookup"><span data-stu-id="53f31-247">We just require some invoice data so that we can design the mobile page.</span></span> <span data-ttu-id="53f31-248">[![工作流页面](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="53f31-248">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1. <span data-ttu-id="53f31-249">在 Finance and Operations URL 中，将菜单项的名称替换为 **VendMobileInvoiceHeaderDetails** 以打开窗体</span><span class="sxs-lookup"><span data-stu-id="53f31-249">In the Finance and Operations URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>
2. <span data-ttu-id="53f31-250">通过**设置**（齿轮）按钮打开移动设计器。</span><span class="sxs-lookup"><span data-stu-id="53f31-250">Open the mobile designer from the **Settings** (gear) button.</span></span>
3. <span data-ttu-id="53f31-251">单击**编辑**按钮在工作区中启动编辑模式。</span><span class="sxs-lookup"><span data-stu-id="53f31-251">Click the **Edit** button to start edit mode in the workspace.</span></span>
4. <span data-ttu-id="53f31-252">选择前面创建的**我的供应商发票**页面，然后单击**编辑**。</span><span class="sxs-lookup"><span data-stu-id="53f31-252">Select the **My vendor invoices** page that you created earlier, and then click **Edit**.</span></span>
5. <span data-ttu-id="53f31-253">在**字段**选项卡上，单击**窗格**列标题。</span><span class="sxs-lookup"><span data-stu-id="53f31-253">On the **Fields** tab, click the **Grid** column heading.</span></span>
6. <span data-ttu-id="53f31-254">单击**属性 &gt; 添加**页面。</span><span class="sxs-lookup"><span data-stu-id="53f31-254">Click **Properties &gt; Add page**.</span></span> <span data-ttu-id="53f31-255">**注释：** 单击**窗格**标题并添加页面时，将自动建立与明细页面之间的关系。</span><span class="sxs-lookup"><span data-stu-id="53f31-255">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>
7. <span data-ttu-id="53f31-256">输入页面标题（如**发票明细**）和描述（如**查看发票抬头和行明细**）。</span><span class="sxs-lookup"><span data-stu-id="53f31-256">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>
8. <span data-ttu-id="53f31-257">单击**选择字段**。</span><span class="sxs-lookup"><span data-stu-id="53f31-257">Click **Select fields**.</span></span> <span data-ttu-id="53f31-258">请注意，添加顺序为字段向最终用户显示的顺序。</span><span class="sxs-lookup"><span data-stu-id="53f31-258">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="53f31-259">只能通过重新选择所有字段才能更改字段的顺序。</span><span class="sxs-lookup"><span data-stu-id="53f31-259">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 
9. <span data-ttu-id="53f31-260">根据此方案的要求，从抬头添加以下字段：</span><span class="sxs-lookup"><span data-stu-id="53f31-260">Add the following fields from the header, based on the requirements for this scenario:</span></span>
   - <span data-ttu-id="53f31-261">供应商名称</span><span class="sxs-lookup"><span data-stu-id="53f31-261">Vendor name</span></span>
   - <span data-ttu-id="53f31-262">发票合计</span><span class="sxs-lookup"><span data-stu-id="53f31-262">Invoice total</span></span>
   - <span data-ttu-id="53f31-263">发票帐户</span><span class="sxs-lookup"><span data-stu-id="53f31-263">Invoice account</span></span>
   - <span data-ttu-id="53f31-264">发票编号</span><span class="sxs-lookup"><span data-stu-id="53f31-264">Invoice number</span></span>
   - <span data-ttu-id="53f31-265">发票日期</span><span class="sxs-lookup"><span data-stu-id="53f31-265">Invoice date</span></span>
   - <span data-ttu-id="53f31-266">发票描述</span><span class="sxs-lookup"><span data-stu-id="53f31-266">Invoice description</span></span>
   - <span data-ttu-id="53f31-267">到期日期</span><span class="sxs-lookup"><span data-stu-id="53f31-267">Due date</span></span>
   - <span data-ttu-id="53f31-268">发票币种</span><span class="sxs-lookup"><span data-stu-id="53f31-268">Invoice currency</span></span>

10. <span data-ttu-id="53f31-269">从页面中的行窗格添加以下字段：</span><span class="sxs-lookup"><span data-stu-id="53f31-269">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="53f31-270">采购类别</span><span class="sxs-lookup"><span data-stu-id="53f31-270">Procurement category</span></span>
    - <span data-ttu-id="53f31-271">数量</span><span class="sxs-lookup"><span data-stu-id="53f31-271">Quantity</span></span>
    - <span data-ttu-id="53f31-272">单价</span><span class="sxs-lookup"><span data-stu-id="53f31-272">Unit price</span></span>
    - <span data-ttu-id="53f31-273">行净额</span><span class="sxs-lookup"><span data-stu-id="53f31-273">Line net amount</span></span>
    - <span data-ttu-id="53f31-274">1099 金额</span><span class="sxs-lookup"><span data-stu-id="53f31-274">1099 amount</span></span>

11. <span data-ttu-id="53f31-275">添加了前面两步骤中的所有字段之后，单击**完成**。</span><span class="sxs-lookup"><span data-stu-id="53f31-275">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="53f31-276">此页面必须类似下图。</span><span class="sxs-lookup"><span data-stu-id="53f31-276">The page must resemble the following illustration.</span></span>
    <span data-ttu-id="53f31-277">[![添加字段后的页面](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="53f31-277">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>
12. <span data-ttu-id="53f31-278">单击**完成**退出编辑模式。</span><span class="sxs-lookup"><span data-stu-id="53f31-278">Click **Done** to exit edit mode.</span></span>
13. <span data-ttu-id="53f31-279">单击**后退**，然后单击**完成**退出工作区</span><span class="sxs-lookup"><span data-stu-id="53f31-279">Click **Back** and then **Done** to exit the workspace</span></span>
14. <span data-ttu-id="53f31-280">单击**发布工作区**以保存工作</span><span class="sxs-lookup"><span data-stu-id="53f31-280">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="53f31-281">工作流操作</span><span class="sxs-lookup"><span data-stu-id="53f31-281">Workflow actions</span></span>

<span data-ttu-id="53f31-282">若要添加工作流操作，请使用 Finance and Operations 中的 **VendMobileInvoiceHeaderDetails** 页面。</span><span class="sxs-lookup"><span data-stu-id="53f31-282">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page in Finance and Operations.</span></span> <span data-ttu-id="53f31-283">若要打开此页面，请替换 URL 中的菜单项名称，如前面执行的操作。</span><span class="sxs-lookup"><span data-stu-id="53f31-283">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="53f31-284">然后通过**设置**（齿轮）按钮打开移动设计器。</span><span class="sxs-lookup"><span data-stu-id="53f31-284">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="53f31-285">执行以下步骤在明细页面上添加工作流操作。</span><span class="sxs-lookup"><span data-stu-id="53f31-285">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="53f31-286">您必须将状态为可提供您要设计的工作流操作的发票分配给您。</span><span class="sxs-lookup"><span data-stu-id="53f31-286">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="53f31-287">记录工作流操作</span><span class="sxs-lookup"><span data-stu-id="53f31-287">Record workflow actions</span></span>
1.  <span data-ttu-id="53f31-288">单击**编辑**按钮在工作区中启动编辑模式。</span><span class="sxs-lookup"><span data-stu-id="53f31-288">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="53f31-289">选择前面创建的**发票明细**页面，然后单击**编辑**。</span><span class="sxs-lookup"><span data-stu-id="53f31-289">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="53f31-290">在**操作**选项卡上，单击**添加操作**。</span><span class="sxs-lookup"><span data-stu-id="53f31-290">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="53f31-291">输入操作标题（如**审核**）和描述（如**审核发票**）。</span><span class="sxs-lookup"><span data-stu-id="53f31-291">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="53f31-292">请注意，此处输入的操作标题将成为移动应用程序中对用户显示的操作名称。</span><span class="sxs-lookup"><span data-stu-id="53f31-292">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="53f31-293">单击**完成**。</span><span class="sxs-lookup"><span data-stu-id="53f31-293">Click **Done**.</span></span>
6.  <span data-ttu-id="53f31-294">单击**选择字段**。</span><span class="sxs-lookup"><span data-stu-id="53f31-294">Click **Select fields**.</span></span>
7.  <span data-ttu-id="53f31-295">完成 **VendMobileInvoiceHeaderDetails** 页面中的工作流流程，然后完成要录制的操作。</span><span class="sxs-lookup"><span data-stu-id="53f31-295">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="53f31-296">确保此流程中输入工作流注释，这样移动体验中也会包括注释字段。</span><span class="sxs-lookup"><span data-stu-id="53f31-296">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="53f31-297">运行工作流操作后，单击**完成**完成“选择字段”任务。</span><span class="sxs-lookup"><span data-stu-id="53f31-297">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="53f31-298">单击**完成**退出编辑模式。</span><span class="sxs-lookup"><span data-stu-id="53f31-298">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="53f31-299">单击**后退**，然后单击**完成**退出工作区</span><span class="sxs-lookup"><span data-stu-id="53f31-299">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="53f31-300">单击**发布工作区**以保存工作</span><span class="sxs-lookup"><span data-stu-id="53f31-300">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="53f31-301">重复前面的步骤，记录需要的所有工作流操作。</span><span class="sxs-lookup"><span data-stu-id="53f31-301">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="53f31-302">创建 .js 文件</span><span class="sxs-lookup"><span data-stu-id="53f31-302">Create a .js file</span></span>
1. <span data-ttu-id="53f31-303">打开“记事本”或 Microsoft Visual Studio，然后粘贴以下代码。</span><span class="sxs-lookup"><span data-stu-id="53f31-303">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="53f31-304">将文件保存为 .js 文件。</span><span class="sxs-lookup"><span data-stu-id="53f31-304">Save the file as a .js file.</span></span> <span data-ttu-id="53f31-305">此代码执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="53f31-305">This code does the following:</span></span>
    - <span data-ttu-id="53f31-306">隐藏我们前面在移动列表页面中添加且与工作流有关的额外列。</span><span class="sxs-lookup"><span data-stu-id="53f31-306">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="53f31-307">我们添加这些列是为了让应用程序在上下文中有这些信息，并且可以执行下一步。</span><span class="sxs-lookup"><span data-stu-id="53f31-307">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="53f31-308">它根据处于活动状态的工作流步骤应用逻辑，以便仅显示这些操作。</span><span class="sxs-lookup"><span data-stu-id="53f31-308">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

> [!NOTE]
> <span data-ttu-id="53f31-309">这些页面和代码中的其他控件的名称必须与工作区中的名称相同。</span><span class="sxs-lookup"><span data-stu-id="53f31-309">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }

2.  <span data-ttu-id="53f31-310">通过选择**逻辑**选项卡，将该代码文件上传到工作区。</span><span class="sxs-lookup"><span data-stu-id="53f31-310">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="53f31-311">单击**完成**退出编辑模式。</span><span class="sxs-lookup"><span data-stu-id="53f31-311">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="53f31-312">单击**后退**，然后单击**完成**退出工作区</span><span class="sxs-lookup"><span data-stu-id="53f31-312">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="53f31-313">单击**发布工作区**以保存工作</span><span class="sxs-lookup"><span data-stu-id="53f31-313">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="53f31-314">供应商发票附件</span><span class="sxs-lookup"><span data-stu-id="53f31-314">Vendor invoice attachments</span></span>

1. <span data-ttu-id="53f31-315">单击页面右上角的**设置**（齿轮）按钮，然后单击**移动应用程序**</span><span class="sxs-lookup"><span data-stu-id="53f31-315">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
2. <span data-ttu-id="53f31-316">单击**编辑**按钮在工作区中启动编辑模式。</span><span class="sxs-lookup"><span data-stu-id="53f31-316">Click the **Edit** button to start edit mode in the workspace.</span></span>
3. <span data-ttu-id="53f31-317">选择前面创建的<strong>发票明细</strong>页面，然后单击**编辑**。</span><span class="sxs-lookup"><span data-stu-id="53f31-317">Select the <strong>Invoice details \*\*page that you created earlier, and then click \*\*Edit</strong>.</span></span>
4. <span data-ttu-id="53f31-318">将**文档管理**选项设置为**是**，如下所示。</span><span class="sxs-lookup"><span data-stu-id="53f31-318">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="53f31-319">**注释：** 如果需要在移动设备上显示附件，可以让此选项保留为**否**（这是默认设置）。</span><span class="sxs-lookup"><span data-stu-id="53f31-319">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
   <span data-ttu-id="53f31-320">![文档管理](./media/docmanagement-216x300.png)</span><span class="sxs-lookup"><span data-stu-id="53f31-320">![Document management](./media/docmanagement-216x300.png)</span></span>
5. <span data-ttu-id="53f31-321">单击**完成**退出编辑模式。</span><span class="sxs-lookup"><span data-stu-id="53f31-321">Click **Done** to exit edit mode.</span></span>
6. <span data-ttu-id="53f31-322">单击**后退**，然后单击**完成**退出工作区</span><span class="sxs-lookup"><span data-stu-id="53f31-322">Click **Back** and then **Done** to exit the workspace</span></span>
7. <span data-ttu-id="53f31-323">单击**发布工作区**以保存工作</span><span class="sxs-lookup"><span data-stu-id="53f31-323">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="53f31-324">供应商发票行配送</span><span class="sxs-lookup"><span data-stu-id="53f31-324">Vendor invoice line distributions</span></span>

<span data-ttu-id="53f31-325">此方案的要求确认将仅有行级别的分配，并且一张发票始终只有一行。</span><span class="sxs-lookup"><span data-stu-id="53f31-325">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="53f31-326">由于此方案非常简单，所以移动设备上的用户体验还必须足够简单，这样用户才不必向下滚动多次即可查看分配。</span><span class="sxs-lookup"><span data-stu-id="53f31-326">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="53f31-327">Finance and Operations 中的供应商发票包含用于显示发票抬头中的所有分配的选项。</span><span class="sxs-lookup"><span data-stu-id="53f31-327">Vendor invoices in Finance and Operations include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="53f31-328">此体验正是移动方案需要的。</span><span class="sxs-lookup"><span data-stu-id="53f31-328">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="53f31-329">因此，我们将使用 **VendMobileInvoiceAllDistributionTree** 页面设计移动方案的此部分。</span><span class="sxs-lookup"><span data-stu-id="53f31-329">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="53f31-330">了解要求可以帮助我们在设计方案时确定要使用哪个特定页面和到底如何为用户优化移动体验。</span><span class="sxs-lookup"><span data-stu-id="53f31-330">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="53f31-331">在第二个方案中，我们将使用其他页面显示分配，因为该方案的要求不同。</span><span class="sxs-lookup"><span data-stu-id="53f31-331">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="53f31-332">在 URL 中，替换 URL 中的菜单项名称，如前面执行的操作。</span><span class="sxs-lookup"><span data-stu-id="53f31-332">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="53f31-333">显示的页面应类似下图。</span><span class="sxs-lookup"><span data-stu-id="53f31-333">The page that appears should resemble the following illustration.</span></span>
<span data-ttu-id="53f31-334">[![“全部分配”页面](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="53f31-334">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>
2.  <span data-ttu-id="53f31-335">通过**设置**（齿轮）按钮打开移动设计器。</span><span class="sxs-lookup"><span data-stu-id="53f31-335">Open the mobile designer from the **Settings** (gear) button.</span></span>
3.  <span data-ttu-id="53f31-336">单击**编辑**按钮在工作区中启动编辑模式。</span><span class="sxs-lookup"><span data-stu-id="53f31-336">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="53f31-337">**注释：** 您将发现自动创建了两个新页面。</span><span class="sxs-lookup"><span data-stu-id="53f31-337">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="53f31-338">系统之所以创建这些页面，是因为您在上一部分中开启了文档管理。</span><span class="sxs-lookup"><span data-stu-id="53f31-338">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="53f31-339">您可以忽略这些新页面。</span><span class="sxs-lookup"><span data-stu-id="53f31-339">You can ignore these new pages.</span></span>
4.  <span data-ttu-id="53f31-340">单击**添加页面**。</span><span class="sxs-lookup"><span data-stu-id="53f31-340">Click **Add page**.</span></span>
5.  <span data-ttu-id="53f31-341">输入页面标题（如**查看会计**）和描述（如**查看发票的会计**）。</span><span class="sxs-lookup"><span data-stu-id="53f31-341">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>
6.  <span data-ttu-id="53f31-342">单击**完成**。</span><span class="sxs-lookup"><span data-stu-id="53f31-342">Click **Done**.</span></span>
7.  <span data-ttu-id="53f31-343">在**字段**选项卡上，单击**选择字段**，从分配页面选择以下字段，然后单击**完成**。</span><span class="sxs-lookup"><span data-stu-id="53f31-343">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="53f31-344">本币金额</span><span class="sxs-lookup"><span data-stu-id="53f31-344">Amount</span></span>
    2.  <span data-ttu-id="53f31-345">币种</span><span class="sxs-lookup"><span data-stu-id="53f31-345">Currency</span></span>
    3.  <span data-ttu-id="53f31-346">会计科目</span><span class="sxs-lookup"><span data-stu-id="53f31-346">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="53f31-347">我们未从分配网格选择**描述**列，因为此方案的要求确认只有延伸价格才是有分配的金额。</span><span class="sxs-lookup"><span data-stu-id="53f31-347">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="53f31-348">因此，我们不需要再一个字段来确定分配针对的金额类型。</span><span class="sxs-lookup"><span data-stu-id="53f31-348">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="53f31-349">但是在下一个方案中，**将**使用此信息，因为该方案的要求指定，其他金额类型有分配（如销售税）。</span><span class="sxs-lookup"><span data-stu-id="53f31-349">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>
8.  <span data-ttu-id="53f31-350">单击**完成**退出编辑模式。</span><span class="sxs-lookup"><span data-stu-id="53f31-350">Click **Done** to exit edit mode.</span></span>
9.  <span data-ttu-id="53f31-351">单击**后退**，然后单击**完成**退出工作区</span><span class="sxs-lookup"><span data-stu-id="53f31-351">Click **Back** and then **Done** to exit the workspace</span></span>
10. <span data-ttu-id="53f31-352">单击**发布工作区**以保存工作</span><span class="sxs-lookup"><span data-stu-id="53f31-352">Click **Publish workspace** to save your work</span></span>

> [!NOTE] 
> <span data-ttu-id="53f31-353">**查看会计**移动页面现在未链接到我们迄今为止设计的任何移动页面。</span><span class="sxs-lookup"><span data-stu-id="53f31-353">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="53f31-354">因为用户应该可以从移动设备上的**发票明细**页面导航到**查看会计**页面，所以我们必须提供从**发票明细**页面到**查看会计**页面的导航。</span><span class="sxs-lookup"><span data-stu-id="53f31-354">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="53f31-355">我们使用通过 JavaScript 的更多逻辑建立此导航。</span><span class="sxs-lookup"><span data-stu-id="53f31-355">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="53f31-356">打开您在前面创建的 .js 文件，然后添加以下代码中突出显示的行。</span><span class="sxs-lookup"><span data-stu-id="53f31-356">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="53f31-357">此代码执行两项操作：</span><span class="sxs-lookup"><span data-stu-id="53f31-357">This code does two things:</span></span>
    1.  <span data-ttu-id="53f31-358">这将帮助确保用户不能直接从工作区导航到**查看会计**页面。</span><span class="sxs-lookup"><span data-stu-id="53f31-358">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="53f31-359">它建立从**发票明细**页面到**查看会计**页面的导航控件。</span><span class="sxs-lookup"><span data-stu-id="53f31-359">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

> [!NOTE] 
> <span data-ttu-id="53f31-360">这些页面和代码中的其他控件的名称必须与工作区中的名称相同。</span><span class="sxs-lookup"><span data-stu-id="53f31-360">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }

2.  <span data-ttu-id="53f31-361">通过选择**逻辑**选项卡，将该代码文件上传到工作区以覆盖以前的代码</span><span class="sxs-lookup"><span data-stu-id="53f31-361">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="53f31-362">单击**完成**退出编辑模式。</span><span class="sxs-lookup"><span data-stu-id="53f31-362">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="53f31-363">单击**后退**，然后单击**完成**退出工作区</span><span class="sxs-lookup"><span data-stu-id="53f31-363">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="53f31-364">单击**发布工作区**以保存工作</span><span class="sxs-lookup"><span data-stu-id="53f31-364">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="53f31-365">验证</span><span class="sxs-lookup"><span data-stu-id="53f31-365">Validation</span></span>

<span data-ttu-id="53f31-366">从您的移动设备打开应用程序，然后连接到您的 Finance and Operations 实例。</span><span class="sxs-lookup"><span data-stu-id="53f31-366">From your mobile device, open the app, and connect to your Finance and Operations instance.</span></span> <span data-ttu-id="53f31-367">确保在供应商发票分配给您检查的位置登录公司。</span><span class="sxs-lookup"><span data-stu-id="53f31-367">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="53f31-368">您应该可以执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="53f31-368">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="53f31-369">查看**我的审核**工作区。</span><span class="sxs-lookup"><span data-stu-id="53f31-369">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="53f31-370">钻取到**我的审核**工作区中，并查看**我的供应商发票**页面。</span><span class="sxs-lookup"><span data-stu-id="53f31-370">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="53f31-371">钻取到**我的供应商发票**页面中，并查看分配给您的发票的列表。</span><span class="sxs-lookup"><span data-stu-id="53f31-371">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="53f31-372">钻取到一张发票中，并查看发票抬头明细和行明细。</span><span class="sxs-lookup"><span data-stu-id="53f31-372">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="53f31-373">在明细页面中，查看附件的链接，并使用该链接导航到附件列表和查看附件。</span><span class="sxs-lookup"><span data-stu-id="53f31-373">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="53f31-374">在明细页面中，查看**查看会计**页面的链接，并使用该链接导航到分配页面和查看分配。</span><span class="sxs-lookup"><span data-stu-id="53f31-374">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="53f31-375">在明细页面中，单击底部的**操作**菜单，并执行适用于工作流步骤的工作流操作。</span><span class="sxs-lookup"><span data-stu-id="53f31-375">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="53f31-376">为 Fabrikam 设计复杂发票审核方案</span><span class="sxs-lookup"><span data-stu-id="53f31-376">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="53f31-377">方案属性</span><span class="sxs-lookup"><span data-stu-id="53f31-377">Scenario attribute</span></span></th>
<th><span data-ttu-id="53f31-378">答卷</span><span class="sxs-lookup"><span data-stu-id="53f31-378">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="53f31-379">用户希望在移动体验中看到发票抬头中的哪些字段？其顺序如何？</span><span class="sxs-lookup"><span data-stu-id="53f31-379">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="53f31-380">供应商名称</span><span class="sxs-lookup"><span data-stu-id="53f31-380">Vendor name</span></span></li>
<li><span data-ttu-id="53f31-381">发票金额</span><span class="sxs-lookup"><span data-stu-id="53f31-381">Invoice amount</span></span></li>
<li><span data-ttu-id="53f31-382">发票帐户</span><span class="sxs-lookup"><span data-stu-id="53f31-382">Invoice account</span></span></li>
<li><span data-ttu-id="53f31-383">发票编号</span><span class="sxs-lookup"><span data-stu-id="53f31-383">Invoice number</span></span></li>
<li><span data-ttu-id="53f31-384">发票日期</span><span class="sxs-lookup"><span data-stu-id="53f31-384">Invoice date</span></span></li>
<li><span data-ttu-id="53f31-385">发票描述</span><span class="sxs-lookup"><span data-stu-id="53f31-385">Invoice description</span></span></li>
<li><span data-ttu-id="53f31-386">到期日期</span><span class="sxs-lookup"><span data-stu-id="53f31-386">Due date</span></span></li>
<li><span data-ttu-id="53f31-387">发票币种</span><span class="sxs-lookup"><span data-stu-id="53f31-387">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53f31-388">用户希望在移动体验中看到发票行中的哪些字段？其顺序如何？</span><span class="sxs-lookup"><span data-stu-id="53f31-388">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="53f31-389">采购类别</span><span class="sxs-lookup"><span data-stu-id="53f31-389">Procurement category</span></span></li>
<li><span data-ttu-id="53f31-390">数量</span><span class="sxs-lookup"><span data-stu-id="53f31-390">Quantity</span></span></li>
<li><span data-ttu-id="53f31-391">单价</span><span class="sxs-lookup"><span data-stu-id="53f31-391">Unit price</span></span></li>
<li><span data-ttu-id="53f31-392">行净额</span><span class="sxs-lookup"><span data-stu-id="53f31-392">Line net amount</span></span></li>
<li><span data-ttu-id="53f31-393">1099 金额</span><span class="sxs-lookup"><span data-stu-id="53f31-393">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53f31-394">一个发票中有多少个发票行？</span><span class="sxs-lookup"><span data-stu-id="53f31-394">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="53f31-395">在此处应用 80-20 规则，并针对 80% 进行优化。</span><span class="sxs-lookup"><span data-stu-id="53f31-395">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="53f31-396">5</span><span class="sxs-lookup"><span data-stu-id="53f31-396">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53f31-397">用户是否希望检查期间在移动设备上显示会计分配（发票编码）？</span><span class="sxs-lookup"><span data-stu-id="53f31-397">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="53f31-398">是</span><span class="sxs-lookup"><span data-stu-id="53f31-398">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53f31-399">一个发票行有多少个会计分配（延伸价格、销售税、费用等）？</span><span class="sxs-lookup"><span data-stu-id="53f31-399">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="53f31-400">再次应用 80-20 规则。</span><span class="sxs-lookup"><span data-stu-id="53f31-400">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="53f31-401">延伸价格：2，销售税：2，费用：2</span><span class="sxs-lookup"><span data-stu-id="53f31-401">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53f31-402">发票的发票抬头中是否也有会计分配？</span><span class="sxs-lookup"><span data-stu-id="53f31-402">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="53f31-403">如果有，这些会计分配在设备上是否可用？</span><span class="sxs-lookup"><span data-stu-id="53f31-403">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="53f31-404">未使用</span><span class="sxs-lookup"><span data-stu-id="53f31-404">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53f31-405">用户是否要在设备上查看发票的附件？</span><span class="sxs-lookup"><span data-stu-id="53f31-405">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="53f31-406">是</span><span class="sxs-lookup"><span data-stu-id="53f31-406">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="53f31-407">后续步骤</span><span class="sxs-lookup"><span data-stu-id="53f31-407">Next steps</span></span>

<span data-ttu-id="53f31-408">可根据方案 2 的要求为方案 1 完成以下变型。</span><span class="sxs-lookup"><span data-stu-id="53f31-408">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="53f31-409">您可以使用此部分提高您的移动应用体验。</span><span class="sxs-lookup"><span data-stu-id="53f31-409">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="53f31-410">因为方案 2 中应该有更多行，所以对设计的以下更改将帮助优化移动设备上的用户体验：</span><span class="sxs-lookup"><span data-stu-id="53f31-410">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="53f31-411">用户可以选择查看单独移动页面上的行，而不是查看明细页面上的发票行（如方案 1 中）。</span><span class="sxs-lookup"><span data-stu-id="53f31-411">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="53f31-412">因为此方案中应该有多张发票，所以如果使用 **VendMobileInvoiceAllDistributionTree** 页面为移动设计分配页面（如方案 1 中），用户可能很难将行与分配关联。</span><span class="sxs-lookup"><span data-stu-id="53f31-412">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="53f31-413">因此，请使用 **VendMobileInvoiceLineDistributionTree** 页面设计分配页面。</span><span class="sxs-lookup"><span data-stu-id="53f31-413">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="53f31-414">理想情况下，应该在此方案中的发票行上下文内显示分配。</span><span class="sxs-lookup"><span data-stu-id="53f31-414">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="53f31-415">因此，请确保用户可以钻取到行中以查看分配页面。</span><span class="sxs-lookup"><span data-stu-id="53f31-415">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="53f31-416">请使用页面链接功能建立钻取，就如在方案 1 中对抬头和明细页面执行的操作。</span><span class="sxs-lookup"><span data-stu-id="53f31-416">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="53f31-417">因为方案 2 中分配上应该有多个金额类型（销售税、费用等），所以显示金额类型的描述非常有用。</span><span class="sxs-lookup"><span data-stu-id="53f31-417">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="53f31-418">（我们在方案 1 中忽略了此信息。）</span><span class="sxs-lookup"><span data-stu-id="53f31-418">(We omitted this information in scenario 1.)</span></span>




