---
title: 为移动设备菜单项中的步骤配置绕过
description: 本文介绍如何配置菜单项的绕过，以便工作人员可以停止当前任务，执行另一个任务，之后返回原始任务时不会丢失任何信息。
author: Mirzaab
ms.date: 09/01/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour, WHSMobileAppFlowStepDetourSelectFields, WHSMobileAppFlowStepSelectPromotedFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 2e387dd4e6499912f2d53dddc17ccc053f1ca699
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689302"
---
# <a name="configure-detours-for-steps-in-mobile-device-menu-items"></a>为移动设备菜单项中的步骤配置绕过

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 10.0.31 GA -->

> [!IMPORTANT]
> 本文中描述的功能仅适用于新的 Warehouse Management 移动应用。 它们不影响旧仓库应用，该应用现在已弃用。

本文介绍如何配置菜单项的绕过，以便工作人员可以“停止”当前任务，执行另一个任务，之后返回原始任务时不会丢失任何信息。

绕过是一个可以从主任务中的步骤打开的单独菜单项。 在绕过结束时，工作人员将返回到他们离开主任务的位置。 在配置期间，您要指定应充当绕过的菜单项。 您还要选择主任务中的哪些字段值应自动转发（复制）到绕过并在那里输入。 因此，您必须了解您希望工作人员可以在任务流中的哪个位置使用绕过。 您还必须确保必须复制到绕过的信息可用于任务流的这一步骤。

## <a name="enable-detours-in-your-system"></a>在系统中启用绕过

您必须先完成以下过程来启用所需的功能并在 Warehouse Management 移动应用中生成所需的字段名称，然后才能够为移动设备菜单项中的步骤配置绕过。

1. 转到 **系统管理 \> 工作区 \> 功能管理**。
1. 确保为您的系统启用 *仓库应用步骤说明* 功能。 从 Supply Chain Management 版本 10.0.29 开始，此功能默认开启。 有关 *仓库应用步骤说明* 功能的详细信息，请参阅[自定义 Warehouse Management 移动应用的步骤标题和说明](mobile-app-titles-instructions.md)。 此功能是 *Warehouse management 应用绕过* 功能的先决条件。
1. 打开以下功能，这些功能提供本文所述的功能：
    - *Warehouse Management 应用绕过*<br>（从 Supply Chain Management 版本 10.0.29 开始，此功能默认开启。）
    - *Warehouse Management 移动应用的多级绕过*
    - *为 Warehouse Management 移动应用自动提交绕过步骤*
1. 如果 *Warehouse Management 应用绕过* 和/或 *Warehouse Management 移动应用的多级绕过* 功能尚未开启，请转到 **Warehouse management \> 设置 \> 移动设备 \> 仓库应用字段名称**，选择 **创建默认设置**，更新 Warehouse Management 移动应用中的字段名称。 有关详细信息，请参阅[为仓库管理移动应用配置字段](configure-app-field-names-priorities-warehouse.md)。
1. 对您使用 Warehouse Management 移动应用的每个法人（公司）重复上一步。

## <a name="configure-a-detour-from-a-menu-specific-override"></a>从特定于菜单的替代配置绕过

使用以下过程从特定于菜单的替代设置绕过。

1. 为相关的菜单和步骤创建特定于菜单的替代，如[自定义 Warehouse Management 移动应用的步骤标题和说明](mobile-app-titles-instructions.md)中所述。
1. 查找要编辑的 **步骤 ID** 与 **菜单项名称** 值组合，然后选择 **步骤 ID** 列中的值。
1. 在出现的页面上，在 **可用绕过(菜单项)** 快速选项卡上，您可以指定应作为绕过的菜单项。 您还可以选择主任务中的哪些字段值应自动复制到绕过中或从绕过中复制。 有关显示如何使用这些设置的示例，请参阅本文后面的场景。

## <a name="sample-scenario-1-sales-picking-where-a-location-inquiry-acts-as-a-detour"></a><a name="scenario-1"></a>示例场景 1：位置查询充当绕过的销售领料

此场景展示如何在工作人员导向的销售领料任务流中将位置查询配置为绕过。 此绕过将使工作人员能够在他们领料的位置查找所有牌照，并选取他们想要用来完成领料的牌照。 如果条形码损坏并因此无法被扫描仪设备读取，这种类型的绕过可能会很有用。 或者，如果工作人员必须了解系统中实际的现有量，这可能很有用。 请注意，此场景仅在您从牌照控制的位置领料时适用。

