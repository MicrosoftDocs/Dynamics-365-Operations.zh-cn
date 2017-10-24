---
title: "呼叫中心目录"
description: "本文介绍 Microsoft Dynamics 365 for Retail 中目录的呼叫中心特定功能。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7be87496ceaea2d1d5f97a5cc17e50dcddbaf33d
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="call-center-catalogs"></a><span data-ttu-id="712a5-103">呼叫中心目录</span><span class="sxs-lookup"><span data-stu-id="712a5-103">Call center catalogs</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="712a5-104">本文介绍 Microsoft Dynamics 365 for Retail 中目录的呼叫中心特定功能。</span><span class="sxs-lookup"><span data-stu-id="712a5-104">This article describes the call center–specific functionality for catalogs in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="712a5-105">在呼叫中心，可以使用产品目录来标识您要为客户提供的产品。</span><span class="sxs-lookup"><span data-stu-id="712a5-105">In a call center, you can use product catalogs to identify the products that you want to offer to customers.</span></span> <span data-ttu-id="712a5-106">呼叫中心常使用打印目录。</span><span class="sxs-lookup"><span data-stu-id="712a5-106">Call centers typically use printed catalogs.</span></span> <span data-ttu-id="712a5-107">打印目录的设计和生产在 Dynamics 365 for Retail 外部处理。</span><span class="sxs-lookup"><span data-stu-id="712a5-107">The design and production of a printed catalog is handled outside Dynamics 365 for Retail.</span></span> <span data-ttu-id="712a5-108">但是，您可以使用您用来设置联机零售目录的同一页面创建和存储目录的数字窗体。</span><span class="sxs-lookup"><span data-stu-id="712a5-108">However, you can create and store a digital form of a catalog by using the same pages that you use to set up online retail catalogs.</span></span> <span data-ttu-id="712a5-109">在您可以创建目录之前，必须设置产品分类和将此分类分配给呼叫中心。</span><span class="sxs-lookup"><span data-stu-id="712a5-109">Before you can create a catalog, you must set up product assortments and assign the assortments to a call center.</span></span> <span data-ttu-id="712a5-110">然后，您可以通过从这些分类中选择产品，从而将产品添加到目录中。</span><span class="sxs-lookup"><span data-stu-id="712a5-110">You then add products to the catalog by selecting products from these assortments.</span></span> <span data-ttu-id="712a5-111">在将产品添加到目录，并且目录就完成好之后，您必须验证该目录来对数据进行验证。</span><span class="sxs-lookup"><span data-stu-id="712a5-111">After products have been added to the catalog, and the catalog is complete, you must validate the catalog to verify the data.</span></span> <span data-ttu-id="712a5-112">然后，必须提交目录以供复查和审核。</span><span class="sxs-lookup"><span data-stu-id="712a5-112">You must then submit the catalog for review and approval.</span></span> <span data-ttu-id="712a5-113">审核目录后，即可发布。</span><span class="sxs-lookup"><span data-stu-id="712a5-113">After the catalog is approved, it can be published.</span></span> <span data-ttu-id="712a5-114">当创建呼叫中心目录时，您可以在发布该目录时，对该目录数据采用快照。</span><span class="sxs-lookup"><span data-stu-id="712a5-114">When a call center catalog is created, you can take a snapshot of the catalog data at the time that the catalog is published.</span></span> <span data-ttu-id="712a5-115">此快照功能允许您访问该目录的某一特定版本，即使以后对该目录做出更改和更新。</span><span class="sxs-lookup"><span data-stu-id="712a5-115">This snapshot functionality lets you access a particular version of the catalog even if the catalog is later changed and updated.</span></span> <span data-ttu-id="712a5-116">还可以对呼叫中心目录进行设置以包括以下可选功能：</span><span class="sxs-lookup"><span data-stu-id="712a5-116">Call center catalogs can also be set up to include the following optional features:</span></span>

-   <span data-ttu-id="712a5-117">**源代码** - 用于跟踪客户对特定目录邮件的响应的源代码。</span><span class="sxs-lookup"><span data-stu-id="712a5-117">**Source codes** – Source codes are used to track the customer response to specific catalog mailings.</span></span>
-   <span data-ttu-id="712a5-118">**免费产品** - 可在不另行收费的情况下包含在客户订单中的产品。</span><span class="sxs-lookup"><span data-stu-id="712a5-118">**Free products** – Products can be included in a customer's order at no additional charge.</span></span> <span data-ttu-id="712a5-119">将目录的源代码输入订单后，这些产品将自动添加到某个订单。</span><span class="sxs-lookup"><span data-stu-id="712a5-119">These products are automatically added to an order when the source code for the catalog is entered into the order.</span></span>
-   <span data-ttu-id="712a5-120">**脚本** - 在创建销售订单时，呼叫中心工作人员向客户读取的脚本和文本。</span><span class="sxs-lookup"><span data-stu-id="712a5-120">**Scripts** – Scripts are texts that a call center worker reads to a customer when a sales order is being created.</span></span> <span data-ttu-id="712a5-121">脚本可以包括问候语或采购方案。</span><span class="sxs-lookup"><span data-stu-id="712a5-121">Scripts can include greetings or purchase suggestions.</span></span>
-   <span data-ttu-id="712a5-122">**页面布局** - 页面布局可捕获产品在打印目录中的页面位置。</span><span class="sxs-lookup"><span data-stu-id="712a5-122">**Page layout** – A page layout captures the page position of products in the printed catalog.</span></span> <span data-ttu-id="712a5-123">此信息用于分析目录区域分析报表。</span><span class="sxs-lookup"><span data-stu-id="712a5-123">This information is used for the catalog area analysis report.</span></span>





