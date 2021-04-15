---
title: 供应商请求配置
description: 此主题介绍在新供应商请求中必须填充的字段。
author: kamaybac
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: a78ec681ff9bfe9f7792da04553e4b543bf4a183
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809294"
---
# <a name="vendor-request-configurations"></a><span data-ttu-id="889bf-103">供应商请求配置</span><span class="sxs-lookup"><span data-stu-id="889bf-103">Vendor request configurations</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="889bf-104">为了完成供应商请求，供应商联系人必须完成潜在供应商注册向导。</span><span class="sxs-lookup"><span data-stu-id="889bf-104">To complete a vendor request, a vendor contact person must complete the prospective vendor registration wizard.</span></span>

<span data-ttu-id="889bf-105">在 **供应商请求配置** 窗体中可以创建配置文件，以指定潜在供应商注册向导中的必填字段和显示字段。</span><span class="sxs-lookup"><span data-stu-id="889bf-105">In the **Vendor request configurations** form, you can create profiles that specify required fields and visible fields in the prospective vendor registration wizard.</span></span>

<span data-ttu-id="889bf-106">供应商注册向导将首先询问潜在供应商用户供应商开展经营所在的国家/地区。</span><span class="sxs-lookup"><span data-stu-id="889bf-106">The vendor registration wizard will start out by asking the prospective vendor user which country/region the vendor is doing business in.</span></span> <span data-ttu-id="889bf-107">此信息决定适用的配置。</span><span class="sxs-lookup"><span data-stu-id="889bf-107">This information determines the applicable configuration.</span></span> <span data-ttu-id="889bf-108">如果没有定义某个国家/地区的具体配置，将使用默认配置。</span><span class="sxs-lookup"><span data-stu-id="889bf-108">If no specific configuration is defined for a country/region, a default configuration will be used.</span></span>

### <a name="set-up-a-vendor-request-configuration"></a><span data-ttu-id="889bf-109">设置供应商请求配置</span><span class="sxs-lookup"><span data-stu-id="889bf-109">Set up a vendor request configuration</span></span>

<span data-ttu-id="889bf-110">默认情况下，在供应商请求配置窗体中提供了一个供应商配置。</span><span class="sxs-lookup"><span data-stu-id="889bf-110">By default, there is a vendor configuration available in the Vendor request configurations form.</span></span>

<span data-ttu-id="889bf-111">不能选择默认配置的国家/地区，因此无法更改 **国家/地区** 部分。</span><span class="sxs-lookup"><span data-stu-id="889bf-111">It is not possible to select country/regions for the default configuration, so the **Countries/regions** section cannot be changed.</span></span>

1. <span data-ttu-id="889bf-112">单击 **采购** > **设置** > **供应商**，然后单击 **供应商请求配置**。</span><span class="sxs-lookup"><span data-stu-id="889bf-112">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2. <span data-ttu-id="889bf-113">单击 **字段** 选项卡可以设置所列字段的状态。</span><span class="sxs-lookup"><span data-stu-id="889bf-113">Click the **Fields** tab to set the status of the listed fields.</span></span>
3. <span data-ttu-id="889bf-114">隐藏（不可见）</span><span class="sxs-lookup"><span data-stu-id="889bf-114">Hidden (Not visible)</span></span>
4. <span data-ttu-id="889bf-115">显示（可见但非必填）</span><span class="sxs-lookup"><span data-stu-id="889bf-115">Displayed (Visible but not mandatory)</span></span>
5. <span data-ttu-id="889bf-116">必填（可见且必填）</span><span class="sxs-lookup"><span data-stu-id="889bf-116">Required (Visible and mandatory)</span></span>
6. <span data-ttu-id="889bf-117">单击 **内容** 选项卡可指定文本是否要显示在向导上，以及是否应该确认潜在供应商用户必须接受后才能进入向导的下一步。</span><span class="sxs-lookup"><span data-stu-id="889bf-117">Click the **Content** tab to specify if text is going to be shown on the wizard and if there should be an acknowledgement that the prospective vendor user must accept this before moving to the next step in the wizard.</span></span> <span data-ttu-id="889bf-118">将针对用户必须接受后才能继续的任何条款和条件请求确认。</span><span class="sxs-lookup"><span data-stu-id="889bf-118">The acknowledgement will be requested for any terms and conditions that the user must accept to continue.</span></span>

<span data-ttu-id="889bf-119">您还可以输入在完成向导时将要显示的确认消息，并且可以添加一个或多个调查表。</span><span class="sxs-lookup"><span data-stu-id="889bf-119">You can also enter a confirmation message that will be displayed when the wizard is finalized, and you can add one or more questionnaires.</span></span>

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a><span data-ttu-id="889bf-120">为特定国家/地区创建供应商配置</span><span class="sxs-lookup"><span data-stu-id="889bf-120">Create a vendor configuration for a specific country/region</span></span>
1.  <span data-ttu-id="889bf-121">单击 **采购** > **设置** > **供应商**，然后单击 **供应商请求配置**。</span><span class="sxs-lookup"><span data-stu-id="889bf-121">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2.  <span data-ttu-id="889bf-122">单击 **新建** 以创建新的配置，然后为该配置提供一个名称。</span><span class="sxs-lookup"><span data-stu-id="889bf-122">Click **New** to create a new configuration, and provide a name for the configuration.</span></span>
3.  <span data-ttu-id="889bf-123">单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="889bf-123">Click **Save**.</span></span>
4.  <span data-ttu-id="889bf-124">打开 **国家/地区** 选项卡以选择使用配置的国家/地区。</span><span class="sxs-lookup"><span data-stu-id="889bf-124">Open the **Country/regions** tab to select the country/region that the configuration should be used for.</span></span>
5.  <span data-ttu-id="889bf-125">按照以下默认配置指南完成配置。</span><span class="sxs-lookup"><span data-stu-id="889bf-125">Complete the configuration by following the guidelines for the default configuration.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]