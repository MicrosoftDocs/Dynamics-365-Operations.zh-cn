---
title: 开始使用电子开票附加产品
description: 本主题提供的信息将帮助您开始使用 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中的电子开票附加产品。
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
ms.openlocfilehash: 61933bb846383932d7dd73e9c4d3c2db7a515a98
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2020
ms.locfileid: "3835913"
---
# <a name="get-started-with-the-electronic-invoicing-add-on"></a>开始使用电子开票附加产品

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

本主题提供的信息将帮助您开始使用电子开票附加产品。 首先，它会指导您完成 Microsoft Dynamics Lifecycle Services (LCS)、Regulatory Configuration Services (RCS) 和 Dynamics 365 Finance 中的配置步骤。 然后，将介绍使用 Dynamics 365 Finance 或 Dynamics 365 Supply Chain Management 通过服务提交文档的流程。 您还会了解到如何解释提交日志。

## <a name="availability"></a>可用性

电子开票附加产品最初可在多个国家/地区使用。 此加载项支持创建电子发票和提交以下业务文档：

| 国家/地区  | 业务文档                          |
|-----------------|--------------------------------------------|
| 奥地利         | 销售和项目发票                 |
| 比利时         | 销售和项目发票                 |
| 巴西          | 电子会计单据模型 55 (NF-e) |
| 丹麦         | 销售和项目发票                 |
| 爱沙尼亚         | 销售和项目发票                 |
| 芬兰         | 销售和项目发票                 |
| 法国          | 销售和项目发票                 |
| 德国         | 销售和项目发票                 |
| 意大利           | 销售和项目发票                 |
| 墨西哥          | CFDI 发票                               |
| 荷兰     | 销售和项目发票                 |
| 挪威          | 销售和项目发票                 |
| 西班牙           | 销售和项目发票                 |
| 欧洲          | PEPPOL 销售和项目发票          |
    
## <a name="licensing"></a>许可授权

您可以通过当前许可证使用电子开票附加产品。 使用此服务不需要其他许可证。

## <a name="prerequisites"></a>先决条件

在完成本主题中的步骤之前，必须具备以下先决条件：

- 访问您的 LCS 帐户。
- 一个包含 Finance 或 Supply Chain Management 版本 10.0.12 或更高版本的 LCS 部署项目。
- 访问您的 RCS 帐户。
- 通过**功能管理**模块为您的 RCS 帐户启用全球化功能。 有关详细信息，请参阅 [Regulatory Configuration Services (RCS) - 全球化功能](rcs-globalization-feature.md)
- 在 Azure 中创建密钥保管库资源和存储帐户。 有关详细信息，请参阅[创建 Azure 存储帐户和密钥保管库](e-invoicing-create-azure-storage-account-key-vault.md)。

## <a name="overview"></a>概览

下图显示了您将在本主题中完成的五个主要步骤。

![本主题中五个步骤的概览](media/e-invoicing-services-get-started-overview-5-steps.png)

1. **Azure 资源设置：** 在 Azure 密钥保管库中配置 Azure 存储和数字证书的上载。
2. **LCS 设置：** 安装微服务加载项。
3. **RCS 设置：** 设置环境、用户访问权限和电子开票功能。
4. **客户端设置：** 设置客户端与电子开票附加产品之间的连接，关闭用于提交和接收电子文档响应的旧功能。
5. **提交发票：** 通过电子开票附加产品提交电子文档，并接收响应。

> [!NOTE]
> 本主题中的有些配置步骤是通用的，与国家/地区不相关。 国家/地区特定的步骤和设置过程在国家/地区特定主题中介绍。

## <a name="lcs-setup"></a>LCS 设置

1. 登录您的 LCS 帐户。
2. 选择 LCS 部署项目。 必须先设置并运行项目，您才能够选择项目。
3. 在**环境加载项**快速选项卡上，选择**安装新加载项**。
4. 选择**业务文档提交**。
5. 在**设置加载项**对话框的 **AAD 应用程序 ID** 字段中，输入 **091c98b0-a1c9-4b02-b62c-7753395ccabe**。 此值是一个固定值。
6. 在 **AAD 租户 ID** 字段中，输入您的 Azure 订阅帐户的 ID。

    ![LCS 中的“设置加载项”对话框](media/e-invoicing-services-get-started-lcs-addin-setup.png)

