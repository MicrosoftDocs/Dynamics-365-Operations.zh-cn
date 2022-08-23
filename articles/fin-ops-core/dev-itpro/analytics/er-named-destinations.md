---
title: 配置打印管理记录特定的电子报告目标
description: 本文介绍如何为配置为生成出站文档的电子报告 (ER) 格式配置打印管理记录特定目标。
author: kfend
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: 10.0.21
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.form: ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: 7c92d580f6adebdba12b7964a42fd4752e9c9205
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285052"
---
# <a name="configure-print-management-record-specific-er-destinations"></a>配置打印管理记录特定的电子报告目标

[!include [banner](../includes/banner.md)]

本文说明系统管理员或应收帐款职员角色的用户如何执行以下任务：

- 为生成普通发票的 ER 解决方案配置指定的[电子报告 (ER)](general-electronic-reporting.md)。
- 将 ER 目标分配给单个[打印管理](document-reporting-services.md)记录。

这些过程可以在 USMF 公司中完成。 无需进行编码。

## <a name="introduction"></a>简介

您可以为用于生成出站文档的 ER [格式](general-electronic-reporting.md)[配置](general-electronic-reporting.md#Configuration)的文件输出组件中的每个文件夹[配置](electronic-reporting-destinations.md)目标。 运行这种类型的 ER 格式时，如果具有适当的访问权限，也可以在运行时更改配置的目标设置。

在 Microsoft Dynamics 365 Finance **版本 10.0.17 及更高版本** 中，可以为 ER 格式[设置](er-apis-app10-0-17.md)操作代码，以指定用户通过运行该 ER 格式执行的操作。 例如，在 **应收账款** 模块中，在打印管理设置中，您可以选择一个 ER 格式来生成特定的业务文档，如普通发票。 然后，您可以选择 **查看** 预览发票，或选择 **打印** 将其发送到打印机。 如果在运行时为正在运行的 ER 格式传递了操作，您可以[为不同的用户操作配置不同的 ER 目标](er-action-dependent-destinations.md)。

在 Finance **版本 10.0.21 及更高版本** 中，可以为 ER 格式[设置](er-apis-app10-0-21.md)指定的目标，并将此目标分配给运行该 ER 格式时处理的打印管理记录。 例如，在 **应收帐款** 模块的打印管理设置中，您需要配置 **原始** 记录以执行以下操作：

- 运行 ER 格式。
- 将生成的发票通过电子邮件发送给客户。
- 配置 **复制** 记录以运行相同的格式。
- 将发票副本打印到网络打印机。

在这种情况下，必须为正在运行的 ER 格式配置不同的 ER 目标，并且必须为不同的打印管理记录选择目标。

## <a name="prerequisites"></a>先决条件

在开始之前，必须在 [功能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace)工作区中打开 **允许设置每个打印管理项的 ER 目标** 功能。 还必须更改源代码以允许在当前 Finance 实例中配置指定的 ER 目标并启用[新](er-apis-app10-0-21.md) ER API。

此外，必须将 **普通发票 (Excel)** ER 配置[导入](er-download-configurations-global-repo.md)到您的 Finance 实例中。

## <a name="configure-a-new-er-destination"></a>配置新 ER 目标

1. 转至 **应收帐款** \> **发票** \> **所有普通发票**。
2. 选择客户帐户 **US-001** 的发票。
3. 在 **普通发票** 页面上的 **发票** 选项卡上，在 **打印管理** 组中，选择 **打印管理**。
4. 在 **打印管理设置** 页面上，展开 **模块 - 应收帐款** \> **文档** \> **普通发票**，选择 **原始** 记录，然后执行以下步骤：

    1.  遵守所选记录的当前设置：
        -   在 **报表格式** 字段中选择了默认 SSRS 报表 **FreeTextInvoice.Report**。
        -   **\<Default\>** 名称显示在 **目标** 字段中，通知未针对分配的 SSRS 报表选择自定义目标。 
    2.  在 **报表格式** 字段中，选择 **普通发票 (Excel)** ER 格式配置。
        -   **目标** 字段的名称已更改为 **目标名称**。
        -   **\<No named destination\>** 名称显示在 **目标名称** 字段中，通知未针对分配的 ER 格式选择指定目标。
    3.  选择 **目标名称** 字段右侧的箭头按钮。    
    4. 在 **电子报告指定目标** 页面上的 **名称** 字段中输入 **主目标**。
    5. 选择 **保存**。
    6. 在 **文件目标** 快速选项卡上，[配置](er-destination-type-email.md)**报表** 组件的 **电子邮件** 目标。
    7. 关闭 **电子报告指定目标** 页面。
    8. 在 **打印管理设置** 页面上的 **目标名称** 字段中，选择 **主目标** 指定目标。

    ![为所选 ER 格式配置指定的 ER 目标，并将其分配给“打印管理设置”页上配置的打印管理记录](./media/er-named-destinations-01.gif)

    您现在已为 **普通发票 (Excel)** 格式配置了指定的 ER 目标 **主目标**，并将其分配到了 **模块 - 应收帐款** \> **单据** \> **普通发票** 下的 **原始** 打印管理记录。

5. 展开 **模块 - 应收帐款** \>**帐户 - US-001** \>**普通发票**，选择 **原始** 记录，然后按照以下步骤操作：

    1. 选择并按住（或右键单击）此记录，然后选择 **替代**。
    2. 选择 **目标名称** 字段右侧的箭头按钮。
    3. 在 **电子报告指定目标** 页面的操作窗格上，选择 **新建**。
    4. 在 **名称** 字段中，输入 **US-001 目标**。
    5. 在 **文件目标** 快速选项卡上，[配置](er-destination-type-print.md)**报表** 组件的 **打印机** 目标。
    6. 关闭 **电子报告指定目标** 页面。
    7. 在 **打印管理设置** 页面上的 **目标名称** 字段中，选择 **US-001 目标** 指定目标。

    ![为所选 ER 格式配置指定的 ER 目标，并将其分配给“打印管理设置”页上配置的打印管理记录](./media/er-named-destinations-02.gif)

    您现在已为 **普通发票 (Excel)** 格式配置了指定的 ER 目标 **US-001 目标**，并将其分配到了 **模块 - 应收帐款** \> **帐户 - US-001** \> **普通发票** 下的 **原始** 打印管理记录。

现在，在处理普通发票时，将运行 **普通发票 (Excel)** ER 格式，并发生以下事件之一：

- 如果普通发票适用于 US-001 以外的客户，则生成的文档将通过电子邮件发送。
- 如果普通发票适用于客户 US-001，则将打印生成的文档。

> [!NOTE]
> 如果尚未为运行时处理的打印管理记录定义指定目标，则使用默认 ER 目标（如果它们可用于正在运行的 ER 格式）。

> [!IMPORTANT]
> 在 **电子报告目标** 页（**组织管理** \>**电子报告** \>**电子报告目标**）上，如果您选择为其配置了至少一个指定目标的 ER 格式，则会通知您是否存在指定的目标。
>
> ![有关在“电子报告目标”页上存在所选 ER 格式的已配置指定目标的通知](./media/er-named-destinations-03.png)
>
> 如果删除默认目标，也将删除所有指定的目标。 如果为打印管理记录选择了这些指定的目标，则将取消选择这些指定目标。

## <a name="copy-an-existing-er-destination-as-a-new-named-destination"></a>将现有 ER 目标复制为新的指定目标

当默认的指定 ER 目标可用于 ER 格式时，它可以用作新 ER 目标的模板。 若要创建基于默认目标的新 ER 目标，请在 **电子报告指定目标** 页上选择 **从默认值中复制**。 新目标名为 **默认**。 您可以根据需要多次重复此步骤。

您可以选择任何现有的指定目标作为新指定目标的模板。 若要创建基于选定的指定目标的新指定 ER 目标，请在 **电子报告指定目标** 页上选择 **复制**。 新目标的名称与所选指定目标的名称相同，但添加了后缀“副本”。 您可以根据需要多次重复此步骤。

## <a name="security-considerations"></a>安全考虑

仅当您有 [权限](../sysadmin/role-based-security.md#permissions)执行此任务时，才能在 **打印管理设置** 页面上设置指定的 ER 目标。 如果将 **配置电子报告格式目标**[责任](../sysadmin/role-based-security.md#duties)分配给您的一个[安全角色](../sysadmin/role-based-security.md#security-roles)，则可以向您授予权限。 有关详细信息，请参阅[安全性注意事项](electronic-reporting-destinations.md#security-considerations)。

## <a name="additional-resources"></a>其他资源

[电子报告 (ER) 概览](general-electronic-reporting.md)

[电子报告 (ER) 目标](electronic-reporting-destinations.md)

[针对 Application update 10.0.17 的电子报告框架 API 更改](er-apis-app10-0-17.md)

[针对 Application update 10.0.21 的电子报告框架 API 更改](er-apis-app10-0-21.md)

[更改代码以允许用户配置和使用指定的 ER 目标](er-api-named-destinations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
