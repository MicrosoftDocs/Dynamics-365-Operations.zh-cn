---
title: Lifecycle Services 的双写入设置
description: 本主题说明如何从 Microsoft Dynamics Lifecycle Services (LCS) 设置双写入连接。
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: eb4170ef6cb09c862f6a4163670c519d5d8077fb
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103561"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="54427-103">Lifecycle Services 的双写入设置</span><span class="sxs-lookup"><span data-stu-id="54427-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="54427-104">本主题说明如何从 Microsoft Dynamics Lifecycle Services (LCS) 启用双写入。</span><span class="sxs-lookup"><span data-stu-id="54427-104">This topic explains how to enable dual-write from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="54427-105">先决条件</span><span class="sxs-lookup"><span data-stu-id="54427-105">Prerequisites</span></span>

<span data-ttu-id="54427-106">您必须按照以下主题中所述完成 Power Platform 集成：</span><span class="sxs-lookup"><span data-stu-id="54427-106">You must complete the Power Platform integration as described in the following topics:</span></span>

+ [<span data-ttu-id="54427-107">Power Platform 集成 - 在环境部署期间启用</span><span class="sxs-lookup"><span data-stu-id="54427-107">Power Platform Integration - Enable during environment deployment</span></span>](../../power-platform/overview.md#enable-during-environment-deployment)
+ [<span data-ttu-id="54427-108">Power Platform 集成 - 在环境部署后设置</span><span class="sxs-lookup"><span data-stu-id="54427-108">Power Platform integration - Set up after environment deployment</span></span>](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a><span data-ttu-id="54427-109">为新 Dataverse 环境设置双写入</span><span class="sxs-lookup"><span data-stu-id="54427-109">Set up dual-write for new Dataverse environments</span></span>

<span data-ttu-id="54427-110">按照以下步骤从 LCS **环境详细信息** 页设置双写入：</span><span class="sxs-lookup"><span data-stu-id="54427-110">Follow these steps to set up dual-write from LCS **Environment Details** page:</span></span>

1. <span data-ttu-id="54427-111">在 **环境详细信息** 页上，展开 **Power Platform 集成** 部分。</span><span class="sxs-lookup"><span data-stu-id="54427-111">On the **Environment Details** page, expand the **Power Platform Integration** section.</span></span>

2. <span data-ttu-id="54427-112">选择 **双写入应用程序** 按钮。</span><span class="sxs-lookup"><span data-stu-id="54427-112">Select the **Dual-write application** button.</span></span>

    ![Power Platform 集成](media/powerplat_integration_step2.png)

3. <span data-ttu-id="54427-114">查看条款和条件，然后选择 **配置**。</span><span class="sxs-lookup"><span data-stu-id="54427-114">Review the terms and conditions, and then select **Configure**.</span></span>

4. <span data-ttu-id="54427-115">选择 **确定** 继续。</span><span class="sxs-lookup"><span data-stu-id="54427-115">Select **OK** to continue.</span></span>

5. <span data-ttu-id="54427-116">您可以通过定期刷新环境详细信息页来监视进度。</span><span class="sxs-lookup"><span data-stu-id="54427-116">You can monitor the progress by periodically refreshing the environment details page.</span></span> <span data-ttu-id="54427-117">设置通常需要 30 分钟或更短时间。</span><span class="sxs-lookup"><span data-stu-id="54427-117">Setup typically takes 30 minutes or less.</span></span>  

6. <span data-ttu-id="54427-118">设置完成后，一条消息将通知您过程是成功还是失败。</span><span class="sxs-lookup"><span data-stu-id="54427-118">When the setup is complete, a message will inform you if the process was successful or if there was a failure.</span></span> <span data-ttu-id="54427-119">如果设置失败，会显示相关的错误消息。</span><span class="sxs-lookup"><span data-stu-id="54427-119">If the setup failed, then a related error message is displayed.</span></span> <span data-ttu-id="54427-120">您必须解决所有错误，然后再进行下一步。</span><span class="sxs-lookup"><span data-stu-id="54427-120">You must fix any errors before moving to the next step.</span></span>

7. <span data-ttu-id="54427-121">选择 **链接到 Power Platform 环境** 在 Dataverse 和当前环境的数据库之间创建链接。</span><span class="sxs-lookup"><span data-stu-id="54427-121">Select **Link to Power Platform environment** to create a link between Dataverse and the current environment's databases.</span></span> <span data-ttu-id="54427-122">这通常需要不到 5 分钟时间。</span><span class="sxs-lookup"><span data-stu-id="54427-122">This typically takes less than 5 minutes.</span></span>

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="链接到 Power Platform 环境":::

8. <span data-ttu-id="54427-124">链接完成后，将显示一个超链接。</span><span class="sxs-lookup"><span data-stu-id="54427-124">When the linking is complete, a hyperlink is displayed.</span></span> <span data-ttu-id="54427-125">使用此链接登录到 Finance and Operations 环境中的双写入管理区域。</span><span class="sxs-lookup"><span data-stu-id="54427-125">Use the link to sign in to the dual-write administration area in the Finance and Operations environment.</span></span> <span data-ttu-id="54427-126">从那里，您可以设置实体映射。</span><span class="sxs-lookup"><span data-stu-id="54427-126">From there, you can set up entity mappings.</span></span>

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a><span data-ttu-id="54427-127">为现有 Dataverse 环境设置双写入</span><span class="sxs-lookup"><span data-stu-id="54427-127">Set up dual-write for an existing Dataverse environment</span></span>

<span data-ttu-id="54427-128">要为现有 Dataverse 环境设置双写入，必须创建 Microsoft [支持票证](../../lifecycle-services/lcs-support.md)。</span><span class="sxs-lookup"><span data-stu-id="54427-128">To set up dual-write for an existing Dataverse environment, you must create a Microsoft [support ticket](../../lifecycle-services/lcs-support.md).</span></span> <span data-ttu-id="54427-129">票证必须包括：</span><span class="sxs-lookup"><span data-stu-id="54427-129">The ticket must include:</span></span>

+ <span data-ttu-id="54427-130">您的 Finance and Operations 环境 ID。</span><span class="sxs-lookup"><span data-stu-id="54427-130">Your Finance and Operations environment ID.</span></span>
+ <span data-ttu-id="54427-131">Lifecycle Services 中的环境名称。</span><span class="sxs-lookup"><span data-stu-id="54427-131">Your environment name from Lifecycle Services.</span></span>
+ <span data-ttu-id="54427-132">来自 Power Platform 管理中心的 Dataverse 组织 ID 或 Power Platform 环境 ID。</span><span class="sxs-lookup"><span data-stu-id="54427-132">The Dataverse organization ID or Power Platform Environment ID from Power Platform Admin Center.</span></span> <span data-ttu-id="54427-133">在您的票证中，要求 ID 是用于 Power Platform 集成的实例。</span><span class="sxs-lookup"><span data-stu-id="54427-133">In your ticket, request that the ID be the instance used for Power Platform integration.</span></span>

> [!NOTE]
> <span data-ttu-id="54427-134">不能使用 LCS 取消链接环境。</span><span class="sxs-lookup"><span data-stu-id="54427-134">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="54427-135">若要取消链接环境，请在 Finance and Operations 环境中打开 **数据集成** 工作区，然后选择 **取消链接**。</span><span class="sxs-lookup"><span data-stu-id="54427-135">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
