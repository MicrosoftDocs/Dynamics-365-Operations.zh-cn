---
title: "评估客户和产品收益率"
description: "本文介绍如何使用内存中的实时分析来从您的 Microsoft Dynamics 365 for Retail 数据访问、探索和深入了解客户和产品收益率。"
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 84a9e0b3936adcf2ed99fddca77dd57dfedeb050
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---

# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="c4c0d-103">评估客户和产品收益率</span><span class="sxs-lookup"><span data-stu-id="c4c0d-103">Assess customer and product profitability</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="c4c0d-104">本文介绍如何使用内存中的实时分析来从您的 Microsoft Dynamics 365 for Retail 数据访问、探索和深入了解客户和产品收益率。</span><span class="sxs-lookup"><span data-stu-id="c4c0d-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Microsoft Dynamics 365 for Retail data.</span></span> 

<span data-ttu-id="c4c0d-105">作为 Dynamics 365 for Retail 的一部分，用户可以基于以下条件之一，研究跨组织层次结构不同级别的排名靠前的客户（10 到 100）的收益率：</span><span class="sxs-lookup"><span data-stu-id="c4c0d-105">As part of Dynamics 365 for Retail, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

-   <span data-ttu-id="c4c0d-106">销售额</span><span class="sxs-lookup"><span data-stu-id="c4c0d-106">Sales amount</span></span>
-   <span data-ttu-id="c4c0d-107">数量</span><span class="sxs-lookup"><span data-stu-id="c4c0d-107">Quantity</span></span>
-   <span data-ttu-id="c4c0d-108">毛利润率</span><span class="sxs-lookup"><span data-stu-id="c4c0d-108">Gross profit margin</span></span>
-   <span data-ttu-id="c4c0d-109">毛利百分比</span><span class="sxs-lookup"><span data-stu-id="c4c0d-109">Margin percentage</span></span>

<span data-ttu-id="c4c0d-110">对于此评估，您可以使用现成的**排名靠前的客户**报表，您可以从以下任何位置打开此报表：</span><span class="sxs-lookup"><span data-stu-id="c4c0d-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

-   <span data-ttu-id="c4c0d-111">**零售商店管理**工作区 &gt; **零售** &gt; **渠道** &gt; **零售商店管理** &gt; **报表** &gt; **排名靠前的客户报表**</span><span class="sxs-lookup"><span data-stu-id="c4c0d-111">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top customers report**</span></span>
-   <span data-ttu-id="c4c0d-112">**查询和报表**部分 &gt; **零售** &gt; **查询和报表** &gt; **销售报表** &gt; **排名靠前的客户报表**</span><span class="sxs-lookup"><span data-stu-id="c4c0d-112">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="c4c0d-113">同样，用户可以基于以下条件之一，研究跨组织层次结构不同级别的排名靠前的产品（10 到 100）的收益率：</span><span class="sxs-lookup"><span data-stu-id="c4c0d-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

-   <span data-ttu-id="c4c0d-114">销售额</span><span class="sxs-lookup"><span data-stu-id="c4c0d-114">Sales amount</span></span>
-   <span data-ttu-id="c4c0d-115">数量</span><span class="sxs-lookup"><span data-stu-id="c4c0d-115">Quantity</span></span>
-   <span data-ttu-id="c4c0d-116">毛利润率</span><span class="sxs-lookup"><span data-stu-id="c4c0d-116">Gross profit margin</span></span>
-   <span data-ttu-id="c4c0d-117">毛利百分比</span><span class="sxs-lookup"><span data-stu-id="c4c0d-117">Margin percentage</span></span>

<span data-ttu-id="c4c0d-118">对于此评估，您可以使用现成的**排名靠前的产品**报表，您可以从以下任何位置打开此报表：</span><span class="sxs-lookup"><span data-stu-id="c4c0d-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

-   <span data-ttu-id="c4c0d-119">**零售商店管理**工作区 &gt; **零售** &gt; **渠道** &gt; **零售商店管理** &gt; **报表** &gt; **排名靠前的产品报表**</span><span class="sxs-lookup"><span data-stu-id="c4c0d-119">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
-   <span data-ttu-id="c4c0d-120">**类别和产品管理**工作区 &gt; **零售** &gt; **产品和类别** &gt; **零售商店管理** &gt; **报表** &gt; **排名靠前的产品报表**</span><span class="sxs-lookup"><span data-stu-id="c4c0d-120">**Category and product management** workspace &gt; **Retail** &gt; **Products and categories** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
-   <span data-ttu-id="c4c0d-121">**查询和报表**部分 &gt; **零售** &gt; **查询和报表** &gt; **销售报表** &gt; **排名靠前的产品报表**</span><span class="sxs-lookup"><span data-stu-id="c4c0d-121">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>




