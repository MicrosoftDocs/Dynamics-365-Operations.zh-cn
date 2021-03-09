---
title: 工作人员如何使用生产车间执行界面
description: 本主题从工作人员的角度介绍了如何使用生产车间执行界面。
author: johanhoffmann
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 40c6794fdf25da44a75aba4a502a89966c0ec4d0
ms.sourcegitcommit: 9dd2d38e76d4d93171315ec319e6ce7d51d4e6c7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/15/2020
ms.locfileid: "4012455"
---
# <a name="how-workers-use-the-production-floor-execution-interface"></a>工作人员如何使用生产车间执行界面

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

生产车间执行界面针对触摸交互进行了优化。 它的设计提供了视觉对比，可以满足车间环境的可访问性要求。 它提供与作业卡设备相同的所有功能。 但是，它还允许从作业列表中并行启动多个作业。 （此功能也称为 *作业捆绑* 。）此外，从作业列表中，工作人员可以打开在 Microsoft Dynamics 365 指南中创建的指南。 通过此方法，他们可以在 HoloLens 上获取视觉说明。

## <a name="sign-in-to-the-production-floor-execution-interface-as-a-worker"></a>以工作人员身份登录生产车间执行界面

在工作人员可以开始使用该设备之前，主管或技术人员必须准备该设备并在 Dynamics 365 Supply Chain Management 中打开正确的页面。 有关如何设置设备的详细信息，请参阅[设置设备以运行生产车间执行界面](production-floor-execution-setup.md)。

准备好设备后，设备上将显示登录页面。 此页面显示有关本地工作单元的作业状态的信息。 此信息会定期更新。 在该页面上，工作人员使用其锁屏提醒 ID 进行登录。 尽管工作人员不必具有 Supply Chain Management 的用户帐户，但他们必须具有可在登录时使用的 *时间登记工作人员* 帐户。

![生产车间执行界面登录页面](media/pfei-sign-in-page.png "生产车间执行界面登录页面")

本主题的其余部分介绍了工作人员如何与界面进行交互。

## <a name="all-jobs-tab"></a>所有作业选项卡

**所有作业** 选项卡提供了一个作业列表，显示状态为 *未开始* 、 *已停止* 或 *已开始* 的所有生产作业。

![所有作业选项卡](media/pfei-all-jobs-tab.png "所有作业选项卡")

作业列表具有以下列。 （数字对应上一图中的数字。）

1. **选择列** – 最左边的列使用复选标记指示工作人员已选择的作业。 工作人员可以同时在列表中选择多个作业。 若要在列表中选择所有作业，请选择列标题中的复选标记。 选择单个作业后，有关该作业的详细信息将显示在页面的下部。
1. **作业状态列** – 此列使用符号指示每个作业的状态。 此列中没有符号的作业的状态为 *未开始* 。 绿色三角形指示状态为 *已开始* 。 两个黄色竖线指示状态为 *已停止* 的作业。
1. **高优先级列** – 此列使用感叹号指示具有高优先级的作业。
1. **订单** – 此列显示作业的生产订单编号。
1. **描述** – 此列显示作业所属的工序的描述。
1. **已请求** – 此列显示作业计划生产的数量。
1. **已开始** – 此列显示作业已开始的数量。
1. **已完成** – 此列显示作业已完成的数量。
1. **已报废** – 此列显示作业已报废的数量。
1. **剩余** – 此列显示作业剩余完成的数量。

## <a name="active-jobs-tab"></a>活动作业选项卡

![活动作业选项卡](media/pfei-active-jobs-tab.png "活动作业选项卡")

**活动作业** 选项卡上的作业列表具有以下列：

- **选择列** – 最左边的列使用复选标记指示工作人员已选择的作业。 工作人员可以同时在列表中选择多个作业。 若要在列表中选择所有作业，请选择列标题中的复选标记。 选择单个作业后，有关该作业的详细信息将显示在页面的下部。
- **订单** – 此列显示作业的生产订单编号。
- **描述** – 此列显示作业所属的工序的描述。
- **已请求** – 此列显示作业计划生产的数量。
- **已开始** – 此列显示作业已开始的数量。
- **已完成** – 此列显示作业已完成的数量。
- **已报废** – 此列显示作业已报废的数量。
- **剩余** – 此列显示作业剩余完成的数量。

## <a name="starting-and-completing-production-jobs"></a>开始和完成生产作业

工作人员通过在 **所有作业** 选项卡上选择作业，然后选择 **开始作业** 以打开 **开始作业** 对话框来开始生产作业。

![开始作业对话框](media/pfei-start-job-dialog.png "开始作业对话框")

工作人员使用 **开始作业** 对话框确认生产数量，然后开始作业。 工作人员可以通过选择 **数量** 字段，然后使用出现的数字键盘来调整数量。 然后，工作人员选择 **开始** 以开始处理作业。 **开始作业** 对话框将关闭，作业将添加到 **活动作业** 选项卡。

工作人员可以开始处于任何状态的作业。 当工作人员开始状态为 *未开始* 的作业时， **开始作业** 对话框中的 **数量** 字段最初显示完整数量。 当工作人员开始状态为 *已开始* 或 *已停止* 的作业时， **数量** 字段最初显示剩余数量。

## <a name="reporting-good-quantities"></a>报告完好数量

当工作人员完成或部分完成作业时，他们可以通过在 **活动作业** 选项卡上选择作业，然后选择 **报告进度** 来报告已生产的完好数量。 然后，在 **报告进度** 对话框中，工作人员使用数字键盘输入完好数量。 默认情况下，该数量为空白。 输入数量后，工作人员可以将作业状态更新为 *进行中* 、 *已停止* 或 *已完成* 。

![报告进度对话框](media/pfei-report-progress-dialog.png "报告进度对话框")

