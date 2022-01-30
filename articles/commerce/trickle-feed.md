---
title: 为零售商店交易记录创建基于缓慢馈送的订单
description: 本主题介绍如何为 Microsoft Dynamics 365 Commerce 中的商店交易记录创建基于缓慢馈送的订单。
author: analpert
ms.date: 01/11/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 67b66cd4bf2a77f3ab7f33f691156e38cc13770a
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/12/2022
ms.locfileid: "7964620"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a>为零售商店交易记录创建基于缓慢馈送的订单

[!include [banner](includes/banner.md)]

如果您使用的是 Microsoft Dynamics 365 Commerce 版本 10.0.5 及更高版本，我们建议您将所有对帐单过帐流程转换为基于缓慢馈送的对帐单过帐流程。 使用缓慢馈送功能可获得的重要性能和业务权益。 可实现全天候处理销售交易记录。 在一天结束时可在财务报表中处理支付方式和现金管理交易记录。 使用缓慢馈送功能可对销售订单、发票和付款进行连续处理。 因此，可以近乎实时更新和确认库存、收入和付款事宜。

## <a name="use-trickle-feed-based-posting"></a>使用基于缓慢馈送的过帐

> [!IMPORTANT]
> 在启用基于缓慢馈送的过帐之前，您必须确保不存在已计算和未过帐的对帐单。 在启用此功能之前对所有对帐单进行过帐。 您可以在 **商店财务** 工作区中查看未结对帐单。

要启用基于缓慢馈送的零售交易记录过帐，请在 **功能管理** 工作区中启用 **零售对帐单 - 缓慢馈送** 功能。 对帐单将拆分为两种类型：交易记录对帐单和财务报表。

### <a name="transactional-statements"></a>交易记录对帐单

计划以高频率全天执行交易记录对帐单处理作业，以便在将交易记录上传到 Commerce Headquarters 时创建文档。 执行 **P 作业** 时，交易记录将从商店加载到 Commerce Headquarters 中。 您还必须执行 **验证商店交易记录** 作业才能对交易记录进行验证，以便交易记录对帐单选取交易记录。

安排以下作业以高频率执行：

- 要计算交易记录对帐单，请执行 **批量计算交易记录对帐单** 作业（**Retail 和 Commerce \> Retail 和 Commerce IT \> POS 过帐 \> 批量计算交易记录对帐单**）。 此作业将选取所有未过帐和已验证的交易记录，然后将这些交易记录添加到新的交易记录对帐单中。
- 要批量过帐交易记录对帐单，请执行 **批量过帐交易记录对帐单** 作业（**Retail 和 Commerce \> Retail 和 Commerce IT \> POS 过帐 \> 批量过帐交易记录对帐单**）。 此作业将执行过帐流程，为无任何错误的未过帐对帐单创建销售订单、销售发票、付款日记帐、折扣日记帐和收支交易记录。 

### <a name="financial-statements"></a>财务报表

财务报表处理是一天中最后一道流程。 此类型的对帐单处理仅支持 **班次** 结算方法，将仅选取已结束的班次。 对帐单仅限用于财务对帐。 对帐单仅针对支付方式的计算金额与交易记录金额之间的差额而创建日记帐，以及针对其他现金管理交易记录创建日记帐。

财务报表还可以用于审查以下交易记录：钱币清点交易记录、付款交易记录、银行支付交易记录和金库支付交易记录。 仅当选择财务报表时，支付方式详细信息页才可见。

![仅在选择财务报表时，有关已过帐报表窗体的支付方式详细信息部分的图像才可显示。](./media/Trickle-feed-posted-statements-transaction-view.png)

根据预计的工作结束时间，安排下列财务报表作业的开始时间和结束时间：

- 要计算财务报表，请执行 **批量计算财务报表** 作业（**Retail 和 Commerce \> Retail 和 Commerce IT \> POS 过帐 \> 批量计算财务报表**）。 此作业将收集所有未过帐的财务交易记录并将其添加到新的财务报表中。
- 要批量过帐财务报表，请执行 **批量过帐财务报表** 作业（**Retail 和 Commerce \> Retail 和 Commerce IT \> POS 过帐 \> 批量过帐财务报表**）。

### <a name="manually-create-statements"></a>手动创建对帐单

也可以手动创建交易记录对帐单和财务报表类型。 

1. 转至 **Retail 和 Commerce \> 渠道 \> 商店**，然后选择 **对帐单**。 
2. 选择 **新建**，然后选择要创建的对帐单类型。 **对帐单** 页面上的字段将显示与所选对帐单类型相关的数据，**对帐单组** 下的操作将显示相关的操作。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
