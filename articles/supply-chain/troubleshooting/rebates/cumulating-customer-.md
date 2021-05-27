---
title: 使用物料返点组时客户返点累计失败
description: 当您将客户返点协议与物料返点组结合使用时，将计算返点，但累计将失败。
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026293"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>使用物料返点组时客户返点累计失败

知识库编号：4611372

## <a name="symptoms"></a>故障特征

当您将客户返点协议（*金额* 类型）与物料返点组结合使用时，将计算返点，但累计将失败。

## <a name="resolution"></a>解决方法

此系统行为是有意设计的。 物料组仅将具有相同阈值条件的物料分组在一起。 返点条件（阈值）针对每个物料的金额设置，不是针对物料组中任何物料的累计金额设置。
