---
title: Microsoft Dynamics 365 Field Service 集成概览
description: 本文提供与 Microsoft Dynamics 365 Field Service 集成的概览。
author: Henrikan
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: b0427d33ac39d34bccc302e58bb84e1ad4c3598c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888432"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a>Microsoft Dynamics 365 Field Service 集成概览

[!include[banner](../includes/banner.md)]



Supply Chain Management 实现 Dynamics 365 Supply Chain Management 与 Dynamics 365 Field Service 之间的业务流程同步。 集成方案的配置方法是使用可扩展的数据集成器模板和 Microsoft Dataverse 实现业务流程同步。
可使用标准模板创建定制集成项目，还可以使用模板映射更多标准列和自定义列以及表以调整集成并满足具体业务需求。 

Field Service 集成紧接着现有客户到现金功能建立。

![Supply Chain Management 与 Field Service 之间的业务流程同步。](./media/field-service-integration.png)

Field Service 与 Supply Chain Management 集成的第一阶段的重点是让 Field Service 中的工作订单和协议在 Supply Chain Management 中开票。 支持的流程在 Field Service 中启动，在这里将工作订单的信息作为销售订单同步到 Supply Chain Management。 在 Supply Chain Management 中，将为销售订单开票以生成发票单据。 此外，还会将 Field Service 协议发票的信息同步到 Supply Chain Management。 Microsoft Dynamics 365 数据集成器使用可定制项目同步数据。 可使用标准模板创建定制集成项目，还可以使用模板映射更多标准列和自定义列以及表以调整集成并满足具体要求。

Field Service 与 Supply Chain Management 集成的第二阶段是实现以下项的同步：

- [将 Supply Chain Management 中的产品直接同步到 Field Service 中的产品](field-service-product.md)
- [将 Field Service 中的工作订单同步到 Supply Chain Management 中的销售订单](field-service-work-order.md)
- [将 Field Service 中的协议发票同步为 Supply Chain Management 中的普通发票](field-service-invoice.md)

若要查看有关如何在 Field Service 与 Supply Chain Management 之间同步工作订单的示例，请观看下面的 YouTube 短片：[如何使用 Microsoft Dynamics 365 集成同步工作订单](https://www.youtube.com/watch?v=46ylO7raZAo)。

## <a name="integration-with-field-service-including-inventory-and-project-information"></a>与 Field Service 的集成，包括库存和项目信息

此第二个阶段的附加功能关注为现场技术人员提供有关 Supply Chain Management 的库存信息的见解，让他们可以更新库存水平、执行物料转移。 此外，安装或为售出货物提供服务的公司将通过项目集成受益于更好地控制以及对完整销售和服务流程的了解。

### <a name="functionality-includes-integration-of"></a>功能包括以下集成：
- 仓库信息
- 现有库存信息
- 库存转移
- 库存调整
- 与 Dynamics 365 Field Service 工作订单连接的 Supply Chain Management 项目
- 包含 Supply Chain Management 项目链接的 Dynamics 365 Field Service 工作订单将此项目编号应用于销售订单以允许从项目开票。 

![在 Supply Chain Management 和 Field Service 之间同步业务流程，包括库存和项目信息。](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a>Field Service 与 Supply Chain Management 集成的第二阶段支持与以下模板的同步：
- 仓库（Supply Chain Management 到 Field Service）- 仓库从 Supply Chain Management 到 Field Service [高级查询] 
- 产品库存（Supply Chain Management 到 Field Service）- 库存级别信息从 Supply Chain Management 到 Field Service [高级查询] 
- 库存调整（Field Service 到 Supply Chain Management）- 库存调整从 Field Service 到 Supply Chain Management [高级查询] 
- 库存转移（Field Service 到 Supply Chain Management）- 库存转移从 Field Service 到 Supply Chain Management [高级查询] 
- 项目（Supply Chain Management 到 Field Service）- 项目列表从 Supply Chain Management 到 Field Service 
- 项目的工作订单（Field Service 到 Supply Chain Management）- Field Service 中的工作订单到 Supply Chain Management 中的销售订单，支持项目[高级查询] 
- 包含库存单位的 Field Service 产品（Supply Chain Management 到 Sales）- Supply Chain Management“适售的已发布产品”到 Field Service 的“销售产品”，包括库存单位 

## <a name="system-requirements"></a>系统要求

### <a name="system-requirements-for-supply-chain-management"></a>Supply Chain Management 的系统要求
Field Service 集成支持以下版本：

- Dynamics 365 for Finance and Operations 版本 8.1.2（2018 年 12 月）通过平台更新 22 (7.0.5095) 在 2018 年 12 月发布，具有应用程序内部版本号 8.1.195。 

### <a name="system-requirements-for-field-service"></a>Field Service 的系统要求
若要使用 Field Service 集成解决方案，必须安装以下组件：

- Dynamics 365 9.1.x 上的 Field Service（版本 8.2.0.286）或更高版本 - 2018 年 11 月发布
- Dynamics 365 版本 1.15.0.1 或更高版本的从目标客户到现金 (P2C) 解决方案。 可从 [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3) 下载此解决方案。
- 适用于 Dynamics 365 版本 2.0.0.0 或更高版本的“Field Service 集成、项目和库存”解决方案。 可从 [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2) 下载此解决方案。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]