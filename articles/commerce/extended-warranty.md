---
title: 创建和配置延长保修
description: 本主题介绍延长保修，以及如何在 Microsoft Dynamics 365 Commerce 中创建和配置延长保修。
author: sijoshi
manager: annbe
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: sijoshi
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a875343d9b93f5ebf2c2992fba8b2f182310461e
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621185"
---
# <a name="create-and-configure-extended-warranties"></a><span data-ttu-id="109a6-103">创建和配置延长保修</span><span class="sxs-lookup"><span data-stu-id="109a6-103">Create and configure extended warranties</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="109a6-104">本主题介绍延长保修，以及如何在 Microsoft Dynamics 365 Commerce 中创建和配置延长保修。</span><span class="sxs-lookup"><span data-stu-id="109a6-104">This topic covers extended warranties and describes how to create and configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="109a6-105">概览</span><span class="sxs-lookup"><span data-stu-id="109a6-105">Overview</span></span>

<span data-ttu-id="109a6-106">在购买产品时，尤其是在购买高价出售的消费产品（如手机和计算机）时，客户越来越多地会选择延长支持和服务。</span><span class="sxs-lookup"><span data-stu-id="109a6-106">Customers are increasingly choosing extended support and services when they buy products, especially consumer products that are sold at a premium price point, such as phones and computers.</span></span> <span data-ttu-id="109a6-107">通过为购买的产品提供延长保修，零售商可以帮助建立客户忠诚度。</span><span class="sxs-lookup"><span data-stu-id="109a6-107">By providing extended warranties for purchase, retailers can help build customer loyalty.</span></span> <span data-ttu-id="109a6-108">延长保修让客户知道可以在哪里获得服务和支持。</span><span class="sxs-lookup"><span data-stu-id="109a6-108">Extended warranties let customers know where they can go for service and support.</span></span> <span data-ttu-id="109a6-109">因此，他们可以确信自己的问题将得到有效处理。</span><span class="sxs-lookup"><span data-stu-id="109a6-109">Therefore, they can have confidence that their issues will be handled effectively.</span></span>

<span data-ttu-id="109a6-110">延长保修可以在最初购买产品时通过零售渠道向客户出售。</span><span class="sxs-lookup"><span data-stu-id="109a6-110">Extended warranties can be sold to customers in a retail channel during the initial product purchase.</span></span> <span data-ttu-id="109a6-111">也可以在最初购买后的限定时间内出售。</span><span class="sxs-lookup"><span data-stu-id="109a6-111">They can also be sold for a limited time after the initial purchase.</span></span>

### <a name="warranty-item-setup"></a><span data-ttu-id="109a6-112">保修物料设置</span><span class="sxs-lookup"><span data-stu-id="109a6-112">Warranty item setup</span></span>

<span data-ttu-id="109a6-113">Dynamics 365 Commerce 提供的功能可让您创建保修物料并为其设置属性。</span><span class="sxs-lookup"><span data-stu-id="109a6-113">Dynamics 365 Commerce provides functionality that lets you create a warranty item and set attributes for it.</span></span> <span data-ttu-id="109a6-114">这些属性包括产品与保修项目之间的关联、保修价格以及保修期限。</span><span class="sxs-lookup"><span data-stu-id="109a6-114">These attributes include the association between a product and a warranty item, the price of the warranty, and the duration of the warranty.</span></span> <span data-ttu-id="109a6-115">在配置了保修项目并将其发布给组织单位之后，零售商可以通过现代销售点 (MPOS)、在线商店和其他零售渠道出售保修。</span><span class="sxs-lookup"><span data-stu-id="109a6-115">After a warranty item is configured and released to the organizational unit, a retailer can sell warranties through Modern Point of Sale (MPOS), online stores, and other retail channels.</span></span>

### <a name="warranty-item-sales"></a><span data-ttu-id="109a6-116">保修项目销售</span><span class="sxs-lookup"><span data-stu-id="109a6-116">Warranty item sales</span></span>

<span data-ttu-id="109a6-117">延长保修在最初购买产品时通过零售渠道出售。</span><span class="sxs-lookup"><span data-stu-id="109a6-117">Extended warranties are sold in a retail channel during the initial product purchase.</span></span> <span data-ttu-id="109a6-118">也可以在最初购买后的限定时间内出售。</span><span class="sxs-lookup"><span data-stu-id="109a6-118">They can also be sold for a limited time after the initial purchase.</span></span>

<span data-ttu-id="109a6-119">在销售点 (POS)，当相关产品被添加到客户的购物车时，系统会提示销售内勤添加延长保修。</span><span class="sxs-lookup"><span data-stu-id="109a6-119">At the point of sale (POS), sales associates are prompted to add an extended warranty when a related product is added to a customer's cart.</span></span> <span data-ttu-id="109a6-120">因此，追加销售或交叉销售机会将作为销售流的一部分显示给销售内勤。</span><span class="sxs-lookup"><span data-stu-id="109a6-120">Therefore, an upsell or cross-sell opportunity is presented to sales associates as part of the sales flow.</span></span>

<span data-ttu-id="109a6-121">客户也可以后来返回为他们先前购买的产品购买延长保修。</span><span class="sxs-lookup"><span data-stu-id="109a6-121">Customers can also return later and buy an extended warranty for a product that they previously purchased.</span></span> <span data-ttu-id="109a6-122">在这些情况下，销售内勤可以查找原始交易，然后向客户出售相关的延长保修项目。</span><span class="sxs-lookup"><span data-stu-id="109a6-122">In these cases, a sales associate can look up the original transaction and sell the customer the related extended warranty item.</span></span>

### <a name="warranty-terminology"></a><span data-ttu-id="109a6-123">保修术语</span><span class="sxs-lookup"><span data-stu-id="109a6-123">Warranty terminology</span></span>

<span data-ttu-id="109a6-124">下表定义了一些与保修相关的术语。</span><span class="sxs-lookup"><span data-stu-id="109a6-124">The following table defines some warranty-related terms.</span></span>

