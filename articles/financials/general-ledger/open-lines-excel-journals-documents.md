---
title: "从 Excel 发布日记帐行和单据"
description: "本主题说明如何从 Microsoft Excel 输入和发布普通日记帐的行。 其中包含有关您可使用的各种模板的信息，具体取决于您要输入的交易记录类型。"
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e6e159f84e188bad49db7b99a43c99f2e4d744be
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="publish-journal-lines-and-documents-from-excel"></a><span data-ttu-id="cd98b-104">从 Excel 发布日记帐行和单据</span><span class="sxs-lookup"><span data-stu-id="cd98b-104">Publish journal lines and documents from Excel</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="cd98b-105">本主题说明如何从 Microsoft Excel 输入和发布普通日记帐的行。</span><span class="sxs-lookup"><span data-stu-id="cd98b-105">This topic explains how to enter and publish lines for general journals from Microsoft Excel.</span></span> <span data-ttu-id="cd98b-106">其中包含有关您可使用的各种模板的信息，具体取决于您要输入的交易记录类型。</span><span class="sxs-lookup"><span data-stu-id="cd98b-106">It includes information about the various templates that you can use, depending on the type of transactions that you're entering.</span></span>

<span data-ttu-id="cd98b-107">用户可从 Microsoft Excel 输入和发布财务日记帐的行。</span><span class="sxs-lookup"><span data-stu-id="cd98b-107">Users can enter and publish lines for financial journals from Microsoft Excel.</span></span> <span data-ttu-id="cd98b-108">用户创建日记帐之后，**在 Excel 中打开文件**按钮将显示可用模板。</span><span class="sxs-lookup"><span data-stu-id="cd98b-108">After a user creates a journal, the **Open lines in Excel** button displays the templates that are available.</span></span> <span data-ttu-id="cd98b-109">模板设计为支持特定方案，但是日记帐中并非支持科目类型的所有组合。</span><span class="sxs-lookup"><span data-stu-id="cd98b-109">Templates are designed to support specific scenarios, however not every combination of account type is supported in the journal.</span></span> <span data-ttu-id="cd98b-110">下表显示可用模板及其支持的科目类型。</span><span class="sxs-lookup"><span data-stu-id="cd98b-110">The following table shows the templates that are available and the account types which they support.</span></span>
|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd98b-111">**模板**</span><span class="sxs-lookup"><span data-stu-id="cd98b-111">**Template**</span></span>             | <span data-ttu-id="cd98b-112">**支持的科目类型**</span><span class="sxs-lookup"><span data-stu-id="cd98b-112">**Supported account types**</span></span>                                                                                             | <span data-ttu-id="cd98b-113">**模板的访问方法**</span><span class="sxs-lookup"><span data-stu-id="cd98b-113">**How to access the template**</span></span>                                                          |
| <span data-ttu-id="cd98b-114">分类日记帐行</span><span class="sxs-lookup"><span data-stu-id="cd98b-114">Ledger journal lines</span></span>     | <span data-ttu-id="cd98b-115">支持“科目：分类帐、客户、供应商、银行抵销科目：分类帐、客户、供应商、银行内部公司”。</span><span class="sxs-lookup"><span data-stu-id="cd98b-115">Account: Ledger, Customer, Vendor, Bank Offset account: Ledger, Customer, Vendor, Bank Intercompany is supported.</span></span>       | <span data-ttu-id="cd98b-116">普通日记帐</span><span class="sxs-lookup"><span data-stu-id="cd98b-116">General journal</span></span>                                                                         |
| <span data-ttu-id="cd98b-117">发票登记簿</span><span class="sxs-lookup"><span data-stu-id="cd98b-117">Invoice register</span></span>         | <span data-ttu-id="cd98b-118">不支持“科目：供应商抵销科目：分类帐内部公司”。</span><span class="sxs-lookup"><span data-stu-id="cd98b-118">Account: Vendor Offset account: Ledger Intercompany isn't supported.</span></span>                                                    | <span data-ttu-id="cd98b-119">AP 发票登记簿</span><span class="sxs-lookup"><span data-stu-id="cd98b-119">AP invoice register</span></span>                                                                     |
| <span data-ttu-id="cd98b-120">发票日记帐</span><span class="sxs-lookup"><span data-stu-id="cd98b-120">Invoice journal</span></span>          | <span data-ttu-id="cd98b-121">支持“科目：供应商抵销科目：分类帐内部公司”。</span><span class="sxs-lookup"><span data-stu-id="cd98b-121">Accounts: Vendor Offset account: Ledger Intercompany is supported.</span></span>                                                      | <span data-ttu-id="cd98b-122">AP 发票日记帐</span><span class="sxs-lookup"><span data-stu-id="cd98b-122">AP invoice journal</span></span>                                                                      |
| <span data-ttu-id="cd98b-123">供应商发票</span><span class="sxs-lookup"><span data-stu-id="cd98b-123">Vendor invoice</span></span>           |                                                                                                                         | <span data-ttu-id="cd98b-124">供应商发票</span><span class="sxs-lookup"><span data-stu-id="cd98b-124">Vendor invoice</span></span>                                                                          |
| <span data-ttu-id="cd98b-125">客户发票日记帐</span><span class="sxs-lookup"><span data-stu-id="cd98b-125">Customer invoice journal</span></span> | <span data-ttu-id="cd98b-126">支持“科目：客户抵销科目：分类帐内部公司”。</span><span class="sxs-lookup"><span data-stu-id="cd98b-126">Account: Customer Offset account: Ledger Intercompany is supported.</span></span>                                                     | <span data-ttu-id="cd98b-127">普通日记帐</span><span class="sxs-lookup"><span data-stu-id="cd98b-127">General journal</span></span>                                                                         |
| <span data-ttu-id="cd98b-128">普通发票</span><span class="sxs-lookup"><span data-stu-id="cd98b-128">Free text invoice</span></span>        |                                                                                                                         | <span data-ttu-id="cd98b-129">在**普通发票**页中，单击**在 Excel 中打开**（Microsoft Office 图标）。</span><span class="sxs-lookup"><span data-stu-id="cd98b-129">On the **Free text invoice** page, click **Open in Excel** (the Microsoft Office icon).</span></span> |
| <span data-ttu-id="cd98b-130">固定资产日记帐</span><span class="sxs-lookup"><span data-stu-id="cd98b-130">Fixed assets journal</span></span>     | <span data-ttu-id="cd98b-131">资产到分类帐、银行、客户或供应商。</span><span class="sxs-lookup"><span data-stu-id="cd98b-131">Asset to ledger, bank, customer, or vendor.</span></span> <span data-ttu-id="cd98b-132">不支持“内部公司”。</span><span class="sxs-lookup"><span data-stu-id="cd98b-132">Intercompany isn't supported.</span></span>                                               | <span data-ttu-id="cd98b-133">固定资产日记帐</span><span class="sxs-lookup"><span data-stu-id="cd98b-133">Fixed asset journal</span></span>                                                                     |
| <span data-ttu-id="cd98b-134">供应商付款日记帐</span><span class="sxs-lookup"><span data-stu-id="cd98b-134">Vendor payment journal</span></span>   | <span data-ttu-id="cd98b-135">不支持“科目：供应商抵销科目：分类帐、银行内部公司”。</span><span class="sxs-lookup"><span data-stu-id="cd98b-135">Account: Vendor Offset account: Ledger, Bank Intercompany is supported.</span></span>                                                 | <span data-ttu-id="cd98b-136">供应商付款日记帐</span><span class="sxs-lookup"><span data-stu-id="cd98b-136">Vendor payment journal</span></span>                                                                  |
| <span data-ttu-id="cd98b-137">客户付款日记帐</span><span class="sxs-lookup"><span data-stu-id="cd98b-137">Customer payment journal</span></span> | <span data-ttu-id="cd98b-138">支持“科目：客户抵销科目：分类帐、银行内部公司”。</span><span class="sxs-lookup"><span data-stu-id="cd98b-138">Account: Customer Offset account: Ledger, Bank Intercompany is supported.</span></span>                                               | <span data-ttu-id="cd98b-139">客户付款日记帐</span><span class="sxs-lookup"><span data-stu-id="cd98b-139">Customer payment journal</span></span>                                                                |
| <span data-ttu-id="cd98b-140">项目支出日记帐</span><span class="sxs-lookup"><span data-stu-id="cd98b-140">Project expense journal</span></span>  | <span data-ttu-id="cd98b-141">支持“科目：项目、分类帐、客户、供应商抵销科目：项目、分类帐、客户、供应商、银行内部公司”。</span><span class="sxs-lookup"><span data-stu-id="cd98b-141">Account: Project, Ledger, Customer, Vendor Offset account: Project, Ledger, Customer, Vendor Intercompany is supported.</span></span> | <span data-ttu-id="cd98b-142">普通日记帐费用（在“项目管理和会计”下）</span><span class="sxs-lookup"><span data-stu-id="cd98b-142">General journal Expense (under Project management and accounting)</span></span>                       |

