---
title: 安装、设置和更新客户门户
description: 本主题提供客户门户的许可详细信息和设置说明。
author: dasani-madipalli
manager: tfehr
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e61fc5f7151a0bb61d496d47f4ad4e727a2a1d65
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529522"
---
# <a name="install-set-up-and-update-the-customer-portal"></a>安装、设置和更新客户门户

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="licensing-requirements"></a>许可要求

要实施客户门户，您必须具有以下许可证：

- **Power Apps 门户** – 托管客户门户需要此许可证。 门户根据使用获得许可。 有关详细信息，请参阅 [Power Apps 门户许可要求](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals)。
- **双写入** – 您必须具有必要的许可证才能为 Supply Chain Management 启用双写入。 有关详细信息，请参阅[双写入的系统要求](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md)。

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a>双写入和 Power Apps 门户的依赖关系

客户门户依赖 Power Apps 门户和双写入，如下图所示。

![客户门户依赖关系](media/customer-portal-elements.png "客户门户依赖关系")

与 Supply Chain Management 的其他功能不同，客户门户模板位于 Power Apps 门户中。 因此，客户门户受 Power Apps 门户和采用双写入的实体提供的功能限制。

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a>启用客户门户需要设置

确定已有必需的许可证后，您可以按照[双写入初始同步说明](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md)所述设置双写入。

确保以双写入方式启用以下实体映射：

- 销售订单头
- 销售订单详细信息
- 科目
- 联系人
- 产品

完成此设置后，您可以预配客户门户模板。

## <a name="provision-the-customer-portal"></a>预配客户门户

开始之前，请确保您已经完成了[所需设置](#required-setup)。 然后按照以下步骤预配客户门户。

1. 转到 [make.powerapps.com](https://make.powerapps.com/)。
2. 确保您使用的是启用了双写入的环境。
3. 在 **创建** 选项卡上，向下滚动到 **从模板开始** 部分，然后选择名为 **客户门户** 的模板。
4. 按照屏幕上的说明操作。

预配完成后，您可以在 **主页** 页面 **我的应用** 部分访问客户门户。

> [!NOTE]
> 如果您使用的环境中未安装双写入解决方案，您会收到错误消息，客户门户不会预配。

## <a name="update-the-customer-portal"></a>更新客户门户

以后可能会向客户门户添加更多功能。 Microsoft 对基础解决方案组件所做的任何更改都将自动显示在您的环境中。 但是，在您的环境中预配的网站不会自动反映对配置数据所作的更改。 您必须通过从新模板获取代码并将其与预配的网站合并来手动应用这些更改。

## <a name="additional-resources"></a>其他资源

要了解如何设置和自定义客户门户，您应该先查看以下有关基础技术的文档：

- [Power Apps 门户文档](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [双写入文档](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

为了有效地管理门户，您必须了解 Power Apps 门户和 Common Data Service 生命周期。 有关详细信息，请参阅以下资源：

- [关于门户生命周期](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [升级门户](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [迁移门户配置](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [解决方案生命周期管理：Dynamics 365 for Customer Engagement 应用](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]