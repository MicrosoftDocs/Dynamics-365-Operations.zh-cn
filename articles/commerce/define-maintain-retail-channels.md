---
title: 定义和维护零售渠道
description: 本主题提供设置实体商店（在 Dynamics 365 Commerce 中称为商店）的流程的概览。 它包含有关在设置商店前后必须完成的任务的信息。
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 51524ad6918d962d70a8a700f135f96e236f7d34
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000867"
---
# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="5d0e8-104">定义和维护零售渠道</span><span class="sxs-lookup"><span data-stu-id="5d0e8-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5d0e8-105">本主题提供设置实体商店（在 Dynamics 365 Commerce 中称为商店）的流程的概览。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as stores in Dynamics 365 Commerce.</span></span> <span data-ttu-id="5d0e8-106">它包含有关在设置商店前后必须完成的任务的信息。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-106">It includes information about the tasks that you must complete both before and after you set up a store.</span></span>

<span data-ttu-id="5d0e8-107">Commerce 支持多个渠道，例如在线商店、呼叫中心和实体商店。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-107">Commerce supports multiple channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="5d0e8-108">实体商店也叫做商店。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-108">A brick-and-mortar store is called a store.</span></span> <span data-ttu-id="5d0e8-109">每个商店可以有自己的付款方式、价格组、销售终端收银机 (POS)、登记、收入帐户和支出帐户以及职员。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-109">Each store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="5d0e8-110">您必须先为商店设置所有这些元素，然后再创建商店。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-110">You must set up all these elements for a store before you create it.</span></span> <span data-ttu-id="5d0e8-111">在创建商店后，分配您希望其提供的产品。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-111">After you create the store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="5d0e8-112">您还可以将员工、收银机和客户分配到商店。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="5d0e8-113">最后，您将新商店添加到组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-stores"></a><span data-ttu-id="5d0e8-114">设置存储</span><span class="sxs-lookup"><span data-stu-id="5d0e8-114">Setting up stores</span></span>

<span data-ttu-id="5d0e8-115">在您可以在 Commerce 中设置商店之前，必须完成某些先决任务。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-115">Before you can set up a store in Commerce, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="5d0e8-116">然后，您可以创建商店并添加详细信息。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-116">You can then create the store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="5d0e8-117">先决条件</span><span class="sxs-lookup"><span data-stu-id="5d0e8-117">Prerequisites</span></span>

<span data-ttu-id="5d0e8-118">您必须先完成以下任务，然后才能设置商店：</span><span class="sxs-lookup"><span data-stu-id="5d0e8-118">You must complete the following tasks before you can set up a store:</span></span>

1. <span data-ttu-id="5d0e8-119">配置您的组织结构和设置零售分类、补货和报告的组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="5d0e8-120">设置代表商店的仓库。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-120">Set up a warehouse that represents the store.</span></span>
3. <span data-ttu-id="5d0e8-121">设置商店、商店报表和报表凭证的编号规则。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-121">Set up number sequences for stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="5d0e8-122">配置 Commerce 参数。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-122">Configure parameters for Commerce.</span></span>
5. <span data-ttu-id="5d0e8-123">设置商店接受的付款方式。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="5d0e8-124">要处理 POS 收银机上的信用卡交易记录，您还可以设置付款服务。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-124">To process credit card transactions at POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="5d0e8-125">设置销售税组。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="5d0e8-126">设置产品：</span><span class="sxs-lookup"><span data-stu-id="5d0e8-126">Set up products.</span></span> <span data-ttu-id="5d0e8-127">作为此任务的一部分，您还可设置产品层次结构、产品变型和产品分类。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-127">As part of this task, you also set up product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="5d0e8-128">设置产品价格组。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-128">Set up product price groups.</span></span>
10. <span data-ttu-id="5d0e8-129">设置产品定价。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-129">Set up product pricing.</span></span> <span data-ttu-id="5d0e8-130">作为此任务的一部分，您还可设置价格调整、折扣和折扣期间。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="5d0e8-131">设置职员。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5d0e8-132">您还必须向工作人员分配适当的权限，以便他们可使用 POS 系统登录并执行任务。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the POS system.</span></span>

