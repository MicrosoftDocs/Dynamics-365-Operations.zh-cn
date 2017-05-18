---
title: "成本对象"
description: "本文提供有关成本对象的信息，并说明如何累计成本和数量。 成本对象是为其累计成本和数量的实体。 成本对象实体可以是产品或产品变型，例如样式和颜色的变型。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 42d7ba8a41840024dc16df6863ba5eabd9c37c09
ms.contentlocale: zh-cn
ms.lasthandoff: 04/25/2017


---

# <a name="cost-objects"></a>成本对象

[!include[banner](../includes/banner.md)]


本文提供有关成本对象的信息，并说明如何累计成本和数量。 成本对象是为其累计成本和数量的实体。 成本对象实体可以是产品或产品变型，例如样式和颜色的变型。  

<a name="cost-objects"></a>成本对象
------------

**“成本对象”**页面列出在某个产品上登记的所有成本对象。 成本对象由来自以下源的数据定义：

-   产品
-   产品维度组
-   存储维度组
-   跟踪维度组

**注意：**成本对象仅表示**“直接材料”**类型的成本元素。 成本对象和库存对象在为财务库存所选的库存维度定义成本对象的方式上存在差异。 例如，某个物料具有以下配置：

-   **站点：**Physical inventory = Yes, Financial inventory = Yes
-   **仓库：**Physical inventory = Yes, Financial inventory = No
-   **批号：**Physical inventory = Yes, Financial inventory = No

下表显示了成本对象和库存对象的定义。

| 对象类型      | 物料编号 | 站点 | 仓库 | 批号 |
|------------------|-------------|------|-----------|-----------|
| 成本对象      |  x           |  x    |           |           |
| 库存对象 |  x           |  x    |   x        |  x         |

## <a name="accumulation-of-costs-and-quantities"></a>成本和数量的累计
-   **“值”**字段中的值为以下值的和：
    -   实际成本额
    -   财务成本额
    -   调整
-   **“数量”**字段中的值为以下值的和：
    -   已接收
    -   已扣除
    -   已过帐的数量
-   **“平均单位成本”**字段为计算字段。 该值通过用**“值”**值除以**“数量”**值得出。

**注意：****包括实际成本** 参数不影响之前的计算。

<a name="see-also"></a>请参阅
--------

[产品维度组](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[存储维度组](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[跟踪维度组](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[Microsoft Dynamics AX 中的新增功能和变更功能](/dynamics365/operations/dev-itpro/get-started/whats-new-changed)

[成本条目](cost-entries.md)




