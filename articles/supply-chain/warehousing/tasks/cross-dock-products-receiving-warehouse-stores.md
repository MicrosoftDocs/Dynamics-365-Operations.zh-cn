---
title: 将产品从接收仓库越库配送到商店
description: 此程序会逐步演示如何创建和处理越库配送，以将产品从采购订单的收货位置配送到一个或许多商店。
author: Mirzaab
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailBuyersPushPerPackage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e65535a1879eab229f185e0e97d81a304fd292d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572953"
---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a>将产品从接收仓库越库配送到商店

[!include [banner](../../includes/banner.md)]

此程序会逐步演示如何创建和处理越库配送，以将产品从采购订单的收货位置配送到一个或许多商店。 用户可以定义多个配置，并让系统建议如何配送产品，或手动输入物料的配送目的地，以及如何配送到每一个商店。 该程序不包括可用于越库配送的数据的设置，例如补货规则、组织层次结构和商店权重。 该程序使用 USRT 演示公司。

1. 转到“所有采购订单”。
2. 选择列表中的一个采购订单，然后单击链接以打开该订单。
3. 在操作窗格上，单击“Retail 和 Commerce”。
4. 单击“越库配送”。
5. 单击“编辑”。
    * 该类别可用于过滤“行”部分中的物料。  
6. 在列表中，找到并选择所需记录。
7. 在“越库配送数量”字段中，输入一个值，以指定所采购的选定产品的应配送数量。
8. 在“其他越库配送数量”字段中，输入一个值，以指定所采购的可用产品的配送数量
9. 在“配送”字段中，输入“位置权重”。
    * 您可以选择其他类型，以使用其他配送规则。  
10. 在“补货层次结构”字段中，选择一个值。
11. 选择“遵守分类”字段中的“是”。
12. 单击“计算数量”。
13. 单击“创建订单”。
14. 单击“是”。
15. 在列表中，查找和选择一个已收到产品的仓库。
16. 单击“订单”以查看为选定仓库创建的订单



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]