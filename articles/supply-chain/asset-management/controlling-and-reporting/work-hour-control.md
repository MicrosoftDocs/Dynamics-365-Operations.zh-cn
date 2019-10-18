---
title: 工时控制
description: 本主题介绍资产管理中的工时控制。
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
ms.openlocfilehash: 916e7b8d5d494dbae0659504957f7f0798a6834b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918364"
---
# <a name="work-hour-control"></a>工时控制

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

在资产管理中，可计算工时，以便获取资产、功能位置或工作订单的实际工时与预算工时的比较概览。 实际工时基于过帐的交易记录。

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a>资产、功能位置和工作订单的工时控制

为资产、功能位置和工作订单创建的计算几乎相同。 唯一区别是，对于资产和功能位置，还可以在计算中包括子资产和子位置。 日期是记录登记时的交易记录日期。

1. 单击**资产管理** > **查询** > **资产** > **资产工时控制**或**功能位置工时控制**，或**资产管理** > **查询** > **工作订单** > **工作订单工时控制**。

2. 在**资产工时控制**对话框中，

3. 在**资产工时控制** / **功能位置工时控制** / **工作订单工时控制**对话框中的**开始日期**和**结束日期**字段中，选择要计算的期间。

4. 如果需要，选择计算中要包括的**财务维度集**。

5. 如果不希望显示包含零工时的结果，请在**忽略零**切换按钮上选择“是”。

6. 可使用**级别**字段指示要与功能位置有关的工时控制行的详细程度。 例如，如果在字段中插入数字“1”，并且采用了多级别功能位置层次结构，则将在最上级别显示某个功能位置的所有工时控制行，因此，可以从较低级别的功能位置叠加行中的工时。 如果在**级别**字段中插入数字“0”，将看到详细结果，其中显示其关联的所有功能位置级别的所有工时控制行。

7. 若要将与子资产关联的成本显示为单独行，请在**包括子资产**切换按钮上选择“是”。

8. 如果要限制搜索，可在**要包括的记录**快速选项卡上选择特定资产/功能位置/工作订单。

9. 单击**确定**开始计算。

10. 在**资产工时控制**页上的**分组依据**操作窗格组中，单击相关按钮显示计算的所需详细程度。 将突出显示所选操作窗格按钮。 单击按钮将其激活或停用。

下图显示**资产工时控制**计算的示例。

![图 1](media/04-controlling-and-reporting.png)

另外一种创建工时计算的方法是在**所有资产**或**有效资产**中选择多个资产。 然后单击**常规**快速选项卡上的**工时控制**按钮。 将在**要包括的记录**快速选项卡上的**资产**字段中自动插入所选资产。 单击**资产工时控制**对话框中的**确定**，然后将显示所选资产的计算。 可以在**所有功能位置**或**有效功能位置**中对功能位置执行同样的过程，也可以在**所有工作订单**或**有效工作订单**中对工作订单执行同样的过程。

>[!NOTE]
>**原始预算**字段显示工作订单预测中的预算工时。 **实际工时**字段显示工作订单中的已过帐工时。 **承诺工时**字段显示在与工作订单关联时，公司承诺的工时总量。
