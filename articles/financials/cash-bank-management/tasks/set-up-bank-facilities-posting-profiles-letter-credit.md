--- 
title: "设置信用证的银行设施和过帐模板"
description: "该过程会从始至终引导您创建所需的“银行融资和过帐模板”，以便处理“信用证”。"
author: kweekley
manager: AnnBe
ms.date: 10/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 18ad27eb673745d09569f6a49c8bc66132550f35
ms.openlocfilehash: 9ad19534091bdbd8924f90174b720d818b9ed778
ms.contentlocale: zh-cn
ms.lasthandoff: 10/27/2017

---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a>设置信用证的银行设施和过帐模板

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

该过程会从始至终引导您创建所需的“银行融资和过帐模板”，以便处理“信用证”。 

此任务使用演示公司“USMF”。






## <a name="general-ledger-parameter"></a>总分类帐参数
1. 转到“现金和银行管理”>“设置”>“现金和管理银行参数”。
2. 展开“银行单据”部分。
3. 选择“启用进口信用证”选项。
4. 选择“启用出口信用证”选项。
5. 单击“保存”。
6. 关闭该页面。

## <a name="create-bank-facility"></a>创建银行融资
1. 转到“现金和银行管理”>“设置”>“银行融资”。
2. 单击“新建”。
3. 在“融资组”字段中，输入银行融资组名称。
4. 在“描述”字段中，输入银行融资组的描述。
5. 单击“保存”。
6. 单击“融资类型”选项卡。
7. 单击“新建”。
8. 在“融资类型”字段中，输入唯一代码。
9. 在“描述”字段中，键入一个值。
10. 在“融资组”字段中，单击下拉按钮以打开查找。
11. 在列表中，找到并选择所需记录。
12. 在列表中，单击所选行中的链接。
13. 在“融资性质”字段中，选择银行融资的性质。
14. 单击“保存”。
15. 关闭该页面。

## <a name="bank-posting-profile"></a>银行过帐模板
1. 转到“现金和银行管理”>“设置”>“银行单据过帐模板”。
2. 单击“新建”。
3. 在“帐户/组号码”字段中，单击下拉按钮以打开查找。
4. 在列表中，找到并选择所需记录。
5. 在列表中，单击所选行中的链接。
6. 选择主要帐户以进行结算。
    * 此帐户会在计算现金流预测时使用。  
7. 在“收费帐户”字段中，选择交易费用适用的帐户。
8. 在“利润帐户”字段中，选择交易利润适用的帐户。
    * 当过账打开的毛利时借记此科目，当过账贷款时贷记此科目。  
9. 单击“保存”。


