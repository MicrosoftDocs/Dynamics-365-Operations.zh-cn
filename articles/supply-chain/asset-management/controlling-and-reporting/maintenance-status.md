---
title: 维护状态
description: 本主题说明如何在资产管理中计算维护状态。
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
ms.openlocfilehash: 516607c056125a16e075c33f3c2ad069efb396d9
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918341"
---
# <a name="maintenance-status"></a>维护状态

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

在资产管理中，可创建计算来查看特定期间新的、有效的和已完成的维护请求、工作订单和维护停机时间活动的概览。 也可以查看同一期间的已完成条件评估数量。 可使用此计算获取有关传入的和已完成的维护请求和工作订单的概览。

## <a name="make-a-maintenance-status-calculation"></a>创建维护状态计算

1. 单击**资产管理** > **查询** > **维护状态**。

2. 在**计算状态**对话框的**开始日期**和**结束日期**字段中选择要为其创建计算的期间。

3. 可使用**级别**字段指示要与功能位置有关的维护行的详细程度。 例如，如果在字段中插入数字“1”，并且采用了多级别功能位置结构，则将在最上级别显示某个功能位置的所有维护安排行，因此，可以从较低级别的功能位置叠加行中的状态。 如果在**级别**字段中插入数字“0”，将看到详细结果，其中显示其关联的所有功能位置级别的所有维护行。

4. 单击**确定**开始计算。

5. 在**分组依据**操作窗格组中，单击相关按钮显示所需成本计算详细程度。 将突出显示所选操作窗格按钮。 单击按钮将其激活或停用。

6. 每次通过激活或停用**分组依据**按钮或通过为新期间创建计算来进行更改时，都应该单击**更新**按钮以更新计算。

7. 如果要创建新的维护状态计算，请单击**状态**。

>[!NOTE]
>**维护状态**中显示的结果仅包括具有实际开始日期和时间的维护请求和工作订单。 结束日期和时间可以为空。

*示例 1：*

在下图中，已激活**年**和**月**按钮。 可在此处获取基于与维护请求和工作订单关联的月工作负载和吞吐量的一般概览。 

![图 1](media/13-controlling-and-reporting.png)

*示例 2：*

在下图中，已添加了有关功能位置的信息。 请注意，可以比较多个功能位置（可以是地理位置、工厂或工作区域）的工作负载和吞吐量。 

![图 2](media/14-controlling-and-reporting.png)

