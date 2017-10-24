--- 
title: "向客户分配普通发票模板"
description: "此任务展示的是如何将普通发票模板分配到客户。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3bcb59c6edd04877dc2a052002be513205ae840a
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a>向客户分配普通发票模板

[!include[task guide banner](../../includes/task-guide-banner.md)]

此任务展示的是如何将普通发票模板分配到客户。 此任务使用 USMF 演示公司，旨在为负责管理和处理应收账款发票的用户使用。

1. 转到“应付账款”>“客户”>“所有客户”。
2. 在列表中，找到并选择所需记录。
3. 在操作窗格上，单击“发票”。
4. 单击“重复发票”。
    * 使用此页将普通发票模板分配给客户，并指定发送给客户的频率。  
5. 单击“新建”以将新模板分配给客户。
6. 选择您要分配给客户的普通发票模板。
7. 在列表中，找到并选择所需记录。
8. 在列表中，单击所选行中的链接。
9. 输入生成第一张发票的日期。
    * 输入重复执行的结束日期。  
    * 选择以下选项之一：无结束日期 - 将会无限期生成发票，直到删除来自该客户帐户的模板。  计费结束日期 - 选择此选项并输入可以生成发票的最后日期。  
    * 在发票生成后，最大累计金额将停止生成。  
    * 输入使用所选模板可以达到的最大累计金额。 例如，若您输入 1,000.00，并在每月生成 100.00 金额的发票，则发票在生成第十个时将停止生成。  
    * 从普通发票模板或客户帐户，通过使用默认值生成经常性发票。  
    * 创建发票时，选择是否使用普通发票模板或客户帐户来确定语言、过帐模板、销售税组、物料销售税组、清单代码、交货国家/地区、币种、付款期限、付款方式、付款说明、付款计划、现金折扣、财务维度和转帐单的默认值。  
10. 选择重复执行模式。
    * 每日 – 选择此选项并在“每”字段中输入天数。 例如，如果您输入 15，将为此客户每 15 天生成一次发票。  每周 - 选择此选项并在“每”字段中输入周数。 例如，如果您输入 2，将为此客户每两周生成一次发票。  每月 - 选择此选项并在“每”字段中输入月数。 例如，如果您输入 6，将为此客户每六个月生成一次发票。  每年 - 选择此选项并在“每”字段中输入年数。 例如，如果您输入 2，将为此客户每两年生成一次发票。  
11. 在“每”字段中，输入一个数字。


