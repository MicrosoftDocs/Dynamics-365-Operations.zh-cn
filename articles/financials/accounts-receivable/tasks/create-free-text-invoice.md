--- 
title: "创建普通发票"
description: "此任务指南演示如何创建普通发票。"
author: mikefalkner
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ef3cad6538d9efbd1c1881f4b7d771382d9b1ba8
ms.openlocfilehash: 87e293008fd748aa0dcc6b3caa94a4889bed35de
ms.contentlocale: zh-cn
ms.lasthandoff: 10/26/2017

---
# <a name="create-a-free-text-invoice"></a>创建普通发票

[!include[task guide banner](../../includes/task-guide-banner.md)]

此任务指南演示如何创建普通发票。 本任务使用 USMF 公司进行演示。

1. 转到“应收账款”>“发票”>“所有普通发票”。
2. 单击“新建”。
3. 在“客户帐户”字段中，选择一个值。
    * 发票帐户将默认为用于客户帐户的同一帐户。   
    * 如果发票未过帐，会计状态最开始为“进行中”。   
    * 发票过帐后，将分配发票编号。  
    * 如果您使用 SEPA 授权，当您选择客户帐户时，直接借记授权将自动填充授权。  
4. 在“描述”字段中，键入一个值。
5. 在“主科目”字段中，指定没有维度的帐号。
    * 您还可以为主科目输入一个或多个字符，并使用查找功能查找科目。 您稍后将在此指南输入维度。  
6. 展开“行明细”快速选项卡，以便您可以将维度添加到主科目。
7. 单击“财务维度行”选项卡。
    * 这些维度仅适用于所选行。    
    * 销售税组将从客户处填充信息。 如果客户没有销售税组，则使用主科目的销售税组信息。  
    * 物料销售税组根据主科目填充。 如果主科目没有物料销售税组，则使用“总帐中销售税参数”中的物料销售税组。    
8. 在“数量”字段中，输入一个数字。
    * 数量为可选项。  
9. 在“单位价格”字段中，输入一个数字。
    * 单位价格为可选项。  
    * 此金额计算为数量乘以单位价格。 不过，您可以覆盖计算值，另外输入一个金额。  
10. 单击“销售税”查看为您的发票计算的销售税。
    * 在此页查看销售税金额，您也可以在“调整”选项卡上覆盖这些金额。  
11. 单击“确定”。
12. 单击“费用”，以添加费用到您的发票中。 
13. 在“费用代码”字段中，输入一个值。
14. 在“费用数值”字段中，输入一个数目。
15. 关闭该页面。
16. 单击“总计”查看汇总的发票详细信息和总计。
17. 单击“关闭”。
18. 单击“过帐”过帐该发票。 在过帐前，您可以取消。
    * 更改发票打印时的时间：选择“当前”（各发票更新后即打印），或选择“之后”（在更新所有发票后打印）。  
    * 如果要更改过帐前客户信用额度的检查方式，则更改“信用额度”类型。  
    * 如果您要打印发票，则选择“是”。  
    * 如果您要将发票过帐，则选择“是”。 您可以打印未过帐发票。  
19. 单击“确定”。


