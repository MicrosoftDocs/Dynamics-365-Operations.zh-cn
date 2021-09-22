---
title: 执行拆分领料时单位 %1 的数量无效
description: 跨多个批次执行拆分领料时，可能会出现数量对单位 %1 无效这一错误。 本页面有助于解决问题。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4627db7400d6ccd81f25f100de4696058ce35c42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475645"
---
# <a name="quantity-is-not-valid-when-performing-a-split-pick-across-multiple-batches"></a>在跨多个批次执行拆分领料时数量无效

## <a name="symptoms"></a>故障特征

当您尝试跨多个批次执行 *拆分领料* 时，会收到以下错误消息：

> 对于单位 %1，数量无效。

## <a name="resolution"></a>解决方法

仓库工作人员必须在 Warehouse Management 移动应用中使用 *领料短缺* 流程。 如果您尝试从同一库位为多个批次领料，还可以在应用中使用 **完全** 选项。
