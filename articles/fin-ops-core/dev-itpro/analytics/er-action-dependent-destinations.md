---
title: 配置依赖操作的 ER 目标
description: 本主题介绍如何为配置为生成出站文档的电子报告 (ER) 格式配置依赖操作的目标。
author: NickSelin
ms.date: 02/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 7decdb1d759284c616ecf928c10f99098627472d
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893570"
---
# <a name="configure-action-dependent-er-destinations"></a><span data-ttu-id="51438-103">配置依赖操作的 ER 目标</span><span class="sxs-lookup"><span data-stu-id="51438-103">Configure action-dependent ER destinations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51438-104">您可以为用于生成出站文档的[电子报告 (ER)](general-electronic-reporting.md) [格式](general-electronic-reporting.md#FormatComponentOutbound)[配置](general-electronic-reporting.md#Configuration)的每个输出组件（文件夹或文件）配置[目标](electronic-reporting-destinations.md)。</span><span class="sxs-lookup"><span data-stu-id="51438-104">You can configure [destinations](electronic-reporting-destinations.md) for each output component (folder or file) of an [Electronic reporting (ER)](general-electronic-reporting.md) [format](general-electronic-reporting.md#FormatComponentOutbound) [configuration](general-electronic-reporting.md#Configuration) that is used to generate an outbound document.</span></span> <span data-ttu-id="51438-105">运行这种类型的 ER 格式、具有适当访问权限的用户，也可以在运行时更改配置的目标设置。</span><span class="sxs-lookup"><span data-stu-id="51438-105">Users who run an ER format of this type, and who have appropriate access rights, can also change the configured destination settings at runtime.</span></span>

<span data-ttu-id="51438-106">在 Microsoft Dynamics 365 Finance **版本 10.0.17 及更高版本** 中，ER 格式可以通过[设置](er-apis-app10-0-17.md)用户执行（通过运行该 ER 格式）的操作代码来运行。</span><span class="sxs-lookup"><span data-stu-id="51438-106">In Microsoft Dynamics 365 Finance **version 10.0.17 and later**, an ER format can be run by [provisioning](er-apis-app10-0-17.md) an action code that the user performs by running that ER format.</span></span> <span data-ttu-id="51438-107">例如，在 **应收账款** 模块中，在打印管理设置中，您可以选择一个 ER 格式来生成特定的业务文档，如普通发票。</span><span class="sxs-lookup"><span data-stu-id="51438-107">For example, in the **Accounts receivable** module, in the Print management settings, you can select an ER format that generates a specific business document, such as a free text invoice.</span></span> <span data-ttu-id="51438-108">然后，您可以选择 **查看** 预览发票，或选择 **打印** 将其发送到打印机。</span><span class="sxs-lookup"><span data-stu-id="51438-108">You can then select **View** to preview the invoice or **Print** to send it to a printer.</span></span> <span data-ttu-id="51438-109">如果在运行时为正在运行的 ER 格式传递了用户操作，您可以为不同的用户操作配置不同的 ER 目标。</span><span class="sxs-lookup"><span data-stu-id="51438-109">If a user action is passed for the running ER format at runtime, you can configure different ER destinations for different user actions.</span></span> <span data-ttu-id="51438-110">本主题说明如何为此类型的 ER 格式配置 ER 目标。</span><span class="sxs-lookup"><span data-stu-id="51438-110">This topic explains how to configure ER destinations for this type of ER format.</span></span>

## <a name="make-action-dependent-er-destinations-available"></a><span data-ttu-id="51438-111">让依赖操作的 ER 目标可用</span><span class="sxs-lookup"><span data-stu-id="51438-111">Make action-dependent ER destinations available</span></span>

