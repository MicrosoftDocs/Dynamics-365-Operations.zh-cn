---
title: 主计划为虚拟产品生成计划订单
description: 主计划在运行后为虚拟产品生成了计划订单。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ea4bdb3729d163126234e02524cef331051cd48
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026310"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a><span data-ttu-id="b2ab4-103">主计划为虚拟产品生成计划订单</span><span class="sxs-lookup"><span data-stu-id="b2ab4-103">Master planning generates planned orders for phantom products</span></span>

<span data-ttu-id="b2ab4-104">知识库编号：4614729</span><span class="sxs-lookup"><span data-stu-id="b2ab4-104">KB number: 4614729</span></span>

## <a name="symptoms"></a><span data-ttu-id="b2ab4-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="b2ab4-105">Symptoms</span></span>

<span data-ttu-id="b2ab4-106">主计划在运行后为虚拟产品生成了计划订单。</span><span class="sxs-lookup"><span data-stu-id="b2ab4-106">Planned orders are generated for phantom products after master planning is run.</span></span>

## <a name="resolution"></a><span data-ttu-id="b2ab4-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="b2ab4-107">Resolution</span></span>

<span data-ttu-id="b2ab4-108">已发布产品的 **虚拟** 选项的设置确定物料清单 (BOM) 上的默认行类型。</span><span class="sxs-lookup"><span data-stu-id="b2ab4-108">The setting of the **Phantom** option for released products determines the default line type on the bill of material (BOM).</span></span> <span data-ttu-id="b2ab4-109">当 **虚拟** 选项设置为 *是* 时，系统仍会为物料创建计划订单，但每个计划订单的 **直接派生要求** 选项将设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="b2ab4-109">When the **Phantom** option is set to *Yes*, the system will still create planned orders for the item, but the **Directly derived requirement** option for each planned order will be set to *Yes*.</span></span> <span data-ttu-id="b2ab4-110">因此，计划生产订单无法自行确认。</span><span class="sxs-lookup"><span data-stu-id="b2ab4-110">Therefore, the planned production order can't be firmed on its own.</span></span> <span data-ttu-id="b2ab4-111">而是在确认父生产订单时，始终自动包括在内。</span><span class="sxs-lookup"><span data-stu-id="b2ab4-111">Instead, it will always be automatically included when the parent production order is firmed.</span></span> <span data-ttu-id="b2ab4-112">而且，计划虚拟订单的物料清单行将包括在父生产订单的物料清单中。</span><span class="sxs-lookup"><span data-stu-id="b2ab4-112">Additionally, the BOM lines of the planned phantom order will be included in the BOM of the parent production order.</span></span>
