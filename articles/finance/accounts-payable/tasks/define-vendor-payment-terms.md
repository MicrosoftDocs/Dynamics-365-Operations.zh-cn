---
title: 定义供应商付款期限
description: 本主题说明如何设置供应商发票的付款期限。
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2199c12e92d631d3eb058637c48b53335d779f2d
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109798"
---
# <a name="define-vendor-payment-terms"></a>定义供应商付款期限

[!include [banner](../../includes/banner.md)]

本主题说明如何设置供应商发票的付款期限。 此任务使用 USMF 公司演示。

1. 转到 **导航窗格 > 模块 > 应付帐款 > 付款设置 > 付款期限**。
2. 选择 **新建**。 **支付条款** 页用于定义如何计算到期日。 并非用于定义如何计算现金折扣日期。  
3. 在 **付款期限** 字段中，键入一个值。
4. 在 **描述** 字段中，键入一个值。
5. 在 **天数** 字段中，输入一个数字。 此处输入的数字将会被添加到截止日期，或添加到 **付款方式** 所规定的结束日期。 例如，如果您选择 **净额**，该数字将添加到截止日期。 如果您选择 **本月**，将添加到当前月的最后一天来计算截止日期。  
6. 选择 **保存**。
7. 关闭该页面。
8. 转到 **应付帐款 > 付款设置 > 现金折扣**。
9. 选择 **新建**。
10. 在 **现金折扣** 字段中，输入 ID。
11. 在 **描述** 字段中，键入一个值。
12. 如果供应商提供了一个分层折扣，请选择当前到期日后的下一个现金折扣。
13. 关闭该页面。
14. 在 **天数** 字段中，输入一个数字。 在 **天数** 字段中输入的数量，将根据 **净额/本月** 字段中的选项，用于计算 **现金折扣日期**。 如果选择 **净额**，则数量将添加到发票日期以确定现金折扣日期。 如果已选择 **本月数**，则该天数将添加到本月的最后日期以确定现金折扣日期。  
15. 在 **折扣** 字段中，输入现金折扣的百分比。 
16. 输入将为客户发票将现金折扣过帐到的主科目，然后输入将为供应商发票把现金折扣过帐到的主科目。 如果将 **折扣抵消帐户** 设置为 **使用供应商折扣的主科目**，则应使用该“主科目”。 如果该选项设置为 **发票行上的帐号**，现金折扣将过帐到发票行上的资产或支出帐户。  
17. 选择 **保存**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
