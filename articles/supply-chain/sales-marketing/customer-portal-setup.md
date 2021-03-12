---
title: 安装、设置和更新客户门户
description: 本主题提供客户门户的许可详细信息和设置说明。
author: dasani-madipalli
manager: tfehr
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 2153bbca2be7c72e48b9dc51b1f7fdbe2ab89903
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977730"
---
# <a name="install-set-up-and-update-the-customer-portal"></a><span data-ttu-id="59add-103">安装、设置和更新客户门户</span><span class="sxs-lookup"><span data-stu-id="59add-103">Install, set up, and update the Customer portal</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="licensing-requirements"></a><span data-ttu-id="59add-104">许可要求</span><span class="sxs-lookup"><span data-stu-id="59add-104">Licensing requirements</span></span>

<span data-ttu-id="59add-105">要实施客户门户，您必须具有以下许可证：</span><span class="sxs-lookup"><span data-stu-id="59add-105">To implement the Customer portal, you must have the following licenses:</span></span>

- <span data-ttu-id="59add-106">**Power Apps 门户** – 托管客户门户需要此许可证。</span><span class="sxs-lookup"><span data-stu-id="59add-106">**Power Apps portals** – This license is required to host the Customer portal.</span></span> <span data-ttu-id="59add-107">门户根据使用获得许可。</span><span class="sxs-lookup"><span data-stu-id="59add-107">Portals are licensed based on usage.</span></span> <span data-ttu-id="59add-108">有关详细信息，请参阅 [Power Apps 门户许可要求](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals)。</span><span class="sxs-lookup"><span data-stu-id="59add-108">For more information, see the [Power Apps portals licensing requirements](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span></span>
- <span data-ttu-id="59add-109">**双写入** – 您必须具有必要的许可证才能为 Supply Chain Management 表启用双写入。</span><span class="sxs-lookup"><span data-stu-id="59add-109">**Dual-write** – You must have the necessary licenses to enable dual-write for Supply Chain Management tables.</span></span> <span data-ttu-id="59add-110">有关详细信息，请参阅[双写入的系统要求](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md)。</span><span class="sxs-lookup"><span data-stu-id="59add-110">For more information, see the [system requirements for dual-write](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span></span>

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a><span data-ttu-id="59add-111">双写入和 Power Apps 门户的依赖关系</span><span class="sxs-lookup"><span data-stu-id="59add-111">Dependencies on dual-write and Power Apps portals</span></span>

<span data-ttu-id="59add-112">客户门户依赖 Power Apps 门户和双写入，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="59add-112">The Customer portal depends on Power Apps portals and dual-write, as shown in the following illustration.</span></span>

<span data-ttu-id="59add-113">![客户门户依赖关系](media/customer-portal-elements.png "客户门户依赖关系")</span><span class="sxs-lookup"><span data-stu-id="59add-113">![Customer portal dependencies](media/customer-portal-elements.png "Customer portal dependencies")</span></span>

<span data-ttu-id="59add-114">与 Supply Chain Management 的其他功能不同，客户门户模板位于 Power Apps 门户中。</span><span class="sxs-lookup"><span data-stu-id="59add-114">Unlike other features from Supply Chain Management, the Customer portal template resides in Power Apps portals.</span></span> <span data-ttu-id="59add-115">因此，客户门户受 Power Apps 门户和采用双写入的表提供的功能限制。</span><span class="sxs-lookup"><span data-stu-id="59add-115">Therefore, the Customer portal is limited by the functionality and capabilities that are provided by Power Apps portals and the tables in dual-write.</span></span>

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a><span data-ttu-id="59add-116">启用客户门户需要设置</span><span class="sxs-lookup"><span data-stu-id="59add-116">Required setup to enable the Customer portal</span></span>

<span data-ttu-id="59add-117">确定已有必需的许可证后，您可以按照[双写入初始同步说明](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md)所述设置双写入。</span><span class="sxs-lookup"><span data-stu-id="59add-117">After you've made sure that you have the required licenses, you can set up dual-write as described in the [dual-write initial synchronization instructions](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span></span>

<span data-ttu-id="59add-118">确保以双写入方式启用以下表映射：</span><span class="sxs-lookup"><span data-stu-id="59add-118">Be sure to enable the following table mappings in dual-write:</span></span>

- <span data-ttu-id="59add-119">销售订单头</span><span class="sxs-lookup"><span data-stu-id="59add-119">Sales Order Header</span></span>
- <span data-ttu-id="59add-120">销售订单详细信息</span><span class="sxs-lookup"><span data-stu-id="59add-120">Sales Order Details</span></span>
- <span data-ttu-id="59add-121">科目</span><span class="sxs-lookup"><span data-stu-id="59add-121">Accounts</span></span>
- <span data-ttu-id="59add-122">联系人</span><span class="sxs-lookup"><span data-stu-id="59add-122">Contacts</span></span>
- <span data-ttu-id="59add-123">产品</span><span class="sxs-lookup"><span data-stu-id="59add-123">Products</span></span>

<span data-ttu-id="59add-124">完成此设置后，您可以预配客户门户模板。</span><span class="sxs-lookup"><span data-stu-id="59add-124">After this setup is completed, you can provision the Customer portal template.</span></span>

## <a name="provision-the-customer-portal"></a><span data-ttu-id="59add-125">预配客户门户</span><span class="sxs-lookup"><span data-stu-id="59add-125">Provision the Customer portal</span></span>

<span data-ttu-id="59add-126">开始之前，请确保您已经完成了[所需设置](#required-setup)。</span><span class="sxs-lookup"><span data-stu-id="59add-126">Before you begin, make sure that you've already completed the [required setup](#required-setup).</span></span> <span data-ttu-id="59add-127">然后按照以下步骤预配客户门户。</span><span class="sxs-lookup"><span data-stu-id="59add-127">Then follow these steps to provision the Customer portal.</span></span>

1. <span data-ttu-id="59add-128">转到 [make.powerapps.com](https://make.powerapps.com/)。</span><span class="sxs-lookup"><span data-stu-id="59add-128">Go to [make.powerapps.com](https://make.powerapps.com/).</span></span>
2. <span data-ttu-id="59add-129">确保您使用的是启用了双写入的环境。</span><span class="sxs-lookup"><span data-stu-id="59add-129">Make sure that you're using the environment where you enabled dual-write.</span></span>
3. <span data-ttu-id="59add-130">在 **创建** 选项卡上，向下滚动到 **从模板开始** 部分，然后选择名为 **客户门户** 的模板。</span><span class="sxs-lookup"><span data-stu-id="59add-130">On the **Create** tab, scroll down to the **Start from template** section, and select the template that is named **Customer Portal**.</span></span>
4. <span data-ttu-id="59add-131">按照屏幕上的说明操作。</span><span class="sxs-lookup"><span data-stu-id="59add-131">Follow the on-screen instructions.</span></span>

<span data-ttu-id="59add-132">预配完成后，您可以在 **主页** 页面 **我的应用** 部分访问客户门户。</span><span class="sxs-lookup"><span data-stu-id="59add-132">After provisioning is completed, you can access the Customer portal in the **Your apps** section of the **Home** page.</span></span>

> [!NOTE]
> <span data-ttu-id="59add-133">如果您使用的环境中未安装双写入解决方案，您会收到错误消息，客户门户不会预配。</span><span class="sxs-lookup"><span data-stu-id="59add-133">If the dual-write solution isn't installed in the environment that you're working in, you will receive an error message, and the Customer portal won't be provisioned.</span></span>

## <a name="update-the-customer-portal"></a><span data-ttu-id="59add-134">更新客户门户</span><span class="sxs-lookup"><span data-stu-id="59add-134">Update the Customer portal</span></span>

<span data-ttu-id="59add-135">以后可能会向客户门户添加更多功能。</span><span class="sxs-lookup"><span data-stu-id="59add-135">More functionality might be added to the Customer portal later.</span></span> <span data-ttu-id="59add-136">Microsoft 对基础解决方案组件所做的任何更改都将自动显示在您的环境中。</span><span class="sxs-lookup"><span data-stu-id="59add-136">Any changes that Microsoft makes to the underlying solution components will automatically appear in your environment.</span></span> <span data-ttu-id="59add-137">但是，在您的环境中预配的网站不会自动反映对配置数据所作的更改。</span><span class="sxs-lookup"><span data-stu-id="59add-137">However, the website that is provisioned in your environment won't automatically reflect changes that are made to the configuration data.</span></span> <span data-ttu-id="59add-138">您必须通过从新模板获取代码并将其与预配的网站合并来手动应用这些更改。</span><span class="sxs-lookup"><span data-stu-id="59add-138">You will have to manually apply those changes by getting the code from the new template and merging it with the provisioned website.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59add-139">其他资源</span><span class="sxs-lookup"><span data-stu-id="59add-139">Additional resources</span></span>

<span data-ttu-id="59add-140">要了解如何设置和自定义客户门户，您应该先查看以下有关基础技术的文档：</span><span class="sxs-lookup"><span data-stu-id="59add-140">To learn how you can set up and customize the Customer portal, you should start by reviewing the following documentation for the underlying technologies:</span></span>

- [<span data-ttu-id="59add-141">Power Apps 门户文档</span><span class="sxs-lookup"><span data-stu-id="59add-141">Power Apps portals documentation</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [<span data-ttu-id="59add-142">双写入文档</span><span class="sxs-lookup"><span data-stu-id="59add-142">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

<span data-ttu-id="59add-143">为了有效地管理门户，您必须了解 Power Apps 门户和 Microsoft Dataverse 生命周期。</span><span class="sxs-lookup"><span data-stu-id="59add-143">To effectively manage your portals, you must understand the Power Apps portals and Microsoft Dataverse lifecycle.</span></span> <span data-ttu-id="59add-144">有关详细信息，请参阅以下资源：</span><span class="sxs-lookup"><span data-stu-id="59add-144">For more information, see the following resources:</span></span>

- [<span data-ttu-id="59add-145">关于门户生命周期</span><span class="sxs-lookup"><span data-stu-id="59add-145">About portal lifecycle</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="59add-146">升级门户</span><span class="sxs-lookup"><span data-stu-id="59add-146">Upgrade a portal</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="59add-147">迁移门户配置</span><span class="sxs-lookup"><span data-stu-id="59add-147">Migrate portal configuration</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="59add-148">解决方案生命周期管理：Dynamics 365 for Customer Engagement 应用</span><span class="sxs-lookup"><span data-stu-id="59add-148">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)
