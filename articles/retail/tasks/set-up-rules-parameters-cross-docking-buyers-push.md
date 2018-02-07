--- 
title: "设置越库配送和集中采购配送的规则和参数"
description: "此程序会演示补货规则的创建步骤。"
author: josaw1
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1ff41a18be066b6f32c5172bda38c389e7f34128
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a>设置越库配送和集中采购配送的规则和参数

[!include[task guide banner](../includes/task-guide-banner.md)]

此程序会演示补货规则的创建步骤。 在使用越库配送和集中采购配送时，补货规则可用于控制如何将产品配送到商店。 可以为商店或商店组设置补货规则。 在使用补货规则作为越库配送或集中采购配送的配送方法时，规则内为每一行定义的权重将控制如何在商店之间分配产品的数量。 此程序使用 USRT 演示公司。

1. 转至“补货规则”。
2. 单击“新建”。
3. 在“补货规则”字段中，输入一个值。
4. 在“描述”字段中，键入一个值。
5. 单击“保存”。
6. 单击“添加”。
7. 在列表中，标记所选的行。
    * 您可以选择“补货层次结构”或“渠道”类型。 该值可以控制“名称”中的选择是渠道层次结构还是特定渠道。  对于本示例，将它设置为“补货层次结构”。  
8. 在“名称”字段中，选择一个值。
    * 默认权重值使用仓库定义的权重进行填充。  此权重可用于补货规则，或者您可以在“权重”字段中输入一个新的权重。  
9. 在“权重”字段中，输入一个数字。
10. 单击“添加”。
11. 在列表中，标记所选的行。
12. 在“类型”字段中，选择“渠道”。
13. 在“名称”字段中，输入或选择一个值。
14. 在“权重”字段中，输入一个数字。
15. 单击“保存”。


