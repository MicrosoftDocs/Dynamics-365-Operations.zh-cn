---
title: Common Data Service 中的公司概念
description: 本主题介绍 Finance and Operations 与 Common Data Service 之间的公司数据集成。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 444bfc1698a206ca34e67f742df63431a3b02649
ms.sourcegitcommit: 7da8811f1a7db858efb76edb0bdf857a47d07600
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/27/2020
ms.locfileid: "3728405"
---
# <a name="company-concept-in-common-data-service"></a><span data-ttu-id="79daf-103">Common Data Service 中的公司概念</span><span class="sxs-lookup"><span data-stu-id="79daf-103">Company concept in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="79daf-104">在 Finance and Operations 中，*公司*的概念既是法律构造，又是业务构造。</span><span class="sxs-lookup"><span data-stu-id="79daf-104">In Finance and Operations, the concept of a *company* is both a legal construct and a business construct.</span></span> <span data-ttu-id="79daf-105">还是数据的安全和可见性界限。</span><span class="sxs-lookup"><span data-stu-id="79daf-105">It's also a security and visibility boundary for data.</span></span> <span data-ttu-id="79daf-106">用户始终在单个公司的上下文中工作，并且大多数数据已剥离了公司的性质。</span><span class="sxs-lookup"><span data-stu-id="79daf-106">Users always work in the context of a single company, and most of the data is striped by company.</span></span>

<span data-ttu-id="79daf-107">Common Data Service 没有同等概念。</span><span class="sxs-lookup"><span data-stu-id="79daf-107">Common Data Service doesn't have an equivalent concept.</span></span> <span data-ttu-id="79daf-108">最接近的概念是*业务单位*，这主要是用户数据的安全和可见性界限。</span><span class="sxs-lookup"><span data-stu-id="79daf-108">The closest concept is *business unit*, which is primarily a security and visibility boundary for user data.</span></span> <span data-ttu-id="79daf-109">此概念没有公司概念具有的同样法律或业务含义。</span><span class="sxs-lookup"><span data-stu-id="79daf-109">This concept doesn't have the same legal or business implications as the company concept.</span></span>

<span data-ttu-id="79daf-110">因为业务单位和公司不是同等概念，所以不能为了 Common Data Service 集成而在两者之间强制执行一对一 (1:1) 的映射。</span><span class="sxs-lookup"><span data-stu-id="79daf-110">Because business unit and company aren't equivalent concepts, it isn't possible to force a one-to-one (1:1) mapping between them for the purpose of Common Data Service integration.</span></span> <span data-ttu-id="79daf-111">但是，因为默认情况下用户必须可以在应用程序和 Common Data Service 中查看相同的记录，所以 Microsoft 在 Common Data Service 中引入了一个新实体，名称为 cdm\_Company。</span><span class="sxs-lookup"><span data-stu-id="79daf-111">However, because users must, by default, be able to see the same records in the application and Common Data Service, Microsoft has introduced a new entity in Common Data Service that is named cdm\_Company.</span></span> <span data-ttu-id="79daf-112">这个实体与应用程序中的公司实体等同。</span><span class="sxs-lookup"><span data-stu-id="79daf-112">This entity is equivalent to the Company entity in the application.</span></span> <span data-ttu-id="79daf-113">为了帮助确保应用程序与 Common Data Service 之间记录的原始可见性等同，所以我们建议在 Common Data Service 中对数据进行以下设置：</span><span class="sxs-lookup"><span data-stu-id="79daf-113">To help guarantee that visibility of records is equivalent between the application and Common Data Service out of the box, we recommend the following setup for data in Common Data Service:</span></span>

+ <span data-ttu-id="79daf-114">为启用了双写入的每个 Finance and Operations Company 记录创建一个关联的 cdm\_Company 记录。</span><span class="sxs-lookup"><span data-stu-id="79daf-114">For each Finance and Operations Company record that is enabled for dual-write, an associated cdm\_Company record is created.</span></span>
+ <span data-ttu-id="79daf-115">创建一个 cdm\_Company 记录并为其启用双写入时，将创建一个同名的默认业务单位。</span><span class="sxs-lookup"><span data-stu-id="79daf-115">When a cdm\_Company record is created and enabled for dual-write, a default business unit is created that has the same name.</span></span> <span data-ttu-id="79daf-116">尽管会为这个业务单位自动创建一个默认团队，但是不会使用该业务单位。</span><span class="sxs-lookup"><span data-stu-id="79daf-116">Although a default team is automatically created for that business unit, the business unit isn't used.</span></span>
+ <span data-ttu-id="79daf-117">将单独创建一个同名的负责团队。</span><span class="sxs-lookup"><span data-stu-id="79daf-117">A separate owner team is created that has the same name.</span></span> <span data-ttu-id="79daf-118">还会将其与该业务单位关联。</span><span class="sxs-lookup"><span data-stu-id="79daf-118">It's also associated with the business unit.</span></span>
+ <span data-ttu-id="79daf-119">默认情况下，创建的并双写入 Common Data Service 的所有记录的负责人都将设置为与关联业务单位链接的“DW 负责人”团队。</span><span class="sxs-lookup"><span data-stu-id="79daf-119">By default, the owner of any record that is created and dual-written to Common Data Service is set to the "DW Owner" team that is linked to the associated business unit.</span></span>

