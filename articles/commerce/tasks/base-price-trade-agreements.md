---
title: 基价和贸易协议
description: 此程序会逐步演示如何创建渠道特定销售价格贸易协议。
author: josaw1
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bab25988a9d4aad4d4e36fd9bdffbbf52473435e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259450"
---
# <a name="base-price-and-trade-agreements"></a>基价和贸易协议

[!include [banner](../includes/banner.md)]

此程序会逐步演示如何创建渠道特定销售价格贸易协议。 此程序使用 USRT 演示数据公司。

1. 在 **导航窗格** 中，转到 **模块 > Retail 和 Commerce > 定价和折扣管理 > 价格组 > 所有价格组**。 价格组是一种将贸易协议分配给特定渠道的方式。 使用价格组将贸易协议分配给某一渠道会启用渠道特定价格。  
2. 单击 **新建**。
3. 在 **价格组** 字段中，输入一个值。
4. 在 **名称** 字段中，键入一个值。
5. 单击 **保存**。
6. 关闭该页面。
7. 在 **导航窗格** 中，转到 **模块 > Retail 和 Commerce > 渠道 > 商店 > 所有商店**。
8. 在列表中，选择“纽约”。
9. 单击“操作窗格”上的 **商店**。
10. 单击 **价格组**。
11. 单击 **新建**。
12. 在 **价格组** 字段中，单击下拉按钮以打开查找。
13. 在列表中，找到并选择所需记录。
14. 单击 **保存**。
15. 关闭该页面。
16. 关闭该页面。
17. 在 **导航窗格** 中，转到 **模块 > Retail 和 Commerce > 产品和类别 > 已发布的产品(按类别)**。
18. 在列表中，单击所选行中的链接。
19. 单击 **编辑**。
20. 展开 **销售** 快速选项卡。
21. 在 **价格** 字段中，输入一个数字。 如果未找到任何适用的贸易协议，则会使用此价格。  
22. 单击 **保存**。
23. 在 **操作窗格** 上，单击 **销售**。
24. 单击 **创建贸易协议**。
25. 单击 **新建**。
26. 在 **名称** 字段中，单击下拉按钮以打开查找。
27. 在列表中，选择 **Commerce**。 在演示数据中，**Commerce** 日记帐名称拥有默认关系 **价格(销售)**。 这意味着所有新建的行将默认设置为销售价格贸易协议。  
28. 在 **操作窗格** 上，单击 **行**。
29. 在 **当事方代码类型** 字段中，选择“组”。
30. 在 **帐户选择** 字段中，单击下拉按钮以打开查找。
31. 在列表中，找到并选择所需记录。 这将完成从渠道到价格组再到贸易协议的链接。  
32. 在 **物料关系** 字段中，输入一个值。
33. 在 **货币金额** 字段中，输入一个数字。
34. 在 **详细信息** 快速选项卡中，选中或取消选中 **查找下一个** 复选框。 在 **查找下一个** 被设置为“是”时，定价引擎将继续检索销售价格更低的适用贸易协议。 在 **查找下一个** 被设置为“否”时，价格引擎会停止检索并使用该贸易协议。  
35. 单击 **过帐**。
36. 单击 **确定**。
37. 关闭该页面。
38. 在 **操作窗格** 上，单击“销售”。
39. 单击 **销售价**。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]