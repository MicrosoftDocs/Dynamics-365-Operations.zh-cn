---
title: 工程更改管理参数
description: 本主题介绍如何为 Microsoft Dynamics 365 Supply Chain Management 配置工程更改管理功能。
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 0cf0e56a8aece98379aa0f181d7b7ff665767544
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/29/2020
ms.locfileid: "4423451"
---
# <a name="engineering-change-management-parameters"></a>工程更改管理参数

[!include [banner](../includes/banner.md)]

**工程更改管理参数** 页面包含设置参数，用于更改与发布产品结构和工程更改管理流程相关的默认行为。

## <a name="open-the-engineering-change-management-parameters-page"></a>打开工程更改管理参数页面

若要打开 **工程更改管理参数** 页面，请转到 **工程更改管理 \> 设置 \> 工程更改管理参数**。 然后，您可以按照本主题其余部分中的说明设置字段。

## <a name="release-control-tab"></a>发布控制选项卡

下表介绍 **工程更改管理参数** 页面的 **发布控制** 选项卡上可用的字段。 这些字段影响发布产品结构流程。

| 字段 | 说明 |
|---|---|
| 物料编号规则 | 选择在将产品发布给法人时应如何定义物料编号。 如果接收法人中的产品编号应与工程公司中的产品编号匹配，选择 *工程产品编号*。 如果产品应该采用接收法人中产品编号的编号规则中的下一个编号，选择 *本地物料编号规则*。 |
| 物料清单名称规则 | 选择在法人中接收（发布）产品时如何定义物料清单 (BOM) 的名称。 选择 *工程名称* 或 *接收物料编号*。 |
| 工艺路线名称规则 | 选择在法人中接收（发布）产品的工艺路线时应如何定义工艺路线名称。 选择 *工程名称* 或 *接收物料编号*。 |
| 运行物料清单检查 | 选择在法人中接收（发布）产品时是否将运行 BOM 检查。 |
| 无效物料清单的发布行为 | 选择在具有无效 BOM 时是否可以发布产品。 选择 *接受*、*仅警告* 或 *不允许*。 |
| 无效工艺路线的发布行为 | 选择在具有无效工艺路线时是否可以发布产品。 选择 *接受*、*仅警告* 或 *不允许*。|
| 产品接受 | 选择在可以在法人中发布产品之前是否需要额外的接受步骤。 选择 *手动* 以添加接受步骤。 在这种情况下，**打开产品发布** 页面将显示产品。 选择 *自动* 以在发布产品及其发布产品结构之后，立即在目标法人中的 **已发布产品** 页面上直接显示产品。 |

## <a name="engineering-change-management-tab"></a>工程更改管理选项卡

下表介绍 **工程更改管理参数** 页面的 **工程更改管理** 选项卡上可用的字段。 这些设置将影响工程更改管理流程。

| 字段 | 说明 |
|---|---|
| 类别 | 创建工程更改请求时将使用的默认类别。 |
| 优先级 | 创建工程更改请求时将使用的默认优先级。 |
| 严重性规则 | 选择应如何建立工程更改订单的严重性。 如果用户期望在 **严重性** 字段中输入值，选择 *手动*。 选择 *计算*，以在操作窗格上选择工程更改订单的 **计算严重性** 时让系统计算 **严重性** 字段的值。 在这种情况下，系统将使用在 **严重性规则集** 页面上定义的严重性规则。 选择 *自动计算* 以根据严重性规则集自动计算和填充 **严重性** 字段的值。 |
| 重新发布受影响的产品 | 通过工程更改订单重新发布产品时，此字段适用。 您可以选择应该在 **发布** 对话框中提出所有产品还是仅受影响的产品。 |
| 要发布的物料清单级别 | 要发布的 BOM 级别的深度。 如果 BOM 具有比在此处指定的值更高的级别（即，如果更深），仅发布高于指定值的级别。 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]