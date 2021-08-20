---
title: 在领料单登记期间选择位置时发生错误
description: 在领料单登记期间选择位置时发生错误。
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: da5905fb7ed1e890c85e891843379aa07de3279bd8972d6fc57136aa703c9ea4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762786"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a>在领料单登记期间选择位置时发生错误

知识库编号：4613106

## <a name="symptoms"></a>故障特征

当您的系统配置为自动预留销售订单时，会发生此问题。 如果您尝试选择领料单登记行的位置，在使用仓库管理 (WMS) 预留流程时会收到以下错误消息：

> 无法使用新维度更新数量

发生此问题的原因可能是由于您在指定位置没有足够的现有库存量。

## <a name="resolution"></a>解决方法

此系统行为是有意设计的。

在使用仓库级预留流程的场景中，如果不会在所有库存维度级别预留现有库存量，并且您在指定位置没有足够的现有库存量，建议您从领料行使用手动预留流程。 然后，您可以使用 *预留批次* 功能为所有可用的现有数量分配更低级别的预留，如位置。
