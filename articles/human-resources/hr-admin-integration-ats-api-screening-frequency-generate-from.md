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
ms.openlocfilehash: 7b87bff6925721a20ad9d8bf92e64113d30333defd2d6708b445bcd2126e485a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766234"
---
# <a name="screening-frequency-generate-from"></a>筛选频率生成来源

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