| <span data-ttu-id="109a6-125">条款</span><span class="sxs-lookup"><span data-stu-id="109a6-125">Term</span></span> | <span data-ttu-id="109a6-126">说明</span><span class="sxs-lookup"><span data-stu-id="109a6-126">Description</span></span> |
|------------------------------|--------------|
| <span data-ttu-id="109a6-127">延长保修/保修</span><span class="sxs-lookup"><span data-stu-id="109a6-127">Extended warranty/Warranty</span></span> | <span data-ttu-id="109a6-128">*延长保修*是指为客户提供延长保修的服务协议或合同。</span><span class="sxs-lookup"><span data-stu-id="109a6-128">An *extended warranty* refers to a service agreement or contract that provides a prolonged warranty to customers.</span></span> <span data-ttu-id="109a6-129">延长保修包括在延长保修覆盖期间内更换或维修商品的附加服务。</span><span class="sxs-lookup"><span data-stu-id="109a6-129">The extended warranty includes the additional service of replacing or repairing goods during the extended warranty's coverage period.</span></span> |
| <span data-ttu-id="109a6-130">制造商保修</span><span class="sxs-lookup"><span data-stu-id="109a6-130">Manufacturer's warranty</span></span> | <span data-ttu-id="109a6-131">*制造商保修*（通常称为*有限保修*）是客户购买产品时获得的保修。</span><span class="sxs-lookup"><span data-stu-id="109a6-131">A *manufacturer's warranty* (often referred to as a *limited warranty*) is the warranty that customers receive when they purchase a product.</span></span> <span data-ttu-id="109a6-132">以下是制造商保修的一些特征：</span><span class="sxs-lookup"><span data-stu-id="109a6-132">Here are some features of a manufacturer's warranty:</span></span><ul><li><span data-ttu-id="109a6-133">保修成本包含在产品成本中。</span><span class="sxs-lookup"><span data-stu-id="109a6-133">The warranty cost is included in the cost of the product.</span></span> <span data-ttu-id="109a6-134">客户不必为制造商保修支付任何额外费用。</span><span class="sxs-lookup"><span data-stu-id="109a6-134">Customers don't have to pay any additional amount for a manufacturer's warranty.</span></span></li><li><span data-ttu-id="109a6-135">根据产品类别，制造商保修通常持续 30 天、六个月或一年。</span><span class="sxs-lookup"><span data-stu-id="109a6-135">Depending on the product category, a manufacturer's warranty typically lasts 30 days, six months, or one year.</span></span> <span data-ttu-id="109a6-136">（对于大多数消费类电子产品，保修期为一年）。</span><span class="sxs-lookup"><span data-stu-id="109a6-136">(For most consumer electronics, the warranty lasts one year).</span></span></li><li><span data-ttu-id="109a6-137">保修覆盖由于机械或电气故障导致的任何缺陷。</span><span class="sxs-lookup"><span data-stu-id="109a6-137">The warranty covers any defects that are caused by mechanical or electrical failures.</span></span> <span data-ttu-id="109a6-138">覆盖范围有限，不包括对所购买产品的任何意外损坏。</span><span class="sxs-lookup"><span data-stu-id="109a6-138">Coverage is limited, and it doesn't include any accidental damage to the purchased product.</span></span> <span data-ttu-id="109a6-139">想要为所购买产品提供日常损坏保护的客户应该购买延长保修。</span><span class="sxs-lookup"><span data-stu-id="109a6-139">Customers who want to protect the products that they purchase from everyday damages should invest in an extended warranty.</span></span> <span data-ttu-id="109a6-140">延长保修期为两到十年，具体取决于产品类别。</span><span class="sxs-lookup"><span data-stu-id="109a6-140">Extended warranties last two to ten years, depending on the product category.</span></span> <span data-ttu-id="109a6-141">另外还具有更广泛的覆盖范围，覆盖日常事故，如跌落、漏损和污渍。</span><span class="sxs-lookup"><span data-stu-id="109a6-141">They also have wider coverage and cover everyday mishaps such as drops, spills, and stains.</span></span></li></ul> |
| <span data-ttu-id="109a6-142">保修物料</span><span class="sxs-lookup"><span data-stu-id="109a6-142">Warranty item</span></span> | <span data-ttu-id="109a6-143">*保修项目*是针对可保修项目出售的延长保修项目。</span><span class="sxs-lookup"><span data-stu-id="109a6-143">A *warranty item* is an extended warranty item that is sold for a warrantable item.</span></span> <span data-ttu-id="109a6-144">一个示例是针对笔记本电脑的两年意外保护计划。</span><span class="sxs-lookup"><span data-stu-id="109a6-144">An example is a two-year accidental protection plan for laptops.</span></span> |
| <span data-ttu-id="109a6-145">可保修物料</span><span class="sxs-lookup"><span data-stu-id="109a6-145">Warrantable item</span></span> | <span data-ttu-id="109a6-146">*可保修物料*是出售保修的序列化产品。</span><span class="sxs-lookup"><span data-stu-id="109a6-146">A *warrantable item* is a serialized product that a warranty is sold for.</span></span> <span data-ttu-id="109a6-147">例如，笔记本电脑是出售两年和三年延长保修的保修项目。</span><span class="sxs-lookup"><span data-stu-id="109a6-147">For example, a laptop is a warrantable item that two-year and three-year extended warranties are sold for.</span></span> |
| <span data-ttu-id="109a6-148">保修组</span><span class="sxs-lookup"><span data-stu-id="109a6-148">Warranty group</span></span> | <span data-ttu-id="109a6-149">*保修组*是保修项目与可保修物料之间的关系。</span><span class="sxs-lookup"><span data-stu-id="109a6-149">A *warranty group* is a relationship between warranty items and warrantable items.</span></span> <span data-ttu-id="109a6-150">POS 使用保修组来确定当将可保修物料添加到客户的购物车时，应提示销售内勤添加哪些保修项目。</span><span class="sxs-lookup"><span data-stu-id="109a6-150">The POS uses warranty groups to determine which warranty items sales associates should be prompted to add when a warrantable item is added to a customer's cart.</span></span> |
| <span data-ttu-id="109a6-151">保修政策</span><span class="sxs-lookup"><span data-stu-id="109a6-151">Warranty policy</span></span> | <span data-ttu-id="109a6-152">*保修政策*是销售保修政策时在 Commerce 中创建的实体。</span><span class="sxs-lookup"><span data-stu-id="109a6-152">A *warranty policy* is an entity that is created in Commerce when a warranty policy is sold.</span></span> <span data-ttu-id="109a6-153">保修政策包括诸如购买的保修项目的开始和结束日期、条款和条件，以及已保修产品的序列号等信息。</span><span class="sxs-lookup"><span data-stu-id="109a6-153">A warranty policy includes information such as the start and end dates of the purchased warranty item, terms and conditions, and the serial number of the warranted product.</span></span> <span data-ttu-id="109a6-154">保修政策编号可以与客户共享，让他们作为所购买延长保修项目的引用信息。</span><span class="sxs-lookup"><span data-stu-id="109a6-154">Warranty policy numbers can be shared with customers, so that they have a reference for the extended warranty item that they purchased.</span></span> |

## <a name="create-a-warranty-item"></a><span data-ttu-id="109a6-155">创建保修项目</span><span class="sxs-lookup"><span data-stu-id="109a6-155">Create a warranty item</span></span>

