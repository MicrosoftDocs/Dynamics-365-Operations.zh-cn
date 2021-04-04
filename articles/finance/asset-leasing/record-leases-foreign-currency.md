---
title: 使用外币记录租赁
description: 本主题说明如何使用非记帐币种或申报币种记录租赁。
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
ms.openlocfilehash: fd4d04ae7e89b8ce41ed745c643b8e736484789d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241482"
---
# <a name="record-leases-in-foreign-currencies"></a>使用外币记录租赁

[!include [banner](../includes/banner.md)]

采用非记帐币种或申报币种的租赁的资产租赁科目是在 **分类帐设置** 页上建立的。 所有租赁均应以其交易币种输入。 换句话说，应使用租赁合同中指定的币种输入。 本主题说明如何使用非记帐币种或申报币种记录租赁。

如果您以外币形式输入租赁，则使用权 (ROU) 资产会以记帐币种和申报币种折旧。 这些币种在 **分类帐设置** 页中配置。 固定资产中也使用此行为。 当您以外币创建租赁时，请在 **币种** 字段中选择交易币种。

记帐币种的汇率是 **记帐币种汇率** 字段中的默认值。 申报币种的汇率是 **申报币种汇率** 字段中的默认值。 这些汇率自租赁开始之日起生效。 **记帐币种汇率** 和 **申报币种汇率** 字段位于 **租赁详细信息** 页面的 **财务和申报汇率信息** 快速选项卡中。

1. 选中 **固定利率** 复选框以覆盖自动输入的汇率，然后输入新汇率。
2. 在其他字段中，输入租赁所需的信息，然后选择 **创建计划**。
3. 在新的 **租赁详细信息** 页面上，选择 **帐簿**。
4. 在 **租赁帐簿** 页面上的 **财务和申报交换信息** 选项卡上，验证 **记帐币种初始使用权资产** 和 **申报币种初始使用权资产** 字段的值。 这些字段中的每个字段均以相应币种显示折算后的使用权资产余额。 只要您更改任何财务信息，这些字段就会更新。 在确认付款计划之前，请选择 **创建计划**。

    初始确认日记帐条目记录使用租赁中列出的货币汇率的使用权资产。 日记帐条目还包括 **记帐币种初始使用权资产** 和 **申报币种初始使用权资产** 字段的值。

## <a name="subsequent-measurement-for-foreign-currency-leases"></a>外币租赁的后续计量

折旧计划以申报币种、记帐币种和交易币种显示预期的折旧费用金额。

要以申报币种或记帐币种查看使用权资产余额和折旧金额，请打开 **资产折旧计划** 页，然后选中 **显示记帐币种金额** 或 **显示申报币种金额** 复选框。

当您针对以外币计价的租赁创建折旧费用日记帐条目时，该条目将使用租赁中列出的汇率。 还使用 **记帐币种初始使用权资产** 和 **申报币种初始使用权资产** 字段的值。

最终折旧费用金额可以通过使用稍微不同的汇率来计算，因此使用权资产可以以记帐货币和申报币种完全折旧。

如果租赁已重新分类为 **延期租金**，系统会自动清除记帐币种和申报币种的汇率（如果已定义）。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]