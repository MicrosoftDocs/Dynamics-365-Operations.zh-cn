---
title: "定义和维护零售渠道"
description: "本主题提供设置实体商店（在 Microsoft Dynamics 365 for Retail 中称为零售商店）的流程的概览。 它包含有关在设置零售商店前后必须完成的任务的信息。"
author: mugunthanm
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 055ff18b16fa2680c73564b7a7ef0c087c55e701
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="6a2a0-104">定义和维护零售渠道</span><span class="sxs-lookup"><span data-stu-id="6a2a0-104">Define and maintain retail channels</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="6a2a0-105">本主题提供设置实体商店（在 Microsoft Dynamics 365 for Retail 中称为零售商店）的流程的概览。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as retail stores in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="6a2a0-106">它包含有关在设置零售商店前后必须完成的任务的信息。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-106">It includes information about the tasks that you must complete both before and after you set up a retail store.</span></span>

<span data-ttu-id="6a2a0-107">Dynamics 365 for Retail 支持多个零售渠道，例如在线商店、呼叫中心和实体商店。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-107">Dynamics 365 for Retail supports multiple retail channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="6a2a0-108">实体商店也叫做零售商店。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-108">A brick-and-mortar store is called a retail store.</span></span> <span data-ttu-id="6a2a0-109">每个零售商店可以有自己的付款方式、价格组、销售终端 (POS) 收银机、收入帐户和支出帐户以及职员。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-109">Each retail store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="6a2a0-110">您必须先为零售商店设置所有这些元素，然后再创建零售商店。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-110">You must set up all these elements for a retail store before you create it.</span></span> <span data-ttu-id="6a2a0-111">在创建零售商店后，分配您希望其提供的产品。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-111">After you create the retail store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="6a2a0-112">您还可以将员工、收银机和客户分配到商店。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="6a2a0-113">最后，您将新商店添加到组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-retail-stores"></a><span data-ttu-id="6a2a0-114">设置零售商店</span><span class="sxs-lookup"><span data-stu-id="6a2a0-114">Setting up retail stores</span></span>
<span data-ttu-id="6a2a0-115">您必须先完成一些先决任务，然后才能在 Dynamics 365 for Retail 中设置零售商店。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-115">Before you can set up a retail store in Dynamics 365 for Retail, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="6a2a0-116">然后，您可以创建零售商店并添加详细信息。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-116">You can then create the retail store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="6a2a0-117">必备项</span><span class="sxs-lookup"><span data-stu-id="6a2a0-117">Prerequisites</span></span>

<span data-ttu-id="6a2a0-118">您必须先完成以下任务，然后才能设置零售商店：</span><span class="sxs-lookup"><span data-stu-id="6a2a0-118">You must complete the following tasks before you can set up a retail store:</span></span>

1.  <span data-ttu-id="6a2a0-119">配置您的组织结构和设置零售分类、补货和报告的组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2.  <span data-ttu-id="6a2a0-120">设置代表零售商店的仓库。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-120">Set up a warehouse that represents the retail store.</span></span>
3.  <span data-ttu-id="6a2a0-121">设置零售商店、商店报表和报表凭证的编号规则。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-121">Set up number sequences for retail stores, store statements, and statement vouchers.</span></span>
4.  <span data-ttu-id="6a2a0-122">配置零售的参数。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-122">Configure parameters for Retail.</span></span>
5.  <span data-ttu-id="6a2a0-123">设置商店接受的付款方式。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-123">Set up the methods of payment that the store accepts.</span></span>
6.  <span data-ttu-id="6a2a0-124">要处理零售 POS 收银机上的信用卡交易记录，您还可以设置付款服务。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-124">To process credit card transactions at retail POS registers, you can also set up payment services.</span></span>
7.  <span data-ttu-id="6a2a0-125">设置销售税组。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-125">Set up sales tax groups.</span></span>
8.  <span data-ttu-id="6a2a0-126">设置零售产品。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-126">Set up retail products.</span></span> <span data-ttu-id="6a2a0-127">作为此任务的一部分，您还可设置零售产品层次结构、产品变型和产品分类。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-127">As part of this task, you also set up retail product hierarchies, product variants, and product assortments.</span></span>
9.  <span data-ttu-id="6a2a0-128">设置产品价格组。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-128">Set up product price groups.</span></span>
10. <span data-ttu-id="6a2a0-129">设置零售产品定价。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-129">Set up retail product pricing.</span></span> <span data-ttu-id="6a2a0-130">作为此任务的一部分，您还可设置价格调整、折扣和折扣期间。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="6a2a0-131">设置职员。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-131">Set up staff members.</span></span> <span data-ttu-id="6a2a0-132">**注意：**您还必须向工作人员分配适当的权限，以便他们可使用适用于 Retail POS 系统的 Dynamics 365 for Retail 登录并执行任务。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-132">**Note:** You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the Dynamics 365 for Retail for Retail POS system.</span></span>
12. <span data-ttu-id="6a2a0-133">配置要分配给商店的 Retail POS 配置文件。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-133">Configure the Retail POS profiles to assign to the store.</span></span> <span data-ttu-id="6a2a0-134">此任务包括许多其他任务，例如，设置收银机、设置脱机配置文件和设置收据格式和配置文件。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="6a2a0-135">查看包含在先决任务中的所有任务，并仅完成适用于您的任务。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-135">Review all the tasks that are included in the prerequisite, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-retail-store"></a><span data-ttu-id="6a2a0-136">设置零售商店</span><span class="sxs-lookup"><span data-stu-id="6a2a0-136">Set up a retail store</span></span>

