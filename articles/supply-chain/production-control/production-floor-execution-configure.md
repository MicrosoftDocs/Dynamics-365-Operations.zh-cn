---
title: 配置生产车间执行界面
description: 本文介绍了如何为生产车间执行界面创建一个或多个配置。 当您打开生产车间执行界面时，它将自动加载特定于浏览器和设备的选定配置和作业筛选器。 在配置中，设置必须适用于特定使用情况的策略。
author: johanhoffmann
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9eefde163473e11b01bfa0adf9b3694c830f1488
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899402"
---
# <a name="configure-the-production-floor-execution-interface"></a>配置生产车间执行界面

[!include [banner](../includes/banner.md)]

车间工作人员使用生产车间执行界面来登记他们的日常工作，例如何时开始作业、报告关于作业的反馈、登记间接活动和报告缺勤。 这些登记是跟踪生产订单的进度和成本以及计算工作人员付薪的依据的基础。

当您打开生产车间执行界面时，它将自动加载特定于浏览器和设备的选定配置和作业筛选器。 在配置中，设置必须适用于特定使用情况的策略。 下面提供了一些使用情况示例：

- 在公司大厅的设备上，员工在进入办公室时打卡上班，在当天离开办公室时打开下班。
- 在车间的设备上，机器操作员在开始和完成作业时进行登记。 他们还登记工间休息和间接活动。

本文介绍为您现场使用的每个设备配置生产车间执行界面的各种选项。

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>开启生产车间执行界面及其相关的可选功能

必须先在系统中打开生产车间执行界面本身以及本文中所述的几个可选设置，然后才能使用它们。 使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)页根据需要打开以下小节中所述的任一或所有功能。

### <a name="the-production-floor-execution-interface"></a>生产车间执行界面

这是本文介绍的主要功能，是本节中提到的所有其他功能的先决条件。 从 Supply Chain Management 10.0.25 开始，此功能是强制性的，无法关闭。 如果您运行的版本早于 10.0.25，管理员可以通过在 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区中搜索 *生产车间执行* 功能来打开或关闭此功能。

### <a name="generate-license-plates"></a>生成牌照

这些功能让牌照功能在生产车间执行界面可用。 如果您想要使用它们，请在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开以下功能（按此顺序）：

1. *用于报告为完工入库的牌照已添加作业卡设备*<br>（从 Supply Chain Management 版本 10.0.21 开始，此功能默认开启。 从 Supply Chain Management 版本 10.0.25 开始，此功能是强制性的。）
1. *在作业卡设备中报告为完工入库时，启用牌照编号的自动生成*<br>（从 Supply Chain Management 版本 10.0.25 开始，此功能是强制性的。）

### <a name="print-labels"></a>打印标签

这些功能让标签打印功能在生产车间执行界面可用。 如果您想要使用它们，请在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开以下功能（按此顺序）：

1. *用于报告为完工入库的牌照已添加作业卡设备*<br>（从 Supply Chain Management 版本 10.0.21 开始，此功能默认开启。 从 Supply Chain Management 版本 10.0.25 开始，此功能是强制性的。）
1. *通过作业卡设备打印标签*<br>（从 Supply Chain Management 版本 10.0.25 开始，此功能是强制性的。）

### <a name="allow-locking-the-touch-screen"></a>允许锁定触摸屏

此功能使工作人员可以锁定触摸屏，以便对其进行净化。

从 Supply Chain Management 版本 10.0.21 开始，此功能默认开启。 从 Supply Chain Management 10.0.25 开始，此功能是强制性的，无法关闭。 如果您运行的版本早于 10.0.25，管理员可以通过在 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区搜索 *用于锁定作业卡设备和作业卡终端以便对其进行净化的功能* 功能来打开或关闭此功能。

### <a name="asset-management-functionality-for-the-production-floor-execution-interface"></a>生产车间执行界面的资产管理功能

此功能将资产管理选项卡添加到生产车间执行界面。 工作人员可以使用此选项卡来选择连接到作业列表中所选筛选器内机器资源的资产。 对于选择的机器资产，工作人员可以通过最多四个所选计数器的计数器值查看资产的状态和运行状况。 如果您想要使用此功能，请在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开以下功能：

