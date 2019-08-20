---
title: 输入对固定资产的添加件
description: 本流程展示如何对现有固定资产表添加新的成员。
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe1a1d4db696ac013afee05b697b301383232134
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839945"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a><span data-ttu-id="d3ea4-103">输入对固定资产的添加件</span><span class="sxs-lookup"><span data-stu-id="d3ea4-103">Enter an addition to a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d3ea4-104">本流程展示如何对现有固定资产表添加新的成员。</span><span class="sxs-lookup"><span data-stu-id="d3ea4-104">This procedure shows how to add an addition to an existing fixed asset.</span></span> <span data-ttu-id="d3ea4-105">固定资产添加功能的目的就是追踪添加的资产项目，对固定资产进行维护和改进，也只是以提供信息为目的。</span><span class="sxs-lookup"><span data-stu-id="d3ea4-105">The purpose of Fixed asset additions is to track item additions, maintenance, or improvements for an asset, and is informational only.</span></span> <span data-ttu-id="d3ea4-106">任何对固定资产价值或服务年限的改变要单独进行。</span><span class="sxs-lookup"><span data-stu-id="d3ea4-106">Any changes to the fixed asset value or service life must be made separately.</span></span>   

<span data-ttu-id="d3ea4-107">本流程需要用到会计角色，使用来自法定实体 USMF 的演示数据。</span><span class="sxs-lookup"><span data-stu-id="d3ea4-107">The procedure uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="d3ea4-108">在导航窗格中，转到**模块 > 固定资产 > 固定资产 > 固定资产**。</span><span class="sxs-lookup"><span data-stu-id="d3ea4-108">In the Navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="d3ea4-109">在列表中，查找并选择要添加的固定资产。</span><span class="sxs-lookup"><span data-stu-id="d3ea4-109">In the list, find and select the fixed asset for the addition.</span></span>
3. <span data-ttu-id="d3ea4-110">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="d3ea4-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="d3ea4-111">在操作窗格上，单击**固定资产**。</span><span class="sxs-lookup"><span data-stu-id="d3ea4-111">On the Action Pane, click **Fixed asset**.</span></span>
5. <span data-ttu-id="d3ea4-112">单击**固定资产物料添加**。</span><span class="sxs-lookup"><span data-stu-id="d3ea4-112">Click **Fixed asset additions**.</span></span>
6. <span data-ttu-id="d3ea4-113">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="d3ea4-113">Click **New**.</span></span>
7. <span data-ttu-id="d3ea4-114">在**名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d3ea4-114">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="d3ea4-115">在**购置日期**字段中，设置添加采购或服务的日期。</span><span class="sxs-lookup"><span data-stu-id="d3ea4-115">In the **Acquisition date** field, set the date of the addition purchase or service.</span></span>
9. <span data-ttu-id="d3ea4-116">在**单位成本**字段中，输入资产物料、维护或其他改善成本。</span><span class="sxs-lookup"><span data-stu-id="d3ea4-116">In the **Unit cost** field, enter the cost of the item, maintenance, or other improvement for the asset.</span></span>
10. <span data-ttu-id="d3ea4-117">在**数量**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="d3ea4-117">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="d3ea4-118">总成本对固定资产的值没有影响，仅用于跟踪和提供信息。</span><span class="sxs-lookup"><span data-stu-id="d3ea4-118">The total cost will have no impact on the value of the fixed asset and is for tracking and informational purposes only.</span></span> <span data-ttu-id="d3ea4-119">如果要将成本资本化，则必须单独过帐调高交易。</span><span class="sxs-lookup"><span data-stu-id="d3ea4-119">If the cost will be capitalized, then a write-up adjustment transaction must be posted separately.</span></span>  
11. <span data-ttu-id="d3ea4-120">单击**常规**选项卡。</span><span class="sxs-lookup"><span data-stu-id="d3ea4-120">Click the **General** tab.</span></span>

    * <span data-ttu-id="d3ea4-121">如果增加物提供了资产的服务年限，怎讲**增加服务年限**设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="d3ea4-121">Set **Increases service life** to **Yes** if the addition increases the service life of the asset.</span></span>  
    * <span data-ttu-id="d3ea4-122">该字段仅用于提供信息。</span><span class="sxs-lookup"><span data-stu-id="d3ea4-122">This field is informational only.</span></span> <span data-ttu-id="d3ea4-123">要提高使用年限，请修改资产价值模型和折旧帐簿中的使用年限。</span><span class="sxs-lookup"><span data-stu-id="d3ea4-123">To increase the service life, modify the Service life on the Value models and/or Depreciation books for the asset.</span></span>  

