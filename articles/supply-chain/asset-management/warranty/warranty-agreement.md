---
title: 保修协议
description: 本主题介绍资产管理中的保修协议。
author: josaw1
manager: tfehr
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7080af2059c9c9bcdd11ca0ee9c5e339cef69302
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021496"
---
# <a name="warranty-agreements"></a><span data-ttu-id="c48a9-103">保修协议</span><span class="sxs-lookup"><span data-stu-id="c48a9-103">Warranty agreements</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="c48a9-104">在资产管理中，可以设置应用于资产或资产类型的保修条款。</span><span class="sxs-lookup"><span data-stu-id="c48a9-104">In Asset Management, you can set up warranty terms that can be connected to an asset or an asset type.</span></span> <span data-ttu-id="c48a9-105">保修条款是为特定期间创建的。</span><span class="sxs-lookup"><span data-stu-id="c48a9-105">Warranty terms are created for a specific period.</span></span> <span data-ttu-id="c48a9-106">设置的保修可以提供完全覆盖，也可以提供部分覆盖，您可以设置与工时、费用和物料关联的条款。</span><span class="sxs-lookup"><span data-stu-id="c48a9-106">Warranty can be set up to provide full coverage or partial coverage, and you can set up terms that are related to hours, expenses, and items.</span></span>

<span data-ttu-id="c48a9-107">第一步是创建适用于您的设备的任何供应商保修协议。</span><span class="sxs-lookup"><span data-stu-id="c48a9-107">The first step is to create any vendor warranty agreements that you have for your equipment.</span></span> <span data-ttu-id="c48a9-108">然后将保修协议与资产或资产类型关联。</span><span class="sxs-lookup"><span data-stu-id="c48a9-108">You then attach warranty agreements to assets or asset types.</span></span> <span data-ttu-id="c48a9-109">供应商保修协议仅用于参考。</span><span class="sxs-lookup"><span data-stu-id="c48a9-109">Vendor warranty agreements are used only for informational purposes.</span></span> <span data-ttu-id="c48a9-110">如果为资产设置了供应商保修，则可查看该资产的保修覆盖期间。</span><span class="sxs-lookup"><span data-stu-id="c48a9-110">If vendor warranty is set up on an asset, you can see the warranty coverage period on the asset.</span></span>

## <a name="create-a-warranty-agreement"></a><span data-ttu-id="c48a9-111">创建保修协议</span><span class="sxs-lookup"><span data-stu-id="c48a9-111">Create a warranty agreement</span></span>

<span data-ttu-id="c48a9-112">一个保修协议中包含多个协议行，以便覆盖工作时间、费用和物料的保修。</span><span class="sxs-lookup"><span data-stu-id="c48a9-112">A warranty agreement can include several agreement lines to cover the warranty for work hours, expenses, and items.</span></span>

1. <span data-ttu-id="c48a9-113">选择 **资产管理** \> **设置** \> **资产** \> **保修**。</span><span class="sxs-lookup"><span data-stu-id="c48a9-113">Select **Asset management** \> **Setup** \> **Assets** \> **Warranty**.</span></span>
2. <span data-ttu-id="c48a9-114">选择 **新建** 创建产品。</span><span class="sxs-lookup"><span data-stu-id="c48a9-114">Select **New** to create a product.</span></span>
3. <span data-ttu-id="c48a9-115">在 **保修** 字段中，输入保修 ID。</span><span class="sxs-lookup"><span data-stu-id="c48a9-115">In the **Warranty** field, enter a warranty ID.</span></span> 
4. <span data-ttu-id="c48a9-116">在 **名称** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="c48a9-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="c48a9-117">**详细信息** 快速选项卡上的 **资产** 字段显示使用保修协议的有效资产的数量。</span><span class="sxs-lookup"><span data-stu-id="c48a9-117">On the **Details** FastTab, the **Assets** field shows the number of active assets that use the warranty agreement.</span></span>

5. <span data-ttu-id="c48a9-118">在 **保修行** 快速选项卡上，按照以下步骤添加应包含在保修协议中的行：</span><span class="sxs-lookup"><span data-stu-id="c48a9-118">On the **Warranty lines** FastTab, follow these steps to add lines that should be included in a warranty agreement:</span></span>

    1. <span data-ttu-id="c48a9-119">选择 **添加行**，向保修添加新条件。</span><span class="sxs-lookup"><span data-stu-id="c48a9-119">Select **Add line** to add a new condition to the warranty.</span></span> <span data-ttu-id="c48a9-120">将在 **行** 字段中输入连续的行号。</span><span class="sxs-lookup"><span data-stu-id="c48a9-120">A sequential line number is automatically entered in the **Line** field.</span></span>
    2. <span data-ttu-id="c48a9-121">在 **期间** 字段中，选择保修期的类型。</span><span class="sxs-lookup"><span data-stu-id="c48a9-121">In the **Period** field, select the type of warranty period.</span></span>
    3. <span data-ttu-id="c48a9-122">在 **间隔** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="c48a9-122">In the **Interval** field, enter a number.</span></span> <span data-ttu-id="c48a9-123">此字段定义保修的有效期间数量。</span><span class="sxs-lookup"><span data-stu-id="c48a9-123">This field defines the number of periods that the warranty should be valid for.</span></span>
    4. <span data-ttu-id="c48a9-124">在 **百分比** 字段中，输入保修行的覆盖百分比。</span><span class="sxs-lookup"><span data-stu-id="c48a9-124">In the **Percent** field, enter the coverage percentage for the warranty line.</span></span> <span data-ttu-id="c48a9-125">此百分比指示公司涵盖的量。</span><span class="sxs-lookup"><span data-stu-id="c48a9-125">The percentage indicates how much is covered by your company.</span></span>

![保修页面](media/01-warranty.png)
