---
title: 有关如何设置双写入的指南
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
ms.openlocfilehash: 2d77a1458f3f4c79b231e6a6d7cc320b8ee1fad9
ms.sourcegitcommit: ee643d651d57560bccae2f99238faa39881f5c64
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088498"
---
# <a name="guidance-for-how-to-set-up-dual-write"></a><span data-ttu-id="889b1-103">有关如何设置双写入的指南</span><span class="sxs-lookup"><span data-stu-id="889b1-103">Guidance for how to set up dual-write</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="889b1-104">可以在 Finance and Operations 环境与 Common Data Service 环境之间建立双写入连接。</span><span class="sxs-lookup"><span data-stu-id="889b1-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="889b1-105">**Finance and Operations 环境** 为 **Finance and Operations 应用** （例如，Microsoft Dynamics 365 Finance、Dynamics 365 Supply Chain Management 和 Dynamics 365 Retail）提供基础平台。</span><span class="sxs-lookup"><span data-stu-id="889b1-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, and Dynamics 365 Retail).</span></span>
+ <span data-ttu-id="889b1-106">**Common Data Service 环境** 为 **Customer Engagement 应用** （Dynamics 365 Sales、Dynamics 365 Customer Service、Dynamics 365 Field Service、Dynamics 365 Marketing 和 Dynamics 365 Project Service Automation）提供基础平台。</span><span class="sxs-lookup"><span data-stu-id="889b1-106">A **Common Data Service environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

>[!IMPORTANT]
><span data-ttu-id="889b1-107">Finance and Operations 中的 Human Resources 支持双写入连接，但 Dynamics 365 Human Resources 应用不支持。</span><span class="sxs-lookup"><span data-stu-id="889b1-107">Human Resources in Finance and Operations supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="889b1-108">设置机制取决于订阅和环境。</span><span class="sxs-lookup"><span data-stu-id="889b1-108">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="889b1-109">对于 Finance and Operations 应用的新实例，双写入连接的设置在 Microsoft Dynamics Lifecycle Services (LCS) 中开始。</span><span class="sxs-lookup"><span data-stu-id="889b1-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="889b1-110">如果您有 Power Platform 的许可证，并且您的租户没有 Common Data Service 环境，您将获取一个新的该环境。</span><span class="sxs-lookup"><span data-stu-id="889b1-110">If you have a license for Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="889b1-111">对于现有实例的 Finance and Operations 应用，双写入连接的设置在 Finance and Operations 环境中开始。</span><span class="sxs-lookup"><span data-stu-id="889b1-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="889b1-112">在实体上开始双写入之前，您可以运行初始同步以处理 Finance and Operations 应用和 Customer Engagement 应用上的现有数据。</span><span class="sxs-lookup"><span data-stu-id="889b1-112">Before you start dual-write on an entity, you can run an initial sync to handle existing data on both sides of Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="889b1-113">如果不需要在两个环境之间同步数据，则可以跳过初始同步。</span><span class="sxs-lookup"><span data-stu-id="889b1-113">You can skip the initial sync if you don't need to synchronize data between the two environments.</span></span>

<span data-ttu-id="889b1-114">初始同步使您可以将现有数据从一个应用双向复制到另一个应用。</span><span class="sxs-lookup"><span data-stu-id="889b1-114">An initial sync lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="889b1-115">根据已有的环境以及环境中的数据类型，有几种不同的设置方案。</span><span class="sxs-lookup"><span data-stu-id="889b1-115">There are several different setup scenarios depending on which environments you already have and what type of data is in the environments.</span></span>

