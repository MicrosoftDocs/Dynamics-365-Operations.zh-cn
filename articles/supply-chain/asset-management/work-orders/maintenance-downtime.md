---
title: 工作订单的维护停机时间
description: 此主题介绍如何为工作订单中选择的资产创建维护停机时间登记。
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 53487a0173453ef7a8f5ea818672d999fe71cb65
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020903"
---
# <a name="maintenance-downtime-for-work-orders"></a>工作订单的维护停机时间

[!include [banner](../../includes/banner.md)]


可以为工作订单中选择的资产创建维护停机时间登记。 如果要登记生产区域中一台或多台机器的维护停机时间，此功能非常有用。 首先，创建要使用的维护停机时间原因代码，如 **分解** 和 **计划停止**。 此步骤在 **维护停机时间原因代码** 页面执行。 然后，可以在 **维护停机时间** 页面创建维护停机时间登记，并添加相关的维护停机时间原因代码。

## <a name="create-maintenance-downtime-reason-codes"></a>创建维护停机原因代码

1. 选择 **资产管理** > **设置** > **工作订单** > **维护停机时间原因代码**。

2. 选择 **新建**。

3. 在 **维护停机时间原因代码** 字段中，输入维护停机时间原因代码的 ID。

4. 在 **名称** 字段中输入名称。

5. 如果原因代码应包含在资产的关键绩效指标 (KPI) 的计算中，请选中 **KPI 包括** 复选框。 通常，KPI 计算中不应包括计划的停产，因为它们不会影响预计绩效。

6. 选择 **保存**。

下图显示 **维护停机时间原因代码** 页面的示例。

![图 1](media/15-work-orders.png)

创建要使用的维护停机时间原因代码之后，可以为工作订单和资产创建维护停机时间登记。


## <a name="create-maintenance-downtime-registrations"></a>创建维护停机时间登记

1. 单击 **资产管理** > **常用** > **工作订单** > **所有工作订单** 或 **有效工作订单**。

2. 选择工作订单，然后在 **工作订单** 选项卡上，在 **资产** 组中，选择 **维护停机时间**。

3. 选择 **新建**。

4. 在 **开始时间** 和 **结束时间** 字段中，定义维护停机时间登记的日期和时间间隔。

>[!NOTE]
>离开 **结束时间** 字段时，将在 **持续时间** 字段中自动插入以小时为单位的持续时间。

5. 在 **维护停机时间原因代码** 字段中，选择原因代码。

6. 重复执行第 3 步到第 5 步，以添加更多登记。

7. 选择 **保存**。

下图显示了维护停机时间登记的示例。

![图 2](media/16-work-orders.png)

用于计算维护停机时间登记的日历取决于在设置资产和参数时进行的选择。 如果在 **所有资产** 页面的 **固定资产** 快速选项卡上的 **资源** 字段中为资产选择资源，则使用为关联的资源组设置的日历，如下图中所示。

![图 3](media/17-work-orders.png)

如果不为资产选择任何资源，则使用在 **资产管理参数** 页面选择的标准日历，如下图中所示。

![图 4](media/18-work-orders.png)

要查看所有维护停机时间登记的概览，单击 **资产管理** > **查询** > **维护停机时间**。

>[!NOTE]
>**资产管理** 模块中使用的所有日历均在 **组织管理** > **设置** > **日历** > **日历** 中设置。

