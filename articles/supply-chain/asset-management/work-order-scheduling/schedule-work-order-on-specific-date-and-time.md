---
title: 将工作订单安排到特定日期和时间
description: 本主题介绍如何在资产管理中将工作订单安排到特定日期和时间。
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e1b9fc2f51e92a4760a612d778b65cfc1b4e2a9e
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017359"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a>将工作订单安排到特定日期和时间

[!include [banner](../../includes/banner.md)]

 

如果必须将工作订单安排到特定日期 *和* 时间，可在资产管理中替换标准安排流程，并为工作订单创建特定安排。

1. 单击 **资产管理** > **常用** > **工作订单** > **所有工作订单** 或 **有效工作订单**。

2. 在工作订单列表的 **工作订单** 列中，单击工作订单 ID。

3. 单击 **编辑**。

4. 在 **工作订单标题** 快速选项卡上，在 **预计的开始时间** 和 **预计的结束时间** 字段中插入开始和结束日期和时间。

    ![图 1](media/05-work-order-scheduling.png)

5. 在 **常规** 选项卡上，单击 **计划** 以使用标准计划流程，如果要将工作订单分配给特定工作人员，则单击 **分派**。

6. 若要替换任何现有产能预留以确保将工作订单安排在预计期间，请在 **安排工作订单** 对话框 > **有限产能** 部分中按照下图所示进行选择。 这意味着安排流程将忽略现有产能预留，因为此工作订单必须在预计开始时间开始。

    ![图 2](media/06-work-order-scheduling.png)

7. 单击 **确定** 开始安排。

8. 如果安排流程导致双倍预订，您将在屏幕中看到一条消息，并且可以调整相关工作订单。

>[!NOTE]
>若要将某位维护工人安排给此工作订单，该维护工人必须在预计开始日期和时间有空。 工人可用性在[工人日历](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md)中设置。 

