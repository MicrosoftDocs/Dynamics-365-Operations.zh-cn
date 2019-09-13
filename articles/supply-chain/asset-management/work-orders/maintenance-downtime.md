---
title: 维护停机时间
description: 本主题介绍资产管理中的维护停机时间。
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918236"
---
# <a name="maintenance-downtime"></a>维护停机时间


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

可以为工作订单中选择的资产创建维护停机时间登记。 如果要登记生产区域中一台或多台机器的维护停机时间，这非常有用。 首先，创建要使用的维护停机时间原因代码，例如，分解和计划停止。 此操作在**维护停机时间原因代码**中执行。 接下来，可以在**维护停机时间**中创建维护停机时间登记，并添加相关原因代码。

## <a name="create-maintenance-downtime-reason-codes"></a>创建维护停机原因代码

1. 单击**资产管理** > **设置** > **工作订单** > **维护停机时间原因代码**。

2. 单击**新建**。

3. 在**维护停机时间原因代码**字段中插入 ID。

4. 在**名称**字段中插入原因代码的名称。

5. 如果资产 KPI 计算中应该包含原因代码，请选中 **KPI 包括**复选框。 KPI 计算中通常不应包括计划的停产，因为它们不会影响预计绩效。

6. 单击**保存**。

![图 1](media/15-work-orders.png)


创建要使用的维护停机时间原因代码之后，可以为工作订单和资产创建维护停机时间登记。


## <a name="create-maintenance-downtime-registrations"></a>创建维护停机时间登记

1. 单击**资产管理** > **常用** > **工作订单** > **所有工作订单**或**有效工作订单**。

2. 选择工作订单，然后单击**维护停机时间**。

3. 单击**新建**。

4. 在**开始时间**和**结束时间**字段中插入维护停机时间登记的日期和时间间隔。

5. 离开**结束时间**字段时，将在**持续时间**字段中自动插入以小时为单位的持续时间。

6. 在**维护停机时间原因代码**字段中选择原因代码。

7. 如果要添加更多登记，请重复步骤 3-6。

8. 单击**保存**。


![图 2](media/16-work-orders.png)


用于计算维护停机时间登记的日历取决于在设置资产和参数时进行的选择。 如果在**资产** > **固定资产**快速选项卡 > **资源**字段中为资产选择资源，则使用为关联的资源组设置的日历，如下图中所示。

![图 3](media/17-work-orders.png)


如果不为资产选择任何资源，则使用**资产管理参数**中选择的标准日历，如下图中所示。

![图 4](media/18-work-orders.png)


单击**企业资产管理** > **查询** > **维护停机时间**以查看所有维护停机时间登记的概览。

>[!NOTE]
>**资产管理**模块中使用的所有日历均在**组织管理** > **设置** > **日历** > **日历**中设置。

