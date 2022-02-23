---
title: 开始使用适用于巴西的电子开票附加产品
description: 本主题提供的信息将帮助您开始使用 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中适用于巴西的电子开票附加产品。
author: gionoder
manager: AnnBe
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 0320bd1d9e93cc30ed75f28e387ac2ec8dbfc226
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4962826"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a>开始使用适用于巴西的电子开票附加产品 

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> 适用于巴西的电子开票附加产品当前不支持 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中内置的会计单据集成中提供的所有功能。

本主题提供的信息将帮助您开始使用适用于巴西的电子开票附加产品。 指导您完成 Regulatory Configuration Services (RCS) 以及 Finance 和 Supply Chain Management 中与国家/地区相关的配置步骤。 另外还指导您完成通过服务提交 NF-e 会计单据（电子会计单据模型 55）的流程，并说明如何查看处理结果和会计单据的状态。

## <a name="prerequisites"></a>先决条件

在完成本主题中的步骤之前，您必须[开始使用电子开票附加产品](e-invoicing-get-started.md)中的步骤。

## <a name="rcs-setup"></a>RCS 设置

在 RCS 设置期间，您将完成以下任务：

1. 导入 NF-e 会计单据的电子开票功能。
2. 查看提交 NF-e 会计单据以进行授权所需的文件格式。
3. 查看请求取消批准的 NF-e 所需的文件格式。
4. 配置提交 NF-e 会计单据以进行授权所需的事件。
5. 配置请求取消批准的 NF-e 所需的事件。
6. 将电子开票功能分配到电子开票附加产品环境。
7. 发布电子开票功能。

> [!NOTE]
> “电子开票功能”是配置和发布以使用电子开票附加产品服务器的资源的通用名称。 电子开票功能的设置将使用电子报告 (ER) 配置格式来创建可配置的导出和导入文件，与使用操作和操作流来支持创建可配置规则以发送请求、导入响应和分析响应内容，以及另外一些设置相结合。

## <a name="import-the-e-invoicing-feature"></a>导入电子开票功能

1. 登录您的 RCS 帐户
2. 在 **全球化功能** 工作区中，在 **功能** 部分，选择 **电子开票** 磁贴。
3. 在 **电子开票功能** 页上，选择 **导入** 从全局存储库中导入 NF-e 会计单据电子开票功能。

    ![“导入”按钮](media/e-Invoicing-services-get-started-BRA-Select-Import-e-Invoicing-feature.png)

4. 选择 NF-e 会计单据功能，然后选择 **导入**。

    ![导入 NF-e 功能](media/e-Invoicing-services-get-started-BRA-Select-Import-NF-e-feature.png)

### <a name="create-a-new-version-of-the-nf-e-fiscal-document-feature"></a>创建新版本的 NF-e 会计单据功能

- 在 **电子开票功能** 页上的 **版本** 选项卡上，选择 **新建**。

![添加新的电子开票功能版本](media/e-Invoicing-services-get-started-BRA-Select-New-e-Invoicing-feature-version.png)

### <a name="update-the-configuration-version"></a>更新配置版本

1. 在 **电子开票功能** 页上的 **配置** 选项卡上，选择 **添加** 或 **删除** 管理配置版本（ER 文件格式配置）。

    ![管理电子开票功能配置](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-configurations.png)

    - 当您创建新版本的 NF-e 会计单据功能时，所有配置版本（ER 文件格式）都将从最新版本继承。
    - 要提交 NF-e 会计单据以进行授权，需要以下配置版本：

        - NFe 提交导出格式
        - NFe 响应消息导入
        - NFe 错误日志导入

    - 要提交 NF-e 取消，需要以下配置版本：

        - NFe 取消导出格式

2. 在列表中，选择配置版本，然后选择 **编辑** 或 **查看** 打开 **格式设计器** 页，您可以在其中编辑或查看配置。

    ![打开“格式设计器”页](media/e-Invoicing-services-get-started-BRA-Configuration-ER-fomat-designer.png)

3. 使用 **格式设计器** 页编辑或查看 ER 格式文件配置。 有关详细信息，请参阅[创建电子单据配置](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration)。

    ![“格式设计器”页面](media/e-Invoicing-services-get-started-BRA-ER-Format-designer.png)

### <a name="manage-the-e-invoicing-feature-setups"></a>管理电子开票功能设置

- 在 **电子开票功能** 页上的 **设置** 选项卡上，选择 **添加** 或 **删除** 管理电子开票功能设置（即 NF-e 事件）。

![管理电子开票功能设置](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-setup.png)

当您创建从另一个电子开票功能派生的 NF-e 会计单据功能的新版本时，所有功能设置（NF-e 事件）均从最新版本继承。

