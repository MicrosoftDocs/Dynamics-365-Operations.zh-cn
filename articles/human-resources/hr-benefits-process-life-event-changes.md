---
title: 处理生命事件更改
description: 在 Microsoft Dynamics 365 Human Resources 中处理生命事件更改以进行生命事件更改。
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ae1aa74c7e463cd0d8c8d740394b998030c8498f
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229985"
---
# <a name="process-life-event-changes"></a>处理生命事件更改

在 Microsoft Dynamics 365 Human Resources 中处理生命事件更改以进行两项生命事件更改：

- 生日更改
- 资格规则覆盖到期更改 

1. 在**福利管理**工作区中，在**处理**下，选择**生命事件更改处理**。

2. 在**运行生命事件更改流程**对话框中，为以下字段指定值：

   | 字段 | 说明 |
   | --- | --- |
   | 登记期间 | 要处理其间的生命事件更改的登记期间。 |
   | 法人 | 要为其处理生命事件更改的法人。 |

3. 如果要在后台运行此流程，请选择**在后台运行**并执行以下任务：

   1. 输入流程的信息。

   2. 要设置重复性作业，请选择**重复**，输入重复信息，然后选择**确定**。

   3. 要设置作业预警，请选择**预警**，选择要接收的预警，然后选择**确定**。

   4. 选择**确定**。 流程将使用您设置的参数运行。

4. 选择**确定**。
