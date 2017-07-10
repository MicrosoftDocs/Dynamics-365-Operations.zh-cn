---
title: "监控预测准确性"
description: "本文介绍 Microsoft Dynamics 365 for Finance and Operations 计算的预测准确性的类型，并说明如何可以查看准确性值。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 56d3f0312e684ab076f9116ac6638bcd67b52e58
ms.contentlocale: zh-cn
ms.lasthandoff: 06/13/2017


---

# <a name="monitor-forecast-accuracy"></a>监控预测准确性

[!include[banner](../includes/banner.md)]


本文介绍 Microsoft Dynamics 365 for Finance and Operations 计算的预测准确性的类型，并说明如何可以查看准确性值。

Finance and Operations 计算以下类型的预测准确性：

-   历史预测准确性，通过比较主计划使用的历史预测和历史需求。 若要查看历史预测准确性的值（绝对值和百分比值），请单击**需求预测详细信息**页的**显示准确性**。
-   用于生成预测的预测模型的估计精确性。 您可以在**需求预测详细信息**页的**模型详细信息 - MAPE** 下查看准确率百分比。 

**注意：**如果您使用 Finance and Operations 需求预测 Microsoft Azure 机器学习服务，内部模型准确性的计算基于测试数据集。 若要指定测试数据集的规模，请在**需求预测参数**页上设置参数 **TEST\_SET\_SIZE\_PERCENT**。 例如，如果您将该值设置为 **20**，历史数据的最后 20% 将用于计算内部模型准确性。


<a name="see-also"></a>请参阅
--------

[授权调整后的需求预测](authorize-adjusted-forecast.md)

[在计算需求预测时，需从历史交易记录数据中删除离群值](remove-historical-outliers-calculating-demand-forecast.md)




