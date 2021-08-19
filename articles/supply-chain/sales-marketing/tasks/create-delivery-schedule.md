---
title: 创建交货计划
description: 此过程显示如何为销售订单创建交货计划。
author: omulvad
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesDeliverySchedule, SalesEditLines,  SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 815d474f37630852e09edefbee220266dd8ad12fdcbdd48a2b58122859b259f6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733388"
---
# <a name="create-delivery-schedule"></a>创建交货计划

[!include [banner](../../includes/banner.md)]

此过程显示如何为销售订单创建交货计划。 在请求在多个装运中交付订单或报价单上的数量时，使用交货计划。 您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。


## <a name="create-delivery-schedule"></a>创建交货计划
1. 转到“所有销售订单”。
2. 单击“新建”。
3. 在“客户帐户”字段中，输入或选择一个值。
4. 单击“确定”。
5. 在“物料编号”字段中，输入或选择一个值。
6. 在“数量”字段中，输入大于 1 的数字。
7. 单击“销售订单行”。
8. 单击“交货计划”。
    * “交货计划”页是您可以指定装运数量的位置，订单行的总数量将会交付给客户。    
    * 默认情况下，系统将复制总数量和原始销售行的交付详细信息到交货计划第一行。 在此示例中，我们为两个装运创建一个计划，第一个装运日期抵消第二个装运日期一周。  
9. 在“数量”字段中，输入为总数量的一部分的数字。
10. 单击“新建”。
11. 在“数量”字段中，输入剩余数量。
12. 在“要求装运日期”字段中，输入第一行交货日期前一周的日期。
    * 一旦已分配费用至原始订单行，“费用转换”快速选项卡上的两个选项控制您想要分配到交货计划行上的费用。 如果已选择“复制总额”，同一费用金额将复制到每行。 对于“分配到交货行”选项，其将费用平均分摊到交货行。  
    * 只可以拆分固定费用，而仍将可变费用复制到这些行。  
13. 将光标远离第二个交货行，以更新页面。
    * 您可以通过查看“总计”和“剩余”字段，跟踪查看分配到交货计划行的总数量。 在剩余数量为零时，原始行的全部数量已分配到计划中。   
14. 单击“确定”。
    * 交货计划现在已复制到订单行。   
    * 原始订单行，即业务行，已转换为具有多个交货项的订单行。 其将标有不同图标，且作为交货行的抬头。  
    * 这两个新行（即交货行）共同构成一个交货计划。 该订单将处理这些新行，而不是原始行。 如果打印单据（如确认单、领料单、装箱单或发票），则只显示交货行。   
    * 交货行可以有不同的交货日期、数量、交货方式以及站点和仓库等存储维度。 但是，产品维度必须始终与业务行上维度一致，且不能更改。  
15. 在“数量”字段中，输入大于当前数字的数字。
16. 选择业务行，以查看数量重新计算的影响。
17. 在操作窗格中，单击“领料和装箱”。
18. 单击“发布装箱单”。
19. 展开“参数”部分。
20. 在“数量”字段中，选择“所有”。
    * 请注意，将为两个交货计划行，而不是原始订单行创建装箱单。  
21. 在“打印装箱单”字段选择“是”。
22. 单击“确定”。
23. 单击“是”。
24. 关闭该页面。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]