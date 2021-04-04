---
title: 预警概览
description: 本主题提供了有关预警的一般信息。 您可以使用预警保持了解有关您想要在工作日期间跟踪的事件。
author: tjvass
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: e57b065dc1a2c0db593b38106f4391e281feb1e6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565030"
---
# <a name="alerts-overview"></a>预警概览

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a>关于预警
预警形成系统中重要事件的通知系统。 您可以使用预警保持了解有关您想要在工作日期间跟踪的事件。 您可轻松创建自己的一套预警规则，以便获得有关逾期交货、删除订单、价格更改或其他必须响应的事件的预警。

在企业资源规划 (ERP) 中，有多个典型场景可以使用预警功能。 下面举了一些示例加以说明。

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a>场景 1：为新销售订单创建预警规则

1. 打开 **所有销售订单** 页。
2. 在操作窗格上，在 **选项** 选项卡，在 **共享** 组中，选择 **创建自定义预警**。
3. 在 **创建预警规则** 对话框，在 **在以下情况下提示** 快速选项卡上，在 **事件** 字段中，选择 **记录已创建**。

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a>场景 2：为交货日期延期创建预警规则

1. 打开 **所有采购订单** 页。
2. 选择采购订单 ID 以访问采购订单详细信息。
3. 展开 **采购订单头** 快速选项卡。
4. 在操作窗格上，在 **选项** 选项卡，在 **共享** 组中，选择 **创建自定义预警**。
5. 在 **创建预警规则** 对话框，在 **在以下情况下提示** 快速选项卡上，在 **字段** 字段中，选择 **交货日期**。
6. 在 **事件** 字段，选择 **已延迟**。
    
关闭 **创建预警规则** 对话框后，您的规则将出现在 **管理预警规则** 页。 您可以使用 **管理预警规则** 页更新您现有的预警规则。 例如，您可以修改事件触发器、更新事件通知、更新到期日期。 若要打开 **管理预警规则** 页，使用操作窗格的 **选项** 选项卡上的 **提示我** 按钮。

## <a name="what-occurs-when-an-alert-rule-is-created"></a>创建预警规则时会发生什么情况？

在您创建预警规则时，可以将预定义的事件与一个特定字段关联。 例如，到达字段中指定的日期时，或者字段的内容更改时。 或者，您可以将某一事件与特定页面中的记录关联。 例如，创建记录或删除记录。

该字段或该页面中的记录发生所选事件时，向您发送预警。 例如，您创建规则将特定采购订单行的 **交货日期** 字段与 **在此时间量之前到期** 事件关联。 您将时间范围设置为五天。 在此案例中，在该采购订单行的交付日期五天后发送预警。

此外，您可以通过设置条件来细化预警规则。 例如，您可以获得为特定供应商帐户创建新的采购订单的预警。

## <a name="preparing-for-an-alert"></a>准备预警

设置预警规则之前，请确定何时或在何种情况下您想要收到预警。 当您确定要通知的事件时，找到出现引起该事件的数据的页面。 事件可以是即将来临的日期，也可以是发生的特定更改。 因此，您必须找到指定此日期或者显示更改的字段或创建的新记录的页面。 获得此信息之后，您便可以创建预警规则。

## <a name="components-of-an-alert-rule"></a>预警规则的组件

预警规则有五个组件：

- **事件** – 触发预警规则的事件可以是即将来临的日期，也可以是发生的具体更改。 您在 **创建预警规则** 对话框的 **发送有关作业状态更改的电子邮件预警** 快速选项卡上定义事件。
- **条件** – 在 **创建预警规则** 对话框的 **提示以下事项** 快速选项卡上，您可以选择条件的作用域，来控制您什么时候收到与事件有关的预警。 您可以只将这个规则应用到当前记录或应用到页面上的所有可见记录。 如果在多个法人中应用规则，则您可以将 **组织范围** 选项设置为 **是**。
- **规则到期** – 在 **创建预警规则** 对话框的 **在以下时间之前提示** 快速选项卡上，可以指定预警规则应处于有效状态的时长。
- **内容** – 在 **创建预警规则** 对话框的 **提示以下内容** 快速选项卡上，可以指定预警消息应使用的主题文本和消息。
- **用户** – 在 **创建预警规则** 对话框的 **被警告者** 快速选项卡上，可以指定应接收预警消息的用户。 默认状态下，将选择您的用户 ID。

    > [!NOTE]
    > 此选项仅限组织管理员使用。

## <a name="videos"></a>视频

### <a name="how-to-use-alerts-to-monitor-filtered-data"></a>如何使用预警监控筛选数据

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3DWZ3]

YouTube 上的 [Finance and Operations 播放列表](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)中包含[如何使用预警监控筛选数据](https://youtu.be/ZYKMcv6kl9s)视频（上面所示）。

### <a name="alert-rule-options"></a>预警规则选项

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3E4PV]

YouTube 上的 [Finance and Operations 播放列表](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)中包含[预警规则选项](https://youtu.be/cpzimwOjicM)视频（上面所示）。




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]