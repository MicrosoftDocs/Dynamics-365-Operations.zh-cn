---
title: 招聘请求状态
description: 本文介绍 Dynamics 365 Human Resources 的招聘请求状态选项集。
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
ms.openlocfilehash: 6a8cb8bc61786425c996b976a2914e7b650e3941
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859595"
---
# <a name="recruiting-request-status"></a>招聘请求状态


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本文介绍 Dynamics 365 Human Resources 的招聘请求状态选项集。

物理名称：mshr_hcmrecruitingrequeststatus

此枚举为 RecruitingRequest 的状态值提供选项集。

| 值 | 标签 | 说明 |
| --- | --- | --- |
| 200000000 | 草案 | 请求处于草稿状态，尚未准备好进行有效招聘。 |
| 200000001 | 正在审核 | 请求已提交，正在传送以通过工作流进行审批。 仅在工作流启用时可用。 |
| 200000002 | 待处理 | 请求正在等待工作流操作。 仅在工作流启用时可用。 |
| 200000003 | 已取消 | 已取消请求。 仅在工作流启用时可用。 |
| 200000004 | 已拒绝 | 请求已被拒绝。 仅在工作流启用时可用。 |
| 200000005 | 可用 | 任何工作流均已完成并获得批准，请求已准备好可以进行有效招聘。 |
| 200000006 | 已结 | 招聘请求已关闭。 |

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[招聘请求的查询示例](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
