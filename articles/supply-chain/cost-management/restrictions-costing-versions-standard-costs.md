---
title: 对标准成本的成本计算版本的限制
description: 本文介绍适用于标准成本的成本计算版本的限制。
author: JennySong-SH
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c5c00ae8952e2c80d97d039271a6f5c63e9a72f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867976"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>对标准成本的成本计算版本的限制

[!include [banner](../includes/banner.md)]

本文介绍适用于标准成本的成本计算版本的限制。 

以下限制有助于确保符合标准成本计算准则：

-  费用必须包括在某一物料的成本中。 制造物料的费用表示在物料清单 (BOM) 和工艺路线信息内的摊销的固定成本。 因此，单位成本中必须包括这些费用。 采购物料的费用也包括在物料的单位成本中。

-  制造物料的标准成本计算必须基于标准成本的成本计算版本内的成本记录。 成本数据的备选来源只能用于计划成本的成本计算版本，例如针对采购物料的销售价贸易协议。 成本数据的备用来源由 BOM 计算组定义。

-  BOM 计算必须在单级分解模式下执行。

标准成本的物料成本数据可以复制到包含标准成本或计划成本的其他成本计算版本中。 但是，计划成本的物料成本数据不能复制到包含标准成本的成本版本中，因为本文前面列出的限制不应用于计划成本。

## <a name="related-articles"></a>相关文章

[成本计算版本概览](costing-versions.md)

[更新非制造环境中的标准成本](update-standard-costs-non-manufacturing-environment.md)

[准备为制造物料维护标准成本](update-standard-costs-manufacturing-environment.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]