<span data-ttu-id="51438-112">要在当前的 Finance 实例中配置依赖操作的 ER 目标，并启用 [新](er-apis-app10-0-17.md) ER API，打开 [功能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace)工作区，然后打开 **配置特定的 ER 目标以用于不同的 PM 操作** 功能。</span><span class="sxs-lookup"><span data-stu-id="51438-112">To configure action-dependent ER destinations in the current Finance instance and enable the [new](er-apis-app10-0-17.md) ER API, open the [Feature management](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace) workspace, and turn on the **Configure specific ER destinations to be used for different PM actions** feature.</span></span> <span data-ttu-id="51438-113">要在运行时将已配置的 ER 目标用于 [特定](#reports-list-wave1)报表，请启用功能 **根据特定于用户操作的 ER 目标路由 PM 报表的输出(第 1 波)**。</span><span class="sxs-lookup"><span data-stu-id="51438-113">To use configured ER destinations for [specific](#reports-list-wave1) reports at runtime, enable the feature, **Route output of PM reports based on ER destinations that are user action specific (wave 1)**.</span></span>

## <a name="configure-action-dependent-er-destinations"></a><span data-ttu-id="51438-114">配置依赖操作的 ER 目标</span><span class="sxs-lookup"><span data-stu-id="51438-114">Configure action-dependent ER destinations</span></span>

<span data-ttu-id="51438-115">打开 **配置特定的 ER 目标以用于不同的 PM 操作** 功能时，可以在 **电子报告目标** 页的 **文件目标** 快速选项卡上配置依赖操作的 ER 目标。</span><span class="sxs-lookup"><span data-stu-id="51438-115">When you turn on the **Configure specific ER destinations to be used for different PM actions** feature, you can configure action-dependent ER destinations on the **File destination** FastTab of the **Electronic reporting destination** page.</span></span> <span data-ttu-id="51438-116">对于每个组件，您可以添加记录并启用特定的 ER 目标。</span><span class="sxs-lookup"><span data-stu-id="51438-116">For each component, you can add a record and enable specific ER destinations.</span></span> <span data-ttu-id="51438-117">对于每个记录，您必须指定应该应用配置的 ER 目标的文档类型。</span><span class="sxs-lookup"><span data-stu-id="51438-117">For each record, you must specify the type of document that the configured ER destinations should be applied for.</span></span> <span data-ttu-id="51438-118">在 **文档类型** 字段中，选择以下值之一：</span><span class="sxs-lookup"><span data-stu-id="51438-118">In the **Document type** field, select one of the following values:</span></span>

- <span data-ttu-id="51438-119">如果在运行时未提供用户操作代码，则选择 **电子** 应用配置的目标。</span><span class="sxs-lookup"><span data-stu-id="51438-119">Select **Electronic** to apply the configured destinations if no user action code is provided at runtime.</span></span>
- <span data-ttu-id="51438-120">如果在运行时提供了用户操作代码，则选择 **打印管理** 应用配置的目标。</span><span class="sxs-lookup"><span data-stu-id="51438-120">Select **Print management** to apply the configured destinations if a user action code is provided at runtime.</span></span>
- <span data-ttu-id="51438-121">选择 **任何** 将始终应用配置的目标，不论在运行时是否提供了用户操作。</span><span class="sxs-lookup"><span data-stu-id="51438-121">Select **Any** to always apply the configured destinations, regardless of whether a user action is provided at runtime.</span></span>

<span data-ttu-id="51438-122">如果选择 **打印管理** 文档类型，则必须指定应该应用配置的 ER 目标的用户操作。</span><span class="sxs-lookup"><span data-stu-id="51438-122">If you select the **Print management** document type, you must specify the user actions that the configured ER destinations should be applied for.</span></span> <span data-ttu-id="51438-123">在 **打印管理操作** 字段中，选择以下值之一：</span><span class="sxs-lookup"><span data-stu-id="51438-123">In the **Print management action** field, select one of the following values:</span></span>

- <span data-ttu-id="51438-124">如果在运行时提供了 **查看** 用户操作，则选择 **查看** 应用配置的目标。</span><span class="sxs-lookup"><span data-stu-id="51438-124">Select **View** to apply the configured destinations if the **View** user action is provided at runtime.</span></span>
- <span data-ttu-id="51438-125">如果在运行时提供了 **打印** 用户操作，则选择 **打印** 应用配置的目标。</span><span class="sxs-lookup"><span data-stu-id="51438-125">Select **Print** to apply the configured destinations if the **Print** user action is provided at runtime.</span></span>
- <span data-ttu-id="51438-126">如果在运行时提供了 **发送** 用户操作，则选择 **发送** 应用配置的目标。</span><span class="sxs-lookup"><span data-stu-id="51438-126">Select **Send** to apply the configured destinations if the **Send** user action is provided at runtime.</span></span>

> [!NOTE]
> <span data-ttu-id="51438-127">可以为单个目标记录选择多个操作。</span><span class="sxs-lookup"><span data-stu-id="51438-127">Multiple actions can be selected for a single destination record.</span></span>

<span data-ttu-id="51438-128">如果选择 **任何** 文档类型，将在 **打印管理操作** 字段中自动选择 **自动检测** 作为用户操作，将发生以下行为：</span><span class="sxs-lookup"><span data-stu-id="51438-128">If you select the **Any** document type, **Autodetect** is automatically selected in the **Print management action** field as a user action, and the following behavior occurs:</span></span>

- <span data-ttu-id="51438-129">如果在运行时未提供用户操作代码，将应用所有配置的 ER 目标。</span><span class="sxs-lookup"><span data-stu-id="51438-129">If no user action code is provided at runtime, all configured ER destinations are applied.</span></span>
- <span data-ttu-id="51438-130">如果在运行时提供了用户操作代码，将应用为特定操作预定义的 ER 目标，**无论是否启用**：</span><span class="sxs-lookup"><span data-stu-id="51438-130">If a user action code is provided at runtime, an ER destination that is predefined for a specific action is applied, **regardless of whether it has been enabled**:</span></span>

    - <span data-ttu-id="51438-131">在运行时提供 **查看** 操作时，将应用 **屏幕** ER 目标。</span><span class="sxs-lookup"><span data-stu-id="51438-131">When the **View** action is provided at runtime, the **Screen** ER destination is applied.</span></span>
    - <span data-ttu-id="51438-132">在运行时提供 **发送** 操作时，将应用 **电子邮件** ER 目标。</span><span class="sxs-lookup"><span data-stu-id="51438-132">When the **Send** action is provided at runtime, the **Email** ER destination is applied.</span></span>
    - <span data-ttu-id="51438-133">在运行时提供 **打印** 操作时，将应用 **打印机** ER 目标。</span><span class="sxs-lookup"><span data-stu-id="51438-133">When the **Print** action is provided at runtime, the **Printer** ER destination is applied.</span></span>

<span data-ttu-id="51438-134">例如，您可以使用 **普通发票(Excel)** ER 格式在发布[普通发票](../../../finance/accounts-receivable/create-free-text-invoice-new.md)时打印该发票。</span><span class="sxs-lookup"><span data-stu-id="51438-134">For example, you can use the **Free text invoice (Excel)** ER format to print a [free text invoice](../../../finance/accounts-receivable/create-free-text-invoice-new.md) when you post it.</span></span> <span data-ttu-id="51438-135">要路由生成的文档，您必须为此 ER 格式配置 ER 目标。</span><span class="sxs-lookup"><span data-stu-id="51438-135">To route a generated document, you must configure ER destinations for this ER format.</span></span> <span data-ttu-id="51438-136">例如，您可能需要配置这些 ER 目标，才能对生成的文档执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="51438-136">For example, you may need to configure these ER destinations to perform the following on a generated document:</span></span>

- <span data-ttu-id="51438-137">如果运行 ER 格式但未提供操作代码（例如，以电子方式发送文档时），将文档存档。</span><span class="sxs-lookup"><span data-stu-id="51438-137">Archive the document if the ER format is run but no action code is provided (for example, when the document is sent electronically).</span></span>
- <span data-ttu-id="51438-138">当用户执行 **查看** 操作时，在 Web 浏览器中预览文档。</span><span class="sxs-lookup"><span data-stu-id="51438-138">Preview the document in a web browser when a user performs the **View** action.</span></span>
- <span data-ttu-id="51438-139">用户执行 **打印** 操作时，存档并打印文档。</span><span class="sxs-lookup"><span data-stu-id="51438-139">Archive and print the document when a user performs the **Print** action.</span></span>
- <span data-ttu-id="51438-140">用户执行 **发送** 操作时，存档文档，并将其作为出站电子邮件的附件通过电子邮件发送。</span><span class="sxs-lookup"><span data-stu-id="51438-140">Archive the document and email it as the attachment of an outbound email message when a user performs the **Send** action.</span></span>

<span data-ttu-id="51438-141">下图显示了在为单个用户操作配置了每个记录时，如何通过将 ER 目标配置为单个目标记录集来实现此目的：</span><span class="sxs-lookup"><span data-stu-id="51438-141">The following illustration shows how you can achieve this configuring ER destinations as the set of individual destination records when every record is configured for an individual user action:</span></span>

![为单个用户操作配置了每个目标记录时，具有针对 ER 格式的依赖操作的目标设置的电子报告目标页面](./media/er-destination-action-dependent-01.png)

<span data-ttu-id="51438-143">下图显示了在为单个目标配置了每个记录时，如何另外通过将 ER 目标配置为单个目标记录集来实现相同目的：</span><span class="sxs-lookup"><span data-stu-id="51438-143">The following illustration shows how you can achieve the same alternatively configuring ER destinations as the set of individual destination records when every record is configured for an individual destination:</span></span>

![为单个目标配置了每个目标记录时，具有针对 ER 格式的依赖操作的目标设置的电子报告目标页面](./media/er-destination-action-dependent-01a.png)

> [!NOTE]
> <span data-ttu-id="51438-145">如果为正在运行的 ER 格式提供了操作代码，但尚未为该操作代码配置目标，将应用[默认](electronic-reporting-destinations.md#default-behavior)目标行为。</span><span class="sxs-lookup"><span data-stu-id="51438-145">If an action code is provided for the running ER format, but no destinations have been configured for that action code, the [default](electronic-reporting-destinations.md#default-behavior) destination behavior is applied.</span></span>

## <a name="change-action-dependent-er-destinations-at-runtime"></a><span data-ttu-id="51438-146">在运行时更改依赖操作的 ER 目标</span><span class="sxs-lookup"><span data-stu-id="51438-146">Change action-dependent ER destinations at runtime</span></span>

<span data-ttu-id="51438-147">ER 格式运行时，如果用户操作已由具有适当[权限](electronic-reporting-destinations.md#security-considerations)可以在运行时更改配置的目标设置的用户设置，将出现一个对话框，提供更改已配置目标设置的选项。</span><span class="sxs-lookup"><span data-stu-id="51438-147">When an ER format is run, if user actions have been provisioned by users who have the appropriate [permissions](electronic-reporting-destinations.md#security-considerations) to change configured destination settings at runtime, a dialog box appears that gives the option to change the configured destination settings.</span></span> <span data-ttu-id="51438-148">此对话框是可选的，其外观取决于 ER 框架发起的运行 ER 格式的调用如何实现。</span><span class="sxs-lookup"><span data-stu-id="51438-148">This dialog box is optional, and its appearance depends on how the call that the ER framework makes to run an ER format has been implemented.</span></span> <span data-ttu-id="51438-149">如果出现此对话框，其中的 ER 目标将根据提供的用户操作启用。</span><span class="sxs-lookup"><span data-stu-id="51438-149">If this dialog box appears, the ER destinations in it will be enabled according to the user action that is provided.</span></span>

<span data-ttu-id="51438-150">下图显示了如果已设置 **打印机** 操作并为此格式配置了 ER 目标（如本主题前面所示），在 [发布](../../../finance/accounts-receivable/create-free-text-invoice-new.md)普通发票和运行 **普通发票(Excel)** ER 格式生成此文档时，出现的 **电子报告格式目标** 对话框的示例。</span><span class="sxs-lookup"><span data-stu-id="51438-150">The following illustration shows an example of the **Electronic reporting format destinations** dialog box that appears when a free text invoice is [posted](../../../finance/accounts-receivable/create-free-text-invoice-new.md) and the **Free text invoice (Excel)** ER format is run to generate this document, if the **Printer** action was provisioned and ER destinations were configured for this format as shown earlier in this topic.</span></span>

![提供更改为正在运行的 ER 格式初始配置的 ER 目标的选项的对话框](./media/er-destination-action-dependent-02.gif)

> [!NOTE]
> <span data-ttu-id="51438-152">如果您为正在运行的 ER 格式的多个组件配置了 ER 目标，将为每个已配置的 ER 格式组件单独提供一个选项。</span><span class="sxs-lookup"><span data-stu-id="51438-152">If you configured ER destinations for several components of the running ER format, an option will be offered separately for every configured component of the ER format.</span></span>

## <a name="verify-the-provided-user-action"></a><span data-ttu-id="51438-153">验证提供的用户操作</span><span class="sxs-lookup"><span data-stu-id="51438-153">Verify the provided user action</span></span>

<span data-ttu-id="51438-154">执行特定用户操作时，可以验证为正在运行的 ER 格式提供了哪些用户操作（如果有）。</span><span class="sxs-lookup"><span data-stu-id="51438-154">You can verify what user action, if any, is provided for the running ER format when you perform a specific user action.</span></span> <span data-ttu-id="51438-155">当您必须配置依赖操作的 ER 目标，但是您不确定提供了哪个用户操作代码（如果有）时，此验证很重要。</span><span class="sxs-lookup"><span data-stu-id="51438-155">This verification is important when you must configure action-dependent ER destinations, but you aren't sure which user action code, if any, is provided.</span></span> <span data-ttu-id="51438-156">例如，当您开始发布普通发票，并将 **发布普通发票** 对话框中的 **打印发票** 选项设置为 **是** 时，您可以将 **使用打印管理目标** 选项设置为 **是** 或 **否**。</span><span class="sxs-lookup"><span data-stu-id="51438-156">For example, when you start to post a free text invoice and set the **Print invoice** option to **Yes** in the **Post free text invoice** dialog box, you can set the **Use print management destination** option to **Yes** or **No**.</span></span>

<span data-ttu-id="51438-157">请按照下列步骤验证提供的用户操作代码。</span><span class="sxs-lookup"><span data-stu-id="51438-157">Follow these steps to verify the user action code that is provided.</span></span>

1. <span data-ttu-id="51438-158">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="51438-158">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="51438-159">在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。</span><span class="sxs-lookup"><span data-stu-id="51438-159">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="51438-160">在 **使用参数** 对话框中，将 **在调试模式下运行** 选项 [设置](er-trace-reports-compare-baseline.md#configure-er-parameters-to-use-the-baseline-feature)为 **是**。</span><span class="sxs-lookup"><span data-stu-id="51438-160">In the **User parameters** dialog box, [set](er-trace-reports-compare-baseline.md#configure-er-parameters-to-use-the-baseline-feature) the **Run in debug mode** option to **Yes**.</span></span>
4. <span data-ttu-id="51438-161">通过运行 ER 格式执行用户操作。</span><span class="sxs-lookup"><span data-stu-id="51438-161">Perform a user action by running an ER format.</span></span> <span data-ttu-id="51438-162">请记住，ER 用户参数是公司特定和用户特定参数。</span><span class="sxs-lookup"><span data-stu-id="51438-162">Remember that ER user parameters are company-specific and user-specific.</span></span>
5. <span data-ttu-id="51438-163">转到 **组织管理** \> **电子申报** \> **配置调试日志**。</span><span class="sxs-lookup"><span data-stu-id="51438-163">Go to **Organization administration** \> **Electronic reporting** \> **Configuration debug logs**.</span></span>
6. <span data-ttu-id="51438-164">在 **配置调试日志** 页上，筛选 ER 运行日志来查找您的 ER 格式运行的日志。</span><span class="sxs-lookup"><span data-stu-id="51438-164">On the **Configuration debug logs** page, filter the ER run logs to find the log for your ER format run.</span></span>
7. <span data-ttu-id="51438-165">如果为 ER 格式运行提供了任何操作，请查看必须包含呈现所提供的用户操作代码的记录的日志条目。</span><span class="sxs-lookup"><span data-stu-id="51438-165">Review the log entries that must contain the record that presents the provided user action code, if any action has been provided for the ER format run.</span></span>

    ![电子报告运行日志页，其中包含有关为筛选出的 ER 格式运行提供的用户操作代码的信息](./media/er-destination-action-dependent-03.png)

## <a name=""></a><span data-ttu-id="51438-167"><a name="reports-list-wave1">业务文档列表（第 1 波）</a></span><span class="sxs-lookup"><span data-stu-id="51438-167"><a name="reports-list-wave1">List of business documents (wave 1)</a></span></span>

<span data-ttu-id="51438-168">以下业务文档列表由功能 **根据特定于用户操作的 ER 目标路由 PM 报表的输出(第 1 波)** 控制：</span><span class="sxs-lookup"><span data-stu-id="51438-168">The following list of business documents are controlled by the feature, **Route output of PM reports based on ER destinations that are user action specific (wave 1)**:</span></span>

- <span data-ttu-id="51438-169">客户发票（普通发票）</span><span class="sxs-lookup"><span data-stu-id="51438-169">Customer invoice (Free text invoice)</span></span>
- <span data-ttu-id="51438-170">客户发票（销售发票）</span><span class="sxs-lookup"><span data-stu-id="51438-170">Customer invoice (Sales invoice)</span></span>
- <span data-ttu-id="51438-171">采购订单</span><span class="sxs-lookup"><span data-stu-id="51438-171">Purchase order</span></span>
- <span data-ttu-id="51438-172">采购订单采购查询</span><span class="sxs-lookup"><span data-stu-id="51438-172">Purchase order purchase inquiry</span></span>
- <span data-ttu-id="51438-173">销售订单确认</span><span class="sxs-lookup"><span data-stu-id="51438-173">Sales order confirmation</span></span>
- <span data-ttu-id="51438-174">催款单</span><span class="sxs-lookup"><span data-stu-id="51438-174">Collections letter note</span></span>
- <span data-ttu-id="51438-175">客户帐户对帐单</span><span class="sxs-lookup"><span data-stu-id="51438-175">Customer account statement</span></span>
- <span data-ttu-id="51438-176">利息单</span><span class="sxs-lookup"><span data-stu-id="51438-176">Interest note</span></span>
- <span data-ttu-id="51438-177">供应商付款通知</span><span class="sxs-lookup"><span data-stu-id="51438-177">Vendor payment advice</span></span>
- <span data-ttu-id="51438-178">询价</span><span class="sxs-lookup"><span data-stu-id="51438-178">Request for quotation</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51438-179">其他资源</span><span class="sxs-lookup"><span data-stu-id="51438-179">Additional resources</span></span>

[<span data-ttu-id="51438-180">电子报告 (ER) 概览</span><span class="sxs-lookup"><span data-stu-id="51438-180">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="51438-181">电子报告 (ER) 目标</span><span class="sxs-lookup"><span data-stu-id="51438-181">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)

[<span data-ttu-id="51438-182">针对 Application update 10.0.17 的电子报告框架 API 更改</span><span class="sxs-lookup"><span data-stu-id="51438-182">Electronic reporting framework API changes for Application update 10.0.17</span></span>](er-apis-app10-0-17.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]