---
title: 双写入设置指南
description: 此主题介绍支持双写入的方案。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 47c07dd0e2f311b61297340a48a5a31cb1de3903
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685657"
---
# <a name="guidance-for-dual-write-setup"></a><span data-ttu-id="c5fd5-103">双写入设置指南</span><span class="sxs-lookup"><span data-stu-id="c5fd5-103">Guidance for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c5fd5-104">可以在 Finance and Operations 环境与 Dataverse 环境之间建立双写入连接。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-104">You can set up a dual-write connection between a Finance and Operations environment and a Dataverse environment.</span></span>

+ <span data-ttu-id="c5fd5-105">**Finance and Operations 环境** 为 **Finance and Operations 应用**（如 Microsoft Dynamics 365 Finance、Dynamics 365 Supply Chain Management、Dynamics 365 Commerce 和 Dynamics 365 Human Resources）提供基础平台。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="c5fd5-106">**Dataverse 环境** 为 **Customer Engagement 应用**（Dynamics 365 Sales、Dynamics 365 Customer Service、Dynamics 365 Field Service、Dynamics 365 Marketing 和 Dynamics 365 Project Service Automation）提供基础平台。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-106">A **Dataverse environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c5fd5-107">Dynamics 365 Finance 中的 Human Resources 模块支持双写入连接，但 Dynamics 365 Human Resources 应用不支持。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-107">The Human Resources module in Dynamics 365 Finance supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="c5fd5-108">设置机制取决于订阅和环境：</span><span class="sxs-lookup"><span data-stu-id="c5fd5-108">The setup mechanism varies, depending on your subscription and the environment:</span></span>

+ <span data-ttu-id="c5fd5-109">对于 Finance and Operations 应用的新实例，双写入连接的设置在 Microsoft Dynamics Lifecycle Services (LCS) 中开始。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="c5fd5-110">如果您有 Microsoft Power Platform 的许可证，并且您的租户没有 Dataverse 环境，您将获取一个新的该环境。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-110">If you have a license for Microsoft Power Platform, you will get a new Dataverse environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="c5fd5-111">对于现有实例的 Finance and Operations 应用，双写入连接的设置在 Finance and Operations 环境中开始。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="c5fd5-112">在实体上开始双写入之前，您可以运行初始同步以处理 Finance and Operations 应用和 Customer Engagement 应用上的现有数据。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-112">Before you start dual-write on an entity, you can run an initial synchronization to handle existing data on both sides: Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="c5fd5-113">如果不需要在两个环境之间同步数据，则可以跳过初始同步。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-113">You can skip the initial synchronization if you don't have to sync data between the two environments.</span></span>

<span data-ttu-id="c5fd5-114">初始同步使您可以将现有数据从一个应用双向复制到另一个应用。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-114">An initial synchronization lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="c5fd5-115">根据已有的环境及其中的数据类型，有几种设置方案。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-115">There are several setup scenarios, depending on the environments that you already have and the type of data in them.</span></span>