<span data-ttu-id="889b1-116">支持以下设置方案：</span><span class="sxs-lookup"><span data-stu-id="889b1-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="889b1-117">一个新的 Finance and Operations 应用实例和一个新的 Customer Engagement 应用实例</span><span class="sxs-lookup"><span data-stu-id="889b1-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="889b1-118">一个新的 Finance and Operations 应用实例和一个现有的 Customer Engagement 应用实例</span><span class="sxs-lookup"><span data-stu-id="889b1-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="889b1-119">一个具有数据的新 Finance and Operations 应用实例和一个新的 Customer Engagement 应用实例</span><span class="sxs-lookup"><span data-stu-id="889b1-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="889b1-120">一个具有数据的新 Finance and Operations 应用实例和一个现有的 Customer Engagement 应用实例</span><span class="sxs-lookup"><span data-stu-id="889b1-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="889b1-121">一个现有的 Finance and Operations 应用实例和一个新的 Customer Engagement 应用实例</span><span class="sxs-lookup"><span data-stu-id="889b1-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="889b1-122">一个现有的 Finance and Operations 应用实例和一个现有的 Customer Engagement 应用实例</span><span class="sxs-lookup"><span data-stu-id="889b1-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="889b1-123">一个新的 Finance and Operations 应用实例和一个新的 Customer Engagement 应用实例</span><span class="sxs-lookup"><span data-stu-id="889b1-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="889b1-124">若要在一个无数据的新 Finance and Operations 应用实例与一个新的 Customer Engagement 应用实例之间设置双写入连接，请按照[从 Lifecycle Services 设置双写入](lcs-setup.md)中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="889b1-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="889b1-125">完成连接设置之后，将自动执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="889b1-125">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="889b1-126">预配一个新的空 Finance and Operations 环境。</span><span class="sxs-lookup"><span data-stu-id="889b1-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="889b1-127">预配一个新的空 Customer Engagement 应用实例，其中已安装了 CRM 主解决方案。</span><span class="sxs-lookup"><span data-stu-id="889b1-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="889b1-128">为 DAT 公司数据建立双写入连接。</span><span class="sxs-lookup"><span data-stu-id="889b1-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="889b1-129">为实时同步启用实体映射。</span><span class="sxs-lookup"><span data-stu-id="889b1-129">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="889b1-130">然后，这两个环境准备好了进行实时数据同步。</span><span class="sxs-lookup"><span data-stu-id="889b1-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="889b1-131">一个新的 Finance and Operations 应用实例和一个现有的 Customer Engagement 应用实例</span><span class="sxs-lookup"><span data-stu-id="889b1-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="889b1-132">若要在一个无数据的新 Finance and Operations 应用实例与一个现有的 Customer Engagement 应用实例之间设置双写入连接，请按照[从 Lifecycle Services 设置双写入](lcs-setup.md)中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="889b1-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="889b1-133">完成连接设置之后，将自动执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="889b1-133">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="889b1-134">预配一个新的空 Finance and Operations 环境。</span><span class="sxs-lookup"><span data-stu-id="889b1-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="889b1-135">为 DAT 公司数据建立双写入连接。</span><span class="sxs-lookup"><span data-stu-id="889b1-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="889b1-136">为实时同步启用实体映射。</span><span class="sxs-lookup"><span data-stu-id="889b1-136">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="889b1-137">然后，这两个环境准备好了进行实时数据同步。</span><span class="sxs-lookup"><span data-stu-id="889b1-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="889b1-138">若要将现有 Common Data Service 数据同步到 Finance and Operations 应用，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="889b1-138">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="889b1-139">在 Finance and Operations 应用中创建一个新公司。</span><span class="sxs-lookup"><span data-stu-id="889b1-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="889b1-140">将该公司添加到双写入连接设置。</span><span class="sxs-lookup"><span data-stu-id="889b1-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="889b1-141">通过使用三个字母的国际标准化组织 (ISO) 公司代码[引导](bootstrap-company-data.md) Common Data Service 数据。</span><span class="sxs-lookup"><span data-stu-id="889b1-141">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="889b1-142">对要同步其数据的实体运行 **初始同步** 功能。</span><span class="sxs-lookup"><span data-stu-id="889b1-142">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="889b1-143">有关示例和替代方法，请参阅[示例](#example)。</span><span class="sxs-lookup"><span data-stu-id="889b1-143">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="889b1-144">一个具有数据的新 Finance and Operations 应用实例和一个新的 Customer Engagement 应用实例</span><span class="sxs-lookup"><span data-stu-id="889b1-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="889b1-145">若要在一个具有数据的新 Finance and Operations 应用实例与一个新的 Customer Engagement 应用实例之间设置双写入连接，请按照本主题前面的[一个新的 Finance and Operations 应用实例和一个新的 Customer Engagement 应用实例](#new-new)部分中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="889b1-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="889b1-146">完成连接设置后，如果要将数据同步到 Customer Engagement 应用，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="889b1-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="889b1-147">从 LCS 页面打开 Finance and Operations 应用，然后转到 **数据管理 \> 双写入** 。</span><span class="sxs-lookup"><span data-stu-id="889b1-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="889b1-148">对要同步其数据的实体运行 **初始同步** 功能。</span><span class="sxs-lookup"><span data-stu-id="889b1-148">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="889b1-149">有关示例和替代方法，请参阅[示例](#example)。</span><span class="sxs-lookup"><span data-stu-id="889b1-149">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="889b1-150">一个具有数据的新 Finance and Operations 应用实例和一个现有的 Customer Engagement 应用实例</span><span class="sxs-lookup"><span data-stu-id="889b1-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="889b1-151">若要在一个具有数据的新 Finance and Operations 应用实例与一个现有的 Customer Engagement 应用实例之间设置双写入连接，请按照本主题前面的[一个新的 Finance and Operations 应用实例和一个现有的 Customer Engagement 应用实例](#new-existing)部分中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="889b1-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="889b1-152">完成连接设置后，如果要将数据同步到 Customer Engagement 应用，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="889b1-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="889b1-153">从 LCS 页面打开 Finance and Operations 应用，然后转到 **数据管理 \> 双写入** 。</span><span class="sxs-lookup"><span data-stu-id="889b1-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="889b1-154">对要同步其数据的实体运行 **初始同步** 功能。</span><span class="sxs-lookup"><span data-stu-id="889b1-154">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="889b1-155">若要将现有 Common Data Service 数据同步到 Finance and Operations 应用，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="889b1-155">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="889b1-156">在 Finance and Operations 应用中创建一个新公司。</span><span class="sxs-lookup"><span data-stu-id="889b1-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="889b1-157">将该公司添加到双写入连接设置。</span><span class="sxs-lookup"><span data-stu-id="889b1-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="889b1-158">通过使用三个字母的 ISO 公司代码[引导](bootstrap-company-data.md) Common Data Service 数据。</span><span class="sxs-lookup"><span data-stu-id="889b1-158">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="889b1-159">对要同步其数据的实体运行 **初始同步** 功能。</span><span class="sxs-lookup"><span data-stu-id="889b1-159">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="889b1-160">有关示例和替代方法，请参阅[示例](#example)。</span><span class="sxs-lookup"><span data-stu-id="889b1-160">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="889b1-161">一个现有的 Finance and Operations 应用实例和一个新的 Customer Engagement 应用实例</span><span class="sxs-lookup"><span data-stu-id="889b1-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="889b1-162">若要在一个现有的 Finance and Operations 应用实例与一个新的 Customer Engagement 应用实例之间设置双写入连接，需要在 Finance and Operation 环境中进行。</span><span class="sxs-lookup"><span data-stu-id="889b1-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="889b1-163">[从 Finance and Operations 应用设置连接](enable-dual-write.md)。</span><span class="sxs-lookup"><span data-stu-id="889b1-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="889b1-164">对要同步其数据的实体运行 **初始同步** 功能。</span><span class="sxs-lookup"><span data-stu-id="889b1-164">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="889b1-165">有关示例和替代方法，请参阅[示例](#example)。</span><span class="sxs-lookup"><span data-stu-id="889b1-165">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="889b1-166">一个现有的 Finance and Operations 应用实例和一个现有的 Customer Engagement 应用实例</span><span class="sxs-lookup"><span data-stu-id="889b1-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="889b1-167">若要在一个现有的 Finance and Operations 应用实例与一个现有的 Customer Engagement 应用实例之间设置双写入连接，需要在 Finance and Operation 环境中进行。</span><span class="sxs-lookup"><span data-stu-id="889b1-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app  occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="889b1-168">从 Finance and Operations 应用设置连接。</span><span class="sxs-lookup"><span data-stu-id="889b1-168">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="889b1-169">若要将现有 Common Data Service 数据同步到 Finance and Operations 应用，请使用三个字母的 ISO 公司代码[引导](bootstrap-company-data.md) Common Data Service 数据。</span><span class="sxs-lookup"><span data-stu-id="889b1-169">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="889b1-170">对要同步其数据的实体运行 **初始同步** 功能。</span><span class="sxs-lookup"><span data-stu-id="889b1-170">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="889b1-171">有关示例和替代方法，请参阅[示例](#example)。</span><span class="sxs-lookup"><span data-stu-id="889b1-171">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="example"></a><span data-ttu-id="889b1-172">示例</span><span class="sxs-lookup"><span data-stu-id="889b1-172">Example</span></span>

<span data-ttu-id="889b1-173">有关示例，请参见[启用客户 V3 到联系人的实体映射](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)</span><span class="sxs-lookup"><span data-stu-id="889b1-173">For an example, see [Enabling the Customers V3—Contacts entity map](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)</span></span>

<span data-ttu-id="889b1-174">有关基于每个实体中需要运行初始同步的数据量的替代方法，请参阅[初始同步的注意事项](initial-sync-guidance.md)。</span><span class="sxs-lookup"><span data-stu-id="889b1-174">For an alternative approach based on data volumes in each entity that need to run initial sync, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>
