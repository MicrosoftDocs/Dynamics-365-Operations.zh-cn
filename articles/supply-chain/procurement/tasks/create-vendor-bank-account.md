---
title: 创建供应商银行帐户
description: 此过程演示如何为供应商创建银行帐户。
author: mkirknel
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f8092ab7f960fd36515afb8448dfe1e262197595
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383128"
---
# <a name="create-a-vendor-bank-account"></a>创建供应商银行帐户

[!include [banner](../../includes/banner.md)]

此过程演示如何为供应商创建银行帐户。 您可以在演示数据公司 USMF 中使用此过程。

1. 转到**导航窗格 > 模块 > 采购 > 供应商 > 所有供应商**。
2. 选择要为其创建银行帐户的供应商，然后单击**供应商帐户 ID** 字段中的链接。
3. 在**操作窗格**上，单击**供应商**。
4. 单击**银行帐户**。
5. 在**操作窗格**中，单击**复制**。
6. 在**银行帐户**字段中，键入一个值。 此 ID 将用于识别供应商记录中的银行帐户。  
7. 在**名称**字段中，键入一个值。
8. 在**银行组**字段中，输入或选择一个值。
9. 在**银行代号类型**字段中选择一个选项。 这是用于国际支付的银行代号的类型。  
10. 在**银行帐号**字段中，输入一个值。
11. 在 **SWIFT 代码**字段中，键入一个值。
12. 在 **IBAN** 字段，键入一个值。
    - IBAN 编号的格式必须正确。 例如，您可以使用 DE89370400440532013000。  
    - 如果已到达生效日期，但尚未超过到期日期，则银行帐户的状态为“有效”。 如果“生效日期”和“到期日期”字段均为空白，则也是处于“有效”状态。 如果“生效日期”和“到期日期”字段中的日期均为未来日期，则不可使用电子付款。 可使用其他付款类型，且银行帐户有效。  
13. 展开**设置**部分。
14. 在**文本代码**字段中，键入一个值。 此字段指定接收方的银行对账单上显示的代码。  
15. 在**发送给银行的消息**字段中，键入一个值。
16. 在**汇率参考**字段中，键入一个值。 这是任何远期汇率或定期汇率的参考编号。
17. 在**货币**字段中，输入或选择一个值。 当发布预验证时，此部分提供其状态（待定或已审核）的概览。  
18. 展开**地址**部分。
19. 展开**预验证**部分。
20. 展开**联系信息**部分。
21. 在**电话**字段，输入一个值。
22. 关闭该页面。
23. 单击**编辑**。
24. 展开**付款**部分。
25. 在**银行帐户**字段中，选择您刚才创建的帐户。
26. 单击**保存**。 地址可以从银行组继承（如果已指定），也可以在此处添加。  

