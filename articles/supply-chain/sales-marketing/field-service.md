---
title: "与 Microsoft Dynamics 365 for Field Service 集成"
description: "此主题概述与 Microsoft Dynamics 365 for Field Service 集成。"
author: ChristianRytt
manager: AnnBe
ms.date: 08/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 95031534c43dc0578e258bc3e5376c429d72b0ab
ms.openlocfilehash: 673ab2a101cee1a3dbbb1249f582d959cecc7f7f
ms.contentlocale: zh-cn
ms.lasthandoff: 12/23/2018

---

# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>与 Microsoft Dynamics 365 for Field Service 集成

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations 支持在 Finance and Operations 与 Microsoft Dynamics 365 for Field Service 之间同步业务流程。 集成方案的配置方法是使用可扩展的数据集成器模板和 Common Data Service (CDS) 实现业务流程同步。
可使用标准模板创建定制集成项目，还可以使用模板映射更多标准字段和定制字段以及实体以调整集成并满足具体业务需求。 

Field Service 集成紧接着现有客户到现金功能建立。

![Finance and Operations 与 Field Service 之间的业务流程同步](./media/field-service-integration.png)

Field Service 与 Finance and Operations 集成的第一阶段的重点是让 Field Service 中的工作订单和协议在 Finance and Operations 中开票。 支持的流程在 Field Service 中启动，在这里将工作订单的信息作为销售订单同步到 Finance and Operations。 在 Finance and Operations 中，将为销售订单开票以生成发票单据。 此外，还会将 Field Service 协议发票的信息同步到 Finance and Operations。 Microsoft Dynamics 365 数据集成器使用可定制项目同步数据。 可使用标准模板创建定制集成项目，还可以使用模板映射更多标准字段和定制字段以及实体以调整集成并满足具体要求。

Field Service 与 Finance and Operations 集成的第二阶段是实现以下项的同步：

- [Finance and Operations 中的产品到 Field Service 中的产品（包括产品类型信息）](field-service-product.md)
- [Field Service 中的工作订单到 Finance and Operations 中的销售订单](field-service-work-order.md)
- [Field Service 中的发票到 Finance and Operations 中的普通发票](field-service-invoice.md)

若要查看有关如何在 Field Service 与 Finance and Operations 之间同步工作订单的示例，请观看下面的 YouTube 短片：[如何使用 Microsoft Dynamics 365 集成同步工作订单](https://www.youtube.com/watch?v=46ylO7raZAo)。

## <a name="system-requirements-for-finance-and-operations"></a>Finance and Operations 的系统要求
Field Service 集成支持以下版本：

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations 版本 8.0（2018 年 4 月）或更高版本

- Dynamics 365 for Finance and Operations 版本 8.0（2018 年 4 月）已于 2018 年 4 月发布，其中包含带平台更新 15 (7.0.4841.35234) 的应用程序版本号 8.0.30.8020。 

## <a name="system-requirements-for-field-service"></a>Field Service 的系统要求
若要使用 Field Service 集成解决方案，必须安装以下组件：

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>Microsoft Dynamics 365 for Field Service 9.0 或更高版本

- Dynamics 365 for Field Service 版本 1612 (9.0.1.733) (DB 9.0.1.733) 联机或更高版本。
- Dynamics 365 版本 1.15.0.1 或更高版本的从目标客户到现金 (P2C) 解决方案。 可从 [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3) 下载此解决方案。
- 适用于 Dynamics 365 版本 1.0.0.0 或更高版本的 Field Service 集成解决方案。 可从 [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegration) 下载此解决方案。

# <a name="integration-with-microsoft-dynamics-365-for-field-service-including-inventory-and-project-information"></a>与 Microsoft Dynamics 365 for Field Service 的集成，包括库存和项目信息

此第二个阶段的附加功能关注为现场技术人员提供有关 Finance and Operations 的库存信息的见解，让他们可以更新库存水平、执行物料转移。 此外，安装或为售出货物提供服务的公司将通过项目集成受益于更好地控制以及对完整销售和服务流程的了解。

### <a name="functionality-includes-integration-of"></a>功能包括以下集成：
- 仓库信息
- 现有库存信息
- 库存转移
- 库存调整
- 与 Dynamics 365 for Field Service 工作订单连接的 Dynamics 365 for Finance and Operations 项目
- 包含 Dynamics 365 for Finance and Operations 项目链接的 Dynamics 365 for Field Service 工作订单将此项目编号应用到 Dynamics 365 for Finance and Operations 销售订单以允许从项目开票。 

![Finance and Operations 与 Field Service 之间的业务流程同步](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-finance-and-operations-enables-synchronization-with-the-following-templates"></a>Field Service 与 Finance and Operations 集成的第二阶段支持与以下模板的同步：
- 仓库（Fin and Ops 到 Field Service）- 仓库从 Finance and Operations 到 Field Service [高级查询] 
- 产品库存（Fin and Ops 到 Field Service）- 库存水平信息从 Finance and Operations 到 Field Service [高级查询] 
- 库存调整（Field Service 到 Fin and Ops）- 库存调整从 Field Service 到 Finance and Operations [高级查询] 
- 库存转移（Field Service 到 Fin and Ops）- 库存转移从 Field Service 到 Finance and Operations [高级查询] 
- 项目（Fin and Ops 到 Field Service）- 项目列表从 Finance and Operations 到 Field Service 
- 项目的工作订单（Field Service 到 Fin and Ops）- Field Service 中工作订单到 Finance and Operations 中的销售订单，提供项目支持[高级查询] 
- 包含库存单位的 Field Service 产品（Fin and Ops 到 Sales）- Finance and Operations“适售的已发布产品”到 Field Service 的“销售产品”，包括库存单位 

## <a name="system-requirements-for-finance-and-operations"></a>Finance and Operations 的系统要求
Field Service 集成支持以下版本：

- Dynamics 365 for Finance and Operations 版本 8.1.2（2019 年 12 月）已于 2019 年 12 月发布，其中包含带平台更新 22 (7.0.5095) 的应用程序版本号 8.1.195。 

## <a name="system-requirements-for-field-service"></a>Field Service 的系统要求
若要使用 Field Service 集成解决方案，必须安装以下组件：

- Dynamics 365 9.1.x 上的 Field Service for Dynamics 365（版本 8.2.0.286）或更高版本 - 2018 年 11 月发布
- Dynamics 365 版本 1.15.0.1 或更高版本的从目标客户到现金 (P2C) 解决方案。 可从 [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3) 下载此解决方案。
- 适用于 Dynamics 365 版本 2.0.0.0 或更高版本的“Field Service 集成、项目和库存”解决方案。 可从 [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2) 下载此解决方案。

