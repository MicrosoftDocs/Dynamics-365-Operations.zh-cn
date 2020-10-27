---
title: 贷方预订交易记录
description: 本主题演示如何创建预订交易记录。
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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c4cbc3cd5deff709ac0818358dcc87fa69a7d872
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983469"
---
# <a name="credit-subscription-transactions"></a>贷方预订交易记录 

[!include [banner](../includes/banner.md)]


## <a name="credit-subscription-transactions"></a>贷方预订交易记录

1.  单击**服务管理** \> **常用** \> **服务预订** \> **所有服务预订**。

2.  选择附加到您要为其创建贷方通知单的预订交易记录的预订。

3.  选择**分析**选项卡，然后在“操作窗格”上单击**费用交易记录**按钮。

4.  从**费用交易记录**窗体中选择您想为其创建贷方通知单的交易记录。

5.  单击**功能** \> **为贷方通知单选择**。

6.  从**为贷方通知单选择**窗体中，选择您要贷记的交易记录，然后单击**确定**。


> [!NOTE]
> <P>当您创建贷方通知单时，请确保您选择了<STRONG>贷方通知单</STRONG>。 这是在<STRONG>创建发票</STRONG>对话框中的<STRONG>开票方法</STRONG>列表中找到的。</P>

如果**服务管理参数**窗体中的**冲销贷记的应计项目**字段设置为**手动**，则您必须首先单独冲销每个应计收入交易记录，然后才能为该交易记录创建贷方通知单方案。

## <a name="see-also"></a>请参阅

[发票预订交易记录](invoice-subscription-transactions.md)


 