<span data-ttu-id="79daf-120">下图显示 Common Data Service 中这种数据设置的示例。</span><span class="sxs-lookup"><span data-stu-id="79daf-120">The following illustration shows an example of this data setup in Common Data Service.</span></span>

![Common Data Service 中的数据设置](media/dual-write-company-1.png)

<span data-ttu-id="79daf-122">因为此配置，所以与 USMF 公司有关的所有记录都将由与 Common Data Service 中的 USMF 业务单位链接的团队负责。</span><span class="sxs-lookup"><span data-stu-id="79daf-122">Because of this configuration, any record that is related to the USMF company will be owned by a team that is linked to the USMF business unit in Common Data Service.</span></span> <span data-ttu-id="79daf-123">因此，所有可以通过设置为业务单位级可见性的安全角色访问该业务单位的用户现在都可以查看这些记录。</span><span class="sxs-lookup"><span data-stu-id="79daf-123">Therefore, any user who has access to that business unit through a security role that is set to business unit–level visibility can now see those records.</span></span> <span data-ttu-id="79daf-124">以下示例显示如何使用团队正确访问这些记录。</span><span class="sxs-lookup"><span data-stu-id="79daf-124">The following example shows how teams can be used to provide the correct access to those records.</span></span>

+ <span data-ttu-id="79daf-125">将为“USMF 销售”团队的成员分配“销售经理”角色。</span><span class="sxs-lookup"><span data-stu-id="79daf-125">The "Sales Manager" role is assigned to members of the "USMF Sales" team.</span></span>
+ <span data-ttu-id="79daf-126">具有“销售经理”角色的用户可以访问担任所属同一个业务单位的成员的所有帐户记录。</span><span class="sxs-lookup"><span data-stu-id="79daf-126">Users who have the "Sales Manager" role can access any account records that are members of the same business unit that they are members of.</span></span>
+ <span data-ttu-id="79daf-127">“USMF 销售”团队已链接至前面介绍的 USMF 业务单位。</span><span class="sxs-lookup"><span data-stu-id="79daf-127">The "USMF Sales" team is linked to the USMF business unit that was mentioned earlier.</span></span>
+ <span data-ttu-id="79daf-128">因此，“USMF 销售”团队的成员可以查看“USMF DW”用户负责的所有客户，这些客户来自 Finance and Operations 中的 USMF 公司实体。</span><span class="sxs-lookup"><span data-stu-id="79daf-128">Therefore, members of the "USMF Sales" team can see any account that is owned by the "USMF DW" user, which would have come from the USMF Company entity in Finance and Operations.</span></span>

![如何使用团队](media/dual-write-company-2.png)

<span data-ttu-id="79daf-130">上图显示，业务单位、公司和团队之间的这种 1:1 映射还只是开始。</span><span class="sxs-lookup"><span data-stu-id="79daf-130">As the preceding illustration shows, this 1:1 mapping between business unit, company, and team is just a starting point.</span></span> <span data-ttu-id="79daf-131">在此示例中，在 Common Data Service 中手动新建了“欧洲”业务单位，同时充当 DEMF 和 ESMF 的父级。</span><span class="sxs-lookup"><span data-stu-id="79daf-131">In this example, a new "Europe" business unit is manually created in Common Data Service as the parent for both DEMF and ESMF.</span></span> <span data-ttu-id="79daf-132">这个新的根业务单位未与双写入关联。</span><span class="sxs-lookup"><span data-stu-id="79daf-132">This new root business unit is unrelated to dual-write.</span></span> <span data-ttu-id="79daf-133">但是，可用于为“EUR 销售”团队的成员提供 DEMF 和 ESMF 中的客户数据的访问权限，方法是在关联的安全角色中将数据可用性设置为**父级/子级 BU**。</span><span class="sxs-lookup"><span data-stu-id="79daf-133">However, it can be used to give members of the "EUR Sales" team access to account data in both DEMF and ESMF by setting the data visibility to **Parent/Child BU** in the associated security role.</span></span>

