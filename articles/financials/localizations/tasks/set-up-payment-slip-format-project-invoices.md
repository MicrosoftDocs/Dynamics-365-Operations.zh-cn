--- 
title: "设置项目发票的付款单格式"
description: "企业通常将打印的付款单附加到发票上以帮助客户，并提供用于过帐和结算的付款参考。"
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 02/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 9700571110a1b488e250dd8ee7b8c5c8f15cbc01
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-payment-slip-format-for-project-invoices"></a>设置项目发票的付款单格式

[!include[task guide banner](../../includes/task-guide-banner.md)]

企业通常将打印的付款单附加到发票上以帮助客户，并提供用于过帐和结算的付款参考。 除了销售发票和普通发票，付款单可用于项目或服务发票，催款单、利息单和帐户对账单。 若要处理付款单，首先设置您的债权人标识号和付款单附件格式。

该程序适用于 DEMF 演示公司。 

该功能可用于首选地址在丹麦的法人。


## <a name="set-up-a-creditor-id-number"></a>设置债权人 ID 号
1. 转至“组织管理”>“组织”>“法人”。
2. 展开或折叠“银行帐户信息”部分。
3. 单击“编辑”。
4. 在“FI 债权人 ID”字段中，键入一个值。
5. 单击“保存”。
6. 关闭该页面。

## <a name="set-up-a-payment-slip-format-for-invoices-notes-letters-and-statements"></a>为发票、本票、字母和报表设置付款单格式
1. 转到应收帐项目>设置>表格>表格设置。
2. 单击“发票”选项卡。
3. 在客户发票字段中“关联付款附件”，选择一个选项。
    * None： 不打印付账单。 如果付款金额是以除了丹麦克朗 (DKK) 的币种表示，则选择此选项。   FIK 751： 如果打算在付账单上手写付款金额和付款日期，就打印FIK 751 付账单。   FIK 752： 如果打算用电脑生成的带有打印好的付款金额及日期的付款帐单，就打印FIK 752 付账单。  
4. 单击“保存”。
5. 单击“普通文本发票”选项卡。
6. 在“普通文本发票的相关付款附件”字段中，选择一个选项。
    * None： 不打印付账单。 如果付款金额是以除了丹麦克朗 (DKK) 的币种表示，则选择此选项。   FIK 751： 如果打算在付账单上手写付款金额和付款日期，就打印FIK 751 付账单。   FIK 752： 如果打算用电脑生成的带有打印好的付款金额及日期的付款帐单，就打印FIK 752 付账单。  
7. 单击“保存”。
8. 单击“利息单”选项卡。
9. 在利息单字段中“关联付款附件”，选择一个选项。
    * None： 不打印付账单。 如果付款金额是以除了丹麦克朗 (DKK) 的币种表示，则选择此选项。   FIK 751： 如果打算在付账单上手写付款金额和付款日期，就打印FIK 751 付账单。   FIK 752： 如果打算用电脑生成的带有打印好的付款金额及日期的付款帐单，就打印FIK 752 付账单。  
10. 单击“保存”。
11. 单击“收款单”选项卡。
12. 在收款单字段中“关联付款附件”字段中，选择一个选项。
    * None： 不打印付账单。 如果付款金额是以除了丹麦克朗 (DKK) 的币种表示，则选择此选项。   FIK 751： 如果打算在付账单上手写付款金额和付款日期，就打印FIK 751 付账单。   FIK 752： 如果打算用电脑生成的带有打印好的付款金额及日期的付款帐单，就打印FIK 752 付账单。  
13. 单击“保存”。
14. 单击“会计财务报表”选项卡。
15. 在会计财务报表字段中“关联付款附件”，选择一个选项。
    * None： 不打印付账单。 如果付款金额是以除了丹麦克朗 (DKK) 的币种表示，则选择此选项。   FIK 751： 如果打算在付账单上手写付款金额和付款日期，就打印FIK 751 付账单。   FIK 752： 如果打算用电脑生成的带有打印好的付款金额及日期的付款帐单，就打印FIK 752 付账单。  
16. 单击“保存”。
17. 关闭该页面。


