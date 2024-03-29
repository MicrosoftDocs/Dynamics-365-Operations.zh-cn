---
title: 中国式凭证
description: 本文描述中国式凭证，以及如何在 Microsoft Dynamics 365 Finance 中使用它们。
author: AdamTrukawka
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: China (PRC)
ms.author: atrukawk
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 261454
ms.search.form: LedgerVoucherType_CN, VoucherTypeWizard_CN
ms.openlocfilehash: 9f96077c2c0e9ce62f78221c22d0aeb7e2cc1bfb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286661"
---
# <a name="chinese-vouchers"></a>中国式凭证

[!include [banner](../includes/banner.md)]

本文描述中国式凭证，以及如何使用它们。

您必须为各已过帐的日志创建凭据文档。 可以打印纸质凭证和已过帐日志。 根据您的需求，您可以使用凭证类型设置向导设置常用的 **获取**、**付款** 和 **转移** 凭证类型，也可以在 **凭证类型设置** 页面中创建新的凭证类型。 您可以使用预订凭证输入交易记录并将其分组为“收货凭证”、“付款凭证”或“转移凭证”。 

从每个月第一天起的持续编号规则应分配给各凭证类型。 在 **凭证类型设置** 页面中，可以为将凭证交易记录过帐到指定会计科目定义验证规则。 过帐凭证期间，将根据 **凭证类型设置** 页面中指定的规则运行验证。 如果为单据选择的凭证类型有误，将收到一条消息。 

例如，为 **获取** 凭证类型选择 **信贷** 类型的会计科目。 但是，为 **获取** 凭证类型定义的验证规则指定会计科目必须为借方科目。 在这种情况下，将收到一条消息，说明中国式凭证类型无效。 然后可以进行相应更改，并且可以再次过帐凭证。 

有关详细信息，请参阅[设置中国式凭证](./tasks/set-up-chinese-vouchers.md)。

## <a name="voucher-creation-methods"></a>凭证创建方法
您可以在 **总帐** 页面中使用 **简单** 或 **高级** 方法创建凭证交易记录。 如果通过使用 **简单** 方法创建简单凭证类型的日记帐凭证，在所有日记帐行中选择的凭证类型应相同。 **高级** 方式可让您创建其他凭证类型的多个日志行。 

## <a name="check-for-continuity-in-voucher-numbers"></a>检查凭证号的连续性
中国式凭证号应连续，并且会计期间内应该没有间隔。 可以运行批处理确定中国式凭证号中是否有间隔。 批处理验证交易记录日期，然后为连续性对这些凭证进行重新编号。 为进行跟踪，可以生成 **中国式凭证连续性检查** 报告。 此报告显示已重新编号的中国式凭证的历史记录。 有关详细信息，请参阅[中国式凭证连续性检查](./tasks/chinese-voucher-continuity-check.md)。

## <a name="printing-a-chinese-voucher"></a>打印中国式凭证
可以在过帐凭证之前或之后打印中国式凭证。 在过帐之前或之后，已打印凭据显示诸如已重新编号的中国式凭证的历史记录的信息或税务信息。 在过帐之前或之后检查已打印信息以验证信息是否相同，以及信息是否正确。 例如，如果在日记帐凭证中选择销售税，最终凭证信息中将包含销售税。 但是，此销售税可能与日记帐中的销售税不同。 打印结果必须准确，并且必须与最后过帐之后生成的结果相同。 因此，您可以通过日志凭据和凭据交易记录打印信息正确的中国式凭据。 还可以在按中国式凭据和会计期间筛选信息之后，打印批处理中的中国式凭据。

## <a name="additional-resources"></a>其他资源
- [过帐普通日记帐的凭证](./tasks/post-vouchers-general-journal.md)
- [从其他模块（如销售发票）过帐凭证](./tasks/post-vouchers-other-modules-like-sales-invoices.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
