---
title: 为 Warehouse Management 移动应用中的步骤配置提升的字段
description: 本文介绍如何为 Warehouse Management 移动应用的任务流中的步骤提升和突出显示特定信息。
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 3451b1aec525cd0738af558b183f8676d20294a0
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336056"
---
# <a name="configure-promoted-fields-for-steps-in-the-warehouse-management-mobile-app"></a>为 Warehouse Management 移动应用中的步骤配置提升的字段

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> 本文中描述的功能仅适用于新的 Warehouse Management 移动应用。 它们不影响旧仓库应用，该应用现在已弃用。

本文介绍如何为 Warehouse Management 移动应用的任务流中的步骤提升和突出显示特定信息。 此功能可以帮助员工在处理流时将注意力集中在最重要的字段上。 对于每个流程中的每个步骤，管理员可以选择要提升的字段以及要突出显示的字段。

## <a name="enable-promoted-fields-in-your-system"></a>在系统中启用提升的字段

如果您运行的是 Supply Chain Management 版本 10.0.28 或更早版本，您必须先完成以下过程来启用所需的功能并在 Warehouse Management 移动应用中生成所需的字段名称，然后才能够设置提升的字段。 如果您运行的是 Supply Chain Management 版本 10.0.29 或更高版本，这些功能是强制性的，无法关闭，因此您可以跳过此过程。

1. 转到 **系统管理 \> 工作区 \> 功能管理**。 （有关此页面的详细信息，请参阅[功能管理概述](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)。）
1. 确保为您的系统启用 *仓库应用步骤说明* 功能。 此功能是 *仓库应用提升的字段* 功能的先决条件。 从 Supply Chain Management 版本 10.0.29 开始，此功能是强制性的，无法关闭。 有关 *仓库应用步骤说明* 功能的详细信息，请参阅[自定义 Warehouse Management 移动应用的步骤标题和说明](mobile-app-titles-instructions.md)。
1. 确保为您的系统启用 *仓库应用提升的字段* 功能。 这是本文所述的功能。 从 Supply Chain Management 版本 10.0.29 开始，此功能是强制性的，无法关闭。
1. 通过转到 **Warehouse management \> 设置 \> 移动设备 \> 仓库应用字段名称**，选择 **创建默认设置**，更新 Warehouse Management 移动应用中的字段名称。 对您使用 Warehouse Management 移动应用的每个法人（公司）重复此步骤。 有关详细信息，请参阅[为仓库管理移动应用配置字段](configure-app-field-names-priorities-warehouse.md)。

## <a name="configure-promoted-fields-from-a-menu-specific-override"></a>从特定于菜单的替代配置提升的字段

使用以下过程设置提升的字段。

1. 为相关的菜单和步骤创建特定于菜单的替代，如[自定义 Warehouse Management 移动应用的步骤标题和说明](mobile-app-titles-instructions.md)中所述。
1. 查找要编辑的 **步骤 ID** 与 **菜单项名称** 值组合，然后选择 **步骤 ID** 列中的值。
1. 在显示的页面上，在 **选择提升的字段** 快速选项卡上，选择工具栏上的 **选择字段**。
1. 在 **提升的字段** 对话框中，选择要提升的字段。 您还可以突出显示最多两个选定的字段。 突出显示的字段在 Warehouse Management 移动应用中将以粗体显示。 当您选择字段时，应考虑到有些屏幕可能足够大，会仅显示前一到两个提升的字段。 有关显示如何使用这些设置的示例，请参阅本文后面的场景。

    > [!NOTE]
    > **可用字段** 列表仅限于可以为菜单项显示的字段。 但是，其他因素（如物料构成）将确定字段是否实际显示在 Warehouse Management 移动应用中。 如果您已配置提升的字段，则仅选定的字段会显示在 Warehouse Management 移动应用的主页上。 不过，工作人员仍可以通过点击详细信息页查看其余字段。

1. 选择 **确定** 应用设置。 您选择的字段现在已在 **选择提升的字段** 快速选项卡中列出。

## <a name="example-scenario"></a>示例场景

### <a name="enable-sample-data"></a>启用示例数据

要使用指定的示例记录和值完成此场景，您必须使用已安装标准[演示数据](../../fin-ops-core/fin-ops/get-started/demo-data.md)的系统。 开始前，还必须选择 **USMF** 法人。

### <a name="configure-sales-picking-with-promoted-steps-on-the-license-plate-step"></a>在牌照步骤上配置具有提升的步骤的销售领料

在此过程中，您将为牌照步骤中的 **销售领料** 菜单项设置提升和突出显示的字段。

1. 转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备步骤**。
1. 找到名为 *LicensePlateId* 的步骤 ID，选择它。
1. 在操作窗格中选择 **添加步骤配置**。
1. 在下拉对话框中，使用 **菜单项** 字段查找并选择 *销售领料*。
1. 选择 **确定**。
1. 您刚才创建的替代的详细信息页将显示。 在 **选择提升的字段** 快速选项卡上，选择工具栏上的 **选择字段**。
1. 在 **提升的字段** 对话框中，您可以选择要提升和突出显示的字段。 在 **可用字段** 列表中，查找并选择以下字段，然后使用按钮将它们移至 **所选字段** 列表：

    - 库位
    - 物料
    - 产品名称
    - 库存状态

1. 使用向上箭头和向下箭头按钮自定义字段在 **所选字段** 列表中的顺序。 在 Warehouse Management 移动应用中，这些字段将按照您在此处设置的顺序显示。
1. 选择 **位置** 字段，然后选择 **突出显示**。
1. 选择 **确定** 保存配置。

### <a name="view-the-promoted-fields-in-the-warehouse-management-mobile-app"></a>在 Warehouse Management 移动应用中查看提升的字段

在此过程中，您将打开 Warehouse Management 移动应用并完成步骤以查看您在上一过程中提升和突出显示的字段。

1. 在 Microsoft Dynamics 365 Supply Chain Management 中，创建一个销售订单，该销售订单需要从已跟踪牌照的位置领料的领料步骤。 然后将销售订单下达到仓库。 记下生成的工作 ID。
1. 打开 Warehouse Management 移动应用，登录仓库 24。 （在标准演示数据中，使用 *24* 作为用户 ID 和 *1* 作为密码登录。）
1. 选择 **出站** 菜单，然后选择 **销售领料** 菜单项。
1. 按照屏幕上的数据输入说明输入步骤 1 中生成的工作 ID。
1. 在包含文本 **扫描牌照** 的步骤上，您应会看到您在详细信息页上所作的更改。 字段将按照您为提升的字段设置的顺序显示，**位置** 字段以粗体显示。
