---
title: 筛选频率生成来源
description: 本主题介绍 Dynamics 365 Human Resources 的筛选频率生成来源选项集。
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 27c6c62f3ac312ee502df969f25f1b16761cba03
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067796"
---
# <a name="screening-frequency-generate-from"></a>筛选频率生成来源


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 的筛选频率生成来源选项集。

物理名称：mshr_hcmfrequencygeneratefrom

此枚举提供用于确定下一次所需筛选的计算开始日期的值选项集。

| 值 | 标签 | 说明 |
| --- | --- | --- |
| 200000000 未选择 | 未选择值。 |
| 200000001 完成日期 | 从上一次筛选完成日期开始计算。 |
| 200000002 必需日期 | 从上一次必需筛选日期开始计算。 |

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[可雇用的应聘者的查询示例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