<span data-ttu-id="109a6-156">要在 Commerce 中创建保修项目，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="109a6-156">To create a warranty item in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="109a6-157">转至 **Retail 和 Commerce \> 产品和类别 \> 产品**。</span><span class="sxs-lookup"><span data-stu-id="109a6-157">Go to **Retail and Commerce \> Products and categories \> Products**.</span></span>
1. <span data-ttu-id="109a6-158">选择**新建**创建保修项目。</span><span class="sxs-lookup"><span data-stu-id="109a6-158">Select **New** to create a warranty item.</span></span>
1. <span data-ttu-id="109a6-159">在**新建产品**对话框中，在**产品类型**字段中选择**服务**。</span><span class="sxs-lookup"><span data-stu-id="109a6-159">In the **New product** dialog box, in the **Product type** field, select **Service**.</span></span>
1. <span data-ttu-id="109a6-160">在**产品子类型**字段中，选择**产品**。</span><span class="sxs-lookup"><span data-stu-id="109a6-160">In the **Product subtype** field, select **Product**.</span></span>
1. <span data-ttu-id="109a6-161">在**产品服务类型**字段中，选择**服务**。</span><span class="sxs-lookup"><span data-stu-id="109a6-161">In the **Product service type** field, select **Service**.</span></span>
1. <span data-ttu-id="109a6-162">在**产品名称**字段中，输入产品名称。</span><span class="sxs-lookup"><span data-stu-id="109a6-162">In the **Product name** field, enter the product name.</span></span>
1. <span data-ttu-id="109a6-163">在**零售类别**字段中，在下拉对话框中选择一个值，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="109a6-163">In the **Retail category** field, select a value in the drop-down dialog box, and then select **OK**.</span></span>
1. <span data-ttu-id="109a6-164">在**产品编号**中，输入产品编号。</span><span class="sxs-lookup"><span data-stu-id="109a6-164">In the **Product number**, enter the product number.</span></span>
1. <span data-ttu-id="109a6-165">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="109a6-165">Select **OK**.</span></span>
1. <span data-ttu-id="109a6-166">在**产品详细信息**页面上，在**保修**快速选项卡上，设置**时间单位**和**时间长度**字段。</span><span class="sxs-lookup"><span data-stu-id="109a6-166">On the **Product details** page, on the **Warranty** FastTab, set the **Unit of time** and **Length of time** fields.</span></span>

    | <span data-ttu-id="109a6-167">字段名称</span><span class="sxs-lookup"><span data-stu-id="109a6-167">Field name</span></span> | <span data-ttu-id="109a6-168">值</span><span class="sxs-lookup"><span data-stu-id="109a6-168">Value</span></span> | <span data-ttu-id="109a6-169">说明</span><span class="sxs-lookup"><span data-stu-id="109a6-169">Description</span></span> |
    |------------|-------|-------------|
    | <span data-ttu-id="109a6-170">时间单位</span><span class="sxs-lookup"><span data-stu-id="109a6-170">Unit of time</span></span> | <span data-ttu-id="109a6-171">**天**、**周**、**月**或**年**</span><span class="sxs-lookup"><span data-stu-id="109a6-171">**Day(s)**, **Week(s)**, **Month(s)**, or **Year(s)**</span></span> | <span data-ttu-id="109a6-172">此字段指定用于保修的时间单位。</span><span class="sxs-lookup"><span data-stu-id="109a6-172">This field specifies the unit of time that is used for the warranty.</span></span> |
    | <span data-ttu-id="109a6-173">时间长度</span><span class="sxs-lookup"><span data-stu-id="109a6-173">Length of time</span></span> | <span data-ttu-id="109a6-174">一个正整数值</span><span class="sxs-lookup"><span data-stu-id="109a6-174">A positive integer value</span></span> | <span data-ttu-id="109a6-175">此字段以所选的时间单位指定保修期限。</span><span class="sxs-lookup"><span data-stu-id="109a6-175">This field specifies the duration of the warranty in the selected unit of time.</span></span> |

    <span data-ttu-id="109a6-176">例如，对于两年保修，将**时间单位**字段设置为**年**，将**时间长度**字段设置为 **2**。</span><span class="sxs-lookup"><span data-stu-id="109a6-176">For example, for a two-year warranty, set the **Unit of time** field to **Year(s)** and the **Length of time** field to **2**.</span></span> <span data-ttu-id="109a6-177">或者，将**时间单位**字段设置为**月**，**时间长度**字段设置为 **24**，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="109a6-177">Alternatively, set the set the **Unit of time** field to **Month(s)** and the **Length of time** field to **24**, as shown in the following illustration.</span></span>

    ![保修项目的产品详细信息页](./media/ew-time-properties.png)

