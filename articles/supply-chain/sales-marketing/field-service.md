---
title: "与 Microsoft Dynamics 365 for Field Service 集成"
description: "此主题概述与 Microsoft Dynamics 365 for Field Service 集成。"
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a57e23691a6b4d48c6b8dd6d1f61fc9730365b39
ms.openlocfilehash: 0c1268d2fddcf7b28ecfc3197f21e9d30a5a5855
ms.contentlocale: zh-cn
ms.lasthandoff: 05/31/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>与 Microsoft Dynamics 365 for Field Service 集成

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations 支持在 Finance and Operations 与 Microsoft Dynamics 365 for Field Service 之间同步业务流程。 集成方案的配置方法是使用可扩展的数据集成器模板和 Common Data Service (CDS) 实现业务流程同步。

[![Finance and Operations 与 Field Service 之间的业务流程同步](./media/field-service-integration.png)](./media/field-service-integration.png)

Field Service 与 Finance and Operations 集成的第一阶段的重点是让 Field Service 中的工作订单和协议在 Finance and Operations 中开票。 支持的流程在 Field Service 中启动，在这里将工作订单的信息作为销售订单同步到 Finance and Operations。 在 Finance and Operations 中，将为销售订单开票以生成发票单据。 此外，还会将 Field Service 协议发票的信息同步到 Finance and Operations。 Microsoft Dynamics 365 数据集成器使用可定制项目同步数据。 可使用标准模板创建定制集成项目，还可以使用模板映射更多标准字段和定制字段以及实体以调整集成并满足具体要求。

Field Service 与 Finance and Operations 集成的第二阶段是实现以下项的同步：

- [Finance and Operations 中的产品到 Field Service 中的产品（包括产品类型信息）](field-service-product.md)
- [Field Service 中的工作订单到 Finance and Operations 中的销售订单](field-service-work-order.md)
- [Field Service 中的发票到 Finance and Operations 中的普通发票](field-service-invoice.md)

若要查看有关如何在 Field Service 与 Finance and Operations 之间同步工作订单的示例，请观看下面的 YouTube 短片：[在 Dynamics 365 for Field Service 与 Finance and Operations 之间同步工作订单](https://www.youtube.com/watch?v=hAB4TDVMjxU)。

[![](https://img.youtube.com/vi/hAB4TDVMjxU/0.jpg)](https://www.youtube.com/watch?v=hAB4TDVMjxU)

## <a name="system-requirements-for-finance-and-operations"></a>Finance and Operations 的系统要求
Field Service 集成支持以下版本：

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations 版本 8.0（2018 年 4 月）或更高版本

- Dynamics 365 for Finance and Operations 版本 8.0（2018 年 4 月）已于 2018 年 4 月发布，其中包含带平台更新 15 (7.0.4841.35234) 的应用程序版本号 8.0.30.8020。 

## <a name="system-requirements-for-field-service"></a>Field Service 的系统要求
若要使用 Field Service 集成解决方案，必须安装以下组件：

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>Microsoft Dynamics 365 for Field Service 9.0 或更高版本

- Dynamics 365 for Field Service 版本 1612 (9.0.1.733) (DB 9.0.1.733) 联机或更高版本。
- Dynamics 365 版本 1.15.0.1 或更高版本的从目标客户到现金 (P2C) 解决方案。 可从 [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3) 下载此解决方案。
- 适用于 Dynamics 365 版本 1.0.0.0 或更高版本的 Field Service 集成解决方案。 可从 [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration) 下载此解决方案。

