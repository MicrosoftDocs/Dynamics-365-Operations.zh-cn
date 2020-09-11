---
title: 支持双写入的方案
description: 此主题介绍支持双写入的方案。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/17/2020
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
ms.openlocfilehash: 275d24d8f32fd1d2d15356d14c5c6591e8503c65
ms.sourcegitcommit: ec4df354602c20f48f8581bfe5be0c04c66d2927
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/19/2020
ms.locfileid: "3706244"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="d17cc-103">支持双写入的方案</span><span class="sxs-lookup"><span data-stu-id="d17cc-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="d17cc-104">可以在 Finance and Operations 环境与 Common Data Service 环境之间建立双写入连接。</span><span class="sxs-lookup"><span data-stu-id="d17cc-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="d17cc-105">**Finance and Operations 环境**为 **Finance and Operations 应用**（例如，Microsoft Dynamics 365 Finance、Dynamics 365 Supply Chain Management 和 Dynamics 365 Retail）提供基础平台。</span><span class="sxs-lookup"><span data-stu-id="d17cc-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, and Dynamics 365 Retail).</span></span>
+ <span data-ttu-id="d17cc-106">**Common Data Service 环境**为 **Dynamics 365 中的模型驱动应用**（Dynamics 365 Sales、Dynamics 365 Customer Service、Dynamics 365 Field Service、Dynamics 365 Marketing 和 Dynamics 365 Project Service Automation）提供基础平台。</span><span class="sxs-lookup"><span data-stu-id="d17cc-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

