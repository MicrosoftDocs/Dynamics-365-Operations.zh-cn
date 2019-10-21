---
title: 创建工作订单
description: 本主题介绍如何在资产管理中创建工作订单。
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0a348bc9b7f5a24c5a3ac57113d430a92020b893
ms.sourcegitcommit: 6476f27c8d3dced7c2e9a7344a4e378b51a1983e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/27/2019
ms.locfileid: "1922106"
---
# <a name="creating-work-orders"></a>创建工作订单

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

已安排了预防性维护作业之后，接下来需要为这些作业创建工作订单。 这在其中一个维护安排内完成。 维护安排中的已安排作业可以采用不同类型：

| 引用类型 | 说明                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| 维护计划     | 基于维护安排类型“时间”或“计数器”的预防性维护作业。                       |
| 维护阶段    | 其中包含多个需要相似维护类型的资产的预防性维护作业。           |
| 维护请求   | 手动创建的资产维护或维修请求，可转化为工作订单。 |


1. 单击**资产管理** > **常用** > **所有维护安排**或**打开维护安排行**或**打开维护安排池**。

2. 选择要为其创建工作订单的已安排维护作业，然后单击**工作订单**。 在**创建工作订单**对话框中，将在**维护预测工时数**字段中显示所选行的预测工时总数。

3. 在**参数**部分中，选择应创建多少个工作订单。 可为每个维护安排行创建一个工作订单，或根据在**每个以下对象一个工作订单**部分中进行的选择创建一些工作订单。

4. 选择将在创建的所有工作订单中使用的**工作订单类型**。 下图显示了**创建工作订单**对话框的示例。

![图 1](media/18-preventive-maintenance.png)

5. 单击 **确定**。 将创建一个或多个工作订单。

