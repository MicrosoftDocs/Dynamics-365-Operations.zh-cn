---
title: 维护安排
description: 本文介绍资产管理中的维护安排。
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectCalendarCreateWO, EntAssetObjectCalendarListPagePoolsOpen, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePreviewPart, EntAssetObjectCalendarEdit, EntAssetObjectCalendarAdjust, EntAssetObjectCalendarDiscard, EntAssetObjectCalendarInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 782a8cc1f9e64b8c2d4364212c9c5755c103bbfb
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017049"
---
# <a name="maintenance-schedule"></a>维护安排

[!include [banner](../../includes/banner.md)]

 

维护安排中包含预计要执行的所有预防性维护计划、维护请求和维护阶段的列表。可能已将某些安排行转换成了工作订单。

这四个维护安排视图稍有不同，具体取决于要查看哪些维护安排行。

| 菜单项                  | 内容的描述                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 所有维护安排       | 将显示所有维护安排行。     |
| 我的资产计划        | 此列表中显示其中包含在您作为工人关联的功能位置(在[维护工人和工人组](../setup-for-objects/workers-and-worker-groups.md)中设置)安装的资产的所有维护安排行。 |
| 打开维护安排行 | 此列表中显示状态为“已创建”（表示尚未转换为工作订单或尚未被放弃）的维护安排行。                                            |
| 打开维护安排池 | 此列表中显示与工作订单池关联的维护安排行。                                                                                                                  |

>[!NOTE]
>如果一个维护安排行包含在多个工作订单池中(请参阅 [工作订单池](../work-orders/work-order-pools.md))，将为 **打开维护安排池** 中的每个池显示一条记录。 这是为了优化工作订单池中的筛选选项。

若要打开一个维护安排：

1. 单击 **资产管理** > **维护安排** > **所有维护安排** 或 **打开维护安排行** 或 **打开维护安排池**。

2. 若要更新维护安排，请单击 **维护计划** 或 **维护阶段**。 

3. 可编辑维护安排行，方法是选择维护安排行，然后单击 **编辑**。 例如，可以轻松更新作业的服务级别或负责工人。 只能编辑尚未与工作订单关联的维护安排行。

4. 可删除维护安排行，方法是在列表页中选择该维护安排行，然后单击 **删除**。

5. 可放弃维护安排行，方法是在列表页中选择该维护安排行，然后单击 **放弃**。 此功能非常有用，例如，当一个资产有 2,000 公里的维护计划和 10,000 公里的维护计划时。 然后，您可能希望放弃基于 2,000 公里维护计划创建，并且与 10,000 公里、 20,000 公里、30,000 公里，以此类推的维护计划一致的行。 如果放弃与某个维护计划关联的维护安排行，安排维护计划时，始终不会再次显示该行。

6. 如果希望选择的所有维护安排行包含在同一个工作订单池中，可以在 **所有维护安排** 中选择一些维护安排行，然后单击 **工作订单池**。

7. 如果要对多个维护安排行进行相同调整，可以在 **所有维护安排** 或 **打开维护安排行** 或 **打开维护安排池** 中选择一些维护安排行，然后单击 **调整安排**。 可更改与所选维护安排行关联的预计开始日期和结束日期，服务级别，以及负责维护工人组或负责维护工人。

- 将维护安排行与工作订单关联之后，将在 **工作订单** 字段中显示工作订单 ID。  
- 可在 **所有资产** 详细信息视图 > **资产维护计划** 快速选项卡上为资产选择维护计划。 以后，如果在 **所有资产** 中删除与资产关联的维护计划行，也将自动删除已根据维护计划创建且状态为“已创建”的所有维护计划行。 另请参阅[创建资产](../objects/create-an-object.md)。

下图显示 **所有维护安排** 列表页。

![图 1.](media/16-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]