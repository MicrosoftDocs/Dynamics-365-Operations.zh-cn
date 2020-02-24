---
title: 在供应商设计之间切换
description: 本主题介绍如何在 Finance and Operations 应用与 Common Data Service 之间的供应商数据集成之间切换。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
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
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 587a9b98f28b11e303aff4b59e9726f220d956eb
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019653"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="afd59-103">在供应商设计之间切换</span><span class="sxs-lookup"><span data-stu-id="afd59-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="afd59-104">供应商数据流</span><span class="sxs-lookup"><span data-stu-id="afd59-104">Vendor data flow</span></span> 

<span data-ttu-id="afd59-105">如果您使用其他 Dynamics 365 应用进行供应商主控，并且希望隔离供应商信息与客户信息，请使用此基本供应商设计。</span><span class="sxs-lookup"><span data-stu-id="afd59-105">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![基本供应商流](media/dual-write-vendor-data-flow.png)
 
<span data-ttu-id="afd59-107">如果您使用其他 Dynamics 365 应用进行供应商主控，并且希望继续使用**客户**实体存储供应商信息，请使用此扩展供应商设计。</span><span class="sxs-lookup"><span data-stu-id="afd59-107">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="afd59-108">在此设计中，扩展的供应商信息（如供应商暂停状态和供应商配置文件）存储在 Common Data Service 中的**供应商**实体中。</span><span class="sxs-lookup"><span data-stu-id="afd59-108">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![扩展供应商流](media/dual-write-vendor-detail.jpg)
 
<span data-ttu-id="afd59-110">请按照以下步骤使用扩展供应商设计：</span><span class="sxs-lookup"><span data-stu-id="afd59-110">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="afd59-111">**SupplyChainCommon** 解决方案包包含工作流程模板，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="afd59-111">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="afd59-112">![工作流程模板](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="afd59-112">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="afd59-113">使用工作流程模板创建新的工作流程：</span><span class="sxs-lookup"><span data-stu-id="afd59-113">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="afd59-114">使用**在客户实体中创建供应商**工作流程模板为**供应商**实体创建新的工作流程，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="afd59-114">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="afd59-115">此工作流处理**客户**实体的供应商创建方案。</span><span class="sxs-lookup"><span data-stu-id="afd59-115">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="afd59-116">![在客户实体中创建供应商](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="afd59-116">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="afd59-117">使用**更新客户实体**工作流程模板为**供应商**实体创建新的工作流程，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="afd59-117">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="afd59-118">此工作流处理**客户**实体的供应商更新方案。</span><span class="sxs-lookup"><span data-stu-id="afd59-118">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="afd59-119">![更新客户实体](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="afd59-119">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="afd59-120">从在**客户**实体上创建的模板创建新工作流程。</span><span class="sxs-lookup"><span data-stu-id="afd59-120">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="afd59-121">![在供应商实体中创建供应商](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="afd59-121">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="afd59-122">![更新供应商实体](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="afd59-122">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="afd59-123">您可以根据需要将工作流配置为实时或后台工作流。</span><span class="sxs-lookup"><span data-stu-id="afd59-123">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="afd59-124">![转换为后台工作流程](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="afd59-124">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="afd59-125">启用您在**客户**和**供应商**实体上创建的工作流，以开始使用**客户**实体存储供应商信息。</span><span class="sxs-lookup"><span data-stu-id="afd59-125">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the **Account** entity for storing vendor information.</span></span> 
 
