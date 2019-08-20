---
title: Finance and Operations 与 Common Data Service 之间的近实时数据集成
description: 本主题提供 Microsoft Dynamics 365 for Finance and Operations 与 Common Data Service 之间的集成概述。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: aa614c8e6a79a3f7a4f8f2f99f1f1bd1a67ac921
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797220"
---
# <a name="near-real-time-data-integration-between-finance-and-operations-and-common-data-service"></a>Finance and Operations 与 Common Data Service 之间的近实时数据集成

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

在现在的数字世界中，业务生态系统把 Microsoft Dynamics 365 套件作为整体使用。 因为来自人员、客户、运营和物联网 (IoT) 设备的数据传输到一个源，所以可能发生数字反馈循环。 Dynamics 365 for Finance and Operations 与 Dynamics 365 for Customer Engagement 应用程序之间的集成对实现此体验至关重要。 Customer Engagement 应用程序以 Common Data Service 为基础。 Finance and Operations 数据与 Common Data Service 之间的集成让 Customer Engagement 应用程序可以与 Finance and Operations 之间连贯、流畅地通信。

Finance and Operations 和 Common Data Service 通过双写入框架提供 Finance and Operations 与 Customer Engagement 应用程序之间的近实时数据同步。 范围广阔，跨越 Finance and Operations 的 28 个外围应用。 目的是通过用于连接应用程序之间的业务流程的无缝数据流来提供“单 Dynamics 365”用户体验。

![体系结构概览图](media/dual-write-overview.jpg)

客户可以采用以下价值主张：

+ [Common Data Service 中的组织层次结构](dual-write-organization.md)
+ [Common Data Service 中的公司概念](dual-write-company.md)
+ [集成客户主控](dual-write-customer.md)
+ [集成供应商主控](dual-write-vendor.md)
+ 统一基础产品

## <a name="system-requirements"></a>系统要求

同步、双向、近实时数据流需要以下版本：

+ 带平台更新 28 或更高版本的 Microsoft Dynamics 365 for Finance and Operations 版本 10.0.4（2019 年 7 月）
+ Microsoft Dynamics 365 for Customer Engagement，平台版本 9.1 (4.2) 或更高版本

## <a name="setup-instructions"></a>设置说明

按照以下步骤设置 Finance and Operations 与 Common Data Service 之间的集成。
    
1. 有关设置双写入系统，请参阅[分步指南](https://aka.ms/dualwrite-docs)中的“发布双写入预览版”。
2. 从[Finance and Operations、Common Data Service 和 Customer Engagement 集成](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer 组下载和安装解决方案。 包中包含五个解决方案：

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. 遵循[同步初始参考数据](dual-write-initial.md)的执行顺序。
4. 如果遇到双写入同步问题，请参阅[数据集成疑难解答指南](dual-write-troubleshooting.md)。

> [!IMPORTANT]
> 不能并排运行双写入和[目标客户到现金](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct)。 如果正在运行目标客户到现金解决方案，则必须将其卸载。 还必须禁用目标客户到现金解决方案中的客户和供应商双写入模板。
