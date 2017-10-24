--- 
title: "设置固定资产折旧分摊（中国）"
description: "在日本， 固定资产折旧费用可以被多个部门分摊。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: China (PRC), Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 5868174793c1a613c7a7fe8c8242c4c57b0d0908
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-fixed-asset-depreciation-allocation-china"></a>设置固定资产折旧分摊（中国）

[!include[task guide banner](../../includes/task-guide-banner.md)]

在日本， 固定资产折旧费用可以被多个部门分摊。 



这个任务帮你走一遍如何设置固定资产折旧费用分配流程。 



用于创建此任务的演示数据公司是 JPMF。


## <a name="create-a-fixed-asset-allocation-rule"></a>创建“固定资产分配规则”
1. 选择固定资产>设置>折旧费用分配规则。
2. 单击“新建”。
3. 在“规则 ID”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 在“维度名称”字段中，输入一个值。
6. 单击“添加”。
7. 在“业务单元”字段中，键入一个值。
    * 输入第一个分配目标的信息。  
8. 在“百分比”字段中，输入一个数字。
    * 所有分配目标的合计总数必须为 100。  
9. 在“抵销帐户”字段中，指定所需值。
10. 单击“添加”。
11. 在“业务单元”字段中，键入一个值。
12. 在“百分比”字段中，输入一个数字。
    * 所有分配目标的合计总数必须为 100。  
13. 在“抵销帐户”字段中，指定所需值。
14. 单击“保存”。

## <a name="assign-a-fixed-asset-allocation-rule-to-a-posting-profile"></a>将固定资产分配规则分配给过帐模板。
1. 转到“固定资产”>“设置”>“固定资产过帐模板”。
2. 单击“编辑”。
3. 在“交易类型”字段中，选择“折旧”。
4. 在列表中，找到并选择所需记录。
    * 选择您想要与分配规则链接的记录。  
5. 展开“折旧费用分配规则”部分。
6. 在“资产折旧费用分配”字段中，键入一个值。
7. 单击“保存”。


