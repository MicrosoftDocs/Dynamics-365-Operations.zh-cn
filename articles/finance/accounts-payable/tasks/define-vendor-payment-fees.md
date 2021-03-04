---
title: 定义供应商付款费用
description: 设置供应商付款费用。
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 404bd1e22caa8098f114a2dcc67dd420509cce2b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440593"
---
# <a name="define-vendor-payment-fees"></a>定义供应商付款费用

[!include [banner](../../includes/banner.md)]

设置供应商付款费用。 本任务使用 USMF 公司进行演示。

1. 转到“应付帐款”>“付款设置”>“付款费用”。
2. 单击“新建”。
3. 在“费用 ID”字段中，输入一个值。
    * “费用 ID”应描述何时使用此费用，如“EFT_Fee”。  
4. 在“名称”字段中，键入一个值。
5. 在“费用描述”字段中，键入一个值。
    * 添加描述以提供何时评估费用的更多详细信息。  
6. 在“支付”字段中，选择“供应商”或“分类帐”。
    * 当向贵组织支付该费用时，请使用“分类帐”。  当评估供应商费用时，请使用供应商。  
7. 在费用支付位置输入一个主要帐号。
    * 只有在费用选项中选择“分类帐”时，此选项才可用。  
8. 选择可供该费用使用的日记帐。 
    * 对于供应商付款费用，您可以选择“供应商支付”日记帐。  
9. 单击“保存”。
10. 单击“付款费用”设置。
    * 继续在“付款费用”设置中，定义何时将该费用设置为所选日记帐的默认项。  
11. 选择“表单”、“组”或“所有”。
    * “表单”用于选择一个单一的银行帐户，“组”用于选择一个银行组，“所有”是将此费用设置应用于所有银行帐户。  
12. 选择某一银行组或某一银行帐户。
    * 如果您选择的为“组”，查找操作将显示银行组；如果您选择的为“表单”，查找操作将显示银行帐号。  
13. 选择用于评估该费用时的付款方式。
14. 选择当前付款方式的“付款说明”。
    * 电子资金转帐付款方式应遵循“付款说明”。  
15. 选择费用是为百分比、金额或间隔。
16. 输入费用的百分比或金额。
    * 如果“费用”为百分比，则输入百分比。 如果“费用”为金额，则输入该费用金额。 如果“费用”为间隔，则使用“间隔选项卡”定义分层费用。  
17. 在“费用币种”字段中，选择评估费用的币种。
    * 该币种用于费用。 付款币种用于定义，基于付款的币种，应何时评估支出规则。 例如，当使用欧元付款时，您选择的银行可能会收取费用，但对于其他付款将不会评估费用。  
18. 单击“保存”。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]