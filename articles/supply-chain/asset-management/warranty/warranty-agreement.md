---
title: 保修协议
description: 本主题介绍资产管理中的保修协议。
author: josaw1
manager: AnnBe
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 71905d5b362c80d48b78210b59cacfb1e7899757
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874685"
---
# <a name="warranty-agreements"></a><span data-ttu-id="05507-103">保修协议</span><span class="sxs-lookup"><span data-stu-id="05507-103">Warranty agreements</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="05507-104">在资产管理中，可以设置应用于资产或资产类型的保修条款。</span><span class="sxs-lookup"><span data-stu-id="05507-104">In Asset Management, you can set up warranty terms that can be connected to an asset or an asset type.</span></span> <span data-ttu-id="05507-105">保修条款是为特定期间创建的。</span><span class="sxs-lookup"><span data-stu-id="05507-105">Warranty terms are created for a specific period.</span></span> <span data-ttu-id="05507-106">设置的保修可以提供完全覆盖，也可以提供部分覆盖，您可以设置与工时、费用和物料关联的条款。</span><span class="sxs-lookup"><span data-stu-id="05507-106">Warranty can be set up to provide full coverage or partial coverage, and you can set up terms that are related to hours, expenses, and items.</span></span>

<span data-ttu-id="05507-107">第一步是创建适用于您的设备的任何供应商保修协议。</span><span class="sxs-lookup"><span data-stu-id="05507-107">The first step is to create any vendor warranty agreements that you have for your equipment.</span></span> <span data-ttu-id="05507-108">然后将保修协议与资产或资产类型关联。</span><span class="sxs-lookup"><span data-stu-id="05507-108">You then attach warranty agreements to assets or asset types.</span></span> <span data-ttu-id="05507-109">供应商保修协议仅用于参考。</span><span class="sxs-lookup"><span data-stu-id="05507-109">Vendor warranty agreements are used only for informational purposes.</span></span> <span data-ttu-id="05507-110">如果为资产设置了供应商保修，则可查看该资产的保修覆盖期间。</span><span class="sxs-lookup"><span data-stu-id="05507-110">If vendor warranty is set up on an asset, you can see the warranty coverage period on the asset.</span></span>

## <a name="create-a-warranty-agreement"></a><span data-ttu-id="05507-111">创建保修协议</span><span class="sxs-lookup"><span data-stu-id="05507-111">Create a warranty agreement</span></span>

<span data-ttu-id="05507-112">一个保修协议中包含多个协议行，以便覆盖工作时间、费用和物料的保修。</span><span class="sxs-lookup"><span data-stu-id="05507-112">A warranty agreement can include several agreement lines to cover the warranty for work hours, expenses, and items.</span></span>

1. <span data-ttu-id="05507-113">选择**资产管理** \> **设置** \> **资产** \> **保修**。</span><span class="sxs-lookup"><span data-stu-id="05507-113">Select **Asset management** \> **Setup** \> **Assets** \> **Warranty**.</span></span>
2. <span data-ttu-id="05507-114">选择**新建**创建产品。</span><span class="sxs-lookup"><span data-stu-id="05507-114">Select **New** to create a product.</span></span>
3. <span data-ttu-id="05507-115">在**保修**字段中，输入保修 ID。</span><span class="sxs-lookup"><span data-stu-id="05507-115">In the **Warranty** field, enter a warranty ID.</span></span>
4. <span data-ttu-id="05507-116">在**名称**字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="05507-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="05507-117">**详细信息**快速选项卡上的**资产**字段显示使用保修协议的有效资产的数量。</span><span class="sxs-lookup"><span data-stu-id="05507-117">On the **Details** FastTab, the **Assets** field shows the number of active assets that use the warranty agreement.</span></span>

5. <span data-ttu-id="05507-118">在**工时保修**和**物料保修**快速选项卡上，执行以下步骤添加保修协议中应该包含的与工时或物料有关的行：</span><span class="sxs-lookup"><span data-stu-id="05507-118">On the **Hour warranty** and **Item warranty** FastTabs, follow these steps to add lines that should be included in a warranty agreement that pertains to hours or items:</span></span>

    1. <span data-ttu-id="05507-119">选择**添加行**，向保修添加新条件。</span><span class="sxs-lookup"><span data-stu-id="05507-119">Select **Add line** to add a new condition to the warranty.</span></span> <span data-ttu-id="05507-120">将在**行**字段中输入连续的行号。</span><span class="sxs-lookup"><span data-stu-id="05507-120">A sequential line number is automatically entered in the **Line** field.</span></span>
    2. <span data-ttu-id="05507-121">在**期间**字段中，选择保修期的类型。</span><span class="sxs-lookup"><span data-stu-id="05507-121">In the **Period** field, select the type of warranty period.</span></span>
    3. <span data-ttu-id="05507-122">在**间隔**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="05507-122">In the **Interval** field, enter a number.</span></span> <span data-ttu-id="05507-123">此字段定义保修的有效期间数量。</span><span class="sxs-lookup"><span data-stu-id="05507-123">This field defines the number of periods that the warranty should be valid for.</span></span>
    4. <span data-ttu-id="05507-124">在**百分比**字段中，输入保修行的覆盖百分比。</span><span class="sxs-lookup"><span data-stu-id="05507-124">In the **Percent** field, enter the coverage percentage for the warranty line.</span></span> <span data-ttu-id="05507-125">此百分比指示公司涵盖的量。</span><span class="sxs-lookup"><span data-stu-id="05507-125">The percentage indicates how much is covered by your company.</span></span>

![图 1](media/01-warranty.png)