## <a name="reporting-scrap"></a>报告废料

当工作人员完成或部分完成作业时，他们可以通过在 **活动作业** 选项卡上选择作业，然后选择 **报告废料** 来报告废料。 然后，在 **报告废料** 对话框中，工作人员使用数字键盘输入废料数量。 工作人员还将选择原因（ *无* 、 *机器* 、 *操作员* 或 *材料* ）。

![报告废料对话框](media/pfei-report-scrap-dialog.png "报告废料对话框")

## <a name="completing-a-job-and-starting-a-new-job"></a>完成作业并开始新作业

通常，工作人员通过在 **活动作业** 选项卡上选择一个或多个当前作业，然后选择 **报告进度** 来完成作业。 然后，他们输入已生产的数量（完好数量）并将状态设置为 *完成* 。 如果选择了多个作业，则工作人员将使用 **上一个** 和 **下一个** 按钮来进行切换。 若要开始新作业，工作人员在 **所有作业** 选项卡上选择它，然后选择 **开始作业** 。

工作人员也可以在上一个作业仍处于打开状态时开始新作业。 同样，工作人员在 **所有作业** 选项卡上选择新作业，然后选择 **开始作业** 。 但是，在这种情况下， **开始作业** 对话框将通知工作人员他们当前正在处理一个作业，因此他们必须在开始新作业之前停止或完成该作业。

## <a name="working-on-multiple-jobs-in-parallel"></a>并行处理多个作业

一个工作人员可以同时（即并行）处理多个作业。 在这种情况下，该工作人员正在处理的作业集称为 *作业捆绑* 。 工作人员可以将新作业添加到捆绑中，或完成捆绑中的一个或多个作业。 以下两种场景显示了工作人员如何并行处理作业。

### <a name="scenario-1-a-worker-who-has-no-active-jobs-wants-to-start-two-jobs-and-work-on-them-in-parallel"></a>场景 1：没有活动作业的工作人员想要开始两个作业并且并行处理它们

工作人员在 **所有作业** 选项卡上选择两个作业，然后选择 **开始作业** 。 **开始作业** 对话框显示这两个选定的作业，工作人员可以在每个作业上调整要开始的数量。 然后，工作人员确认对话框并可以开始这两个作业。

### <a name="scenario-2-a-worker-who-has-two-active-jobs-that-are-in-progress-wants-to-start-a-third-job-and-work-on-it-in-parallel-with-the-other-two"></a>场景 2：有两个正在进行的活动作业的工作人员想要开始第三个作业并且与其他两个作业并行处理它

工作人员在 **所有作业** 选项卡上选择第三个作业，然后选择 **捆绑** 。 在 **捆绑** 对话框中，工作人员可以调整要开始的数量。 然后，工作人员通过选择 **捆绑** 确认对话框。

## <a name="working-on-indirect-activities"></a>处理间接活动

间接活动是与生产订单不直接相关的活动。 间接活动可以灵活定义，如[设置考勤管理的间接活动](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-indirect-activities-for-time-and-attendance)中所述。

例如，Contoso 的车间工作人员 Shannon 想要参加公司会议，而会议被认为是间接活动。 以下两种场景之一适用：

- **Shannon 正在处理一个或多个活动作业。** Shannon 选择 **活动** ，确定活动（会议）并确认她的选择。 显示的消息通知她，她有正在进行的作业。 从该消息中，Shannon 可以选择在参加会议之前完成或停止她正在处理的作业。
- **Shannon 没有任何活动作业。** Shannon 选择 **活动** ，确定活动（会议），确认她的选择。 现在，她已登记参加会议。

在这两种场景下，在 Shannon 确认选择后，她都会进入登录页面或等待她确认已从间接活动中返回的页面。 显示的页面取决于生产车间执行界面的配置。 （有关详细信息，请参阅[配置生产车间执行界面](production-floor-execution-configure.md)。）

## <a name="working-on-breaks"></a>处理工间休息

工作人员可以登记工间休息。 工间休息可以灵活定义，如[基于登记付薪](pay-based-on-registrations.md)中所述。

工作人员通过选择 **工间休息** ，然后选择表示工间休息类型（例如午餐）的卡片来登记工间休息。 在工作人员确认选择后，设备将显示登录页面或等待工作人员确认他们已从工间休息返回的页面。 显示的页面取决于生产车间执行界面的配置。 （有关详细信息，请参阅[配置生产车间执行界面](production-floor-execution-configure.md)。）

## <a name="opening-instructions"></a>打开说明

工作人员可以通过选择 **说明** 打开附加到作业的文档。 仅在文档与主数据中的作业相关联时， **说明** 按钮才可用。 例如，将为工作人员提供附加到 Supply Chain Management 中 **已发布产品** 页面上的产品的文档，以在工作车间执行界面中打开。

## <a name="opening-mixed-reality-guides-for-hololens"></a>打开 HoloLens 的混合现实指南

[Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/) 可以通过提供使用混合现实的实践学习来帮助工作人员执行作业。 您可以定义通过分步说明指导工作人员使用他们所需的工具和零件的标准化流程，并展示如何在实际工作中使用这些工具。 下面是流程的概述。

1. 每当工作人员在车间执行界面中打开作业列表时，该界面将为显示的作业找到所有相关的指南。
1. 工作人员选择 **指南** 以查看指南列表。
1. 工作人员在列表中选择相关的指南。
1. 车间执行界面显示所选指南的 QR 码。
1. 工作人员使用 HoloLens 并浏览 QR 码以开始使用指南。
1. 工作人员通过指南工作以了解任务。

有关如何创建、分配和使用 HoloLens 指南的详细信息，请参阅[为生产中的工作人员提供混合现实指南](instruction-guides-in-production-overview.md)。