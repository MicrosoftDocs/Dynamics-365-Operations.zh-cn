---
title: 负责的维护工人
description: 本主题说明如何在资产管理中设置负责的维护工人。
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkerResponsible
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad6b1757952fb0e5b970f82f75d99919a7f0745e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261157"
---
# <a name="responsible-maintenance-workers"></a><span data-ttu-id="28e1f-103">负责的维护工人</span><span class="sxs-lookup"><span data-stu-id="28e1f-103">Responsible maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="28e1f-104">可以将负责的维护工人与资产类型、资产、功能位置、维护作业类型类别、维护作业类型、维护作业类型变体和贸易关联。</span><span class="sxs-lookup"><span data-stu-id="28e1f-104">Responsible maintenance workers can be related to asset types, assets, functional locations, maintenance job type categories, maintenance job types, maintenance job type variants, and trades.</span></span> <span data-ttu-id="28e1f-105">可以在工作订单和维护请求中使用，以指示与应负责工作订单的维护工人有关的偏好。</span><span class="sxs-lookup"><span data-stu-id="28e1f-105">They can be used on work orders and maintenance requests to indicate a preference about the maintenance workers who should be responsible for a work order.</span></span> <span data-ttu-id="28e1f-106">（但是，这些维护工人不必是安排来履行工作订单的同一位工人。）此功能为可选功能。</span><span class="sxs-lookup"><span data-stu-id="28e1f-106">(However, those maintenance workers aren't necessarily the same workers who are scheduled to carry out the work order.) Use of this functionality is optional.</span></span> <span data-ttu-id="28e1f-107">例如，可用于为特定工作类型或工作领域选择负责的工人或工人组。</span><span class="sxs-lookup"><span data-stu-id="28e1f-107">For example, it can be used to select responsible workers or worker groups for specific work types or work areas.</span></span>

<span data-ttu-id="28e1f-108">工作订单生命周期或维护请求生命周期期间，可以更改或更新负责的维护工人。</span><span class="sxs-lookup"><span data-stu-id="28e1f-108">During a work order lifecycle or a maintenance request lifecycle, responsible maintenance workers can be changed or updated.</span></span> <span data-ttu-id="28e1f-109">例如，可以将此更改或更新与维护请求生命周期状态或工作订单生命周期状态的更改关联。</span><span class="sxs-lookup"><span data-stu-id="28e1f-109">This change or update might be related to, for example, a change in the maintenance request lifecycle state or the work order lifecycle state.</span></span>

<span data-ttu-id="28e1f-110">安排工作订单期间，*不* 使用 **负责的维护工人** 页上的设置。</span><span class="sxs-lookup"><span data-stu-id="28e1f-110">The setup on the **Responsible maintenance workers** page is *not* used during work order scheduling.</span></span>

> [!NOTE]
> <span data-ttu-id="28e1f-111">在资产管理中，也可以设置安排工作订单期间可以分配给工人的 *首选* 维护工人。</span><span class="sxs-lookup"><span data-stu-id="28e1f-111">In Asset Management, you can also set up *preferred* maintenance workers who might be allocated to work orders during work order scheduling.</span></span>

<span data-ttu-id="28e1f-112">设置负责的维护工人之前，必须设置应该可供选择的工人和维护工人组。</span><span class="sxs-lookup"><span data-stu-id="28e1f-112">Before you can set up responsible maintenance workers, you must set up the workers and maintenance worker groups that should be available for selection.</span></span> <span data-ttu-id="28e1f-113">有关如何设置工人和维护工人组的信息，请参阅[维护工人和工人组](../setup-for-objects/workers-and-worker-groups.md)。</span><span class="sxs-lookup"><span data-stu-id="28e1f-113">For information about how to set up workers and maintenance worker groups, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-responsible-maintenance-workers"></a><span data-ttu-id="28e1f-114">设置负责的维护工人</span><span class="sxs-lookup"><span data-stu-id="28e1f-114">Set up responsible maintenance workers</span></span>

