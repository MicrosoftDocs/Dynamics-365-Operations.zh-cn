---
title: 设置中国的基本税务集成模板
description: 此过程显示如何设置税务集成模板，更新有关颁发增值税发票的客户设置，以及为中国设置增值税发票说明。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxProfileTable_CN, HcmWorkerLookUp, UnitOfMeasureLookup, CustTable, LogisticsPostalAddress, TaxGroupLookup, VATInvoiceDescTable_CN
audience: Application User
ms.reviewer: kfend
ms.search.region: China (PRC)
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ad39f0142acf124507816ef09a352859eb4836b4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205456"
---
# <a name="set-up-basic-tax-integration-profile-for-china"></a>设置中国的基本税务集成模板

[!include [banner](../../includes/banner.md)]

此过程显示如何设置税务集成模板，更新有关颁发增值税发票的客户设置，以及为中国设置增值税发票说明。

必须先完成“金税集成导入设置”过程和“维护金税导出格式”过程，才能完成此过程。

本流程是用演示公司 CNMF 数据生成的。 此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。

1. 转到“税金”>“设置”>“税务集成”>“税务集成模板”。
2. 单击“新建”。
3. 在“模板 ID”字段中，键入一个值。
4. 在“模板名称”字段中，键入一个值。
5. 在“销售税代码”字段中，输入或选择一个值。
6. 在“验证金额限制”字段中选择“是”。
7. 在“最大发票金额”字段中，输入一个数字。
8. 在“含税”字段中选择“是”。
9. 在“默认商品”字段中，键入一个值。
10. 在“复核”字段中，输入或选择一个值。
11. 在“收款”字段中，输入或选择一个值。
12. 在“格式映射”字段中，输入或选择一个值。
13. 在“普通增值税发票”字段中选择“是”。
14. 展开“描述和单位的缺省值”部分。
15. 单击“新建”。
16. 在列表中，标记所选的行。
17. 在“描述”字段中，键入一个值。
18. 在“单位”字段中，输入或选择一个值。
19. 转到“应付帐款”>“客户”>“所有客户”。
20. 选择一个客户。
21. 单击“登记 ID”。
22. 单击“添加”。
23. 在“登记类型”字段中，输入或选择一个值。
24. 改变登记类型。
25. 在“登记编号”字段中，键入一个值。
26. 单击“保存”。
27. 关闭该页面。
28. 展开“发票和交货”部分。
29. 单击“编辑”。
30. 在“销售税组”字段，输入或选择一个值。
31. 转到“税金”“设置”>“税务集成”>“增值税发票描述”。
32. 单击“新建”。
33. 在“增值税发票描述 ID”字段中，输入一个值。
34. 在“描述”字段中，键入一个值。
35. 在“单位”字段中，输入或选择一个值。
36. 单击“保存”。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]