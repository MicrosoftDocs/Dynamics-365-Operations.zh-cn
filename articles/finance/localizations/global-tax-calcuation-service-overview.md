---
title: 税款计算(预览版)
description: 本主题说明税务计算功能的总体范围和功能。
author: wangchen
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bab6e0e0ea1b9fb7f598e37843b52e3ba9c7f94e
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/03/2021
ms.locfileid: "6336624"
---
# <a name="tax-calculation-preview"></a>税款计算(预览版)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

税务计算是一种超级可扩展的多租户服务，使 Global Tax Engine 可以自动化并简化税务确定和计算流程。 税务引擎完全可配置。 可配置的元素包括但不限于应纳税数据模型、税码、税务适用性矩阵和税务计算公式。 税务引擎在 Microsoft Azure 核心服务平台上运行，并提供现代技术和指数可扩展性。

税务计算与 Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 集成。 最终，它还将与 Dynamics 365 Project Operations、Dynamics 365 Commerce 以及其他第一方和第三方应用程序集成。

> [!IMPORTANT]
> 当您启用税务计算服务时，可能在数据中心（维护您的服务数据的数据中心除外）中执行对相关数据的某些操作。 在启用税务计算服务之前，查看[条款和条件](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md)。 我们非常尊重您的隐私。 要了解详细信息，请阅读我们的[隐私声明](https://go.microsoft.com/fwlink/?LinkId=521839)。

税务计算是基于微服务的税务引擎，可提供指数可扩展性。 它可以帮助您执行以下任务：

- 通过 Regulatory Configuration Service (RCS) 配置税务计算。 RCS 是增强版本的电子报告 (ER) 设计器，可作为独立服务提供。
- 配置税务矩阵以自动确定税码和税率。
- 配置税务矩阵以自动确定税务登记编号。
- 配置税务计算设计器以定义公式和条件。
- 跨法人共享税务确定和计算解决方案。

若要使用税务计算服务，请在 Microsoft Dynamics Lifecycle Services (LCS) 中从您的项目安装税务计算服务加载项。 然后，在 RCS 中完成设置，并在 Finance 和 Supply Chain Management 中启用税务计算服务。 有关详细信息，请参阅[开始使用税务服务](./global-get-started-with-tax-calculation-service.md)。

## <a name="availability"></a>可用性

税务计算通过公开预览版计划仅在沙盒环境中对所选客户可用。 最终，它将在生产环境中对所有客户公开可用。

将继续提供新功能，因此务必经常查看最新文档，以了解受支持功能的覆盖率和范围。

税务计算在以下 Azure 地理区域中部署。 它还将根据客户需求部署到更多 Azure 地理区域：

- 美国
- 欧洲

> [!NOTE]
> 税务计算不支持 Dynamics 365 的本地部署。 它还不支持早期版本，例如 Dynamics AX 2012。

## <a name="feature-highlights"></a>功能亮点

- 可配置的税务矩阵，用于自动确定和计算税务
- 支持多个税务登记编号
- 对税务确定和计算的转移单支持
- 对确定多个税务登记编号的转移单支持

## <a name="supported-transactions"></a>支持的交易

可以通过法人和交易启用税务计算。 支持以下交易：

- 销售流程

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

- 采购流程

    - 采购订单
    - 确认单
    - 收货清单
    - 产品收据
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

- 库存流程

    - 转移单 – 装运
    - 转移单 – 接收

## <a name="related-resources"></a>相关资源

[开始使用税务服务](./global-get-started-with-tax-calculation-service.md)

[多个增值税登记编号](./emea-multiple-vat-registration-numbers.md)

[转移单的税务功能支持](./tasks/tax-feature-support-for-transfer-order.md)

[如何在税务服务中生成扩展](./tax-service-add-data-fields-tax-integration-by-extension.md)