>[!IMPORTANT]
><span data-ttu-id="d17cc-107">Finance and Operations 中的 Human Resources 支持双写入连接，但 Dynamics 365 Human Resources 应用不支持。</span><span class="sxs-lookup"><span data-stu-id="d17cc-107">Human Resources in Finance and Operations supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="d17cc-108">设置机制取决于订阅和环境。</span><span class="sxs-lookup"><span data-stu-id="d17cc-108">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="d17cc-109">对于 Finance and Operations 应用的新实例，双写入连接的设置在 Microsoft Dynamics Lifecycle Services (LCS) 中开始。</span><span class="sxs-lookup"><span data-stu-id="d17cc-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="d17cc-110">如果您有 Microsoft Power Platform 的许可证，并且您的租户没有 Common Data Service 环境，您将获取一个新的该环境。</span><span class="sxs-lookup"><span data-stu-id="d17cc-110">If you have a license for Microsoft Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="d17cc-111">对于现有实例的 Finance and Operations 应用，双写入连接的设置在 Finance and Operations 环境中开始。</span><span class="sxs-lookup"><span data-stu-id="d17cc-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="d17cc-112">支持以下设置方案：</span><span class="sxs-lookup"><span data-stu-id="d17cc-112">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="d17cc-113">一个新 Finance and Operations 应用实例和一个新模型驱动应用实例</span><span class="sxs-lookup"><span data-stu-id="d17cc-113">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="d17cc-114">一个新 Finance and Operations 应用实例和一个现有模型驱动应用实例</span><span class="sxs-lookup"><span data-stu-id="d17cc-114">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="d17cc-115">一个具有演示数据的新 Finance and Operations 应用实例和一个新模型驱动应用实例</span><span class="sxs-lookup"><span data-stu-id="d17cc-115">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="d17cc-116">一个具有演示数据的新 Finance and Operations 应用实例和一个现有模型驱动应用实例</span><span class="sxs-lookup"><span data-stu-id="d17cc-116">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="d17cc-117">一个现有 Finance and Operations 应用实例和一个新的或现有模型驱动应用实例</span><span class="sxs-lookup"><span data-stu-id="d17cc-117">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="d17cc-118">一个新 Finance and Operations 应用实例和一个新模型驱动应用实例</span><span class="sxs-lookup"><span data-stu-id="d17cc-118">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="d17cc-119">若要在无数据的 Finance and Operations 应用新实例与 Dynamics 365 中的模型驱动应用新实例之间设置双写入连接，请执行[从 Lifecycle Services 设置双写入](lcs-setup.md)中的步骤。</span><span class="sxs-lookup"><span data-stu-id="d17cc-119">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="d17cc-120">完成连接设置之后，将自动执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="d17cc-120">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="d17cc-121">预配一个新的空 Finance and Operations 环境。</span><span class="sxs-lookup"><span data-stu-id="d17cc-121">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="d17cc-122">预配一个新的空模型驱动应用实例，其中已安装了 CRM 主解决方案。</span><span class="sxs-lookup"><span data-stu-id="d17cc-122">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="d17cc-123">为 DAT 公司数据建立双写入连接。</span><span class="sxs-lookup"><span data-stu-id="d17cc-123">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="d17cc-124">为实时同步启用实体映射。</span><span class="sxs-lookup"><span data-stu-id="d17cc-124">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="d17cc-125">然后，这两个环境准备好了进行实时数据同步。</span><span class="sxs-lookup"><span data-stu-id="d17cc-125">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a><span data-ttu-id="d17cc-126">一个新 Finance and Operations 应用实例和一个现有模型驱动应用实例</span><span class="sxs-lookup"><span data-stu-id="d17cc-126">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="d17cc-127">若要在无数据的 Finance and Operations 应用新实例与 Dynamics 365 中的模型驱动应用现有实例之间设置双写入连接，请执行[从 Lifecycle Services 设置双写入](lcs-setup.md)中的步骤。</span><span class="sxs-lookup"><span data-stu-id="d17cc-127">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="d17cc-128">完成连接设置之后，将自动执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="d17cc-128">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="d17cc-129">预配一个新的空 Finance and Operations 环境。</span><span class="sxs-lookup"><span data-stu-id="d17cc-129">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="d17cc-130">为 DAT 公司数据建立双写入连接。</span><span class="sxs-lookup"><span data-stu-id="d17cc-130">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="d17cc-131">为实时同步启用实体映射。</span><span class="sxs-lookup"><span data-stu-id="d17cc-131">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="d17cc-132">然后，这两个环境准备好了进行实时数据同步。</span><span class="sxs-lookup"><span data-stu-id="d17cc-132">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="d17cc-133">若要将现有 Common Data Service 数据同步到 Finance and Operations 应用，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="d17cc-133">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="d17cc-134">在 Finance and Operations 应用中创建一个新公司。</span><span class="sxs-lookup"><span data-stu-id="d17cc-134">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="d17cc-135">将该公司添加到双写入连接设置。</span><span class="sxs-lookup"><span data-stu-id="d17cc-135">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="d17cc-136">通过使用三个字母的国际标准化组织 (ISO) 公司代码[引导](bootstrap-company-data.md) Common Data Service 数据。</span><span class="sxs-lookup"><span data-stu-id="d17cc-136">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="d17cc-137">因为双写入处于实时同步模式，所以 Common Data Service 中的数据将自动开始流向 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="d17cc-137">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a><span data-ttu-id="d17cc-138">一个具有演示数据的新 Finance and Operations 应用实例和一个新模型驱动应用实例</span><span class="sxs-lookup"><span data-stu-id="d17cc-138">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="d17cc-139">若要在有演示数据的新 Finance and Operations 应用实例与 Dynamics 365 中的模型驱动应用新实例之间建立双写入连接，请执行此主题前文中[一个新 Finance and Operations 应用程序和一个新模型驱动应用实例](#new-new)部分中的步骤。</span><span class="sxs-lookup"><span data-stu-id="d17cc-139">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="d17cc-140">完成连接设置后，如果要将演示数据同步到模型驱动应用，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="d17cc-140">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="d17cc-141">从 LCS 页面打开 Finance and Operations 应用，然后转到**数据管理 \> 双写入**。</span><span class="sxs-lookup"><span data-stu-id="d17cc-141">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="d17cc-142">对要同步其数据的实体运行**初始同步**功能。</span><span class="sxs-lookup"><span data-stu-id="d17cc-142">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a><span data-ttu-id="d17cc-143">一个具有演示数据的新 Finance and Operations 应用实例和一个现有模型驱动应用实例</span><span class="sxs-lookup"><span data-stu-id="d17cc-143">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="d17cc-144">若要在有演示数据的新 Finance and Operations 应用实例与 Dynamics 365 中的模型驱动应用现有实例之间建立双写入连接，请执行此主题前文中[一个新 Finance and Operations 应用程序和一个现有模型驱动应用实例](#new-existing)部分中的步骤。</span><span class="sxs-lookup"><span data-stu-id="d17cc-144">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="d17cc-145">完成连接设置后，如果要将演示数据同步到模型驱动应用，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="d17cc-145">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="d17cc-146">从 LCS 页面打开 Finance and Operations 应用，然后转到**数据管理 \> 双写入**。</span><span class="sxs-lookup"><span data-stu-id="d17cc-146">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="d17cc-147">对要同步其数据的实体运行**初始同步**功能。</span><span class="sxs-lookup"><span data-stu-id="d17cc-147">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="d17cc-148">若要将现有 Common Data Service 数据同步到 Finance and Operations 应用，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="d17cc-148">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="d17cc-149">在 Finance and Operations 应用中创建一个新公司。</span><span class="sxs-lookup"><span data-stu-id="d17cc-149">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="d17cc-150">将该公司添加到双写入连接设置。</span><span class="sxs-lookup"><span data-stu-id="d17cc-150">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="d17cc-151">通过使用三个字母的 ISO 公司代码[引导](bootstrap-company-data.md) Common Data Service 数据。</span><span class="sxs-lookup"><span data-stu-id="d17cc-151">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="d17cc-152">因为双写入处于实时同步模式，所以 Common Data Service 中的数据将自动开始流向 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="d17cc-152">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="d17cc-153">一个现有 Finance and Operations 应用实例和一个新的或现有模型驱动应用实例</span><span class="sxs-lookup"><span data-stu-id="d17cc-153">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="d17cc-154">若要设置现有 Finance and Operations 应用实例与 Dynamics 365 中的模型驱动应用的新的或现有的实例之间的双写入连接，需要在 Finance and Operation 环境中进行。</span><span class="sxs-lookup"><span data-stu-id="d17cc-154">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="d17cc-155">从 Finance and Operations 应用设置连接。</span><span class="sxs-lookup"><span data-stu-id="d17cc-155">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="d17cc-156">若要将现有 Common Data Service 数据同步到 Finance and Operations 应用，请使用三个字母的 ISO 公司代码[引导](bootstrap-company-data.md) Common Data Service 数据。</span><span class="sxs-lookup"><span data-stu-id="d17cc-156">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="d17cc-157">因为双写入处于实时同步模式，所以 Common Data Service 中的数据将自动开始流向 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="d17cc-157">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>
