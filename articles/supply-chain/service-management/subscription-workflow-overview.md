---
title: 预订工作流概览
description: 此主题概要介绍预订工作流。
author: kamaybac
ms.date: 05/07/2018
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd1484563e9650b9ddae543e3440eec2a3ed075c
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2022
ms.locfileid: "7983036"
---
# <a name="subscription-workflow-overview"></a>预订工作流概览 

[!include [banner](../includes/banner.md)]


您是一家提供照明设备维护预定的灯具公司的预订管理员。 一个客户联系您公司购买一年的照明设备维护预订。

## <a name="setting-up-subscriptions"></a>设置预订

若要设置预订，您必须首先为新的服务协议创建一个预订组，或者确认某一预订组存在。 如果存在某一预订组，则必须将它设置为每年对该客户开票，并且计入当年每个月的销售收入。 有关如何设置预订的详细信息，请参阅[设置预订组](set-up-subscription-groups.md)。

在创建该预订组后，您可以创建预订。 有关如何创建服务预订的详细信息，请参阅[从预订组创建服务预订](create-service-subscriptions-from-subscription-group.md)。

## <a name="create-and-modify-subscription-transactions"></a>创建和修改预订交易记录

在设置预定后，您为第一个开票期间（即一年）创建预订费用交易记录。 交易记录的类型为 **常规**。 因此，只能创建开始日期和结束日期对应于以前在 **期间类型** 窗体中创建的期间的预订交易记录。 有关费用交易记录的详细信息，请参阅[创建预订费用交易记录](create-subscription-fee-transactions.md)。

在您为客户设置预订后，记住对于您提供的服务的所有标价，双方已协商了 10% 的折扣。 因此，您必须降低已创建的交易记录费用的价格。

在当天的晚些时候，您客户的联系人给您打电话，指出尽管他们仍需要针对照明设备的服务协议，但它们计划在当年的下半年引入新的照明设备。 因此，他们只需截止到 2013 年 10 月的维护覆盖范围。 为了减少针对客户的预订的月份数，您创建类型为 **缩减天数** 的新的预订费用交易记录。 有关如何缩减天数的详细信息，请参阅[缩减预订费用天数](reduce-the-days-on-subscription-fees.md)。

## <a name="invoice-and-accrue-subscription-transactions"></a>开票和计入预订交易记录

您现在已完成了预订设置，并且可以针对预订为您的客户开票了。 有关如何为预订开票的详细信息，请参阅[为预订交易记录开票](invoice-subscription-transactions.md)。

两天后，您的客户打电话指出，该预订应按美元开票，而非按欧元开票。 因此，您创建一个贷方通知单，并且还按正确的币种创建一个新的预订交易记录。 有关如何贷记预订交易记录的详细信息，请参阅[贷记预订交易记录](credit-subscription-transactions.md)。

在每个月的月末，可将来自客户的预订的当月收入计入损益科目和 WIP 科目。 有关如何应计预订的收入的详细信息，请参阅[应计预订收入](accrue-subscription-revenue.md)。

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]