---
title: 使用集中采购配送将产品从配送中心配送到商店
description: 此程序会逐步演示如何创建和处理集中采购配送，以将产品从一个位置配送到一个或许多商店。
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailBuyersPush, InventLocationIdLookup, InventItemIdLookupSimple, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3720945823cf127f776a9ea6a6ad75a72ceec00c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012333"
---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a>使用集中采购配送将产品从配送中心配送到商店

[!include [banner](../includes/banner.md)]

此程序会逐步演示如何创建和处理集中采购配送，以将产品从一个位置配送到一个或许多商店。 用户可以定义多个配置，并让系统建议如何配送产品，或手动输入物料的配送目的地，以及如何配送到每一个商店。 此程序不包括可用于集中采购配送的数据的设置，例如补货规则、组织层次结构和商店权重。 此程序使用 USRT 演示公司。

1. 转至“集中采购配送”。
2. 单击“新建”。
3. 在“描述”字段中，键入一个值。
4. 在“站点”字段中，输入或选择一个值。
5. 在“仓库”字段中，输入或选择一个带有库存数量的产品的仓库。
6. 单击“添加”。
7. 在列表中，标记所选的行。
8. 在“物料编号”字段中，输入或选择一个产品。
9. 单击“添加”。
10. 在列表中，标记所选的行。
11. 在“物料编号”字段中，输入或选择一个变型产品。
    * 在输入变型产品时，将会为每个变型产品创建行。  
12. 在列表中，标记一行。
13. 在“已配送数量”字段中，输入您想要配送的选定产品的数量。
14. 在“其他配送数量”字段中，输入拥有可用配送数量的产品的数量。
15. 在“配送”字段中，输入“位置权重”。
    * 您可以选择其他类型，以使用其他配送规则。  
16. 在“补货层次结构”字段中，选择一个值。
17. 选择“遵守分类”字段中的“是”。
18. 单击“计算数量”并审查已添加到“仓库”部分的行中的数量。
19. 单击“创建订单”。
20. 单击“是”。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]