7. 选中复选框接受条款和条件。
8. 选择**安装**。

## <a name="rcs-setup"></a>RCS 设置

在 RCS 设置期间，您将完成以下任务：

1. 在 RCS 中设置密钥保管库。
2. 设置与电子开票附加产品服务器的 RCS 集成。
3. 为您的组织创建电子开票附加产品环境。

### <a name="set-up-the-key-vault-in-rcs"></a>在 RCS 中设置密钥保管库

1. 登录您的 RCS 帐户。
2. 在**全球化功能**工作区中，在**环境**部分，选择**电子开票**磁贴。
3. 选择**服务环境**。

    ![选择“服务环境”](media/e-invoicing-services-get-started-select-service-environments.png)

> [!NOTE]
> 选项**相连应用程序**授予通过 RCS 在 Finance 或 Supply Management 中自动配置电子开票附加产品的访问权限。 但是目前，此功能仍在开发中。

4. 在操作窗格中，选择**密钥保管库参数**。

    ![选择“密钥保管库参数”](media/e-invoicing-services-get-started-select-key-vault-parameters.png)

5. 在操作窗格中，选择**新建**添加密钥保管库。
6. 在**密钥保管库 URI** 字段中，输入您在 Azure 中配置的密钥保管库资源的 **DNS 名称**属性值。 有关在哪里可以找到 **DNS 名称**值的信息，请参阅[创建 Azure 存储帐户和密钥保管库](e-invoicing-create-azure-storage-account-key-vault.md)。

    ![“密钥保管库 URI”字段](media/e-invoicing-services-get-started-enter-key-vault-uri.png)

7. 在**证书**快速选项卡上，选择**添加**，然后输入数字证书名称和密钥保管库密码。 两组值都在 Azure 中的密钥保管库资源上配置。

    ![添加证书](media/e-invoicing-services-get-started-add-digital-certificates.png)

8. 如果您所在国家/地区的特定发票要求证书链应用数字签名，请在操作窗格中选择**证书链**，然后输入构成证书链的证书或密钥保管库密码的序列。

### <a name="set-up-the-rcs-integration-with-the-electronic-invoicing-add-on-server"></a>设置与电子开票附加产品服务器的 RCS 集成

1. 在**全球化功能**工作区的**相关链接**部分，选择**电子报告参数**链接。
2. 选择**单击此处连接到 Lifecycle Service**。 如果您不想连接到 LCS，请选择**取消**。
3. 在**电子开票附加产品**选项卡上，在**服务终结点 URI** 字段中，输入 `https://businessdocumentsubmission.us.operations365.dynamics.com/`。
4. 在**应用程序 ID** 字段中，验证其是否显示 ID **0cdb527f-a8d1-4bf8-9436-b352c68682b2**。 此值是一个固定值。
5. 在 **LCS 环境 ID** 字段中，输入您的 LCS 订阅帐户的 ID。

![输入电子开票附加产品参数](media/e-invoicing-services-get-started-enter-e-invoicing-parameters.png)

### <a name="add-an-electronic-invoicing-add-on-environment"></a>添加电子开票附加产品环境

您可以为电子开票附加产品创建不同的环境，如开发、测试或生产环境。

1. 在**全球化功能**工作区中，在**环境**部分，选择**电子开票**磁贴。
2. 选择**新建**创建一个环境。
3. 在**存储 SAS 令牌帐户**字段中，输入您在 RCS 中的密钥保管库中配置的密钥保管库密码的名称。

    ![“存储 SAS 令牌帐户”字段](media/e-invoicing-services-get-started-enter-sas-token-secret.png)

4. 在**用户**快速选项卡上，选择**新建**为此环境的用户授予访问权限。

    ![添加服务用户](media/e-invoicing-services-get-started-enter-service-users.png)

5. 在操作窗格上，选择**发布**将环境发布到电子开票附加产品服务器。

    ![“发布”按钮](media/e-invoicing-services-get-started-publish-service-environment.png)

