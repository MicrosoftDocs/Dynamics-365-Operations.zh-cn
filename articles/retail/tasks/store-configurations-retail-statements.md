---
title: 零售报表的商店配置
description: 此程序会逐步演示零售商店的配置（这会影响到如何创建和过帐零售报表）。
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9fddeb8434d916df1613d61da88110dec8fb4465
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "354705"
---
# <a name="store-configurations-for-retail-statements"></a>零售报表的商店配置

[!include[task guide banner](../includes/task-guide-banner.md)]

此程序会逐步演示零售商店的配置（这会影响到如何创建和过帐零售报表）。 零售商店的财务维度将在另一个程序中论述。 此程序使用 USRT 演示公司。

1. 转至“零售和商业”>“渠道”>“零售商店”>“所有零售商店”。
2. 在列表中，找到并选择所需记录。
3. 在列表中，单击所选行中的链接。
    * “报表/结算”部分中的设置会影响到商店的报表创建、验证和过帐。  打开“报表/结算”部分。  
    * 选择您想要用于对报表行进行分组的方法。  
    * 如果在从报表创建批处理作业创建报表时，每天仅可创建一份报表，请选择“是”。  
    * “清偿申报计算”字段定义了清偿申报是否应合计或是否应使用最后一个。  
    * 选择将舍入差额过帐到其中的会计科目。  
    * 在“最大舍入差额”字段中，您可以输入允许的最大舍入差额。  
    * 在“过帐”字段中，您可以输入报表允许的最大总过帐差额。  
    * 在“班次”字段中，您可以输入报表班次中的最大总过帐差额。  
    * 在“交易”字段中，您可以输入报表行中的最大总过帐差额。  
    * 在“结算方法”字段中，您可以确定将包括在报表中的交易是已结算的班次的一部分，还是定义的日期/时间范围内的任何交易。  
    * 在“工作日结束时”字段中，您可以输入一个时间，如果午夜之后发生的交易应随前一天过帐。  
    * 如果午夜之后发生的交易应过帐为前一天的一部分，请选择“是”。  
    * 选择“是”，以为定义的每种报表方法创建报表。 如果需要为交易数量高的商店提高过帐性能，这可能很有用，因为它将创建许多可并行处理的较小的报表。  
    * 在“默认客户”字段中，您可以选择客户科目，以用于未经预约而来的客户的销售。  

