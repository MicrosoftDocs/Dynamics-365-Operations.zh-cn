---
title: 创建数据集成器项目（预览）
description: 此主题介绍如何创建数据集成器项目。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 050c4f0fe1aea07c3866e2e9d7a6db6c758205ca
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208501"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="91ba5-103">创建数据集成器项目（预览）</span><span class="sxs-lookup"><span data-stu-id="91ba5-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="91ba5-104">此主题介绍如何创建数据集成器项目。</span><span class="sxs-lookup"><span data-stu-id="91ba5-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="91ba5-105">登录到 Microsoft Dynamics 365 Finance。</span><span class="sxs-lookup"><span data-stu-id="91ba5-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="91ba5-106">转到 **工作区 \> 数据管理**，然后选择 **数据实体**。</span><span class="sxs-lookup"><span data-stu-id="91ba5-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="91ba5-107">等至所有数据实体都已刷新，然后再继续下一步。</span><span class="sxs-lookup"><span data-stu-id="91ba5-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="91ba5-108">打开 [Power Apps 门户](https://make.powerapps.com/)，然后按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="91ba5-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="91ba5-109">选择相应环境。</span><span class="sxs-lookup"><span data-stu-id="91ba5-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="91ba5-110">在左侧导航窗格中，选择 **数据 \> 连接**。</span><span class="sxs-lookup"><span data-stu-id="91ba5-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="91ba5-111">连接到以下各项的相应实例：</span><span class="sxs-lookup"><span data-stu-id="91ba5-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="91ba5-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="91ba5-112">Dynamics 365</span></span>
        - <span data-ttu-id="91ba5-113">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="91ba5-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="91ba5-114">打开 [Power Apps 环境](https://admin.powerapps.com/environments)，然后按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="91ba5-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="91ba5-115">选择 **数据集成器**。</span><span class="sxs-lookup"><span data-stu-id="91ba5-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="91ba5-116">选择 **连接集**。</span><span class="sxs-lookup"><span data-stu-id="91ba5-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="91ba5-117">选择 **新建连接集**。</span><span class="sxs-lookup"><span data-stu-id="91ba5-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="91ba5-118">输入连接名称。</span><span class="sxs-lookup"><span data-stu-id="91ba5-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="91ba5-119">为以下项选择相应连接：</span><span class="sxs-lookup"><span data-stu-id="91ba5-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="91ba5-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="91ba5-120">Dynamics 365</span></span>
        - <span data-ttu-id="91ba5-121">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="91ba5-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="91ba5-122">选择相应组织映射。</span><span class="sxs-lookup"><span data-stu-id="91ba5-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="91ba5-123">选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="91ba5-123">Select **Create**.</span></span>

5. <span data-ttu-id="91ba5-124">打开 [Power Apps 环境](https://admin.powerapps.com/environments)，然后按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="91ba5-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="91ba5-125">通过使用刚创建的连接集，为以下模板创建数据集成项目：</span><span class="sxs-lookup"><span data-stu-id="91ba5-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="91ba5-126">客户付款见解结果（CDS 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="91ba5-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="91ba5-127">现金流时序结果（CDS 到 Fin 和 Ops）</span><span class="sxs-lookup"><span data-stu-id="91ba5-127">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="91ba5-128">预算时序结果（CDS 到 Fin 和 Ops）</span><span class="sxs-lookup"><span data-stu-id="91ba5-128">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="91ba5-129">为每个项目设置相应计划。</span><span class="sxs-lookup"><span data-stu-id="91ba5-129">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="91ba5-130">如果在 CDS 中未看到所需实体，请转到 **信用和收款 > 设置 > Finance Insights > Finance insights 参数**，启用客户付款预测功能，然后单击 **创建预测模型** 按钮。</span><span class="sxs-lookup"><span data-stu-id="91ba5-130">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="91ba5-131">当 AI 模型部署完成（成功或失败）后，将在 CDS 中部署创建集成所需的 CDS 实体。</span><span class="sxs-lookup"><span data-stu-id="91ba5-131">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="91ba5-132">隐私声明</span><span class="sxs-lookup"><span data-stu-id="91ba5-132">Privacy notice</span></span>

<span data-ttu-id="91ba5-133">预览版 (1) 采用的隐私和安全措施可能比 Dynamics 365 Finance and Operations 服务少，(2) 不包含在该服务的服务级别协议 (SLA) 中，(3) 不应用于处理应遵守法律或法规合规性要求的个人数据或其他数据，以及 (4) 享受有限支持。</span><span class="sxs-lookup"><span data-stu-id="91ba5-133">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]