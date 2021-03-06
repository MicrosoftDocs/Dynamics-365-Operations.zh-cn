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
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a>拆分实际称重数量时，使用最小数量而不是标准数量

知识库编号：4612073

## <a name="symptoms"></a>故障特征

将实际称重数量拆分为几个批次时，**领料数量** 字段使用为物料设置的最小数量，而不是标准数量。

## <a name="resolution"></a>解决方法

此系统行为是有意设计的。 系统使用每个物料的最小数量设置进行领料。