1. <span data-ttu-id="28e1f-115">选择 **资产管理** \> **设置** \> **工人** \> **负责的维护工人**。</span><span class="sxs-lookup"><span data-stu-id="28e1f-115">Select **Asset management** \> **Setup** \> **Workers** \> **Responsible maintenance workers**.</span></span>
2. <span data-ttu-id="28e1f-116">选择 **新建** 创建记录。</span><span class="sxs-lookup"><span data-stu-id="28e1f-116">Select **New** to create a record.</span></span>
3. <span data-ttu-id="28e1f-117">首先创建默认负责的维护工人或负责的维护工人组设置，可在其中仅设置 **负责的维护工人组** 字段和/或 **负责的工人** 字段。</span><span class="sxs-lookup"><span data-stu-id="28e1f-117">First create a default responsible maintenance worker or responsible maintenance worker group setup, where you set only the **Responsible maintenance worker group** field and/or the **Responsible worker** field.</span></span> <span data-ttu-id="28e1f-118">将其余字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="28e1f-118">Leave the remaining fields blank.</span></span> <span data-ttu-id="28e1f-119">如果在安排工作订单期间没有其他更具体的组合与工作订单的内容匹配，将使用这个默认设置。</span><span class="sxs-lookup"><span data-stu-id="28e1f-119">This default setup will be used during work order scheduling if no other, more specific combination matches the contents of the work order.</span></span>

    > [!NOTE]
    > <span data-ttu-id="28e1f-120">创建维护请求期间，**所有维护请求** 页中有负责的维护工人或负责的维护工人组可供选择时，资产管理将浏览所有负责的维护工人记录以检查可能的匹配项。</span><span class="sxs-lookup"><span data-stu-id="28e1f-120">During creation of a maintenance request, when a responsible maintenance worker or responsible maintenance worker group is made available for selection on the **All maintenance requests** page, Asset Management goes through all responsible maintenance worker records to check for a possible match.</span></span> <span data-ttu-id="28e1f-121">始终先检查最具体的组合。</span><span class="sxs-lookup"><span data-stu-id="28e1f-121">It always checks the most specific combination first.</span></span> <span data-ttu-id="28e1f-122">换句话说，资产管理首先会检查 **贸易** 字段的匹配项。</span><span class="sxs-lookup"><span data-stu-id="28e1f-122">In other words, Asset Management first checks for a match for the **Trade** field.</span></span> <span data-ttu-id="28e1f-123">如果未找到匹配项，将检查 **维护作业类型变体** 字段的匹配项。</span><span class="sxs-lookup"><span data-stu-id="28e1f-123">If no match is found, it checks for a match for the **Maintenance job type variant** field.</span></span> <span data-ttu-id="28e1f-124">如果未找到匹配项，将检查 **维护作业类型** 字段的匹配项，以此类推。</span><span class="sxs-lookup"><span data-stu-id="28e1f-124">If no match is found, it checks for a match for the **Maintenance job type** field, and so on.</span></span> <span data-ttu-id="28e1f-125">您可以在页面的布局中看到，此行为意味着，为了查找最具体的组合，资产管理将从右到左检查每个记录以查找匹配项（依次检查 **贸易**、**维护作业类型变体**、**维护作业类型**、**维护作业类型类别**、**功能位置**、**资产**，最后检查 **资产类型**）。</span><span class="sxs-lookup"><span data-stu-id="28e1f-125">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match (first **Trade**, then **Maintenance job type variant**, then **Maintenance job type**, then **Maintenance job type category**, then **Functional location**, then **Asset**, and finally **Asset type**).</span></span> <span data-ttu-id="28e1f-126">如果未找到匹配项，将使用这七个字段中无可供选择的内容的默认记录。</span><span class="sxs-lookup"><span data-stu-id="28e1f-126">If no match is found, the default record that has no selections in those seven fields is used.</span></span>

<span data-ttu-id="28e1f-127">下图显示 **负责的维护工人** 页的示例。</span><span class="sxs-lookup"><span data-stu-id="28e1f-127">The following illustration shows an example of the **Responsible maintenance workers** page.</span></span>

![负责维护工人页面](media/08-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]