1. <span data-ttu-id="109a6-179">选择**保存**保存保修项目。</span><span class="sxs-lookup"><span data-stu-id="109a6-179">Select **Save** to save the warranty item.</span></span>
1. <span data-ttu-id="109a6-180">将保修产品发布到公司以可以出售。</span><span class="sxs-lookup"><span data-stu-id="109a6-180">Release the warranty product to the company so that it can be sold.</span></span> <span data-ttu-id="109a6-181">有关详细信息，请参阅[设置零售产品](set-up-retail-products.md)。</span><span class="sxs-lookup"><span data-stu-id="109a6-181">For more information, see [Set up retail products](set-up-retail-products.md).</span></span>
1. <span data-ttu-id="109a6-182">在**已发布产品详细信息**页上的**保修**快速选项卡上，设置**价格范围基准**、**下限**和**上限**字段。</span><span class="sxs-lookup"><span data-stu-id="109a6-182">On the **Released product details** page, on the **Warranty** FastTab, set the **Price range base**, **Lower limit**, and **Upper limit** fields.</span></span>

    | <span data-ttu-id="109a6-183">字段名称</span><span class="sxs-lookup"><span data-stu-id="109a6-183">Field name</span></span> | <span data-ttu-id="109a6-184">值</span><span class="sxs-lookup"><span data-stu-id="109a6-184">Value</span></span> | <span data-ttu-id="109a6-185">说明</span><span class="sxs-lookup"><span data-stu-id="109a6-185">Description</span></span> |
    |------------|-------|-------------|
    | <span data-ttu-id="109a6-186">价格范围基数</span><span class="sxs-lookup"><span data-stu-id="109a6-186">Price range base</span></span> | <span data-ttu-id="109a6-187">**无**、**基价**或**出售价格**</span><span class="sxs-lookup"><span data-stu-id="109a6-187">**None**, **Base price**, or **Selling price**</span></span> | <ul><li><span data-ttu-id="109a6-188">**无** – 价格范围的**下限**和**上限**值不适用。</span><span class="sxs-lookup"><span data-stu-id="109a6-188">**None** – The **Lower limit** and **Upper limit** values of price ranges aren't applicable.</span></span></li><li><span data-ttu-id="109a6-189">**基价** – 如果根据可保修物料的价格，保修项目的基价（即没有折扣的价格）在此处指定的**下限**和**上限**之间，给定的保修适用。</span><span class="sxs-lookup"><span data-stu-id="109a6-189">**Base price** – A given warranty will be applicable if the base price (that is, the price without discounts) of the warrantable item is between the **Lower limit** and **Upper limit** values that are specified here, based on the price of the warrantable item.</span></span></li><li><span data-ttu-id="109a6-190">**出售价格** – 保留此值供将来使用。</span><span class="sxs-lookup"><span data-stu-id="109a6-190">**Selling price** – This value is reserved for future use.</span></span></li></ul> |
    | <span data-ttu-id="109a6-191">下限、上限</span><span class="sxs-lookup"><span data-stu-id="109a6-191">Lower limit, Upper limit</span></span> | <span data-ttu-id="109a6-192">一个正整数值</span><span class="sxs-lookup"><span data-stu-id="109a6-192">A positive integer value</span></span> | <span data-ttu-id="109a6-193">这些字段定义可保修物料的价格上限和下限，以及当前保修项目对于可保修物料的适用程度。</span><span class="sxs-lookup"><span data-stu-id="109a6-193">These fields define the upper and lower price limits of the warrantable item, and how the current warranty item is applicable to the warrantable item.</span></span> <span data-ttu-id="109a6-194">这些限制可以基于可保修物料的基价（也称为制造商建议零售价 \[MSRP\]）。</span><span class="sxs-lookup"><span data-stu-id="109a6-194">These limits can be based on the warrantable item's base price (also known as the manufacturer's suggested retail price \[MSRP\]).</span></span> <span data-ttu-id="109a6-195">如果将**价格范围基准**字段设置为**基价**，则仅基价在**下限**和**上限**值之间的可保修物料（产品）会在 POS 上触发添加保修项目的提示。</span><span class="sxs-lookup"><span data-stu-id="109a6-195">If the **Price range base** field is set to **Base price**, only a warrantable item (product) that has a base price between the **Lower limit** and **Upper limit** values will trigger a prompt to add the warranty item at the POS.</span></span> |

    <span data-ttu-id="109a6-196">例如，下图显示**价格范围基准**字段设置为**基价**，**下限**字段设置为 500 美元，**上限**字段设置为 1000 美元。</span><span class="sxs-lookup"><span data-stu-id="109a6-196">For example, the following illustration shows the **Price range base** field set to **Base price**, the **Lower limit** field set to $500, and the **Upper limit** field set to $1000.</span></span>
    
    ![保修项目的已发布产品详细信息页](./media/ew-release-product-details.png)

1. <span data-ttu-id="109a6-198">将保修项目分类到将出售的渠道。</span><span class="sxs-lookup"><span data-stu-id="109a6-198">Assort the warranty item to the channel where it will be sold.</span></span> <span data-ttu-id="109a6-199">有关详细信息，请参阅[设置分类](set-up-assortments.md)。</span><span class="sxs-lookup"><span data-stu-id="109a6-199">For more information, see [Set up assortments](set-up-assortments.md).</span></span>

### <a name="example"></a><span data-ttu-id="109a6-200">示例</span><span class="sxs-lookup"><span data-stu-id="109a6-200">Example</span></span>

<span data-ttu-id="109a6-201">笔记本电脑可保修物料（产品）的基价为 999 美元，有两个笔记本电脑保修项目：</span><span class="sxs-lookup"><span data-stu-id="109a6-201">A laptop warrantable item (product) has a base price $999, and there are two laptop warranty items:</span></span>

- <span data-ttu-id="109a6-202">保修\_1 的下限为 500 美元，上限为 1,000 美元，**价格范围基准**字段设置为**基价**。</span><span class="sxs-lookup"><span data-stu-id="109a6-202">Warranty\_1 has a lower limit of $500 and an upper limit of $1,000, and the **Price range base** field is set to **Base price**.</span></span>
- <span data-ttu-id="109a6-203">保修\_2 的下限为 1,001 美元，上限为 2,000 美元，**价格范围基准**字段设置为**基价**。</span><span class="sxs-lookup"><span data-stu-id="109a6-203">Warranty\_2 has a lower limit of $1,001 and upper limit of $2,000, and the **Price range base** field is set to **Base price**.</span></span>

<span data-ttu-id="109a6-204">在此例中，笔记本电脑可保修物料被添加到客户的购物车后，POS 上将显示添加保修\_1 的提示，因为笔记本电脑的价格在保修\_1 的上限和下限之间。</span><span class="sxs-lookup"><span data-stu-id="109a6-204">In this case, when the laptop warrantable item is added to a customer's cart, a prompt to add Warranty\_1 will be shown at the POS, because the price of the laptop is between the lower and upper limits for Warranty\_1.</span></span>

> [!NOTE]
> <span data-ttu-id="109a6-205">对于此示例，如果您希望保修\_1 和保修\_2 都显示提示，而不考虑可保修物料的价格，请将**价格范围基准**字段设置为**无**。</span><span class="sxs-lookup"><span data-stu-id="109a6-205">For this example, if you want prompts to be shown for both Warranty\_1 and Warranty\_2, regardless of the price of the warrantable item, set the **Price range base** field to **None**.</span></span>

## <a name="configure-channel-specific-settings"></a><span data-ttu-id="109a6-206">配置渠道特定设置</span><span class="sxs-lookup"><span data-stu-id="109a6-206">Configure channel-specific settings</span></span>

<span data-ttu-id="109a6-207">渠道特定设置使您可以指定当可保修物料被添加到客户的购物车时，POS 上是否应显示添加保修项目的提示。</span><span class="sxs-lookup"><span data-stu-id="109a6-207">Channel-specific settings let you specify whether a prompt to add a warranty item should be shown at the POS when a warrantable item is added to a customer's cart.</span></span>

