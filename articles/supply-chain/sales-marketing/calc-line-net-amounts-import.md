---
title: 导入销售订单和报价单时重新计算行净额
description: 本文介绍在导入销售订单和报价单时系统是否以及如何重新计算行净额。 它还解释了如何控制不同版本的 Microsoft Dynamics 365 Supply Chain Management 中的行为。
author: Henrikan
ms.date: 08/05/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2022-06-08
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: edda0c016130e2a273adf8f3d3e00e2d3ae9d5c6
ms.sourcegitcommit: ce58bb883cd1b54026cbb9928f86cb2fee89f43d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/25/2022
ms.locfileid: "9719326"
---
# <a name="recalculate-line-net-amounts-when-importing-sales-orders-and-quotations"></a>导入销售订单和报价单时重新计算行净额

[!include [banner](../includes/banner.md)]

本文介绍在导入销售订单和报价单时系统是否以及如何重新计算行净额。 它还解释了如何控制不同版本的 Microsoft Dynamics 365 Supply Chain Management 中的行为。

## <a name="how-updates-to-net-line-amounts-are-calculated-on-import"></a>如何在导入时计算对净行金额的更新

Supply Chain Management 版本 10.0.23 引入了[缺陷修复 604418](https://fix.lcs.dynamics.com/issue/results/?q=604418)。 此缺陷修复更改了导入现有销售订单和报价单的更新时可更新或重新计算行上的 **净额** 字段的条件。 在版本 10.0.29 中，您可以通过打开 *导入时计算行净额* 功能来替换此缺陷修复。 此功能具有相似的作用，但它提供了一个全局设置，可以在必要时恢复为旧行为。 尽管新行为使系统以更直观的方式工作，但它可能会在满足以下所有条件的特定情况下产生意外结果：

- 使用 Open Data Protocol (OData) 通过 *销售订单行 V2*、*销售报价单行 V2* 或 *退货单行* 实体导入用于更新现有记录的数据，包括使用双重写入、经 Excel 导入/导出功能以及某些第三方集成的情况。
- 实施的 [贸易协议评估政策](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper)制定了一项更改政策，此政策限制对销售订单行、销售报价行和/或退货单行上的 **净额** 字段进行更新。 请注意，对于退货单行，始终会计算 **净额** 字段，不能手动设置。
- 导入的数据包括：对行上的 **净额** 字段所做的更改，或者将导致对一个或多个现有行记录重新计算行上的 **净额** 字段值的更改（如单价、数量或折扣）。

在这些特定情况下，贸易协议评估政策的作用是限制更新行上的 **净额** 字段。 此限制称为 *更改政策*。 由于此政策的缘故，当您使用用户界面编辑或重新计算字段时，系统会提示您确认是否要进行更改。 但是，在导入记录时，系统必须为您做出选择。 在版本 10.0.23 之前，系统始终将行净额保持不变，除非传入行净额为 0（零）。 但是，在较新的版本中，系统始终根据需要更新或重新计算净额，除非已明确指示系统不要执行此操作。 虽然新行为更合乎逻辑，但如果您已在运行采取旧行为的流程或集成，那么这可能会给您带来问题。 本文介绍如何还原到旧行为（如果必须）。

## <a name="control-calculations-of-line-net-amounts-in-versions-10029-and-later"></a>控制版本 10.0.29 及更高版本中的行净额计算

Supply Chain Management 版本 10.0.29 引入了一个名为 *导入时计算行净额* 的功能。 此功能将名为 **计算行净额** 的选项添加到 **应收帐款参数** 页中。 此选项允许您在新行为和旧行为之间进行选择，以计算导入时的行净额。

### <a name="turn-the-calculate-line-net-amount-on-import-feature-on-or-off"></a>启用或关闭“导入时计算行净额”功能

当您更新到版本 10.0.29 时，默认情况下将启用 *导入时计算行净额* 功能，并且新的 **计算行净额** 选项最初设置为 *是*。 *是* 设置对应于新的标准行为。 它与关闭该功能后的系统行为匹配，但 [CalculateLineAmount 参数](#CalculateLineAmount)的功能除外，如本文后面所述。 *无* 设置与版本 10.0.23 之前的系统行为匹配，并且主要用于支持旧版集成方案。

管理员可以使用 [功能管理工作区](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)打开或关闭 *导入时计算行净额* 功能。

### <a name="set-the-calculate-line-net-amount-option"></a>设置“计算行净额”选项

打开 *导入时计算行净额* 功能后，您可以按照以下步骤设置 **计算行净额** 选项。

1. 转至 **应收帐款 \> 设置 \> 应收帐款参数**。
1. 在 **价格** 选项卡上，在 **通过集成进行行净额计算** 快速选项卡上，将 **计算行净额** 选项设置为以下值之一：

    - *是* - 系统将始终在需要时重新计算和更新行金额。 （因此，它将忽略贸易协议评估政策。）
    - *否* - 如果任何行的现有或传入净额为 0（零），则将根据其他值（如单价、数量和折扣）重新计算该行的值。 如果现有或传入净额不同于 0（零），并且针对行上的 **净额** 字段设置了更改政策，则不会重新计算或更新该字段，即使对行价格、数量和/或折扣的传入更改意味着应重新计算行总计也不例外。 此行为与版本 10.0.22 的行为匹配。

### <a name="how-the-calculate-line-net-amount-on-import-feature-affects-the-calculatelineamount-parameter"></a><a name="CalculateLineAmount"></a>“导入时计算行净额”功能如何影响 CalculateLineAmount 参数

打开 *导入时计算行净额* 功能后，`SalesLine` 和 `SalesQuotationLine` 表的 `CalculateLineAmount` 参数无效。 相反，该行为由上一节中描述的 **计算行净额** 选项全局控制。 因此，打开该功能后，您不得对 `CalculateLineAmount` 值有任何依赖。

关闭 *导入时计算行净额* 功能后，`SalesLine` 和 `SalesQuotationLine` 表的 `CalculateLineAmount` 参数的工作方式与其在 Supply Chain Management 版本 10.0.23 至 10.0.28 中的工作方式相同，如下一节所述。

## <a name="control-line-net-amount-calculations-in-versions-10028-and-earlier"></a>控制 10.0.28 及更早版本中的行净额计算

在版本 10.0.23 中引入[缺陷修复 604418](https://fix.lcs.dynamics.com/issue/results/?q=604418) 后，可以选择在编辑行净额或由于其他更改（例如更新了物料价格）而必须重新计算行净额时，每个相关数据实体应有的行为方式。 您可以通过将每个行的新 `CalculateLineAmount` 参数设置为导入的文件中的以下值之一来控制此行为：

- **`CalculateLineAmount` = *1*** - 始终重新计算和更新行上的 **净额** 字段，与是否为该字段设置了更改政策无关，并与传入或现有行净额的值无关。
- **`CalculateLineAmount` = *0*** - 如果任何行的现有或传入净额为 0（零），则将根据其他值（如单价、数量和折扣）重新计算该行的值。 如果现有或传入净额不同于 0（零），并且在行上的 **净额** 字段上设置了更改策略，则不会重新计算或更新该字段。  

系统行为取决于您的 Supply Chain Management 版本：

- 在版本 10.0.22 和更早版本中，系统的行为始终像 `CalculateLineAmount` 设置为 *0* 时一样，并且无法使其行为像 `CalculateLineAmount` 设置为 *1* 时一样。
- 在版本 10.0.23 到 10.0.28 中，对于导入文件中 `CalculateLineAmount` 未明确设置为 *0* 的所有行，系统的行为就像其设置为 *1* 时一样。
