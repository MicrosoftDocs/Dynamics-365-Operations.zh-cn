---
title: 内部公司会计设置
description: 本主题说明如何设置内部公司会计，以便将内部公司日记帐用于分类帐分配和财务日记帐，如日常记帐、供应商发票日记帐和付款日记帐。
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c3bca9d0a7c37716f2334b36d8a948908f52293
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440804"
---
# <a name="intercompany-accounting-setup"></a>内部公司会计设置

[!include [banner](../includes/banner.md)]

本主题说明如何设置内部公司会计，以便将内部公司日记帐用于分类帐分配和财务日记帐，如日常记帐、供应商发票日记帐和付款日记帐。

内部公司日记帐可以在不同方案创建，如为日常记帐、供应商发票日记帐、分类帐分配和集中付款。 若要启用这些方案，必须设置内部公司会计。

## <a name="define-main-accounts"></a>定义主科目
首先，您必须创建内部公司主科目以用于“应付金额”和“应收金额”会计条目。 最好为每个公司使用唯一主科目，以便简化内部公司会计条目的对帐和清除。 如果您使用贸易伙伴或相似维度确定内部公司当事方，您可以定义此维度为在内部公司会计中定义的主科目的固定维度。 在您设置主科目时，应将 **主科目** 页上的 **主科目类型** 字段设置为 **资产负债表**。

## <a name="define-journal-names"></a>定义日记帐名称
其次，必须定义日记帐名称。 将 **日记帐名称** 页上的 **日记帐类型** 字段设置为 **日常**。 最好为进行内部公司会计使用特定的日记帐名称。

## <a name="define-intercompany-accounting-setup"></a>定义内部公司会计设置
**内部公司会计** 页用于创建可彼此交易的法人对。 内部公司会计设置是共享的，因此可从所有法人内查看此设置。 在创建新的法人对时，请确保您知道哪个法人定义为源公司，哪个定义为目标公司。 在输入内部公司交易记录时，该交易记录确定哪个法人发起或创建了该交易记录。 例如，内部公司会计是为 USMF（发起方）和 USSI（目标方）设置的。 如果用户在 USSI 中处于活动状态，并输入了与 USMF 之间的内部公司交易记录，此交易记录将不过帐，因为内部公司会计是仅为充当发起方的 USMF 定义的。 如果两个公司都可以发起交易记录，您需要为互惠设置再创建一个法人对。 

请为源和目标法人选择 **借方科目(应收金额)** 和 **贷方科目(应付金额)**。 定义在目标公司中创建交易记录时使用哪个 **日记帐名称**。 源公司的日记帐已知，因为是用户在创建内部公司交易记录时选择的。 

最后，选择哪个法人将接收支持科目的会计，如集中付款的现金折扣或已有损益。 

可以通过在创建法人对后使用 **创建互惠关系** 按钮，在 **内部公司会计** 页中轻松设置互惠关系。 创建互惠对后，将把目标公司的信息复制到源公司，反之亦然。 将保留为目标公司定义的日记帐。 大多数组织为自己的日记帐名称使用相同的命名约定，因此日记帐名称相同。 如果日记帐名称不同，将在字段中显示警告，通知您日记帐不存在，并且可以选择其他日记帐。



