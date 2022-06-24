---
title: 完成状态
description: 本文介绍 Dynamics 365 Human Resources 的完成状态选项集。
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
ms.openlocfilehash: 32575dfdd9bcd61b8a16bb544a9e7906ec96eaa1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880558"
---
# <a name="completion-status"></a>完成状态


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本文介绍 Dynamics 365 Human Resources 的完成状态选项集。

物理名称：mshr_hcmcompletionstatus

此枚举为应聘者筛选提供状态值选项集。 

| 值 | 标签 | 说明 |
| --- | --- | --- |
| 200000000 | 未完成 | 应聘者尚未完成筛选。 |
| 200000001 | 通过 | 应聘者已通过筛选。 |
| 200000002 | 失败 | 应聘者未通过筛选。 |

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[可雇用的应聘者的查询示例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
