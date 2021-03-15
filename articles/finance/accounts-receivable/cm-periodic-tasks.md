---
title: 定期信用管理任务
description: 本主题描述了管理客户信用额度过程中必须进行的定期任务。
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: b41b87cd3e2e80b87318c5c771d45a4d0e5d4b85
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971695"
---
# <a name="periodic-credit-management-tasks"></a>定期信用管理任务

[!include [banner](../includes/banner.md)]

本主题描述了管理客户信用额度过程中必须进行的定期任务。

## <a name="update-risk-scores"></a>更新风险分数

随着业务的发展和环境的变化，指定客户的信用风险也可能发生变化。 为了帮助维持适合客户的信用额度，您必须定期查看每个风险评分的标准并更新每个客户的评分。 您可以使用 **更新风险评分** 页面（**信用和收款 \> 定期任务 \> 信用管理 \> 更新风险评分**）来更新以下分数。 所有用户定义的计算也会被处理。

- **平均付款天数** – 此分数是客户支付发票所用的平均天数。
- **自从以下时间以来的客户** – 此分数是客户成为您组织的客户的年数。
- **营业开始年份** – 此分数是客户营业的年数。 它使用 **客户** 页上的 **业务开始时间** 字段的值。
- **销售款未清天数** – 该分数基于应收帐款余额、销售收入和前 12 个月的天数。
- **平均余额** – 该分数基于前 12 个月的应收帐款余额。
- **信用管理组**、**帐户状态** 和 **国家/地区** – 这些分数使用来自客户的信息。

## <a name="update-customer-balance-statistics"></a>更新客户余额统计信息

您可以运行 **更新客户余额统计信息** 流程，以更新显示在 **余额统计查询** 页上的余额统计信息计算结果。 此信息用于计算风险评分和 **客户** 页上信用统计速见表中显示的值。

运行该流程时，它将更新单个客户的客户余额统计信息。 要设置批处理作业以为多个客户运行该流程，您可以使用 **计算余额统计** 页面（**信用管理 \> 定期任务 \> 计算余额统计**）。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]