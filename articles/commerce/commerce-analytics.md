---
title: Commerce 分析（预览版）
description: 本主题介绍如何安装和使用 Microsoft Dynamics 365 Commerce 中的分析功能。
author: AamirAllaq
ms.date: 11/23/2021
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 8cfe2af756315b5be3eb22d99376a96166fffc52
ms.sourcegitcommit: f9fca3d55b47e615e5ef64669dab184e057ec234
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/23/2021
ms.locfileid: "7862765"
---
# <a name="commerce-analytics-preview"></a>Commerce 分析（预览版）

[!include [banner](includes/banner.md)]

本主题介绍如何安装 Commerce 分析（预览版）功能，这是 Microsoft Dynamics 365 Commerce 中包含的功能性分析功能。

## <a name="commerce-analytics-preview-live-demo"></a>Commerce 分析（预览版）实时演示

您可以试用 [Commerce 分析（预览版）实时演示](https://aka.ms/CommerceAnalyticsDemo)。

![Commerce 分析（预览版）摘要](media/CommerceAnalytics_Summary.png)
![Commerce 分析（预览版）付款](media/CommerceAnalytics_Payments.png)
![Commerce 分析（预览版）Web 活动](media/CommerceAnalytics_WebActivity.png)


## <a name="commerce-analytics-preview-system-architecture"></a>Commerce 分析（预览版）系统体系结构

### <a name="key-components"></a>重要组件

Commerce 分析（预览版）由以下关键组件组成：

- 随时可用的交互式 Power BI 报表
- Azure Synapse 分析中的 SQL 视图
- Azure Data Lake 中的实体和本体数据
- Data Lake 中的原始数据

![Commerce 分析系统体系结构的关键组件](media/CommerceAnalyticsArchitecture_v2.png)

### <a name="data-flow"></a>数据流

#### <a name="step-1-data-generation"></a>步骤 1：数据生成

数据源自以下来源之一的交易数据或行为数据：

- 呼叫中心助理使用 Commerce HQ 客户端处理销售订单。
- 销售点 (POS) 的出纳将处理销售交易记录。
- 销售额是通过使用无头 Commerce（Commerce Scale Unit）在自定义应用程序中创建的。
- 电子商务购物者将浏览您的电子商务网站。
- 电子商务购物者将在您的电子商务网站上下达订单。
- 数据由诸如 Dynamics 365 Connected Spaces 之类的其他系统生成。

#### <a name="step-2-ingestion-and-pre-processing"></a>第 2 步：引入和预处理

交易数据直接（如果直接在 Commerce HQ 客户端中获取订单）或通过 Commerce Scale Unit（如果在 POS、在电子商务网站或在使用无头 Commerce 的自定义客户端中获取订单）发送到 Commerce HQ。

然后，“导出到 Data Lake”功能用于将交易记录数据复制到您的 Data Lake 中作为原始数据。 在 Data Lake 中，原始数据存储在表文件夹中。

电子商务 Web 活动数据将直接发送到 Data Lake。 其他系统（例如 Dynamics 365 Connected Spaces）生成的数据由这些系统直接发送到 Data Lake。

#### <a name="step-3-transformation-and-aggregation"></a>步骤 3：转换和聚合

在 Data Lake 中存在原始数据后，Commerce 分析服务会读取它，对其进行转换，进行聚合，然后以逻辑实体（在“实体”文件夹中）和聚合度量（在“本体”文件夹中）的形式将其写回 Data Lake。

#### <a name="step-4-querying"></a>第 4 步：查询

Azure Synapse 分析用于通过 Transact-SQL (T-SQL) 接口查询 Data Lake 中的数据。 此界面包括 SQL 视图。 SQL 视图支持直接通过 T-SQL 客户端（用于临时分析）或通过可视化工具（如 Power BI）对 Data Lake 中的数据进行联合查询。

#### <a name="step-5-modeling-and-serving"></a>步骤 5：建模和服务

Azure Synapse 分析功能查询的数据将转到 Power BI 的语义模型。 根据数据类型，它将定期在内存中导入到 Power BI，也可在运行时直接查询。

最后，在 Power BI 视觉对象中呈现数据，以便用户可以查看数据并与之交互。

## <a name="commerce-analytics-preview-functional-overview"></a>Commerce 分析（预览版）功能概览

### <a name="summary"></a>汇总

Commerce 分析模板应用包括以下主报表页面：

1. [顶级筛选器](#TopLevelFilters)
2. [产品](#ProductsPage)
3. [客户](#CustomersPage)
4. [渠道](#ChannelsPage)
5. [销售额](#SalesPage)
6. [毛利](#MarginsPage)
7. [退货](#ReturnsPage)
8. [折扣](#DiscountsPage)
9. [付款](#PaymentsPage)
10. [客户](#CustomersPage)
11. [比较](#ComparisonPage)
12. [Web 活动](#WebActivityPage)
13. [Web 活动 - 顶级筛选器](#WebActivityTopLevelFilters)

####  <a name="top-level-filters"></a><a name="TopLevelFilters"></a> 顶级筛选器

- 日期设置

    - 年
    - 季度
    - 月
    - 周
    - 星期几

- 渠道设置

    - 法人
    - 通道类型
    - 客户类型
    - 销售类型
    - 渠道
    - 组织层次结构

- 产品设置

    - 类别层次结构
    - 类别

####  <a name="products"></a><a name="ProductsPage"></a> 产品

- 销售额
- 毛利
- 退货

####  <a name="customers"></a><a name="CustomersPage"></a> 客户

- 销售额
- 毛利
- 退货

#### <a name="channels"></a><a name="ChannelsPage"></a> 渠道

- 销售额
- 毛利
- 退货

### <a name="sales"></a>销售额 <a name="SalesPage"></a>

- 按交货位置
- 按渠道/商店/终端
- 按员工
- 按操作日期
- 按小时
- 按产品类别

### <a name="margins"></a><a name="MarginsPage"></a> 毛利

- 按交货位置
- 副产品
- 按操作日期

### <a name="returns"></a><a name="ReturnsPage"></a> 退货

- 按金额列出的退货

    - 按商店
    - 副产品
    - 按操作日期

- 按交易记录列出的退货 

    - 按商店
    - 副产品
    - 按操作日期

### <a name="discounts"></a><a name="DiscountsPage"></a> 折扣

- 按商店
- 副产品
- 按操作日期
- 分解

    - 法人
    - 商店
    - 折扣类型
    - 折扣名称
    - 产品

### <a name="payments"></a><a name="PaymentsPage"></a> 付款

- 按渠道/终端
- 按付款方式/类型
- 按操作日期
- 分解

    - 法人
    - 通道类型
    - 商店
    - 终端
    - 付款方式

### <a name="customers"></a><a name="CustomersPage"></a> 客户

- 生存期值 (LTV)

    根据客户在所有 Dynamics 365 Commerce 销售渠道（包括 POS、电子商务和呼叫中心）上花费的总金额计算 LTV。

- Recency

    根据客户上次与组织进行交易互动以来的天数计算 Recency。 目前，Recency 不考虑非交易互动信号，例如电子商务浏览活动。

- 频率

    根据客户与组织进行的交易互动计算频率。 目前，频率不考虑非交易互动信号，例如电子商务浏览活动。

- 关系长度

    关系长度是根据自从在系统中创建客户记录以来的天数计算的。

- 交易记录计数

### <a name="comparison"></a><a name="ComparisonPage"></a> 比较

- 按时间段列出的产品比较

    - 销售额和销售额差额
    - 毛利和毛利差异

- 按时间段列出的客户

    - 销售额和销售额差额
    - 毛利和毛利差异

### <a name="web-activity"></a><a name="WebActivityPage"></a> Web 活动

#### <a name="top-level-filters"></a><a name="WebActivityTopLevelFilters"></a> 顶级筛选器

- 日期范围
- 通道类型
- 渠道
- 类别层次结构

#### <a name="acquisitions"></a>购置价格

- 页面视图

    - 按国家或地区
    - 副产品
    - 按用户登录状态
    - 按操作日期

- 电子商务订单
- 转化率

    - 按操作日期

- 转化漏斗图

    - 按页面类型（主页、类别页或产品详细信息页）列出的页面视图
    - 添加到购物车
    - 结帐
    - 采购

#### <a name="sessions"></a>会话

会话是用户访问电子商务网站过程中的一个事件。 会话在 30 分钟不活动或有效使用 24 小时后被视为结束。

- 按国家或地区
- 按来源（外部引荐者）
- 按用户登录状态
- 会话计数

    - 按操作日期
    - 按条目页

- 按会话列出的订单

    - 按操作日期

- 会话弹回率

    会话弹回是用户访问您的电子商务网站后立即离开的会话。 有关详细信息，请参阅[弹回率](https://en.wikipedia.org/wiki/Bounce_rate)。

- 每个会话的单击次数

#### <a name="visitors"></a>访问者

根据用户使用的特定浏览器和特定设备唯一标识您的电子商务站点中的匿名访问者。 Commerce 分析不会在不同的浏览器或设备中跟踪匿名访问者。 在多个用户会话中唯一标识在同一设备上使用同一浏览器的匿名访问者，直到清除了浏览器的缓存数据或一段时间（通常为 12 个月）过后，以先发生者为准。

如果访问者登录时浏览电子商务站点，则 Commerce 分析可以提供有关他们的其他信息。 此信息基于您的组织以前在所有 Dynamics 365 Commerce 销售渠道（包括 POS、电子商务和呼叫中心）进行采购从而与访问者之间建立的现有关系。 其他信息包括 Recency、关系长度、生存期值和频率数据。

- 访问者毛利
- 访问者平均订单数
- 访问者平均销售额
- 电子商务访问者计数

    - 按操作日期
    - 按位置

        当前，Commerce 分析只能针对电子商务访问者的位置见解提供国家/地区级别粒度。

    - 按 Recency

        根据客户上次与组织进行交易互动以来的天数计算 Recency。 目前，Recency 不考虑非交易互动信号，例如电子商务浏览活动。

    - 按关系长度

        关系长度是根据自从在系统中创建客户记录以来的天数计算的。

    - 按生存期值 (LTV)

        根据客户在所有 Dynamics 365 Commerce 销售渠道（包括 POS、电子商务和呼叫中心）上花费的总金额计算 LTV。

    - 按频率

        根据客户与组织进行的交易互动计算频率。 目前，频率不考虑非交易互动信号，例如电子商务浏览活动。

#### <a name="impressions"></a>展示

展示是电子商务访问者的产品视觉对象单一视图。 例如，电子商务访问者转到电子商务网站的主页，并在 **最畅销产品** 列表模块中查看瑜伽垫产品。 然后，访问者查看 **为您推荐** 列表模块中的相同瑜伽垫产品。 在这种情况下，存在两个产品展示。 

目前，在以下表面中跟踪了展示：

- 列表（例如，**推荐**、**最畅销产品**、**为您推荐** 和 **热门**）
- 购物车模块
- 搜索结果容器
- 类别搜索结果容器

当前，在轮播模块或自定义视觉对象中呈现的产品未计入与展示相关的指标。

**展示报表** 页面包含以下指标：

- 展示计数

    - 按页面类型和模块

        页面类型是针对电子商务网站上的每个页面定义的一般类型页面。 模块类型是显示产品的电子商务视觉模块的类型。

        要按模块查看展示，您可能需要深入钻取页面和模块视觉对象。

    - 副产品
    - 按用户登录状态
    - 按操作日期

- 展示单击计数

    当电子商务访问者选择产品视觉对象时，将发生一次展示单击。 通常，访问者以后会转到产品的产品详细信息页。

- 展示点入率 (CTR)

    CTR 的计算方法是展示单击总数除以展示总数。

## <a name="commerce-analytics-preview-installation"></a>Commerce 分析（预览版）安装

> [!NOTE]
> Commerce 分析（预览版）在美国、加拿大、英国、欧洲、东南亚、东亚、澳大利亚及日本地区处于预览版阶段。 如果您的 Finance and Operations 环境位于这些地区中的任何一个地区，您可以使用 Microsoft Dynamics Lifecycle Services (LCS) 在环境中启用此功能。 在您可以使用此功能之前，请参阅[配置导出到 Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md)。

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a>启用和配置 Commerce 分析（预览版）

若要安装 Commerce 分析（预览版），您必须具有在 Azure 订阅中创建资源的权限。 您还必须具有在 LCS 中安装加载项的权限。 下面是步骤概述：

1. [提交 Commerce 分析（预览版）的预览引入窗体](#joinPreview)。
2. [启用和配置“导出到 Data Lake”](#enableExportToDataLake)。
3. [启用和配置 Commerce 分析（预览版）加载项](#enableCommerceAnalyticsAddin)。
4. [为您的存储帐户生成共享访问签名 (SAS) 令牌](#getSASToken)。
5. [下载 Azure Synapse 视图的部署脚本](#downloadSynapseDeploymentScripts)。
6. [安装和配置 Azure Synapse workspace](#configureAzureSynapse)。
7. [安装 Power BI 模板应用](#powerbi)。

### <a name="submit-the-preview-intake-form-for-commerce-analytics-preview"></a><a name="joinPreview"></a>提交 Commerce 分析（预览版）的预览引入窗体

提交 [Commerce 分析（预览版）的预览引入窗体](https://forms.office.com/r/vW5VLJGXZ2)。 最多留出三个工作日来处理窗体。 处理窗体后，确认电子邮件将发送到您在窗体中提供的电子邮件地址。

### <a name="enable-and-configure-export-to-data-lake"></a><a name="enableExportToDataLake"></a>启用和配置“导出到 Data Lake”

Commerce 分析（预览版）依赖于“导出到 Data Lake”功能，将 Commerce HQ 数据导出到 Data Lake 并保持数据最新。 在配置 Commerce 分析（预览版）之前，请按照[配置导出到 Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) 中的步骤启用并配置“导出到 Data Lake”。

当您正在配置“导出到 Data Lake”时，请记录以下信息，因为您以后必须输入它：

- <a name="keyVault"></a>密钥保管库的域名系统 (DNS) 名称，以及存储应用程序 ID 和应用程序密钥的密钥名称。 有关详细信息，请参阅[将密钥添加到密钥保管库](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets)。
- <a name="storageAccount"></a>Data Lake 实例的存储帐户的名称。 有关详细信息，请参阅[在订阅中创建 Data Lake Storage (Gen2) 帐户](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createsubscription)。

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a>启用和配置 Commerce 分析（预览版）加载项

要在 LCS 中安装 Commerce 分析（预览版）加载项，您必须是 LCS 中计划使用的环境的环境管理员。

要安装和配置 Commerce 分析（预览版）加载项，请按照以下步骤操作。

1. 登录到 [LCS](https://lcs.dynamics.com/)，然后转到您的环境。
2. 在 **环境** 页面的 **环境加载项** 选项卡上，选择 **安装新加载项**。
3. 在对话框中，选择 **Commerce 分析（预览版）**。

    如果未列出 **Commerce 分析（预览版）**，请确保您已加入内部人员计划。

4. 在 **设置加载项** 对话框中，输入以下信息。

    | 信息 | 源 | 示例值 |
    |---|---|---|
    | 您的环境的 Azure AD 租户 ID | 登录到 [Azure 门户](https://portal.azure.com/)，然后打开 **Azure Active Directory** 服务。 然后打开 **属性** 页面，并在 **目录 ID** 字段中复制该值。 | 72f988bf-0000-0000-00000-2d7cd011db47 |
    | 密钥保管库的 DNS 名称 | 输入密钥保管库的 [DNS 名称](#keyVault)。 您应在上一节中记录了此值。 | `https://contosod365datafeedpoc.vault.azure.net/` |
    | 包含应用程序 ID 的密钥 | 输入[存储应用程序 ID 的密钥名称](#keyVault)。 您应在上一节中记录了此值。 | 应用 ID |
    | 包含应用程序密钥的密钥 | 输入[存储应用程序密钥的密钥名称](#keyVault)。 您应在上一节中记录了此值。 | 应用密码 |

5. 通过选择此复选框来接受产品/服务条款，然后选择 **安装**。

    系统会为环境安装和配置 Commerce 分析（预览版）加载项。 此流程或许需要几分钟的时间。 完成后，应在 **环境** 页面上列出 **Commerce 分析（预览版）**，并且状态应为 **已安装**。

### <a name="generate-a-sas-token-for-your-storage-account"></a><a name="getSASToken"></a>为您的存储帐户生成 SAS 令牌

SAS 令牌使外部实体能够访问您的存储帐户，并具有限时有效的特定特权集。 Azure Synapse 将使用 SAS 令牌访问 Data Lake 中的基础数据。

> [!NOTE]
> 由于 Commerce 分析（预览版）存在已知限制，因此，当 SAS 令牌到期时，Azure Synapse 实例将失去对 Data Lake 的访问权限。 因此，当您生成 SAS 令牌时，您应设置组织安全策略允许的最晚到期日期。

若要生成 SAS 令牌，请执行以下步骤。

1. 在 Azure 门户中，转到您在配置“导出到 Data Lake”时创建的[存储帐户](#storageAccount)。
2. 在左窗格中的存储帐户下面选择 **共享访问签名**。
3. 在 **SAS 选项** 页面上，设置以下字段。

    | 字段 | 值 |
    |---|---|
    | 允许的服务 | 选择 **Blob**。 |
    | 允许的资源类型 | 选择 **服务**、**容器** 和 **对象**。 |
    | 允许的权限 | 选择 **读取**、**写入**、**删除**、**列出**、**添加** 和 **创建**。 |
    | Blob 版本控制权限 | 选择 **允许删除版本**。 |
    | 开始和到期日期/时间 | 根据情况设置 SAS 令牌的开始日期和结束日期和时间。 |
    | 允许的 IP 地址 | 保持此字段为空。 |
    | 允许的协议 | 选择 **仅限 HTTPS**。 |
    | 首选路由层 | 选择 **基本（默认）**。 |
    | 签名密钥 | 根据情况选择 **Key1** 或 **Key2**。 |

4. 选择 **生成 SAS 和连接字符串**。
5. 复制 **SAS 令牌** 字段中的值，并将其粘贴到文本编辑器（如 Notepad）中。

### <a name="download-the-deployment-scripts-for-azure-synapse-views"></a><a name="downloadSynapseDeploymentScripts"></a>下载 Azure Synapse 视图的部署脚本

若要在 Azure Synapse workspace 中创建和发布所需的视图，您必须运行一组脚本。 请按照以下步骤下载脚本。

1. 在 GitHub 上，转到 [microsoft/Dynamics365Commerce.Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) 存储库。
2. 通过克隆存储库或将其作为 zip 文件下载，将脚本下载到本地计算机。

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a>安装和配置 Azure Synapse workspace

若要安装和配置 Azure Synapse workspace，请按照以下步骤操作。

1. 在 Azure 订阅中安装 Azure Synapse workspace。 有关详细信息，请参阅[快速入门：创建 Synapse workspace](/azure/synapse-analytics/quickstart-create-workspace)。
2. 在记事本或其他文本编辑器中，从本地计算机上的相应文件夹中打开 **SetupSynapse.sql** 脚本文件，在上一部分中，您已经将 Dynamics365Commerce.Solutions 存储库克隆或下载到此本地计算机。 脚本文件将位于 /Pipeline/CommerceAnalyticsSynapse/ 文件夹下。 在此脚本中，将占位符文本替换为下表中显示的值。

    | 占位符文本 | 替换值 |
    |---|---|
    | placeholder_storageaccount | 您在配置“导出到 Data Lake”时创建的[存储帐户](#storageAccount)的名称。 |
    | <a name="phContainer"></a>placeholder_container | 在 LCS 中成功安装“导出到 Data Lake”加载项后在 Data Lake 实例中创建的存储容器的名称。 若要获取集装箱名称，您必须在 Azure 门户中使用存储资源管理器浏览您的存储帐户。 |
    | placeholder_sastoken | 您生成的 [SAS 令牌](#getSASToken)。 请务必从 SAS 令牌值的开头删除问号 (**?**)。 |
    | <a name="phUserPwd"></a>placeholder_password | 您选择的强密码。 记下此密钥。 它将被设置为脚本创建的新 **reportreadonlyuser** 帐户的密码。 请 **勿** 输入 **sqladminuser**  帐户的密码。 |

3. 复制脚本文件的更新内容。
4. 在 Azure 门户中，转到新 Azure Synapse workspace。 在 **概览** 页面上，选择 **打开 Synapse Studio**。
5. 在 Synapse Studio 中，选择 **新建 \> SQL 脚本**，并将脚本文件的内容粘贴到 SQL 脚本编辑器中。
6. 确保 **使用数据库** 字段设置为 **主**。
7. 选择 **运行**，等待脚本完成运行。 成功执行脚本后，将创建 Commerce 分析数据库、用于访问 Data Lake 的凭据，以及 Power BI 连接到 Azure Synapse 实例将使用的只读用户帐户。
8. 在本地计算机上，在管理模式下打开 Windows PowerShell，然后转到您将 Dynamics365Commerce.Solutions 存储库克隆或下载到的文件夹下面的 /Pipeline/CommerceAnalyticsSynapse/ 文件夹。
9. 通过运行以下命令设置 Windows PowerShell 执行策略。

    ```powershell
    Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
    ```

10. 如果 SQL Server PowerShell 模块尚未安装，请通过运行以下命令来安装它。

    ```powershell
    Install-Module sqlserver
    ```

    > [!NOTE]
    > 在安装此模块期间，可能会提示您安装 NuGet 提供程序。 在这种情况下，选择 **Y** 以安装 NuGet 提供程序。 可能还会提示您确认您正在从不受信任的存储库安装模块。 在这种情况下，选择 **Y** 以继续安装。 您可以选择性地运行 **Set-PSRepository** cmdlet 以信任 **PSGallery** 存储库。

11. 通过运行以下命令发布 Azure Synapse 视图。

    ```powershell
    .\PublishSynapseViews.ps1 -serverName SERVER_NAME -password PASSWORD -storageAccount STORAGE_ACCOUNT -containerName CONTAINER_NAME -datarootpath DATA_ROOT_PATH
    ```

    运行此命令时，请替换占位符值，如下表所示。

    | 占位符值 | 替换值 |
    |---|---|
    | SERVER_NAME | Azure Synapse 无服务器 SQL 终结点的名称。 您可以从 Azure 门户中 Azure Synapse workspace 的 **概览** 页中获取此值。 |
    | PASSWORD | **sqladminuser** 帐户的密码。 |
    | STORAGE_ACCOUNT | Data Lake 的存储帐户的名称。 |
    | CONTAINER_NAME | 由“导出到 Data Lake”功能创建的容器的名称。 此容器就是您在第 2 步中指定为 [placeholder_container](#phContainer) 值的容器。 |
    | DATA_ROOT_PATH | 包含所有数据的容器下的文件夹名称。 |

    > [!NOTE]
    > 您可以在 Azure 门户中使用 Azure 存储浏览器和 Data Lake 存储帐户来查找存储帐户名称、容器名称和数据根路径。

12. 等待脚本完成运行。 成功执行脚本后，将在 Azure Synapse 无服务器 SQL 实例中创建 SQL 视图。

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a>安装 Power BI 模板应用

要安装 Commerce 分析（预览版）的 Power BI 模板应用，请按照以下步骤操作。

1. 使用您的组织 ID 登录到 [Power BI 门户](https://powerbi.microsoft.com/)。
2. 通过转到 [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp) 来安装 Commerce 分析（预览版）Power BI 模板应用。 您可能会收到一条警告，说明 AppSource 上未列出此应用。 选择 **安装**。
3. 如果您是第一次重新此应用，请向前跳转到第 5 步。 如果您之前已安装此应用，则将显示以下用于更新应用的选项：

    - **更新工作区和应用** - 更新现有模板应用，并覆盖现有应用设置，如应用实例名称和权限配置。
    - **仅更新工作区内容而不更新应用** - 更新现有模板应用，但保留现有应用设置。 *此选项是应用更新的建议选项。*
    - **将应用的另一个副本安装到新的工作区** - 创建一个新工作区，然后在其中创建现有模板应用的副本。 现有工作区将保持不变。

4. 选择更新选项之一，然后选择 **安装**。
5. 通过在左窗格中选择 **应用**，然后选择应用，打开已安装的应用。
6. 通过选择 **连接** 将应用连接到您的数据源。 如果您之前已安装该应用，请在黄色消息栏中选择 **连接您的数据** 链接。
7. 设置以下字段。

    | 字段 | 值 |
    |---|---|
    | 服务器 | 输入您在上一节中创建的 Azure Synapse 无服务器 SQL 终结点的名称。 您可以从 Azure 门户中 Azure Synapse workspace 的 **概览** 页中获取此值。 |
    | 数据库 | 输入 **CommerceAnalytics**。 |
    | 语言 | 在列表中选择值。 此字段用于本地化的产品和类别名称。 值区分大小写。 |
    | 日期范围 | 在列表中选择值。 所选月数的数据将导入到 Power BI 数据集中。 您选择的值会影响数据集的大小和同步所需的时间。 |

8. 选择 **下一步**。 系统会提示您输入用于连接到 Azure Synapse SQL 数据库的凭据。 按下表所示设置字段。

    | 字段 | 值 |
    |---|---|
    | 身份验证方法 | 选择 **基本**。 |
    | 用户名 | 输入 **reportreadonlyuser**。 |
    | 密码 | 输入您在 SetupSynapse.sql 脚本中用以替换 [placeholder_password](#phUserPwd) 占位符的值。 此密码是 **reportreadonlyuser** 帐户的密码。 |

9. 选择 **登录并连接**。
10. 等待数据集成功更新。 然后选择 **编辑应用** 按钮以打开应用工作区，您可以在其中查看数据集的更新状态。 在应用工作区中，您还可以选择性地为数据集设置自动更新计划，管理权限并重命名应用实例。

### <a name="privacy"></a><a name="privacy"></a>隐私

我们非常尊重您的隐私。 要了解详细信息，请阅读我们的[隐私声明](https://go.microsoft.com/fwlink/?LinkId=521839)。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
