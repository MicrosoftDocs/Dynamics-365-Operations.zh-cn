---
title: "补偿客户"
description: "本文说明如何为一组客户创建偿还交易记录。 如果某一客户具有贷方余额，您可以为该客户偿还剩余的金额。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b2882ce391c853939e51b27f9ed3b7459f66b134
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="reimburse-customers"></a>补偿客户

[!include[banner](../includes/banner.md)]


本文说明如何为一组客户创建偿还交易记录。 如果某一客户具有贷方余额，您可以为该客户偿还剩余的金额。 

下表显示必须先就绪然后才能开始的先决条件。

| 先决条件                                                            | 描述                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 为法人指定最低偿还金额。          | 在**应收账款参数**页上，在**常规**区域中，在 **最低偿还额**字段中，输入可以偿还客户超额支付的最小金额。 |
| 可选：为每一个可获得偿还的客户添加一个供应商帐户。 | 在**客户**页，在**杂项详细信息**快速选项卡上，在**供应商帐户**字段中，选择客户的供应商帐户。                                           |

当您创建偿还交易记录时，将针对贷方余额创建供应商发票。 偿还流程移除了客户帐户的贷方余额，并创建对应客户的供应商帐户结欠金额。

1.  在“应收账款”中，请运行**偿还**流程。
2.  按以下步骤之一：
    -   若要偿还特定的客户帐户，请单击**选择**，然后在查询中指定客户帐户。
    -   若要偿还所有客户帐户，请单击“**确定**”。

    贷方金额将转移到客户的供应商帐户，并且按一般的付款进行处理。 如果某一客户不具有供应商帐户，则将自动为该客户创建零星供应商帐户。
3.  若要查看创建的偿还交易记录，使用**偿还**页。
4.  在应付账款中，为偿还流程创建的供应商发票创建付款。





