---
title: 设置和处理过渡付款
description: 本文说明如何设置和处理过渡的客户付款。 过渡付款是分两步过帐到总帐的付款。
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode, VendPaymMode, LedgerJournalTable, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb563008f156e1bfa6e4e9a705e9170342719ce7
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775160"
---
# <a name="set-up-and-process-bridged-payments"></a>设置和处理过渡付款

[!include [banner](../includes/banner.md)]

过渡付款是分两步过帐到总帐的付款。 通常，当付款方式设置为 **银行**，并且您必须仅在交易清除银行后才将交易过帐到银行帐户时，应该使用此方法。 但是，您也可以将其用于分类帐科目。 在这种情况下，将在处理过渡过帐时将金额从一个主科目转移到另一个主科目。

您可以从应付帐款或应收帐款创建过渡付款。 尽管本文说明了如何为应收帐款配置过渡过帐，但应付帐款交易的步骤是相似的。

## <a name="set-up-bridging-posting"></a>设置过渡过帐

若要使用过渡过帐，您必须设置一种或多种付款方式，以便它们使用 **过渡过帐** 方法。 然后，您必须选择过渡帐户。

1. 转到 **应收帐款 &gt; 付款设置 &gt; 付款方式**。
2. 选择现有付款方式以对其启用过渡过帐。 或者，创建新付款方式。
3. 选中 **过渡过帐** 复选框。
4. 在 **过渡帐户** 字段中，选择在将付款清算到银行帐户之前应将其过帐到的主科目。
5. 关闭该页面。

## <a name="process-and-transfer-bridging-posting"></a>处理和转移过渡过帐

要创建和处理过渡过帐，请按照以下步骤操作。

1. 转到 **应收帐款 &gt; 付款 &gt; 客户付款日记帐**。
2. 选择 **新建** 创建日记帐。
3. 在 **名称** 字段中选择名称。
4. 将行添加到客户付款日记帐，并选择为过渡过帐配置的付款方式。
5. 将日记帐过帐。 交易将过帐到上一过程中您在 **过渡帐户** 字段中选择的主科目。

当交易已清除银行，并且您要将付款从过渡帐户转移到为付款方式指定的付款帐户时，请按照以下步骤进行操作。

1. 转到 **总帐 &gt; 日记帐条目 &gt; 普通日记帐**。
2. 选择 **新建** 创建日记帐。
3. 在 **名称** 字段中选择名称。
4. 选择 **行** 以打开日记帐详细信息。
5. 选择 **功能 &gt; 选择过渡交易**。
6. 标记已结清的每笔付款，然后选择 **接受**。
7. 将日记帐过帐。
