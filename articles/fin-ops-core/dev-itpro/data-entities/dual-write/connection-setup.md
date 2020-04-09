---
title: 支持双写入的方案
description: 此主题介绍支持双写入的方案。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
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
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: d7ff514768ee8e4797b591da89e190a855385885
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172846"
---
# <a name="supported-scenarios-for-dual-write-setup"></a>支持双写入的方案

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

可以在 Finance and Operations 环境与 Common Data Service 环境之间建立双写入连接。

+ **Finance and Operations 环境** 为 **Finance and Operations 应用**（如 Microsoft Dynamics 365 Finance、Dynamics 365 Supply Chain Management、Dynamics 365 Retail 和 Dynamics 365 Human Resources）提供基础平台。
+ **Common Data Service 环境**为 **Dynamics 365 中的模型驱动应用**（Dynamics 365 Sales、Dynamics 365 Customer Service、Dynamics 365 Field Service、Dynamics 365 Marketing 和 Dynamics 365 Project Service Automation）提供基础平台。

设置机制取决于订阅和环境。

+ 对于 Finance and Operations 应用的新实例，双写入连接的设置在 Microsoft Dynamics Lifecycle Services (LCS) 中开始。 如果您有 Microsoft Power Platform 的许可证，并且您的租户没有 Common Data Service 环境，您将获取一个新的该环境。
+ 对于现有实例的 Finance and Operations 应用，双写入连接的设置在 Finance and Operations 环境中开始。

支持以下设置方案：

+ [一个新 Finance and Operations 应用实例和一个新模型驱动应用实例](#new-new)
+ [一个新 Finance and Operations 应用实例和一个现有模型驱动应用实例](#new-existing)
+ [一个具有演示数据的新 Finance and Operations 应用实例和一个新模型驱动应用实例](#new-demo-new)
+ [一个具有演示数据的新 Finance and Operations 应用实例和一个现有模型驱动应用实例](#new-demo-existing)
+ [一个现有 Finance and Operations 应用实例和一个新的或现有模型驱动应用实例](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a>一个新 Finance and Operations 应用实例和一个新模型驱动应用实例

若要在无数据的 Finance and Operations 应用新实例与 Dynamics 365 中的模型驱动应用新实例之间设置双写入连接，请执行[从 Lifecycle Services 设置双写入](lcs-setup.md)中的步骤。 完成连接设置之后，将自动执行以下操作：

- 预配一个新的空 Finance and Operations 环境。
- 预配一个新的空模型驱动应用实例，其中已安装了 CRM 主解决方案。
- 为 DAT 公司数据建立双写入连接。
- 为实时同步启用实体映射。

然后，这两个环境准备好了进行实时数据同步。

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a>一个新 Finance and Operations 应用实例和一个现有模型驱动应用实例

若要在无数据的 Finance and Operations 应用新实例与 Dynamics 365 中的模型驱动应用现有实例之间设置双写入连接，请执行[从 Lifecycle Services 设置双写入](lcs-setup.md)中的步骤。 完成连接设置之后，将自动执行以下操作：

- 预配一个新的空 Finance and Operations 环境。
- 为 DAT 公司数据建立双写入连接。
- 为实时同步启用实体映射。

然后，这两个环境准备好了进行实时数据同步。

若要将现有 Common Data Service 数据同步到 Finance and Operations 应用，请执行以下步骤。

1. 在 Finance and Operations 应用中创建一个新公司。
2. 将该公司添加到双写入连接设置。
3. 通过使用三个字母的国际标准化组织 (ISO) 公司代码[引导](bootstrap-company-data.md) Common Data Service 数据。

因为双写入处于实时同步模式，所以 Common Data Service 中的数据将自动开始流向 Finance and Operations 应用。

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a>一个具有演示数据的新 Finance and Operations 应用实例和一个新模型驱动应用实例

若要在有演示数据的新 Finance and Operations 应用实例与 Dynamics 365 中的模型驱动应用新实例之间建立双写入连接，请执行此主题前文中[一个新 Finance and Operations 应用程序和一个新模型驱动应用实例](#new-new)部分中的步骤。 完成连接设置后，如果要将演示数据同步到模型驱动应用，请执行以下步骤。

1. 从 LCS 页面打开 Finance and Operations 应用，然后转到**数据管理 \> 双写入**。
2. 对要同步其数据的实体运行**初始同步**功能。

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a>一个具有演示数据的新 Finance and Operations 应用实例和一个现有模型驱动应用实例

若要在有演示数据的新 Finance and Operations 应用实例与 Dynamics 365 中的模型驱动应用现有实例之间建立双写入连接，请执行此主题前文中[一个新 Finance and Operations 应用程序和一个现有模型驱动应用实例](#new-existing)部分中的步骤。 完成连接设置后，如果要将演示数据同步到模型驱动应用，请执行以下步骤。

1. 从 LCS 页面打开 Finance and Operations 应用，然后转到**数据管理 \> 双写入**。
2. 对要同步其数据的实体运行**初始同步**功能。

若要将现有 Common Data Service 数据同步到 Finance and Operations 应用，请执行以下步骤。

1. 在 Finance and Operations 应用中创建一个新公司。
2. 将该公司添加到双写入连接设置。
3. 通过使用三个字母的 ISO 公司代码[引导](bootstrap-company-data.md) Common Data Service 数据。

因为双写入处于实时同步模式，所以 Common Data Service 中的数据将自动开始流向 Finance and Operations 应用。

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a>一个现有 Finance and Operations 应用实例和一个新的或现有模型驱动应用实例

若要设置现有 Finance and Operations 应用实例与 Dynamics 365 中的模型驱动应用的新的或现有的实例之间的双写入连接，需要在 Finance and Operation 环境中进行。

1. 从 Finance and Operations 应用设置连接。
2. 若要将现有 Common Data Service 数据同步到 Finance and Operations 应用，请使用三个字母的 ISO 公司代码[引导](bootstrap-company-data.md) Common Data Service 数据。

因为双写入处于实时同步模式，所以 Common Data Service 中的数据将自动开始流向 Finance and Operations 应用。
