---
title: 招聘请求状态
description: 本主题介绍 Dynamics 365 Human Resources 的招聘请求状态选项集。
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
ms.openlocfilehash: 55ed9c391a1b5f86c3c443b9fceeee5c2301444d
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125946"
---
# <a name="recruiting-request-status"></a>招聘请求状态

本主题介绍 Dynamics 365 Human Resources 的招聘请求状态选项集。

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