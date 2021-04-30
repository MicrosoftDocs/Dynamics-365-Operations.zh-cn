---
title: Dynamics 365 全球化服务
description: 本主题提供 Microsoft Dynamics 365 全球化服务的概述。
author: JaneA07
manager: AnnBe
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8c6f3b7fb4dec0dffe55014e9e2d60620dc3b193
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893040"
---
# <a name="dynamics-365-globalization-services"></a>Dynamics 365 全球化服务

[!include [banner](../includes/banner.md)]

可以配置以下全球化服务以扩展某些 Microsoft Dynamics 365 联机服务中存在的功能：

- **Regulatory Configuration Service (RCS)** 支持配置不同类型的电子文档和报表。 RCS 提供电子报告 (ER) 设计器的增强版本，其中配置存储库是独立服务。 有关详细信息，请参阅 [Regulatory Configuration Service](rcs-overview.md)。
- **电子开票** 将转换的可配置格式、数字签名和连接性的可配置集成与外部 Web 服务（包括认证和响应处理）集成在一起。 有关详细信息，请参阅[电子开票](e-invoicing-service-overview.md)。
- **税务计算** 通过支持多个纳税人标识号、税码确定、税务计算设计器和运行时引擎提供增强的灵活性，以符合全球范围的复杂税务法规。 有关详细信息，请参阅[税务计算](global-tax-calcuation-service-overview.md)。

这些全球化服务提供与以下 Dynamics 365 联机服务的现成集成。

| 联机服务 | RCS | 电子开票 | 税款计算(预览版) |
|----------------|-----|----------------------|---------------------------|
| Dynamics 365 Finance | 是 | 是 | 是 | 
| Dynamics 365 Supply Chain Management | 是 | 是 | 是 | 
| Dynamics 365 Project Operations | 是 | 是 | 不适用 | 
| Dynamics 365 Commerce | 是 | 不适用 | 不适用 | 

> [!NOTE]
> 由于 RCS 的 Azure 地理位置（地区）的可用性不同，此服务的配置可能会导致客户数据传输到为适用 Dynamics 365 联机服务选择的地区之外。 有关详细信息，请参阅 [Dynamics 365 和 Power Platform：可用性、数据位置、语言和本地化](https://aka.ms/rcs/D365Productavailabilityguide)。