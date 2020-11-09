---
title: 开始使用适用于意大利的电子开票附加产品
description: 本主题提供的信息将帮助您开始使用 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中适用于意大利电子开票附加产品的电子开票附加产品。
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c513141f820c95fe3842478361693701f1e3641b
ms.sourcegitcommit: d6250ee5ced43be39e789324a895fd1c07178935
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/19/2020
ms.locfileid: "4039784"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-italy"></a>开始使用适用于意大利的电子开票附加产品

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> 适用于意大利的电子开票附加产品当前可能不支持 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中可用于电子发票的所有功能。 

本主题提供的信息将帮助您开始使用适用于意大利的电子开票附加产品。 指导您完成 Regulatory Configuration Services (RCS) 和 Finance 中与国家/地区相关的配置步骤。 还会指导您完成通过服务提交以意大利特定的 **FatturaPA** 格式生成的电子发票的流程，并说明如何查看处理结果。

## <a name="prerequisites"></a>先决条件

在完成本主题中的步骤之前，您必须[开始使用电子开票附加产品](e-invoicing-get-started.md)中的步骤。

## <a name="rcs-setup"></a>RCS 设置

在 RCS 设置期间，您将完成以下任务：

1. 导入可以 **FatturaPA** 格式导出客户电子发票的电子开票功能。
2. 查看生成、提交和接收有关电子发票的响应所需的格式配置。
3. 配置支持电子发票提交方案的事件。
4. 发布电子开票功能。

> [!NOTE]
> “电子开票功能”是配置和发布以使用电子开票附加产品服务器的资源的通用名称。 在这种情况下，导出客户电子发票是您将要设置的电子开票功能。

## <a name="import-the-e-invoicing-feature"></a>导入电子开票功能

1. 登录您的 RCS 帐户。
2. 在 **全球化功能** 工作区中，在 **功能** 部分，选择 **电子开票** 磁贴。
3. 在 **电子开票功能** 页上，选择 **导入** 从全局存储库中导入电子开票功能。

    > [!NOTE]
    > 如果看不到可用功能列表，请选择 **同步** 。 

4. 选择 **电子发票导出 (IT)** 功能，然后选择 **导入** 。