- *生产车间执行界面的资产管理功能*<br>（从 Supply Chain Management 版本 10.0.25 开始，此功能默认开启。）

### <a name="enable-job-search"></a>启用作业搜索

使用此功能可以将搜索字段添加到作业列表中。 工作人员可以通过输入作业 ID 来查找特定作业，或者通过输入订单 ID 来查找特定订单的所有作业。 工作人员可以使用键盘或通过扫描条码来输入 ID。 如果您想要使用它，请在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开以下功能：

- *生产车间执行界面的作业搜索*<br>（从 Supply Chain Management 版本 10.0.25 开始，此功能默认开启。）

### <a name="enable-reporting-on-co-products-and-by-products"></a>启用联产品和副产品报告

利用此功能，工作人员可以使用生产车间执行界面报告批次订单的进度。 此报告包括联产品和副产品报告。 要使用此功能，在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开以下功能：

- *报告来自生产车间执行界面的联产品和副产品*

### <a name="enable-the-display-of-full-serial-batch-and-license-plate-numbers"></a>启用显示完整序列号、批号和牌照编号

此功能为查看生产车间执行界面中的序列号、批处理和牌照号列表提供了改进的体验。 显示内容从显示有限数量字符的卡视图更改为提供足够空间来显示完整值的列表视图。 该列表还提供搜索特定数字的功能。

从 Supply Chain Management 版本 10.0.25 开始，此功能默认开启。 管理员可以通过在 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区中搜索 *在生产车间执行界面中显示完整序列、批处理和牌照编号* 功能来打开或关闭此功能。

### <a name="enable-registering-of-material-consumption"></a>启用登记物料消耗量

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

此功能使工人能够使用生产车间执行界面来登记材料消耗、批号和序列号。 一些制造商，尤其是加工行业的制造商，必须明确登记每个批次或生产订单的材料消耗量。 例如，工作人员可能会使用秤来称量他们工作时消耗的材料量。 为确保完整的材料可追溯性，这些组织还必须登记生产每个产品时消耗材料的批号。

此功能有两个版本。 一个版本支持 *未* 启用使用高级仓库流程 (WMS) 的物料。 另一个版本支持 *启用* 以使用 WMS 的物料。 要使用此功能，在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开以下一项或全部两项功能（按此顺序），具体取决于您是否有启用了 WMS 的物料：

- *(预览版)在生产车间执行界面(非 WMS)上登记物料消耗量*
- *(预览版)在生产车间执行界面(启用了 WMS)上登记物料消耗量*

> [!IMPORTANT]
> 您可以单独使用非 WMS 功能。 但是，如果使用 WMS，则必须启用全部两项功能。

### <a name="enable-reporting-on-catch-weight-items"></a>启用实际称重物料报告

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

工作人员可以使用生产车间执行界面报告实际称重物料的批次订单的进度。 批次订单是从配方创建的，配方可以定义为将实际称重物料作为配方物料、联产品和副产品。 另外还可以定义一个配方，使其具有针对实际称重定义的成分的配方行。 实际称重物料使用两种度量单位来跟踪库存：实际称重数量和库存数量。 例如，在食品行业，可以将盒装肉定义为一个实际称重物料，其中实际称重数量用于跟踪盒数，库存数量用于跟踪盒重量。

要使用此功能，在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开以下功能：

- *(预览版)报告生产车间执行界面中的实际称重物料*

### <a name="enable-the-my-day-dialog"></a>启用“我的一天”对话框

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until 10.0.27 GA -->

**我的一天** 对话框为工作人员提供了他们的每日注册以及带薪时间、带薪加班、缺勤和带薪缺勤当前余额的概览。

要使用此功能，在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开以下功能：

- *生产车间执行界面的“我的一天”视图*

### <a name="enable-teams"></a>启用 Teams

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until 10.0.27 GA -->

在将多个工作人员分配到同一个生产作业时，他们可以组成一个团队。 团队可以指定一个工作人员作为指导员。 那么剩下的工作人员会自动成为该指导员的助手。 对于所生成的团队，只有指导员必须登记作业状态。 时间记录适用于所有团队成员。

