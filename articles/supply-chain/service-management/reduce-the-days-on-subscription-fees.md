---
title: 缩减预订费用天数
description: 若要缩减现有预订费用的天数，可以创建一个新的交易记录，从中您删除不应继续作为预订费用间隔的一部分的时段。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd76e30b14d0fd21617e0ab7d892ba5ea3e89f2f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217302"
---
# <a name="reduce-the-days-on-subscription-fees"></a>缩减预订费用天数 

[!include [banner](../includes/banner.md)]


若要缩减现有预订费用的天数，可以创建一个新的交易记录，从中您删除不应继续作为预订费用间隔的一部分的时段。

## <a name="reduce-the-days-on-a-subscription-fee"></a>缩减预订费用天数

1.  单击**服务管理** \> **常用** \> **服务预订** \> **所有服务预订**。 选择服务预定，并在“操作窗格”中单击**预订费用**。

2.  在**预订类型**字段中，选择**缩减天数**。

3.  用**开始日期**和**结束日期**字段来定义要从预订费用期间删除的预订费用的日期间隔，然后单击**确定**。

若要查看已创建的交易记录，请在**预订**窗体中，单击**费用交易记录**。

## <a name="example"></a>示例

如果某一预订交易记录期间是从 1 月 1 日到 1 月 31 日，并且您想要将该期间缩减 10 天，则创建一个缩减期间是从 1 月 1 日到 1 月 10 日的新交易记录。 （该缩减期间还可以是从 1 月 5 日到 1 月 15 日或其他任何为期十天的期间）。

此外，如果该缩减期间的**开始日期**是 1 月 21 日（31 减 10），则您可以将**结束日期**设置为 1 月 31 日之后的任何日期，并且 10 天仍将从费用交易记录期间中删除。

## <a name="see-also"></a>请参阅

[缩减天数示例](reduction-days-example.md)

  


