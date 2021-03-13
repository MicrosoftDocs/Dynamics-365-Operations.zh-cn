---
title: 配置生产车间执行界面
description: 本主题介绍了如何为生产车间执行界面创建一个或多个配置。 当您打开生产车间执行界面时，它将自动加载特定于浏览器和设备的选定配置和作业筛选器。 在配置中，设置必须适用于特定使用情况的策略。
author: johanhoffmann
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: e822463ac80be3b1e498f02cb1aad2b214fed815
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2021
ms.locfileid: "5077469"
---
# <a name="configure-the-production-floor-execution-interface"></a>配置生产车间执行界面

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

车间工作人员使用生产车间执行界面来登记他们的日常工作，例如何时开始作业、报告关于作业的反馈、登记间接活动和报告缺勤。 这些登记是跟踪生产订单的进度和成本以及计算工作人员付薪的依据的基础。

当您打开生产车间执行界面时，它将自动加载特定于浏览器和设备的选定配置和作业筛选器。 在配置中，设置必须适用于特定使用情况的策略。 下面提供了一些使用情况示例：

- 在公司大厅的设备上，员工在进入办公室时打卡上班，在当天离开办公室时打开下班。
- 在车间的设备上，机器操作员在开始和完成作业时进行登记。 他们还登记工间休息和间接活动。

本主题介绍配置作业卡设备的各个选项。

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>开启生产车间执行界面及其相关的可选功能

必须先在系统中打开生产车间执行界面本身以及本主题中所述的几个可选设置，然后才能使用它们。 使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)页根据需要打开以下小节中所述的任一或所有功能。

### <a name="the-production-floor-execution-interface"></a>生产车间执行界面

这是此主题中所述的主要功能。 它将生产车间执行界面添加到您的系统。 要启用它，请在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开以下功能：  
- 生产车间执行

### <a name="generate-license-plates"></a>生成牌照

这些功能让牌照功能在生产车间执行界面可用。 如果您想要使用它们，请在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开以下功能（按此顺序）：

1. 用于报告为完工入库的牌照已添加作业卡设备
1. 在作业卡设备中报告为完工入库时，启用牌照编号的自动生成

### <a name="print-labels"></a>打印标签

这些功能让标签打印功能在生产车间执行界面可用。 如果您想要使用它们，请在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开以下功能（按此顺序）：

1. 用于报告为完工入库的牌照已添加作业卡设备
1. 通过作业卡设备打印标签

### <a name="allow-locking-the-touch-screen"></a>允许锁定触摸屏

此功能在生产车间执行界面中添加了一个按钮，让工作人员可以对触摸屏进行净化。 如果您想要使用它，请在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开以下功能：

- 用于锁定作业卡设备和作业卡终端以便对其进行净化的功能

### <a name="asset-management-functionality-for-the-production-floor-execution-interface"></a>生产车间执行界面的资产管理功能

此功能将资产管理选项卡添加到生产车间执行界面。 工作人员可以使用此选项卡来选择连接到作业列表中所选筛选器内机器资源的资产。 对于选择的机器资产，工作人员可以通过最多四个所选计数器的计数器值查看资产的状态和运行状况。 如果您想要使用此功能，请在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开以下功能：

- 生产车间执行界面的资产管理功能

## <a name="work-with-production-floor-execution-configurations"></a>使用生产车间执行配置

若要创建和维护设备配置，请转到 **生产控制 \> 设置 \> 制造执行 \> 配置生产车间执行**。 **配置生产车间执行** 页面显示现有配置的列表。 在此页面上，您可以执行以下操作：

- 选择左列中列出的任何生产车间配置来查看和编辑它。
- 在操作窗格中选择 **新** 将新设备配置添加到列表中。 然后，在 **配置** 字段中，输入名称来标识新配置。 您输入的名称在所有设备配置中必须是唯一的，以后无法再对其进行编辑。

接下来，配置所选设备配置的各种设置。 提供以下字段：

