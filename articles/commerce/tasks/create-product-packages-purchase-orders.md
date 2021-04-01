---
title: 创建采购订单的产品包装
description: 此程序会逐步演示如何创建产品包装，以及在采购订单上使用它。
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d16c5c576ce6b35687fb7edab835d52f6f58e6a0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256965"
---
# <a name="create-product-packages-for-purchase-orders"></a>创建采购订单的产品包装

[!include [banner](../includes/banner.md)]

此程序会逐步演示如何创建产品包装，以及在采购订单上使用它。 采购订单将被用于创建预定义集合产品的订单。 此程序使用 USRT 演示数据公司。


## <a name="create-a-product-package"></a>创建产品包装
1. 转至“Retail 和 Commerce”>“库存管理”>“补货”>“产品包装”。
2. 单击“新建”。
3. 在“包装编号”字段中，输入一个值。
4. 在“描述”字段中，键入一个值。
5. 在“供应商帐户”字段中，单击下拉按钮以打开查找。
6. 在列表中，单击所选行中的链接。
7. 单击“添加”。
8. 在“物料编号”字段中，输入“0160”。
9. 在“尺寸”字段中，单击下拉按钮以打开查找。
10. 在列表中，单击所选行中的链接。
11. 在“数量”字段中，输入一个数字。
12. 单击“添加”。
13. 在“物料编号”字段中，输入“0160”。
14. 在“变型编号”字段中，单击下拉按钮以打开查找。
15. 在列表中，单击所选行中的链接。
16. 在“数量”字段中，输入一个数字。
17. 单击“添加”。
18. 在“物料编号”字段中，输入“0175”。
19. 在“数量”字段中，输入一个数字。
20. 单击“保存”。
21. 关闭该页面。

## <a name="add-package-to-purchase-order"></a>将包装添加到采购订单
1. 转到“应付账款”>“采购订单”>“所有采购订单”。
2. 单击“新建”。
3. 在“供应商帐户”字段中，单击下拉按钮以打开查找。
4. 如果已选定一个供应商，则在列表中，选择以前曾为其创建产品包装的同一供应商。
5. 切换“概况”部分的扩展。
6. 在“位置”字段中，单击下拉按钮打开查询。
7. 在列表中，单击所选行中的链接。
8. 在“仓库”字段，单击下拉按钮以打开查找。
9. 在列表中，单击所选行中的链接。
10. 单击“确定”。
11. 切换“行详细信息”部分的扩展。
12. 单击“产品包装”选项卡。
13. 单击“采购订单行”。
14. 单击“从包装中创建行”。
15. 在列表中，查找并选择在上一步中创建的产品包装。
16. 在“数量”字段中，输入一个数字。
17. 单击“创建”。
18. 单击“保存”。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]