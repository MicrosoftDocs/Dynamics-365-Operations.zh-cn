---
title: 设置保函的银行设施和过帐模板
description: 此任务会创建所需的银行融资和过帐模板，以便处理保函。
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b6da3b9358192997de1d0231e5c9c8eaba92a23b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976258"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>设置保函的银行设施和过帐模板

[!include [banner](../../includes/banner.md)]

此任务会创建所需的银行融资和过帐模板，以便处理保函。



本任务使用 USMF 公司进行演示。 




## <a name="general-ledger-parameter"></a>总分类帐参数
1. 转到“现金和银行管理”>“设置”>“现金和管理银行参数”。
2. 展开“银行单据”部分。
3. 选择“启用保函”选项。
4. 在”交易记录日记帐“字段中，单击下拉按钮以打开查找。
5. 在列表中，找到并选择所需记录。
6. 在列表中，单击所选行中的链接。
7. 单击“数序”选项卡。
    * 定义保函编号的数序代码和保函交易记录参考资料  
8. 单击“保存”。
9. 关闭该页面。

## <a name="create-bank-facility"></a>创建银行融资
1. 转到“现金和银行管理”>“设置”>“银行融资”。
2. 单击“新建”。
3. 在“融资组”字段中，输入保函交易记录适用的银行融资组名称。
4. 在“描述”字段中，键入一个值。
5. 单击“保存”。
6. 单击“融资类型”选项卡。
7. 单击“新建”。
8. 在“融资类型”字段中，输入与银行融资协议有关的银行融资类型的名称。
9. 在“描述”字段中，键入一个值。
10. 在“融资组”字段中，单击下拉按钮以打开查找。
11. 在列表中，找到并选择所需记录。
12. 在列表中，单击所选行中的链接。
13. 在“融资性质”字段中，选择一个选项。
14. 单击“保存”。
15. 关闭该页面。

## <a name="bank-posting-profile"></a>银行过帐模板
1. 转到“现金和银行管理”>“设置”>“银行单据过帐模板”。
2. 单击“新建”。
3. 在“帐户/组号码”字段中，单击下拉按钮以打开查找。
4. 在列表中，找到并选择所需记录。
5. 在列表中，单击所选行中的链接。
6. 在“结算帐户”字段中，选择结算适用的主要帐户。
7. 在“收费帐户”字段中，选择交易费用适用的帐户。
8. 在“利润帐户”字段中，选择交易利润适用的帐户。
9. 在“清算帐户”字段中，选择保函交易记录使用的清除帐户。 
10. 单击“保存”。
11. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]