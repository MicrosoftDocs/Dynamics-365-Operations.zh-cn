---
title: "创建呼叫中心目录"
description: "文本提供创建呼叫中心目录的流程的概览。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, RetailCatalogDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16212
ms.assetid: c9d1b9df-82e8-4b3a-a13c-166df8b9718e
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: bec83606ec6482cba7231356910312c10e20cca2
ms.contentlocale: zh-cn
ms.lasthandoff: 01/17/2018

---

# <a name="create-a-call-center-catalog"></a><span data-ttu-id="d103c-103">创建呼叫中心目录</span><span class="sxs-lookup"><span data-stu-id="d103c-103">Create a call center catalog</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="d103c-104">文本提供创建呼叫中心目录的流程的概览。</span><span class="sxs-lookup"><span data-stu-id="d103c-104">This article provides an overview of the process for creating a catalog for a call center.</span></span> 

<span data-ttu-id="d103c-105">在呼叫中心，可以使用产品目录来标识您要为客户提供的产品。</span><span class="sxs-lookup"><span data-stu-id="d103c-105">In a call center, you can use product catalogs to identify the products that you want to offer to customers.</span></span> <span data-ttu-id="d103c-106">呼叫中心常使用打印目录。</span><span class="sxs-lookup"><span data-stu-id="d103c-106">Call centers typically use printed catalogs.</span></span> <span data-ttu-id="d103c-107">打印目录的设计和生产在 Microsoft Dynamics 365 for Retail 外部处理。</span><span class="sxs-lookup"><span data-stu-id="d103c-107">The design and production of a printed catalog is handled outside Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="d103c-108">但是，您可以使用您用来设置联机零售目录的相同窗体创建和存储目录的数字窗体。</span><span class="sxs-lookup"><span data-stu-id="d103c-108">However, you can create and store a digital form of a catalog by using the same forms that you use to set up online retail catalogs.</span></span> <span data-ttu-id="d103c-109">在您可以创建目录之前，必须设置产品分类和将此分类分配给呼叫中心。</span><span class="sxs-lookup"><span data-stu-id="d103c-109">Before you can create a catalog, you must set up product assortments and assign the assortments to a call center.</span></span> <span data-ttu-id="d103c-110">然后，您可以通过从这些分类中选择产品，从而将产品添加到目录中。</span><span class="sxs-lookup"><span data-stu-id="d103c-110">You then add products to the catalog by selecting products from these assortments.</span></span> <span data-ttu-id="d103c-111">在将产品添加到目录，并且目录就完成好之后，您必须验证该目录来对数据进行验证。</span><span class="sxs-lookup"><span data-stu-id="d103c-111">After products have been added to the catalog, and the catalog is complete, you must validate the catalog to verify the data.</span></span> <span data-ttu-id="d103c-112">然后，必须提交目录以供复查和审核。</span><span class="sxs-lookup"><span data-stu-id="d103c-112">You must then submit the catalog for review and approval.</span></span> <span data-ttu-id="d103c-113">审核目录后，即可发布。</span><span class="sxs-lookup"><span data-stu-id="d103c-113">After the catalog is approved, it can be published.</span></span> <span data-ttu-id="d103c-114">当创建呼叫中心目录时，您可以在发布该目录时，对该目录数据采用快照。</span><span class="sxs-lookup"><span data-stu-id="d103c-114">When a call center catalog is created, you can take a snapshot of the catalog data at the time when the catalog is published.</span></span> <span data-ttu-id="d103c-115">此快照功能允许您访问该目录的某一特定版本，即使以后对该目录做出更改和更新。</span><span class="sxs-lookup"><span data-stu-id="d103c-115">This snapshot functionality lets you access a particular version of the catalog even if the catalog is later changed and updated.</span></span> <span data-ttu-id="d103c-116">还可以对呼叫中心目录进行设置以包括以下可选功能。</span><span class="sxs-lookup"><span data-stu-id="d103c-116">Call center catalogs can also be set up to include the following optional features.</span></span>

