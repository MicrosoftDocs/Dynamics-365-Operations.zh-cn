---
title: 使用审核日记帐将发票数据键入应付帐款
description: 此主题介绍如何使用发票登记簿创建发票，然后使用审核日记帐更新费用帐户。
author: abruer
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f19c31a3ca20ad4b11e2529bdcb9db351c37f6c2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971870"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>使用审核日记帐将发票数据键入应付帐款

[!include [banner](../../includes/banner.md)]

此主题介绍如何使用发票登记簿创建发票，然后使用审核日记帐更新费用帐户。

## <a name="create-and-post-and-invoice"></a>创建并过帐发票
1. 在导航窗格中，转到 **模块 > 应付帐款 > 发票 > 发票登记簿**。
2. 选择 **新建**。
3. 选择您想要使用的发票登记簿名称。
4. 单击 **行**，以打开登记簿和输入费用行。
5. 选择某一供应商。 例如，输入或选择 `US-104`。
6. 在 **发票** 字段中，键入一个值。
7. 在 **描述** 字段中，键入一个值。
8. 在 **信用** 字段中，输入一个数字。
9. 在 **审核人** 字段中，从下拉菜单中选择一个审核人。
10. 选择 **过帐**。

## <a name="approve-an-invoice"></a>审核发票
1. 在导航窗格中，转到 **模块 > 应付帐款 > 发票 > 发票审核**。
2. 选择 **新建**。
3. 选择您想要使用的发票审核日记帐的名称。
4. 选择 **行**，以显示可以选择要审核发票的页面。
5. 选择 **查找凭证**，以显示可供审核的所有发票。
6. 标记您创建的发票，然后单击 **选择**。 选中后，您选择的以上凭证将移动到此列表中。  
7. 选择 **确定**。
8. 单击 **帐号** 字段，以添加费用帐户到发票中。
9. 输入一个帐号，并关闭该字段。 例如，输入 `600120`。
10. 选择 **过帐**。
11. 选择 **凭证** 查看已过帐条目。 发票待定审核帐户被冲销，并替换成实际费用帐户。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]