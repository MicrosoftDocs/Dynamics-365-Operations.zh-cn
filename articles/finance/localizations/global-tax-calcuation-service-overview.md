---
title: 税款计算概览
description: 本文说明税务计算功能的总体范围和功能。
author: wangchen
ms.date: 03/02/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 24d4a722ee143dc0869f758475aaf377e7a9e084
ms.sourcegitcommit: 78576abe5c7cbab1bb69d26c999b038e8c24873a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/13/2022
ms.locfileid: "8954491"
---
# <a name="tax-calculation-overview"></a>税款计算概览

[!include [banner](../includes/banner.md)]

税务计算是一种超级可扩展的多租户服务，使 Global Tax Engine 可以自动化并简化税务确定和计算流程。 税务引擎完全可配置。 可配置的元素包括但不限于应纳税数据模型、税码、税务适用性矩阵和税务计算公式。 税务引擎在 Microsoft Azure 核心服务平台上运行，并提供现代技术和指数可扩展性。

税务计算将 Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 集成。 最终，它还将与 Dynamics 365 Project Operations、Dynamics 365 Commerce 以及其他第一方和第三方应用程序集成。

> [!IMPORTANT]
> 当您启用税款计算时，可能在数据中心（维护您的服务数据的数据中心除外）中执行对相关数据的某些操作。 在启用税款计算之前，查看[条款和条件](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md)。 我们非常尊重您的隐私。 要了解详细信息，请阅读我们的[隐私声明](https://go.microsoft.com/fwlink/?LinkId=521839)。

税款计算是一款基于微服务的税务引擎，它提供指数级可扩展性，并且可以帮助您执行以下任务：

- 通过增强的确定机制自动确定正确的销售税组、物料销售税组和税码。
- 支持一个法人多个税务登记号，自动确定应税交易的正确税务登记号。
- 支持转移单的税务确定、计算、过帐和结算。
- 定义特定业务要求的可配置税金计算公式和条件。
- 在法人之间共享税务确定和计算解决方案，以省去维护工作并避免错误。
- 支持客户和供应商税务登记编号确定。
- 支持列表代码确定。
- 在税区级别支持税款计算参数。

若要使用税款计算，请在 Microsoft Dynamics Lifecycle Services 中从您的项目安装税款计算加载项。 然后，在 [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) 中完成设置，并在 Finance 和 Supply Chain Management 中启用税款计算。 有关详细信息，请参阅[开始使用税务服务](global-get-started-with-tax-calculation-service.md)。

## <a name="availability"></a>可用性

从版本 10.0.21 起，税款计算在生产环境中向所有客户公开发布。

将继续交付新功能。 请经常查看最新的发布计划，以了解受支持功能的覆盖率和范围。

税务计算在以下 Azure 地理区域中部署。 将根据客户需求添加更多 Azure 地理区域。

- 亚太
- 澳大利亚
- 加拿大
- 欧洲
- 日本
- 瑞士
- 英国
- 美国

> [!NOTE]
> 税款计算不支持早期版本的 Dynamics 365，例如 Dynamics AX 2012 或 Dynamics 365 的本地部署。

## <a name="versions"></a>版本
我们建议您使用与您的 Finance 或 Supply Chain Management 版本相匹配的版本导入和设置税款计算配置。

| Finance 或 Supply Chain Management 版本 | 税务配置版本               |
| --------------- | --------------------------------------- |
| 10.0.18         | 税款配置 - 欧洲 30.12.82     |
| 10.0.19         | 税款计算配置 36.38.193 |
| 10.0.20         | 税款计算配置 40.43.208 |
| 10.0.21         | 税款计算配置 40.48.215 |
| 10.0.22         | 税款计算配置 40.48.215 |
| 10.0.23         | 税款计算配置 40.50.221 |
| 10.0.24         | 税款计算配置 40.50.225 |
| 10.0.25         | 税款计算配置 40.50.225 |
| 10.0.26         | 税款计算配置 40.54.234 |
| 10.0.27         | 税款计算配置 40.54.234 |
| 10.0.28         | 税款计算配置 40.54.234 |


## <a name="data-flow"></a>数据流

以下是税款计算的数据流流程的概述。 

1. 在 RCS 中，查看和导入应纳税单据模型配置和模型映射配置。 如果您必须扩展高级方案的配置，请参阅[在税务配置中添加数据字段](tax-service-add-data-fields-tax-configurations.md)。
2. 在 RCS 中，创建或维护税务功能。 您可以使用税务功能来维护税率和税适用性规则。
3. 完成税务功能设置后，将 RCS 中的税务配置和税务功能发布到全局存储库。
4. 在 Finance 中，选择要用于特定法人的税务功能设置版本。
5. 在 Finance 和 Supply Chain Management 中，照常操作交易。 需要税款计算时，客户端将从交易（如销售订单或采购订单）中收集信息，并将信息打包为有效负载。 然后将发送一个请求以计算税款。
6. 从客户端收到税款计算请求，并完成计算。 税务结果随后返回到客户端。
7. Dynamics 365 客户端将收到税务结果，并在销售税页面上显示税金计算结果。

## <a name="supported-transactions"></a>支持的交易

可以通过交易来启用税款计算。 

以下交易在版本 10.0.21 中受支持： 

- 销售额

    - 销售报价
    - 销售订单
    - 确认单
    - 领料单
    - 装箱单
    - 销售账单
    - 贷方通知单
    - 退货单
    - 标题杂项费用
    - 行杂项费用

- 采购

    - 采购订单
    - 确认单
    - 收货清单
    - 产品收货
    - 采购账单
    - 标题杂项费用
    - 行杂项费用
    - 贷方通知单
    - 退货单
    - 采购申请
    - 采购申请行杂项费用
    - 询价
    - 询价标题杂项费用
    - 询价行杂项费用

- 库存

    - 转移单 – 装运
    - 转移单 – 接收

以下交易在版本 10.0.23 中受支持： 

- 普通发票

以下交易在版本 10.0.26 中受支持： 

- 普通日记帐
- 供应商发票日记帐

以下交易在版本 10.0.28 中受支持： 

- 供应商付款日记帐
- 客户付款日记帐

## <a name="supported-countriesregions"></a>支持的国家/地区

法人可以启用税款计算。 

版本 10.0.21 支持法人主要地址的以下国家/地区：

- 奥地利
- 比利时
- 丹麦
- 爱沙尼亚
- 芬兰
- 法国
- 德国
- 匈牙利
- 冰岛
- 爱尔兰
- 意大利
- 拉脱维亚
- 立陶宛
- 荷兰
- 挪威
- 波兰
- 瑞典
- 瑞士
- 英国
- 美国

版本 10.0.22 支持法人主要地址的以下国家/地区：

- 澳大利亚
- 巴林
- 加拿大
- 埃及
- 香港特别行政区
- 科威特
- 新西兰
- 阿曼
- 卡塔尔
- 沙特阿拉伯
- 南非
- 阿拉伯联合酋长国

版本 10.0.23 支持法人主要地址的以下国家/地区：

- 泰国
- 日本
- 马来西亚
- 新加坡

版本 10.0.24 支持法人主要地址的以下国家/地区：

- 墨西哥

版本 10.0.26 支持法人主要地址的以下国家/地区：

- 中国
- 捷克共和国
- 西班牙

## <a name="related-resources"></a>相关资源

[开始使用税务服务](./global-get-started-with-tax-calculation-service.md)

[多个增值税登记编号](./emea-multiple-vat-registration-numbers.md)

[转移单的税务功能支持](./tasks/tax-feature-support-for-transfer-order.md)

[如何在税务服务中生成扩展](./tax-service-add-data-fields-tax-integration-by-extension.md)
