---
title: 创建普通发票模板
description: 此过程说明如何创建普通发票模板。
author: abruer
ms.date: 02/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7baa29ad341bdf7ff874bd7f69cf483b7afc075a
ms.sourcegitcommit: 6102f70d4595d01b90afe5b23dfd8ec2ea030653
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/16/2022
ms.locfileid: "8182501"
---
# <a name="create-a-free-text-invoice-template"></a>创建普通发票模板

[!include [banner](../includes/banner.md)]

对于本演练，请使用 USMF 演示公司数据。 该过程由负责管理和处理“应收帐款”发票的用户负责。

## <a name="create-a-template"></a>创建模板

1. 转到 **应收帐款 > 发票 > 循环发票 > 普通发票模板**。
    * 使用此页面创建普通发票模板，可包括发票行、费用、会计分配模板和分类帐户信息。  
2. 单击 **新建**，创建新的普通发票模板。
3. 在 **模板名称** 字段中，键入一个值。
    * “模板名称”为一个普通发票模板的唯一标识。 两个模板不能具有相同的“模板名称”。  
4. 在 **描述** 字段中，输入模板组描述。
5. 展开 **发票行** 的选项卡。
6. 在 **描述** 字段中，输入发票行描述。
7. 在 **主要帐户** 字段中，选择一个收入帐户。
    * 您可以在选择的客户抵消交易帐户，来确定 **客户过帐模板** 页的发票总额。  
8. 在 **销售税组** 字段中，单击下拉按钮以打开查找。
    * 当前发票行的销售税组，是客户帐户的默认销售税组。  
9. 在列表中，单击所选行中的链接。
10. 在 **物料税务组** 字段中，选择当前发票行的物料销售税额。
11. 在列表中，单击所选行中的链接。
12. 在 **单位价格** 字段中，输入或查看发票行的每计价单位的价格
    * 此金额乘以 **数量** 字段中的值来确定发票行金额。  
13. 在普通发票模板上添加新行。
14. 在 **描述** 字段中，输入发票行描述。
15. 在 **主要帐户** 字段中，选择一个收入帐户。
    * 您可以在选择的客户抵消交易帐户，来确定 **客户过帐模板** 页的发票总额。  
16. 在 **销售税组** 字段中，单击下拉按钮以打开查找。
    * 当前发票行的销售税组，是客户帐户的默认销售税组。  
17. 在列表中，单击所选行中的链接。
18. 在 **物料销售税组** 字段中，单击下拉按钮以打开查找。
    * 当前发票行的物料销售税组。  
19. 在列表中，单击所选行中的链接。
20. 输入或查看发票行的单位数。
    * 该数字乘以“单位价格”字段中的值来确定发票行金额。  
21. 输入或查看发票行的单位价格。 
    * 该金额乘以 **数量** 字段中的值来确定发票行金额。  
22. 查看和修改单独行和所有子行的会计分配。
    * 会计分配定义如何对帐金额，例如将如何对帐普通发票中的收入、税金或费用。  
23. 更新已选发票行的会计分配。
24. 单击 **关闭**。

## <a name="save-a-free-text-invoice-as-a-template"></a>将普通发票保存为模板
也可以将现有普通发票保存为模板。 从 **发票** 选项卡选择 **保存到模板** 时，请为模板提供名称和说明。 如果有同名模板，将看到通知，说明已存在该名称的模板。 仍然可以单击 **确定** 替换该模板。 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
