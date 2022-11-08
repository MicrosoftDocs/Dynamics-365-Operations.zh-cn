---
title: Store Commerce 应用功能
description: 本文介绍 Microsoft Dynamics 365 Commerce 的 Store Commerce 应用中提供的功能。
author: anupamar-ms
ms.date: 10/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2022-09-30
ms.openlocfilehash: d713cc0e9537ae20ffddee6e77779a16e74bd779
ms.sourcegitcommit: eb9a53d5cf10f1ada68757536d6a94b2cb00929d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/27/2022
ms.locfileid: "9725630"
---
# <a name="store-commerce-app-capabilities"></a>Store Commerce 应用功能

[!include [banner](includes/banner.md)]

Store Commerce 应用是 Microsoft Dynamics 365 Commerce 的现代销售点 (POS) 体验。 它让企业能够在店内处理交易，同时管理后端办公系统操作，如库存和订单处理。 此应用还让企业能够通过会员和客户服务来管理客户关系。 

Store Commerce 应用由 Commerce Scale Unit (CSU) 提供支持，可以提供完整的全渠道解决方案。 例如，客户可以在线购买产品，然后在附近的商店提货，从而在不丢失任何数据的情况下继续跨渠道购物。 

本文概述了 Store Commerce 应用的功能。

## <a name="platform"></a>平台

