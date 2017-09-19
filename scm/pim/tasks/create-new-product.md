--- 
title: "创建新产品"
description: "此任务显示如何创建新的共享的产品。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/08/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: 56ce5d965952d0cb41278915e4631ae9d920f5f9
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2017

---
# <a name="create-a-new-product"></a><span data-ttu-id="4e206-103">创建新产品</span><span class="sxs-lookup"><span data-stu-id="4e206-103">Create a new product</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4e206-104">此任务显示如何创建新的共享的产品。</span><span class="sxs-lookup"><span data-stu-id="4e206-104">This task shows how to create a new shared product.</span></span> <span data-ttu-id="4e206-105">它通常由产品设计器执行。</span><span class="sxs-lookup"><span data-stu-id="4e206-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="4e206-106">创建此任务的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="4e206-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="4e206-107">转到“产品信息管理”>“产品”>“产品”。</span><span class="sxs-lookup"><span data-stu-id="4e206-107">Go to Product information management > Products > Products.</span></span>

## <a name="create-a-product"></a><span data-ttu-id="4e206-108">创建产品</span><span class="sxs-lookup"><span data-stu-id="4e206-108">Create a product</span></span>
1. <span data-ttu-id="4e206-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="4e206-109">Click New.</span></span>
2. <span data-ttu-id="4e206-110">在“产品编号”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4e206-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="4e206-111">如果编号规则没有为产品编号设置，必须手动输入它。</span><span class="sxs-lookup"><span data-stu-id="4e206-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
3. <span data-ttu-id="4e206-112">在“产品名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4e206-112">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="4e206-113">产品名称默认为搜索名称。</span><span class="sxs-lookup"><span data-stu-id="4e206-113">The product name defaults to the search name.</span></span> <span data-ttu-id="4e206-114">可以根据需要更改。</span><span class="sxs-lookup"><span data-stu-id="4e206-114">You can change this if needed.</span></span>  
4. <span data-ttu-id="4e206-115">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4e206-115">Click OK.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="4e206-116">设置维度组</span><span class="sxs-lookup"><span data-stu-id="4e206-116">Set up dimension groups</span></span>
1. <span data-ttu-id="4e206-117">单击“维度组”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="4e206-117">Click Dimension groups to open the drop dialog.</span></span>
2. <span data-ttu-id="4e206-118">在“存储维度组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4e206-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="4e206-119">存储维度组确定哪些存储维度您必须在产品的每个交易记录中输入，以及如何在库存中跟踪。</span><span class="sxs-lookup"><span data-stu-id="4e206-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="4e206-120">在“跟踪维度组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4e206-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="4e206-121">跟踪维度组确定哪些跟踪维度您必须为产品的每个交易记录输入，以及如何在库存中处置。</span><span class="sxs-lookup"><span data-stu-id="4e206-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="4e206-122">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4e206-122">Click OK.</span></span>

