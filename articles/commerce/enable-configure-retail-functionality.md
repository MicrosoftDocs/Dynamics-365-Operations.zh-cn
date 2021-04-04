---
title: 初始化新 Commerce 环境中的种子数据
description: 本主题介绍 Dynamics 365 Commerce 的初始化流程期间创建的数据。
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a12bd7a178d8d40db8c919410a00fbf021625f50
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238742"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a><span data-ttu-id="ee7bd-103">初始化新 Commerce 环境中的种子数据</span><span class="sxs-lookup"><span data-stu-id="ee7bd-103">Initialize seed data in new Commerce environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ee7bd-104">本主题介绍 Dynamics 365 Commerce 的初始化流程期间创建的数据。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-104">This article describes the data that's created as part of the initialization process for Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ee7bd-105">在通过 Microsoft Dynamics Lifecycle Services (LCS) 部署商业解决方案后，您必须初始化商业配置以创建基本配置数据。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-105">After the Commerce solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the Commerce configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ee7bd-106">在初始化商业配置之前，请确保为您将设置商店的每个法人指定语言和邮政地址。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-106">Before you initialize the commerce configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up stores.</span></span> <span data-ttu-id="ee7bd-107">必须为您为商业使用的每个法人完成此步骤。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-107">This step must be completed for each legal entity that you use for commerce.</span></span>

<span data-ttu-id="ee7bd-108">若要初始化配置，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-108">To initialize the configuration, follow these steps.</span></span>

1. <span data-ttu-id="ee7bd-109">启动 Commerce 客户端。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-109">Start the Commerce client.</span></span>
2. <span data-ttu-id="ee7bd-110">单击 **Retail 和 Commerce** &gt; **总部设置** &gt; **参数** &gt; **商业参数**。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-110">Click **Retail and Commerce** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Commerce parameters**.</span></span>
3. <span data-ttu-id="ee7bd-111">单击 **初始化**。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-111">Click **Initialize**.</span></span>

<span data-ttu-id="ee7bd-112">初始化创建以下默认配置数据：</span><span class="sxs-lookup"><span data-stu-id="ee7bd-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="ee7bd-113">商业调度作业和子作业</span><span class="sxs-lookup"><span data-stu-id="ee7bd-113">Commerce scheduler jobs and subjobs</span></span>
- <span data-ttu-id="ee7bd-114">商业通道架构</span><span class="sxs-lookup"><span data-stu-id="ee7bd-114">Commerce channel schema</span></span>
- <span data-ttu-id="ee7bd-115">商业配送计划</span><span class="sxs-lookup"><span data-stu-id="ee7bd-115">Commerce distribution schedules</span></span>
- <span data-ttu-id="ee7bd-116">默认屏幕布局，包括按钮网格、图像和主题</span><span class="sxs-lookup"><span data-stu-id="ee7bd-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="ee7bd-117">时区信息</span><span class="sxs-lookup"><span data-stu-id="ee7bd-117">Time zone information</span></span>
- <span data-ttu-id="ee7bd-118">销售点 (POS) 操作</span><span class="sxs-lookup"><span data-stu-id="ee7bd-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="ee7bd-119">POS 权限</span><span class="sxs-lookup"><span data-stu-id="ee7bd-119">POS permissions</span></span>
- <span data-ttu-id="ee7bd-120">渠道报表</span><span class="sxs-lookup"><span data-stu-id="ee7bd-120">Channel reports</span></span>
- <span data-ttu-id="ee7bd-121">属性元数据</span><span class="sxs-lookup"><span data-stu-id="ee7bd-121">Attribute metadata</span></span>
- <span data-ttu-id="ee7bd-122">实体验证模板</span><span class="sxs-lookup"><span data-stu-id="ee7bd-122">Entity validation templates</span></span>
- <span data-ttu-id="ee7bd-123">清除 Commerce Data Exchange 会话历史记录的批处理作业</span><span class="sxs-lookup"><span data-stu-id="ee7bd-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="ee7bd-124">此外，为 Commerce 数据库启用了与支付卡行业 (PCI) 相关的日志记录。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Commerce database.</span></span>

> [!NOTE]
> <span data-ttu-id="ee7bd-125">具有单独配置商业调度的选项。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-125">There is an option to separately configure the Commerce scheduler.</span></span> <span data-ttu-id="ee7bd-126">此选项可以将商业调度配置重置为其默认设置。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-126">This option lets you reset the Commerce scheduler configuration to its default settings.</span></span>

<span data-ttu-id="ee7bd-127">在完成初始化后，必须配置附加的商业数据。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-127">After initialization is completed, you must configure additional commerce data.</span></span> <span data-ttu-id="ee7bd-128">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="ee7bd-128">Here are some examples:</span></span>

- <span data-ttu-id="ee7bd-129">商业参数</span><span class="sxs-lookup"><span data-stu-id="ee7bd-129">Commerce parameters</span></span>
- <span data-ttu-id="ee7bd-130">商业调度程序参数</span><span class="sxs-lookup"><span data-stu-id="ee7bd-130">Commerce scheduler parameters</span></span>
- <span data-ttu-id="ee7bd-131">商业渠道</span><span class="sxs-lookup"><span data-stu-id="ee7bd-131">Commerce channels</span></span>
- <span data-ttu-id="ee7bd-132">登记簿和设备</span><span class="sxs-lookup"><span data-stu-id="ee7bd-132">Registers and devices</span></span>
- <span data-ttu-id="ee7bd-133">分类</span><span class="sxs-lookup"><span data-stu-id="ee7bd-133">Assortments</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]