---
title: 成批创建销售报价单
description: 该过程演示如何有效创建发送一组产品或服务给多个客户的报价单。
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm, SalesQuickQuote
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 227ff0dd03f8917f4551ce08067ef26c6204b059
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422798"
---
# <a name="mass-create-sales-quotations"></a>成批创建销售报价单

[!include [banner](../../includes/banner.md)]

该过程演示如何有效创建发送一组产品或服务给多个客户的报价单。 此成批报价单创建基于报价单模板。 您可以使用演示数据公司 USMF 或您自己的数据运行该过程。


## <a name="create-a-quotation-template"></a>创建报价单模板
1. 转到“销售和市场”>“设置”>“报价单”>“模板组”。
2. 单击“新建”。
3. 在“组 ID”字段中，键入您所选择的 ID。
4. 在“描述”字段中，键入一个值。
5. 单击“保存”。
6. 关闭该页面。
7. 转到“销售和市场营销”>“销售报价单”>“所有报价单”。
8. 单击“新建”。
9. 在“帐户类型”字段中选择“客户”。
10. 在“客户帐户”字段中，输入或选择一个值。
11. 单击“确定”。
    * 对于用作模板的报价单，您必须在报价单标题执行设置步骤。 这必须在您添加行到报价单前完成。   
12. 在“操作窗格”上，单击“选项”。
13. 单击“更改”视图。
14. 单击“标题”视图。
15. 展开“设置”部分。
16. 在“组 ID”字段中，输入或选择一个值。
17. 在“模板名称”字段中，键入一个值。
18. 在“有效”字段中选择“是”。
    * 在您应用模板到新销售报价单时，仅可使用有效的模板。  
19. 在“操作窗格”上，单击“选项”。
20. 单击“更改”视图。
21. 单击“查看行”。
22. 在“物料”字段中，输入或选择一个值。
23. 在“物料”字段中，键入一个值。
24. 关闭该页面。
25. 在“折扣百分比”字段中，输入一个数字。
26. 单击“添加行”。
27. 在“物料”字段中，输入或选择一个值。
28. 在“物料”字段中，键入一个值。
29. 关闭该页面。
30. 在“单位价格”字段中，输入新价格或更改当前价格。
31. 单击“添加行”。
32. 在“物料”字段中，输入或选择一个值。
33. 在“物料”字段中，键入一个值。
34. 关闭该页面。
35. 在“数量”字段中，输入一个数字。
36. 在“折扣”字段中，输入一个数字。
37. 单击“保存”。

## <a name="apply-the-template-to-create-a-single-quotation"></a>使用该模板创建单个报价单
1. 转到“销售和市场营销”>“销售报价单”>“所有报价单”。
    * 请注意，您刚刚创建的报价单标记为了模板。  
2. 单击“新建”。
3. 在“帐户类型”字段中选择“客户”。
4. 在“客户帐户”字段中，输入或选择一个值。
5. 展开“模板”部分。
6. 在“组 ID”字段中，输入或选择一个值。
7. 在“模板名称”字段中，输入或选择一个值。
8. 在“计算方法”字段中，选择“基于模板的值”。
9. 单击“确定”。
    * 新报价单已根据模板的数据和条款创建。  
10. 关闭该页面。
11. 关闭该页面。

## <a name="apply-the-template-to-mass-create-quotations"></a>使用该模板批量创建报价单
1. 转到“销售和市场”>“销售报价单”>“报价单更新”>“批量创建报价单”。
2. 在“帐户类型”字段中选择“客户”。
3. 在“组 ID”字段中，输入或选择一个值。
4. 在“模板名称”字段中，输入或选择一个值。
5. 在“计算方法”字段中，选择“基于模板的值”。
6. 扩展“要包括的记录”部分。
7. 单击“筛选器”。
8. 在“条件”字段中，设置筛选器，使其涵盖您想加入到批量报价单创建中的各种客户。 使用以下格式“客户 1……客户 N”。
    * 例如，您可以设置筛选器为：US-001..US-004  
9. 单击“确定”。
10. 单击“确定”。
11. 转到“销售和市场营销”>“销售报价单”>“所有报价单”。
    * 核实已根据所选的模板，为成批更新程序中指定的所有客户创建报价单。  