### <a name="e-invoicing-feature-setup"></a>电子开票功能设置

“电子开票功能”是配置和发布以使用电子开票附加产品服务器的资源的通用名称。 电子开票功能的设置将使用电子报告 (ER) 配置格式来创建可配置的导出和导入文件，与使用操作和操作流来支持创建可配置规则以发送请求、导入响应和分析响应内容，以及另外一些设置相结合。

由于发票格式和操作流的变化，电子发票功能设置与国家/地区相关。

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>在 Finance 或 Supply Chain Management 中设置电子开票附加产品集成 

在此设置过程中，您将完成以下任务：

1. 打开外部测试版功能
2. 打开电子开票附加产品集成功能以启用与 Finance 的集成。
3. 设置电子开票附加产品终结点的 URL。
4. 导入与国家/地区特定的电子开票功能相关的 ER 配置。
5. 打开适用的国家/地区特定的电子开票功能。
6. 导入 ER 配置并设置作为提交流程的结果更新您的国家/地区特定发票文档所需的响应类型。

### <a name="open-flighted-feature"></a>打开外部测试版功能
电子开票集成功能通过外部测试启用。 外部测试是一个概念，默认情况下允许功能“打开”或“关闭”。 以下步骤在非生产环境中启用外部测试。 

1. 执行以下 SQL 命令：

    插入 SYSFLIGHTING（FLIGHTNAME，已启用）值（“BusinessDocumentSubmissionServiceEnabled”，1）
    
    插入 SYSFLIGHTING（FLIGHTNAME，已启用）值（“ElectronicInvoicingServiceIntegrationFeature”，1）
    
2. 进行上述更改后，在所有 AOS 上执行 IISReset

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>打开电子开票附加产品集成功能

1. 登录 Finance 或 Supply Chain Management。
2. 在**功能管理**工作区中，搜索新功能**可配置电子开票附加产品集成**。 如果“功能管理”页中还未显示此功能，请运行**检查更新**功能
3. 选择此功能，然后然后选择**立即启用**。

### <a name="set-up-the-service-endpoint-url"></a>设置服务终结点 URL

1. 转到**组织管理 \> 设置 \> 电子单据参数**。
2. 在**提交服务**选项卡上，在**服务终结点 URL** 字段中，输入 `https://businessdocumentsubmission.us.operations365.dynamics.com/`。
3. 在**环境**字段中，输入您在 RCS 设置过程中创建的电子开票附加产品环境的名称。

![输入服务参数](media/e-invoicing-services-get-started-enter-service-endpoint.png)

### <a name="import-the-er-configurations"></a>导入 ER 配置

为了能够收集业务数据并将其发送到电子开票附加产品，您必须导入与要使用的国家/地区特定电子开票功能相关的 ER 数据模型和 ER 数据模型配置。

1. 在**电子报告**工作区的**配置提供程序**部分，选择 **Microsoft** 磁贴。 确保此配置提供程序设置为**有效**。 有关如何将提供程序设置为**有效**的信息，请参阅[创建配置提供程序并将其标记为有效](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)。
3. 选择**存储库**。
4. 选择**全局资源**，然后选择**打开**。
5. 在**连接到 Lifecycle Services** 对话框中，选择**单击此处连接到 Lifecycle Service**。
6. 根据要使用电子开票功能的国家或地区，必须导入适用的数据模型、数据模型映射和格式。 有关您应导入的 ER 配置的信息，请参阅国家/地区特定的“开始使用电子开票附加产品”主题。
7. 导入**客户发票上下文模型**。 此模型包含其他参数，这些参数描述在提交业务数据期间 Finance 中用于电子开票附加产品的环境等信息。

### <a name="turn-on-countryregion-specific-e-invoicing-features"></a><a name="region-specific"></a>打开国家/地区特定的电子开票功能

要打开国家/地区特定的电子开票功能，让它们与电子开票附加产品一起使用，必须在要使用此功能的每个法人中打开此功能。 之后，将不再使用旧的电子开票集成，与新电子开票附加产品的集成将打开。

