---
title: 设置固定资产折旧费用分配
description: 在日本， 固定资产折旧费用可以被多个部门分摊。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetAllocationRuleSetup_CN,  AssetPosting
audience: Application User
ms.reviewer: kfend
ms.search.region: China (PRC), Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c80b9d25092e7329f2e37b66fd7b9c8a44cf0509
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821763"
---
# <a name="setup-fixed-asset-depreciation-allocation"></a>设置固定资产折旧费用分配

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]