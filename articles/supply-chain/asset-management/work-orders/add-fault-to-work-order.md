---
title: 将故障添加到工作订单
description: 此主题介绍如何在资产管理中向工作订单添加故障登记。
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e82026f1d73e7368d93109bc0b895b7368ac84d4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423027"
---
# <a name="add-fault-to-work-order"></a>将故障添加到工作订单

[!include [banner](../../includes/banner.md)]



可以向工作订单添加故障设计器中设置的故障。 必须将一个或多个故障记录连接到在工作订单中选择的资产所使用的资产类型。 有关设置的详细信息，请参阅[故障管理](../setup-for-work-orders/fault-management.md)。

1. 选择 **资产管理** > **常用** > **工作订单** > **所有工作订单** 或 **有效工作订单**。

2. 选择要创建故障登记的工作订单，然后，在操作窗格中，在 **工作订单** 选项卡上，在 **资产** 组中，选择 **资产故障**。

3. 在 **特征** 快速选项卡中，选择 **添加行**。 将在 **故障** 字段中自动输入一个连续故障编号。

4. 在 **故障特征** 字段中，选择相关特征。

5. 在 **故障区域** 和 **故障类型** 字段中，选择适当的值。

6. 将在 **故障日期** 字段中自动插入当前日期。 您可以根据需要选择其他日期。

7. 在 **所选故障特征的成因** 快速选项卡上，添加一行来描述问题成因。

8. 在 **所选故障特征的成因** 快速选项卡上，添加一行来描述问题的可行解决方案。

9. 选择 **保存**。

下图显示了故障登记的示例。

![图 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a>查看资产故障

在 **资产故障** 列表中，可概览为资产登记的所有故障。

在 **资产故障** 列表页上，可概览已为资产登记的所有故障。 要打开此页面，请选择 **资产管理** > **查询** > **资产故障** > **资产故障**。


## <a name="print-asset-fault-report"></a>打印资产故障报告

可从 **所有资产** 列表页打印资产故障报告，其中显示所有故障登记和故障统计信息的图形概览。

1. 选择 **资产管理** > **常用** > **资产** > **所有资产**。

2. 选择要为其打印故障报告的资产。

3. 在“操作”窗格中，在 **常规** 选项卡上，在 **报告** 组中，选择 **资产故障**。

4. 输入具体期间，或选择故障类型。

5. 选择 **确定** 打印报告。

>[!NOTE]
>要打印多个资产或资产类型的故障报告，请选择 **资产管理** > **报告** > **资产** > **资产故障**。

