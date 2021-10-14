---
title: 为内部公司客户发票自动登记付款
description: 本主题说明了如何为内部公司客户发票自动登记付款
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: ffc5c7bf44989fbcc18e940b5a7c9df81260d770
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548131"
---
# <a name="register-payments-automatically-for-intercompany-customer-invoices"></a>为内部公司客户发票自动登记付款

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management 在过帐内部公司客户发票时创建客户交易记录。 此客户交易记录直到结算时都保持打开状态，这意味着它已支付。 在相应的内部公司采购订单按发票更新时，将创建与客户交易记录匹配的供应商交易记录。 此供应商交易记录也在结算前保持打开状态。 若要降低差异的风险，可以在过帐应付帐款付款日志时自动创建和过帐应收帐款付款日志。

1. 转到 **销售和市场营销 \> 客户 \> 所有客户**。
1. 在操作窗格上的 **常规** 选项卡中，选择 **内部公司**。
1. 若要在 **内部公司** 页面上设置销售订单的内部公司应收帐款付款，请选择 **销售订单策略** 链接。
1. 在 **付款日记帐** 字段中，选择您想将内部公司供应商付款登记到的账户应收付款日志。 您可以在 **应收帐款参数** 页上设置此项。
1. 如果要自动过帐到此日记帐，请选中 **自动过帐日记帐** 复选框。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