要提交 NF-e 会计单据以进行授权，需要进行 **提交** 功能设置。

要提交 NF-e 取消，需要进行 **取消** 功能设置。

#### <a name="configure-the-submit-feature-setup"></a>配置“提交”功能设置

1. 在 **电子开票功能** 页上的 **设置** 选项卡上，在 **功能设置** 列中，选择 **提交**。
2. 选择 **编辑**。

    ![编辑电子开票功能设置](media/e-Invoicing-services-get-started-BRA-Edit-e-Invoicing-feature-setup.png)

3. 在 **功能版本设置** 页上，选择 **操作** 选项卡管理操作列表。

    ![“操作”选项卡](media/e-Invoicing-services-get-started-BRA-Select-Actions.png)

4. 查看提交 NF-e 进行授权所需的操作。

    | 行动 ID | 操作名称                  | 操作描述                                                |
    |-----------|------------------------------|-------------------------------------------------------------------|
    | 1         | 转换文档           | 创建要提交的 NF-e XML 文件。                          |
    | 2         | 对文档签名                | 将数字证书应用于 XML 文件。                    |
    | 3         | 调用巴西 SEFAZ 服务 | 将签名的 XML 文件提交到 Web 服务以进行授权。 |
    | 4         | 处理响应             | 获取 Web 服务响应。                                     |
    | 5         | 转换文档           | 分析作为响应接收的文件的内容。     |
    | 6         | 转换文档           | 创建 XML 文件来查询提交的状态。    |
    | 7         | 调用巴西 SEFAZ 服务 | 提交请求提交状态的 XML 文件。          |
    | 8         | 处理响应             | 获取 Web 服务响应。                                     |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>为 SEFAZ Web 服务设置 URL 

1. 在 **功能版本设置** 页上的 **操作** 选项卡上，在 **操作** 快速选项卡上，选择 **调用巴西 SEFAZ 服务**（操作 ID **3**）。
2. 在 **参数** 快速选项卡的 **URL 地址参数** 字段中，输入用于 NF-e 提交的 SEFAZ Web 服务的 URL。
3. 在 **操作** 快速选项卡上，选择 **调用巴西 SEFAZ 服务**（操作 ID **7**）。
4. 在 **参数** 快速选项卡的 **URL 地址参数** 字段中，输入用于 NF-e 提交的 SEFAZ Web 服务的 URL。

#### <a name="configure-the-cancellation-feature-setup"></a>配置“取消”功能设置

1. 在 **电子开票功能** 页上的 **设置** 选项卡上，在 **功能设置** 列中，选择 **取消**。
2. 选择 **编辑**。
3. 在 **功能版本设置** 页上，选择 **操作** 选项卡管理操作列表。
4. 查看请求取消批准的 NF-e 所需的操作。

    | 行动 ID | 操作名称                  | 操作描述                                               |
    |-----------|------------------------------|------------------------------------------------------------------|
    | 1         | 转换文档           | 创建要提交的 NF-e 取消 XML 文件。            |
    | 2         | 对文档签名                | 将数字证书应用于 XML 文件。                   |
    | 3         | 调用巴西 SEFAZ 服务 | 将签名的 XML 文件提交到 Web 服务以取消。 |
    | 4         | 处理响应             | 获取 Web 服务响应。                                    |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>为 SEFAZ Web 服务设置 URL

1. 在 **功能版本设置** 页上的 **操作** 选项卡上，在 **操作** 快速选项卡上，选择 **调用巴西 SEFAZ 服务**（操作 ID **3**）。
2. 在 **参数** 快速选项卡的 **URL 地址参数** 字段中，输入用于取消批准的 NF-e 的 SEFAZ Web 服务的 URL。

### <a name="make-an-e-invoicing-environment-available-and-assign-a-draft-version"></a>使电子开票环境可用和分配草稿版本

1. 在 **电子开票功能** 页上的 **环境** 选项卡上，选择 **启用**。
2. 在 **环境** 字段中，选择环境。
3. 在 **生效开始日期** 字段中，选择环境应该生效的日期。
4. 选择 **启用**。

![启用电子开票环境](media/e-Invoicing-services-get-started-BRA-Enable-e-Invoicing-environment.png)

### <a name="change-the-status-to-completed"></a>将状态更改为“已完成”

1. 在 **电子开票功能** 页的 **版本** 选项卡上，选择状态为 **草稿** 的电子开票功能的版本。
2. 选择 **更改状态 \> 完成**。

### <a name="change-the-status-to-publish"></a>将状态更改为“发布”

1. 在 **电子开票功能** 页的 **版本** 选项卡上，选择状态为 **已完成** 的电子开票功能的版本。
2. 选择 **更改状态 \> 发布**。

