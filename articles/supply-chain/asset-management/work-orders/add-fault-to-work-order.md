---
title: 将故障添加到工作订单
description: 此主题介绍如何在资产管理中向工作订单添加故障登记。
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875530"
---
# <a name="add-fault-to-work-order"></a>将故障添加到工作订单

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


可以向工作订单添加故障设计器中设置的故障。 工作订单中选择的资产必须包含与一个或多个故障记录连接的资产类型。 有关设置的详细信息，请参阅[故障管理](../setup-for-work-orders/fault-management.md)部分。

1. 单击**资产管理** > **常用** > **工作订单** > **所有工作订单**或**有效工作订单**。

2. 在列表中，选择要为其创建故障登记的工作订单，然后单击**资产故障**。

3. 在**特征**快速选项卡中，单击**添加行**。 将在**故障**字段中自动插入一个连续故障编号。

4. 在**故障特征**字段中选择相关特征。

5. 选择**故障区域**和**故障类型**。

6. 将在**故障日期**字段中自动插入当前日期。 如有必要，可以选择其他日期。

7. 在**所选故障特征的成因**快速选项卡上，添加一行，用于描述问题成因。

8. 在**所选故障特征的成因**快速选项卡上，添加一行，用于描述问题的可行解决方案。

9. 单击**保存**。

![图 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a>查看资产故障

在**资产故障**列表中，可概览为资产登记的所有故障。

单击**资产管理** > **查询** > **资产故障** > **资产故障**打开列表。


## <a name="print-asset-fault-report"></a>打印资产故障报告

可从**所有资产**列表页打印资产故障报告，其中显示所有故障登记，以及故障统计信息的图形概览。

1. 单击**资产管理** > **常用** > **资产** > **所有资产**。

2. 在**资产**列表中，选择要打印其故障报告的资产。

3. 在**常规**选项卡 > **报告**部分中，单击**资产故障**。

4. 插入具体期间，或选择故障类型。

5. 单击**确定**打印报表。

>[!NOTE]
>也可以通过单击**资产管理** > **报告** > **资产** > **资产故障**来打印多个资产或资产类型的故障报告。

