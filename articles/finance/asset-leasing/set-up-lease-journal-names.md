---
title: 设置租赁日记帐名称
description: 本主题说明如何定义租赁日记帐名称。 租赁日记帐名称指定资产租赁中源于的条目过帐到的日记帐。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c139df124b249ec9dc5d16096e6f45f22d435456
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880878"
---
# <a name="set-up-lease-journal-names"></a>设置租赁日记帐名称

[!include [banner](../includes/banner.md)]

租赁日记帐名称指定资产租赁交易过帐到的日记帐。 **资产租赁参数** 页面中的 **初始确认** 和 **月日记帐名称** 字段中显示分配给 **资产租赁** 日记帐类型的日记帐名称。 只能将 **供应商发票记录** 日记帐类型分配给 **发票日记帐名称** 字段。

要配置租赁日记帐名称，请按照下列步骤操作。

1. 转到 **资产租赁 \> 设置 \> 资产租赁参数**。
2. 在 **常规** 选项卡的 **初始确认日记帐名称** 字段中，选择日记帐。 将把所有初始确认日记帐条目过帐到该日记帐名称。
3. 在 **发票日记帐名称** 字段中，选择日记帐。 如果为租赁帐簿将 **向供应商付款** 选项设置为 **是**，将把租赁和费用付款发票过帐到该日记帐名称。
4. 在 **租赁日记帐名称** 字段中，选择日记帐。 所有折旧、利息和短期重新分类条目都将过帐到该日记帐名称。 如果为租赁帐簿将 **向供应商付款** 选项设置为 **否**，将把租赁付款和费用付款条目也过帐到该日记帐名称。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
