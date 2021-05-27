---
title: 为单个收货上的多个工作标题只打印了一个标签
description: 为单个收货上的多个工作标题只打印了一个标签。
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026302"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a><span data-ttu-id="4edc5-103">为单个收货上的多个工作标题只打印了一个标签</span><span class="sxs-lookup"><span data-stu-id="4edc5-103">Only one label is printed for multiple work headers on a single receipt</span></span>

<span data-ttu-id="4edc5-104">知识库编号：4614667</span><span class="sxs-lookup"><span data-stu-id="4edc5-104">KB number: 4614667</span></span>

## <a name="symptoms"></a><span data-ttu-id="4edc5-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="4edc5-105">Symptoms</span></span>

<span data-ttu-id="4edc5-106">作为单个仓库应用接收事件的一部分，将为同一个目标牌照创建多个工作标题。</span><span class="sxs-lookup"><span data-stu-id="4edc5-106">Multiple work headers are created for the same target license plate as part of a single warehouse app receiving event.</span></span> <span data-ttu-id="4edc5-107">但是，接收产品时只打印一个牌照标签。</span><span class="sxs-lookup"><span data-stu-id="4edc5-107">However, only one license plate label is printed when the product is received.</span></span>

## <a name="resolution"></a><span data-ttu-id="4edc5-108">解决方法</span><span class="sxs-lookup"><span data-stu-id="4edc5-108">Resolution</span></span>

<span data-ttu-id="4edc5-109">此系统行为是有意设计的。</span><span class="sxs-lookup"><span data-stu-id="4edc5-109">The system is behaving as designed.</span></span>

<span data-ttu-id="4edc5-110">在当前设计中，无论存在多少个工作标题和工作行组合，始终是生成一个牌照标签。</span><span class="sxs-lookup"><span data-stu-id="4edc5-110">In the current design, a single license plate label is always generated, regardless of the number of work header and work line combinations that exist.</span></span> <span data-ttu-id="4edc5-111">生成的标签仅包含一个组合的信息。</span><span class="sxs-lookup"><span data-stu-id="4edc5-111">The generated label includes the information for only one combination.</span></span>

<span data-ttu-id="4edc5-112">要解决此问题，请确保将工作标题创建始终映射到一个目标牌照。</span><span class="sxs-lookup"><span data-stu-id="4edc5-112">To work around this issue, make sure that work header creation is always mapped to just one target license plate.</span></span>
