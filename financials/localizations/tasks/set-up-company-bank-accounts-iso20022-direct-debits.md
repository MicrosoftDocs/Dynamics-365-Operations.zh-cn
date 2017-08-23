--- 
title: "设置 ISO20022 直接借记的公司银行帐户"
description: "此任务通过设置所需的特定于公司的银行帐户信息以生成客户付款文件。"
author: mrolecki
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 741d8ddca24e5fe083b4ddf775bb7f2d65a56fee
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a>设置 ISO20022 直接借记的公司银行帐户

[!include[task guide banner](../../includes/task-guide-banner.md)]

此任务通过设置所需的特定于公司的银行帐户信息以生成客户付款文件。 此过程以 ISO 20022 直接借记格式为例。 其他格式可能需要更多设置信息，如公司 ID 或分类代码。



用于创建此任务的演示数据公司是 DEMF。



这是五个用于演示使用电子申报配置的客户付款流程的过程中的第二个。


## <a name="set-up-the-iban-and-swift-codes"></a>设置 IBAN 和 SWIFT 代码
1. 转到现金和银行管理>银行账号。
2. 使用“快速筛选器”以筛选含有 'DEMF OPER' 值的“银行帐户”。
3. 在列表中，单击所选行中的链接。
    * 例如：单击“DEMF OPER”以打开银行帐户详细信息。  
4. 单击“编辑”。
5. 展开或折叠”其他识别“部分。
6. 在“IBAN”字段，键入一个值。
    * 例如，输入“DE89370400440532013000”。  
7. 在“SWIFT 代码”字段中，键入一个值。
    * 例如，输入“DEUTDEFF”。    请注意，许多付款格式不需要 SWIFT\BIC，但是建议还是为银行帐户登记。  
8. 单击“保存”。

## <a name="set-up-a-bank-account-for-the-legal-entity"></a>为法人实体设置银行帐户
1. 转至“组织管理”>“组织”>“法人”。
2. 单击“编辑”。
3. 展开或折叠“银行帐户信息”部分。
4. 在“银行帐户”字段中，单击下拉按钮以打开查找。
5. 在列表中，单击所选行中的链接。
    * 例如：选择“DEMF OPER”银行帐户。  
6. 单击“保存”。


