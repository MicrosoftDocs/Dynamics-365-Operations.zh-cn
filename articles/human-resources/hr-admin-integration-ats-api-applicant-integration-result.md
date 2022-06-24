---
title: 申请人集成结果
description: 本文介绍 Dynamics 365 Human Resources 的申请人集成结果选项集。
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
ms.openlocfilehash: 84f0ba9b197866935535a68006cfdb8c18fa3ad1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902305"
---
# <a name="applicant-integration-result"></a>申请人集成结果


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本文介绍 Dynamics 365 Human Resources 的申请人集成结果选项集。

物理名称：mshr_hcmapplicantintegrationresult

此枚举提供应聘者记录的状态。

| 值 | 标签 | 说明 |
| --- | --- | --- |
| 200000000 | 未处理 | 应聘者仍在考虑之中。 |
| 200000001 | 已雇用 | 应聘者已被雇用。 |
| 200000002 | 未雇用 | 决定不雇用应聘者。 |
| 200000003 | 已消除 | 应聘者被排除在考虑范围之外。 |

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[可雇用的应聘者的查询示例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
