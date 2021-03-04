---
title: 设置租赁帐簿
description: 本主题描述了租赁帐簿中维护的信息。 租赁帐簿中包含确定租赁在系统中的会计方式的会计政策。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 28518341544327f1983e563b719b0f455b6e1c43
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4440952"
---
# <a name="set-up-lease-books"></a>设置租赁帐簿

[!include [banner](../includes/banner.md)]

租赁帐簿中包含确定租赁在系统中的会计方式的会计政策。 除了基于现金的记帐之外，资产租赁还支持以下准则：

- 美国通用会计制度 (US GAAP)
- 会计准则编纂专题 842 (ASC 842)
- ASC 840
- 国际财务报告准则 16 (IFRS 16)
- 国际会计标准 17 (IAS 17)

要创建租赁帐簿，请执行以下步骤。

1. 转到 **资产租赁 \> 设置 \> 租赁帐簿**。
2. 选择 **新建** 添加帐簿。
3. 设置以下字段。

    | 姓名                                     | 说明 |
    |------------------------------------------|-------------|
    | 过帐层                            | 选择要使用的过帐层。 为租赁附加的每本帐簿都是为特定过帐层设置的。 每个过帐层都有不同的过帐目的。 |
    | 租赁类型                               | 选择是自动将租赁分类，还是应将其预定义为金融租赁或经营性租赁。 |
    | 会计框架                     | 选择与帐簿关联的框架。 |
    | 租赁期/使用年限设置          | 如果将租赁类型设置为 **自动**，并且资产使用年限中的租赁期大于或等于此字段中输入的百分比，则系统将租赁分类为金融租赁。  |
    | 现值/资产的公平价值设置   | 输入一个整数以定义将确定租赁类型的阈值。 如果将来的最低租赁付款额的现值大于帐簿设置中用户定义的值，并且如果帐簿的租赁分类设置为自动，则系统会将租赁分类为金融租赁。 |
    | 短期阈值                     | 输入用作短期租赁阈值的月数。 如果租赁期小于或等于您在此处输入的月数，则系统会将租赁归类为短期租赁，并采用延期租金处理。 |
    | 低价值阈值                      | 输入用作低价值租赁的阈值的金额。 如果资产的公平价值小于或等于您在此处输入的值，则系统会将租赁归类为低价值租赁，并采用延期租金处理。 |
    | 向供应商付款                            | 将此选项设置为 **是**，以便允许将租赁付款作为发票过帐到每个租赁中指定的供应商科目。 过帐租赁付款后，将贷记供应商科目。 如果此选项设置为 **否**，将改为贷记 **租赁过帐参数** 页上的 **租赁付款** 过帐类型指定的科目。 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]