要使用此功能，在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开以下功能：

- *生产车间执行界面中的生产团队*

### <a name="enable-additional-configuration-in-the-production-floor-execution-interface"></a>在生产车间执行界面中启用其他配置

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until 10.0.27 GA -->

此功能将以下功能的设置添加到 **配置生产车间执行** 页面：

- 搜索完成后自动打开 **开始作业** 对话框。
- 搜索完成后自动打开 **报告进度** 对话框。
- 在 **报告进度** 对话框中预填充剩余数量。
- 从 **报告进度** 对话框启用材料消耗调整。 （此功能还需要 *在生产车间执行界面(非 WMS)上登记物料消耗量* 功能。）
- 按项目 ID 启用搜索。

本文后面将提供有关如何使用这些设置的信息。

要使用此功能，在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开以下功能：

- *生产车间执行界面上的其他配置*


## <a name="work-with-production-floor-execution-configurations"></a>使用生产车间执行配置

要创建和维护生产车间执行配置，请转到 **生产控制 \> 设置 \> 制造执行 \> 配置生产车间执行**。 **配置生产车间执行** 页面显示现有配置的列表。 在此页面上，您可以执行以下操作：

- 选择左列中列出的任何生产车间配置来查看和编辑它。
- 在操作窗格中选择 **新建** 将新配置添加到列表中。 然后，在 **配置** 字段中，输入名称来标识新配置。 您输入的名称在所有配置中必须是唯一的，以后无法再对其进行编辑。 在 **描述** 字段中，您可以有选择性地输入配置的说明。

接下来，配置所选配置的各种设置，如以下小节所述。

### <a name="the-general-fasttab"></a>“常规”快速选项卡

**常规** 快速选项卡上提供以下设置：

