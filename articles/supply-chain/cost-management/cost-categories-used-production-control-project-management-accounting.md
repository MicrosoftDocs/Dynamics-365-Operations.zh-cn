---
title: "用于项目控制和项目管理核算的成本类别"
description: "某些生产工作类型可以应用于项目时间评估和报告。 本文提供有关您必须为这些用于生产和项目目的生产工作类型定义的成本类别的信息。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjCategory
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 78253
ms.assetid: cfdd58a0-8afa-4a6f-a208-a76e2c162429
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 53141f29cdcd847611e1b6a8dc4c2ded1f09a9c9
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="cost-categories-used-in-production-control-and-project-management-accounting"></a><span data-ttu-id="1eae9-104">用于项目控制和项目管理核算的成本类别</span><span class="sxs-lookup"><span data-stu-id="1eae9-104">Cost categories used in Production control and Project management accounting</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="1eae9-105">某些生产工作类型可以应用于项目时间评估和报告。</span><span class="sxs-lookup"><span data-stu-id="1eae9-105">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="1eae9-106">本文提供有关您必须为这些用于生产和项目目的生产工作类型定义的成本类别的信息。</span><span class="sxs-lookup"><span data-stu-id="1eae9-106">This article provides information about the cost categories that you must define for these types of production work for production and project purposes.</span></span>

<span data-ttu-id="1eae9-107">某些生产工作类型可以应用于项目时间评估和报告。</span><span class="sxs-lookup"><span data-stu-id="1eae9-107">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="1eae9-108">在这种情况下，成本类别需要用于生产和项目目的。</span><span class="sxs-lookup"><span data-stu-id="1eae9-108">In this case, a cost category is required for production and project purposes.</span></span> <span data-ttu-id="1eae9-109">在将某一成本类别用于生产和项目时，必须定义附加的与项目相关的信息。</span><span class="sxs-lookup"><span data-stu-id="1eae9-109">When a cost category is used in production and projects, additional project-related information must be defined.</span></span> <span data-ttu-id="1eae9-110">例如，与项目相关联的每小时成本可以不同于与生产相关联的每小时成本。</span><span class="sxs-lookup"><span data-stu-id="1eae9-110">For example, the hourly costs that are associated with projects can differ from the hourly costs that are associated with production.</span></span> <span data-ttu-id="1eae9-111">您可以使用**成本类别**页来定义用于生产控制和项目管理核算的成本类别。</span><span class="sxs-lookup"><span data-stu-id="1eae9-111">You can use the **Cost categories** page to define a cost category that is used in Production control and Project management accounting.</span></span> 

<span data-ttu-id="1eae9-112">**注意：**成本核算具有**项目类别**页，但此页没有与在此主题中描述的功能的关系。</span><span class="sxs-lookup"><span data-stu-id="1eae9-112">**Note:** Cost accounting has a **Project categories** page, but this page has no relationship to the functionality that is described in this topic.</span></span> <span data-ttu-id="1eae9-113">在项目中使用成本类别时，**成本类别**页具有显示附加的项目相关信息的其他选项卡。</span><span class="sxs-lookup"><span data-stu-id="1eae9-113">When you use a cost category in projects, the **Cost categories** page has additional tabs that show additional project-related information.</span></span> <span data-ttu-id="1eae9-114">此信息包括类别组、行属性和已分配给成本类别的会计科目。</span><span class="sxs-lookup"><span data-stu-id="1eae9-114">This information includes the category group, a line property, and ledger accounts that are assigned to the cost category.</span></span>

-   <span data-ttu-id="1eae9-115">该成本类别必须分配给支持**工时**交易记录类型的某一类别组。</span><span class="sxs-lookup"><span data-stu-id="1eae9-115">The cost category must be assigned to a category group that supports a transaction type of **Hours**.</span></span>
-   <span data-ttu-id="1eae9-116">行属性将指示如何对项目向报告的时间收费的默认信息。</span><span class="sxs-lookup"><span data-stu-id="1eae9-116">The line property indicates default information about how reported time can be charged to a project.</span></span>
-   <span data-ttu-id="1eae9-117">通常，与成本和销售的会计科目定义分配给成本类别的类别组的。</span><span class="sxs-lookup"><span data-stu-id="1eae9-117">Typically, the ledger accounts that are related to costs and sales are defined for the category group that is assigned to the cost category.</span></span> <span data-ttu-id="1eae9-118">但是，特定帐户可以定义单独的成本类别。</span><span class="sxs-lookup"><span data-stu-id="1eae9-118">However, specific accounts can be defined for an individual cost category.</span></span>

<span data-ttu-id="1eae9-119">**成本类别**页上的其他一些按钮可用于访问关于成本类别的与项目相关的信息。</span><span class="sxs-lookup"><span data-stu-id="1eae9-119">Additional buttons on the **Cost categories** page let you access project-related information about a selected cost category.</span></span> <span data-ttu-id="1eae9-120">例如，您可以查看与项目相关的交易记录，定义员工或项目，定义每小时成本和销售价以及查看报表。</span><span class="sxs-lookup"><span data-stu-id="1eae9-120">For example, you can view project-related transactions, define employees or projects, define hourly costs and sales prices, and view reports.</span></span>




