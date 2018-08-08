---
title: "会计源资源管理器"
description: "本文提供有关会计源资源管理器的信息，您可用此信息来进行总帐会计条目后源信息的详细分析。"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: de5de039c0e3332943bae4846768fc628810906e
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---

# <a name="accounting-source-explorer"></a><span data-ttu-id="04e7e-103">会计源资源管理器</span><span class="sxs-lookup"><span data-stu-id="04e7e-103">Accounting source explorer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04e7e-104">本文提供有关会计源资源管理器的信息，您可用此信息来进行总帐会计条目后源信息的详细分析。</span><span class="sxs-lookup"><span data-stu-id="04e7e-104">This article provides information about Accounting source explorer, which you can use for detailed analysis of the source information behind general ledger accounting entries.</span></span>

<span data-ttu-id="04e7e-105">会计源资源管理器是显示源信息的新页面。</span><span class="sxs-lookup"><span data-stu-id="04e7e-105">Accounting source explorer is a new page that shows source information.</span></span> <span data-ttu-id="04e7e-106">您可以使用会计源资源管理器作为单独的工具或分析总帐会计条目后的详细信息。</span><span class="sxs-lookup"><span data-stu-id="04e7e-106">You can use Accounting source explorer either as a stand-alone tool or to analyze the details behind general ledger accounting entries.</span></span> <span data-ttu-id="04e7e-107">例如，您可以使用会计源资源管理器获取线索余额中余额的或凭证交易记录的最详细来源信息。</span><span class="sxs-lookup"><span data-stu-id="04e7e-107">For example, you can use Accounting source explorer to get the most detailed source information for a balance in Trail balance or for a voucher transaction.</span></span> <span data-ttu-id="04e7e-108">您可以使用“导出到 MS Excel”功能进一步划分和切分 Microsoft Excel 中的信息（例如，在数据透视表或在数据透视表报表中）。</span><span class="sxs-lookup"><span data-stu-id="04e7e-108">You can then use the Export to MS Excel feature to further slice and dice the information in Microsoft Excel (for example, in a PivotTable or on a PivotTable report).</span></span>

<span data-ttu-id="04e7e-109">会计源资源管理器始终显示与总帐显示的每个会计科目相同的总金额（例如，在试算平衡表中）。</span><span class="sxs-lookup"><span data-stu-id="04e7e-109">Accounting source explorer always shows the same total amount per ledger account as General ledger shows (for example, in Trial balance).</span></span> <span data-ttu-id="04e7e-110">在试算平衡表中，可以在单独的列显示段。</span><span class="sxs-lookup"><span data-stu-id="04e7e-110">As in Trial balance, you can display segments in separate columns.</span></span> <span data-ttu-id="04e7e-111">只需选择适合的财务维度集。</span><span class="sxs-lookup"><span data-stu-id="04e7e-111">Just select the appropriate financial dimension set.</span></span> 

<span data-ttu-id="04e7e-112">您可以使用参数定义该分析的日期间隔。</span><span class="sxs-lookup"><span data-stu-id="04e7e-112">You can use parameters to define a date interval for the analysis.</span></span> <span data-ttu-id="04e7e-113">此功能类似于试算平衡表中的功能。</span><span class="sxs-lookup"><span data-stu-id="04e7e-113">This functionality also resembles the functionality in Trial balance.</span></span>

<span data-ttu-id="04e7e-114">对于使用原始凭证框架的所有凭证，会计源资源管理器基于会计分配显示附加信息，如果适用，还显示项目会计分配。</span><span class="sxs-lookup"><span data-stu-id="04e7e-114">For all documents that use the source document framework, Accounting source explorer shows additional information, based on accounting distributions and, if applicable, project accounting distributions.</span></span> <span data-ttu-id="04e7e-115">此信息包括货币金额类型、项目、活动、类别和记录属性。</span><span class="sxs-lookup"><span data-stu-id="04e7e-115">This information includes the monetary amount type, project, activity, category, and line property.</span></span> <span data-ttu-id="04e7e-116">下面是您可以执行的分析的一些示例：</span><span class="sxs-lookup"><span data-stu-id="04e7e-116">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="04e7e-117">采购订单和供应商发票之间的差异，因为每个差异由货币金额类型表示，如费用差异</span><span class="sxs-lookup"><span data-stu-id="04e7e-117">Variances between purchase orders and vendor invoices, because each variance is represented by a monetary amount type, such as charge variance</span></span>
-   <span data-ttu-id="04e7e-118">每个项目、业务单位和主科目的计费和非计费工时和支出</span><span class="sxs-lookup"><span data-stu-id="04e7e-118">Billable versus non-billable hours and expenses per project, business unit, and main account</span></span>

<span data-ttu-id="04e7e-119">对于使用原始凭证引用标识概念的原始凭证，会计源资源管理器显示更多详细信息，如客户、供应商、工作人员、产品、数量、单位文本和描述。</span><span class="sxs-lookup"><span data-stu-id="04e7e-119">For source documents that use the source document reference identities concept, Accounting source explorer shows even more details, such as the customer, vendor, worker, product, quantity, unit text, and descriptions.</span></span> <span data-ttu-id="04e7e-120">下面是您可以执行的分析的一些示例：</span><span class="sxs-lookup"><span data-stu-id="04e7e-120">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="04e7e-121">每个业务单位的酒店支出和会计期间酒店品牌，基于支出报表</span><span class="sxs-lookup"><span data-stu-id="04e7e-121">Hotel expenses per business unit and hotel brand for a fiscal period, based on expense reports</span></span>
-   <span data-ttu-id="04e7e-122">每个供应商、产品、部门的折扣</span><span class="sxs-lookup"><span data-stu-id="04e7e-122">Discounts per vendor, product, department</span></span>

<span data-ttu-id="04e7e-123">对于这些凭证，您还可以导航到会计源资源管理器的实际原始凭证。</span><span class="sxs-lookup"><span data-stu-id="04e7e-123">For these documents, you can also navigate to the actual source document from Accounting source explorer.</span></span>