12. <span data-ttu-id="5d0e8-133">配置要分配给商店的 POS 配置文件。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-133">Configure the POS profiles to assign to the store.</span></span> <span data-ttu-id="5d0e8-134">此任务包括许多其他任务，例如，设置收银机、设置脱机配置文件和设置收据格式和配置文件。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="5d0e8-135">查看包含在先决任务中的所有任务，并仅完成适用于您的任务。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-135">Review all the tasks that are included in the prerequisites, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-store"></a><span data-ttu-id="5d0e8-136">设置商店</span><span class="sxs-lookup"><span data-stu-id="5d0e8-136">Set up a store</span></span>

<span data-ttu-id="5d0e8-137">在您完成先决任务后，完成以下任务以设置商店的详细信息：</span><span class="sxs-lookup"><span data-stu-id="5d0e8-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the store:</span></span>

1. <span data-ttu-id="5d0e8-138">创建商店。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-138">Create a store.</span></span>
2. <span data-ttu-id="5d0e8-139">将销售税组分配给商店。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="5d0e8-140">分配商店接受的付款方式。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="5d0e8-141">对您商店中提供的产品，添加有关产品描述的详细信息。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-141">Add details to the product descriptions for products that you offer in your stores.</span></span> <span data-ttu-id="5d0e8-142">例如，您可以添加富文本和图像。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="5d0e8-143">这些产品详细信息将在各种情况下显示，例如 POS 收银机或已打印的标签上。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="5d0e8-144">将商店添加到已分配到 **零售分类**、**零售补货** 或 **零售报告** 的默认组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-store"></a><span data-ttu-id="5d0e8-145">在您设置了商店后</span><span class="sxs-lookup"><span data-stu-id="5d0e8-145">After you set up a store</span></span>

<span data-ttu-id="5d0e8-146">在输入商店的详细信息后，请完成以下任务以发送新的商店数据到 POS：</span><span class="sxs-lookup"><span data-stu-id="5d0e8-146">After you enter the details for the store, complete these tasks to send the new store data to POS:</span></span>

1. <span data-ttu-id="5d0e8-147">配置商店的 POS 收银机。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="5d0e8-148">将产品分类分配到商店。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="5d0e8-149">处理分类以生成包含在分类中的产品列表并使该产品可用在商店找到。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the store.</span></span>
4. <span data-ttu-id="5d0e8-150">将数据（例如编号规则、硬件配置文件和 POS 屏幕布局）发送到 POS 收银机。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the POS registers.</span></span>
5. <span data-ttu-id="5d0e8-151">发布商店，从而将商店数据发送到 POS。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-151">Publish the store to send store data to POS.</span></span>
6. <span data-ttu-id="5d0e8-152">运行作业以将商店数据发送到 POS。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-152">Run the jobs to send the store data to POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="5d0e8-153">组织层次结构</span><span class="sxs-lookup"><span data-stu-id="5d0e8-153">Organization hierarchies</span></span>

<span data-ttu-id="5d0e8-154">Commerce 使用组织层次机构来构造渠道。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-154">Commerce uses organization hierarchies to structure channels.</span></span> <span data-ttu-id="5d0e8-155">组织层次结构表示构成贵企业组织之间的关系。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="5d0e8-156">在您设置商店时，您可以添加到组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="5d0e8-157">存储然后共享用于分类、补货和报告的数据。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>

> [!NOTE]
> <span data-ttu-id="5d0e8-158">要使用 Commerce 销售功能，**多次收货** 的配置键必须启用。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-158">To use Commerce sales functionality, the configuration key for **Multiple ship-to** must be enabled.</span></span> <span data-ttu-id="5d0e8-159">可以在 **系统管理** \> **设置** \> **许可证配置** 下的 **贸易配置** 键中找到此配置键。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-159">This configuration key can be found in the **Trade configuration** keys under **System Administration**\> **Setup** \> **License Configuration**.</span></span> <span data-ttu-id="5d0e8-160">由于会根据在销售订单行级别配置的交货地址执行各种验证，因此这是必需的。</span><span class="sxs-lookup"><span data-stu-id="5d0e8-160">This is required due to various validations based on the delivery address configured at the sales order line level.</span></span>

