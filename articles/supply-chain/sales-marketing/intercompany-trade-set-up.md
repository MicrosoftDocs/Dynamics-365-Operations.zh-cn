---
title: 设置内部公司交易
description: 本文介绍了如何设置内部公司交易
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage, InterCompanyTradingRelationSetupCustomer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 8d956c60db9f3acf2f1759dc3e1922da40d8a514
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905622"
---
# <a name="set-up-intercompany-trade"></a>设置内部公司交易

[!include [banner](../../includes/banner.md)]

为了使 Microsoft Dynamics 365 Supply Chain Management 能够运行内部公司交易，您必须设置要运行内部公司交易的客户和供应商。 还必须设置应付帐款、应收帐款、采购以及销售和市场。

## <a name="before-you-set-up-intercompany-trade"></a>设置内部公司交易前

在您设置内部公司交易前，必须决定哪些客户是内部公司客户以及哪些供应商是内部公司供应商。 对于 Microsoft Dynamics 365 Supply Chain Management 中的每个法人，必须确定将那个交易政策应用至与特定内部公司客户和供应商之间的内部公司交易关系。

特别是，我们建议您和您的组织熟悉内部公司参数。

- 与每个法人中负责内部公司交易的经理讨论该设置的影响。
- 为每个法人设置相应值。

## <a name="set-up-trading-relations"></a>设置贸易关系

若要设置客户和供应商的内部公司交易，请执行以下步骤。

1. 转到 **应付帐款 \> 客户 \> 所有客户**。
1. 选择客户帐户。
1. 在操作窗格上的 **常规** 选项卡中，选择 **内部公司**。
1. 为客户帐户指定内部公司设置参数。 这些参数中包括包含相应供应商和供应商帐户的法人。 参数还包括采购订单策略、销售订单策略、值映射以及销售协议和采购协议的策略。 您还可以指定是使用其他法人中的客户帐户还是供应商帐户的基础数据值。
1. 为法人中其余内部公司客户重复第 1 步到第 4 步。
1. 转到 **应付帐款 \> 供应商 \> 所有供应商**。
1. 选择供应商帐户。
1. 在操作窗格上的 **常规** 选项卡中，选择 **内部公司**。
1. 为供应商帐户指定内部公司设置参数。 这些参数中包括包含相应客户和客户帐户的法人。 参数还包括销售订单策略、采购订单策略、值映射和采购协议及销售协议的策略。 您还可以指定是使用其他法人中的供应商帐户还是客户帐户的基础数据值。
1. 为法人中其余内部公司供应商重复第 6 步到第 9 步。

## <a name="set-up-products"></a>设置产品

若要设置客户和供应商的内部公司交易，请执行以下步骤。

1. 转到 **产品信息管理 \> 产品 \> 所有产品和产品主数据**。
1. 定义发放到要进行内部公司交易的法人实体的产品。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
