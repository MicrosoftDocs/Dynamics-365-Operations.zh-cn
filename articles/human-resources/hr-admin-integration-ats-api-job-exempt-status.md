---
title: 工作免除情况
description: 本主题介绍 Dynamics 365 Human Resources 的工作免除情况选项集。
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4765858f389f28467ae2ac71084c15d2ba0cbe8b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798289"
---
# <a name="job-exempt-status"></a>工作免除情况

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 的工作免除情况选项集。

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