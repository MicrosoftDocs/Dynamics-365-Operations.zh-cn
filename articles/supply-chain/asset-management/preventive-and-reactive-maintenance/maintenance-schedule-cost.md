---
title: 维护安排成本
description: 本主题介绍资产管理中的维护安排成本。
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
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
ms.openlocfilehash: b2f53a4a64b06efc9269c607bfe1fc3a41c90cdd
ms.sourcegitcommit: 6476f27c8d3dced7c2e9a7344a4e378b51a1983e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/27/2019
ms.locfileid: "1922060"
---
# <a name="maintenance-schedule-cost"></a>维护安排成本

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

在资产管理中，可计算维护安排行的预算成本。 如果要获取预计成本（如与为下一年计划的预防性维护作业有关的成本）的概览，这非常有用。 此类计算基于类型为“维护计划”和“维护阶段”与“维护请求”的现有维护安排行。

1. 单击**资产管理** > **查询** > **资产** > **维护安排成本**。

2. 如果要查看按财务维度分组的成本，可在**维护安排成本**对话框中选择**财务维度集**。

>[!NOTE]
>财务维度集在**总帐** > **会计科目表** > **维度** > **财务维度集**中设置。

3. 可使用**级别**字段指示要与功能位置有关的维护安排行的详细程度。 例如，如果在字段中插入数字“1”，并且采用了多级别功能位置结构，则将在最上级别显示某个功能位置的所有维护安排行，因此，可以从较低级别的功能位置叠加行中的工时。 如果在**级别**字段中插入数字“0”，将看到详细结果，其中显示其关联的所有功能位置级别的所有维护安排行。

4. 如果要对特定资产进行计算，请单击**要包括的记录**快速选项卡上的**筛选**，然后选择相关资产。 如果需要，也可以为成本计算指定**预计的开始日期**，或为成本计算选择其他**状态**

5. 单击**确定**开始计算成本。

6. 在**维护安排成本**选项卡上 > **分组依据**操作窗格组中，单击相关按钮显示所需成本计算详细程度。 将突出显示所选操作窗格组按钮。 单击按钮将其激活或停用。

7. 如果要进行新的成本计算，请单击**计算成本**按钮。

下图显示维护安排成本计算的结果。

![图 1](media/17-preventive-maintenance.png)
