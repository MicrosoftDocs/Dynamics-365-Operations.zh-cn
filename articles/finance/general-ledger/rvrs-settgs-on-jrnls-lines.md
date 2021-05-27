---
title: 日记帐和行中的冲销设置
description: 本主题说明了为什么在普通日记帐中输入的冲销条目可能不会包括在已过帐交易记录中的原因。
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 74020f6fc9b0fa8e05a1e2a09fd13dcd60490dc0
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028550"
---
# <a name="reverse-settings-on-journals-and-lines"></a><span data-ttu-id="cc1d3-103">日记帐和行中的冲销设置</span><span class="sxs-lookup"><span data-stu-id="cc1d3-103">Reverse settings on journals and lines</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc1d3-104">本主题说明了为什么在普通日记帐中输入的冲销条目可能不会包括在已过帐交易记录中的原因。</span><span class="sxs-lookup"><span data-stu-id="cc1d3-104">This topic addresses why a reversing entry that was entered on a general journal might not be included on the posted transaction.</span></span>  

## <a name="symptom"></a><span data-ttu-id="cc1d3-105">问题</span><span class="sxs-lookup"><span data-stu-id="cc1d3-105">Symptom</span></span>

<span data-ttu-id="cc1d3-106">普通日记帐包括日记帐中的冲销条目和冲销日期。</span><span class="sxs-lookup"><span data-stu-id="cc1d3-106">A general journal includes a reversing entry and reversing date on the journal.</span></span> <span data-ttu-id="cc1d3-107">过帐日记帐时，未冲销任何凭证。</span><span class="sxs-lookup"><span data-stu-id="cc1d3-107">When you post the journal, none of the vouchers are reversed.</span></span> <span data-ttu-id="cc1d3-108">为什么会发生这种情况？</span><span class="sxs-lookup"><span data-stu-id="cc1d3-108">Why does this happen?</span></span>

## <a name="resolution"></a><span data-ttu-id="cc1d3-109">解决方法</span><span class="sxs-lookup"><span data-stu-id="cc1d3-109">Resolution</span></span>

<span data-ttu-id="cc1d3-110">过帐日记帐时，冲销流程仅关注凭证的 **行** 部分中的 **冲销条目** 和 **冲销日期** 设置。</span><span class="sxs-lookup"><span data-stu-id="cc1d3-110">When the journal is posted, the reversing process looks only at the **Revering entry** and **Reversing date** settings on the **Lines** section of the voucher.</span></span> <span data-ttu-id="cc1d3-111">此方法可以使日记帐包括标记为冲销的某些凭证，以及一些其他类型的凭证。</span><span class="sxs-lookup"><span data-stu-id="cc1d3-111">This approach allows a journal to include some vouchers that are marked for reversing, and others that are not.</span></span>

<span data-ttu-id="cc1d3-112">添加 *新* 行时，日记帐中的值仅用作默认值。</span><span class="sxs-lookup"><span data-stu-id="cc1d3-112">The values from the journal are only used as defaults when adding *new* lines.</span></span> <span data-ttu-id="cc1d3-113">更改日记帐中的值不会影响现有的行。</span><span class="sxs-lookup"><span data-stu-id="cc1d3-113">Changing the values on the journal doesn’t affect existing lines.</span></span> <span data-ttu-id="cc1d3-114">在此示例中，首先输入了凭证行。</span><span class="sxs-lookup"><span data-stu-id="cc1d3-114">In this example, the voucher lines were entered first.</span></span> <span data-ttu-id="cc1d3-115">如果您在将日记帐指定为冲销之前输入行详细信息，所进行的冲销条目和冲销日期指定不会应用于任何现有行。</span><span class="sxs-lookup"><span data-stu-id="cc1d3-115">When you enter the line detail before designating the journal as reversing, the designation as a reversing entry and date won't be applied to any existing lines.</span></span>

<span data-ttu-id="cc1d3-116">更改现有行中的冲销条目或冲销日期会将该更改传播到同一凭证中的其他行。</span><span class="sxs-lookup"><span data-stu-id="cc1d3-116">Changing the reversing entry or reversing date on an existing line propagates that change to other lines in the same voucher.</span></span> <span data-ttu-id="cc1d3-117">为了优化性能，在将更改传播到其他行之后不会刷新网格。</span><span class="sxs-lookup"><span data-stu-id="cc1d3-117">To optimize performance, the grid is not refreshed after propagating changes to other Lines.</span></span> <span data-ttu-id="cc1d3-118">您可以通过刷新网格来显示更新的值。</span><span class="sxs-lookup"><span data-stu-id="cc1d3-118">You can display the updated values by refreshing the grid.</span></span>