### <a name="enable-sample-data"></a>启用示例数据

要使用指定的示例记录和值完成此场景，您必须使用已安装标准[演示数据](../../fin-ops-core/fin-ops/get-started/demo-data.md)的系统。 开始前，还必须选择 **USMF** 法人。

### <a name="create-a-menu-specific-override-and-configure-the-detour-for-scenario-1"></a>创建特定于菜单的替代并为场景 1 配置绕过

在此过程中，您将为牌照步骤中的 **销售领料** 菜单项配置绕过。

1. 转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备步骤**。
1. 找到名为 *LicensePlateId* 的步骤 ID，选择它。
1. 在操作窗格中选择 **添加步骤配置**。
1. 在下拉对话框中，使用 **菜单项** 字段查找并选择 *销售领料*。
1. 选择 **确定**。
1. 您刚才创建的替代的详细信息页将显示。 在 **可用绕过(菜单项)** 快速选项卡上，选择工具栏上的 **添加**。
1. 在 **添加绕过** 对话框中，选择 **位置查询** 作为要在 Warehouse Management 移动应用中提供的绕过。
1. 选择 **确定**。
1. 在 **可用绕过(菜单项)** 快速选项卡上，选择刚才添加的绕过，然后在工具栏上选择 **选择要发送的字段**。
1. 在 **选择要发送的字段** 对话框中，指定应该发送到绕过和从绕过发送的信息。 在此场景中，您使工作人员能够使用他们应该领料的位置作为位置查询绕过的输入。 因此，在 **从销售领料发送** 部分，选择工具栏上的 **添加** 向网格中添加一行。 然后，针对新行设置以下值：

    - **从销售领料复制**：*位置*
    - **粘贴到位置查询中**：*位置*
    - **自动提交**：*已选择*（页面将使用粘贴的 *位置* 值刷新）

1. 由于此场景中的绕过是在牌照步骤上配置的，当工作人员可以将牌照从查询带回主流时，它会很有用。 因此，在 **从位置查询带回** 部分，选择工具栏上的 **添加** 向网格中添加一行。 然后，针对新行设置以下值：

    - **从位置查询复制**：*牌照*
    - **粘贴到销售领料中**：*牌照*
    - **自动提交**：*已清除*（当从具有 *牌照* 值的绕过返回时，不会自动更新）

1. 选择 **确定**。

绕过现已完全配置。 用于启动 **位置查询** 绕过的按钮现在将出现在 **销售领料** 菜单项的牌照步骤上。

### <a name="complete-a-sales-pick-on-a-mobile-device-and-use-the-detour"></a>在移动设备上完成销售领料并使用绕过

在此过程中，您将使用 Warehouse Management 移动应用完成销售领料。 您将使用您刚才配置的绕过来查找您将用于完成领料步骤的牌照。

1. 在 Microsoft Dynamics 365 Supply Chain Management 中，创建一个销售订单，该销售订单需要从已跟踪牌照的位置领料的领料步骤。 然后将销售订单下达到仓库。 记下生成的工作 ID。
1. 打开 Warehouse Management 移动应用，登录仓库 24。 （在标准演示数据中，使用 *24* 作为用户 ID 和 *1* 作为密码登录。）
1. 选择 **出站** 菜单，然后选择 **销售领料** 菜单项。
1. 按照屏幕上的数据输入说明输入步骤 1 中生成的工作 ID。
1. 在包含文本 **扫描牌照** 的步骤上，打开操作菜单。 您应会看到一个标记为 **位置查询** 的新按钮。 左上角的箭头指示按钮将启动绕过。 选择 **位置查询**。
1. 绕过将启动。 在下一页上，确认从主流复制的位置。
1. 在位置中的可用牌照列表中，点击要复制回主流的牌照。 然后选择 **返回** 按钮。
1. 您已返回到销售领料主流，牌照已被从绕过复制回主流。 确认值以继续下一步。
1. 您现在可以通过输入请求的数据输入说明来完成标准流的其余部分。

仓库工作现已完成。 工人在不失去他们在主任务中的位置的情况下成功打开了执行次要任务（位置查询）的绕过，并带回了完成主任务所需的信息。

## <a name="sample-scenario-2-item-inquiry-with-movement-and-adjustment-detours"></a>示例场景 2：使用移动和调整绕过的物料查询

