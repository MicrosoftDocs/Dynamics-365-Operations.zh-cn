---
title: 监控预测准确性
description: 本主题介绍 Dynamics 365 Supply Chain Management 计算的预测准确性的类型，并说明如何可以查看准确性值。
author: roxanadiaconu
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6ad41e002f6246311c3755df5baf4a010f9204ee
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188902"
---
# <a name="monitor-forecast-accuracy"></a>监控预测准确性

[!include [banner](../includes/banner.md)]

本主题介绍 Microsoft Dynamics 365 Supply Chain Management 计算的预测准确性的类型，并说明如何可以查看准确性值。

Supply Chain Management 计算以下类型的预测准确性：

-   历史预测准确性，通过比较主计划使用的历史预测和历史需求。 若要查看历史预测准确性的值（绝对值和百分比值），请单击 **需求预测详细信息** 页的 **显示准确性**。
-   用于生成预测的预测模型的估计精确性。 您可以在 **需求预测详细信息** 页的 **模型详细信息 - MAPE** 下查看准确率百分比。 

> [!NOTE]
> 如果您使用需求预测 Microsoft Azure 机器学习，内部模型准确性的计算基于测试数据集。 若要指定测试数据集的规模，请在 **需求预测参数** 页上设置参数 **TEST\_SET\_SIZE\_PERCENT**。 例如，如果您将该值设置为 **20**，历史数据的最后 20% 将用于计算内部模型准确性。


## <a name="additional-resources"></a>其他资源

[授权调整后的预测](authorize-adjusted-forecast.md)

[在计算需求预测时，需从历史交易记录数据中删除离群值](remove-historical-outliers-calculating-demand-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]