![导入电子发票导出 (IT) 功能](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

从全局存储库导入 **电子发票导出 (IT)** 功能时，还将导入接下来几节中所述的所有设置。

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a>创建新版本的电子发票导出 (IT) 功能

1. 在 **电子开票功能** 页上的 **版本** 选项卡上，选择 **新建** 。 

    ![添加新的电子开票功能版本](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    接下来，您将配置与电子开票功能关联的电子报告 (ER) 格式。

2. 在 **配置** 选项卡上，选择 **添加** 管理配置版本。

    ![管理电子开票功能配置版本](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    在此步骤中，您将添加和配置用于导出意大利电子发票的不同文件的 ER 格式。 对于意大利 FatturaPA 电子发票，请使用以下标准配置或用于电子开票的实际的自定义配置：

    - 销售发票 (IT)
    - 项目发票 (IT)

    当您创建从另一个电子开票功能派生的电子开票功能时，所有 ER 格式都将从原始功能继承。

3. 选择特定的 ER 格式文件配置。
4. 选择 **编辑** 或 **查看** 打开 **格式设计器** 页。

    ![打开“格式设计器”页](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. 使用 **格式设计器** 页编辑和查看 ER 格式文件配置。

    ![“格式设计器”页面](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>管理电子开票功能设置

- 在 **电子开票功能** 页上的 **设置** 选项卡上，选择 **添加** 、 **删除** 或 **编辑** 管理电子开票功能设置。

![管理电子开票功能设置](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

在此步骤中，您将配置适用于电子发票的事件，包括生成 **FatturaPA** 格式的 XML 输出文件和数字签名（如果需要）。

### <a name="configure-the-sales-invoice-feature-setup"></a>配置“销售发票”功能设置

1. 在 **电子开票功能** 页上的 **设置** 选项卡上，在 **功能设置** 列中，选择 **销售发票** 。
2. 选择 **编辑** 。
3. 在 **功能版本设置** 页上，选择 **操作** 选项卡管理操作列表。 操作定义必须按顺序运行以完成事件的完全执行的操作的列表。

    ![“操作”选项卡](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | 行动 ID | 操作名称        | 操作描述                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | 1         | 转换文档 | 以 **FatturaPA** 格式创建电子发票 XML 文件。 |
    | 2         | 对文档签名      | 将数字签名应用于 XML 文件。             |

4. 选择 **适用性规则** 选项卡查看和维护适用性规则。 适用性规则定义操作将在其中运行的上下文。

    ![“适用性规则”选项卡](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. 选择 **变量** 选项卡查看和维护变量。

    ![“变量”选项卡](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. 定义运行操作所需的公共变量。

### <a name="configure-the-project-invoice-feature-setup"></a>配置“项目发票”功能设置 

配置 **项目发票** 功能设置所需的步骤和设置与 **销售发票** 功能设置的步骤和设置非常相似。 处理项目发票时，请参阅销售发票的过程。

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a>将电子开票功能分配到环境

1. 在 **电子开票功能** 页上的 **环境** 选项卡上，选择 **启用** 。
2. 在 **环境** 字段中，选择环境。
3. 在 **生效开始日期** 字段中，选择环境应该生效的日期。
4. 选择 **启用** 。 

![启用电子开票环境](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a>发布电子开票功能

您可以通过将版本状态更改为 **已完成** 或 **已发布** 来发布电子开票功能。

### <a name="change-the-version-status-to-completed"></a>将版本状态更改为“已完成”

1. 在 **电子开票功能** 页的 **版本** 选项卡上，选择状态为 **草稿** 的电子开票功能的版本。
2. 选择 **更改状态 \> 完成** 。 

### <a name="change-the-version-status-to-published"></a>将版本状态更改为“已发布” 

1. 在 **电子开票功能** 页的 **版本** 选项卡上，选择状态为 **已完成** 的电子开票功能的版本。
2. 选择 **更改状态 \> 发布** 。

![更改电子开票功能的状态](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance"></a>在 Finance 中设置电子开票附加产品集成

在 Finance 设置期间，您将完成以下任务：

1. 导入 FatturaPA 电子发票的 ER 数据模型、ER 数据模型映射和上下文配置。
2. 配置对意大利电子发票进行数字签名所需的证书。

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a>导入 ER 数据模型、数据模型映射和格式

1. 在 **电子报告** 工作区中，确认 **业务文档服务** 配置提供程序设置为 **活动** 。
2. 选择 **存储库** 。
3. 选择 **全局资源 \> 打开** 。
4. 导入 **发票模型** 、 **发票模型映射** 和 **客户发票上下文模型** 。

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a>打开导出意大利客户电子发票的功能

1. 转到 **组织管理 \> 设置 \> 电子单据参数** 。
2. 在 **功能** 选项卡上，选中功能引用 **IT00036** 的行中的 **已启用** 复选框。

![打开 FatturaPA 功能](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a>配置电子单据

1. 转到 **组织管理 \> 设置 \> 电子单据参数** 。
2. 在 **电子单据** 选项卡，选择 **添加** ，输入生成意大利电子发票所需的表：

    - **表名称：** 客户发票日记帐
    - **表名称：** 项目发票

3. 为每个表定义一个相关的文档上下文：

    - 对于 **客户发票日记帐** ，选择 **客户发票上下文** 。
    - 对于 **项目发票** ，选择 **项目发票上下文** 。

![设置响应类型](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a>电子发票处理

在 Finance 中进行处理期间，您将完成以下任务：

1. 通过电子开票附加产品生成意大利电子发票
2. 查看执行日志和处理结果

### <a name="generate-electronic-invoices"></a>生成电子发票

打开 **可配置电子开票附加产品集成** 功能并激活 **IT00036** 功能后，将不再使用生成意大利电子发票的旧 Finance 流程。 取而代之的是一个名为 **提交电子单据** 的新流程。

您可以根据对电子发票单据的要求手动提交单据。

> [!NOTE]
> 在继续之前，请验证意大利电子发票所需的设置已完成。 有关详细信息，请参阅[客户电子发票](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices)。 请注意，该主题中所述的某些设置步骤可能由于电子开票附加产品的激活不可用。

1. 转到 **组织管理 \> 定期 \> 电子单据 \> 提交电子单据** 。
2. 对于任何文档的首次提交，请将 **重新提交文档** 选项设置为 **否** 。 如果必须通过服务重新提交文档，请将此选项设置为 **是** 。
3. 在 **要包括的记录** 快速选项卡上，选择 **筛选** 打开 **查询** 对话框，您可以在其中构建查询来选择要提交的文档。

![“提交电子单据”对话框](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a>筛选器查询

1. 在 **查询** 对话框中，配置销售发票和项目发票的筛选条件，或将条件留空以包括所有未提交的发票。

    ![设置提交筛选条件](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. 单击 **确定** 以关闭 **查询** 对话框。
3. 选择 **确定** 提交所选文档。

> ![注意] 在首次尝试通过服务提交文档时，系统会提示您确认与电子开票附加产品的连接。 选择 **单击此处连接到电子单据提交服务** 。

#### <a name="view-submission-logs"></a>查看提交日志

您可以查看所有已提交文档的提交日志。

1. 转到 **组织管理 \> 定期 \> 电子单据 \> 电子单据提交日志** 。
2. 在 **文档类型** 字段中，选择 **客户发票日记帐** 或 **项目发票** 筛选所需的电子单据。

    ![选择文档类型以查看提交日志](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    **提交状态** 列中显示的值表示提交流程的状态。 指示流程是否按配置运行，以及是否需要其他操作。

3. 在操作窗格上，选择 **查询 \> 提交详细信息** 查看提交执行日志的详细信息。

    ![查看提交日志详细信息](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. 在 **处理操作** 快速选项卡上，您可以查看在 RCS 中设置的功能版本中配置的操作的执行日志。 **状态** 列显示操作是否成功运行。
5. 在 **操作文件** 快速选项卡上，您可以查看在执行操作期间生成的中间文件。 您可以选择 **查看** 以 **FatturaPA** 格式下载输出 XML 文件并查看其内容。

## <a name="related-topics"></a>相关主题

- [电子开票附加产品概述](e-invoicing-service-overview.md)
- [开始使用电子开票附加产品](e-invoicing-get-started.md)
- [设置电子开票附加产品](e-invoicing-setup.md)
