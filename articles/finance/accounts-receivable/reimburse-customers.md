---
title: 补偿客户
description: 本文说明如何为一组客户创建偿还交易记录。 如果某一客户具有贷方余额，您可以为该客户偿还剩余的金额。
author: JodiChristiansen
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae6a3078743fc9cd43c71bc1d4531c0553ee53bb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012131"
---
# <a name="reimburse-customers"></a>补偿客户

[!include [banner](../includes/banner.md)]

本文说明如何为一组客户创建偿还交易记录。 如果某一客户具有贷方余额，您可以为该客户偿还剩余的金额。 

下表显示必须先就绪然后才能开始的先决条件。

| 先决条件                                                            | 描述 |
|-------------------------------------------------------------------------|-------------|
| 为法人指定最低偿还金额。          | 在 **应收帐款参数** 页上，在 **常规** 区域中，在 **最低偿还额** 字段中，输入可以偿还客户超额支付的最小金额。 |
| 可选：为每一个可获得偿还的客户添加一个供应商帐户。 | 在 **客户** 页，在 **杂项详细信息** 快速选项卡上，在 **供应商帐户** 字段中，选择客户的供应商帐户。 |

当您创建偿还交易记录时，将针对贷方余额创建供应商发票。 偿还流程移除了客户帐户的贷方余额，并创建对应客户的供应商帐户结欠金额。

1. 在应收帐款中，运行 **偿还** 流程（**应收帐款 \> 定期任务 \> 偿还**）。
2. 要对所有交易记录进行分组，而不考虑分类帐，请将 **汇总客户** 选项设置为 **是**。 要仅对具有类似分类帐维度的交易记录进行分组，请将此选项设置为 **否**。
3. 选择 **包括具有未结借方交易记录的客户** 以选择具有未结算借方金额的客户。
4. 要偿还特定的客户帐户，请在 **要包括的记录** 快速选项卡上选择 **筛选**，然后在查询中指定客户帐户。

    贷方金额将转移到客户的供应商帐户，并且按一般的付款进行处理。 如果某一客户不具有供应商帐户，则将自动为该客户创建零星供应商帐户。

5. 要查看创建的偿还交易记录，请使用 **偿还** 报表（**应收帐款 \> 查询和报表 \> 偿还报表**）。
6. 在应付帐款中，为偿还流程创建的供应商发票创建付款。 有关如何向供应商付款的信息，请参阅[供应商付款概述](../accounts-payable/Vendor-payments-workspace.md)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]