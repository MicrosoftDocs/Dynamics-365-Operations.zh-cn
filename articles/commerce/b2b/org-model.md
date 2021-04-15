---
title: 为 B2B 组织创建组织建模层次结构
description: 本主题介绍如何为企业到企业 (B2B) 组织创建组织建模层次结构。
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 487af939f92ece8bc3e543b3beeffa239baa1863
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799821"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a><span data-ttu-id="9497b-103">为 B2B 组织创建组织建模层次结构</span><span class="sxs-lookup"><span data-stu-id="9497b-103">Create org modeling hierarchies for B2B organizations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9497b-104">本主题介绍如何在 Microsoft Dynamics 365 Commerce 中为企业到企业 (B2B) 组织创建组织建模层次结构。</span><span class="sxs-lookup"><span data-stu-id="9497b-104">This topic describes how to create organizational modeling hierarchies for business-to-business (B2B) organizations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="9497b-105">在 Commerce headquarters 中，业务合作伙伴组织由客户和客户层次结构实体表示。</span><span class="sxs-lookup"><span data-stu-id="9497b-105">In Commerce headquarters, business partner organizations are represented by customer and customer hierarchy entities.</span></span> <span data-ttu-id="9497b-106">业务合作伙伴组织及其用户表示为客户，客户层次结构用于将这些客户彼此关联。</span><span class="sxs-lookup"><span data-stu-id="9497b-106">The business partner organization and its users are represented as customers, and customer hierarchies are used to associate those customers with each other.</span></span>

<span data-ttu-id="9497b-107">批准加入 B2B 电子商务站点的业务合作伙伴请求后，将执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="9497b-107">When a business partner request to join a B2B e-commerce site is approved, the following actions are performed:</span></span>

- <span data-ttu-id="9497b-108">在系统中创建两个新的客户记录：业务合作伙伴组织的 **组织类型** 客户记录和请求者（即提交请求的业务合作伙伴用户）的 **个人类型** 客户记录。</span><span class="sxs-lookup"><span data-stu-id="9497b-108">Two new customer records are created in the system: a **Type Organization** customer record for the business partner organization and a **Type Person** customer record for the requestor (that is, the business partner user who submitted the request).</span></span>
- <span data-ttu-id="9497b-109">在 **客户 \> 客户层次结构** 下创建新的客户层次结构记录。</span><span class="sxs-lookup"><span data-stu-id="9497b-109">A new customer hierarchy record is created under **Customer \> Customer hierarchy**.</span></span> <span data-ttu-id="9497b-110">此记录具有以下标头属性：</span><span class="sxs-lookup"><span data-stu-id="9497b-110">This record has the following header properties:</span></span>

    - <span data-ttu-id="9497b-111">**客户层次结构 ID** – 客户层次结构的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="9497b-111">**Customer hierarchy ID** – A unique ID for the customer hierarchy.</span></span> <span data-ttu-id="9497b-112">此 ID 使用在 Commerce headquarters 中的 Commerce 共享参数中定义的编号规则。</span><span class="sxs-lookup"><span data-stu-id="9497b-112">This ID uses the number sequence that is defined in Commerce shared parameters in Commerce headquarters.</span></span>
    - <span data-ttu-id="9497b-113">**名称** – 加入请求中指定的业务合作伙伴的组织名称。</span><span class="sxs-lookup"><span data-stu-id="9497b-113">**Name** – The organization name of the business partner, as specified in the onboarding request.</span></span>
    - <span data-ttu-id="9497b-114">**目的** – 此属性设置为预定义值 **B2B 组织**。</span><span class="sxs-lookup"><span data-stu-id="9497b-114">**Purpose** – This property is set to the predefined value **B2B organization**.</span></span>
    - <span data-ttu-id="9497b-115">**组织** – 业务合作伙伴的客户 ID。</span><span class="sxs-lookup"><span data-stu-id="9497b-115">**Organization** – The customer ID of the business partner.</span></span>

<span data-ttu-id="9497b-116">以下是客户层次结构记录的详细信息：</span><span class="sxs-lookup"><span data-stu-id="9497b-116">Here are the details of the customer hierarchy record:</span></span>

