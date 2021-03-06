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
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a>禁用“在实际更新时”时批处理号有多个库存交易

知识库编号：4613390

## <a name="symptoms"></a>故障特征

调整批处理号组的 **在实际更新时** 选项设置为 *否* 的物料的采购订单行后，会创建多个库存交易。

创建批处理号组的 **在实际更新时** 选项设置为 *否* 的物料时，如果您修改采购行数量并保存采购订单页面，系统将自动创建新的批处理号。

## <a name="resolution"></a>解决方法

批处理号组的 **在实际更新时** 设置以下列方式工作：

- 当此选项设置为 *是* 时，仅在实际更新后（例如，已装运或接收物料时）创建新的批处理号。
- 当此选项设置为 *否* 时，每次进行适用更新时（例如，向采购订单添加新数量时），都会创建新的批处理号。