1. 转到**组织管理 \> 设置 \> 电子单据参数**。
2. 在**功能**选项卡上，在与您的国家/地区特定电子开票功能相关的功能的行中，选中**已启用**列中的复选框。 有关应打开哪个功能的信息，请参阅国家/地区特定的“开始使用电子开票附加产品”主题。

![打开电子开票功能](media/e-invoicing-services-get-started-enable-invoicing-feature.png)

> [!NOTE]
> 如果您有为不同国家或地区配置的多个法人，您可以为每个法人打开国家/地区特定的电子开票功能。

### <a name="import-er-configurations-and-set-up-the-response-types-to-update-your-countryregion-specific-invoice-document"></a>导入 ER 配置并设置响应类型以更新您的国家/地区特定的发票单据

如果在向政府授权服务提交响应后，提交的发票单据需要更新，必须导入特殊的 ER 数据模型和配置，以使发票单据或任何其他字段的状态得以更新。

1. 在**电子报告**工作区的**配置提供程序**部分，选择 **Microsoft** 磁贴。
2. 选择**存储库**。
3. 选择**全局资源**，然后选择**打开**。
4. 导入**响应消息模型**、**响应消息导入格式**、**映射到目标的响应消息模型**和**文件内容导入格式**。
5. 转到**组织管理 \> 设置 \> 电子单据参数**。
6. 在**电子单据**选项卡上，选择**添加**输入与您的国家/地区特定发票单据相关的表的名称。 有关应选择哪些表名称的信息，请参阅国家/地区特定的“开始使用电子开票附加产品”主题。
7. 选择**响应类型**配置响应类型。 有关应选择哪些表名称的信息，请参阅国家/地区特定的“开始使用电子开票附加产品”主题。

![设置响应类型](media/e-invoicing-services-get-started-set-up-response-types.png)