<span data-ttu-id="109a6-208">要在 Commerce 中配置渠道特定设置，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="109a6-208">To configure channel-specific setting in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="109a6-209">转到 **Retail 和 Commerce \> 产品和类别 \> 保修 \> 保修设置**。</span><span class="sxs-lookup"><span data-stu-id="109a6-209">Go to **Retail and Commerce \> Products and categories \> Warranty \> Warranty settings**.</span></span>
1. <span data-ttu-id="109a6-210">在**渠道特定**选项卡上，在您的渠道的**保修提示**栏中，请执行以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="109a6-210">On the **Channel specific** tab, in the **Prompt for warranty** column for your channel, follow one of these steps:</span></span>

    - <span data-ttu-id="109a6-211">当可保修物料被添加到购物车时，如果应在 POS 上显示保修项目的提示，请选中此复选框。</span><span class="sxs-lookup"><span data-stu-id="109a6-211">Select the check box if a prompt for the warranty item should be shown at the POS when the warrantable item is added to the cart.</span></span>
    - <span data-ttu-id="109a6-212">当可保修物料被添加到购物车时，如果不应在 POS 上显示保修项目的提示，请清除此复选框。</span><span class="sxs-lookup"><span data-stu-id="109a6-212">Clear the check box if no prompt for the warranty item should be shown at the POS when the warrantable item is added to the cart.</span></span>

1. <span data-ttu-id="109a6-213">运行 **1070** 作业将数据同步到渠道。</span><span class="sxs-lookup"><span data-stu-id="109a6-213">Run the **1070** job to sync the data to the channel.</span></span>

## <a name="configure-a-number-sequence-for-warranty-policies"></a><span data-ttu-id="109a6-214">配置保修政策的编号规则</span><span class="sxs-lookup"><span data-stu-id="109a6-214">Configure a number sequence for warranty policies</span></span>

