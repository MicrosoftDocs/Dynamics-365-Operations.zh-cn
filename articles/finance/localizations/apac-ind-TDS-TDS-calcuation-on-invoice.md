---
title: 根据发票的 TDS 计算
description: 本主题提供有关在发票级别计算从源扣缴税款的交易的参考。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 496e87e3028025f738d2f0a697d91c18b77ad1c9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023062"
---
# <a name="tds-calculation-on-invoices"></a>根据发票的 TDS 计算

[!include [banner](../includes/banner.md)]

本主题提供有关在发票级别计算从源扣缴税款的交易的参考。

| 序列号 | 交易记录类型                                 | 交易记录金额 | 页面名称和选择路径                                 | 帐户类型和抵销帐户类型                         |
| ------------- | ------------------------------------------------ | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1.            | 从供应商进行的购买/记录支出   | 借方或贷方  | 普通日记帐页面（总帐 > 日记帐条目 > 普通日记帐）、发票审核日记帐页面（应付帐款 > 发票 > 发票审核）、发票日记帐页面（应付帐款 > 发票 > 发票日记帐） | 分类帐 (Dr.) 供应商 (Cr.).  仅在分类帐帐户具有过帐类型 **采购** - **现金** 时，才为供应商-分类帐组合计算预缴税金。 |
| 2.            | 从客户进行的购买/记录支出 | 借方或贷方  | 普通日记帐页面（总帐 > 日记帐条目 > 普通日记帐）、发票日记帐页面（应付帐款 > 发票 > 发票日记帐） | 分类帐 (Dr.) 客户 (Cr.)                                 |
| 3.            | 从供应商的固定资产的购买              | 借方或贷方  | 普通日记帐页面（总帐 > 日记帐条目 > 普通日记帐）、发票登记薄日记帐页面（应付帐款 > 发票 > 发票登记簿）、发票日记帐页面（应付帐款 > 发票 > 发票日记帐） | 固定资产 (Dr.) 供应商 (Cr.)                             |
| 4.            | 从客户的固定资产的购买            | 借方或贷方  | 普通日记帐页面（总帐 > 日记帐条目 > 普通日记帐）、发票日记帐页面（应付帐款 > 发票 > 发票日记帐） | 固定资产 (Dr.) 客户 (Cr.)                           |
| 5            | 采购发票（应付 TDS）                  |                    | 采购订单页面（应付帐款 > 采购订单 > 所有采购订单） |                                                              |
| 6            | 销售发票（应收 TDS）                  |                    | 销售订单页面（应收帐款 > 订单 > 所有销售订单）、普通发票页面（应收帐款 > 发票 > 所有普通发票） |                                                              |
