---
title: 零售报表的商店配置
description: 此程序会逐步演示商店的配置（这会影响到如何创建和过帐商业报表）。
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1670a1a102f9288cdbd0e4cc981e3aa927d1ad9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232657"
---
# <a name="store-configurations-for-retail-statements"></a>零售报表的商店配置

[!include [banner](../includes/banner.md)]

此程序会逐步演示商店的配置（这会影响到如何创建和过帐商业报表）。 商店的财务维度将在另一个程序中论述。 此程序使用 USRT 演示公司。

1. 在 **导航窗格** 中，转到 **模块 > Retail 和 Commerce > 渠道 > 商店 > 所有商店**。
2. 在列表中，找到并选择所需记录。
3. 在列表中，单击所选行中的链接。
4. 单击 **编辑**。
5. **报表/结算** 快速选项卡中的设置会影响商店的报表创建、验证和过帐。 展开 **报表/结算** 快速选项卡。  
6. 在 **报表方法** 字段中，选择您想要用于报表行分组依据的方法。  
7. 如果在从报表创建批处理作业创建报表时，每天仅可创建一份报表，请在 **每天一个报表** 中选择“是”。  
8. **清偿申报计算** 字段定义了清偿申报是否应合计或是否应使用最后一个。  
9. 在 **舍入** 字段中，选择将舍入差额过帐到其中的会计科目。  
10. 在 **最大舍入差额** 字段中，输入允许的最大舍入差额。
11. 在 **过帐** 字段中，输入报表允许的最大总过帐差额。
12. 在 **班次** 字段中，输入报表班次中的最大总过帐差额。  
13. 在 **交易** 字段中，输入报表行中的最大总过帐差额。  
14. 在 **结算方法** 字段中，定义将包括在报表中的交易是已结算的班次的一部分，还是定义的日期/时间范围内的任何交易。  
15. 在 **工作日结束时** 字段中，输入一个时间，如果午夜之后发生的交易应随前一天过帐。  
16. 如果午夜之后发生的交易应过帐为前一天的一部分，请在 **按工作日过帐** 中选择“是”。  
17. 在 **按报表拆分方法** 中选择“是”，以为定义的每种报表方法创建报表。 如果需要为交易数量高的商店提高过帐性能，此操作可能很有用，因为它将创建许多可并行处理的较小的报表。  
18. 在 **常规** 快速选项卡的 **默认客户** 字段中，您可以选择客户帐户，以用于上门客户的销售。  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]