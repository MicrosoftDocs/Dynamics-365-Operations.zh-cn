---
title: Commerce 分析（预览版）
description: 本文介绍如何安装和使用 Microsoft Dynamics 365 Commerce 中的分析功能。
author: AamirAllaq
ms.date: 02/24/2022
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 9ffa0affa0b80af65dd2aa37ef2fe969752ae332
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887158"
---
# <a name="commerce-analytics-preview"></a>Commerce 分析（预览版）

[!include [banner](includes/banner.md)]

本文介绍如何安装 Commerce 分析（预览版）功能，这是 Microsoft Dynamics 365 Commerce 中包含的功能性分析功能。

## <a name="commerce-analytics-preview-live-demo"></a>Commerce 分析（预览版）实时演示

您可以试用 [Commerce 分析（预览版）实时演示](https://aka.ms/CommerceAnalyticsDemo)。

![Commerce 分析（预览版）摘要](media/CommerceAnalytics_Summary.png)
![Commerce 分析（预览版）付款](media/CommerceAnalytics_Payments.png)
![Commerce 分析（预览版）Web 活动](media/CommerceAnalytics_WebActivity.png)

## <a name="commerce-analytics-preview-system-architecture"></a>Commerce 分析（预览版）系统体系结构

### <a name="key-components"></a>重要组件

Commerce 分析（预览版）由以下关键组件组成：

- 随时可用的交互式 Power BI 报表
- Azure Synapse Analytics 中的 SQL 视图
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

Azure Synapse Analytics 用于通过 Transact-SQL (T-SQL) 接口查询 Data Lake 中的数据。 此界面包括 SQL 视图。 SQL 视图支持直接通过 T-SQL 客户端（用于临时分析）或通过可视化工具（如 Power BI）对 Data Lake 中的数据进行联合查询。

#### <a name="step-5-modeling-and-serving"></a>步骤 5：建模和服务

Azure Synapse Analytics 查询的数据将转到 Power BI 的语义模型。 根据数据类型，它将定期在内存中导入到 Power BI，也可在运行时直接查询。

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

#### <a name="top-level-filters"></a><a name="TopLevelFilters"></a> 顶级筛选器

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

#### <a name="products"></a><a name="ProductsPage"></a> 产品

- 销售额
- 毛利
- 退货

#### <a name="customers"></a><a name="CustomersPage"></a> 客户

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
> Commerce 分析（预览版）在美国、加拿大、英国、欧洲、东南亚、东亚、澳大利亚及日本地区处于预览版阶段。 如果您的财务和运营环境位于这些地区中的任何一个地区，您可以使用 Microsoft Dynamics Lifecycle Services (LCS) 在环境中启用此功能。 在您可以使用此功能之前，请参阅[配置导出到 Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md)。

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a>启用和配置 Commerce 分析（预览版）

若要安装 Commerce 分析（预览版），您必须具有在 Azure 订阅中创建资源的权限。 您还必须具有在 LCS 中安装加载项的权限。

要启用和配置 Commerce 分析（预览），请按照以下步骤操作。

1. [提交 Commerce 分析（预览）的预览引入窗体](#joinPreview)
2. [启用和配置“导出到 Data Lake”加载项](#enableExportToDataLake)。
3. [安装和配置 Azure Synapse workspace](#configureAzureSynapse)。
4. [将机密添加到密钥保管库](#addSecrets)。
5. [启用和配置 Commerce 分析（预览版）加载项](#enableCommerceAnalyticsAddin)。
6. [安装 Power BI 模板应用](#powerbi)。

### <a name="submit-the-preview-intake-form-for-commerce-analytics-preview"></a><a name="joinPreview"></a>提交 Commerce 分析（预览版）的预览引入窗体

提交 [Commerce 分析（预览版）的预览引入窗体](https://forms.office.com/r/vW5VLJGXZ2)。 处理您的请求后，确认电子邮件将发送到您在窗体中提供的电子邮件地址。

### <a name="enable-and-configure-the-export-to-data-lake-add-in"></a><a name="enableExportToDataLake"></a>启用和配置“导出到 Data Lake”加载项

> [!IMPORTANT]
> 配置“导出到 Data Lake”加载项时，请清除“导出到 Data Lake”加载项设置页面上的 **实时数据更改** 复选框，以确保未启用实时数据更改。 **实时数据更改** 功能处于预览阶段，目前不受 Commerce 分析支持。 如果您启用此功能，Commerce 分析将无法处理您在数据湖中的数据，您的大多数 Power BI 报表将不显示任何数据。

Commerce 分析（预览）依赖于“导出到 Data Lake”功能，将 Commerce headquarters 数据导出到 Data Lake 并保持数据最新。 在配置 Commerce 分析（预览版）之前，请按照[配置导出到 Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) 中的步骤启用并配置“导出到 Data Lake”。

当您配置“导出到 Data Lake”加载项时，请记录以下信息，因为您以后必须输入它：

- <a name="keyVault"></a>您提供的密钥保管库的域名系统 (DNS) 名称。
- 您提供的机密名称，其中包含应用程序 ID 和应用程序机密。 有关详细信息，请参阅[将密钥添加到密钥保管库](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets)。

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a>安装和配置 Azure Synapse workspace

Commerce 分析（预览）需要在您的 Azure Synapse workspace 中预配按需 Synapse SQL。 若要安装和配置 Azure Synapse workspace，请按照以下步骤操作。

1. 在 Azure 订阅中安装 Azure Synapse workspace。 有关详细信息，请参阅[快速入门：创建 Synapse workspace](/azure/synapse-analytics/quickstart-create-workspace)。
1. <a name="serverlessep"></a>预配工作区后，打开资源概览页面，记下 **无服务器 SQL 终结点** 值。 在下一节中，您必须将此值存储在密钥保管库中。
1. 在概览页面上，选择 **打开 Synapse Studio** 链接以打开工作区的 Azure Synapse Studio。
1. 在左侧菜单中选择 **管理**。 要查看菜单名称，您可能必须选择左侧菜单上的展开链接。
1. 在 **安全组** 下，选择 **访问控制**。 
1. 选择 **添加**。
1. 在 **添加角色分配** 窗格中，如下表所述设置选项。

    | 选项 | 值 |
    |--------|-------|
    | 范围 | 选择 **工作区**。 |
    | 角色 | 选择 **Synapse SQL 管理员**。|
    | 选择一个用户 | 搜索您[在安装“导出到 Data Lake”加载项期间创建的](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createapplication)应用程序的名称。 当应用程序出现在搜索结果中时，选择它。 应用程序现在将出现在 **所选用户、组或服务主体** 部分。 |

1. 选择 **应用** 完成角色分配。 应用程序已被授予 Synapse SQL 管理员特权。 因此，它可以在配置 Commerce 分析（预览）LCS 加载项期间创建所需的视图。

### <a name="add-secrets-to-the-key-vault"></a><a name="addSecrets"></a>将机密添加到密钥保管库

在配置“导出到 Data Lake”加载项时使用的同一[密钥保管库](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createkeyvault)中，必须添加下表中显示的机密。 对于每个机密，必须提供一个机密名称和指定的值。

| 建议的机密名称 | 密码值 | 示例机密值 |
|---------|---------|---------|
| synapse-sql-server | 您在[配置 Azure Synapse workspace](#serverlessep) 时记下的无服务器 SQL 终结点值。 | `test-ondemand.sql.azuresynapse.net` |
| <a name="roUser"></a>readonly-sql-pwd | 要为 SQL 只读用户设置的密码。 Power BI 报表将使用此密码连接到无服务器 SQL。 要设置此密码，请遵照组织的密码策略操作。 | |

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a>启用和配置 Commerce 分析（预览版）加载项

要在 LCS 中安装 Commerce 分析（预览版）加载项，您必须是 LCS 中计划使用的环境的环境管理员。

要安装和配置 Commerce 分析（预览版）加载项，请按照以下步骤操作。

1. 登录到 [LCS](https://lcs.dynamics.com/)，然后转到您的环境。
2. 在 **环境** 页面的 **环境加载项** 选项卡上，选择 **安装新加载项**。
3. 在对话框中，选择 **Commerce 分析（预览版）**。
4. 在 **设置加载项** 对话框中，输入以下信息。

    | 信息 | 源 | 示例值 |
    |---|---|---|
    | Azure Active Directory (Azure AD) 租户 ID | 登录到 [Azure 门户](https://portal.azure.com/)，然后打开 **Azure Active Directory** 服务。 然后打开 **属性** 页面，并在 **租户 ID** 字段中复制该值。 | `72f988bf-0000-0000-00000-2d7cd011db47` |
    | 您的 Azure 密钥保管库的 DNS 名称 | 输入密钥保管库的 DNS 名称。 您在[配置“导出到 Data Lake”加载项](#keyVault)时应该已记下此值。 | `https://contosod365datafeedpoc.vault.azure.net/` |
    | 包含应用程序 ID 的机密名称 | 输入存储应用程序 ID 的密钥名称。 您在[配置“导出到 Data Lake”加载项](#keyVault)时应该已记下此值。 | `app-id` |
    | 包含应用程序机密的机密名称 | 输入存储应用程序密钥的密钥名称。 您在[配置“导出到 Data Lake”加载项](#keyVault)时应该已记下此值。 | `app-secret` |
    | 包含 Azure Synapse 的无服务器 SQL 终结点的机密名称 | 输入存储无服务器 SQL 终结点的机密名称。 您在[将机密添加到密钥值](#addSecrets)时应该已经创建了此机密。 | `synapse-sql-server` |
    | 包含要在 Azure Synapse 中为 SQL 只读用户设置的密码的机密名称 | 输入存储要为无服务器 SQL 只读用户设置的密码的机密名称。 此用户将为您创建，应在 Power BI 报表中用于连接到无服务器 SQL 服务器。 您在[将机密添加到密钥值](#addSecrets)时应该已经创建了此机密。 | `readonly-sql-pwd` |

1. 通过选择此复选框来接受产品/服务条款，然后选择 **安装**。

    系统会为环境安装和配置 Commerce 分析（预览版）加载项。 此流程或许需要几分钟的时间。 完成后，应在 **环境** 页面上列出 **Commerce 分析（预览版）**，并且状态应为 **已安装**。

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a>安装 Power BI 模板应用

要安装 Commerce 分析（预览版）的 Power BI 模板应用，请按照以下步骤操作。

1. 使用您的组织 ID 登录到 [Power BI 门户](https://powerbi.microsoft.com/)。
1. 通过转到 [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp) 来安装 Commerce 分析（预览版）Power BI 模板应用。 或者，访问 [Dynamics 365 Commerce 分析的 AppSource 页面](https://appsource.microsoft.com/product/power-bi/dynamics-365-commerce.dydnamics-365-commerce-analytics)，选择 **立即获取**。
1. 如果您是第一次重新此应用，请向前跳转到第 5 步。 如果您之前安装过，将应用以下更新应用的选项：

    - **更新工作区和应用** - 更新现有模板应用，并覆盖现有应用设置，如应用实例名称和权限配置。
    - **仅更新工作区内容而不更新应用** - 更新现有模板应用，但保留现有应用设置。 *此选项是应用更新的建议选项。*
    - **将应用的另一个副本安装到新的工作区** - 创建一个新工作区，然后在其中创建现有模板应用的副本。 现有工作区将保持不变。

1. 选择更新选项之一，然后选择 **安装**。
1. 通过在左窗格中选择 **应用**，然后选择应用，打开已安装的应用。
1. 通过选择 **连接** 将应用连接到您的数据源。 如果您之前已安装该应用，请在黄色消息栏中选择 **连接您的数据** 链接。
1. 设置以下字段。

    | 字段 | 值 |
    |---|---|
    | 服务器 | 输入您在[创建 Azure Synapse workspace](#serverlessep) 后记下的无服务器 SQL 终结点。 |
    | 数据库 | 输入 **CommerceAnalytics**。 |
    | 语言 | 在列表中选择值。 此字段用于本地化的产品和类别名称。 值区分大小写。 |
    | 日期范围 | 在列表中选择值。 所选月数的数据将导入到 Power BI 数据集中。 您选择的值会影响数据集的大小和同步所需的时间。 |

1. 选择 **下一步**。 当系统提示您输入用于连接到 Azure Synapse SQL 数据库的凭据时，如下表所示设置字段值。

    | 字段 | 值 |
    |---|---|
    | 身份验证方法 | 选择 **基本**。 |
    | 用户名 | 输入 **reportreadonlyuser**。 |
    | 密码 | 输入您[在密钥保管库中为 SQL 只读用户存储](#roUser)的密码。 |

1. 选择 **登录并连接**。
1. 等待数据集成功更新。 然后选择 **编辑应用** 打开应用工作区，您可以在其中查看数据集的更新状态。 在应用工作区中，您还可以选择性地为数据集设置自动更新计划，管理权限并重命名应用实例。

### <a name="privacy"></a><a name="privacy"></a>隐私

我们非常尊重您的隐私。 要了解详细信息，请阅读我们的[隐私声明](https://go.microsoft.com/fwlink/?LinkId=521839)。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
