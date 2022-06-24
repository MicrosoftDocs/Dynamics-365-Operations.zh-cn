---
title: 工作免除情况
description: 本文介绍 Dynamics 365 Human Resources 的工作免除情况选项集。
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
ms.openlocfilehash: e59a71264d50cecce4d31dfa26ad7f05ef3f34e4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894663"
---
# <a name="job-exempt-status"></a>工作免除情况


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本文介绍 Dynamics 365 Human Resources 的工作免除情况选项集。

物理名称：cdm_jobexemptstatus

此枚举为 FLSA 工作免除情况值指定选项集。 在现有 cdm_jobexemptstatus 选项集中提供。

| 值 | 标签 | 说明 |
| --- | --- | --- |
| 200000000 | 豁免 | 工作根据 FLSA 准则确定免除情况。 |
| 200000001 | NonExempt | 工作根据 FLSA 准则为不免除状态。 |
| 200000002 | 不适用 | FLSA 状态准则不适用于此工作。 |

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[招聘请求的查询示例](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
