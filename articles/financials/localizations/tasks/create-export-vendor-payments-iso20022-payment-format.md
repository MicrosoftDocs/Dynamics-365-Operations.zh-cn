--- 
title: "使用 ISO20022 付款格式创建和导出供应商付款"
description: "此过程显示如何在供应商付款日记帐中创建付款行，并使用 ISO2022 贷方转帐示例生成供应商付款文件。"
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7cc90bc86cd489b124a806c480632dd53ba47f3f
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="13b7d-103">使用 ISO20022 付款格式创建和导出供应商付款</span><span class="sxs-lookup"><span data-stu-id="13b7d-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="13b7d-104">此过程显示如何在供应商付款日记帐中创建付款行，并使用 ISO2022 贷方转帐示例生成供应商付款文件。</span><span class="sxs-lookup"><span data-stu-id="13b7d-104">This procedure shows how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span> 

<span data-ttu-id="13b7d-105">用于创建此过程的演示数据公司是 DEMF。</span><span class="sxs-lookup"><span data-stu-id="13b7d-105">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="13b7d-106">这是五个用于演示使用电子申报配置的供应商付款流程的流程中的第五个。</span><span class="sxs-lookup"><span data-stu-id="13b7d-106">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="13b7d-107">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="13b7d-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-payment-lines"></a><span data-ttu-id="13b7d-108">创建付款行</span><span class="sxs-lookup"><span data-stu-id="13b7d-108">Create payment lines</span></span>
1. <span data-ttu-id="13b7d-109">转至“应付帐款”>“付款”>“付款日记帐”。</span><span class="sxs-lookup"><span data-stu-id="13b7d-109">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="13b7d-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="13b7d-110">Click New.</span></span>
3. <span data-ttu-id="13b7d-111">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="13b7d-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="13b7d-112">在“名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="13b7d-112">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="13b7d-113">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="13b7d-113">Click Lines.</span></span>
6. <span data-ttu-id="13b7d-114">单击“付款方案”。</span><span class="sxs-lookup"><span data-stu-id="13b7d-114">Click Payment proposal.</span></span>
7. <span data-ttu-id="13b7d-115">单击”创建付款方案“。</span><span class="sxs-lookup"><span data-stu-id="13b7d-115">Click Create payment proposal.</span></span>
8. <span data-ttu-id="13b7d-116">扩展“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="13b7d-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="13b7d-117">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="13b7d-117">Click Filter.</span></span>
10. <span data-ttu-id="13b7d-118">在列表中，选择“供应商”表和“供应商帐户”字段的行。</span><span class="sxs-lookup"><span data-stu-id="13b7d-118">In the list, select the row for Vendors table and Vendor account field.</span></span>
11. <span data-ttu-id="13b7d-119">在“标准”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="13b7d-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="13b7d-120">您可以为选择要付款的供应商交易应用任何条件，此示例中则是将 DE-001 用作供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="13b7d-120">You can apply any criteria for selecting vendor transactions to pay, for this example use DE-001 as a vendor account.</span></span>  
12. <span data-ttu-id="13b7d-121">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="13b7d-121">Click OK.</span></span>
13. <span data-ttu-id="13b7d-122">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="13b7d-122">Click OK.</span></span>
14. <span data-ttu-id="13b7d-123">单击”创建付款“。</span><span class="sxs-lookup"><span data-stu-id="13b7d-123">Click Create payments.</span></span>

## <a name="generate-an-iso20022-payment-file"></a><span data-ttu-id="13b7d-124">生成 ISO20022 付款文件</span><span class="sxs-lookup"><span data-stu-id="13b7d-124">Generate an ISO20022 payment file</span></span>