- <span data-ttu-id="9497b-117">请求者的客户记录与客户层次结构相关联。</span><span class="sxs-lookup"><span data-stu-id="9497b-117">The customer record of the requestor is associated with the customer hierarchy.</span></span>
- <span data-ttu-id="9497b-118">管理员角色与请求者关联。</span><span class="sxs-lookup"><span data-stu-id="9497b-118">The administrator role is associated with the requestor.</span></span>

<span data-ttu-id="9497b-119">当管理员将更多用户添加到 B2B 站点上的业务合作伙伴组织时，将在 Commerce headquarters 中为每个用户创建新的客户记录。</span><span class="sxs-lookup"><span data-stu-id="9497b-119">When the administrator adds more users are to the business partner organization on a B2B site, a new customer record for each user is created in Commerce headquarters.</span></span> <span data-ttu-id="9497b-120">此客户记录也将被添加到业务合作伙伴的相关客户层次结构记录中，具有“用户”的角色。</span><span class="sxs-lookup"><span data-stu-id="9497b-120">This customer record is also added to the relevant customer hierarchy record for the business partner and has the role of a "user."</span></span>

> [!NOTE]
> <span data-ttu-id="9497b-121">在大多数情况下，层次结构中所有客户记录的相应属性值应是匹配的。</span><span class="sxs-lookup"><span data-stu-id="9497b-121">In most cases, the corresponding property values of all customer records in a hierarchy should match.</span></span> <span data-ttu-id="9497b-122">例如，由于所有业务合作伙伴用户都应该获得相似的产品价格，因此他们的价格组和关联的配置应该是匹配的。</span><span class="sxs-lookup"><span data-stu-id="9497b-122">For example, because all business partner users should get similar prices for products, their price group and associated configurations should match.</span></span> <span data-ttu-id="9497b-123">但是，系统不强制要求此一致性。</span><span class="sxs-lookup"><span data-stu-id="9497b-123">However, the system doesn't enforce this consistency.</span></span> <span data-ttu-id="9497b-124">因此，相关的 Commerce headquarters 用户负责确保属性值和配置与给定层次结构中的所有客户匹配。</span><span class="sxs-lookup"><span data-stu-id="9497b-124">Therefore, the relevant Commerce headquarters users are responsible for ensuring that the property values and configurations match for all customers in a given hierarchy.</span></span>

<span data-ttu-id="9497b-125">Commerce headquarters 用户可以并排查看层次结构中所有客户记录的属性值。</span><span class="sxs-lookup"><span data-stu-id="9497b-125">Commerce headquarters users can look at the property values for all customer records in the hierarchy in a side-by-side view.</span></span> <span data-ttu-id="9497b-126">通过选择下拉菜单上中选项卡名称，选择相关的客户记录属性。</span><span class="sxs-lookup"><span data-stu-id="9497b-126">Select the relevant customer record properties by selecting the tab names on the drop-down menu.</span></span> <span data-ttu-id="9497b-127">用户可以从此视图直接查看和编辑属性值。</span><span class="sxs-lookup"><span data-stu-id="9497b-127">Users can directly view and edit the property values from this view.</span></span> <span data-ttu-id="9497b-128">或者，如果您要将管理员客户记录中的所有值应用于所有用户客户记录，选择客户层次结构详细信息中的 **替代**。</span><span class="sxs-lookup"><span data-stu-id="9497b-128">Alternatively, if you want to apply all the values from the administrator customer record to all the user customer records, select **Override** in the customer hierarchy details.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9497b-129">其他资源</span><span class="sxs-lookup"><span data-stu-id="9497b-129">Additional resources</span></span>

[<span data-ttu-id="9497b-130">建立 B2B 电子商务站点</span><span class="sxs-lookup"><span data-stu-id="9497b-130">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="9497b-131">在 B2B 电子商务站点上管理业务合作伙伴用户</span><span class="sxs-lookup"><span data-stu-id="9497b-131">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="9497b-132">配置 B2B 电子商务站点的客户帐户付款方式</span><span class="sxs-lookup"><span data-stu-id="9497b-132">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)

[<span data-ttu-id="9497b-133">设置 B2B 电子商务站点的产品数量限制</span><span class="sxs-lookup"><span data-stu-id="9497b-133">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]