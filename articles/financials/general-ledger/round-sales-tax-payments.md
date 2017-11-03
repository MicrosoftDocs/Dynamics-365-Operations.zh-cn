---
title: "销售税付款和舍入规则"
description: "文本说明销售税主管机构的传入规则设置如何工作，以及如何在结算和过帐销售税作业期间舍入销售税余额。"
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8de01b77fcbeb65321e60614b6a11d264460208f
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="sales-tax-payments-and-rounding-rules"></a>销售税付款和舍入规则

[!include[banner](../includes/banner.md)]


文本说明销售税主管机构的传入规则设置如何工作，以及如何在结算和过帐销售税作业期间舍入销售税余额。

销售税需要定期申报和缴纳给税务主管机构。 这可以通过在“销售税”页运行结算和过帐销售税流程完成。 期间销售税将对照销售税帐户结算，销售税余额将过帐到销售税结算帐户。 销售税余额，在销售增值税结算帐户过帐，可以通过在“销售税”页设置舍入规则来按照税务主管机构的要求舍入。 

舍入差额过帐到销售税舍入帐户，在“总帐”的“自动交易记录帐户”字段中选择。

以下示例说明销售税主管机构的舍入规则如何工作。

### <a name="example"></a>示例:

期间的总销售税显示贷方余额 -98,765.43。 法人征收了的增值税超过其支付的金额。 因此，该法人欠税务主管机构款项。 

该法人想要使用将该余额化整为最接近的 1.00 的化整方法。 负责增值税帐户的用户执行以下步骤。

1.  单击“税”&gt;“间接税”&gt;“销售税”&gt;“销售税主管机构”。
2.  在“常规”快速选项卡上，选择“舍入形式”字段中的“标准”。
3.  在“舍入”字段中，输入 1.00。
4.  在向税务主管机构支付销售税时，打开“结算和过帐销售税”页。 （单击“税”&gt;“申报”&gt;“销售税”&gt;“结算和过帐销售税”。）
5.  在销售税结算帐户中，将应交税额 98,765.43 舍入到 98,765。

下表显示通过使用用于“销售税主管机构”页中的“舍入形式”字段的舍方法，如何将 98,765.43 的金额舍入。

| 舍入形式选项                | 舍入值 = 0.01 | 舍入值 = 0.10 | 舍入值 = 1.00 | 舍入值 = 100.00 |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| 标准                              | 98,765.43              | 98,765.40              | 98,765.00              | 98,800.00                |
| 舍尾                            | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                |
| 进位                         | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                |
| 对自身有利，对于贷方余额 | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                |
| 对自身有利，对于借方余额  | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                |

> [!NOTE]                                                                                  
> 如果您选择“对自身有利”，则舍入始终对法人有利。 

有关详细信息，请参阅以下主题：
- [销售税概览](indirect-taxes-overview.md)
- [创建销售税支付](tasks/create-sales-tax-payment.md)
- [在单据中创建销售交易记录](tasks/create-sales-tax-transactions-documents.md)
- [查看已过帐的销售税交易记录](tasks/view-posted-sales-tax-transactions.md)



