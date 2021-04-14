---
title: 招聘请求职位状态
description: 本主题介绍 Dynamics 365 Human Resources 的招聘请求职位状态选项集。
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
ms.openlocfilehash: 7e59e9381fb15b339095d6a71296813e0141e9ab
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5789723"
---
# <a name="recruiting-request-position-status"></a>招聘请求职位状态

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 的招聘请求职位状态选项集。

物理名称：mshr_hcmrecruitingrequestpositionstatus

此枚举为 RecruitingRequestPosition 实体中招聘请求的每个职位的状态值提供选项集。

| 值 | 标签 | 说明 |
| --- | --- | --- |
| 200000000 | 公开 | 招聘请求中的职位空缺，要进行招聘。 这不指示该职位当前没有有效的职位分配。 招聘时该职位上可能有员工。 这仅指示在招聘请求的上下文中该职位可以招聘。 |
| 200000001 | 已填写 | 已选择一名工作人员要分配给该职位。 |
| 200000002 | 已取消 | 此职位的招聘请求已被取消。 |

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[招聘请求的查询示例](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]