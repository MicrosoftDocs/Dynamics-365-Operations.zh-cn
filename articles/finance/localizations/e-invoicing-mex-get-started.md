---
title: 开始使用适用于墨西哥的电子开票
description: 本主题提供的信息将帮助您开始使用适用于墨西哥的电子开票。
author: gionoder
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 76c9f44dcc68b23058319cd317ba8426709fdca7
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2022
ms.locfileid: "7986350"
---
# <a name="get-started-with-electronic-invoicing-for-mexico"></a>开始使用适用于墨西哥的电子开票

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> 适用于墨西哥的电子开票当前可能不支持 Comprobante Fiscal Digital por Internet (CFDI) 单据以及 Microsoft Dynamics 365 Finance 或 Dynamics 365 Supply Chain Management 中内置的相关集成中提供的所有功能。

本主题提供的信息将帮助您开始使用适用于墨西哥的电子开票。 指导您完成 Regulatory Configuration Services (RCS) 和 Finance 中与国家/地区相关的配置步骤。 还将指导您完成 Finance 中通过服务提交 CFDI 发票所必须遵循的步骤，并说明如何查看处理结果和 CFDI 发票的状态。

## <a name="prerequisites"></a>先决条件

在完成本主题中的步骤之前，您必须完成[开始使用电子开票服务管理](e-invoicing-get-started-service-administration.md)和[开始使用电子开票](e-invoicing-get-started.md)中的步骤。

## <a name="set-up-the-cadena-xslt"></a>设置 Cadena XSLT

要将 Cadena XSLT 架构添加到 CFDI 处理全球化功能，请完成以下步骤。

