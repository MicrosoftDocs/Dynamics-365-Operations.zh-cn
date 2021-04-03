---
title: 仓库配置疑难解答
description: 此主题介绍如何解决配置 Microsoft Dynamics 365 Supply Chain Management 时可能遇到的常见问题。
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1fe285f05e5f1ddcb7bd206290b9954cbdaffc75
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "5487089"
---
# <a name="troubleshoot-warehouse-configuration"></a>仓库配置疑难解答

[!include [banner](../includes/banner.md)]

此主题介绍如何解决配置 Microsoft Dynamics 365 Supply Chain Management 时可能遇到的常见问题。

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a>我收到以下错误消息：“牌照或位置无效。”

### <a name="issue-description"></a>问题描述

当您扫描牌照 ID 或位置时，会收到此错误消息。

### <a name="issue-resolution"></a>解决问题

请确保牌照 ID 未在别处保留。 当用户在仓库应用中扫描的值既是有效位置又是有效牌照 ID 时，过去常会发生此问题。 但是，此问题已在版本 10.0.11 中解决。

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a>我收到以下错误消息：“必须为此位置指定牌照。”

### <a name="issue-description"></a>问题描述

如果您使用启用了高级仓库管理 (WMS) 的仓库创建转移单，然后在工作完成后尝试确认装运，这时会收到此错误消息。

### <a name="issue-resolution"></a>解决问题

**默认收货位置** 字段在“来源”仓库的中转仓库中是空白的。 要解决此问题，请在中转仓库中指定默认收货位置。 请确保此位置是由牌照控制的。

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a>我收到以下错误消息：“您无法为库存状态更改创建工作模板行，因为工作类型无效。 请选择其他工作类型。”

### <a name="issue-description"></a>问题描述

对于工作模板，您无法在 **工作模板详细信息** 部分的 **工作类型** 列中选择 *库存状态更改*。

### <a name="issue-resolution"></a>解决问题

此为有意行为。 *库存状态更改* 工作类型仅由系统流程使用。 无法进行配置。 由于工作类型列表固定为枚举，因此无法将多余条目从 **工作类型** 下拉菜单中筛选掉。

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>我收到以下错误消息：“数量对于单位 1% 无效。”

### <a name="issue-description"></a>问题描述

如果存在一个位置有多个牌照的领料工作，此数量对于 *个* 单位将无效。

### <a name="issue-resolution"></a>解决问题

请验证已发布产品或产品变型上的 **单位序列组 ID** 和 **单位转换** 字段是否设置正确。

请注意，此错误消息在版本 10.0.15 中已得到改进（请参阅 [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)）。 新错误消息是“数量无效。 预期为 %1 %2。”

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>在销售订单放置工作的位置指令中，多 SKU 选项不会评估多个位置指令操作。

### <a name="issue-description"></a>问题描述

选择了 **多 SKU** 选项时，*销售订单* 工作订单类型和 *放置* 工作类型的位置指令不会评估多个位置指令操作。 只会评估第一个位置指令操作。

### <a name="issue-resolution"></a>解决问题

一项新功能 *评估多 SKU 位置指令的所有操作* 已在版本 10.0.15 中添加（请参阅 [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)）。 此功能可评估多 SKU 位置指令的所有操作。 如果您需要此功能，请使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)将它打开。

## <a name="i-cant-use-the-warehouse-app-to-do-partial-picking"></a>我无法使用仓库应用进行部分领料。

### <a name="issue-description"></a>问题描述

对于销售订单和转移单，不能跳过物料，进行部分领料。

### <a name="issue-resolution"></a>解决问题

在 **移动设备菜单项** 页上，为设置为处理销售订单或转移订单的每个菜单项，将 **常规** 快速选项卡上的 **允许拆分工作** 选项设置为 *是*。

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a>如何对部分数量工作进行库存状态更改？

### <a name="issue-description"></a>问题描述

您要对批处理的部分数量进行库存状态更改。

### <a name="issue-resolution"></a>解决问题

要使工作人员能够进行此更改，您可以为仓库应用创建菜单项。 在 **移动设备菜单项** 页上，创建（或编辑）具有以下设置的菜单项：

- **模式：***工作*
- **使用现有工作**：*否*
- **工作创建流程**：*移动*
- **显示库存状态**：*是*

您可以根据需要在页面上设置其他字段。

## <a name="the-dock-management-profile-of-a-location-profile-is-not-preventing-inventory-types-from-being-mixed"></a>位置模板的码头管理配置文件未阻止库存类型的混合。

### <a name="issue-description"></a>问题描述

您正在使用 *装运合并政策*。 您已经为 *位置模板* 设置了 *码头管理配置文件*，但是在创建工作时，库存类型在最终位置混合。

### <a name="issue-resolution"></a>解决问题

码头管理配置文件需要工作提前拆分。 换言之，码头管理配置文件预期工作标题不会有多个放置位置。

要让码头管理配置文件有效地管理库存的混合，必须设置工作标题分解。

在此示例中，我们配置了码头管理配置文件，以将 **不应混合的库存类型** 设置为 *装运 ID*，然后我们将为其设置工作标题分解：

1. 转到 **仓库管理 \> 设置 \> 工作 \> 工作模板**。
1. 选择要编辑的 **工作订单类型**（例如，*采购订单*）。
1. 选择要编辑的工作模板。
1. 在操作窗格上，选择 **编辑查询**。
1. 打开 **排序** 选项卡，添加具有以下设置的行：
    - **表** - *临时工作交易*
    - **派生表** - *临时工作交易*
    - **字段** - *装运 ID*
1. 选择 **确定**。
1. 您将返回 **工作模板** 页。 在“操作窗格”中选择 **工作标题中断**。
1. 在操作窗格上，选择 **编辑**。
1. 选中与 **字段名称** 装 *运 ID* 关联的复选框。
1. 在操作窗格上，选择 **保存**。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