- **在下班打卡时报告数量** – 将此选项设置为 *是* 以提示工作人员在下班打卡时报告有关正在进行的作业的反馈。当此选项设置为 *否* 时，不会提示工作人员。
- **锁定员工** – 当此选项设置为 *否* 时，在工作人员进行登记（例如新作业）后，他们将立即注销。 然后，设备将返回到登录页面。 当此选项设置为 *是* 时，工作人员将在作业卡设备中保持登录状态。 但是，工作人员可以手动注销，以便其他工作人员可以在作业卡设备继续在同一系统用户帐户下运行的同时登录。 有关这些帐户的类型的详细信息，请参阅[指定的用户](config-job-card-device.md#assigned-users)。
- **使用实际登记时间** – 将此选项设置为 *是* 以将每个新登记的时间设置为工作人员提交登记时的确切时间。 当此选项设置为 *否* 时，改为使用登录时间。 如果您在工作人员通常在更长时间内保持登录状态的情况下已将 **锁定员工** 和/或 **单个工作人员** 选项设置为 *是*，通常需要将此选项设置为 *是*。
- **单个工作人员** – 如果只有一个工作人员使用此配置已激活的每个作业卡设备，请将此选项设置为 *是*。 当此选项设置为 *是* 时，**锁定员工** 选项将自动设置为 *是*。 另外，此设置消除了工作人员使用锁屏提醒 ID（或其他类似 ID）登录的要求（和能力）。 工作人员改为使用链接到 *已登记时间的工作人员*（在 *工作人员* 表中）的系统用户帐户登录到 Microsoft Dynamics 365 Supply Chain Management，并同时以该工作人员的身份登录到作业卡设备。
- **允许锁定触摸屏** – 将此选项设置为 *是* 以允许工作人员锁定作业卡设备的触摸屏，以便他们可以净化设备。 当此选项设置为 *是* 时，将向设备登录页面添加 **锁定屏幕以净化** 按钮。 当工作人员选择此按钮时，触摸屏会暂时锁定以防止意外输入。 还显示了倒计时计时器。 然后，工作人员可以安全地净化设备和屏幕。 倒计时完成后，触摸屏将自动解锁。
- **屏幕锁定持续时间** – 当 **允许锁定触摸屏** 选项设置为 *是* 时，请使用此选项指定触摸屏应该锁定进行净化的秒数。 持续时间必须在 5 到 120 秒之间。
- **生成牌照** – 将此选项设置为 *是*，每次工作人员使用作业卡设备报告为已完工入库时，都会生成新牌照。 牌照编号根据在 **仓库管理参数** 页面上设置的编号规则生成。 当此选项设置为 *否* 时，工作人员必须在报告为已完工入库时指定一个现有牌照。
- **打印标签** – 将此选项设置为 *是*，以在工作人员使用作业卡设备报告为已完工入库时打印牌照标签。 标签的配置在文档路线中设置，如[牌照标签的文档路线选择布局](../warehousing/document-routing-layout-for-license-plates.md)中所述。
- **选项卡选择** – 使用此节中的设置选择当前配置处于活动状态时，生产车间执行界面应显示哪些选项卡。 您可以根据需要设计任意数量的选项卡，然后根据需要在此处添加和排列。 有关如何在此处设计选项卡和处理设置的详细信息，请参阅[设计生产车间执行界面](production-floor-execution-tabs.md)。

## <a name="clean-up-job-configurations"></a>清理作业配置

当车间主管设置生产车间执行界面时，将选择配置和作业筛选器。 这些选择存储在 Supply Chain Management 中的引用表中，浏览器使用存储在本地 Cookie 中的 ID 在该表中找到正确的行。 该表还记录了工作人员上次登录每个设备的日期和时间。

对于最近 60 天内未记录任何活动的设备，批处理作业会定期清理引用表中的条目。 您也可以随时按照以下步骤手动清理条目。

1. 转到 **生产控制 \> 设置 \> 制造执行 \> 配置生产车间执行**。
1. 在“操作”窗格上，选择 **清理客户端配置**。
1. 在 **清理客户端配置** 对话框中，将 **天数** 字段设置为要考虑的不活动天数（今天之前）。 您将删除在此期间未处于活动状态的设备的所有配置和登录记录。
1. 选择 **确定** 以根据 **天数** 设置清理相关的配置。
