---
title: "查看日记帐分录和交易记录"
description: "本文说明您可以查看日记帐条目和交易记录的各种方式。"
author: RobinARH
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13031
ms.assetid: 281c7ea6-4dfd-4d1f-994f-c361ee299dbe
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: a6848ea9c05536ac18a038b1864c9ccb9408964c
ms.lasthandoff: 03/31/2017


---

# <a name="view-journal-entries-and-transactions"></a>查看日记帐分录和交易记录

本文说明您可以查看日记帐条目和交易记录的各种方式。 

要查看日记帐和交易记录的用户可通过多种方式来访问数据。 他们可以利用提供深化功能的查询页，或者可以在总帐中使用各个报表选项。

## <a name="voucher-transactions"></a>凭证交易记录
**凭证交易记录**是一个查询页，您可以从中选择各个表和字段以指定您要搜索的余额或交易记录的条件。 例如，您可以查看特定日期或帐户的所有交易记录，或特定过帐层中的**运营**类型的所有交易记录。 默认情况下，此页显示日记帐编号、凭证、日期和主科目，不过，您可以添加其他表、字段和条件来缩小搜索范围。

## <a name="audit-trail"></a>审计线索
**审计线索**是显示交易记录类型、描述、交易记录创建人和创建日期的查询页。 从**审计线索**查询页，可以查看凭证交易记录。

## <a name="financial-reports"></a>财务报表
您还可以通过运行财务报表探索和分析总帐交易记录。 因为财务报表的设计可以基于帐户、维度、科目类别或三者组合，您可以通过不同方式深化来查看交易记录。 如果您需要总帐交易记录的更多信息，还可以包括多个交易记录属性作为报表设计的一部分。 此外，如果您要查看构成总帐余额的交易记录，可以深化到核算交易记录，就像您可以从列 **试算平衡表**列表页执行的操作。

## <a name="ledger-reports"></a>分类帐报表
除了财务报表外，可以使用以下分类帐报表查看总帐交易记录：

-   **维度报表** – 此报表可以按天和科目显示交易记录，并且也具有按维度和期间显示交易记录的选项。
-   **分类帐交易记录列表** – 此报表可以在交易记录、核算和帐户的申报币种中显示交易记录。
-   **打印日记帐** – 此报表显示已过帐日记帐的结果。 您可以按日记帐批处理号或日记帐类型运行报表，或者添加更多字段。
-   **已过帐的日记帐交易记录** – 此报表显示已过帐到按凭证分组的日记帐的交易记录。
-   **序时帐（按日期）** – 此报表显示按日期，与日记帐编号、凭证和会计科目一起显示的所有交易记录。 还在交易记录、核算和申报币种中显示交易记录。
-   **交易记录来源** – 此交易记录报表按日记帐，以及按交易记录、核算和申报币种显示帐户。 它还显示用作对方的每一行。


有关详细信息，请参阅[总帐科目余额](general-ledger-account-balances.md)、[会计源资源管理器](\financials\accounts-payable\accounting-source-explorer)和[财务申报](financial-reporting-getting-started.md)


