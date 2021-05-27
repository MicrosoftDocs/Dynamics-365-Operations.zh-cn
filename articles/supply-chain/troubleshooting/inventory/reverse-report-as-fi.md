---
title: 报告为完工入库撤销会创建意外的未结交易
description: 带有标记的报告为完工入库撤销会创建一个未结交易，其中的已冲销数量与已冲销交易具有相同的库存维度。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026315"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a><span data-ttu-id="f30c2-103">报告为完工入库撤销会创建意外的未结交易</span><span class="sxs-lookup"><span data-stu-id="f30c2-103">Reversal of reporting as finished creates an unexpected open transaction</span></span>

<span data-ttu-id="f30c2-104">知识库编号：4612469</span><span class="sxs-lookup"><span data-stu-id="f30c2-104">KB number: 4612469</span></span>

## <a name="symptoms"></a><span data-ttu-id="f30c2-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="f30c2-105">Symptoms</span></span>

<span data-ttu-id="f30c2-106">如果您撤销带有标记的报告为完工入库，系统会创建一个未结交易，其中的已冲销数量与已冲销的交易具有相同的库存维度。</span><span class="sxs-lookup"><span data-stu-id="f30c2-106">If you reverse reporting as finished that has marking, the system creates an open transaction where the reversed quantity has the same inventory dimensions as the transaction that was reversed.</span></span>

## <a name="resolution"></a><span data-ttu-id="f30c2-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="f30c2-107">Resolution</span></span>

<span data-ttu-id="f30c2-108">当您撤销报告为完工入库操作时，库存维度会从生产日记帐初始化。</span><span class="sxs-lookup"><span data-stu-id="f30c2-108">When you reverse a report-as-finished operation, the inventory dimension is initialized from the production journal.</span></span> <span data-ttu-id="f30c2-109">因此，它会获得批处理号。</span><span class="sxs-lookup"><span data-stu-id="f30c2-109">Therefore, it gets the batch number.</span></span> <span data-ttu-id="f30c2-110">由于有标记，销售订单交易将继承此批处理号。</span><span class="sxs-lookup"><span data-stu-id="f30c2-110">Because of marking, the sales order transactions will inherit the batch number.</span></span>

<span data-ttu-id="f30c2-111">维度可以在报告为完工入库过帐时重置。</span><span class="sxs-lookup"><span data-stu-id="f30c2-111">The dimension can be reset when the reporting as finished is posted.</span></span>
