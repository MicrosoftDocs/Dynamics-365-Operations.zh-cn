---
title: 支持双写入的方案
description: 此主题介绍支持双写入的方案。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
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
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 1319f1228b635e207754f7c2516cb2b5353a9edd
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112395"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="3113a-103">支持双写入的方案</span><span class="sxs-lookup"><span data-stu-id="3113a-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="3113a-104">可以在 Finance and Operations 环境与 Common Data Service 环境之间建立双写入连接。</span><span class="sxs-lookup"><span data-stu-id="3113a-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="3113a-105">**Finance and Operations 环境** 为 **Finance and Operations 应用**（如 Microsoft Dynamics 365 Finance、Dynamics 365 Supply Chain Management、Dynamics 365 Retail 和 Dynamics 365 Human Resources）提供基础平台。</span><span class="sxs-lookup"><span data-stu-id="3113a-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="3113a-106">**Common Data Service 环境**为 **Dynamics 365 中的模型驱动应用**（Dynamics 365 Sales、Dynamics 365 Customer Service、Dynamics 365 Field Service、Dynamics 365 Marketing 和 Dynamics 365 Project Service Automation）提供基础平台。</span><span class="sxs-lookup"><span data-stu-id="3113a-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

<span data-ttu-id="3113a-107">设置机制取决于订阅和环境。</span><span class="sxs-lookup"><span data-stu-id="3113a-107">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="3113a-108">对于 Finance and Operations 应用的新实例，双写入连接的设置在 Microsoft Dynamics Lifecycle Services (LCS) 中开始。</span><span class="sxs-lookup"><span data-stu-id="3113a-108">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="3113a-109">如果您有 Microsoft Power Platform 的许可证，并且您的租户没有 Common Data Service 环境，您将获取一个新的该环境。</span><span class="sxs-lookup"><span data-stu-id="3113a-109">If you have a license for Microsoft Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="3113a-110">对于现有实例的 Finance and Operations 应用，双写入连接的设置在 Finance and Operations 环境中开始。</span><span class="sxs-lookup"><span data-stu-id="3113a-110">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="3113a-111">支持以下设置方案：</span><span class="sxs-lookup"><span data-stu-id="3113a-111">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="3113a-112">一个新 Finance and Operations 应用实例和一个新模型驱动应用实例</span><span class="sxs-lookup"><span data-stu-id="3113a-112">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="3113a-113">一个新 Finance and Operations 应用实例和一个现有模型驱动应用实例</span><span class="sxs-lookup"><span data-stu-id="3113a-113">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="3113a-114">一个具有演示数据的新 Finance and Operations 应用实例和一个新模型驱动应用实例</span><span class="sxs-lookup"><span data-stu-id="3113a-114">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="3113a-115">一个具有演示数据的新 Finance and Operations 应用实例和一个现有模型驱动应用实例</span><span class="sxs-lookup"><span data-stu-id="3113a-115">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="3113a-116">一个现有 Finance and Operations 应用实例和一个新的或现有模型驱动应用实例</span><span class="sxs-lookup"><span data-stu-id="3113a-116">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="3113a-117">一个新 Finance and Operations 应用实例和一个新模型驱动应用实例</span><span class="sxs-lookup"><span data-stu-id="3113a-117">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="3113a-118">若要在无数据的 Finance and Operations 应用新实例与 Dynamics 365 中的模型驱动应用新实例之间设置双写入连接，请执行[从 Lifecycle Services 设置双写入](lcs-setup.md)中的步骤。</span><span class="sxs-lookup"><span data-stu-id="3113a-118">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="3113a-119">完成连接设置之后，将自动执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="3113a-119">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="3113a-120">预配一个新的空 Finance and Operations 环境。</span><span class="sxs-lookup"><span data-stu-id="3113a-120">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="3113a-121">预配一个新的空模型驱动应用实例，其中已安装了 CRM 主解决方案。</span><span class="sxs-lookup"><span data-stu-id="3113a-121">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="3113a-122">为 DAT 公司数据建立双写入连接。</span><span class="sxs-lookup"><span data-stu-id="3113a-122">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="3113a-123">为实时同步启用实体映射。</span><span class="sxs-lookup"><span data-stu-id="3113a-123">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="3113a-124">然后，这两个环境准备好了进行实时数据同步。</span><span class="sxs-lookup"><span data-stu-id="3113a-124">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a><span data-ttu-id="3113a-125">一个新 Finance and Operations 应用实例和一个现有模型驱动应用实例</span><span class="sxs-lookup"><span data-stu-id="3113a-125">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="3113a-126">若要在无数据的 Finance and Operations 应用新实例与 Dynamics 365 中的模型驱动应用现有实例之间设置双写入连接，请执行[从 Lifecycle Services 设置双写入](lcs-setup.md)中的步骤。</span><span class="sxs-lookup"><span data-stu-id="3113a-126">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="3113a-127">完成连接设置之后，将自动执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="3113a-127">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="3113a-128">预配一个新的空 Finance and Operations 环境。</span><span class="sxs-lookup"><span data-stu-id="3113a-128">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="3113a-129">为 DAT 公司数据建立双写入连接。</span><span class="sxs-lookup"><span data-stu-id="3113a-129">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="3113a-130">为实时同步启用实体映射。</span><span class="sxs-lookup"><span data-stu-id="3113a-130">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="3113a-131">然后，这两个环境准备好了进行实时数据同步。</span><span class="sxs-lookup"><span data-stu-id="3113a-131">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="3113a-132">若要将现有 Common Data Service 数据同步到 Finance and Operations 应用，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="3113a-132">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="3113a-133">在 Finance and Operations 应用中创建一个新公司。</span><span class="sxs-lookup"><span data-stu-id="3113a-133">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="3113a-134">将该公司添加到双写入连接设置。</span><span class="sxs-lookup"><span data-stu-id="3113a-134">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="3113a-135">通过使用三个字母的国际标准化组织 (ISO) 公司代码[引导](bootstrap-company-data.md) Common Data Service 数据。</span><span class="sxs-lookup"><span data-stu-id="3113a-135">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="3113a-136">因为双写入处于实时同步模式，所以 Common Data Service 中的数据将自动开始流向 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="3113a-136">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a><span data-ttu-id="3113a-137">一个具有演示数据的新 Finance and Operations 应用实例和一个新模型驱动应用实例</span><span class="sxs-lookup"><span data-stu-id="3113a-137">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="3113a-138">若要在有演示数据的新 Finance and Operations 应用实例与 Dynamics 365 中的模型驱动应用新实例之间建立双写入连接，请执行此主题前文中[一个新 Finance and Operations 应用程序和一个新模型驱动应用实例](#new-new)部分中的步骤。</span><span class="sxs-lookup"><span data-stu-id="3113a-138">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="3113a-139">完成连接设置后，如果要将演示数据同步到模型驱动应用，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="3113a-139">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="3113a-140">从 LCS 页面打开 Finance and Operations 应用，然后转到**数据管理 \> 双写入**。</span><span class="sxs-lookup"><span data-stu-id="3113a-140">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="3113a-141">对要同步其数据的实体运行**初始同步**功能。</span><span class="sxs-lookup"><span data-stu-id="3113a-141">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a><span data-ttu-id="3113a-142">一个具有演示数据的新 Finance and Operations 应用实例和一个现有模型驱动应用实例</span><span class="sxs-lookup"><span data-stu-id="3113a-142">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="3113a-143">若要在有演示数据的新 Finance and Operations 应用实例与 Dynamics 365 中的模型驱动应用现有实例之间建立双写入连接，请执行此主题前文中[一个新 Finance and Operations 应用程序和一个现有模型驱动应用实例](#new-existing)部分中的步骤。</span><span class="sxs-lookup"><span data-stu-id="3113a-143">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="3113a-144">完成连接设置后，如果要将演示数据同步到模型驱动应用，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="3113a-144">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="3113a-145">从 LCS 页面打开 Finance and Operations 应用，然后转到**数据管理 \> 双写入**。</span><span class="sxs-lookup"><span data-stu-id="3113a-145">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="3113a-146">对要同步其数据的实体运行**初始同步**功能。</span><span class="sxs-lookup"><span data-stu-id="3113a-146">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="3113a-147">若要将现有 Common Data Service 数据同步到 Finance and Operations 应用，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="3113a-147">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="3113a-148">在 Finance and Operations 应用中创建一个新公司。</span><span class="sxs-lookup"><span data-stu-id="3113a-148">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="3113a-149">将该公司添加到双写入连接设置。</span><span class="sxs-lookup"><span data-stu-id="3113a-149">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="3113a-150">通过使用三个字母的 ISO 公司代码[引导](bootstrap-company-data.md) Common Data Service 数据。</span><span class="sxs-lookup"><span data-stu-id="3113a-150">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="3113a-151">因为双写入处于实时同步模式，所以 Common Data Service 中的数据将自动开始流向 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="3113a-151">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="3113a-152">一个现有 Finance and Operations 应用实例和一个新的或现有模型驱动应用实例</span><span class="sxs-lookup"><span data-stu-id="3113a-152">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="3113a-153">若要设置现有 Finance and Operations 应用实例与 Dynamics 365 中的模型驱动应用的新的或现有的实例之间的双写入连接，需要在 Finance and Operation 环境中进行。</span><span class="sxs-lookup"><span data-stu-id="3113a-153">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="3113a-154">从 Finance and Operations 应用设置连接。</span><span class="sxs-lookup"><span data-stu-id="3113a-154">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="3113a-155">若要将现有 Common Data Service 数据同步到 Finance and Operations 应用，请使用三个字母的 ISO 公司代码[引导](bootstrap-company-data.md) Common Data Service 数据。</span><span class="sxs-lookup"><span data-stu-id="3113a-155">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="3113a-156">因为双写入处于实时同步模式，所以 Common Data Service 中的数据将自动开始流向 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="3113a-156">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>
