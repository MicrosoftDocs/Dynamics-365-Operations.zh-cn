---
title: 申请人集成结果
description: 本主题介绍 Dynamics 365 Human Resources 的申请人集成结果选项集。
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dd25eca9cccf46ec4e4bb2a1d948ca98985e73e4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467545"
---
# <a name="applicant-integration-result"></a>申请人集成结果

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 的申请人集成结果选项集。

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