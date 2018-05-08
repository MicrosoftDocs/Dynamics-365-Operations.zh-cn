---
title: "服务间隔"
description: "服务间隔指示在您创建服务订单时为服务协议行创建服务订单行所采用的频率。"
author: YuyuScheller
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4ea10e4c0fbfd21538bba16d2b01deb3e4b3a10d
ms.openlocfilehash: 4a51a3c3483e81cefdaf3d8e62a4f1f47fcd706b
ms.contentlocale: zh-cn
ms.lasthandoff: 02/20/2018

---

# <a name="service-intervals"></a>服务间隔

[!include [banner](../includes/banner.md)]

服务协议间隔指示在您自动创建服务订单时为服务协议行创建服务订单行所采用的频率。

在您自动创建服务订单时，将从该协议行的开始日期根据您为服务协议行指定的间隔创建服务订单行。

如果**服务协议**页面中某一服务协议行的**间隔**字段为空，则该行是一次性事件，不用于重复创建服务订单。

## <a name="example"></a>示例

此示例阐释服务间隔将如何影响在服务订单上的服务协议行和服务订单行。

### <a name="create-a-service-agreement"></a>创建服务协议

首先，创建一个服务协议，并将**合并服务订单**选项设置为**按服务协议**。

1. 单击**服务协议**
2. 在**新建**组中的**服务协议**选项卡上的**操作窗格**上，单击**服务协议**创建新的服务协议。
3. 输入描述，在**项目 ID** 字段中选择某一项目，并在**开始日期**字段中输入日期。
4. 在**合并服务订单** 字段中，选择**按服务协议**。

您现在创建了以下服务协议：

| Project      | 开始日期                                                                         |
|--------------|------------------------------------------------------------------------------------|
| 您的项目 | 为项目指定的日期。 在此示例中，使用了当前日期。 |

### <a name="create-a-service-agreement-line"></a>创建服务协议行

接下来，您创建交易记录类型为**工时**的服务协议行。

为了完成示例的这一部分，您必须在**服务间隔**页面中创建服务间隔为 10 天。 

1. 选择您刚创建的服务协议。 
2. 在**行**快速选项卡上，单击**添加**按钮以在**服务协议**页面的下部窗格中创建一个新行。
3. 在**交易记录类型**字段中选择**工时**。
4. 在**工作人员**字段中，选择要提供服务的工作人员。
5. 在**服务间隔**字段中，选择 10 天的服务间隔。

现在您已使用以下信息创建了一个服务协议行：

| 交易记录类型 | 入职日期                               | 服务间隔 |
|------------------|------------------------------------------|------------------|
| 工时             | 当前日期。                        | 每 10 天    |
| 工作线程           | 要执行服务的工作人员。 |                  |

不存在为该行指定的时间范围。 

### <a name="create-planned-service-orders"></a>创建计划的服务订单

您现在可以为下个月创建计划的服务订单和服务订单行。

1. 在**服务协议**页面**操作窗格**上的**交付**选项卡中，单击**计划服务订单**。
2. 在**创建服务订单**页面中，在**开始日期**字段中输入当前日期，在**结束日期**字段中输入距离当前日期一个月的日期。
3. 将**工时**滑块设置为**是**。 
4. 单击“确定”。

因为不存在针对服务订单的分组（由**合并服务订单**字段中的**按服务协议**选项定义），所以，为每个服务订单创建一个服务订单行。

### <a name="service-orders-created"></a>服务订单已创建

在您在**创建服务订单**对话框中指定的时间范围中，已创建三个服务订单行。 您可以在**服务协议**页面中查看服务订单行（**操作窗格** \> **交付** 选项卡 \> **查看**按钮）。

## <a name="related-topics"></a>相关主题

[设置服务间隔](set-up-service-intervals.md)  


