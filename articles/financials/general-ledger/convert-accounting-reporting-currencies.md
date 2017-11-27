---
title: "转换记帐或申报币种"
description: "必须更改该记帐币种或申报币种的公司有两个选项。"
author: aprilolson
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 78223
ms.assetid: 31c56f9a-9c64-40a2-90e3-1969a760614b
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ad840f4ed2cf27615e699a13fcd8be7f3c2cd5c8
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="convert-accounting-or-reporting-currencies"></a>转换记帐或申报币种

[!include[banner](../includes/banner.md)]


必须更改该记帐币种或申报币种的公司有两个选项。 第一个选项是创建一个新公司并全新开始。 第二个选项是运行记帐和申报币种转换流程。 这是一个运行时间很长的流程，会更改系统中的每个交易记录。 在流程可以运行之前，必须进行某些设置。

## <a name="preparing-the-legal-entity-for-currency-conversion"></a>为币种转换准备法人
在可以转换法人的币种之前，您必须为客户和供应商帐户恢复所有外币重估金额，然后关闭上个会计年度。 您还必须为转换准备数据库，然后对要进行币种转换的法人的帐户做出所需的更改。 在您完成了币种转换后，您必须完成一些附加程序。 您必须对账已转换金额中的舍入尾差、重新计算业务统计数据、分录分类账交易记录、限制对转换工具的访问并为客户和供应商账户重估外币金额。

## <a name="setting-up-accounts-for-automatic-transactions"></a>为自动交易记录设置帐户
在币种转换流程中，损益或尾差会过帐到在**“自动交易记录帐户”**页上定义的帐户。 在转换流程运行前，主科目必须分配到以下类型的交易记录：

-   记帐币种折算收益
-   记帐币种折算损失
-   以记帐币种表示的尾差
-   以申报币种表示的尾差
-   年结

## <a name="posting-rounding-differences-and-sum-recalculations"></a>过帐舍入尾差和合计重新计算
以下信息说明化整时可能发生的差异：

-   如果产品价格已转换为 0（零），将生成一份报告，其中显示在转换前的产品编号、模块类型、价格和单位。
-   增值税和总帐之间的化整差额过帐到普通记帐日志。
-   重新计算重估外币金额、客户和供应商交易记录金额。
-   为每个客户和供应商交易记录的化整差额创建客户和供应商结算记录。
-   将客户和供应商的舍入差额过账至普通记账日志。
-   重新计算在已关帐库存交易记录中的已结算的成本金额和成本调整金额。
-   将库存管理中的舍入差额过帐到普通记帐日志。
-   重新计算现有库存量。
-   重新计算在分类帐日志中的总金额。
-   重新计算分类帐结算单。
-   重新计算帐户余额。
-   将在总帐中的舍入差额过帐到普通记帐日志。
-   重新计算未结的分录。
-   计算在帐户余额中的最终余额。

如果您转换新的分类帐会计币种，在重新计算总金额或过帐舍入差额期间产生错误时，必须关闭“**日记帐记帐币种转换**”页。 然后总金额会重新计算，并且舍入差额将过帐。

## <a name="processing-the-currency-conversion"></a>处理币种转换
当您开始转换币种转换流程时，所有用户都必须从系统退出。 您必须定义新的分类帐或申报币种和汇率。 当您单击**“确定”**时，该流程会运行并更新系统中的每个交易记录。 币种转换是很长的流程。 当完成时，您将看到记帐或申报币种在**“分类帐”**页上已更新。

## <a name="completing-the-currency-conversion"></a>完成币种转换
币种转换后，您必须重新生成所有对账报告以确保所有转换金额都是正确的。

-   如果分类账记账币种的转换导致了舍入尾差，则将不会通过使用发生舍入尾差的凭证过账这些差额。 相反，将通过为转换过账输入的凭证过账这些差额。 转换后，按凭证和日期检查的所有报告将包括这些舍入尾差。 此行为是正确的，并且可以忽略。
-   如果客户和供应商的对帐报表在合计行上显示差异金额，并且在转换前不存在任何差异金额，则必须过帐此差异金额。 该科目是客户和供应商的汇总科目。 对方科目是针对转换损失或转换收益的会计科目。

当所有分录日志均已删除时，您可以将分录记入日志。 单击“**总帐**”&gt;“**定期**”&gt;“**日记帐**”&gt;“**日记帐分录**”。 如果需要重估，您可以在转换币种后重估外币金额。 您通过为重估选择**“方法”**字段中的**“标准”**，重估外币金额。

有关详细信息，请参阅[将过帐的日记帐条目记入日记帐](tasks/journalize-posted-journal-entries.md)。


