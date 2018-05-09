---
title: "供应商请求配置"
description: "此主题介绍在新供应商请求中必须填充的字段。"
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5610d1fc2adff0d04ea3931de4b1e23225e50ff0
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="vendor-request-configurations"></a><span data-ttu-id="4b8c3-103">供应商请求配置</span><span class="sxs-lookup"><span data-stu-id="4b8c3-103">Vendor request configurations</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b8c3-104">为了完成供应商请求，供应商联系人必须完成潜在供应商注册向导。</span><span class="sxs-lookup"><span data-stu-id="4b8c3-104">To complete a vendor request, a vendor contact person must complete the prospective vendor registration wizard.</span></span>

<span data-ttu-id="4b8c3-105">在**供应商请求配置**窗体中可以创建配置文件，以指定潜在供应商注册向导中的必填字段和显示字段。</span><span class="sxs-lookup"><span data-stu-id="4b8c3-105">In the **Vendor request configurations** form, you can create profiles that specify required fields and visible fields in the prospective vendor registration wizard.</span></span>

<span data-ttu-id="4b8c3-106">供应商注册向导将首先询问潜在供应商用户供应商开展经营所在的国家/地区。</span><span class="sxs-lookup"><span data-stu-id="4b8c3-106">The vendor registration wizard will start out by asking the prospective vendor user which country/region the vendor is doing business in.</span></span> <span data-ttu-id="4b8c3-107">此信息决定适用的配置。</span><span class="sxs-lookup"><span data-stu-id="4b8c3-107">This information determines the applicable configuration.</span></span> <span data-ttu-id="4b8c3-108">如果没有定义某个国家/地区的具体配置，将使用默认配置。</span><span class="sxs-lookup"><span data-stu-id="4b8c3-108">If no specific configuration is defined for a country/region, a default configuration will be used.</span></span>

### <a name="set-up-a-vendor-request-configuration"></a><span data-ttu-id="4b8c3-109">设置供应商请求配置</span><span class="sxs-lookup"><span data-stu-id="4b8c3-109">Set up a vendor request configuration</span></span>

<span data-ttu-id="4b8c3-110">默认情况下，在供应商请求配置窗体中提供了一个供应商配置。</span><span class="sxs-lookup"><span data-stu-id="4b8c3-110">By default, there is a vendor configuration available in the Vendor request configurations form.</span></span>

<span data-ttu-id="4b8c3-111">不能选择默认配置的国家/地区，因此无法更改**国家/地区**部分。</span><span class="sxs-lookup"><span data-stu-id="4b8c3-111">It is not possible to select country/regions for the default configuration, so the **Countries/regions** section cannot be changed.</span></span>

1. <span data-ttu-id="4b8c3-112">单击**采购** > **设置** > **供应商**，然后单击**供应商请求配置**。</span><span class="sxs-lookup"><span data-stu-id="4b8c3-112">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2. <span data-ttu-id="4b8c3-113">单击**字段**选项卡可以设置所列字段的状态。</span><span class="sxs-lookup"><span data-stu-id="4b8c3-113">Click the **Fields** tab to set the status of the listed fields.</span></span>
3. <span data-ttu-id="4b8c3-114">隐藏（不可见）</span><span class="sxs-lookup"><span data-stu-id="4b8c3-114">Hidden (Not visible)</span></span>
4. <span data-ttu-id="4b8c3-115">显示（可见但非必填）</span><span class="sxs-lookup"><span data-stu-id="4b8c3-115">Displayed (Visible but not mandatory)</span></span>
5. <span data-ttu-id="4b8c3-116">必填（可见且必填）</span><span class="sxs-lookup"><span data-stu-id="4b8c3-116">Required (Visible and mandatory)</span></span>
6. <span data-ttu-id="4b8c3-117">单击**内容**选项卡可指定文本是否要显示在向导上，以及是否应该确认潜在供应商用户必须接受后才能进入向导的下一步。</span><span class="sxs-lookup"><span data-stu-id="4b8c3-117">Click the **Content** tab to specify if text is going to be shown on the wizard and if there should be an acknowledgement that the prospective vendor user must accept this before moving to the next step in the wizard.</span></span> <span data-ttu-id="4b8c3-118">将针对用户必须接受后才能继续的任何条款和条件请求确认。</span><span class="sxs-lookup"><span data-stu-id="4b8c3-118">The acknowledgement will be requested for any terms and conditions that the user must accept to continue.</span></span>

<span data-ttu-id="4b8c3-119">您还可以输入在完成向导时将要显示的确认消息，并且可以添加一个或多个调查表。</span><span class="sxs-lookup"><span data-stu-id="4b8c3-119">You can also enter a confirmation message that will be displayed when the wizard is finalized, and you can add one or more questionnaires.</span></span>

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a><span data-ttu-id="4b8c3-120">为特定国家/地区创建供应商配置</span><span class="sxs-lookup"><span data-stu-id="4b8c3-120">Create a vendor configuration for a specific country/region</span></span>
1.  <span data-ttu-id="4b8c3-121">单击**采购** > **设置** > **供应商**，然后单击**供应商请求配置**。</span><span class="sxs-lookup"><span data-stu-id="4b8c3-121">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2.  <span data-ttu-id="4b8c3-122">单击**新建**以创建新的配置，然后为该配置提供一个名称。</span><span class="sxs-lookup"><span data-stu-id="4b8c3-122">Click **New** to create a new configuration, and provide a name for the configuration.</span></span>
3.  <span data-ttu-id="4b8c3-123">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="4b8c3-123">Click **Save**.</span></span>
4.  <span data-ttu-id="4b8c3-124">打开**国家/地区**选项卡以选择使用配置的国家/地区。</span><span class="sxs-lookup"><span data-stu-id="4b8c3-124">Open the **Country/regions** tab to select the country/region that the configuration should be used for.</span></span>
5.  <span data-ttu-id="4b8c3-125">按照以下默认配置指南完成配置。</span><span class="sxs-lookup"><span data-stu-id="4b8c3-125">Complete the configuration by following the guidelines for the default configuration.</span></span>