<span data-ttu-id="cd98b-143">发布行时，将验证行，以便确保其符合财务日记帐中设置的规则。</span><span class="sxs-lookup"><span data-stu-id="cd98b-143">When the lines are published, they are validated to make sure that they comply with the rules that are set up in the financial journals.</span></span> <span data-ttu-id="cd98b-144">发布行之后，用户可从 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 编辑或过帐凭证。</span><span class="sxs-lookup"><span data-stu-id="cd98b-144">After the lines are published, users can edit or post the vouchers from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> 

<span data-ttu-id="cd98b-145">若要向模板添加财务维度，需要执行更多更改。</span><span class="sxs-lookup"><span data-stu-id="cd98b-145">To add financial dimensions to a template, additional changes are required.</span></span> <span data-ttu-id="cd98b-146">有关详细信息，请参阅[向 Microsoft Excel 模板添加维度](../../dev-itpro/financial/add-dimensions-excel-templates.md)。</span><span class="sxs-lookup"><span data-stu-id="cd98b-146">For additional information, see [Add dimensions to the Microsoft Excel template](../../dev-itpro/financial/add-dimensions-excel-templates.md).</span></span> <span data-ttu-id="cd98b-147">维度添加到实体之后，将在 Excel 设计器中可用，并可添加到模板。</span><span class="sxs-lookup"><span data-stu-id="cd98b-147">After dimensions are added to the entity, they are available in the Excel designer and can be added to the template.</span></span>






