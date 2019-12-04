---
title: 在供应商设计之间切换
description: ''
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
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772356"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="b2894-102">在供应商设计之间切换</span><span class="sxs-lookup"><span data-stu-id="b2894-102">Switch between vendor designs</span></span>

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="b2894-103">供应商数据流</span><span class="sxs-lookup"><span data-stu-id="b2894-103">Vendor data flow</span></span> 

<span data-ttu-id="b2894-104">如果您使用其他 Dynamics 365 应用进行供应商主控，并且希望隔离供应商信息与客户信息，请使用此基本供应商设计。</span><span class="sxs-lookup"><span data-stu-id="b2894-104">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![基本供应商流](media/dual-write-switch-1.png)
 
<span data-ttu-id="b2894-106">如果您使用其他 Dynamics 365 应用进行供应商主控，并且希望继续使用**客户**实体存储供应商信息，请使用此扩展供应商设计。</span><span class="sxs-lookup"><span data-stu-id="b2894-106">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="b2894-107">在此设计中，扩展的供应商信息（如供应商暂停状态和供应商配置文件）存储在 Common Data Service 中的**供应商**实体中。</span><span class="sxs-lookup"><span data-stu-id="b2894-107">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![扩展供应商流](media/dual-write-switch-2.png)
 
<span data-ttu-id="b2894-109">请按照以下步骤使用扩展供应商设计：</span><span class="sxs-lookup"><span data-stu-id="b2894-109">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="b2894-110">**SupplyChainCommon** 解决方案包包含工作流程模板，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="b2894-110">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="b2894-111">![工作流程模板](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="b2894-111">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="b2894-112">使用工作流程模板创建新的工作流程：</span><span class="sxs-lookup"><span data-stu-id="b2894-112">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="b2894-113">使用**在客户实体中创建供应商**工作流程模板为**供应商**实体创建新的工作流程，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="b2894-113">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="b2894-114">此工作流处理**客户**实体的供应商创建方案。</span><span class="sxs-lookup"><span data-stu-id="b2894-114">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="b2894-115">![在客户实体中创建供应商](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="b2894-115">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="b2894-116">使用**更新客户实体**工作流程模板为**供应商**实体创建新的工作流程，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="b2894-116">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="b2894-117">此工作流处理**客户**实体的供应商更新方案。</span><span class="sxs-lookup"><span data-stu-id="b2894-117">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="b2894-118">![更新客户实体](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="b2894-118">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="b2894-119">从在**客户**实体上创建的模板创建新工作流程。</span><span class="sxs-lookup"><span data-stu-id="b2894-119">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="b2894-120">![在供应商实体中创建供应商](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="b2894-120">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="b2894-121">![更新供应商实体](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="b2894-121">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="b2894-122">您可以根据需要将工作流配置为实时或后台工作流。</span><span class="sxs-lookup"><span data-stu-id="b2894-122">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="b2894-123">![转换为后台工作流程](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="b2894-123">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="b2894-124">启用您在**客户**和**供应商**实体上创建的工作流，以开始使用 Customer Engagement **客户**实体存储供应商信息。</span><span class="sxs-lookup"><span data-stu-id="b2894-124">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the Customer Engagement **Account** entity for storing vendor information.</span></span> 
 
