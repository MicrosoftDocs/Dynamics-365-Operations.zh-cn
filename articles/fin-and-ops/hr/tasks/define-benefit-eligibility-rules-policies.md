--- 
title: "定义福利资格规则和策略"
description: "此记录将显示您创建福利资格规则和政策并将规则分配给福利的方法。"
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 807e6a41d603a5327d713d1ab742cc0d961a7784
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="define-benefit-eligibility-rules-and-policies"></a>定义福利资格规则和策略

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

此记录将显示您创建福利资格规则和政策并将规则分配给福利的方法。  

创建此记录时使用的演示数据公司为 USMF。


## <a name="create-benefit-eligibility-policy-rule-type"></a>创建福利资格政策规则类型
1. 转到“人力资源”>“福利”>“资格”>“福利资格政策规则类型”。
2. 单击“新建”。
3. 在“规则名称”字段中，输入一个值。
4. 在“描述”字段中，键入一个值。
5. 在“查询名称”字段中，单击下拉按钮以打开查找。
6. 在列表中，单击所选行中的链接。
7. 单击“保存”。
8. 关闭该页面。

## <a name="benefit-eligibility-policy"></a>福利资格策略
1. 转到“人力资源”>“福利”>“资格”>“福利资格政策”。
2. 选择一个现有的福利政策。
3. 在列表中，单击所选行中的链接。
4. 切换“政策组织”部分的扩展。  在此处可以添加或删除您想要加入政策内的所有组织。
5. 展开或折叠“政策规则”部分。
6. 在列表中，查找并选择以前创建的政策规则。
7. 单击“创建政策规则”。
8. 在“生效日期”字段中，输入您希望政策开始生效的日期。
    * 如果您希望这些更改生效，则设置生效日期和结束日期，以允许您以后对策略规则作出更改，并且将来无需返回到策略。  
9. 
    * 例如，如果您希望规则仅适用于销售经理，您可以创建 Where 子句进行规定：Where 职位描述等于销售经理。  您可以在规则中设置 And 或 Or 或多个 Where 语句。  
10. 单击“确定”。
11. 关闭该页面。
12. 关闭该页面。

## <a name="assign-rule-to-benefit"></a>分配福利规则
1. 转到“人力资源”>“福利”>“福利”。
2. 在列表中，找到并选择所需记录。
3. 在列表中，单击所选行中的链接。
4. 展开或折叠“资格规则”部分。
5. 单击“编辑”。
6. 在“资格”字段中，从列表选择“规则”。
7. 在“规则类型”字段中，单击下拉按钮以打开查找。
8. 在列表中，查找并选择以前创建的规则。
9. 在列表中，单击所选行中的链接。
10. 单击“保存”。
11. 关闭窗体。