<span data-ttu-id="6a2a0-137">在您完成先决任务后，完成以下任务以设置零售商店的详细信息：</span><span class="sxs-lookup"><span data-stu-id="6a2a0-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the retail store:</span></span>

1.  <span data-ttu-id="6a2a0-138">创建零售商店。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-138">Create a retail store.</span></span>
2.  <span data-ttu-id="6a2a0-139">将销售税组分配给商店。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-139">Assign a sales tax group to the store.</span></span>
3.  <span data-ttu-id="6a2a0-140">分配商店接受的付款方式。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-140">Assign the accepted payment methods to the store.</span></span>
4.  <span data-ttu-id="6a2a0-141">对您零售商店中提供的产品，添加有关产品描述的详细信息。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-141">Add details to the product descriptions for products that you offer in your retail stores.</span></span> <span data-ttu-id="6a2a0-142">例如，您可以添加富文本和图像。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="6a2a0-143">这些产品详细信息将在各种情况下显示，例如 POS 收银机或已打印的标签上。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5.  <span data-ttu-id="6a2a0-144">将商店添加到已分配到**“零售分类”**、**“零售补货”**或**“零售报告”**的默认组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-retail-store"></a><span data-ttu-id="6a2a0-145">在您设置了零售商店后</span><span class="sxs-lookup"><span data-stu-id="6a2a0-145">After you set up a retail store</span></span>

<span data-ttu-id="6a2a0-146">在输入零售商店的详细信息后，请完成以下任务以将新的零售商店数据发送到 Retail POS：</span><span class="sxs-lookup"><span data-stu-id="6a2a0-146">After you enter the details for the retail store, complete these tasks to send the new retail store data to Retail POS:</span></span>

1.  <span data-ttu-id="6a2a0-147">配置商店的 POS 收银机。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-147">Configure the POS registers for the store.</span></span>
2.  <span data-ttu-id="6a2a0-148">将产品分类分配到商店。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-148">Assign product assortments to the store.</span></span>
3.  <span data-ttu-id="6a2a0-149">处理分类以生成包含在分类中的产品列表并使该产品可用在零售商店找到。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store.</span></span>
4.  <span data-ttu-id="6a2a0-150">将数据（例如编号规则、硬件配置文件和 POS 屏幕布局）发送到 Retail POS 收银机。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.</span></span>
5.  <span data-ttu-id="6a2a0-151">发布零售商店以将商店数据发送到 Retail POS。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-151">Publish the retail store to send store data to Retail POS.</span></span>
6.  <span data-ttu-id="6a2a0-152">运行作业以将商店数据发送到 Retail POS。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-152">Run the jobs to send the store data to Retail POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="6a2a0-153">组织层次结构</span><span class="sxs-lookup"><span data-stu-id="6a2a0-153">Organization hierarchies</span></span>
<span data-ttu-id="6a2a0-154">Retail 使用组织层次机构来构造零售渠道。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-154">Retail uses organization hierarchies to structure retail channels.</span></span> <span data-ttu-id="6a2a0-155">组织层次结构表示构成贵企业组织之间的关系。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="6a2a0-156">在您设置商店时，您可以添加到组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="6a2a0-157">存储然后共享用于分类、补货和报告的数据。</span><span class="sxs-lookup"><span data-stu-id="6a2a0-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>