-   <span data-ttu-id="d103c-117">**源代码** – 用于跟踪客户对特定目录邮件的响应的代码。</span><span class="sxs-lookup"><span data-stu-id="d103c-117">**Source codes** – Codes that are used to track the customer response to particular catalog mailings.</span></span>
-   <span data-ttu-id="d103c-118">**免费产品** – 在不另行收费的情况下包含在客户订单中的产品。</span><span class="sxs-lookup"><span data-stu-id="d103c-118">**Free products** – Products that are included in a customer's order at no additional charge.</span></span> <span data-ttu-id="d103c-119">当把该目录的源代码输入订单时，这些产品会被自动添加到该订单。</span><span class="sxs-lookup"><span data-stu-id="d103c-119">These products are automatically added to the order when the source code for the catalog is entered into the order.</span></span>
-   <span data-ttu-id="d103c-120">**脚本** – 在创建销售订单时，呼叫中心工作人员给客户朗读的文本。</span><span class="sxs-lookup"><span data-stu-id="d103c-120">**Scripts** – Texts that a call center worker reads to a customer when a sales order is being created.</span></span> <span data-ttu-id="d103c-121">脚本可以包括问候语或采购方案。</span><span class="sxs-lookup"><span data-stu-id="d103c-121">Scripts can include greetings or purchase suggestions.</span></span>
-   <span data-ttu-id="d103c-122">**向上销售或交叉销售物料** - 在特定产品添加到订单时显示为建议的物料。</span><span class="sxs-lookup"><span data-stu-id="d103c-122">**Upsell or cross-sell items** - Items that are displayed as a suggestion when a specific product is added to the order.</span></span>

<span data-ttu-id="d103c-123">在审核和发布目录之前，必须设置这些选项。</span><span class="sxs-lookup"><span data-stu-id="d103c-123">These options must be set up before the catalog is approved and published.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d103c-124">必备项</span><span class="sxs-lookup"><span data-stu-id="d103c-124">Prerequisites</span></span>
<span data-ttu-id="d103c-125">在您开始之前，必须完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="d103c-125">The following tasks must be completed before you start:</span></span>

-   <span data-ttu-id="d103c-126">设置产品和产品分类。</span><span class="sxs-lookup"><span data-stu-id="d103c-126">Set up products and product assortments.</span></span>
-   <span data-ttu-id="d103c-127">设置零售产品。</span><span class="sxs-lookup"><span data-stu-id="d103c-127">Set up retail products.</span></span>
-   <span data-ttu-id="d103c-128">设置分类。</span><span class="sxs-lookup"><span data-stu-id="d103c-128">Set up an assortment.</span></span>
-   <span data-ttu-id="d103c-129">创建呼叫中心。</span><span class="sxs-lookup"><span data-stu-id="d103c-129">Create a call center.</span></span>
-   <span data-ttu-id="d103c-130">设置呼叫中心。</span><span class="sxs-lookup"><span data-stu-id="d103c-130">Set up a call center.</span></span>
-   <span data-ttu-id="d103c-131">将呼叫中心添加到组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="d103c-131">Add the call center to an organization hierarchy.</span></span>
-   <span data-ttu-id="d103c-132">创建或修改组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="d103c-132">Create or modify an organization hierarchy.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="d103c-133">创建目录</span><span class="sxs-lookup"><span data-stu-id="d103c-133">Create a catalog</span></span>
<span data-ttu-id="d103c-134">您必须首先创建一个目录，再将产品添加到该目录中，然后审查并更新产品的属性。</span><span class="sxs-lookup"><span data-stu-id="d103c-134">You must first create a catalog, add products to the catalog, and then review and update the attributes for the products.</span></span>

## <a name="validate-the-catalog"></a><span data-ttu-id="d103c-135">验证目录</span><span class="sxs-lookup"><span data-stu-id="d103c-135">Validate the catalog</span></span>
<span data-ttu-id="d103c-136">在您完成设置该目录后，必须验证它。</span><span class="sxs-lookup"><span data-stu-id="d103c-136">After you've finished setting up the catalog, you must validate it.</span></span> <span data-ttu-id="d103c-137">此验证流程验证渠道属性和产品属性所需的数据是否完整有效，并验证是否可以发布此目录。</span><span class="sxs-lookup"><span data-stu-id="d103c-137">The validation process verifies that the data that is required for channel attributes and product attributes is complete and valid, and that the catalog can be published.</span></span>

## <a name="submit-the-catalog-for-review-and-approval"></a><span data-ttu-id="d103c-138">提交目录以供审核和批准</span><span class="sxs-lookup"><span data-stu-id="d103c-138">Submit the catalog for review and approval</span></span>
<span data-ttu-id="d103c-139">验证目录后，您可以提交目录以供审查和审核。</span><span class="sxs-lookup"><span data-stu-id="d103c-139">After a catalog is validated, you can submit the catalog for review and approval.</span></span> <span data-ttu-id="d103c-140">必须先审核目录，然后才可发布。</span><span class="sxs-lookup"><span data-stu-id="d103c-140">A catalog must be approved before it can be published.</span></span> <span data-ttu-id="d103c-141">您可以配置工作流，以便自动审核目录或需要人工审核。</span><span class="sxs-lookup"><span data-stu-id="d103c-141">You can configure a workflow so that catalogs either are automatically approved or require manual approval.</span></span>

