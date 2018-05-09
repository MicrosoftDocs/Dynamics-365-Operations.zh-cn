--- 
title: "输入对固定资产的添加件"
description: "本流程展示如何对现有固定资产表添加新的成员。"
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5e5d45f15b69310b5b03a0a9093c1bd0e5647bcd
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---
# <a name="enter-an-addition-to-a-fixed-asset"></a><span data-ttu-id="41c22-103">输入对固定资产的添加件</span><span class="sxs-lookup"><span data-stu-id="41c22-103">Enter an addition to a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="41c22-104">本流程展示如何对现有固定资产表添加新的成员。</span><span class="sxs-lookup"><span data-stu-id="41c22-104">This procedure shows how to add an addition to an existing fixed asset.</span></span> <span data-ttu-id="41c22-105">固定资产添加功能的目的就是追踪添加的资产项目，对固定资产进行维护和改进，也只是以提供信息为目的。</span><span class="sxs-lookup"><span data-stu-id="41c22-105">The purpose of Fixed asset additions is to track item additions, maintenance, or improvements for an asset, and is informational only.</span></span> <span data-ttu-id="41c22-106">任何对固定资产价值或服务年限的改变要单独进行。</span><span class="sxs-lookup"><span data-stu-id="41c22-106">Any changes to the fixed asset value or service life must be made separately.</span></span>   



<span data-ttu-id="41c22-107">本流程需要用到会计角色，使用来自法定实体 USMF 的演示数据。</span><span class="sxs-lookup"><span data-stu-id="41c22-107">The procedure uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="41c22-108">转到“固定资产”>“固定资产”>“固定资产”。</span><span class="sxs-lookup"><span data-stu-id="41c22-108">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="41c22-109">在列表中，查找并选择要添加的固定资产。</span><span class="sxs-lookup"><span data-stu-id="41c22-109">In the list, find and select the fixed asset for the addition.</span></span>
3. <span data-ttu-id="41c22-110">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="41c22-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="41c22-111">在“操作”窗格上，单击“固定资产”。</span><span class="sxs-lookup"><span data-stu-id="41c22-111">On the Action Pane, click Fixed asset.</span></span>
5. <span data-ttu-id="41c22-112">单击“固定资产物料添加”。</span><span class="sxs-lookup"><span data-stu-id="41c22-112">Click Fixed asset additions.</span></span>
6. <span data-ttu-id="41c22-113">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="41c22-113">Click New.</span></span>
7. <span data-ttu-id="41c22-114">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="41c22-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="41c22-115">设置添加物料采购或使用日期。</span><span class="sxs-lookup"><span data-stu-id="41c22-115">Set the date of the addition purchase or service.</span></span>
9. <span data-ttu-id="41c22-116">输入资产物料、维护或其他改善成本。</span><span class="sxs-lookup"><span data-stu-id="41c22-116">Enter the cost of the item, maintenance, or other improvement for the asset.</span></span>
10. <span data-ttu-id="41c22-117">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="41c22-117">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="41c22-118">总成本对固定资产的值没有影响，仅用于跟踪和提供信息。</span><span class="sxs-lookup"><span data-stu-id="41c22-118">The total cost will have no impact on the value of the fixed asset and is for tracking and informational purposes only.</span></span> <span data-ttu-id="41c22-119">如果要将成本资本化，则必须单独过帐调高交易。</span><span class="sxs-lookup"><span data-stu-id="41c22-119">If the cost will be capitalized, then a write-up adjustment transaction must be posted separately.</span></span>  
11. <span data-ttu-id="41c22-120">单击“常规”选项卡。</span><span class="sxs-lookup"><span data-stu-id="41c22-120">Click the General tab.</span></span>
    * <span data-ttu-id="41c22-121">如果增加物提供了资产的服务年限，设置增加服务年限</span><span class="sxs-lookup"><span data-stu-id="41c22-121">Set Increases service life if the addition increases the service life of the asset.</span></span>  
    * <span data-ttu-id="41c22-122">该字段仅用于提供信息。</span><span class="sxs-lookup"><span data-stu-id="41c22-122">This field is informational only.</span></span> <span data-ttu-id="41c22-123">要提高使用年限，请修改资产价值模型和折旧帐簿中的使用年限。</span><span class="sxs-lookup"><span data-stu-id="41c22-123">To increase the service life, modify the Service life on the Value models and/or Depreciation books for the asset.</span></span>  


