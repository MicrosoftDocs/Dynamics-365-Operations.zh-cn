---
title: 配置依赖操作的 ER 目标
description: 本文介绍如何为配置为生成出站文档的电子报告 (ER) 格式配置依赖操作的目标。
author: kfend
ms.date: 12/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.form: ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: 80a432a431891c02e4bf5c71cfe2bd9642c41c75
ms.sourcegitcommit: e9000d0716f7fa45175b03477c533a9df2bfe96d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/13/2022
ms.locfileid: "9843789"
---
# <a name="configure-action-dependent-er-destinations"></a>配置依赖操作的 ER 目标

[!include [banner](../includes/banner.md)]

您可以为用于生成出站文档的[电子报告 (ER)](general-electronic-reporting.md) 格式[配置](general-electronic-reporting.md#Configuration)的每个输出组件（文件夹或文件）配置[目标](electronic-reporting-destinations.md)。 运行这种类型的 ER 格式、具有适当访问权限的用户，也可以在运行时更改配置的目标设置。

在 Microsoft Dynamics 365 Finance **版本 10.0.17 及更高版本** 中，ER 格式可以通过[设置](er-apis-app10-0-17.md)用户执行（通过运行该 ER 格式）的操作代码来运行。 例如，在 **应收账款** 模块中，在打印管理设置中，您可以选择一个 ER 格式来生成特定的业务文档，如普通发票。 然后，您可以选择 **查看** 预览发票，或选择 **打印** 将其发送到打印机。 如果在运行时为正在运行的 ER 格式传递了用户操作，您可以为不同的用户操作配置不同的 ER 目标。 本文说明如何为此类型的 ER 格式配置 ER 目标。

## <a name="make-action-dependent-er-destinations-available"></a>让依赖操作的 ER 目标可用

要在当前的 Finance 实例中配置依赖操作的 ER 目标，并启用 [新](er-apis-app10-0-17.md) ER API，打开 [功能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace)工作区，然后打开 **配置特定的 ER 目标以用于不同的 PM 操作** 功能。 要在运行时将已配置的 ER 目标用于报表，请启用 **根据特定于用户操作的 ER 目标路由 PM 报表的输出(第 1 波)** 功能。

## <a name="configure-action-dependent-er-destinations"></a>配置依赖操作的 ER 目标

打开 **配置特定的 ER 目标以用于不同的 PM 操作** 功能时，可以在 **电子报告目标** 页的 **文件目标** 快速选项卡上配置依赖操作的 ER 目标。 对于每个组件，您可以添加记录并启用特定的 ER 目标。 对于每个记录，您必须指定应该应用配置的 ER 目标的文档类型。 在 **文档类型** 字段中，选择以下值之一：

- 如果在运行时未提供用户操作代码，则选择 **电子** 应用配置的目标。
- 如果在运行时提供了用户操作代码，则选择 **打印管理** 应用配置的目标。
- 选择 **任何** 将始终应用配置的目标，不论在运行时是否提供了用户操作。

如果选择 **打印管理** 文档类型，则必须指定应该应用配置的 ER 目标的用户操作。 在 **打印管理操作** 字段中，选择以下值之一：

- 如果在运行时提供了 **查看** 用户操作，则选择 **查看** 应用配置的目标。
- 如果在运行时提供了 **打印** 用户操作，则选择 **打印** 应用配置的目标。
- 如果在运行时提供了 **发送** 用户操作，则选择 **发送** 应用配置的目标。

> [!NOTE]
> 可以为单个目标记录选择多个操作。

如果选择 **任何** 文档类型，将在 **打印管理操作** 字段中自动选择 **自动检测** 作为用户操作，将发生以下行为：

- 如果在运行时未提供用户操作代码，将应用所有配置的 ER 目标。
- 如果在运行时提供了用户操作代码，将应用为特定操作预定义的 ER 目标，**无论是否启用**：

    - 在运行时提供 **查看** 操作时，将应用 **屏幕** ER 目标。
    - 在运行时提供 **发送** 操作时，将应用 **电子邮件** ER 目标。
    - 在运行时提供 **打印** 操作时，将应用 **打印机** ER 目标。

例如，您可以使用 **普通发票(Excel)** ER 格式在发布[普通发票](../../../finance/accounts-receivable/create-free-text-invoice-new.md)时打印该发票。 要路由生成的文档，您必须为此 ER 格式配置 ER 目标。 例如，您可能需要配置这些 ER 目标，才能对生成的文档执行以下操作：

- 如果运行 ER 格式但未提供操作代码（例如，以电子方式发送文档时），将文档存档。
- 当用户执行 **查看** 操作时，在 Web 浏览器中预览文档。
- 用户执行 **打印** 操作时，存档并打印文档。
- 用户执行 **发送** 操作时，存档文档，并将其作为出站电子邮件的附件通过电子邮件发送。

下图显示了在为单个用户操作配置了每个记录时，如何通过将 ER 目标配置为单个目标记录集来实现此目的：

![为单个用户操作配置每个目标记录时，具有针对 ER 格式的依赖操作的目标设置的电子报告目标页面。](./media/er-destination-action-dependent-01.png)

下图显示了在为单个目标配置了每个记录时，如何另外通过将 ER 目标配置为单个目标记录集来实现相同目的：

![为单个目标配置每个目标记录时，具有针对 ER 格式的依赖操作的目标设置的电子报告目标页面。](./media/er-destination-action-dependent-01a.png)

> [!NOTE]
> 如果为正在运行的 ER 格式提供了操作代码，但尚未为该操作代码配置目标，将应用[默认](electronic-reporting-destinations.md#default-behavior)目标行为。

## <a name="change-action-dependent-er-destinations-at-runtime"></a>在运行时更改依赖操作的 ER 目标

ER 格式运行时，如果用户操作已由具有适当[权限](electronic-reporting-destinations.md#security-considerations)可以在运行时更改配置的目标设置的用户设置，将出现一个对话框，提供更改已配置目标设置的选项。 此对话框是可选的，其外观取决于 ER 框架发起的运行 ER 格式的调用如何实现。 如果出现此对话框，其中的 ER 目标将根据提供的用户操作启用。

下图显示了如果已设置 **打印机** 操作并为此格式配置了 ER 目标（如本文前面所示），在 [发布](../../../finance/accounts-receivable/create-free-text-invoice-new.md)普通发票和运行 **普通发票(Excel)** ER 格式生成此文档时，出现的 **电子报告格式目标** 对话框的示例。

![提供更改为正在运行的 ER 格式初始配置的 ER 目标的选项的对话框。](./media/er-destination-action-dependent-02.gif)

> [!NOTE]
> 如果您为正在运行的 ER 格式的多个组件配置了 ER 目标，将为每个已配置的 ER 格式组件单独提供一个选项。

如果多种 ER 格式适合用作所选文档的报告模板，则所有适用的 ER 报告模板的所有 ER 目标都将显示在对话框中，并可在运行时进行手动调整。

如果没有 [SQL Server 报告服务 (SSRS)](SSRS-report.md) 报告模板适用于所选文档，则会动态隐藏打印管理目标的标准选项。

从 Finance 版本 **10.0.31** 开始，您可以在运行时为以下业务文档手动更改分配的 ER 目标：

- 客户帐户对帐单
- 利息单
- 催款单
- 客户付款通知
- 供应商付款通知

要激活在运行时更改 ER 目标的功能，请启用 [功能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace)工作区中的 **允许在运行时调整 ER 目标** 功能。

> [!IMPORTANT]
> 对于 **客户付款通知** 和 **供应商付款通知** 报告，手动更改 ER 目标的功能仅在 **ForcePrintJobSettings** 外部测试版启用后才可用。

[![在运行时调整 ER 目标。](./media/ERdestinaiotnChangeUI.jpg)](./media/ERdestinaiotnChangeUI.jpg)

> [!NOTE]
> 在 **使用打印管理目标** 选项设置为 **是** 时，系统使用为特定 ER 报告配置的默认 ER 目标。 在对话框中进行的所有手动更改都将被忽略。 将 **使用打印管理目标** 选项设置为 **否**，以在即将运行报告之前将文档处理到对话框中定义的 ER 目标。

以下业务文档在运行时未假定用户明确选择操作：

- 客户帐户对帐单
- 利息单
- 催款单
- 客户付款通知
- 供应商付款通知

以下逻辑用于确定在处理上述报告时使用哪个操作：

- 如果启用了 **ForcePrintJobSettings** 外部测试版：

    - 如果 **使用打印管理目标** 选项设置为 **是**，则使用 **打印** 操作。
    - 如果 **使用打印管理目标** 选项设置为 **否**，则使用 **查看** 操作。

- 如果未启用 **ForcePrintJobSettings** 外部测试版：

    - 如果 **使用打印管理目标** 选项设置为 **是**，则对 **客户付款通知** 和 **供应商付款通知** 报告使用 **打印** 操作。
    - 如果 **使用打印管理目标** 选项设置为 **否**，则对 **客户付款通知** 和 **供应商付款通知** 报告始终使用默认的 SSRS 报告模板。
    - **打印** 操作始终用于 **客户帐户对帐单**、**利息单** 和 **催款单注释** 报告。

对于前面的逻辑，可以使用 **打印** 或 **查看** 操作来配置依赖于操作的 ER 报告目标。 在运行时，对话框中只会筛选为特定操作配置的 ER 目标。

## <a name="verify-the-provided-user-action"></a>验证提供的用户操作

执行特定用户操作时，可以验证为正在运行的 ER 格式提供了哪些用户操作（如果有）。 当您必须配置依赖操作的 ER 目标，但是您不确定提供了哪个用户操作代码（如果有）时，此验证很重要。 例如，当您开始发布普通发票，并将 **发布普通发票** 对话框中的 **打印发票** 选项设置为 **是** 时，您可以将 **使用打印管理目标** 选项设置为 **是** 或 **否**。

请按照下列步骤验证提供的用户操作代码。

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。
3. 在 **使用参数** 对话框中，将 **在调试模式下运行** 选项 [设置](er-trace-reports-compare-baseline.md#configure-er-parameters-to-use-the-baseline-feature)为 **是**。
4. 通过运行 ER 格式执行用户操作。 请记住，ER 用户参数是公司特定和用户特定参数。
5. 转到 **组织管理** \> **电子申报** \> **配置调试日志**。
6. 在 **配置调试日志** 页上，筛选 ER 运行日志来查找您的 ER 格式运行的日志。
7. 如果为 ER 格式运行提供了任何操作，请查看必须包含呈现所提供的用户操作代码的记录的日志条目。

    ![电子报告运行日志页面，其中包含有关为筛选出的 ER 格式运行提供的用户操作代码的信息。](./media/er-destination-action-dependent-03.png)

## <a name="additional-resources"></a>其他资源

[电子报告 (ER) 概览](general-electronic-reporting.md)

[电子报告 (ER) 目标](electronic-reporting-destinations.md)

[针对 Application update 10.0.17 的电子报告框架 API 更改](er-apis-app10-0-17.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
