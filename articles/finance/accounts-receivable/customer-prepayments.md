---
title: 客户预付款
description: 本文说明如何设置和处理客户预付款（也称为客户保证金）。
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f085d45895530aaf0a16439f62dfc13b27da84b6
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799425"
---
# <a name="customer-prepayments"></a>客户预付款

[!include [banner](../includes/banner.md)]

当您从客户处收到付款时，将使用客户预付款，但是没有可以据其结算付款的发票。 这些付款类型也称为客户保证金。

设置和使用客户预付款的流程包括以下基本步骤。

1. 为预付款创建客户过帐模板。
2. 设置 **具有预付款日记帐凭证的过帐模板** 参数。
3. 创建客户付款日记帐，然后选中每一行上的 **预付款日记帐凭证** 复选框。
4. 过帐客户付款日记帐。
5. 生成发票后，使用 **结算未结交易** 页通过发票结算预付款。

## <a name="create-a-customer-posting-profile-for-prepayments"></a>为预付款创建客户过帐模板

通常，当您在货物或服务交付之前或在系统中存在发票之前接受客户的预付款或保证金时，您需要在会计科目表中将现金记录为负债而不是资产。 但是，根据您所在的国家或地区，将这些金额记录在总帐中的要求可能会有所不同。 因此，请务必咨询您的会计师，了解所有适用的本地法规。

一般而言，创建可用于预付款的过帐模板的流程与创建其他过帐模板的流程相同。 主要区别在于您在 **汇总科目** 字段中选择的主科目。 有关详细信息，请参阅[客户过帐模板](customer-posting-profiles.md)。

## <a name="define-parameters-for-customer-prepayments"></a>定义客户预付款的参数

在配置客户预付系统时，必须考虑两个主要的应收帐款参数。 请按照以下步骤配置这些参数。

1. 转至 **应收帐款 \> 设置 \> 应收帐款参数**。
2. 可选：在 **分类帐和销售税** 选项卡上的 **付款** 快速选项卡上，将 **预付款日记帐凭证含销售税** 选项设置为 **是**。
3. 在 **具有预付款日记帐凭证的过帐模板** 字段中，选择过帐客户预付款时要使用的客户过帐模板。
4. 关闭该页面。

## <a name="create-customer-prepayment-vouchers"></a>创建客户预付款凭证

创建客户付款日记帐时，对于每笔预付款，必须在 **客户付款日记帐** 页上将 **预付款日记帐凭证** 选项设置为 **是**。 按照以下步骤创建客户预付款。

1. 转到 **应收帐款 \> 付款 \> 客户付款日记帐**。
2. 选择 **新建** 创建日记帐。
3. 在 **名称** 字段中，选择要使用的日记帐名称。

    > [!IMPORTANT]
    > 如果您在上一过程中将 **预付款日记帐凭证含销售税** 选项设置为 **是**，则必须选择选择了 **金额包括销售税** 参数的日记帐名称。 

4. 可选：在 **描述** 字段中，输入详细描述。
5. 选择 **行**。
6. 如果不存在空白行，选择 **新建** 创建一行。
7. 在 **日期** 字段中，输入应过帐预付款的日期。
8. 在 **客户** 字段中，选择下一个预付款的客户。
9. 可选：在 **描述** 字段中，输入交易的详细描述。
10. 在 **信用** 字段中，输入预付款的金额。
11. 在 **抵销帐户** 字段中，选择要抵销付款的帐户。 例如，选择要向其过帐付款的银行或主帐户。
12. 在 **付款方式** 字段中，选择客户的付款方式。
13. 在 **付款** 选项卡上，将 **预付款日记帐凭证** 选项设置为 **是**。
14. 对必须过帐的每个其他预付款重复步骤 7 到 13。
15. 选择 **过帐** 完成日记帐。

## <a name="settle-prepayments-with-invoices"></a>使用发票结算预付款

您可以使用 **客户付款** 工作区轻松找到和结算尚未完全结算的付款。

1. 在 **主页** 仪表板上，选择 **客户付款** 磁贴。
2. 在 **客户交易** 部分的 **未结算付款** 选项卡上，搜索并选择要结算的付款。
3. 选择 **结算交易**。
4. 选中发票和将要结算的付款的 **标记** 复选框。
5. 选择 **过帐**。

有关如何结算未结交易的详细信息，请参阅[结算概述](/dynamics365/finance/cash-bank-management/settlement-overview)。
