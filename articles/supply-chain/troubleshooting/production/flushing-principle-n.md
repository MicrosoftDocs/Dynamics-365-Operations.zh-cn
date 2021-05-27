---
title: 未遵从物料清单行上的耗用原则设置
description: 未采用物料清单 (BOM) 行上的耗用原则设置。
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 84a84728016119a2a02f59f6903171afbceb48e7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026305"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a><span data-ttu-id="4fa88-103">未遵从物料清单行上的耗用原则设置</span><span class="sxs-lookup"><span data-stu-id="4fa88-103">Flushing principle settings on BOM lines aren't respected</span></span>

<span data-ttu-id="4fa88-104">知识库编号：4612725</span><span class="sxs-lookup"><span data-stu-id="4fa88-104">KB number: 4612725</span></span>

## <a name="symptoms"></a><span data-ttu-id="4fa88-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="4fa88-105">Symptoms</span></span>

<span data-ttu-id="4fa88-106">当 **生产控制参数** 页的 **自动更新** 选项卡上的 **自动物料清单消耗量** 字段设置为 *耗用原则* 时，会发生此问题。</span><span class="sxs-lookup"><span data-stu-id="4fa88-106">This issue occurs when the **Automatic BOM consumption** field on the **Automatic update** tab of the **Production control parameters** page is set to *Flushing principle*.</span></span> <span data-ttu-id="4fa88-107">此设置指示在接收采购订单时所有物料清单 (BOM) 行应自动消耗。</span><span class="sxs-lookup"><span data-stu-id="4fa88-107">This setting indicates that all bill of materials (BOM) lines should automatically be consumed when a purchase order is received.</span></span> <span data-ttu-id="4fa88-108">如果物料清单行上的 **耗用原则** 字段明确设置为 *手动*，您可能会预期物料清单行不会自动消耗。</span><span class="sxs-lookup"><span data-stu-id="4fa88-108">If the **Flushing principle** field on BOM lines is explicitly set to *Manual*, you might expect that the BOM lines won't automatically be consumed.</span></span> <span data-ttu-id="4fa88-109">但是，发生此问题时，**耗用原则** 字段设置为 *手动* 的物料清单行还是会自动消耗。</span><span class="sxs-lookup"><span data-stu-id="4fa88-109">However, when this issue occurs, BOM lines where the **Flushing principle** field is set to *Manual* are automatically consumed anyway.</span></span>

## <a name="resolution"></a><span data-ttu-id="4fa88-110">解决方法</span><span class="sxs-lookup"><span data-stu-id="4fa88-110">Resolution</span></span>

<span data-ttu-id="4fa88-111">如果遇到此问题，可以将生产控制参数设置为替代物料清单行上的 **耗用原则** 设置。</span><span class="sxs-lookup"><span data-stu-id="4fa88-111">If you're experiencing this issue, your production control parameters might be set up to override the **Flushing principle** setting on BOM lines.</span></span> <span data-ttu-id="4fa88-112">在 **生产控制参数** 页上的 **自动更新** 选项卡上，检查 **自动物料清单消耗量** 字段的值。</span><span class="sxs-lookup"><span data-stu-id="4fa88-112">On the **Production control parameters** page, on the **Automatic update** tab, check the value of the **Automatic BOM consumption** field.</span></span> <span data-ttu-id="4fa88-113">如果设置为 *始终*，系统将忽略所有物料清单行上的 **耗用原则** 设置，会始终耗用行。</span><span class="sxs-lookup"><span data-stu-id="4fa88-113">If it's set to *Always*, the system will disregard the **Flushing principle** setting on all BOM lines and will always flush the lines.</span></span> <span data-ttu-id="4fa88-114">要让系统遵从物料清单行上的 **耗用原则** 设置，将 **自动物料清单消耗量** 字段的值更改为 *耗用原则*。</span><span class="sxs-lookup"><span data-stu-id="4fa88-114">To make the system respect the **Flushing principle** setting on BOM lines, change the value of the **Automatic BOM consumption** field to *Flushing principle*.</span></span>
