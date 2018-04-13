--- 
title: "设置 ISO20022 贷方转帐的公司银行帐户"
description: "此过程显示如何设置生成付款文件所需的，公司具体的银行帐户信息。"
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1d0eabdfdeb5ed7d0bdb6df87ebdfa0d41e87492
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a>设置 ISO20022 贷方转帐的公司银行帐户

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

此过程显示如何设置生成付款文件所需的，公司具体的银行帐户信息。 您设置生成 ISO 20022 贷方转帐格式所需的信息，但是根据格式可能需要其他信息，如德国 ID 或分类代码。 

用于创建此过程的演示数据公司是 DEMF。

这是五个用于演示使用电子申报配置的供应商付款流程的流程中的第二个。 此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。


## <a name="set-up-iban-and-swift-code"></a>设置 BAN 和 SWIFT 代码
1. 转到现金和银行管理>银行账号。
2. 使用“快速筛选器”以筛选含有 'DEMF OPER' 值的“银行帐户”。
3. 单击“DEMF OPER”以打开银行帐户详细信息。
4. 单击“编辑”。
5. 展开”其他识别“部分。
6. 在“IBAN”字段中，键入“DE89370400440532013000”。
7. 在“SWIFT 代码”字段中，键入“DEUTDEFF”。
    * 请注意，许多付款格式不需要 SWIFT\BIC，但是建议还是为银行帐户登记。  
8. 单击“保存”。

## <a name="set-up-bank-account-for-the-legal-entity"></a>为法人实体设置银行帐户
1. 转至“组织管理”>“组织”>“法人”。
2. 单击“编辑”。
3. 展开“银行帐户信息”部分。
4. 在“银行帐户”字段中，输入或选择一个值。
5. 单击“保存”。