## <a name="e-invoicing-feature-names-by-country"></a>按国家/地区排列的电子开票功能名称 
下表描述了可从电子报告全局存储库下载以生成电子发票的其他电子开票功能。
在 RCS 中，您可以下载此表中列出的电子开票功能、ER 配置以及可用的电子开票功能设置。
在 Finance 中，您可以在**电子单据参数**页上启用相关功能引用，以为这些国家/地区开具电子发票。 有关详细信息，请参阅本主题前面的[打开国家/地区特定的电子开票功能](#region-specific)一节。

| 功能名称                      | 说明                                 | ER 配置                                                                                                  | 设置                                                                                                                                                         | 国家/地区  | 功能引用      |
|-----------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------|------------------------|
| 奥地利电子发票 (AT) | 奥地利的销售和项目发票      | - OIOUBL 销售发票 <br>- OIOUBL 项目发票 <br>- OIOUBL 销售贷方通知单 <br>- OIOUBL 项目贷方通知单 | - 销售发票生成 (AT) <br>- 项目发票生成 (AT) <br>- 销售贷方通知单生成 (AT) <br>- 项目贷方通知单生成 (AT)         | 奥地利         | EUR-00023              |
| 比利时电子发票 (BE)   | 比利时的销售和项目发票      | - UBL 销售发票 BE <br>- UBL 项目发票 BE <br>- UBL 项目贷方通知单 BE <br>- UBL 销售贷方通知单 BE | - 销售发票生成 (BE)<br>- 项目发票生成 (BE) <br>- 销售贷方通知单生成 (BE) <br>- 项目贷方通知单生成 (BE)         | 比利时         | EUR-00023              |
| 丹麦电子发票 (DK)    | 丹麦的销售和项目发票      | - OIOUBL 销售发票 <br>- OIOUBL 项目发票 <br>- OIOUBL 销售贷方通知单 <br>- OIOUBL 项目贷方通知单 | - 销售发票生成 (DK) <br>- 项目发票生成 (DK) <br>- 销售贷方通知单生成 (DK)<br>- 项目贷方通知单生成 (DK)         | 丹麦         | EUR-00023<br> DK-00001 |
| 荷兰电子发票 (NL)     | 荷兰的销售和项目发票  | - UBL 销售发票 NL <br>- UBL 项目发票 NL <br>- UBL 销售贷方通知单 NL <br>- UBL 项目贷方通知单 NL | - 销售发票生成 (NL) <br> - 项目发票生成 (NL) <br> - 销售贷方通知单生成 (NL) <br>- 项目贷方通知单生成 (NL)          | 荷兰 | EUR-00023              |
| 爱沙尼亚电子发票 (EE)  | 爱沙尼亚的销售和项目发票      | - 销售发票 (EE) <br> - 项目发票 (EE)                                                                     | - 销售发票生成 (EE) <br>- 项目发票生成 (EE)                                                                                           | 爱沙尼亚         | EUR-00023              |
| 芬兰电子发票 (FI)   | 芬兰的销售和项目发票      | - 销售发票 (FI) <br>- 项目发票生成 (FI)                                                          | - 销售发票生成 (FI) <br>- 项目发票生成 (FI)                                                                                           | 芬兰         | EUR-00023              |
| 法国电子发票 (FR)    | 法国的销售和项目发票    | - UBL 销售发票 FR <br> - UBL 项目发票 FR <br> - UBL 销售贷方通知单 FR <br>- UBL 项目贷方通知单 FR | - 销售发票生成 (FR) <br> - 项目发票生成 (FR) <br>- 销售贷方通知单生成 (FR) <br>- 项目贷方通知单生成 (FR)         | 法国          | EUR-00023              |
| 德国电子发票 (DE)    | 德国的销售和项目发票      |- 销售发票 (DE) <br> - 项目发票 <DE>                                                                     | - 销售发票生成 (DE) <br>- 项目发票生成 (DE)                                                                                           | 德国         | EUR-00023              |
| 挪威电子发票 (NO) | 挪威的销售和项目发票       | - OIOUBL 销售发票 <br>- OIOUBL 项目发票 <br>- OIOUBL 销售贷方通知单 <br>- OIOUBL 项目贷方通知单 | - 销售发票生成 (NO) <br>- 项目发票生成 (NO) <br>- 销售贷方通知单生成 (NO) <br>- 项目贷方通知单生成 (NO)          | 挪威          | EUR-00023<br> NO-00010 |
| 西班牙电子发票 (ES)   | 西班牙的销售和项目发票        | - 销售发票 (ES) <br>- 项目发票 (ES)                                                                     | - 销售发票生成 (ES) <br>- 项目发票生成 (ES)                                                                                           | 西班牙           | EUR-00023 <br>ES-00025 |
| 意大利电子发票 (IT)   | 意大利的销售和项目发票        | - （预览）销售发票 (IT) <br> - 项目发票 (IT)                                                           | - 销售发票 <br> - 项目发票                                                                                                                           | 意大利           | EUR-00023 <br>IT-00036 |
| PEPPOL 电子发票         | PEPPOL 销售和项目发票生成 | - PEPPOL 销售发票 <br>- PEPPOL 项目发票 <br>- PEPPOL 销售贷方通知单 <br> - PEPPOL 项目贷方通知单 | - PEPPOL 销售发票生成 <br>- PEPPOL 项目发票生成 <br>- PEPPOL 销售贷方通知单生成 <br>- PEPPOL 项目贷方通知单生成 |                 | EUR-00023              |


## <a name="electronic-invoice-processing-in-finance-and-supply-chain-management"></a>Finance 和 Supply Chain Management 中的电子发票处理

在处理期间，您将完成以下任务：

1. 通过电子开票附加产品提交业务文档（发票）。
2. 查看提交执行日志。

### <a name="submit-business-documents"></a>提交业务文档

在常规提交过程中，客户端与电子开票附加产品之间的通信是双向的。 目的是在提交电子单据时完成两项主要任务：

1. 发送所有正在等待从 Finance 提交的具有正确提交状态且符合选择条件的电子单据。
2. 将电子开票附加产品为先前提交的电子单据返回的响应导入到 Finance 中。 导入后，将分析响应，并相应地更新业务文档的状态。

您可以手动或根据计划要求提交业务文档。

1. 转到**组织管理 \> 定期 \> 电子单据 \> 提交电子单据**。
2. 对于任何文档的首次提交，请始终将**重新提交文档**选项设置为**否**。 如果必须通过服务重新提交文档，请将此选项设置为**是**。
3. 在**要包括的记录**快速选项卡上，选择**筛选**打开**查询**对话框，您可以在其中构建查询来选择要提交的文档。

![“提交电子单据”对话框](media/e-invoicing-services-get-started-submission-form.png)

### <a name="filter-query"></a>筛选器查询

1. 在**查询**对话框的**范围**选项卡上，使用**表**、**派生表**、**字段**和**条件**字段输入筛选条件。
2. 选择**添加**添加选择业务文档所需的任意数量的其他条件。

    ![设置提交筛选条件](media/e-invoicing-services-get-started-set-up-submission-filter-criteria.png)

3. 单击**确定**以关闭**查询**对话框。
4. 选择**确定**将选定的业务文档提交到电子开票附加产品。

    > [!NOTE]
    > 在首次尝试通过服务提交文档时，系统会提示您确认与电子开票附加产品的连接。 选择**单击此处连接到电子单据提交服务**。
    >
    > ![连接到“电子单据提交服务”消息框](media/e-invoicing-services-get-started-dialog-form-connect-e-Invoicing-services.png)
    >
    > 如果连接成功，您会收到确认消息。
    >
    > ![连接到电子开票附加产品的确认](media/e-invoicing-services-get-started-confirmation-connection-e-invoicing-services.png)

5. 关闭对话框。

> [!NOTE]
> 每次提交后，操作中心会显示已提交文档的数量。
>
> ![操作中心消息](media/e-invoicing-services-get-started-view-action-center-messages.png)

### <a name="submission-by-batch"></a>批量提交

您可以根据配置的批处理执行频率，自动执行提交流程并让它在后台运行，而不是手动提交文档。

1. 在**提交电子单据**对话框中，在**在后台运行**快速选项卡上，将**批处理**选项设置为**是**。
2. 在**定期**选项卡上，配置批处理频率。

![设置批量提交](media/e-invoicing-services-get-started-set-up-submission-batch.png)

### <a name="view-all-submission-logs"></a>查看所有提交日志

1. 转到**组织管理 \> 定期 \> 电子单据 \> 电子单据提交日志**。
2. 在**文档类型**字段中，选择要作为筛选依据的文档类型。

    ![选择要查看提交日志的文档类型](media/e-invoicing-services-get-started-select-document-type-for-viewing-submission-log.png)

    > [!IMPORTANT]
    > **提交状态**列中显示的值表示与提交流程本身的完成相关的状态。 指示在 RCS 中配置的操作流是否一直运行到最后，不论电子单据是被批准还是被拒绝。 **提交状态**列中的值不表示已提交文档的状态。 您可以在提交日志详细信息中的**处理操作日志**快速选项卡上查看已提交文档的状态（即文档是被批准还是被拒绝），如下文所述。

3. 在操作窗格上，选择**查询 \> 提交详细信息**。
4. 查看提交日志详细信息。

    ![提交日志详细信息](media/e-invoicing-services-get-started-view-submission-log-form.png)

提交日志中显示的结果取决于 RCS 中电子开票功能的设置。 但是，无论设置如何，提交日志始终有三个快速选项卡：

- **处理操作** – 此快速选项卡显示在 RCS 中设置的功能版本中配置的操作的执行日志。 **状态**列显示操作是否成功运行。
- **操作文件** – 此快速选项卡显示在执行操作期间生成的中间文件。 您可以选择**查看**下载文件和查看文件内容。
- **处理操作日志** – 此快速选项卡显示电子开票附加产品与目标 Web 服务之间的通信结果。 另外还显示 Web 服务处理返回的内容。

## <a name="related-topics"></a>相关主题

- [电子开票附加产品概述](e-invoicing-service-overview.md)
- [开始使用适用于巴西的电子开票附加产品](e-invoicing-bra-get-started.md)
- [开始使用适用于墨西哥的电子开票附加产品](e-invoicing-mex-get-started.md)
- [开始使用适用于意大利的电子开票附加产品](e-invoicing-ita-get-started.md)
- [设置电子开票附加产品](e-invoicing-setup.md)
