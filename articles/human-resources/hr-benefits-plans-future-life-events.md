---
title: 配置将来生活事件
description: 本文介绍如何在 Dynamics 365 Human Resources 中计划未来生活事件。
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2cb3ca03e0d9d7e5423a405f1eb0372e1c19588d
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227976"
---
# <a name="configure-future-life-events"></a>配置将来生活事件

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [banner](../includes/preview-banner.md)]

您可以在 Dynamics 365 Human Resources 中计划未来的生活事件。

1. 在 **福利管理** 工作区中，在 **设置** 下，选择 **未来生活事件**。

2. 选择 **新建**。

3. 为以下字段指定值：

   | 字段 | 说明 |
   | --- | --- |
   | 生活事件日期 | 系统将处理在登记期间直到该日期为止的所有事件。 |
   | 已记录生活事件 | 记录生活事件的日期和时间。 |
   | 日志类型 | 显示操作是否为以下操作之一：</br></br>- **更新** – 对跟踪生活事件的现有记录进行更改</br></br>- **插入** – 创建新的生活事件记录 |
   | 生活事件类型 ID | 生活事件类型的唯一标识符。 |
   | 生活事件类型 | 促进更新员工福利登记的催化剂。 有关更多信息，请参阅“生活事件触发器”一节。 |
   | Status | 生活事件是否已处理。 |
   | 行 | 未来生活事件的行号。 |

4. 选择 **保存**。 

您可以删除未来的生活事件。 如果删除了已处理的未来生活事件，则将来的记录也会被删除。 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
