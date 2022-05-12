---
title: 设置租赁日记帐名称
description: 本主题说明如何定义租赁日记帐名称。 租赁日记帐名称指定资产租赁中源于的条目过帐到的日记帐。
author: moaamer
ms.date: 12/03/2021
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
ms.openlocfilehash: a92461e742f1675e4cfda89e6c80c5b087ff5bfb
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644888"
---
# <a name="set-up-lease-journal-names"></a>设置租赁日记帐名称

[!include [banner](../includes/banner.md)]


租赁日记帐名称指定资产租赁交易过帐到的日记帐。 **资产租赁参数** 页面中的 **初始确认** 和 **月日记帐名称** 字段中显示分配给 **资产租赁** 日记帐类型的日记帐名称。 只能将 **供应商发票记录** 日记帐类型分配给 **发票日记帐名称** 字段。

系统将锁定某些财务字段从而使其不能被编辑，以防止交易和计划之间出现任何差异。 已锁定的某些字段包括：**帐户**、**金额**、**财务维度**、**货币** 和 **交易类型**。 此外，您将无法在任何资产租赁日记帐条目中添加或删除日记帐条目行，因为这可能会导致计划与交易之间出现差异。


要配置租赁日记帐名称，请完成以下步骤。

1. 转到 **资产租赁 \> 设置 \> 资产租赁参数**。
2. 在 **常规** 选项卡的 **初始确认日记帐名称** 字段中，选择日记帐。 将把所有初始确认日记帐条目过帐到该日记帐名称。
3. 在 **发票日记帐名称** 字段中，选择日记帐。 如果为租赁帐簿将 **向供应商付款** 选项设置为 **是**，将把租赁和费用付款发票过帐到该日记帐名称。
4. 在 **租赁日记帐名称** 字段中，选择日记帐。 所有折旧、利息和短期重新分类条目都将过帐到该日记帐名称。 如果为租赁帐簿将 **向供应商付款** 选项设置为 **否**，将把租赁付款和费用付款条目也过帐到该日记帐名称。
5. 在 **租赁修改日记帐名称** 字段中，选择日记帐。 租赁调整、终止和减损交易将过帐到此日记帐名称。 您选择的日记帐名称不应被分配工作流或审批。 如果未定义租赁修改日记帐名称，租赁调整、终止和减损交易将过帐到在 **租赁日记帐名称** 字段中选择的日记帐名称。 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