此场景展示如何在位置查询任务流中将移动和调整配置为多个绕过。 在工作人员到达某个位置，发现该位置的库存与系统中登记的不同，因此必须调整或移动货物的情况下，此功能非常有用。

您可以根据需要将位置查询替换为牌照查询或物料查询。

### <a name="enable-sample-data"></a>启用示例数据

要使用指定的示例记录和值完成此场景，您必须使用已安装标准[演示数据](../../fin-ops-core/fin-ops/get-started/demo-data.md)的系统。 开始前，还必须选择 **USMF** 法人。

### <a name="create-a-menu-specific-override-and-configure-the-detour-for-scenario-2"></a>创建特定于菜单的替代并为场景 2 配置绕过

在此过程中，您将为牌照步骤中的 **销售领料** 菜单项配置绕过。

1. 转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备步骤**。
1. 查找并选择名为 *LocationInquiryList* 的步骤 ID。

    > [!NOTE]
    > 要使用物料查询而不是位置查询，请选择步骤 ID 名为 *ItemInquiryList* 的行。 要使用牌照查询，请选择步骤 ID 名为 *LPInquiryList* 的行。

1. 在操作窗格中选择 **添加步骤配置**。
1. 在下拉对话框中，使用 **菜单项** 字段查找并选择 *位置查询*。
1. 选择 **确定**。
1. 您刚才创建的替代的详细信息页将显示。 在 **可用绕过(菜单项)** 快速选项卡上，选择工具栏上的 **添加**。
1. 在 **添加绕过** 对话框中，选择 **移动** 作为要在 Warehouse Management 移动应用中提供的绕过。
1. 选择 **确定**。
1. 在 **可用绕过(菜单项)** 快速选项卡上，选择刚才添加的绕过，然后在工具栏上选择 **选择要发送的字段**。
1. 在 **选择要发送的字段** 对话中，指定应该发送到绕过和从绕过发送的信息。 在此场景中，您预期到工作人员会查找牌照控制的位置。 因此，将牌照从查询复制到 **移动** 绕过会有帮助。 在 **从销售领料发送** 部分，选择工具栏上的 **添加** 向网格中添加一行。 然后，针对新行设置以下值：

    - **从位置查询复制**：*位置*
    - **在移动中粘贴**：*位置/牌照*
    - **自动提交**：*已清除*（不会自动更新）

    在此绕过中，您预期不会有任何信息被复制回来，因为主流是不需要额外步骤的查询。

1. 选择 **确定**。

绕过现已完全配置。 用于启动 **移动** 绕过的按钮现在将出现在 **位置查询** 菜单项的牌照步骤上。

### <a name="do-a-location-inquiry-on-a-mobile-device-and-use-the-detour"></a>在移动设备上执行位置查询并使用绕过

在此过程中，您将使用 Warehouse Management 移动应用执行位置查询。 然后，您将使用绕过完成货物移动。

1. 打开 Warehouse Management 移动应用，登录仓库 24。 （在标准演示数据中，使用 *24* 作为用户 ID 和 *1* 作为密码登录。）
1. 选择 **库存** 菜单，然后选择 **位置查询** 菜单项。
1. 输入要查询的位置，如 *FL-001*。
1. 列表显示后，点击并按住其中的一个卡以显示可用绕过。
1. 选择 **移动**。
1. 请注意，牌照已从您选择的卡中复制。 确认值。
1. 您现在可以按照标准任务流完成移动。 工作完成后，打开操作菜单，选择 **取消**。
1. 您将返回到 **位置查询** 页面。 请注意，值不会自动更新。 因此，您必须手动刷新页面才能看到移动绕过的变化。

> [!NOTE]
> *Warehouse Management 移动应用的多级绕过* 功能使您能够定义多级绕过（绕过内的绕过），这将允许工作人员从现有的绕过跳到另一个，然后再跳回。 此功能支持两个级别的现成绕过，如有必要，您可以通过在 `WHSWorkUserSessionState` 表上创建代码扩展来自定义系统以支持三个或更多级别的绕过。
>
> *为 Warehouse Management 移动应用自动提交绕过步骤* 功能可以让工作人员在 Warehouse Management 移动应用中更快、更轻松地完成绕过流。 它可以通过让应用在后端填充绕过数据来跳过一些流步骤，然后通过自动提交页面自动移动到下一步，如 [*示例场景 1：位置查询充当绕过的销售领料*](#scenario-1)中所示。