<span data-ttu-id="109a6-215">每个保修政策由按编号规则生成的保修政策编号唯一标识。</span><span class="sxs-lookup"><span data-stu-id="109a6-215">Each warranty policy is uniquely identified by a warranty policy number that is generated by a number sequence.</span></span> <span data-ttu-id="109a6-216">有关编号规则的详细信息，请参阅[编号规则概览](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="109a6-216">For more information about number sequences, see [Number sequences overview](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span></span>

<span data-ttu-id="109a6-217">要在 Commerce 中配置保修政策的编号规则，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="109a6-217">To configure a number sequence for warranty policies in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="109a6-218">转到 **Retail 和 Commerce \> 产品和类别 \> 保修 \> 保修设置**。</span><span class="sxs-lookup"><span data-stu-id="109a6-218">Go to **Retail and Commerce \> Products and categories \> Warranty \> Warranty settings**.</span></span>
1. <span data-ttu-id="109a6-219">在**编号规则**选项卡上，在**保修政策**引用一行中，在**编号规则代码**字段中输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="109a6-219">On the **Number sequences** tab, in the row for the **Warranty policy** reference, enter or select a value in the **Number sequence code** field.</span></span>

## <a name="set-up-a-warranty-group"></a><span data-ttu-id="109a6-220">设置保修组</span><span class="sxs-lookup"><span data-stu-id="109a6-220">Set up a warranty group</span></span>

<span data-ttu-id="109a6-221">保修组是保修项目与可保修物料之间的关系。</span><span class="sxs-lookup"><span data-stu-id="109a6-221">A warranty group is a relationship between warranty items and warrantable items.</span></span> <span data-ttu-id="109a6-222">POS 使用保修组来确定当将可保修物料添加到客户的购物车时，应提示销售内勤添加哪些保修项目。</span><span class="sxs-lookup"><span data-stu-id="109a6-222">The POS uses warranty groups to determine which warranty items sales associates should be prompted to add when a warrantable item is added to a customer's cart.</span></span>

<span data-ttu-id="109a6-223">要在 Commerce 中设置保修组，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="109a6-223">To set up a warranty group in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="109a6-224">转到 **Retail 和 Commerce \> 产品和类别 \> 保修 \> 保修组**。</span><span class="sxs-lookup"><span data-stu-id="109a6-224">Go to **Retail and Commerce \> Products and categories \> Warranty \> Warranty groups**.</span></span>
1. <span data-ttu-id="109a6-225">选择**新建**创建保修组。</span><span class="sxs-lookup"><span data-stu-id="109a6-225">Select **New** to create a warranty group.</span></span>
1. <span data-ttu-id="109a6-226">在**名称**字段中，为新组输入名称。</span><span class="sxs-lookup"><span data-stu-id="109a6-226">In the **Name** field, enter a name for the new group.</span></span>
1. <span data-ttu-id="109a6-227">在**常规**快速选项卡上，在**描述**字段中，输入组的描述。</span><span class="sxs-lookup"><span data-stu-id="109a6-227">On the **General** FastTab, in the **Description** field, enter a description of the group.</span></span>
1. <span data-ttu-id="109a6-228">在**保修产品**快速选项卡上，选择**添加行**添加保修项目。</span><span class="sxs-lookup"><span data-stu-id="109a6-228">On the **Warranty products** FastTab, select **Add line** to add a warranty item.</span></span>
1. <span data-ttu-id="109a6-229">在**显示顺序**字段中，输入数字以在 POS 上对保修组进行排名。</span><span class="sxs-lookup"><span data-stu-id="109a6-229">In the **Display order** field, enter a number to rank the warranty group at the POS.</span></span> <span data-ttu-id="109a6-230">POS 将在保修提示中按升序显示保修项目。</span><span class="sxs-lookup"><span data-stu-id="109a6-230">The POS will show warranty items in order of ascending rank in the warranty prompt.</span></span>
1. <span data-ttu-id="109a6-231">在**可保修产品**快速选项卡上，选择**添加行**添加可保修产品。</span><span class="sxs-lookup"><span data-stu-id="109a6-231">On the **Warrantable products** FastTab, select **Add line** to add warrantable products.</span></span>
1. <span data-ttu-id="109a6-232">如果保修项目适用于整个可保修物料（产品）类别，请在**类别**字段中选择该类别。</span><span class="sxs-lookup"><span data-stu-id="109a6-232">If the warranty item is applicable to a whole category of warrantable items (products), select the category in the **Category** field.</span></span> <span data-ttu-id="109a6-233">如果保修项目适用于特定的可保修物料（产品），请在**产品**字段中选择该产品。</span><span class="sxs-lookup"><span data-stu-id="109a6-233">If the warranty item is applicable to a specific warrantable item (product), select the product in the **Product** field.</span></span>
1. <span data-ttu-id="109a6-234">在**适用渠道**快速选项卡上，选择**添加行**添加您要在其中出售保修项目的渠道。</span><span class="sxs-lookup"><span data-stu-id="109a6-234">On the **Applicable channels** FastTab, select **Add line** to add the channel where you want to sell the warranty item.</span></span>
1. <span data-ttu-id="109a6-235">选择**保存**保存配置。</span><span class="sxs-lookup"><span data-stu-id="109a6-235">Select **Save** to save the configuration.</span></span>
1. <span data-ttu-id="109a6-236">选择**发布**发布保修组。</span><span class="sxs-lookup"><span data-stu-id="109a6-236">Select **Publish** to publish the warranty group.</span></span>
1. <span data-ttu-id="109a6-237">运行 **1040** 作业将数据同步到渠道。</span><span class="sxs-lookup"><span data-stu-id="109a6-237">Run the **1040** job to sync the data to channel.</span></span>

## <a name="sell-warranty-items-at-the-pos"></a><span data-ttu-id="109a6-238">在 POS 上出售保修项目</span><span class="sxs-lookup"><span data-stu-id="109a6-238">Sell warranty items at the POS</span></span>

<span data-ttu-id="109a6-239">通过两个 POS 操作，销售内勤可以在客户购买工作流中出售保修项目：</span><span class="sxs-lookup"><span data-stu-id="109a6-239">Two POS operations let sales associates sell warranty items during the workflow for customer purchases:</span></span>

- <span data-ttu-id="109a6-240">**添加保修** – 此操作将触发提示，显示购物车中选定的可保修物料的适用保修。</span><span class="sxs-lookup"><span data-stu-id="109a6-240">**Add warranty** – This operation triggers a prompt that shows applicable warranties for a warrantable item that is selected in the cart.</span></span>
- <span data-ttu-id="109a6-241">**将保修添加到现有交易** – 通过此操作，销售内勤可以出售先前已售出的可保修物料的保修。</span><span class="sxs-lookup"><span data-stu-id="109a6-241">**Add warranty to existing transaction** – This operation lets sales associates sell warranties for warrantable items that were previously sold.</span></span> <span data-ttu-id="109a6-242">销售内勤可以通过输入交易的收据编号来查找可保修物料的原始交易。</span><span class="sxs-lookup"><span data-stu-id="109a6-242">Sales associates can find the original transaction for a warrantable item by entering the receipt number of the transaction.</span></span>

<span data-ttu-id="109a6-243">下图显示了一个 POS 终端页面的示例，页面上显示了为当前购买的可保修物料添加保修项目的提示。</span><span class="sxs-lookup"><span data-stu-id="109a6-243">The following illustration shows an example of a a POS terminal page with a prompt to add a warranty item for the current purchase of a warrantable item.</span></span>

![为当前购买的产品添加保修项目的提示示例](./media/ew-sell-warranty.png)

<span data-ttu-id="109a6-245">下图显示了为先前售出的可保修物料添加保修项目的功能的示例。</span><span class="sxs-lookup"><span data-stu-id="109a6-245">The following illustration shows an example of the feature for adding a warranty item for a warrantable item that was previously sold.</span></span>

![为先前售出的可保修物料添加保修项目的功能的示例](./media/ew-add-warranty-existing.png)

## <a name="process-warranty-transactions"></a><span data-ttu-id="109a6-247">处理保修交易记录</span><span class="sxs-lookup"><span data-stu-id="109a6-247">Process warranty transactions</span></span>

<span data-ttu-id="109a6-248">如果是在现金和结转交易中出售保修，在 Commerce Headquarters 中过账交易后，Commerce 用户可以运行**处理保修交易**作业来处理保修交易并创建保修政策。</span><span class="sxs-lookup"><span data-stu-id="109a6-248">When warranties are sold in cash-and-carry transactions, after the transactions are posted in Commerce headquarters, Commerce users can run the **Process warranty transactions** job to process the warranty transactions and create warranty policies.</span></span>

<span data-ttu-id="109a6-249">要在 Commerce Headquarters 中处理保修交易，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="109a6-249">To process warranty transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="109a6-250">转到 **Retail 和 Commerce \> 产品和类别 \> 保修 \> 处理保修交易**。</span><span class="sxs-lookup"><span data-stu-id="109a6-250">Go to **Retail and Commerce \> Products and categories \> Warranty \> Process warranty transactions**.</span></span>
1. <span data-ttu-id="109a6-251">在**选择组织节点**对话框中，在**组织层次结构**字段中选择一个值。</span><span class="sxs-lookup"><span data-stu-id="109a6-251">In the **Choose organization nodes** dialog box, in the **Organizational hierarchy** field, select a value.</span></span>
1. <span data-ttu-id="109a6-252">在**可用组织节点**列表中，选择单个商店，如果要为一组商店创建批处理作业，则选择一个节点。</span><span class="sxs-lookup"><span data-stu-id="109a6-252">In the **Available organization nodes** list, select either an individual store or, if you want to create the batch job for a group of stores, a node.</span></span>
1. <span data-ttu-id="109a6-253">选择向右箭头按钮，将您的选择添加到**选定组织节点**列表中。</span><span class="sxs-lookup"><span data-stu-id="109a6-253">Select the right arrow button to add your selection to the **Selected organization nodes** list.</span></span>
1. <span data-ttu-id="109a6-254">选择**在后台运行**选项卡。</span><span class="sxs-lookup"><span data-stu-id="109a6-254">Select the **Run in the background** tab.</span></span>
1. <span data-ttu-id="109a6-255">将**批处理**选项设置为**是**，然后选择**重复执行**。</span><span class="sxs-lookup"><span data-stu-id="109a6-255">Set the **Batch processing** option to **Yes**, and then select **Recurrence**.</span></span>
1. <span data-ttu-id="109a6-256">在**定义重复执行**对话框的**开始日期**字段中，选择或输入重复执行的开始日期。</span><span class="sxs-lookup"><span data-stu-id="109a6-256">In the **Define recurrence** dialog box, in the **Start date** field, select or enter a start date for the recurrence.</span></span>
1. <span data-ttu-id="109a6-257">在**开始时间**字段中，选择或输入重复执行的开始时间。</span><span class="sxs-lookup"><span data-stu-id="109a6-257">In the **Start time** field, select or enter a start time for the recurrence.</span></span>
1. <span data-ttu-id="109a6-258">按以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="109a6-258">Follow one of these steps:</span></span>

    - <span data-ttu-id="109a6-259">如果重复执行应该永远不结束，请选择**无结束日期**选项。</span><span class="sxs-lookup"><span data-stu-id="109a6-259">Select the **No end date** option if the recurrence should never end.</span></span>
    - <span data-ttu-id="109a6-260">如果重复执行应在特定运行次数后结束，请选择**之后结束**选项。</span><span class="sxs-lookup"><span data-stu-id="109a6-260">Select the **End after** option if the recurrence should end after a specific number of runs.</span></span> <span data-ttu-id="109a6-261">如果选择此选项，请输入运行次数。</span><span class="sxs-lookup"><span data-stu-id="109a6-261">If you select this option, enter the number of runs.</span></span>
    - <span data-ttu-id="109a6-262">如果重复执行应在特定日期之前结束，请选择**结束日期**选项。</span><span class="sxs-lookup"><span data-stu-id="109a6-262">Select the **End by** option if the recurrence should end by a specific date.</span></span> <span data-ttu-id="109a6-263">如果选择此选项，请选择或输入日期。</span><span class="sxs-lookup"><span data-stu-id="109a6-263">If you select this option, select or enter the date.</span></span>

1. <span data-ttu-id="109a6-264">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="109a6-264">Select **OK**.</span></span>
1. <span data-ttu-id="109a6-265">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="109a6-265">Select **OK**.</span></span>

## <a name="warranty-policies"></a><span data-ttu-id="109a6-266">保修政策</span><span class="sxs-lookup"><span data-stu-id="109a6-266">Warranty policies</span></span>

<span data-ttu-id="109a6-267">出售延长保修时，将自动创建保修政策实体。</span><span class="sxs-lookup"><span data-stu-id="109a6-267">When an extended warranty is sold, a warranty policy entity is automatically created.</span></span> <span data-ttu-id="109a6-268">保修政策编号可以与客户共享，让他们作为所购买保修项目的引用信息。</span><span class="sxs-lookup"><span data-stu-id="109a6-268">Warranty policy numbers can be shared with customers, so that they have a reference for the warranty item that they purchased.</span></span> <span data-ttu-id="109a6-269">保修政策的属性包括保修的有效开始日期和到期日期、条款和条件以及出售保修的可保修物料的序列号。</span><span class="sxs-lookup"><span data-stu-id="109a6-269">The properties of warranty policies include the effective start date and expiration date of the warranty, terms and conditions, and the serial number of the warrantable item that the warranty was sold for.</span></span>

> [!NOTE]
> <span data-ttu-id="109a6-270">创建保修政策实体时，会自动生成保修政策属性。</span><span class="sxs-lookup"><span data-stu-id="109a6-270">Warranty policy properties are automatically generated when warranty policy entities are created.</span></span> <span data-ttu-id="109a6-271">当前，它们不能手动配置或编辑。</span><span class="sxs-lookup"><span data-stu-id="109a6-271">Currently, they can't be manually configured or edited.</span></span>

<span data-ttu-id="109a6-272">下表描述了保修政策属性及其值。</span><span class="sxs-lookup"><span data-stu-id="109a6-272">The following table describes the warranty policy properties and their values.</span></span> <span data-ttu-id="109a6-273">在 Commerce headquarters 中，数据库表名为 WARRANTYPOLICY。</span><span class="sxs-lookup"><span data-stu-id="109a6-273">In Commerce headquarters, the database table is named WARRANTYPOLICY.</span></span>

| <span data-ttu-id="109a6-274">属性名称</span><span class="sxs-lookup"><span data-stu-id="109a6-274">Property name</span></span> | <span data-ttu-id="109a6-275">值</span><span class="sxs-lookup"><span data-stu-id="109a6-275">Value</span></span> | <span data-ttu-id="109a6-276">说明</span><span class="sxs-lookup"><span data-stu-id="109a6-276">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="109a6-277">PolicyNumber</span><span class="sxs-lookup"><span data-stu-id="109a6-277">PolicyNumber</span></span> | <span data-ttu-id="109a6-278">一个字符串（最多 20 个字符）</span><span class="sxs-lookup"><span data-stu-id="109a6-278">A character string (maximum of 20 characters)</span></span> | <span data-ttu-id="109a6-279">保修政策编号</span><span class="sxs-lookup"><span data-stu-id="109a6-279">The warranty policy number</span></span> |
| <span data-ttu-id="109a6-280">WarrantiedItemId</span><span class="sxs-lookup"><span data-stu-id="109a6-280">WarrantiedItemId</span></span> | <span data-ttu-id="109a6-281">一个字符串（最多 20 个字符）</span><span class="sxs-lookup"><span data-stu-id="109a6-281">A character string (maximum of 20 characters)</span></span> | <span data-ttu-id="109a6-282">可保修物料的 ID</span><span class="sxs-lookup"><span data-stu-id="109a6-282">The ID of the warrantable item</span></span> |
| <span data-ttu-id="109a6-283">WarrantiedInventoryLotId</span><span class="sxs-lookup"><span data-stu-id="109a6-283">WarrantiedInventoryLotId</span></span> | <span data-ttu-id="109a6-284">一个字符串（最多 20 个字符）</span><span class="sxs-lookup"><span data-stu-id="109a6-284">A character string (maximum of 20 characters)</span></span> | <span data-ttu-id="109a6-285">可保修物料的库存批次 ID</span><span class="sxs-lookup"><span data-stu-id="109a6-285">The inventory lot ID of the warrantable item</span></span> |
| <span data-ttu-id="109a6-286">WarrantiedSerialNumber</span><span class="sxs-lookup"><span data-stu-id="109a6-286">WarrantiedSerialNumber</span></span> | <span data-ttu-id="109a6-287">一个字符串（最多 20 个字符）</span><span class="sxs-lookup"><span data-stu-id="109a6-287">A character string (maximum of 20 characters)</span></span> | <span data-ttu-id="109a6-288">可保修物料的序列号</span><span class="sxs-lookup"><span data-stu-id="109a6-288">The serial number of the warrantable item</span></span> |
| <span data-ttu-id="109a6-289">WarrantiedFulfilledDate</span><span class="sxs-lookup"><span data-stu-id="109a6-289">WarrantiedFulfilledDate</span></span> | <span data-ttu-id="109a6-290">一个日期</span><span class="sxs-lookup"><span data-stu-id="109a6-290">A date</span></span> | <span data-ttu-id="109a6-291">可保修物料的履行日期</span><span class="sxs-lookup"><span data-stu-id="109a6-291">The fulfillment date of the warrantable item</span></span> |
| <span data-ttu-id="109a6-292">WarrantyItemId</span><span class="sxs-lookup"><span data-stu-id="109a6-292">WarrantyItemId</span></span> | <span data-ttu-id="109a6-293">一个字符串（最多 20 个字符）</span><span class="sxs-lookup"><span data-stu-id="109a6-293">A character string (maximum of 20 characters)</span></span> | <span data-ttu-id="109a6-294">保修项目的 ID</span><span class="sxs-lookup"><span data-stu-id="109a6-294">The ID of the warranty item</span></span> |
| <span data-ttu-id="109a6-295">WarrantyInventoryLotId</span><span class="sxs-lookup"><span data-stu-id="109a6-295">WarrantyInventoryLotId</span></span> | <span data-ttu-id="109a6-296">一个字符串（最多 20 个字符）</span><span class="sxs-lookup"><span data-stu-id="109a6-296">A character string (maximum of 20 characters)</span></span> | <span data-ttu-id="109a6-297">保修项目的库存批次 ID</span><span class="sxs-lookup"><span data-stu-id="109a6-297">The inventory lot ID of the warranty item</span></span> |
| <span data-ttu-id="109a6-298">WarrantySalesDate</span><span class="sxs-lookup"><span data-stu-id="109a6-298">WarrantySalesDate</span></span> | <span data-ttu-id="109a6-299">一个日期</span><span class="sxs-lookup"><span data-stu-id="109a6-299">A date</span></span> | <span data-ttu-id="109a6-300">保修项目的销售日期</span><span class="sxs-lookup"><span data-stu-id="109a6-300">The sale date of the warranty item</span></span> |
| <span data-ttu-id="109a6-301">WarrantyEffectiveDate</span><span class="sxs-lookup"><span data-stu-id="109a6-301">WarrantyEffectiveDate</span></span> | <span data-ttu-id="109a6-302">一个日期</span><span class="sxs-lookup"><span data-stu-id="109a6-302">A date</span></span> | <span data-ttu-id="109a6-303">保修政策的生效日期</span><span class="sxs-lookup"><span data-stu-id="109a6-303">The effective date of the warranty policy</span></span> |
| <span data-ttu-id="109a6-304">WarrantyExpirationDate</span><span class="sxs-lookup"><span data-stu-id="109a6-304">WarrantyExpirationDate</span></span> | <span data-ttu-id="109a6-305">一个日期</span><span class="sxs-lookup"><span data-stu-id="109a6-305">A date</span></span> | <span data-ttu-id="109a6-306">保修政策的到期日期</span><span class="sxs-lookup"><span data-stu-id="109a6-306">The expiration date of the warranty policy</span></span> |
| <span data-ttu-id="109a6-307">CustAccount</span><span class="sxs-lookup"><span data-stu-id="109a6-307">CustAccount</span></span> | <span data-ttu-id="109a6-308">一个字符串（最多 20 个字符）</span><span class="sxs-lookup"><span data-stu-id="109a6-308">A character string (maximum of 20 characters)</span></span> | <span data-ttu-id="109a6-309">客户帐号</span><span class="sxs-lookup"><span data-stu-id="109a6-309">The customer account number</span></span> |
| <span data-ttu-id="109a6-310">状态</span><span class="sxs-lookup"><span data-stu-id="109a6-310">Status</span></span> | <span data-ttu-id="109a6-311">**已创建**、**已失效**、**已生效**或**已过期**</span><span class="sxs-lookup"><span data-stu-id="109a6-311">**Created**, **Voided**, **Effective**, or **Expired**</span></span> | <span data-ttu-id="109a6-312">保修政策的状态</span><span class="sxs-lookup"><span data-stu-id="109a6-312">The status of the warranty policy</span></span> |
| <span data-ttu-id="109a6-313">说明</span><span class="sxs-lookup"><span data-stu-id="109a6-313">Notes</span></span> | <span data-ttu-id="109a6-314">一个字符串（最多 255 个字符）</span><span class="sxs-lookup"><span data-stu-id="109a6-314">A character string (a maximum of 255 characters)</span></span> | <span data-ttu-id="109a6-315">有关保修政策的注意事项，如条款和条件</span><span class="sxs-lookup"><span data-stu-id="109a6-315">Notes about the warranty policy, such as terms and conditions</span></span> |

## <a name="frequently-asked-questions-faq"></a><span data-ttu-id="109a6-316">常见问题 (FAQ)</span><span class="sxs-lookup"><span data-stu-id="109a6-316">Frequently asked questions (FAQ)</span></span>

<span data-ttu-id="109a6-317">**为什么我在 POS 中看不到保修提示？**</span><span class="sxs-lookup"><span data-stu-id="109a6-317">**Why don't I see a warranty prompt in the POS?**</span></span>

<span data-ttu-id="109a6-318">请确保将保修项目分类到渠道中。</span><span class="sxs-lookup"><span data-stu-id="109a6-318">Make sure that the warranty item is assorted to the channel.</span></span> <span data-ttu-id="109a6-319">另外还要确保配置了保修组，使其包括相关渠道。</span><span class="sxs-lookup"><span data-stu-id="109a6-319">Also make sure that the warranty group is configured so that it includes the relevant channel.</span></span>

<span data-ttu-id="109a6-320">**当我尝试向现有交易添加保修并输入客户订单收据编号时，为什么看不到任何交易记录行项？**</span><span class="sxs-lookup"><span data-stu-id="109a6-320">**When I try to add a warranty to an existing transaction and enter the customer order receipt number, why don't I see any transaction line items?**</span></span>

<span data-ttu-id="109a6-321">仅当运行拉入作业（P 作业）将收据上载到 Commerce headquarters 时，才能找到收据。</span><span class="sxs-lookup"><span data-stu-id="109a6-321">Receipts can be found only if a pull job (P-job) is run to upload the receipts to Commerce headquarters.</span></span> <span data-ttu-id="109a6-322">要运行 P 作业，请转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 配送计划**，选择 **P-0001** 作业，然后选择**立即运行**。</span><span class="sxs-lookup"><span data-stu-id="109a6-322">To run the P-job, go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**, select the **P-0001** job, and then select **Run now**.</span></span>

<span data-ttu-id="109a6-323">**为什么保修功能仅适用于序列化产品？**</span><span class="sxs-lookup"><span data-stu-id="109a6-323">**Why is the warranty feature applicable only to serialized products?**</span></span>

<span data-ttu-id="109a6-324">保修是为特定的唯一产品提供的服务。</span><span class="sxs-lookup"><span data-stu-id="109a6-324">A warranty is a service that is provided for a specific, unique product.</span></span> <span data-ttu-id="109a6-325">在 Dynamics 365 中，产品只能通过序列号唯一标识。</span><span class="sxs-lookup"><span data-stu-id="109a6-325">In Dynamics 365, a product can be uniquely identified only by a serial number.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="109a6-326">其他资源</span><span class="sxs-lookup"><span data-stu-id="109a6-326">Additional resources</span></span>

[<span data-ttu-id="109a6-327">设置零售产品</span><span class="sxs-lookup"><span data-stu-id="109a6-327">Set up retail products</span></span>](set-up-retail-products.md)

[<span data-ttu-id="109a6-328">设置分类</span><span class="sxs-lookup"><span data-stu-id="109a6-328">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="109a6-329">编号规则概览</span><span class="sxs-lookup"><span data-stu-id="109a6-329">Number sequences overview</span></span>](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)