<span data-ttu-id="79daf-134">最后要介绍的是双写入如何确定应该将记录分配给哪个负责团队。</span><span class="sxs-lookup"><span data-stu-id="79daf-134">A final topic to discuss is how dual-write determines which owner team it should assign records to.</span></span> <span data-ttu-id="79daf-135">此行为由 cdm\_Company 记录中的**默认负责团队**控制。</span><span class="sxs-lookup"><span data-stu-id="79daf-135">This behavior is controlled by the **Default owning team** field on the cdm\_Company record.</span></span> <span data-ttu-id="79daf-136">如果为 cdm\_Company 记录启用双写入，一个插件将自动创建关联的业务单位和负责团队（如果还没有），并设置**默认负责团队**字段。</span><span class="sxs-lookup"><span data-stu-id="79daf-136">When a cdm\_Company record is enabled for dual-write, a plug-in automatically creates the associated business unit and owner team (if it doesn't already exist), and sets the **Default owning team** field.</span></span> <span data-ttu-id="79daf-137">管理员可以将此字段更改为其他值。</span><span class="sxs-lookup"><span data-stu-id="79daf-137">The admin can change this field to a different value.</span></span> <span data-ttu-id="79daf-138">但是，只要为该实体启用了双写入，管理员就不能清除该字段。</span><span class="sxs-lookup"><span data-stu-id="79daf-138">However, the admin can't clear the field as long as the entity is enabled for dual-write.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="79daf-139">![默认负责团队字段](media/dual-write-default-owning-team.jpg)</span><span class="sxs-lookup"><span data-stu-id="79daf-139">![Default owning team field](media/dual-write-default-owning-team.jpg)</span></span>

## <a name="company-striping-and-bootstrapping"></a><span data-ttu-id="79daf-140">公司剥离和自扩展</span><span class="sxs-lookup"><span data-stu-id="79daf-140">Company striping and bootstrapping</span></span>

<span data-ttu-id="79daf-141">Common Data Service 集成通过使用公司标识符剥离数据来为公司提供奇偶校验。</span><span class="sxs-lookup"><span data-stu-id="79daf-141">Common Data Service integration brings company parity by using a company identifier to stripe data.</span></span> <span data-ttu-id="79daf-142">如下图所示，已扩展了特定于公司的所有实体，以使其与 cdm\_Company 实体之间存在多对一 (N:1) 关系。</span><span class="sxs-lookup"><span data-stu-id="79daf-142">As the following illustration shows, all company-specific entities are extended so that they have a many-to-one (N:1) relationship with the cdm\_Company entity.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="79daf-143">![特定于公司的实体与 cdm_Company 实体之间的 N:1 关系](media/dual-write-bootstrapping.png)</span><span class="sxs-lookup"><span data-stu-id="79daf-143">![N:1 relationship between a company-specific entity and the cdm_Company entity](media/dual-write-bootstrapping.png)</span></span>

+ <span data-ttu-id="79daf-144">对于记录，添加并保存公司之后，该值变为只读。</span><span class="sxs-lookup"><span data-stu-id="79daf-144">For records, after a company is added and saved, the value becomes read-only.</span></span> <span data-ttu-id="79daf-145">因此，用户应确保选择正确的公司。</span><span class="sxs-lookup"><span data-stu-id="79daf-145">Therefore, users should make sure that they select the correct company.</span></span>
+ <span data-ttu-id="79daf-146">只有包含公司数据的记录才符合应用程序与 Common Data Service 之间的双写入的资格。</span><span class="sxs-lookup"><span data-stu-id="79daf-146">Only records that have company data are eligible for dual-write between the application and Common Data Service.</span></span>
+ <span data-ttu-id="79daf-147">对于现有 Common Data Service 数据，很快将提供管理员引导的自扩展体验。</span><span class="sxs-lookup"><span data-stu-id="79daf-147">For existing Common Data Service data, an admin-led bootstrapping experience will soon be available.</span></span>


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a><span data-ttu-id="79daf-148">在 Customer Engagement 应用中自动填充公司名称</span><span class="sxs-lookup"><span data-stu-id="79daf-148">Autopopulate company name in customer engagement apps</span></span>

<span data-ttu-id="79daf-149">有几种方法可以在 Customer Engagement 应用中自动填充公司名称。</span><span class="sxs-lookup"><span data-stu-id="79daf-149">There are several ways to auto-populate the company name in customer engagement apps.</span></span>

+ <span data-ttu-id="79daf-150">如果您是系统管理员，可以通过导航到**高级设置 > 系统 > 安全性 > 用户**来设置默认公司。</span><span class="sxs-lookup"><span data-stu-id="79daf-150">If you are a system administrator, you can set the default company by navigating to **Advanced Settings > System > Security > Users**.</span></span> <span data-ttu-id="79daf-151">打开**用户**窗体，然后在**组织信息**部分，设置**窗体中的默认公司**值。</span><span class="sxs-lookup"><span data-stu-id="79daf-151">Open the **User** form, and in the **Organization Information** section, set the **Company to default on Forms** value.</span></span>

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="在“组织信息”部分设置默认公司。":::

+ <span data-ttu-id="79daf-153">如果您对**业务单位**级别的 **SystemUser** 实体具有**写入**访问权限，可以通过从**公司**下拉菜单中选择公司来更改任何一个窗体上的默认公司。</span><span class="sxs-lookup"><span data-stu-id="79daf-153">If you have **Write** access to the **SystemUser** entity for the **Business Unit** level, then you can change the default company on any form by selecting a company from the **Company** drop-down menu.</span></span>

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="更改新客户中的公司名称。":::

+ <span data-ttu-id="79daf-155">如果您对多个公司中的数据具有**写入**访问权限，可以通过选择属于不同公司的记录来更改默认公司。</span><span class="sxs-lookup"><span data-stu-id="79daf-155">If you have **Write** access to data in more than one company, then you can change the default company by choosing a record that belongs to different company.</span></span>

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="通过选择记录更改默认公司。":::

+ <span data-ttu-id="79daf-157">如果您是系统配置者或管理员，想要在自定义窗体上自动填充公司数据，可以使用[窗体事件](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids)。</span><span class="sxs-lookup"><span data-stu-id="79daf-157">If you are a system configurator or administrator, and you want to auto-populate company data on a custom form, then you can use [form events](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span></span> <span data-ttu-id="79daf-158">将 JavaScript 引用添加到 **msdyn_/DefaultCompany.js** 并使用以下事件。</span><span class="sxs-lookup"><span data-stu-id="79daf-158">Add a JavaScript reference to **msdyn_/DefaultCompany.js** and use the following events.</span></span> <span data-ttu-id="79daf-159">您可以使用任何现成的窗体，例如，**客户**窗体。</span><span class="sxs-lookup"><span data-stu-id="79daf-159">You can use any out-of-the-box form, for example, the **Account** form.</span></span>

    + <span data-ttu-id="79daf-160">窗体的 **OnLoad** 事件：设置 **defaultCompany** 字段。</span><span class="sxs-lookup"><span data-stu-id="79daf-160">**OnLoad** event for the form: Set the **defaultCompany** field.</span></span>
    + <span data-ttu-id="79daf-161">**公司**字段的 **OnChange** 事件：设置 **updateDefaultCompany** 字段。</span><span class="sxs-lookup"><span data-stu-id="79daf-161">**OnChange** event for the **Company** field: Set the **updateDefaultCompany** field.</span></span>

## <a name="apply-filtering-based-on-the-company-context"></a><span data-ttu-id="79daf-162">基于公司上下文应用筛选</span><span class="sxs-lookup"><span data-stu-id="79daf-162">Apply filtering based on the company context</span></span>

<span data-ttu-id="79daf-163">要在自定义窗体或添加到标准窗体的自定义查找字段中基于公司上下文应用筛选，请打开窗体，然后使用**相关记录筛选**部分应用公司筛选器。</span><span class="sxs-lookup"><span data-stu-id="79daf-163">To apply filtering based on the company context on your custom forms or on custom lookup fields added to the standard forms, open the form and use the **Related Records Filtering** section to apply the company filter.</span></span> <span data-ttu-id="79daf-164">您必须为每个需要基于给定记录中的基础公司来筛选的查找字段设置此项。</span><span class="sxs-lookup"><span data-stu-id="79daf-164">You must set this for each lookup field that requires filtering based on the underlying company on a given record.</span></span> <span data-ttu-id="79daf-165">下图中显示了**客户**的设置。</span><span class="sxs-lookup"><span data-stu-id="79daf-165">The setting is shown for **Account** in the following illustration.</span></span>

:::image type="content" source="media/apply-company-context.png" alt-text="应用公司上下文":::

