---
title: 购买和出售休假
description: 本主题介绍如何在 Dynamics 365 Human Resources 中提交购买和出售休假请求。
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 80b7125df93d9bdfb866b37abebbdc412d7e5b95
ms.sourcegitcommit: 67c4ed957e43d4d60bb609d93921a0be9619e675
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2022
ms.locfileid: "8509379"
---
# <a name="buy-and-sell-leave"></a>购买和出售休假


>[!Important]
>本主题中提到的功能目前对独立 Dynamics 365 Human Resources 上的客户可用。 在 Finance 版本 10.0.26 之后，部分或全部功能将作为未来版本的一部分在 Finance 基础结构上提供。

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

在 Dynamics 365 Human Resources 中，您可以根据公司设置的购买和出售休假策略提交购买和出售休假请求。  

## <a name="request-to-buy-leave"></a>购买休假的请求

1. 在 **员工自助服务** 工作区中，在 **休息时间余额** 磁贴中选择 **购买休假请求**。 

2. 添加一个 **休假类型**，然后输入您想要购买的休假金额的 **金额**。 

3. 准备好提交请求时选择 **提交**。 

您的余额将自动更新，或者在更新之前经过审批流程。 这取决于如何配置购买策略。

## <a name="request-to-sell-leave"></a>出售休假请求

1. 在 **员工自助服务** 工作区中，在 **休息时间余额** 磁贴中选择 **出售休假请求**。 

2. 添加一个 **休假类型**，然后输入您想要出售的休假金额的 **金额**。 

3. 准备好提交请求时选择 **提交**。

您的余额将自动更新，或者在更新之前经过审批流程。 这取决于如何配置购买策略。


## <a name="troubleshooting"></a>疑难解答 

如果购买或出售休假请求工作流失败，具有 **EssLeaveBuySellRequestApprover** 特权的用户可以查看所有休假购买和出售请求的消息日志。 为此，请转到 **休假和缺勤 > 链接 > 购买和出售休假请求 > 消息日志**（在左上角）。 **消息日志** 向用户显示交易的处理方式和关联的工作流历史记录。


## <a name="see-also"></a>请参阅

[休假和缺勤概览](hr-leave-and-absence-overview.md)</br>
[管理购买和出售休假策略](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
