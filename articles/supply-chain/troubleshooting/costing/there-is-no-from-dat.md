---
title: “物料价格”页的“有效价格”选项卡上没有“开始日期”值
description: “物料价格”页的“有效价格”选项卡上没有“开始日期”值。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026318"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a><span data-ttu-id="604bb-103">“物料价格”页的“有效价格”选项卡上没有“开始日期”值</span><span class="sxs-lookup"><span data-stu-id="604bb-103">There is no From date value on the Active prices tab of the Item price page</span></span>

<span data-ttu-id="604bb-104">知识库编号：4613548</span><span class="sxs-lookup"><span data-stu-id="604bb-104">KB number: 4613548</span></span>

## <a name="symptoms"></a><span data-ttu-id="604bb-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="604bb-105">Symptoms</span></span>

<span data-ttu-id="604bb-106">**物料价格** 页的 **有效价格** 选项卡上没有 **开始日期** 值。</span><span class="sxs-lookup"><span data-stu-id="604bb-106">There is no **From date** value on the **Active prices** tab of the **Item price** page.</span></span>

## <a name="resolution"></a><span data-ttu-id="604bb-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="604bb-107">Resolution</span></span>

<span data-ttu-id="604bb-108">未决价格上设置的 **开始日期** 值（生效日期）不会转移到有效价格。</span><span class="sxs-lookup"><span data-stu-id="604bb-108">The **From date** value (effective date) that is set on the pending price isn't transferred to the active price.</span></span>

<span data-ttu-id="604bb-109">当物料成本记录初次输入时，它具有 *待定* 状态和预期生效日期。</span><span class="sxs-lookup"><span data-stu-id="604bb-109">When an item cost record is first entered, it has a status of *Pending* and an intended effective date.</span></span> <span data-ttu-id="604bb-110">当您激活物料成本记录时，状态将更新为 *有效*，生效日期将更新为激活日期。</span><span class="sxs-lookup"><span data-stu-id="604bb-110">When you activate the item cost record, the status is updated to *Active*, and the effective date is updated to the activation date.</span></span> <span data-ttu-id="604bb-111">因此，有效价格的激活日期始终是激活的实际日期。</span><span class="sxs-lookup"><span data-stu-id="604bb-111">Therefore, the active price's activation date is always the actual date of the activation.</span></span>

<span data-ttu-id="604bb-112">有关详细信息，请参阅[成本计算版本概述](../../cost-management/costing-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="604bb-112">For more information, see [Costing versions overview](../../cost-management/costing-versions.md).</span></span>
