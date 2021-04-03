---
title: 客户拥有资产维护工作的计费
description: 本主题说明如何创建、处理以及为完成的客户拥有资产维护工作计费。
author: johanhoffmann
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjInvoiceTable, ProjProjectsListPage, ProjTable, EntAssetWorkOrderType, EntAssetWorkOrderProjectSetup, EntAssetObjectTable, EntAssetWorkOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a93436d101e6201c9d86279ea5b1a37fcc644fd1
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500446"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a>客户拥有资产维护工作的计费

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]

*工作订单计费* 功能让您可以创建、处理和为完成的客户拥有资产维护工作计费。 此功能让您可以执行以下任务：

- 将客户连接到他们拥有的资产。
- 在创建工作订单时选择客户并查看该客户拥有的资产。
- 为每个客户设置父项目。
- 根据工作订单登记工时、物料、支出和费用，然后为客户创建发票方案。

此外，此功能还提供以下功能：

- 客户父项目的项目合同将自动复制到相关的工作订单项目。
- 资产管理现在可以在工作订单预测和工作订单日记帐上使用 *费用* 项目交易类型。

## <a name="turn-on-the-customer-billing-feature"></a>开启客户计费功能

此功能只有在系统中开启之后才能使用。 管理员可以使用[功能管理](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能。 在 **功能管理** 工作区中，此功能按照下面的方式列出：

- **模块**：*项目管理和会计*
- **功能名称**：*工作订单计费*

## <a name="example-scenario"></a>示例场景

若要了解此功能的工作原理，请完成以下示例场景。

若要使用此处指定的示例记录和值完成此场景，使用的系统中必须已安装标准[演示数据](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md)。 开始前，必须选择 **USMF** 法人。

使用生产系统时，也可以将此场景用作使用此功能的指导。 但是，在此情况下，必须替换为您自己的值，而您可能会缺少标准演示数据提供的某些类型的必需记录。

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a>步骤 1：为客户创建新的项目合同

1. 转到 **项目管理和会计 \> 项目 \> 项目合同**。
1. 在操作窗格上，选择 **新建**。
1. 在 **新建项目合同** 对话框中，设置以下值：

    - **名称**：*Pelican 批发*
    - **融资类型**：*客户*
    - **融资来源**：*US-013*（*Pelican 批发*）

1. 选择 **确定**。

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a>步骤 2：为客户创建新的父项目

您在此处创建的父项目将在为客户创建工作订单时使用。

1. 转到 **项目管理和会计 \> 项目 \> 所有项目**。
1. 在操作窗格上，选择 **新建**。
1. 在 **新建项目** 对话框中，设置以下值：

    - **项目类型**：*时间和材料*
    - **项目名称**：*Pelican 批发工作订单*
    - **项目组**：*TM*
    - **项目合同 ID**：*Pelican 批发*（您之前创建的合同）
    - **开始日期：** 选择今天的日期。

1. 选择 **创建项目**。
1. 新项目将打开。 记下 **项目 ID** 值。 您稍后必须输入此值。

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a>步骤 3：在资产管理中创建新的工作订单类型

1. 转到 **资产管理 \> 设置 \> 工作订单 \> 工作订单类型**。
1. 在操作窗格上，选择 **新建**。
1. 新记录将添加到列表中。 为它设置以下值：

    - **工作订单类型**：*服务*
    - **名称**：*服务工作订单*
    - **工作订单生命周期状态**：*标准*

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a>步骤 4：将客户帐户链接到父项目

现在，您必须在资产管理中的项目设置中将客户帐户链接到父项目。

1. 转到 **资产管理 \> 设置 \> 工作订单 \> 项目设置**。
1. 在 **父项目** 选项卡中，选择 **添加** 添加一行。
1. 在新行中，设置以下值：

    - **客户帐户**：*US-013* (*Pelican 批发*)
    - **项目 ID：** 输入您之前记下的项目 ID。

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a>步骤 5：将项目组和类型链接到工作订单项目

您应该仍然在 **项目设置** 页（**资产管理 \> 设置 \> 工作订单 \> 项目设置**）。

1. 在 **项目组** 选项卡中，选择 **添加** 添加一行。
1. 在新行中，设置以下值：

    - **工作订单类型**：*服务*（您之前创建的工作订单类型）
    - **项目组**：*TM*

> [!NOTE]
> 工作订单项目上的项目合同始终从父项目继承。

### <a name="step-6-link-an-asset-to-the-customer-id"></a>步骤 6：将资产链接到客户 ID

1. 转到 **资产管理 \> 资产 \> 有效资产**。
1. 在 **筛选器** 字段中，输入 *VE-102*，然后选择按 **资产** 筛选。
1. 选择资产以打开其设置。
1. 在 **客户** 快速选项卡上，将 **客户帐户** 字段设置为 *US-013* (*Pelican 批发*)。

    **名称** 字段将自动更新为 *Pelican 批发*。

### <a name="step-7-create-a-new-work-order-on-the-asset"></a>步骤 7：在资产上创建新工作订单

1. 转到 **资产管理 \> 工作订单 \> 有效工作订单**。
1. 在操作窗格上，选择 **新建**。
1. 在 **创建工作订单** 对话框中，设置以下值：

    - **工作订单类型**：*服务*
    - **描述**：*维修卡车*
    - **客户帐户**：*US-013* (*Pelican 批发*)
    - **资产**：*VE-102*

        > [!NOTE]
        > 查找仅显示链接到所选客户帐户的资产。

    - **维护作业类型**：*维修*
    - **贸易**：*机械*
    - **服务级别**：*4*

1. 选择 **确定**。

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a>步骤 8：查看工作订单并开始处理

在本节中，您将处理上一节中创建的工作订单。

1. 按照下列步骤验证父项目是否是 *Pelican 批发工作订单* 项目：

    1. 在 **工作订单维护作业** 部分，选择一行。
    1. 在 **行详细信息** 快速选项卡上，检查 **项目 ID** 值。 它应该是 *\<Parent-Project-ID\>-\<Project-ID\>* 形式的带连字符的数字。 此值是一个链接。
    1. 选择项目 ID 链接可以打开一个页面，您可以在其中查看父项目和项目名称。

1. 在操作窗格的 **工作订单** 选项卡上，在 **生命周期状态** 组中，选择 **更新工作订单状态**。
1. 在 **更新工作订单状态** 对话框中的 **选择** 列中，选中 **生命周期状态** 字段设置为 *进行中* 的行的复选框。
1. 选择 **确定**。
1. 在 **生命周期状态: 进行中** 对话框中，选择 **确定**。

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a>步骤 9：发布在工作订单上花费的工时并创建新发票方案

在本节中，您将继续处理在上一节中处理的工作订单。

1. 在操作窗格上，在 **工作订单** 选项卡的 **项目** 组中，选择 **日记帐**。

    **工作订单日记帐** 页将出现。 在这里，您可以登记您在工作订单上花费的时间。

1. 在 **工时** 快速选项卡中，选择 **添加行**。
1. 在新行上，将 **工时** 字段设置为 *4*。
1. 在操作窗格上，选择 **过帐日记帐**。
1. 关闭 **工作订单日记帐** 页以返回到工作订单。
1. 在操作窗格上的 **开票** 选项卡中，选择 **新建发票方案**。
1. 在 **创建发票方案** 对话框中的 **项目交易** 部分，为要开票的每一行选中 **选择** 复选框。
1. 选择 **确定** 关闭对话框，查看新发票方案。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]