<span data-ttu-id="c5fd5-116">支持以下设置方案：</span><span class="sxs-lookup"><span data-stu-id="c5fd5-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="c5fd5-117">一个新的 Finance and Operations 应用实例和一个新的 Customer Engagement 应用实例</span><span class="sxs-lookup"><span data-stu-id="c5fd5-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="c5fd5-118">一个新的 Finance and Operations 应用实例和一个现有的 Customer Engagement 应用实例</span><span class="sxs-lookup"><span data-stu-id="c5fd5-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="c5fd5-119">一个具有数据的新 Finance and Operations 应用实例和一个新的 Customer Engagement 应用实例</span><span class="sxs-lookup"><span data-stu-id="c5fd5-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="c5fd5-120">一个具有数据的新 Finance and Operations 应用实例和一个现有的 Customer Engagement 应用实例</span><span class="sxs-lookup"><span data-stu-id="c5fd5-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="c5fd5-121">一个现有的 Finance and Operations 应用实例和一个新的 Customer Engagement 应用实例</span><span class="sxs-lookup"><span data-stu-id="c5fd5-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="c5fd5-122">一个现有的 Finance and Operations 应用实例和一个现有的 Customer Engagement 应用实例</span><span class="sxs-lookup"><span data-stu-id="c5fd5-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="c5fd5-123">一个新的 Finance and Operations 应用实例和一个新的 Customer Engagement 应用实例</span><span class="sxs-lookup"><span data-stu-id="c5fd5-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="c5fd5-124">若要在一个无数据的新 Finance and Operations 应用实例与一个新的 Customer Engagement 应用实例之间设置双写入连接，请按照[从 Lifecycle Services 设置双写入](lcs-setup.md)中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="c5fd5-125">完成连接设置之后，将自动执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="c5fd5-125">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="c5fd5-126">预配一个新的空 Finance and Operations 环境。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="c5fd5-127">预配一个新的空 Customer Engagement 应用实例，其中已安装了 CRM 主解决方案。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="c5fd5-128">为 DAT 公司数据建立双写入连接。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="c5fd5-129">为实时同步启用表映射。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-129">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="c5fd5-130">然后，这两个环境准备好了进行实时数据同步。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="c5fd5-131">一个新的 Finance and Operations 应用实例和一个现有的 Customer Engagement 应用实例</span><span class="sxs-lookup"><span data-stu-id="c5fd5-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="c5fd5-132">若要在一个无数据的新 Finance and Operations 应用实例与一个现有的 Customer Engagement 应用实例之间设置双写入连接，请按照[从 Lifecycle Services 设置双写入](lcs-setup.md)中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="c5fd5-133">完成连接设置之后，将自动执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="c5fd5-133">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="c5fd5-134">预配一个新的空 Finance and Operations 环境。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="c5fd5-135">为 DAT 公司数据建立双写入连接。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="c5fd5-136">为实时同步启用表映射。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-136">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="c5fd5-137">然后，这两个环境准备好了进行实时数据同步。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="c5fd5-138">若要将现有 Dataverse 数据同步到 Finance and Operations 应用，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-138">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="c5fd5-139">在 Finance and Operations 应用中创建一个新公司。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="c5fd5-140">将该公司添加到双写入连接设置。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="c5fd5-141">通过使用三个字母的国际标准化组织 (ISO) 公司代码[引导](bootstrap-company-data.md) Dataverse 数据。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-141">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="c5fd5-142">对要同步其数据的表运行 **初始同步** 功能。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-142">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="c5fd5-143">有关示例和备用方法的链接，请参阅本主题后文的[示例](#example)部分。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-143">For links to an example and an alternative approach, see the [Example](#example) section later in this topic.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="c5fd5-144">一个具有数据的新 Finance and Operations 应用实例和一个新的 Customer Engagement 应用实例</span><span class="sxs-lookup"><span data-stu-id="c5fd5-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="c5fd5-145">若要在一个具有数据的新 Finance and Operations 应用实例与一个新的 Customer Engagement 应用实例之间设置双写入连接，请按照本主题前面的[一个新的 Finance and Operations 应用实例和一个新的 Customer Engagement 应用实例](#new-new)部分中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="c5fd5-146">完成连接设置后，如果要将数据同步到 Customer Engagement 应用，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="c5fd5-147">从 LCS 页面打开 Finance and Operations 应用，然后转到 **数据管理 \> 双写入**。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="c5fd5-148">对要同步其数据的表运行 **初始同步** 功能。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-148">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="c5fd5-149">有关示例和备用方法的链接，请参阅[示例](#example)部分。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-149">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="c5fd5-150">一个具有数据的新 Finance and Operations 应用实例和一个现有的 Customer Engagement 应用实例</span><span class="sxs-lookup"><span data-stu-id="c5fd5-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="c5fd5-151">若要在一个具有数据的新 Finance and Operations 应用实例与一个现有的 Customer Engagement 应用实例之间设置双写入连接，请按照本主题前面的[一个新的 Finance and Operations 应用实例和一个现有的 Customer Engagement 应用实例](#new-existing)部分中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="c5fd5-152">完成连接设置后，如果要将数据同步到 Customer Engagement 应用，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="c5fd5-153">从 LCS 页面打开 Finance and Operations 应用，然后转到 **数据管理 \> 双写入**。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="c5fd5-154">对要同步其数据的表运行 **初始同步** 功能。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-154">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="c5fd5-155">若要将现有 Dataverse 数据同步到 Finance and Operations 应用，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-155">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="c5fd5-156">在 Finance and Operations 应用中创建一个新公司。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="c5fd5-157">将该公司添加到双写入连接设置。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="c5fd5-158">通过使用三个字母的 ISO 公司代码[引导](bootstrap-company-data.md) Dataverse 数据。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-158">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="c5fd5-159">对要同步其数据的表运行 **初始同步** 功能。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-159">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="c5fd5-160">有关示例和备用方法的链接，请参阅[示例](#example)部分。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-160">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="c5fd5-161">一个现有的 Finance and Operations 应用实例和一个新的 Customer Engagement 应用实例</span><span class="sxs-lookup"><span data-stu-id="c5fd5-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="c5fd5-162">若要在一个现有的 Finance and Operations 应用实例与一个新的 Customer Engagement 应用实例之间设置双写入连接，需要在 Finance and Operation 环境中进行。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="c5fd5-163">[从 Finance and Operations 应用设置连接](enable-dual-write.md)。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="c5fd5-164">对要同步其数据的表运行 **初始同步** 功能。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-164">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="c5fd5-165">有关示例和备用方法的链接，请参阅[示例](#example)部分。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-165">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="c5fd5-166">一个现有的 Finance and Operations 应用实例和一个现有的 Customer Engagement 应用实例</span><span class="sxs-lookup"><span data-stu-id="c5fd5-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="c5fd5-167">若要在一个现有的 Finance and Operations 应用实例与一个现有的 Customer Engagement 应用实例之间设置双写入连接，需要在 Finance and Operation 环境中进行。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="c5fd5-168">[从 Finance and Operations 应用设置连接](enable-dual-write.md)。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-168">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="c5fd5-169">若要将现有 Dataverse 数据同步到 Finance and Operations 应用，请使用三个字母的 ISO 公司代码[引导](bootstrap-company-data.md) Dataverse 数据。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-169">To sync the existing Dataverse data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="c5fd5-170">对要同步其数据的表运行 **初始同步** 功能。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-170">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="c5fd5-171">有关示例和备用方法的链接，请参阅[示例](#example)部分。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-171">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="example"></a><span data-ttu-id="c5fd5-172">示例</span><span class="sxs-lookup"><span data-stu-id="c5fd5-172">Example</span></span>

<span data-ttu-id="c5fd5-173">有关示例，请参见[启用客户 V3 到联系人的表映射](enable-entity-map.md#enable-table-map)</span><span class="sxs-lookup"><span data-stu-id="c5fd5-173">For an example, see [Enabling the Customers V3—Contacts table map](enable-entity-map.md#enable-table-map)</span></span>

<span data-ttu-id="c5fd5-174">有关基于每个实体中必须运行初始同步的数据量的替代方法，请参阅[初始同步的注意事项](initial-sync-guidance.md)。</span><span class="sxs-lookup"><span data-stu-id="c5fd5-174">For an alternative approach that is based on data volumes in each entity that must run an initial synchronization, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>
