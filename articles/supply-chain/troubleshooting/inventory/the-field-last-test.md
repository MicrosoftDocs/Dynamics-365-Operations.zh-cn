---
title: 创建多个质检订单时，“上次测试日期”字段不更新
description: 创建多个质检订单时，“上次测试日期”字段不更新。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026314"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a><span data-ttu-id="a4a33-103">创建多个质检订单时，“上次测试日期”字段不更新</span><span class="sxs-lookup"><span data-stu-id="a4a33-103">The Last tested date field isn't updated when multiple quality orders are created</span></span>

<span data-ttu-id="a4a33-104">知识库编号：4612803</span><span class="sxs-lookup"><span data-stu-id="a4a33-104">KB number: 4612803</span></span>

## <a name="symptoms"></a><span data-ttu-id="a4a33-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="a4a33-105">Symptoms</span></span>

<span data-ttu-id="a4a33-106">创建多个质检订单时，**上次测试日期** 字段不更新。</span><span class="sxs-lookup"><span data-stu-id="a4a33-106">The **Last tested date** field isn't updated when multiple quality orders are created.</span></span>

## <a name="resolution"></a><span data-ttu-id="a4a33-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="a4a33-107">Resolution</span></span>

<span data-ttu-id="a4a33-108">此系统行为是有意设计的。</span><span class="sxs-lookup"><span data-stu-id="a4a33-108">The system is behaving as designed.</span></span> <span data-ttu-id="a4a33-109">上次测试日期与质检订单不相关。</span><span class="sxs-lookup"><span data-stu-id="a4a33-109">The last tested date isn't related to quality orders.</span></span> <span data-ttu-id="a4a33-110">它存储首次购买或制造成品的日期。</span><span class="sxs-lookup"><span data-stu-id="a4a33-110">It stores the date when the finished goods were first purchased or manufactured.</span></span> <span data-ttu-id="a4a33-111">此日期用于计算保质期建议日期。</span><span class="sxs-lookup"><span data-stu-id="a4a33-111">This date is used to calculate the shelf life advice date.</span></span>
