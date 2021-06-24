---
title: 创建数据集成器项目（预览）
description: 此主题介绍如何创建数据集成器项目。
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 59f85c64ea7b1f539a245e08b76bd6a34797b0ca
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186460"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="3c218-103">创建数据集成器项目（预览）</span><span class="sxs-lookup"><span data-stu-id="3c218-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="3c218-104">此主题介绍如何创建数据集成器项目。</span><span class="sxs-lookup"><span data-stu-id="3c218-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="3c218-105">登录到 Microsoft Dynamics 365 Finance。</span><span class="sxs-lookup"><span data-stu-id="3c218-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="3c218-106">转到 **工作区 \> 数据管理**，然后选择 **数据实体**。</span><span class="sxs-lookup"><span data-stu-id="3c218-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="3c218-107">等至所有数据实体都已刷新，然后再继续下一步。</span><span class="sxs-lookup"><span data-stu-id="3c218-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="3c218-108">打开 [Power Apps 门户](https://make.powerapps.com/)，然后按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="3c218-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="3c218-109">选择相应环境。</span><span class="sxs-lookup"><span data-stu-id="3c218-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="3c218-110">在左侧导航窗格中，选择 **数据 \> 连接**。</span><span class="sxs-lookup"><span data-stu-id="3c218-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="3c218-111">连接到以下各项的相应实例：</span><span class="sxs-lookup"><span data-stu-id="3c218-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="3c218-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="3c218-112">Dynamics 365</span></span>
        - <span data-ttu-id="3c218-113">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="3c218-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="3c218-114">打开 [Power Apps 环境](https://admin.powerapps.com/environments)，然后按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="3c218-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="3c218-115">选择 **数据集成器**。</span><span class="sxs-lookup"><span data-stu-id="3c218-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="3c218-116">选择 **连接集**。</span><span class="sxs-lookup"><span data-stu-id="3c218-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="3c218-117">选择 **新建连接集**。</span><span class="sxs-lookup"><span data-stu-id="3c218-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="3c218-118">输入连接名称。</span><span class="sxs-lookup"><span data-stu-id="3c218-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="3c218-119">为以下项选择相应连接：</span><span class="sxs-lookup"><span data-stu-id="3c218-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="3c218-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="3c218-120">Dynamics 365</span></span>
        - <span data-ttu-id="3c218-121">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="3c218-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="3c218-122">选择相应组织映射。</span><span class="sxs-lookup"><span data-stu-id="3c218-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="3c218-123">选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="3c218-123">Select **Create**.</span></span>

5. <span data-ttu-id="3c218-124">打开 [Power Apps 环境](https://admin.powerapps.com/environments)，然后按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="3c218-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="3c218-125">通过使用刚创建的连接集，为以下模板创建数据集成项目：</span><span class="sxs-lookup"><span data-stu-id="3c218-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="3c218-126">客户付款见解结果（CDS 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="3c218-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
            - <span data-ttu-id="3c218-127">如果使用的是版本 10.0.17 或更高版本，则需要使用名为“客户付款见解结果（CDS 到 Fin and Ops 10.0.17+）”的模板。</span><span class="sxs-lookup"><span data-stu-id="3c218-127">If you are using version 10.0.17 or later, you need to use the template named, Customer payment insights result (CDS to Fin and Ops 10.0.17+).</span></span>
        - <span data-ttu-id="3c218-128">现金流时序结果（CDS 到 Fin 和 Ops）</span><span class="sxs-lookup"><span data-stu-id="3c218-128">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="3c218-129">预算时序结果（CDS 到 Fin 和 Ops）</span><span class="sxs-lookup"><span data-stu-id="3c218-129">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="3c218-130">为每个项目设置相应计划。</span><span class="sxs-lookup"><span data-stu-id="3c218-130">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="3c218-131">如果在 CDS 中未看到所需实体，请转到 **信用和收款 > 设置 > Finance Insights > Finance insights 参数**，启用客户付款预测功能，然后单击 **创建预测模型** 按钮。</span><span class="sxs-lookup"><span data-stu-id="3c218-131">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="3c218-132">当 AI 模型部署完成（成功或失败）后，将在 CDS 中部署创建集成所需的 CDS 实体。</span><span class="sxs-lookup"><span data-stu-id="3c218-132">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
