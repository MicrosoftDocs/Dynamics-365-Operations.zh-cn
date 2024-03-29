---
title: 更改工作的工作池
description: 本文说明如何使用工作项的“更改工作池”按钮来更改现有工作的工作池。
author: Mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 817b45e8f5af957801a0af04e50acf20ba16c26d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900613"
---
# <a name="change-work-pool-on-work"></a>更改工作的工作池

[!include [banner](../includes/banner.md)]

您可以使用工作池将工作组织到组。 例如，您可以创建工作池以为在特定仓库库位进行的工作分类。

*更改工作的工作池* 功能在工作项的“操作窗格”中添加了 **更改工作池** 按钮。 因此，仓库经理可以轻松地更改现有工作的工作池。 此功能使经理可以对仓库车间的变化做出快速反应，并有助于提高他们适应变化情况的能力，改进将工作转移到另一个工作池的需求。

## <a name="turn-the-change-work-pool-on-work-feature-on-or-off"></a>打开或关闭“更改工作的工作池”功能

从 Supply Chain Management 10.0.25 开始，此功能是强制性的，无法关闭。 如果您运行的版本早于 10.0.25，管理员可以通过在 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区中搜索 *更改工作的工作池* 功能来打开或关闭此功能。

## <a name="set-up-the-change-work-pool-on-work-feature"></a>设置“更改工作的工作池”功能

要使用此功能，您必须设置一些工作池。 您还可以设置工作模板，让它们自动分配池。 如果要完成本文后面提供的示例场景，请按照本部分中的说明设置系统。

### <a name="set-up-work-pools"></a>设置工作池

工作池让您可以按类型组织工作项。 要使用 *更改工作的工作池* 功能，您必须至少有两个可用工作池。 要查看和添加工作池，请按照下列步骤操作。

1. 转到 **仓库管理 \> 设置 \> 工作 \> 工作池**。
1. 如果您使用的是 **USMF** 公司的演示数据，并将演练本文后面的示例方案，请添加两个具有以下设置的工作池：

    - 工作池 1：

        - **工作池 ID**：*Webshop*
        - **描述**：*网上商店*

    - 工作池 2：

        - **工作池 ID**：*CallCenter*
        - **描述**：*呼叫中心*

1. 在操作窗格上，选择 **保存**。

### <a name="set-up-work-templates"></a>设置工作模板

对于每个工作模板，您可以根据需要设置默认工作池。 对于每个相关模板，您可以在 **工作池 ID** 栏分配工作池。 这样，使用给定模板生成的所有工作项将会自动继承分配的工作池。 如果您使用的是 **USMF** 公司的演示数据，并将演练本文后面的示例方案，请按照以下步骤操作。

1. 转到 **仓库管理 \> 设置 \> 工作 \> 工作模板**。
1. 在操作窗格上，选择 **编辑** 将页面设置为编辑模式。
1. 通过设置以下值来编辑模板：

    - **工作模板**：*62 领料装箱*
    - **工作池 ID**：*Webshop*

1. 选择 **保存**。

## <a name="example-scenario"></a>示例场景

此方案演示如何通过更改工作项的工作池来更改现有工作项的处理流。 它使用 **USMF** 公司的演示数据以及本文前面建议的设置。

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>创建销售订单并将其下达到仓库

1. 确认仓库 *62* 中的物料 *A0001* 和 *A0002* 有足够的现有库存量。 转到 **库存管理 \> 查询和报表 \> 现有量列表**，然后按以下所示编辑筛选器：

    - **仓库** 值以 *62* 开头。
    - **物料编号** 值为 *A001* 或 *A002*。

    每一项的演示数据应有 10 个。

    接下来，您必须创建一个销售订单。

1. 转到 **销售和营销 \> 销售订单 \> 所有销售订单**。
1. 在操作窗格上，选择 **新建**。
1. 在 **创建销售订单** 对话框中，设置以下值：

    - **客户帐户**：*US-007*
    - **仓库**：*62*

1. 选择 **确定** 创建销售订单，然后关闭对话框。
1. 将打开新销售订单。 **销售订单行** 快速选项卡上的网格中应包含一个新的空行。 在这个行中，设置以下值：

    - **物料编号：***A0001*
    - **数量：** *2*

1. 在网格上方的 **库存** 菜单中，选择 **预留**。
1. 在 **预留** 页面的“操作窗格”中，选择 **预留批次** 预留库存。
1. 关闭该页面。
1. 在 **销售订单行** 快速选项卡上，选择 **添加行** 在您的销售订单中添加另一行。 在这个行中，设置以下值：

    - **物料编号：***A0002*
    - **数量：** *2*

1. 在网格上方的 **库存** 菜单中，选择 **预留**。
1. 在 **预留** 页面的“操作窗格”中，选择 **预留批次** 预留库存。
1. 关闭该页面。
1. 在“操作窗格”上的 **仓库** 选项卡上，选择 **发放到仓库**。
1. 您将收到信息性消息，其中显示从下达创建的波次 ID 和装运 ID。 记录波次 ID。

### <a name="review-the-outbound-wave"></a>查看出站波次

1. 转到 **仓库管理 \> 出站波次 \> 装运波次 \> 所有波次**。
1. 在网格中，搜索从销售订单下达创建的波次 ID。
1. 选择波次 ID 查看详细信息。
1. 在 **波次行** 快速选项卡上，确保显示了销售订单的装运 ID。

    > [!TIP]
    > 如果在装运波次模板的设置中将 **在发放到仓库时处理波次** 选项设置为 *否*，则必须通过从“操作窗格”上的 **波次** 选项卡选择 **处理** 来手动处理波次以创建工作。

1. 确保波次已处理。 此处理将创建所需的工作。

### <a name="view-work-details-and-change-the-work-pool"></a>查看工作详细信息与更改工作池

您可以使用 **工作详细信息** 页面查看已创建的工作和管理工作池。

1. 转到 **仓库管理 \> 工作 \> 工作详细信息**。
1. 选择刚才创建的工作的行。 **订单编号** 列将显示销售订单编号。

    **工作池 ID** 字段将设置为在工作模板中设置的工作池 ID。

    > [!TIP]
    > 如果看不到 **工作池 ID** 字段，将列添加到网格，然后刷新页面。

1. 要更改与工作 ID 关联的工作池，请在“操作”窗格上，在 **工作** 选项卡上，选择 **更改工作池 ID**。
1. 在 **更改工作池** 对话框中的 **参数** 快速选项卡上，在 **工作池 ID** 字段中，选择 *CallCenter*。
1. 选择 **确定** 应用更改。
1. 请注意，**工作池 ID** 字段的值现已更改为 *CallCenter*。

> [!IMPORTANT]
> 当出现 **更改工作池** 对话框时，默认情况下，**工作池 ID** 字段可能为空白。 如果选择 **确定** 应用更改时此字段为空白，则将工作池从工作中完全删除。
>
> 除了切换工作池外，您还可以使用此过程将工作池添加到没有工作池的任何工作项中，或从有工作池的任何工作项中删除工作池。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]