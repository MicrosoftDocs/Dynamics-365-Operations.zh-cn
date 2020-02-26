---
title: 与 Common Data Service 的近实时数据集成
description: 本主题提供 Finance and Operations 与 Common Data Service 之间的集成概述。
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
ms.openlocfilehash: 1c09b0c0bb695e7695acb7a8821ffb99ae1f6f06
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019662"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a>与 Common Data Service 的近实时数据集成

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

在现在的数字世界中，业务生态系统把 Microsoft Dynamics 365 应用程序作为整体使用。 因为来自人员、客户、运营和物联网 (IoT) 设备的数据传输到一个源，所以可能发生数字反馈循环。 Finance and Operations 应用与其他 Dynamics 365 应用程序之间的集成对实现此体验至关重要。 有些应用程序以 Common Data Service 为基础。 Finance and Operations 应用数据与 Common Data Service 之间的集成使其他应用程序与 Finance and Operations 之间能够进行连贯流畅的通信。

Finance and Operations 应用和 Common Data Service 通过双写入框架提供 Finance and Operations 应用与其他 Dynamics 365 应用程序之间的近实时数据同步。 范围广阔，跨越应用程序的 28 个外围应用。 目的是通过用于连接应用程序之间的业务流程的无缝数据流来提供“单 Dynamics 365”用户体验。

![体系结构概览图](media/dual-write-overview.jpg)

可以采用以下价值主张：

+ [Common Data Service 中的组织层次结构](organization-mapping.md)
+ [Common Data Service 中的公司概念](company-data.md)
+ [集成客户主控](customer-mapping.md)
+ [集成的分类帐](ledger-mapping.md)
+ [通用产品体验](product-mapping.md)
+ [集成供应商主控](vendor-mapping.md)
+ [集成的站点和仓库](sites-warehouses-mapping.md)
+ [集成的税收主数据](tax-mapping.md)

## <a name="system-requirements"></a>系统要求

同步、双向、近实时数据流需要以下版本：

+ 带平台更新 28 或更高版本的 Microsoft Dynamics 365 for Finance and Operations 版本 10.0.4（2019 年 7 月）
+ Microsoft Dynamics 365 for Customer Engagement，平台版本 9.1 (4.2) 或更高版本

## <a name="setup-instructions"></a>设置说明

请按照以下步骤设置 Finance and Operations 应用与 Common Data Service 之间的集成。
    
1. 有关设置双写入系统，请参阅[分步指南](https://aka.ms/dualwrite-docs)中的“发布双写入预览版”。
2. 从[通过双重写入实现 Fin Ops 和 CDS/CE 集成](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer 组下载和安装解决方案。 包中包含五个解决方案：

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. 遵循[同步初始参考数据](initial-sync.md)的执行顺序。
4. 如果遇到双写入同步问题，请参阅[数据集成疑难解答指南](dual-write-troubleshooting.md)。

> [!IMPORTANT]
> 不能并排运行双写入和[目标客户到现金](../../../../supply-chain/sales-marketing/prospect-to-cash.md)。 如果正在运行目标客户到现金解决方案，则必须将其卸载。 还必须禁用目标客户到现金解决方案中的客户和供应商双写入模板。
