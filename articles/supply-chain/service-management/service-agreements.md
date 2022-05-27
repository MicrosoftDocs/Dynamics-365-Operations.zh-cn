---
title: 制定和建立服务协议概览
description: 在服务协议中，您可以定义在典型服务访问中使用的资源以及如何对这些资源向客户开票。
author: sorenva
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 559f4571a60ea8ec048b291e3b6a0a93e8bc9d44
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677693"
---
# <a name="develop-and-establish-service-agreements-overview"></a>制定和建立服务协议概览

[!include [banner](../includes/banner.md)]

在服务协议中，您可以定义在典型服务访问中使用的资源以及如何对这些资源向客户开票。

所有服务协议都附加到交易记录通过其过帐和开票的项目。 不过，您还可以通过项目直接对服务订单交易记录开票，而不必首先将该服务订单连接到某一服务协议。 如果服务订单针对仅限一次性的服务访问，并且快速处理服务交易记录的需要优先于维护某一时段中与客户有关的详细服务协议信息的需要，则您可能决定要这样做。

## <a name="service-agreement"></a>服务协议

在每个服务协议中，您必须指定项目、服务协议 ID 和服务协议组。 服务协议组可用于对服务协议进行排序和组织。

服务协议的标题包含应用于所有附加的协议行的设置：

-  服务协议是否被暂停。 如果服务协议被暂停，您不能根据服务协议生成服务订单。
-  服务协议的持续时间。
-  服务订单行如何合并到服务订单中。
-  服务协议是否是模板。

在服务协议标题中，您还设置通过输入要附加到该协议的各行的特定服务任务或服务对象可用于该服务协议的所有的服务对象和服务任务。

从服务协议标题，您还可以将服务协议行或服务模板行复制到当前服务协议中。

您可以暂停服务协议并停止执行各个服务协议行。

如果选中服务协议行的 **暂停** 复选框，则不能：

-    从服务协议自动或手动创建服务订单。

如果选中服务协议行的 **已停止** 复选框，则不能：

-    从服务协议行自动或手动创建服务订单。
-    将服务协议行复制到其他服务协议或服务订单。


> [!NOTE]
> 如果暂停服务协议，则停止执行所有附加的行而不管这些行的状态是什么。

## <a name="service-agreement-lines"></a>服务协议行

每个服务协议行详细描述建议的服务工作的内容。 这些行包含以下设置：

-  交易记录类型和交易记录类型的描述。
-  执行服务工作的员工。
-  必须根据服务协议对其执行服务的对象。
-  执行工作以及登记关联物料、支出和费用交易记录的频率。
-  服务订单行可组合到某一服务订单中的时间范围。
-  用于将多组协议行一起组合到工作任务中和用于向服务技术人员和客户总结要提供什么服务任务的服务任务。
-  是否停止某一行。 如果停止某一行，您不能为该单独的行创建服务订单。
-  诸如类别和行属性之类的项目设置。

## <a name="related-topics"></a>相关主题

[创建服务协议](create-service-agreements.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]