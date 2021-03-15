---
title: 在资产租赁中过帐转换调整日记帐条目
description: 本主题介绍使您可以将租赁组合转换到会计准则编纂专题 842 (ASC 842) 和国际财务报告准则 16 (IFRS 16) 这两种新的租赁会计标准的功能。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 51ae41e22507d77f32b8b0f4685cce797fd19cff
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969545"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a>在资产租赁中过帐转换调整日记帐条目

[!include [banner](../includes/banner.md)]

本主题介绍使您可以将租赁组合转换到会计准则编纂专题 842 (ASC 842)（这是美国公认会计准则 (US GAAP) 中的准则）和国际财务报告准则 16 (IFRS 16) 这两种新的租赁会计标准的功能。

有关如何设置帐簿以转换到新标准的信息，请参阅[设置租赁帐簿](set-up-lease-books.md)。

创建转换调整日记帐条目时，将生成日记帐条目。 该条目反映在该日期根据新准则记录租赁对资产负债表的影响。 将为该日期的帐面金额借记相应资产科目，并贷记负债科目。 差值将借记或贷记到保留收益。

要按照新记帐准则过帐转换调整，请按照下列步骤操作。

1. 在 **租赁摘要** 页上，选择租赁，然后选择 **帐簿**。
2. 在帐簿中，选择 **付款计划**。
3. 在 **付款计划** 对话框中，选择 **确认**。 然后关闭对话框。
4. 选择 **转换调整**。

    > [!NOTE]
    > 只能为分配给 **转换帐簿** 字段可用的帐簿分配的租赁帐簿创建转换调整。 如果 **租赁开始** 字段中的值晚于转换日期，将不更新 **转换调整** 字段中的值。

5. 要查看日记帐条目，请选择 **资产租赁日记帐**。
6. 选择新日记帐，然后选择 **过帐**。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]