![发布电子开票功能](media/e-Invoicing-services-get-started-BRA-Publish-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>在 Finance 或 Supply Chain Management 中设置电子开票附加产品集成

在设置期间，您将完成以下任务：

1. 打开适用于巴西的 NF-e 联邦功能。
2. 导入特定的 ER 数据模型、数据模型映射以及 NF-e 会计单据所需的格式。
3. 导入 ER 配置，并设置返回提交流程后更新会计单据的状态所需的响应类型。

### <a name="turn-on-the-nf-e-federal-feature-for-brazil"></a>打开适用于巴西的 NF-e 联邦功能

1. 转到 **组织管理 \> 设置 \> 电子单据参数**。
2. 在 **功能** 选项卡上，选中功能引用 **BR00053** 的行中的 **启用** 复选框。

### <a name="import-the-er-data-model-mapping-required-for-nf-e-fiscal-documents"></a>导入 NF-e 会计单据所需的 ER 数据模型映射

1. 登录 Finance。
2. 在 **电子报告** 工作区的 **配置提供程序** 部分，选择 **Microsoft** 磁贴。 确保此配置提供程序设置为 **有效**。 有关如何将提供程序设置为 **有效** 的信息，请参阅[创建配置提供程序并将其标记为有效](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)。
3. 选择 **存储库**。
4. 选择 **全局资源 \> 打开**。
5. 导入 **会计单据映射** 配置。

### <a name="import-er-configurations-and-set-up-the-response-types-for-fiscal-documents"></a>导入 ER 配置并设置会计单据的响应类型

1. 在 **电子报告** 工作区的 **配置提供程序** 部分，选择 **Microsoft** 磁贴。
2. 选择 **存储库**。
3. 选择 **全局资源 \> 打开**。
4. 导入 **NF-e 错误日志导入 (BR)**、**NF-e 响应数据导入格式 (BR)** 和 **NF-e 响应消息导入 (BR)**。
5. 转到 **组织管理 \> 设置 \> 电子单据参数**。
6. 在 **电子单据** 选项卡上，选择 **添加**。
6. 在 **表名称** 字段中，输入 **会计单据标题**。
7. 在 **单据上下文** 字段中，选择 **客户发票上下文模型 – 会计单据上下文**。
8. 选择 **响应类型**。
9. 选择 **新建**，然后在 **响应类型** 字段中选择 **Response**。
10. 在 **提交状态** 字段中，选择 **待处理**。
11. 在 **模型映射** 字段中，选择 **响应消息导入格式 – 来自响应消息的模型映射**。
12. 选择 **保存**。
13. 选择 **新建**，然后在 **响应类型** 字段中输入 **ResponseData**。
14. 在 **提交状态** 字段中，选择 **待处理**。
15. 在 **模型映射** 字段中，选择 **NFe 响应数据导入格式 – 响应数据导入**。
16. 选择 **保存**。

## <a name="electronic-invoice-processing"></a>电子发票处理

在 Finance 中进行处理期间，您将完成以下任务：

1. 通过电子开票附加产品提交会计单据。
2. 查看提交执行日志和处理结果。
3. 通过电子开票附加产品提交会计单据的取消。

### <a name="submit-nf-e-fiscal-documents-for-sefaz-authorization"></a>提交 NF-e 会计单据以进行 SEFAZ 授权 

打开 **可配置电子开票附加产品集成** 功能后，将不再使用提交 NF-e 会计单据进行授权的旧流程（**导出/导入 NF-e 流程**）。 取而代之的是一个名为 **提交电子单据** 的新流程。

> [!NOTE]
> 在继续之前，请确保您有由客户的财务设施签发的一个或多个客户会计单据模型 55。 这些会计单据的方向必须设置为 **传出**，状态必须为 **已创建**。 有关详细信息，请参阅[签发客户会计单据（巴西）](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document)。

1. 转到 **组织管理 \> 定期 \> 电子单据 \> 提交电子单据**。
2. 对于任何文档的首次提交，请始终将 **重新提交文档** 选项设置为 **否**。 如果必须通过服务重新提交文档，请将此选项设置为 **是**。
3. 在 **要包括的记录** 快速选项卡上，选择 **筛选** 打开 **查询** 对话框，您可以在其中构建查询来选择要提交的文档。
4. 在 **范围** 选项卡上，选择 **添加**。
5. 在 **表** 字段中，选择 **会计单据标题**。
6. 在 **派生表** 字段中，选择 **会计单据标题**。
6. 在 **字段** 字段中，选择 **编号**。
7. 在 **条件** 字段中，输入应提交的会计单据的编号。
8. 单击 **确定** 以关闭 **查询** 对话框。
8. 选择 **确定** 提交所选文档。

> [!NOTE]
> 在首次尝试通过服务提交文档时，系统会提示您确认与电子开票附加产品的连接。 选择 **单击此处连接到电子单据提交服务**。

### <a name="view-all-submission-logs"></a>查看所有提交日志

打开 **可配置电子开票附加产品集成** 功能后，将出现一个新页面，可让您跟进文档提交过程。 您可以使用此页面查看所有已提交文档的提交日志。

1. 转到 **组织管理 \> 定期 \> 电子单据 \> 电子单据提交日志**。
2. 在 **文档类型** 字段中，选择 **会计单据标题** 仅筛选出会计单据。
3. 在操作窗格上，选择 **查询 \> 提交详细信息** 查看提交执行日志的详细信息。

![查看提交日志详细信息](media/e-Invoicing-services-get-started-BRA-View-Submission-log-details.png)

> [!NOTE] 
> 对于 NF-e 会计单据，**错误代码** 列显示 SEFAZ Web 服务返回的返回代码。

### <a name="view-submission-logs-through-the-fiscal-document-page"></a>通过会计单据页查看提交日志

打开 **可配置电子开票附加产品集成** 功能后，您还可以通过会计单据页查看提交日志。

1. 转到 **总帐 \> 查询和报表 \> 会计单据 \> 所有会计单据**。
2. 选择以前通过电子开票附加产品提交的会计单据。
3. 在操作窗格上的 **NF-e 联邦** 选项卡中，选择 **电子单据日志**。

![从会计单据页查看提交日志](media/e-Invoicing-services-get-started-BRA-View-Submission-log-from-Fiscal-document-viewer.png)

### <a name="submit-approved-nf-e-fiscal-documents-for-sefaz-cancellation"></a>提交批准的 NF-e 会计单据以取消 SEFAZ

打开 **可配置电子开票附加产品集成** 功能后，不能再使用旧的取消 NF-e 会计单据的流程。 取而代之的是嵌入在 **电子单据提交日志** 页上的新取消流程。

> [!NOTE]
> 确保已为批准的 NF-e 会计单据运行了客户会计单据取消。 有关详细信息，请参阅[取消客户会计单据（巴西）](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents)。

1. 转到 **组织管理 \> 定期 \> 电子单据 \> 电子单据提交日志**。
2. 选择会计单据，然后选择 **功能 \> 发送相关提交**。
3. 为相关提交输入描述，然后选择 **确定**。

### <a name="view-cancellation-submission-logs"></a>查看取消提交日志

1. 转到 **组织管理 \> 定期 \> 电子单据 \> 电子单据提交日志**。
2. 在 **文档类型** 字段中，选择 **会计单据标题** 仅筛选出会计单据。
3. 选择会计单据，然后在操作窗格上，选择 **查询 \> 相关提交**。

    相关提交是与首先进行的主要提交相关的提交。 例如，授权特定 NF-e 的提交是主要提交。 请求取消 SEFAZ 中同一个 NF-e 的提交是相关提交。 此提交之所以存在，只是因为它要请求取消通过另一个提交执行的作业。

    **相关提交** 页显示给定会计单据的所有相关提交及其提交状态。 在下图中，第一行表示请求审批会计单据的提交。 第二行表示取消该会计单据的提交。

    ![查看取消提交日志](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log.png)

4. 在操作窗格上，选择 **查询 \> 提交详细信息** 查看提交执行日志的详细信息。

    ![查看取消提交日志详细信息](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log-details.png)

## <a name="privacy-notice"></a>隐私声明
启用 BR-00053（NF-e 联邦）功能可能需要发送有限的数据，其中包括组织税务登记 ID。 这将被传输到税务机构授权的第三方机构，以便以与政府的 Web 服务集成所需的预定义格式向该税务机构发送电子发票。 管理员可以通过导航到 **组织管理 \> 设置 \> 电子单据参数** 来启用和禁用 BR-00053（NF-e 联邦）功能。 选择 **功能** 选项卡，选择包含 BR-00053 功能的行，然后进行适当的选择。 从这些外部系统导入到此 Dynamics 365 在线服务的数据受我们的[隐私声明](https://go.microsoft.com/fwlink/?LinkId=512132)的约束。 有关详细信息，请查阅国家/地区特定功能文档中的“隐私声明”部分。


## <a name="additional-resources"></a>其他资源

- [电子开票附加产品概述](e-invoicing-service-overview.md)
- [开始使用电子开票附加产品](e-invoicing-get-started.md)
- [设置电子开票附加产品](e-invoicing-setup.md)
