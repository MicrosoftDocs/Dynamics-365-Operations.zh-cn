---
title: "初始化新 Retail 环境中的种子数据"
description: "本主题介绍 Microsoft Dynamics 365 for Retail 的初始化流程期间创建的数据。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7388324fe8a9abc8fc3d723b7c8df2c73d76a2ae
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a><span data-ttu-id="a567e-103">初始化新 Retail 环境中的种子数据</span><span class="sxs-lookup"><span data-stu-id="a567e-103">Initialize seed data in a new Retail environment</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="a567e-104">本主题介绍 Microsoft Dynamics 365 for Retail 的初始化流程期间创建的数据。</span><span class="sxs-lookup"><span data-stu-id="a567e-104">This article describes the data that's created as part of the initialization process for Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="a567e-105">在通过 Microsoft Dynamics Lifecycle Services (LCS) 部署零售解决方案后，您必须初始化零售配置以创建基本配置数据。</span><span class="sxs-lookup"><span data-stu-id="a567e-105">After the Retail solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the retail configuration to create the basic configuration data.</span></span> <span data-ttu-id="a567e-106">**重要提示：**在初始化零售配置之前，请确保为您将设置零售商店的每个法人指定语言和邮政地址。</span><span class="sxs-lookup"><span data-stu-id="a567e-106">**Important:** Before you initialize the retail configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up retail stores.</span></span> <span data-ttu-id="a567e-107">必须为您为零售使用的每个法人完成此步骤。</span><span class="sxs-lookup"><span data-stu-id="a567e-107">This step must be completed for each legal entity that you use for retail.</span></span> <span data-ttu-id="a567e-108">若要初始化零售配置，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="a567e-108">To initialize the retail configuration, follow these steps.</span></span>

1.  <span data-ttu-id="a567e-109">启动 Dynamics 365 for Retail 客户端。</span><span class="sxs-lookup"><span data-stu-id="a567e-109">Start the Dynamics 365 for Retail client.</span></span>
2.  <span data-ttu-id="a567e-110">单击**零售** &gt; **总部设置** &gt; **参数** &gt; **零售参数**。</span><span class="sxs-lookup"><span data-stu-id="a567e-110">Click **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.</span></span>
3.  <span data-ttu-id="a567e-111">单击**初始化**。</span><span class="sxs-lookup"><span data-stu-id="a567e-111">Click **Initialize**.</span></span>

<span data-ttu-id="a567e-112">初始化创建以下默认配置数据：</span><span class="sxs-lookup"><span data-stu-id="a567e-112">Initialization creates the following default configuration data:</span></span>

-   <span data-ttu-id="a567e-113">零售调度作业和子作业</span><span class="sxs-lookup"><span data-stu-id="a567e-113">Retail scheduler jobs and subjobs</span></span>
-   <span data-ttu-id="a567e-114">零售通道架构</span><span class="sxs-lookup"><span data-stu-id="a567e-114">Retail channel schema</span></span>
-   <span data-ttu-id="a567e-115">零售配送计划</span><span class="sxs-lookup"><span data-stu-id="a567e-115">Retail distribution schedules</span></span>
-   <span data-ttu-id="a567e-116">默认屏幕布局，包括按钮网格、图像和主题</span><span class="sxs-lookup"><span data-stu-id="a567e-116">Default screen layouts, which include button grids, images, and themes</span></span>
-   <span data-ttu-id="a567e-117">时区信息</span><span class="sxs-lookup"><span data-stu-id="a567e-117">Time zone information</span></span>
-   <span data-ttu-id="a567e-118">销售点 (POS) 操作</span><span class="sxs-lookup"><span data-stu-id="a567e-118">Point-of-sale (POS) operations</span></span>
-   <span data-ttu-id="a567e-119">POS 权限</span><span class="sxs-lookup"><span data-stu-id="a567e-119">POS permissions</span></span>
-   <span data-ttu-id="a567e-120">渠道报表</span><span class="sxs-lookup"><span data-stu-id="a567e-120">Channel reports</span></span>
-   <span data-ttu-id="a567e-121">属性元数据</span><span class="sxs-lookup"><span data-stu-id="a567e-121">Attribute metadata</span></span>
-   <span data-ttu-id="a567e-122">实体验证模板</span><span class="sxs-lookup"><span data-stu-id="a567e-122">Entity validation templates</span></span>
-   <span data-ttu-id="a567e-123">清除商业数据交换的会话历史记录的批处理作业</span><span class="sxs-lookup"><span data-stu-id="a567e-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="a567e-124">此外，与支付卡行业 (PCI) 相关的日志记录为 Dynamics 365 for Retail 数据库启用。</span><span class="sxs-lookup"><span data-stu-id="a567e-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Dynamics 365 for Retail database.</span></span> <span data-ttu-id="a567e-125">**注意：**具有单独配置零售调度的选项。</span><span class="sxs-lookup"><span data-stu-id="a567e-125">**Note:** There is an option to separately configure the Retail scheduler.</span></span> <span data-ttu-id="a567e-126">此选项可以将零售调度配置重置为其默认设置。</span><span class="sxs-lookup"><span data-stu-id="a567e-126">This option lets you reset the Retail scheduler configuration to its default settings.</span></span> <span data-ttu-id="a567e-127">在完成初始化后，必须配置附加的零售数据。</span><span class="sxs-lookup"><span data-stu-id="a567e-127">After initialization is completed, you must configure additional retail data.</span></span> <span data-ttu-id="a567e-128">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="a567e-128">Here are some examples:</span></span>

-   <span data-ttu-id="a567e-129">零售参数</span><span class="sxs-lookup"><span data-stu-id="a567e-129">Retail parameters</span></span>
-   <span data-ttu-id="a567e-130">零售调度参数设置</span><span class="sxs-lookup"><span data-stu-id="a567e-130">Retail scheduler parameters</span></span>
-   <span data-ttu-id="a567e-131">零售渠道</span><span class="sxs-lookup"><span data-stu-id="a567e-131">Retail channels</span></span>
-   <span data-ttu-id="a567e-132">登记簿和设备</span><span class="sxs-lookup"><span data-stu-id="a567e-132">Registers and devices</span></span>
-   <span data-ttu-id="a567e-133">分类</span><span class="sxs-lookup"><span data-stu-id="a567e-133">Assortments</span></span>





