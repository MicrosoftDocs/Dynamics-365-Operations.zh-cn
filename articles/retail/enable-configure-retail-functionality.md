---
title: 初始化新 Retail 环境中的种子数据
description: 本主题介绍 Dynamics 365 Retail 的初始化流程期间创建的数据。
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
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 49b21d81437ebd7cc55076444ee71ae1143bfac0
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025508"
---
# <a name="initialize-seed-data-in-new-retail-environments"></a><span data-ttu-id="ec377-103">初始化新 Retail 环境中的种子数据</span><span class="sxs-lookup"><span data-stu-id="ec377-103">Initialize seed data in new Retail environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ec377-104">本主题介绍 Dynamics 365 Retail 的初始化流程期间创建的数据。</span><span class="sxs-lookup"><span data-stu-id="ec377-104">This article describes the data that's created as part of the initialization process for Dynamics 365 Retail.</span></span>

<span data-ttu-id="ec377-105">在通过 Microsoft Dynamics Lifecycle Services (LCS) 部署零售解决方案后，您必须初始化零售配置以创建基本配置数据。</span><span class="sxs-lookup"><span data-stu-id="ec377-105">After the Retail solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the retail configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ec377-106">在初始化零售配置之前，请确保为您将设置零售商店的每个法人指定语言和邮政地址。</span><span class="sxs-lookup"><span data-stu-id="ec377-106">Before you initialize the retail configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up retail stores.</span></span> <span data-ttu-id="ec377-107">必须为您为零售使用的每个法人完成此步骤。</span><span class="sxs-lookup"><span data-stu-id="ec377-107">This step must be completed for each legal entity that you use for retail.</span></span>

<span data-ttu-id="ec377-108">若要初始化零售配置，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="ec377-108">To initialize the retail configuration, follow these steps.</span></span>

1. <span data-ttu-id="ec377-109">启动 Retail 客户端。</span><span class="sxs-lookup"><span data-stu-id="ec377-109">Start the Retail client.</span></span>
2. <span data-ttu-id="ec377-110">单击**零售** &gt; **总部设置** &gt; **参数** &gt; **零售参数**。</span><span class="sxs-lookup"><span data-stu-id="ec377-110">Click **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.</span></span>
3. <span data-ttu-id="ec377-111">单击**初始化**。</span><span class="sxs-lookup"><span data-stu-id="ec377-111">Click **Initialize**.</span></span>

<span data-ttu-id="ec377-112">初始化创建以下默认配置数据：</span><span class="sxs-lookup"><span data-stu-id="ec377-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="ec377-113">零售调度作业和子作业</span><span class="sxs-lookup"><span data-stu-id="ec377-113">Retail scheduler jobs and subjobs</span></span>
- <span data-ttu-id="ec377-114">零售通道架构</span><span class="sxs-lookup"><span data-stu-id="ec377-114">Retail channel schema</span></span>
- <span data-ttu-id="ec377-115">零售配送计划</span><span class="sxs-lookup"><span data-stu-id="ec377-115">Retail distribution schedules</span></span>
- <span data-ttu-id="ec377-116">默认屏幕布局，包括按钮网格、图像和主题</span><span class="sxs-lookup"><span data-stu-id="ec377-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="ec377-117">时区信息</span><span class="sxs-lookup"><span data-stu-id="ec377-117">Time zone information</span></span>
- <span data-ttu-id="ec377-118">销售点 (POS) 操作</span><span class="sxs-lookup"><span data-stu-id="ec377-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="ec377-119">POS 权限</span><span class="sxs-lookup"><span data-stu-id="ec377-119">POS permissions</span></span>
- <span data-ttu-id="ec377-120">渠道报表</span><span class="sxs-lookup"><span data-stu-id="ec377-120">Channel reports</span></span>
- <span data-ttu-id="ec377-121">属性元数据</span><span class="sxs-lookup"><span data-stu-id="ec377-121">Attribute metadata</span></span>
- <span data-ttu-id="ec377-122">实体验证模板</span><span class="sxs-lookup"><span data-stu-id="ec377-122">Entity validation templates</span></span>
- <span data-ttu-id="ec377-123">清除 Commerce Data Exchange 会话历史记录的批处理作业</span><span class="sxs-lookup"><span data-stu-id="ec377-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="ec377-124">此外，与支付卡行业 (PCI) 相关的日志记录为 Retail 数据库启用。</span><span class="sxs-lookup"><span data-stu-id="ec377-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Retail database.</span></span>

> [!NOTE]
> <span data-ttu-id="ec377-125">具有单独配置零售调度的选项。</span><span class="sxs-lookup"><span data-stu-id="ec377-125">There is an option to separately configure the Retail scheduler.</span></span> <span data-ttu-id="ec377-126">此选项可以将零售调度配置重置为其默认设置。</span><span class="sxs-lookup"><span data-stu-id="ec377-126">This option lets you reset the Retail scheduler configuration to its default settings.</span></span>

<span data-ttu-id="ec377-127">在完成初始化后，必须配置附加的零售数据。</span><span class="sxs-lookup"><span data-stu-id="ec377-127">After initialization is completed, you must configure additional retail data.</span></span> <span data-ttu-id="ec377-128">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="ec377-128">Here are some examples:</span></span>

- <span data-ttu-id="ec377-129">零售参数</span><span class="sxs-lookup"><span data-stu-id="ec377-129">Retail parameters</span></span>
- <span data-ttu-id="ec377-130">零售调度参数设置</span><span class="sxs-lookup"><span data-stu-id="ec377-130">Retail scheduler parameters</span></span>
- <span data-ttu-id="ec377-131">零售渠道</span><span class="sxs-lookup"><span data-stu-id="ec377-131">Retail channels</span></span>
- <span data-ttu-id="ec377-132">登记簿和设备</span><span class="sxs-lookup"><span data-stu-id="ec377-132">Registers and devices</span></span>
- <span data-ttu-id="ec377-133">分类</span><span class="sxs-lookup"><span data-stu-id="ec377-133">Assortments</span></span>
