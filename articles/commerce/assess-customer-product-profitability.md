---
title: 评估客户和产品收益率
description: 本文介绍了如何使用内存中和实时分析来从您的 Dynamics 365 Commerce 数据访问、探索和深入了解客户和产品收益率。
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: SysOperationsTemplateForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 3218a29995791ce0d9a42d5b6d898d6e548f0f1d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410463"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="5c054-103">评估客户和产品收益率</span><span class="sxs-lookup"><span data-stu-id="5c054-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5c054-104">本文介绍了如何使用内存中和实时分析来从您的 Dynamics 365 Commerce 数据访问、探索和深入了解客户和产品收益率。</span><span class="sxs-lookup"><span data-stu-id="5c054-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="5c054-105">作为 Commerce 的一部分，用户可以基于以下条件之一，研究跨组织层次结构不同级别的排名靠前的客户（10 到 100）的收益率：</span><span class="sxs-lookup"><span data-stu-id="5c054-105">As part of Commerce, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="5c054-106">销售额</span><span class="sxs-lookup"><span data-stu-id="5c054-106">Sales amount</span></span>
- <span data-ttu-id="5c054-107">数量</span><span class="sxs-lookup"><span data-stu-id="5c054-107">Quantity</span></span>
- <span data-ttu-id="5c054-108">毛利润率</span><span class="sxs-lookup"><span data-stu-id="5c054-108">Gross profit margin</span></span>
- <span data-ttu-id="5c054-109">毛利百分比</span><span class="sxs-lookup"><span data-stu-id="5c054-109">Margin percentage</span></span>

<span data-ttu-id="5c054-110">对于此评估，您可以使用现成的 **排名靠前的客户** 报表，您可以从以下任何位置打开此报表：</span><span class="sxs-lookup"><span data-stu-id="5c054-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="5c054-111">**商店管理** 工作区 &gt; **Retail 和 Commerce** &gt; **渠道** &gt; **商店管理** &gt; **报表** &gt; **排名靠前的客户报表**</span><span class="sxs-lookup"><span data-stu-id="5c054-111">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="5c054-112">**查询和报表** 部分 &gt; **Retail 和 Commerce** &gt; **查询和报表** &gt; **销售报表** &gt; **排名靠前的客户报表**</span><span class="sxs-lookup"><span data-stu-id="5c054-112">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="5c054-113">同样，用户可以基于以下条件之一，研究跨组织层次结构不同级别的排名靠前的产品（10 到 100）的收益率：</span><span class="sxs-lookup"><span data-stu-id="5c054-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="5c054-114">销售额</span><span class="sxs-lookup"><span data-stu-id="5c054-114">Sales amount</span></span>
- <span data-ttu-id="5c054-115">数量</span><span class="sxs-lookup"><span data-stu-id="5c054-115">Quantity</span></span>
- <span data-ttu-id="5c054-116">毛利润率</span><span class="sxs-lookup"><span data-stu-id="5c054-116">Gross profit margin</span></span>
- <span data-ttu-id="5c054-117">毛利百分比</span><span class="sxs-lookup"><span data-stu-id="5c054-117">Margin percentage</span></span>

<span data-ttu-id="5c054-118">对于此评估，您可以使用现成的 **排名靠前的产品** 报表，您可以从以下任何位置打开此报表：</span><span class="sxs-lookup"><span data-stu-id="5c054-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="5c054-119">**商店管理** 工作区 &gt; **Retail 和 Commerce** &gt; **渠道** &gt; **商店管理** &gt; **报表** &gt; **排名靠前的产品报表**</span><span class="sxs-lookup"><span data-stu-id="5c054-119">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="5c054-120">**类别和产品管理** 工作区 &gt; **Retail 和 Commerce** &gt; **产品和类别** &gt; **商店管理** &gt; **报表** &gt; **排名靠前的产品报表**</span><span class="sxs-lookup"><span data-stu-id="5c054-120">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Products and categories** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="5c054-121">**查询和报表** 部分 &gt; **Retail 和 Commerce** &gt; **查询和报表** &gt; **销售报表** &gt; **排名靠前的产品报表**</span><span class="sxs-lookup"><span data-stu-id="5c054-121">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>
