---
title: 固定资产前滚报表
description: 本主题说明如何使用固定资产前滚报表。
author: moaamer
ms.date: 01/08/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2017-12-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: cbdb63c8b52baf030be10f27c27d27d58e3103a5
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/06/2022
ms.locfileid: "8720465"
---
# <a name="fixed-assets-roll-forward-report"></a>固定资产前滚报表

[!include [banner](../includes/banner.md)]

**固定资产前滚** 报表以通俗易懂的 Microsoft Excel 格式提供期间结帐、财务报表和报税所需的详细固定资产数据。 该报表中包含固定资产的期初余额和期末余额，期间的评估变动，以及该期间发生的任何新资产购置和处置。 将为单个固定资产报告数据，还将为固定资产组和法人汇总价值。

**固定资产前滚** 报表使用电子申报 (ER) 框架。 必须先从 Microsoft Dynamics Lifecycle Services (LCS) 导入固定资产模型和固定资产前滚配置，才能运行该报表。 有关说明，请参阅[从 Lifecycle Services 下载电子申报配置](/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs)。

此报表在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3 中提供，或作为 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition（2017 年 7 月）的修补程序提供。 必须为安装了 2017 年 7 月版本的环境应用三个修补程序：

- **KB 4041754：** 不能从 LCS 下载电子申报 (ER) 配置，因为应用了平台更新包后不适用于当前版本
- **KB 4056107：** 电子申报 (GER) 累积更新 5
- **KB 4056353：** 固定资产对帐单报表和附注报表不满足 GAAP 和 IFRS 中的要求

下表说明报表中的可用字段。


|                    字段                    |                                                                                                                                说明                                                                                                                                |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|              余额：期初              |                                                                                           报表中指定的“开始”日期的固定资产帐面净值。                                                                                           |
|              余额：期末              |                                                                                            报表中指定的“结束”日期的固定资产帐面净值。                                                                                            |
|         购置：期初值         |                                                 截止报表中指定的“开始”日期的类型为<strong>购置</strong>和<strong>购置调整</strong>的所有交易记录的总和。                                                  |
|      购置：期间购置      |                                                 报表的日期范围内过帐且类型为<strong>购置</strong>和<strong>购置调整</strong>的所有交易记录的总和。                                                  |
|       购置：期间处置        |                                                                        报表的日期范围内过帐且具有处置交易记录的所有购置冲销的总和。                                                                        |
|         购置：期末值         |                                                  截止报表中指定的“结束”日期的类型为<strong>购置</strong>和<strong>购置调整</strong>的所有交易记录的总和。                                                   |
|        折旧：期初值         | 截止报表中指定的“开始”日期的类型为<strong>折旧</strong>、<strong>折旧调整</strong>、<strong>特殊折旧补偿</strong>和<strong>特别折旧</strong>的所有交易记录的总和。 |
|     折旧：期间折旧     |                         报表的日期范围内过帐且类型为<strong>折旧</strong>、<strong>折旧调整</strong>和<strong>特别折旧</strong>的所有交易记录的总和。                          |
| 折旧：期间特殊折旧 |                                                              报表的日期范围内过帐且类型为<strong>特殊折旧补偿</strong>的所有交易记录的总和。                                                               |
|       折旧：期间处置       |                                                                       报表的日期范围内过帐且具有处置交易记录的所有折旧冲销的总和。                                                                        |
|        折旧：期末值         |  截止报表中指定的“结束”日期的类型为<strong>折旧</strong>、<strong>折旧调整</strong>、<strong>特殊折旧补偿</strong>和<strong>特别折旧</strong>的所有交易记录的总和。  |
|    调高/调低：期初值     |                              截止报表中指定的“开始”日期的类型为<strong>调高</strong>、<strong>调低</strong>和<strong>重估</strong>的所有交易记录的总和。                               |
|   调高/调低：期间调高   |                                                                    报表的日期范围内过帐且类型为<strong>调高</strong>的所有交易记录的总和。                                                                    |
|  调高/调低：期间调低  |                                                                   报表的日期范围内过帐且类型为<strong>调低</strong>的所有交易记录的总和。                                                                   |
| 调高/调低：期间重估  |                                                                        报表的日期范围内过帐且类型为<strong>重估</strong>的所有交易记录的总和。                                                                        |
|   调高/调低：期间处置   |                                                           报表的日期范围内过帐且具有处置交易记录的所有调高、调低和重估冲销的总和。                                                           |
|    调高/调低：期末值     |                               截止报表中指定的“结束”日期的类型为<strong>调高</strong>、<strong>调低</strong>和<strong>重估</strong>的所有交易记录的总和。                                |
|          处置：处置日期           |                                                                                                                固定资产帐簿的处置日期。                                                                                                                |
|    处置：处置时的帐面净值    |                                                                                                    处置时固定资产帐簿的帐面净值。                                                                                                    |
|            处置：销售值            |                                                                                               具有处置 - 销售交易记录的固定资产帐簿的销售值。                                                                                                |
|           处置：损耗值            |                                                                                               具有处置 - 损耗交易记录的固定资产帐簿的损耗值。                                                                                               |
|           处置：损益            |                                                                                 作为固定资产帐簿的处置交易记录一部分计算的损益值。                                                                                 |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