| 功能 | Description | 文档 | 补充内容 |
|---|---|---|---|
| 全渠道 | Dynamics 365 Commerce 提供统一后勤办公系统、商店内、呼叫中心和数字体验的综合性全渠道解决方案。 | [概览](index.md) | [技术交流](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/dynamics-365-commerce-overview-november-2-2020) |
| 无头商务 | Commerce Scale Unit 承载无头商务引擎。 无头商务引擎充当所有商务业务逻辑的中心点，为完整的全渠道解决方案提供支持。 | <p>[体系结构概览](commerce-architecture.md)</p><p>[无头体系结构](dev-itpro/retail-server-architecture.md)</p> | [技术交流](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-commerce-architecture-overview-december-4-2020) |
| Commerce headquarters | Commerce headquarters 提供支持产品、员工、业务流程、定价和其他业务所需功能的配置的后端办公系统功能。 | [体系结构概览](commerce-architecture.md) | |
| 销售点 (POS) | Store Commerce 应用是 Dynamics 365 Commerce 的 POS 体验。 它提供功能丰富且全面的 POS 功能，可帮助销售助理、出纳和经理提供卓越的客户服务。 此外，它还为零售商提供多个部署选项，有助于提高绩效，并提供改进的应用程序生命周期管理 (ALM)。 | [Store Commerce 应用](dev-itpro/store-commerce.md) | <p>[技术交流](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/modernize-the-dynamics-365-commerce-in-store-technology-using-the-new-store-commerce-app-march-30-2022)</p><p>[视频](https://youtu.be/7B332XH_zfs)</p><p>[从 MPOS 迁移到 Store Commerce](dev-itpro/pos-extension/migrate-mpos-store-commerce.md)</p> |
| 云部署 | 可以部署多个 Commerce Scale Unit 实例来实现负荷分散和地理接近。 | [云部署](../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md) | |
| 本地部署 | 使用本地业务数据部署，Commerce 客户可以更好地拥有和管理 Dynamics 365 环境。 | [本地部署](../fin-ops-core/dev-itpro/deployment/deploy-retail-onprem.md) | |

## <a name="device-management"></a>设备管理

| 功能 | Description | 文档 | 补充内容 |
|---|---|---|---|
| 多种外形规格 | Store Commerce 应用支持多种设备外形规格，如 PC、平板电脑和移动设备。 响应式用户界面 (UI) 让布局能够自动调整大小，适应屏幕大小。 | [视觉对象配置](pos-screen-layouts.md) | |
| 跨平台 | Store Commerce 应用在 Web、Windows、iOS 和 Android 平台上受支持。 | [平台](dev-itpro/hybridapp.md) | |
| 品牌 | 屏幕设计器可让您自定义屏幕布局来满足您的业务要求。 此外，可以根据员工角色创建主题、布局、颜色和图像，然后可以在用户之间共享，以实现品牌一致性和易用性。 | [视觉对象配置](pos-screen-layouts.md) | [视频](https://www.youtube.com/watch?v=ldqCw2wf5fY) |
| 拓扑 | 根据网络可用性，支持不同的店内拓扑。 | <p>[拓扑](dev-itpro/retail-modern-pos-architecture.md)</p><p>[信息图](dev-itpro/retail-in-store-topology.md)</p> | |
| 多设备管理 | 可以从 Commerce headquarters 轻松管理各个商店中的多个设备。 | [启用](set-up-activation-accounts-validate-devices-hq.md) | [技术交流](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/commerce-mass-deployment-with-sccm-system-center-configuration-manager-october-6-2022) |

## <a name="employee-management"></a>员工管理

| 功能 | Description | 文档 | 补充内容 |
|---|---|---|---|
| 登录 | 每个商店员工可以有专用登录方式。 登录类型包括用户名、条码、磁条阅读器 (MSR)、生物识别和 Azure Active Directory (Azure AD)。 | <p>[Azure AD](aad-pos-logon.md)</p><p>[扩展登录](extended-logon.md)</p> | |
| 权限 | 支持不同级别的员工权限，如创建订单的权限和编辑订单的权限。 | [权限](tasks/create-pos-permission-groups.md) | |
| 工时和出勤管理 | 考勤可以使用打卡时间功能进行管理。 考勤数据可以使用 Dynamics 365 Human Resources 应用处理到工资单中。 | [工时管理](retail-time-attendance.md) | |
| 销售佣金 | 销售代表可以跟踪销售来计算佣金或其他奖励。 | [佣金](pos-sales-groups-track-commissions.md) | |

## <a name="merchandising"></a>促销

| 功能 | Description | 文档 | 补充内容 |
|---|---|---|---|
| 分类管理 | 促销经理可以对产品进行分类，让产品可以在特定渠道和特定时段内销售。 | [分类](assortments.md) | |
| 目录 | 促销经理可以管理目录，以确定您希望以目录特定价格提供的产品。 | [目录](/dynamicsax-2012/appuser-itpro/about-retail-product-catalogs) | |
| 产品和类别管理 | 在 Commerce headquarters 中，促销经理可以创建具有变型、属性、度量单位等的产品。 还可以定义类别层次结构来组织管理产品。 | [产品](retail-hierarchies.md) | |
| 捆绑 | 促销经理可以对产品进行分组，以捆绑销售或套件形式出售产品。 | [配套件](/dynamicsax-2012/appuser-itpro/about-setting-up-retail-product-kits) | |
| 信息代码 | 使用信息代码可提示出纳在不同 POS 操作（如商品销售、商品退货或客户选择）期间输入信息。 | [信息代码](/dynamicsax-2012/appuser-itpro/about-info-codes-retail) | |
| 链接物料 | 使用链接物料可在将物料添加到交易中时追加销售产品。 | [链接物料](/dynamicsax-2012/appuser-itpro/set-up-products-for-cross-selling-and-up-selling) | |
| 保修 | 延长保修可以与产品一起出售。 | [保修](extended-warranty.md) | |
| 标签打印 | 可以生成包含产品信息的标签，如批号、序列号和到期日期。 | [标签打印](/dynamicsax-2012/appuser-itpro/create-and-print-labels-overview) | |

## <a name="assisted-selling"></a>协助销售

| 功能 | Description | 文档 | 补充内容 |
|---|---|---|---|
| 产品浏览 | 按类别浏览产品。 | [产品层次结构](retail-hierarchies.md) | |
| 产品搜索 | 按名称搜索产品，使用品牌、价格和材料等产品属性细化搜索。 此功能由 Azure 认知搜索提供支持。 | [云助力的搜索](cloud-powered-search-overview.md) | |
| 产品详细信息页面 | 丰富的产品详细信息页面可以包括图像、描述、产品属性和推荐产品。 建议由建议服务提供支持。 | | |
| 产品比较 | 比较多种产品，帮助客户选择一种添加到交易中。 | | |
| 无限通道 | 轻松查找其他商店的库存，然后创建订单。 | [查找库存](pos-inventory-lookup-operation.md) | [技术交流](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| 推荐 | 使用建议服务追加销售和交叉销售产品。 此服务使用专利技术根据购买趋势以及新到货、相似外观和畅销等特征提出建议。 这些建议可在产品详细信息页面、**客户详细信息** 页面和 **交易** 页面上找到。 | [推荐](product-recommendations.md) | [技术交流](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-recommendations-march-2-2021) |

## <a name="customer-relationship"></a>客户关系

| 功能 | Description | 文档 | 补充内容 |
|---|---|---|---|
| 客户管理 | 创建、编辑和管理客户帐户。 可以在异步模式下管理客户帐户以避免实时处理。 | [管理](customer-mgmt-stores.md) | |
| 客户属性 | 客户属性框架允许根据业务要求捕获额外的客户相关数据。 | [属性](dev-itpro/customer-attributes.md) | |
| 客户详细信息页面 | 丰富的客户详细信息页面提供客户跨所有渠道交互的全渠道视图。 这些交互包括购买、愿望列表和会员积分。 | | |
| 云助力的客户搜索 | 按姓名、电话号码、电子邮件地址、会员卡、地址等搜索客户。 | [云助力的搜索](pos-search-improvements.md#customer-search) | |
| 会员和奖励 | 客户可以加入会员计划，跨渠道赚取和兑换会员积分。 | [忠诚度](set-up-customer-loyalty-program.md) | |
| 客户服务解决方案 | 使用客户手册管理关键客户，在客户配置文件中跟踪活动和注释。 Dynamics 365 Customer Insights 集成让商店员工可以了解每个客户的下一个最佳行为。 | [客户服务解决方案](clienteling-overview.md#activities-and-notes) | |

## <a name="pricing-and-discounts"></a>定价和折扣

| 功能 | Description | 文档 | 补充内容 |
|---|---|---|---|
| 贸易协议 | 定价经理可以根据特定客户的长期交易，使用贸易协议来定义特殊价格。 | [定价](price-management.md)| [视频](https://www.youtube.com/watch?v=r2VD8IxHesM) |
| 销售协议 | 定价经理可以使用销售协议在企业到企业 (B2B) 商业场景中定义基于合同的价格。 | [定价](price-management.md) | |
| 价格调整 | 定价经理可以使用价格调整功能创建、跟踪和管理产品一段时间内的降价。 | [价格调整](price-adjustments-discounts.md) | |
| 折扣 | 定价经理可以设置多种类型的折扣来开展各种促销活动。 这些折扣包括简单折扣、数量折扣、阈值折扣、组合购买折扣、基于支付方式的折扣和装运折扣。 | [折扣](retail-discounts-overview.md) | |
| 优惠券 | 定价经理可以设置优惠券代码或条码，将它们与折扣链接，然后分发给客户。 销售助理可以将优惠券添加到销售交易中或将其删除。 | [优惠券](coupons.md) | |
| 价格组 | 定价经理可以使用价格组功能根据渠道、目录、隶属关系或会员计划定义上下文价格。 | [定价](price-management.md) | |
| 可用促销 | 销售助理可以轻松查找商店中可用的产品促销、已添加到交易的产品等。 | [定价功能](pos-pricing-functions.md) | |
| 价格查询 | 销售助理可以快速查看商店中产品的有效销售价格。 | [定价功能](pos-pricing-functions.md) | |
| 价格替代 | 具有所需权限的销售助理可以替代系统配置或计算的价格。 | [定价功能](pos-pricing-functions.md) | |
| 手动折扣 | 具有所需权限的销售助理可以在销售交易或销售行应用手动折扣。 | [定价功能](pos-pricing-functions.md) | |

## <a name="electronic-payments"></a>电子支付

| 功能 | Description | 文档 | 补充内容 |
|---|---|---|---|
| 贷方和借方 | Store Commerce 应用支持通过 Adyen 付款网关进行主要信用卡和借记卡付款，并支持通过 PayPal 履行订单。 付款 SDK 允许独立软件供应商 (ISV) 集成支持的外部网关连接。 | <p>[Adyen](dev-itpro/adyen-connector.md?tabs=10-0-23)</p><p>[PayPal](paypal.md)</p><p>[付款](payment-methods.md)</p> | <p>[技术交流](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-configuration-february-9-2021)</p><p>[技术交流](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-overview-processing-february-4-2021)</p> |
| 数字钱包支持 | Store Commerce 应用支持通过数字钱包付款方式进行付款，这些付款方式不像传统信用卡和借记卡那样使用银行标识号 (BIN) 范围。 付款方式可以映射到数字钱包付款，如 Adyen。 | [电子钱包](wallets.md) | |
| 礼品卡支持 | 银行标识号 Dynamics 365 礼品卡、储值解决方案 (SVS) 和 Givex 礼品卡。 礼品卡可以按订单购买和兑换。 | [礼品卡](dev-itpro/gift-card.md) | [技术交流](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/d365-commerce-internal-gift-cards-november-16-2021) |
| 欺诈保护 | Dynamics 365 Fraud Protection 帮助您阻止欺诈活动，发现欺诈可能被忽视的地方。 | [欺诈保护](dev-itpro/dfp.md) | [视频](https://www.youtube.com/watch?v=j_1nEiq3LfM) |

## <a name="taxes-and-charges"></a>税收和费用

| 功能 | Description | 文档 | 补充内容 |
|---|---|---|---|
| 税金 | Store Commerce 应用支持很多类型的间接税收，例如销售税、增值税 (VAT)，商品劳务税 (GST)，基于单位的费用和预缴税金。 | [税金](/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json) | |
| 费用 | 可以在行级别、标题级别、作为自动收费、按渠道等配置费用。 | [费用](omni-auto-charges.md) | |

## <a name="order-processing-and-fulfillment"></a>订单处理和履行

| 功能 | Description | 文档 | 补充内容 |
|---|---|---|---|
| 订单创建 | 可以为装运或在附近商店提货创建订单。 可以为提货提供时间段。 | [概览](customer-orders-overview.md) | |
| 订单修改 | 订单可以修改、退货、取消，等等。 | <p>[取消](customer-orders-overview.md#cancel-a-customer-order)</p><p>[退货](pos-returns.md)</p> | |
| 搜索订单 | 使用特定于订单的信息搜索和筛选订单。 | [搜索](enhancedorderrecall.md) | |
| 订单属性 | 订单属性框架允许根据业务要求捕获额外的订单相关信息。 | [属性](dev-itpro/order-attributes.md) | |
| 直接交货 | 项目可以标记为由供应商直接交付到客户地址。 直接交货也称作直接出货。 | [直接交货](/dynamics365/supply-chain/sales-marketing/tasks/ship-orders-direct-deliveries) | |
| 报价单 | 商店员工可以为客户创建报价单，并可以指定特殊价格、手动折扣和报价单有效期。 | [报价单](/dynamics365/supply-chain/sales-marketing/tasks/create-edit-sales-quotations) | |
| 履行 | 商店可以领取、包装和装运订单。 可以将装箱单添加到准备装运的包裹中。 | [履行](order-fulfillment-overview.md) | [技术交流](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-supporting-buy-online-pickup-in-store-curbside-with-dynamics-365-commerce-pos-february-3-2021) |
| 分配的订单管理 | Store Commerce 应用支持智能订单履行优化，优化可以根据业务性质、客户类型、订单来源和订单交货方式配置业务策略。 | [DOM](dom.md) | |

## <a name="inventory-management"></a>库存管理

| 功能 | Description | 文档 | 补充内容 |
|---|---|---|---|
| 集中采购配送 | 简化从配送中心到多个商店或仓库的可用库存分配。 | [集中采购配送](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [技术交流](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| 越库配送 | 简化将传入采购订单的库存分配到多个商店或仓库。 | [越库配送](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [技术交流](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| 入站库存 | 通过采购订单从供应商处接收库存，或通过转移单从另一个仓库接收库存。 创建入站采购订单或转移单请求。 | [传入](pos-inbound-inventory-operation.md) | [技术交流](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| 出站库存 | 通过转移单将库存运送到另一个仓库，并创建出站转移单请求。 | [传出](pos-outbound-inventory-operation.md) | [技术交流](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| 查找库存 | 检查各商店和仓库的产品现有库存，并检查未来日期的可承诺 (ATP) 库存。 | [查找库存](pos-inventory-lookup-operation.md) | [技术交流](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| 库存调整 | 调整进出商店仓库的库存以满足特定的业务要求，无需使用销售、收货或重新盘点。 | [库存调整](work-with-store-inventory.md) | [技术交流](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| 存货盘点 | 盘点实际库存，并调整系统记帐库存以与其匹配。 | [盘点](work-with-store-inventory.md) | [技术交流](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| 库存变动 | 在商店内的两个位置之间移动库存。 | [变动](work-with-store-inventory.md) | [技术交流](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |

## <a name="financials"></a>财务

| 功能 | Description | 文档 | 补充内容 |
|---|---|---|---|
| 现金管理 | Store Commerce 应用支持管理商店中的现金和其他指定支付方式。 此外，可以启用商店中的班次对帐来使用高级现金管理功能。 | [现金](cash-mgmt.md) | |
| 财务报表和对帐 | 商店的现金和事务性交易通过对帐单过帐流程在 Commerce headquarters 中记录。 | [对帐单](retail-statements.md) | |
| 收入和支出交易 | 处理商店中的小额现金交易，记录不是以传统方式收到的收入，如失物招领处的资金、大堂咖啡店的收入份额以及地毯清洁服务。 | [对帐单](retail-statements.md) | |
| 发票付款 | 根据发票捕获付款。 | [账单](payinvoice.md) | |

## <a name="employee-productivity"></a>员工工作效率

| 功能 | Description | 文档 | 补充内容 |
|---|---|---|---|
| 任务管理 | 创建任务列表和任务，并将它们分配到商店和员工。 跨商店跟踪任务的状态。 提供与 Microsoft Teams 的无缝集成。 | <p>[任务管理](task-mgmt-overview.md)</p><p>[Microsoft Teams](commerce-teams-integration.md)</p> | [视频](https://www.youtube.com/watch?v=ES1whB4C2lU) |

## <a name="hardware-and-peripherals"></a>硬件和外围设备

| 功能 | Description | 文档 | 补充内容 |
|---|---|---|---|
| 连接外围设备 | 将打印机、银箱、扫描仪和付款设备等外围设备连接到 POS 终端。 | [外围设备](retail-peripherals-overview.md) ||
| 共享外围设备 | 通过将收据打印机、银箱和付款设备连接到共享硬件工作站，可以在很多终端之间共享这些设备。 | <p>[硬件工作站](retail-peripherals-overview.md) ||
| POS 和外围设备模拟器 | 外围设备模拟器支持对通常需要实际 POS 外围设备的方案进行测试。 它还附带一个 POS 模拟器，可用于测试实际外围设备的兼容性，而无需部署 POS 客户端。 | [模拟器](dev-itpro/retail-peripheral-simulator.md) | |

## <a name="receipts"></a>收货

| 功能 | Description | 文档 | 补充内容 |
|---|---|---|---|
| 打印收据 | 销售收据、信用卡收据、礼品收据、发票等各类收据均可默认打印或在结帐时出纳员确认后打印。 还可以从日记帐重新打印。 | [打印](receipt-templates-printing.md) | |
| 电子邮件收据 | 结帐完成后，可以从 POS 通过电子邮件发送收据。 | [电子邮件](email-receipts.md) | |
| 设计收据 | 可以自定义商店收据，让它们显示适合零售商和交易类型的数据和布局。 收据还可以扩展，显示零售商所需的自定义数据。 | [设计](receipt-templates-printing.md) | |

## <a name="offline-support"></a>脱机支持

| 功能 | Description | 文档 | 补充内容 |
|---|---|---|---|
| 无缝脱机 | 无缝脱机让您即使在 Internet 连接受限或不可用时也能继续交易。 数据排除可帮助您减少脱机数据库的数据大小并最大限度地提高性能。 | [脱机](pos-operations.md) | |
| 基于性能的切换 | 当检测到性能下降时切换到脱机模式。 | [脱机](dev-itpro/implementation-considerations-offline.md) | [视频](https://youtu.be/sQU-2pgHToI) |
| 脱机仪表板 | **脱机状态** 仪表板显示每个设备的数据的脱机状态、错误和详细信息。 因此，可以轻松地管理很多设备的状态。 | [脱机](dev-itpro/implementation-considerations-offline.md) | [视频](https://youtu.be/sQU-2pgHToI)|

## <a name="extensibility"></a>可扩展性

| 功能 | Description | 文档 | 补充内容 |
|---|---|---|---|
| Commerce headquarters | 可以通过添加或修改业务流程来自定义 Commerce headquarters 解决方案。 Commerce headquarters 支持使用元数据和代码驱动的扩展模型来添加自定义功能。 它可以轻松集成到外部解决方案中。 | [概览](dev-itpro/extend-customer-cdx-package.md) | [技术交流](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-unlock-the-power-of-dynamics-365-commerce-commerce-extensibility-overview-february-23-2021) |
| 无头商务 | 此可扩展的全渠道 API 框架可用于自定义和添加业务逻辑。 具有请求处理程序以及触发前和触发后扩展模式的 API。 | [CSU](dev-itpro/retail-server-customer-consumer-api.md) | [技术交流](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| Commerce SDK | Commerce SDK 包括扩展或自定义 Dynamics 365 Commerce 功能所需的代码、代码示例、模板和工具。 SDK 在 GitHub 中的不同存储库 (repos) 中发布，具体取决于扩展组件。 | [SDK](dev-itpro/retail-sdk/sdk-github.md) | [技术交流](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| 销售点 | 使用 Commerce SDK 的 POS 扩展功能可以独立扩展 Store Commerce 应用。 此框架支持自定义用户体验 (UX)、工作流和业务逻辑。 | [POS](dev-itpro/pos-extension/pos-extension-overview.md) | [技术交流](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |

## <a name="reporting"></a>报告

| 功能 | Description | 文档 | 补充内容 |
|---|---|---|---|
| 销售报表 | 商店经理可以使用按员工、收银机、付款类型、退货、产品等分类的销售报表。 经理可以查看这些报表，并使用它们来分配佣金和识别产品趋势。 | | |

## <a name="diagnostics"></a>诊断

| 功能 | Description | 文档 | 补充内容 |
|---|---|---|---|
| 操作见解 | 商店精选服务运行状况可靠性和性能指标在客户的 Application Insights 订阅中提供。 提供高级警报和监视功能。 | | |
| 运行状况检查 | 可以通过运行运行状况检查操作来验证连接到 POS 的外围设备的可用性。 然后会修复和验证各个外围设备问题。 | [运行状况检查](pos-healthcheck.md) | [视频](https://www.youtube.com/watch?v=RfPDNmnqYvY) |

## <a name="globalization"></a>全球化

| 功能 | Description | 文档 | 补充内容 |
|---|---|---|---|
| 多市场支持 | 天然支持市场特定功能，如会计整合、GST、预付款开单和预付款。 此功能覆盖欧洲、美洲、俄罗斯、亚洲、沙特阿拉伯等多个市场。 | [全球化](localizations/fiscal-integration-for-retail-channel.md) | |

## <a name="compliance"></a>合规性

| 功能 | Description | 文档 | 补充内容 |
|---|---|---|---|
| Microsoft 标准 | Store Commerce 应用符合 Microsoft 的安全、隐私、辅助功能、一般数据保护条例 (GDPR)、欧盟 (EU) 数据边界等标准。 | | |

