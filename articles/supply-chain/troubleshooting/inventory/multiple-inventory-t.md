---
title: 禁用“在实际更新时”时批处理号有多个库存交易
description: 调整批处理号组的“在实际更新时”选项设置为“否”的物料的采购订单行后，会创建多个库存交易。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1fa54cdfdbc5608fb6c7114dced0f96bab47253e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026317"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a><span data-ttu-id="b2112-103">禁用“在实际更新时”时批处理号有多个库存交易</span><span class="sxs-lookup"><span data-stu-id="b2112-103">Multiple inventory transactions for batch numbers when On physical update is disabled</span></span>

<span data-ttu-id="b2112-104">知识库编号：4613390</span><span class="sxs-lookup"><span data-stu-id="b2112-104">KB number: 4613390</span></span>

## <a name="symptoms"></a><span data-ttu-id="b2112-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="b2112-105">Symptoms</span></span>

<span data-ttu-id="b2112-106">调整批处理号组的 **在实际更新时** 选项设置为 *否* 的物料的采购订单行后，会创建多个库存交易。</span><span class="sxs-lookup"><span data-stu-id="b2112-106">Multiple inventory transactions are created after you adjust a purchase order line for items where the **On physical update** option of the batch number group is set to *No*.</span></span>

<span data-ttu-id="b2112-107">创建批处理号组的 **在实际更新时** 选项设置为 *否* 的物料时，如果您修改采购行数量并保存采购订单页面，系统将自动创建新的批处理号。</span><span class="sxs-lookup"><span data-stu-id="b2112-107">When you create an item where the **On physical update** option of the batch number group is set to *No*, the system automatically creates a new batch number if you modify a purchase line quantity and save the purchase order page.</span></span>

## <a name="resolution"></a><span data-ttu-id="b2112-108">解决方法</span><span class="sxs-lookup"><span data-stu-id="b2112-108">Resolution</span></span>

<span data-ttu-id="b2112-109">批处理号组的 **在实际更新时** 设置以下列方式工作：</span><span class="sxs-lookup"><span data-stu-id="b2112-109">The **On physical update** setting for batch number groups works in the following way:</span></span>

- <span data-ttu-id="b2112-110">当此选项设置为 *是* 时，仅在实际更新后（例如，已装运或接收物料时）创建新的批处理号。</span><span class="sxs-lookup"><span data-stu-id="b2112-110">When the option is set to *Yes*, new batch numbers are created only after a physical update (for example, when items are shipped or received).</span></span>
- <span data-ttu-id="b2112-111">当此选项设置为 *否* 时，每次进行适用更新时（例如，向采购订单添加新数量时），都会创建新的批处理号。</span><span class="sxs-lookup"><span data-stu-id="b2112-111">When the option is set to *No*, a new batch number is created every time that an applicable update occurs (for example, when a new quantity is added to a purchase order).</span></span>
