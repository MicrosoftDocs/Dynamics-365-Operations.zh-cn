---
title: 双写入设置指南
description: 本文介绍支持双写入的方案。
author: RamaKrishnamoorthy
ms.date: 06/28/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: b27cabf495448fcd82edd374bb59e6e5a664c7e9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289735"
---
# <a name="guidance-for-dual-write-setup"></a>双写入设置指南

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]



可以在财务和运营环境与 Dataverse 环境之间建立双写入连接。

+ **财务和运营环境** 为 **财务和运营应用**（例如，Microsoft Dynamics 365 Finance、Dynamics 365 Supply Chain Management、Dynamics 365 Commerce 和 Dynamics 365 Human Resources）提供基础平台。
+ **Dataverse 环境** 为 **客户互动应用**（Dynamics 365 Sales、Dynamics 365 Customer Service、Dynamics 365 column Service、Dynamics 365 Marketing 和 Dynamics 365 Project Service Automation）提供基础平台。


> [!IMPORTANT]
> Dynamics 365 Finance 中的人力资源模块支持双写入连接，但 Dynamics 365 Human Resources 应用不支持。

设置机制取决于订阅和环境：

+ 对于财务和运营应用的新实例，双写入连接的设置在 Microsoft Dynamics Lifecycle Services (LCS) 中开始。 如果您有 Microsoft Power Platform 的许可证，并且您的租户没有 Dataverse 环境，您将获取一个新的该环境。
+ 对于财务和运营应用的现有实例，双写入连接的设置在财务和运营环境中开始。

在实体上开始双写入之前，您可以运行初始同步以处理财务和运营应用和客户互动应用上的现有数据。 如果不需要在两个环境之间同步数据，则可以跳过初始同步。

初始同步使您可以将现有数据从一个应用双向复制到另一个应用。 根据已有的环境及其中的数据类型，有几种设置方案。

支持以下设置方案：

+ [一个新的财务和运营应用实例和一个新的客户互动应用实例](#new-new)
+ [一个新的财务和运营应用实例和一个现有的客户互动应用实例](#new-existing)
+ [一个具有数据的新财务和运营应用实例和一个新的客户互动应用实例](#new-data-new)
+ [一个具有数据的新财务和运营应用实例和一个现有的客户互动应用实例](#new-data-existing)
+ [一个现有的财务和运营应用实例和一个新的客户互动应用实例](#existing-new)
+ [一个现有的财务和运营应用实例和一个现有的客户互动应用实例](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>一个新的财务和运营应用实例和一个新的客户互动应用实例

若要在一个无数据的新财务和运营应用实例与一个新的 Customer Engagement 应用实例之间设置双写入连接，请按照[从 Lifecycle Services 设置双写入](lcs-setup.md)中的步骤操作。 完成连接设置之后，将自动执行以下操作：

- 预配新的空财务和运营环境。
- 预配一个新的空 Customer Engagement 应用实例，其中已安装了 CRM 主解决方案。
- 为 DAT 公司数据建立双写入连接。
- 为实时同步启用表映射。

然后，这两个环境准备好了进行实时数据同步。

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>一个新的财务和运营应用实例和一个现有的客户互动应用实例

若要在一个无数据的新财务和运营应用实例与一个现有的客户互动应用实例之间设置双写入连接，请按照[从 Lifecycle Services 设置双写入](lcs-setup.md)中的步骤操作。 完成连接设置之后，将自动执行以下操作：

- 预配新的空财务和运营环境。
- 为 DAT 公司数据建立双写入连接。
- 为实时同步启用表映射。

然后，这两个环境准备好了进行实时数据同步。

若要将现有 Dataverse 数据同步到财务和运营应用，请执行以下步骤。

1. 在财务和运营应用中创建新公司。
2. 将该公司添加到双写入连接设置。
3. 通过使用三个字母的国际标准化组织 (ISO) 公司代码[引导](bootstrap-company-data.md) Dataverse 数据。
4. 对要同步其数据的表运行 **初始同步** 功能。

有关示例和备用方法的链接，请参阅本文后面的[示例](#example)一节。

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>一个具有数据的新财务和运营应用实例和一个新的客户互动应用实例

若要在一个具有数据的新财务和运营应用实例与一个新的客户互动应用实例之间设置双写入连接，请按照本文前面的[一个新的财务和运营应用实例和一个新的客户互动应用实例](#new-new)一节中的步骤操作。 完成连接设置后，如果要将数据同步到 Customer Engagement 应用，请按照以下步骤操作。

1. 从 LCS 页面打开财务和运营应用，然后转到 **数据管理 \> 双写入**。
2. 对要同步其数据的表运行 **初始同步** 功能。

有关示例和备用方法的链接，请参阅[示例](#example)部分。

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>一个具有数据的新财务和运营应用实例和一个现有的客户互动应用实例

若要在一个具有数据的新财务和运营应用实例与一个现有的客户互动应用实例之间设置双写入连接，请按照本文前面的[一个新的财务和运营应用实例和一个现有的客户互动应用实例](#new-existing)一节中的步骤操作。 完成连接设置后，如果要将数据同步到 Customer Engagement 应用，请按照以下步骤操作。

1. 从 LCS 页面打开财务和运营应用，然后转到 **数据管理 \> 双写入**。
2. 对要同步其数据的表运行 **初始同步** 功能。

若要将现有 Dataverse 数据同步到财务和运营应用，请执行以下步骤。

1. 在财务和运营应用中创建新公司。
2. 将该公司添加到双写入连接设置。
3. 通过使用三个字母的 ISO 公司代码[引导](bootstrap-company-data.md) Dataverse 数据。
4. 对要同步其数据的表运行 **初始同步** 功能。

有关示例和备用方法的链接，请参阅[示例](#example)部分。

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>一个现有的财务和运营应用实例和一个新的客户互动应用实例

若要在一个现有的财务和运营应用实例与一个新的客户互动应用实例之间设置双写入连接，需要在财务和运营环境中进行。

1. [从财务和运营应用设置连接](enable-dual-write.md)。
2. 对要同步其数据的表运行 **初始同步** 功能。

有关示例和备用方法的链接，请参阅[示例](#example)部分。

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>一个现有的财务和运营应用实例和一个现有的客户互动应用实例

若要在一个现有的财务和运营应用实例与一个现有的客户互动应用实例之间设置双写入连接，需要在财务和运营环境中进行。

1. [从财务和运营应用设置连接](enable-dual-write.md)。
2. 若要将现有 Dataverse 数据同步到财务和运营应用，请使用三个字母的 ISO 公司代码[引导](bootstrap-company-data.md) Dataverse 数据。
3. 对要同步其数据的表运行 **初始同步** 功能。

有关示例和备用方法的链接，请参阅[示例](#example)部分。

## <a name="example"></a>示例

有关示例，请参见[启用客户 V3 到联系人的表映射](enable-entity-map.md#enable-table-map)

有关基于每个实体中必须运行初始同步的数据量的替代方法，请参阅[初始同步的注意事项](initial-sync-guidance.md)。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
