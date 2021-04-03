---
title: 在计算需求预测时，需从历史交易记录数据中删除离群值
description: 本文描述如何从用于计算需求预测的历史数据中排除外离群值。 通过排除离群值，您可以提高预测准确性。
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup, ReqDemPlanOutlierQueryPreview
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2b44990dadec6203b28baa83954b15d04f8fc20
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259906"
---
# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a>在计算需求预测时，需从历史交易记录数据中删除离群值

[!include [banner](../includes/banner.md)]

本文描述如何从用于计算需求预测的历史数据中排除外离群值。 通过排除离群值，您可以提高预测准确性。

可以排除离群值以提高预测的精确度。 这是可选任务。 下面是流程的概述：

1.  单击 **主计划** &gt; **设置** &gt; **需求预测** &gt; **离群值删除** 以打开 **离群值删除** 页，从中可以使用查询选择要排除的交易记录。
2.  选择查询申请的公司，然后输入名称和描述。 **查询日期** 字段自动设置为当前日期。
3.  选中 **有效** 复选框可以从历史数据中排除由查询找到的交易记录。 在您创建基准预测时，此设置将生效。
4.  在 **离群值删除查询** 页上，当计算基准预测时，您可以删除、添加和选择定义将被排除的交易记录的标准。 例如，选择要排除的特定物料或订单交易记录。
5.  单击 **显示交易记录**。 **离群值交易记录** 页列出了满足查询中所定义标准的交易记录，并且在计算需求预测时，将从历史数据中排除此交易记录。

**注释：** 您还可以创建基于现有查询的查询。 选择要复制的查询，然后单击 **复制**。 **查询日期** 字段标识版本。 您可以按原样使用查询，也可以单击 **编辑查询** 修改条件。 （可选）您可以修改新查询的名称和描述。

<a name="additional-resources"></a>其他资源
--------

[需求预测概览](introduction-demand-forecasting.md)

[监控预测准确性](monitor-forecast-accuracy.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]