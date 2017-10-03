---
title: "设置欺诈预警"
description: "此主题说明在订单处理过程中，如何设置预警规则来通知客户服务代表潜在的欺诈信息。 您可以定义特别的代码用以自动或手动地暂停可疑订单。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7255f2b7e49f56a731d0e3745b4752091013668b
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017



---

# <a name="set-up-fraud-alerts"></a>设置欺诈预警

[!include[banner](includes/banner.md)]


此主题说明在订单处理过程中，如何设置预警规则来通知客户服务代表潜在的欺诈信息。 您可以定义特别的代码用以自动或手动地暂停可疑订单。 

在设置和使用欺诈检查规则之前，您必须启用欺诈检查并在呼叫中心参数中定义基本欺诈检查值。 有以下两种类型的欺诈规则：

-   **静态规则** 使用特定的值，例如已列入黑名单的电话号码。
-   **动态规则** 可由变量和条件构成。

在创建动态规则之前，您需创建变量和条件，它们定义了规则适用对象以及适用场合。 例如，您需要创建一个规则以要求将客户 1202 下达的价值 1,000.00 或更高的任何销售订单置于暂停状态，直到客户付款被确认。 在此情况下，变量为客户 1202 和订单总和 1,000.00。 此条件指定，如果客户 1202 下达了订单且订单的总金额大于或等于 1,000.00，则必须将销售订单置于暂停状态，直到客户付款被确认。




