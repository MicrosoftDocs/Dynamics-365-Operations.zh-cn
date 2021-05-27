---
title: 拆分实际称重数量时，使用最小数量而不是标准数量
description: 将实际称重数量拆分为几个批次时，“领料数量”字段使用为物料设置的最小数量，而不是标准数量。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 185365ced5c4516d8fcdbdca88794d0078615888
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026312"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a><span data-ttu-id="f1640-103">拆分实际称重数量时，使用最小数量而不是标准数量</span><span class="sxs-lookup"><span data-stu-id="f1640-103">When a catch-weight quantity is split, minimum quantity is used instead of nominal quantity</span></span>

<span data-ttu-id="f1640-104">知识库编号：4612073</span><span class="sxs-lookup"><span data-stu-id="f1640-104">KB number: 4612073</span></span>

## <a name="symptoms"></a><span data-ttu-id="f1640-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="f1640-105">Symptoms</span></span>

<span data-ttu-id="f1640-106">将实际称重数量拆分为几个批次时，**领料数量** 字段使用为物料设置的最小数量，而不是标准数量。</span><span class="sxs-lookup"><span data-stu-id="f1640-106">When a catch-weight quantity is being split into batches, the **Pick qty** field uses the minimum quantity that is set for the item, not the nominal quantity.</span></span>

## <a name="resolution"></a><span data-ttu-id="f1640-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="f1640-107">Resolution</span></span>

<span data-ttu-id="f1640-108">此系统行为是有意设计的。</span><span class="sxs-lookup"><span data-stu-id="f1640-108">The system is behaving as designed.</span></span> <span data-ttu-id="f1640-109">系统使用每个物料的最小数量设置进行领料。</span><span class="sxs-lookup"><span data-stu-id="f1640-109">The system uses each item's minimum quantity setup for picking.</span></span>