1. 从 [SAT 网站](http://www.sat.gob.mx/sitio_internet/cfd/3/cadenaoriginal_3_3/cadenaoriginal_3_3.xslt)下载架构。
2. 将架构压缩到 ZIP 文件。
3. 将 xslt 文件保存到在服务环境中为新容器设置的 Azure 存储帐户。

## <a name="rcs-setup"></a>RCS 设置

在 RCS 设置期间，您将完成以下任务：

1. 导入电子开票功能来处理 CFDI 发票。
2. 查看生成、提交和接收有关 CFDI 发票的响应以及提交和接收有关取消的响应所需的格式配置。
3. 配置支持 CFDI 发票提交方案的事件。
4. 发布 CFDI 发票的电子开票功能。

> [!NOTE]
> “电子开票功能”是配置和发布以使用电子开票服务器的资源的通用名称。 在这种情况下，CFDI 发票 (MX) 是您将要设置的电子开票功能。

## <a name="import-the-e-invoicing-feature"></a>导入电子开票功能

1. 登录您的 RCS 帐户。
2. 在 **全球化功能** 工作区中，在 **功能** 部分，选择 **电子开票** 磁贴。
3. 在 **电子开票功能** 页上，选择 **导入** 从全局存储库中导入 **CFDI 发票 (MX)** 功能。

    > [!NOTE]
    > 如果您没有在列表中看到此功能，请选择 **同步**，然后重复步骤 3。

![导入 CFDI 发票 (MX) 功能。](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

从全局存储库导入 **CFDI 发票 (MX)** 能时，还将导入所有功能设置，包括配置和操作。

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a>创建新版本的 CFDI 发票 (MX) 功能

例如，如果必须更新 URL，您可以创建新版本。 有关详细信息，请参阅[电子开票 CFDI](tasks/mx-00010-e-invoicing-cfdi.md)。

- 在 **电子开票功能** 页上的 **版本** 选项卡上，选择 **新建**。

![添加新的电子开票功能版本。](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a>更新配置版本

1. 在 **电子开票功能** 页上的 **配置** 选项卡上，选择 **添加** 或 **删除** 管理配置版本（ER 文件格式配置）。

    ![管理电子开票功能配置。](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    创建新版本时，所有配置都将从上次发布的版本继承。 要处理 CFDI 发票，需要以下配置：

    - CFDI 发票 (BusinessDocumentService)
    - CFDI 响应消息导入
    - CFDI 错误日志导入
    - CFDI 取消请求 (MX) (BusinessDocumentService)
    - CFDI 发票 (BusinessDocumentService)

2. 在列表中，选择配置版本，然后选择 **编辑** 或 **查看** 打开 **格式设计器** 页，您可以在其中编辑或查看配置。

    ![打开“格式设计器”页面。](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. 使用 **格式设计器** 页编辑和查看 ER 格式文件配置。 有关详细信息，请参阅[创建电子单据配置](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration.md)。

    ![“格式设计器”页面。](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>管理电子开票功能设置

- 在 **电子开票功能** 页上的 **设置** 选项卡上，选择 **添加**、**删除** 或 **编辑** 管理电子开票功能设置。

![管理电子开票功能设置。](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

要提交 CFDI 发票进行授权（生成 XML 文件、提交 XML 文件和处理响应），需要 **销售发票** 功能设置。

要提交 CFDI 发票取消，需要 **取消** 和 **取消** 功能设置。

### <a name="configure-the-sales-invoice-feature-setup"></a>配置“销售发票”功能设置

1. 在 **电子开票功能** 页上的 **设置** 选项卡上，在 **功能设置** 列中，选择 **销售发票**。
2. 选择 **编辑** 配置操作、适用性规则和变量。

    ![编辑电子开票功能设置。](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. 在 **功能版本设置** 页上，选择 **操作** 选项卡管理操作列表。 操作定义必须按顺序运行以完成事件的完全执行的操作的列表。

    ![“操作”选项卡。](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | 行动 ID | 变动                   | 操作名称                                  | 操作描述                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | 1         | 转换文档       | 生成没有数字签名的 CFDI 电子发票 | 生成 CFDI 电子发票。                                |
    | 2         | 对文档签名            | 数字签名                                 | 对电子发票进行数字签名以进行提交。                |
    | 3         | 调用墨西哥 PAC 服务 | 提交 CFDI 电子发票                        | Windows Communication Foundation (WCF) 客户端提交 CFDI 电子发票。 |
    | 4         | 处理响应         | 分析 Web 服务响应                 | 分析 Web 服务响应，并返回错误日志。 |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a>为墨西哥 PAC Web 服务设置 URL 

1. 在 **功能版本设置** 页上的 **操作** 选项卡上，在 **操作** 快速选项卡上，选择 **调用墨西哥 PAC 服务**。
2. 在 **参数** 快速选项卡的 **URL 地址** 字段中，输入用于提交 CFDI 发票的 Web 服务的 URL。

> [!NOTE]
> 使用相同的步骤为 **取消** 和 **取消请求** 功能设置更新 **调用墨西哥 PAC 服务** 操作的 URL。

### <a name="set-up-the-path-for-the-cadena-xlst-schema"></a>设置 Cadena XLST 架构的路径

1. 在 **功能版本设置** 页上的 **变量** 选项卡上，选择变量名称 **DigitalSignatureXSLT**。
2. 在 **值** 字段中输入：{"containerUrl":"https://&lt;AccountStorageName&gt;.blob.core.windows.net/&lt;ContainerName&gt;","path":"&lt;RelativePath&gt;"}
   
    其中：<RelativePath> = folder\\folder\\filename，使用双反斜杠，ContainerName 必须表示用于服务的容器。
   
    变量示例将是这样：
    
    {"path":"xxxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx\\dev\\cadena_xslt","containerUrl":https://yyyyyyyyyy.blob.core.windows.net/containername}

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a>将草稿版本分配给电子开票环境

1. 在 **电子开票功能** 页上的 **环境** 选项卡上，选择 **启用**。
2. 在 **环境** 字段中，选择环境。
3. 在 **生效开始日期** 字段中，选择环境应该生效的日期。
3. 选择 **启用**。

![启用电子开票环境。](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a>将版本状态更改为“已完成”

1. 在 **电子开票功能** 页的 **版本** 选项卡上，选择状态为 **草稿** 的电子开票功能的版本。
2. 选择 **更改状态 \> 完成**。

## <a name="change-the-version-status-to-published"></a>将版本状态更改为“已发布”

- 在 **电子开票功能** 页上的 **版本** 选项卡上，选择 **更改状态 \> 发布**。

## <a name="publish-the-e-invoicing-feature"></a>发布电子开票功能

1. 在 **电子开票功能** 页上，选择 **版本** 选项卡管理 **CFDI 发票 (MX)** 功能的状态。
2. 选择 **更改状态** 更改功能的状态。

![更改电子开票功能的状态。](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing--integration-in-finance"></a>在 Finance 中设置电子开票集成

若要在 Finance 中设置电子开票，您将完成以下任务：

1. 导入 ER 数据模型、ER 数据模型映射以及 CFDI 发票所需的格式。
2. 配置更新 CFDI 发票的响应类型。 这些响应类型用于来自授权认证提供程序 (PAC) 服务器的响应。

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a>导入 CFDI 发票的 ER 数据模型、ER 数据模型映射和上下文配置

1. 登录 Finance。
2. 在 **电子报告** 工作区的 **配置提供程序** 部分，选择 **Microsoft** 标题。 确保此配置提供程序设置为 **有效**。 有关如何将提供程序设置为 **有效** 的信息，请参阅[创建配置提供程序并将其标记为有效](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)。
3. 选择 **存储库**。
4. 选择 **全局资源 \> 打开**。
5. 导入 **发票模型**、**发票模型映射**、**CFDI 发票格式 (MX)**、**CFDI 发票取消请求格式 (MX)** 和 **CFDI 发票取消格式 (MX)**。

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a>打开处理 CFDI 发票的功能

1. 转到 **组织管理 \> 设置 \> 电子单据参数**。
2. 在 **功能** 选项卡上，选中功能引用 **MX-00010** 和 **MX-00016** 的行中的 **启用** 复选框。

![打开处理 CFDI 发票的功能。](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a>导入 ER 配置并设置更新 CFDI 发票的响应类型

#### <a name="import-er-configurations"></a>导入 ER 配置

1. 在 **电子报告** 工作区的 **配置提供程序** 部分，选择 **Microsoft** 标题。
3. 选择 **存储库**。
4. 选择 **全局资源 \> 打开**。
5. 导入 **响应消息模型**、**CFDI 错误日志导入 (MX)** 和 **CFDI 响应消息导入 (MX)**。

#### <a name="set-up-the-response-types"></a>设置响应类型

1. 转到 **组织管理 \> 设置 \> 电子单据参数**。
2. 在 **电子单据** 选项卡上，选择 **添加**。
3. 输入客户发票日记帐，然后在 **表名称** 字段中，选择项目发票。
4. 为每个表定义一个相关的文档上下文：

    - 对于 **客户发票日记帐**，输入 **客户发票上下文**。
    - 对于 **项目发票**，输入 **项目发票上下文**。

4. 选择 **响应类型** 配置可以从电子开票返回并包含在客户发票日记帐或项目发票中的响应类型。
5. 选择 **新建**，然后在 **响应类型** 字段中选择 **Response**。
6. 在 **提交状态** 字段中，选择 **待处理**。
7. 在 **模型映射** 字段中，选择 **响应消息导入格式 – 来自响应消息的模型映射**。
8. 选择 **保存**。
9. 选择 **新建**，然后在 **响应类型** 字段中选择 **ResponseData**。
10. 在 **提交状态** 字段中，选择 **待处理**。
11. 在 **模型映射** 字段中，选择 **CFDI 响应数据导入格式(详细信息) – 响应数据导入**。
12. 选择 **保存**。

## <a name="process-electronic-invoices-in-finance"></a>在 Finance 中处理电子发票 

在通过电子开票在 Finance 中处理 CFDI 发票期间，您可以执行以下任务：

- 提交 CFDI 发票。
- 查看提交执行日志。
- 提交 CFDI 发票的取消。

### <a name="submit-cfdi-invoices"></a>提交 CFDI 发票

打开 **可配置电子开票集成** 功能后，将不再使用用于提交 CFDI 发票的 **导出/导入电子发票** 流程（**应收帐款 \> 发票 \> 电子发票**）。 取而代之的是一个名为 **提交电子单据** 的新流程。

> [!NOTE]
> 在使用新的 **提交电子单据** 流程前，请验证墨西哥电子发票所需的设置已完成。 有关详细信息，请参阅 [CFDI 布局版本 3.3](./latam-mex-cfdi-3-3.md)。

1. 转到 **组织管理 \> 定期 \> 电子单据 \> 提交电子单据**。
2. 对于任何文档的首次提交，请始终将 **重新提交文档** 选项设置为 **否**。 如果必须通过服务重新提交文档，请将此选项设置为 **是**。
3. 在 **要包括的记录** 快速选项卡上，选择 **筛选** 打开 **查询** 对话框，您可以在其中构建查询来选择要提交的文档。

![提交 CFDI 文档。](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> 在首次尝试通过服务提交单据时，系统会提示您确认与电子开票的连接。 选择 **单击此处连接到电子单据提交服务**。

### <a name="view-submission-logs"></a>查看提交日志

您可以查看所有已提交文档或仅一个已提交文档的提交日志。

#### <a name="view-all-submission-logs"></a>查看所有提交日志

打开 **可配置电子开票集成** 功能后，将出现一个新页面，可让您跟进单据提交流程。 您可以使用此页面查看所有已提交文档的提交日志。

1. 转到 **组织管理 \> 定期 \> 电子单据 \> 电子单据提交日志**。
2. 在 **文档类型** 字段中，选择 **客户发票日记帐** 筛选所需的电子单据。

    ![选择文档类型以查看提交日志。](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. 在操作窗格上，选择 **查询 \> 提交详细信息** 查看提交执行日志的详细信息。

    ![查看提交日志详细信息。](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

提交日志中的信息划分到三个快速选项卡：

- **处理操作** – 此快速选项卡显示在 RCS 中设置的功能版本中配置的操作的执行日志。 **状态** 列显示操作是否成功运行。
- **操作文件** – 此快速选项卡显示在执行操作期间生成的中间文件。 您可以选择 **查看** 下载和查看文件。
- **处理操作日志** – 此快速选项卡显示电子开票与目标 Web 服务之间的通信结果。 另外还显示 Web 服务的处理返回的内容。 **错误代码** 列显示授权 Web 服务返回的返回代码。

授权所提交的 CFDI 发票后，其状态将更新为 **已批准**。

#### <a name="view-submission-logs-from-cfdi-invoices"></a>查看 CFDI 发票的提交日志

打开 **可配置电子开票集成** 功能后，您还可以查看 CFDI 发票的提交日志。

1. 转到 **应收帐款 \> 查询与报表 \> CFDI（电子发票）**。
2. 选择打开 **可配置电子开票集成** 功能后提交的 CFDI 发票。
3. 在操作窗格上的 **历史记录** 选项卡中，选择 **电子单据日志**。

![查看 CFDI 发票的提交日志。](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> 对于在打开 **可配置电子开票集成** 功能之前提交的 CFDI 发票，**历史记录** 按钮可用。 对于在打开 **可配置电子开票集成** 功能之后提交的 CFDI 发票，**历史记录** 按钮不可用。

### <a name="submit-cancellation-of-cfdi-invoices"></a>提交 CFDI 发票的取消

打开 **可配置电子开票集成** 功能后，不再使用旧的取消 CFDI 发票流程。 取而代之的是嵌入在 **电子单据提交日志** 页上的新取消流程。

1. 转到 **应收帐款 \> 查询与报表 \> CFDI（电子发票）**。
2. 如果 CFDI 发票的状态为 **已批准**，选择 **功能 \> 取消 CFDI**。
3. 转到 **组织管理 \> 定期 \> 电子单据 \> 电子单据提交日志**。
4. 选择 CFDI 发票，然后选择 **功能 \> 发送相关提交**。
5. 为相关提交输入描述，然后选择 **确定**。

#### <a name="view-cancellation-submission-logs"></a>查看取消提交日志

1. 转到 **组织管理 \> 定期 \> 电子单据 \> 电子单据提交日志**。
2. 在 **文档类型** 字段中，选择 **客户发票日记帐** 仅筛选出客户发票日记帐单据。
3. 选择 CFDI 发票，然后在操作窗格上，选择 **查询 \> 相关提交**。

    **相关提交** 页显示给定 CFDI 发票的所有相关提交及其提交状态。 在下图中，第一行表示请求审批 CFDI 发票的提交。 第二行表示取消该 CFDI 发票的提交。

    ![查看取消提交日志。](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. 在操作窗格上，选择 **查询 \> 提交详细信息** 查看提交执行日志的详细信息。

    ![查看取消提交日志详细信息。](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a>隐私声明
启用 **CFDI 墨西哥电子发票 (MX)** 功能可能需要发送有限的数据，其中包括组织税务登记 ID。 这将被传输到税务机构授权的第三方机构，以便以与政府的 Web 服务集成所需的预定义格式向该税务机构发送电子发票。 管理员可以通过导航到 **组织管理 \> 设置 \> 电子单据参数** 来启用和禁用 **CFDI 墨西哥电子发票 (MX)** 功能。 选择 **功能** 选项卡，选择包含 **CFDI 墨西哥电子发票 (MX)** 功能的行，然后进行适当的选择。 从这些外部系统导入到此 Dynamics 365 在线服务的数据受我们的[隐私声明](https://go.microsoft.com/fwlink/?LinkId=512132)的约束。 有关详细信息，请查阅国家/地区特定功能文档中的“隐私声明”部分。

## <a name="additional-resources"></a>其他资源

- [电子开票概览](e-invoicing-service-overview.md)
- [开始使用电子开票](e-invoicing-get-started.md)
- [设置电子开票](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