## <a name="optional-add-source-codes-free-products-and-scripts"></a><span data-ttu-id="d103c-142">可选：添加源代码、免费产品和脚本</span><span class="sxs-lookup"><span data-stu-id="d103c-142">Optional: Add source codes, free products, and scripts</span></span>
<span data-ttu-id="d103c-143">您还可以将以下各项添加到呼叫中心目录。</span><span class="sxs-lookup"><span data-stu-id="d103c-143">You can also add the following items to a call center catalog.</span></span> <span data-ttu-id="d103c-144">这些项是可选的。</span><span class="sxs-lookup"><span data-stu-id="d103c-144">These items are optional.</span></span>

-   <span data-ttu-id="d103c-145">**“源代码”**可以由提供印刷目录的公司使用，用来跟踪客户对特定目录的响应。</span><span class="sxs-lookup"><span data-stu-id="d103c-145">**Source codes** can be used by companies that provide printed catalogs to track the customer response to particular catalogs.</span></span> <span data-ttu-id="d103c-146">源代码通常被印刷在目录的背面，在客户购买时也会输入到销售订单中。</span><span class="sxs-lookup"><span data-stu-id="d103c-146">Source codes are often printed on the back of a catalog and are entered into the sales order when a customer makes a purchase.</span></span> <span data-ttu-id="d103c-147">若要将源代码添加给目录，您必须首先创建目标市场。</span><span class="sxs-lookup"><span data-stu-id="d103c-147">To add a source code to the catalog, you must first create a target market.</span></span> <span data-ttu-id="d103c-148">目标市场通常映射到所拥有的或租赁的邮寄列表。</span><span class="sxs-lookup"><span data-stu-id="d103c-148">The target market is usually mapped to an owned or rented mailing list.</span></span>
-   <span data-ttu-id="d103c-149">**免费产品**是促销物料，在引用该目录时会免费包括在客户的订单中。</span><span class="sxs-lookup"><span data-stu-id="d103c-149">**Free products** are promotional items that are included free of charge with the customer's order when the catalog is referenced.</span></span>
-   <span data-ttu-id="d103c-150">**脚本**可以用于在目录上下文或目录内的产品中引导工作人员与客户的交互。</span><span class="sxs-lookup"><span data-stu-id="d103c-150">**Scripts** can be used to guide the worker's interactions with customers in the context of a catalog or a product within a catalog.</span></span>

## <a name="publish-the-catalog"></a><span data-ttu-id="d103c-151">发布目录</span><span class="sxs-lookup"><span data-stu-id="d103c-151">Publish the catalog</span></span>
<span data-ttu-id="d103c-152">通过发布呼叫中心的目录，就完成了该目录中的产品信息。</span><span class="sxs-lookup"><span data-stu-id="d103c-152">By publishing a catalog for a call center, you finalize the product information in the catalog.</span></span> <span data-ttu-id="d103c-153">发布还指示该目录可供您要执行的任何其他操作使用。</span><span class="sxs-lookup"><span data-stu-id="d103c-153">Publication also indicates that the catalog is ready for any additional actions that you want to perform.</span></span> <span data-ttu-id="d103c-154">例如，您可以创建打印目录。</span><span class="sxs-lookup"><span data-stu-id="d103c-154">For example, you can create a printed catalog.</span></span> <span data-ttu-id="d103c-155">您可以手动发布目录，也可以按照计划使用批处理发布。</span><span class="sxs-lookup"><span data-stu-id="d103c-155">You can publish your catalogs manually, or you can use a batch process to publish according to a schedule.</span></span> <span data-ttu-id="d103c-156">必须先验证和审核目录，然后才能发布目录。</span><span class="sxs-lookup"><span data-stu-id="d103c-156">Before you can publish a catalog, the catalog must be validated and approved.</span></span> <span data-ttu-id="d103c-157">发布目录后，若要更改该目录，可以撤销该目录，然后重新发布它。</span><span class="sxs-lookup"><span data-stu-id="d103c-157">To change the catalog after it's published, you can retract the catalog and then republish it.</span></span>




