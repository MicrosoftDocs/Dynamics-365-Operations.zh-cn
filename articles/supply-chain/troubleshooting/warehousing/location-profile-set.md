---
title: 位置模板不允许负库存，但允许负现有库存量
description: 位置模板的“允许负库存”选项设置为“否”，但系统仍允许负现有库存量。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026301"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a><span data-ttu-id="f0442-103">位置模板不允许负库存，但允许负现有库存量</span><span class="sxs-lookup"><span data-stu-id="f0442-103">Location profile disallows negative inventory, but negative on-hand inventory is permitted</span></span>

<span data-ttu-id="f0442-104">知识库编号：4613622</span><span class="sxs-lookup"><span data-stu-id="f0442-104">KB number: 4613622</span></span>

## <a name="symptoms"></a><span data-ttu-id="f0442-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="f0442-105">Symptoms</span></span>

<span data-ttu-id="f0442-106">位置模板的 **允许负库存** 选项设置为 *否*，但系统仍允许负现有库存量。</span><span class="sxs-lookup"><span data-stu-id="f0442-106">The **Allow negative inventory** option for the location profile is set to *No*, but the system still allows negative on-hand inventory.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="f0442-107">示例场景</span><span class="sxs-lookup"><span data-stu-id="f0442-107">Example scenario</span></span>

<span data-ttu-id="f0442-108">对于政府监管的交易，系统必须能够在帐面亏损中记录负库存。</span><span class="sxs-lookup"><span data-stu-id="f0442-108">For government-regulated transactions, the system must be able to record negative inventory to book losses.</span></span> <span data-ttu-id="f0442-109">您希望某个物料能够显示负库存，但只是在指定位置，如油罐。</span><span class="sxs-lookup"><span data-stu-id="f0442-109">You want an item to be able to show negative inventory, but only in designated locations, such as tanks.</span></span> <span data-ttu-id="f0442-110">但是，如果物料模型组允许负库存，您会发现位置是否设置为允许负库存都没有影响。</span><span class="sxs-lookup"><span data-stu-id="f0442-110">However, if the item model group allows negative inventory, you find that it doesn't matter whether the location is set to allow negative inventory.</span></span> <span data-ttu-id="f0442-111">如果设置了物料，以不允许负库存，如何设置位置模板则无关紧要。</span><span class="sxs-lookup"><span data-stu-id="f0442-111">If the item is set up so that negative inventory isn't allowed, it doesn't matter how the location profile is set up.</span></span>

## <a name="resolution"></a><span data-ttu-id="f0442-112">解决方法</span><span class="sxs-lookup"><span data-stu-id="f0442-112">Resolution</span></span>

<span data-ttu-id="f0442-113">位置模板中的 **允许负库存** 设置仅适用于仓库流程，如领料。</span><span class="sxs-lookup"><span data-stu-id="f0442-113">The **Allow negative inventory** setting from the location profile applies only to warehouse processes, such as picking.</span></span> <span data-ttu-id="f0442-114">但是，设置为允许负库存的物料模型组会影响库存管理和仓库管理模块中的所有流程，位置模板不会替代此设置。</span><span class="sxs-lookup"><span data-stu-id="f0442-114">However, item model groups that are set to allow negative inventory affect all processes from the Inventory management and Warehouse management modules, and the location profile won't override the setting.</span></span>

<span data-ttu-id="f0442-115">您可以控制是否允许仓库支持负库存。</span><span class="sxs-lookup"><span data-stu-id="f0442-115">You can control whether a warehouse is allowed to carry negative inventory.</span></span> <span data-ttu-id="f0442-116">将物料模型组设置为不允许负实际库存，仅将相关仓库设置为允许负库存。</span><span class="sxs-lookup"><span data-stu-id="f0442-116">Set your item model groups to disallow negative physical inventory, and set only the relevant warehouse to allow negative inventory.</span></span>
