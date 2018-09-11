--- 
title: "输入销售协议"
description: "该过程向您显示如何创建销售协议，以向一位客户承诺在一段时间内购买的产品达到协商的金额时获得特别折扣。"
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8c11164f7edb8e05b93f3c58b9707c0bf2482228
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="enter-sales-agreements"></a>输入销售协议

[!include [task guide banner](../../includes/task-guide-banner.md)]

该过程向您显示如何创建以下内容的销售协议：向一位客户承诺如果在一段时间内购买的产品达到

议定的金额，将提供特别折扣。 您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。


## <a name="set-up-sales-agreement-header"></a>设置销售协议标题
1. 转到“销售和市场”>“销售协议”>“销售协议”。
2. 单击“新建”。
3. 在“客户帐户”字段中，单击下拉按钮以打开查找。
4. 在列表中，找到并选择所需记录。
5. 在列表中，单击所选行中的链接。
6. 在“销售协议分类”字段，单击下拉按钮以打开查找。
7. 在列表中，单击所选行中的链接。
8. 展开“常规”部分。
9. 在“默认承诺”字段中，选择“产品价值承诺”。
    * 承诺类型是您必须在协议中分配的用于定义如何执行协议合同的一个强制性条件。 四种预定义类型可以设置客户的承诺目标，表示为数量或值。 数量承诺类型仅适用于特定的产品，但是基于值的类型适用于特定和非特定的产品销售。  
10. 在“到期日期”字段中，将日期设置为您想要协议终止的将来的日期。
11. 单击“确定”。

## <a name="set-up-product-value-commitment-lines"></a>设置产品值承诺行
1. 单击“添加行”。
2. 在“物料编号”字段中，单击下拉按钮以打开查找。
3. 在列表中，找到并选择所需记录。
4. 在列表中，单击所选行中的链接。
    * 为协议所选择的承诺类型会影响您可以为协议行输入信息的种类。 例如，对于基于值的协议，必须为客户承诺购买您的货物的金额指定总净额（使用协定币种）。 在此示例中，由于您在为某一客户创建的购买特定值的产品的协议，所以该行上的“数量和单位”字段不可用。   
5. 在“净额”字段中，输入客户承诺要购买产品的金额。
6. 在“折扣百分比”字段，输入与该协议相关的应用于客户销售订单行的百分值。
7. 展开“行明细”部分。
8. 在“执行最大”字段中，选择“是”。
    * 强制选择“最大”意味着使用承诺的特价、折扣和/或付款期限的所有销售订单行的总金额不能超过该承诺所指定的金额。  
    * 最小和最大发放金额指定了使用所选协议的每个销售订单的销售值的范围。   
9. 展开“销售协议标题”部分。
    * 除非协议的状态设置为“有效”，否则销售订单不能与协议关联，因而不能参与协议的履行。 在此阶段，您可以手动更改状态。 但是，当您确认客户的协议时，状态通常将更改。  
10. 在“操作窗格”上单击“销售协议”。
11. 单击“确认”。
    * 确保“标记协议”作为有效选项设置为“是”。  
12. 在“打印报告”字段中，选择“是”。
13. 单击“确定”。
14. 关闭该页面。
    * 协议现在生效，您可以将客户订单链接到协议，来抵消承诺目标。  