- **仅上下班打卡** - 将此选项设置为 *是* 将创建仅提供上班打卡和下班打卡功能的简化界面。 此设置将禁用此页面上的大多数其他选项。 您必须先从 **选项卡选择** 快速选项卡中删除所有行，然后才能启用此选项。
- **启用搜索** - 将此选项设置为 *是* 将在作业列表中包含搜索字段。 工作人员可以通过输入作业 ID 来查找特定作业，或者他们可以通过输入订单 ID 来查找特定订单的所有作业。 工作人员可以使用键盘或通过扫描条码来输入 ID。
- **按项目 ID 启用搜索** - 将此选项设置为 *是*，以使工作人员能够在生产车间执行界面的搜索字段中按项目 ID（以及作业 ID 和订单 ID）进行搜索。 仅当 **启用搜索** 选项也设置为 *是*，才能将此选项设置为 *是*。
- **自动打开开始对话框** – 如果此选项设置为 *是*，那么当工作人员使用搜索栏查找作业时，将自动打开 **开始作业** 对话框。
- **自动打开报告进度对话框** – 如果此选项设置为 *是*，那么当工作人员使用搜索栏查找作业时，将自动打开 **报告进度** 对话框。
- **启用调整材料** - 将此选项设置为 *是* 可以在 **报告进度** 对话框中启用 **调整材料** 按钮。 工作人员可以选择此按钮以调整作业的物料消耗量。
- **在下班打卡时报告数量** – 将此选项设置为 *是* 以提示工作人员在下班打卡时报告有关正在进行的作业的反馈。当此选项设置为 *否* 时，不会提示工作人员。
- **锁定员工** – 当此选项设置为 *否* 时，在工作人员进行登记（例如新作业）后，他们将立即注销。 然后，界面将返回到登录页面。 当此选项设置为 *是* 时，工作人员将在生产车间执行界面保持登录状态。 但是，工作人员可以手动注销，以便其他工作人员可以在生产车间执行界面继续在同一系统用户帐户下运行的同时登录。 有关这些帐户的类型的详细信息，请参阅[指定的用户](config-job-card-device.md#assigned-users)。
- **使用实际登记时间** – 将此选项设置为 *是* 以将每个新登记的时间设置为工作人员提交登记时的确切时间。 当此选项设置为 *否* 时，改为使用登录时间。 如果您在工作人员通常在更长时间内保持登录状态的情况下已将 **锁定员工** 和/或 **单个工作人员** 选项设置为 *是*，通常需要将此选项设置为 *是*。
- **单个工作人员** – 如果只有一个工作人员使用此配置已激活的每个生产车间执行界面，请将此选项设置为 *是*。 当此选项设置为 *是* 时，**锁定员工** 选项将自动设置为 *是*。 另外，此设置消除了工作人员使用锁屏提醒 ID（或其他类似 ID）登录的要求（和能力）。 工作人员改为使用链接到 *已登记时间的工作人员*（在 *工作人员* 表中）的系统用户帐户登录到 Microsoft Dynamics 365 Supply Chain Management，并同时以该工作人员的身份登录到生产车间执行界面。
- **允许锁定触摸屏** – 将此选项设置为 *是* 以允许工作人员锁定生产车间执行界面的触摸屏，以便他们可以净化屏幕。 当此选项设置为 *是* 时，将向登录页面添加 **锁定屏幕以净化** 按钮。 当工作人员选择此按钮时，触摸屏会暂时锁定以防止意外输入。 还显示了倒计时计时器。 然后，工作人员可以安全地净化设备和屏幕。 倒计时完成后，触摸屏将自动解锁。
- **屏幕锁定持续时间** – 当 **允许锁定触摸屏** 选项设置为 *是* 时，请使用此选项指定触摸屏应该锁定进行净化的秒数。 持续时间必须在 5 到 120 秒之间。
- **生成牌照** – 将此选项设置为 *是*，每次工作人员使用生产车间执行界面报告为已完工入库时，都会生成新牌照。 牌照编号根据在 **仓库管理参数** 页面上设置的编号规则生成。 当此选项设置为 *否* 时，工作人员必须在报告为已完工入库时指定一个现有牌照。
- **打印标签** – 将此选项设置为 *是*，以在工作人员使用生产车间执行界面报告为已完工入库时打印牌照标签。 标签的配置在文档路线中设置，如[牌照标签的文档路线选择布局](../warehousing/document-routing-layout-for-license-plates.md)中所述。

### <a name="the-tab-selection-fasttab"></a>“选项卡选择”快速选项卡

使用 **选项卡选择** 快速选项卡中的设置，可以选择当前配置处于活动状态时，生产车间执行界面应显示哪些选项卡。 您可以根据需要设计任意数量的选项卡，然后使用快速选项卡工具栏上的按钮根据需要添加和排列它们。 有关如何在此处设计选项卡和处理设置的信息，请参阅[设计生产车间执行界面](production-floor-execution-tabs.md)。

### <a name="the-report-progress-fasttab"></a>“报告进度”快速选项卡

**报告进度** 快速选项卡上提供以下设置：

- **启用调整材料** - 将此选项设置为 *是* 可以在 **报告进度** 对话框中包含 **调整材料** 按钮。 工作人员可以选择此按钮以调整作业的物料消耗量。
- **默认剩余数量** – 将此选项设置为 *是* 以在 **报告进度** 对话框中预填充生产作业的预期剩余数量。

## <a name="clean-up-job-configurations"></a>清理作业配置

当车间主管设置生产车间执行界面时，将选择配置和作业筛选器。 这些选择存储在 Supply Chain Management 中的引用表中，浏览器使用存储在本地 Cookie 中的 ID 在该表中找到正确的行。 该表还记录了工作人员上次登录每个设备的日期和时间。

对于最近 60 天内未记录任何活动的设备，批处理作业会定期清理引用表中的条目。 您也可以随时按照以下步骤手动清理条目。

1. 转到 **生产控制 \> 设置 \> 制造执行 \> 配置生产车间执行**。
1. 在“操作”窗格上，选择 **清理客户端配置**。
1. 在 **清理客户端配置** 对话框中，将 **天数** 字段设置为要考虑的不活动天数（今天之前）。 您将删除在此期间未处于活动状态的设备的所有配置和登录记录。
1. 选择 **确定** 以根据 **天数** 设置清理相关的配置。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
