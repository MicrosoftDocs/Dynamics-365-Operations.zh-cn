---
title: 创建和管理客户门户用户
description: 本主题说明如何创建客户门户用户帐户并为其设置权限。
author: dasani-madipalli
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b63ebae10f23a27115313acb6381fa176e64fbd6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261061"
---
# <a name="create-and-manage-customer-portal-users"></a>创建和管理客户门户用户

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

在现成的实现中，用户无法自助注册使用客户门户创建的网站。 要登录和使用网站，必须由管理员邀请用户。Microsoft 有意阻止了用户自助注册的能力。

必须先为用户创建联系人记录，该用户才可以使用网站。 此记录指示用户属于哪个客户帐户和法人。 此信息对于确保用户可以创建和查看销售订单至关重要。

用户自助注册时，将自动为其创建联系人记录。 因此，您无法确保用户选择正确的客户帐户和法人。 另一方面，邀请流程允许管理员在邀请发送之前将正确的客户帐户和法人分配给联系人记录。 如果您正在考虑自定义解决方案以使用户可以自助注册，请务必考虑可能的后果。

## <a name="video"></a>视频
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ADkI]

[邀请客户注册和使用您的客户门户](https://youtu.be/drGUYHX9QIQ)视频（上方所示）包括在 YouTube 上提供的 [Finance and Operations 播放列表](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)中。

## <a name="prerequisite-setup"></a>先决条件设置

Power Apps 门户中的联系人作为记录存储在 Microsoft Dataverse 中的 **联系人** 表中。 然后双写入根据需要将这些记录同步到 Microsoft Dynamics 365 Supply Chain Management。

![客户门户联系人的系统图](media/customer-portal-contacts.png "客户门户联系人的系统图")

在开始邀请新客户之前，请确保以双写入形式启用了 **联系人** 表映射。

## <a name="the-invitation-process"></a>邀请流程

要将现有联系人邀请到客户门户，请按照 Power Apps 门户文档中的[向门户邀请联系人](https://docs.microsoft.com/powerapps/maker/portals/configure/invite-contacts)中的步骤操作。

在邀请客户加入客户门户之前，请确保客户的[联系人记录](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts)已通过以下方式提供并设置：

1. 将 **公司** 字段设置为您希望客户在 Supply Chain Management 中所属的法人。
2. 将 **帐号** 字段设置为您希望用户在 Supply Chain Management 中拥有的客户帐号。

联系人创建后，您应该可以在 Supply Chain Management 中看到它。

有关详细信息，请参阅 Power Apps 门户文档中的[配置要在门户上使用的联系人](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts)。

## <a name="out-of-box-web-roles-and-table-permissions"></a>现成的 Web 角色和表权限

Power Apps 门户中的用户角色由 [Web 角色](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles)和[表权限](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions)定义。 为客户门户定义了一些现成角色。 您可以创建新角色，并可以修改或删除现有角色。

### <a name="out-of-box-web-roles"></a>现成的 Web 角色

本节介绍随客户门户提供的 Web 角色。

有关如何修改现成的用户角色的详细信息，请参阅 Power Apps 门户文档中的[为门户创建 Web 角色](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles)和[使用门户的表权限添加基于记录的安全性](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions)。

#### <a name="administrator"></a>管理员

管理员负责监管和维护网站。 此人将预配和设置客户门户。 管理员维护门户的 IT 和安全性，并确保一切顺利进行。 管理员还可以通过添加新功能、创建新角色等来自定义和/或更改门户。

#### <a name="customer-representative"></a>客户代表

客户代表为客户公司工作，负责管理公司下的订单。 客户代表可以查看已为公司下达的所有订单以及下达订单的用户。 此外，客户代表还可以查看有关整个客户的信息，以及哪些联系人可以代表该客户下订单。

#### <a name="authorized-users"></a>授权用户

授权用户可以下订单和查看所下订单的状态。 但是，他们无法查看公司中其他用户所下订单的状态。

#### <a name="unauthorized-users"></a>未授权用户

未授权用户无法查看任何数据。 他们只能查看公共信息，如条款和条件，以及有关运行客户门户的公司的详细信息。

#### <a name="example"></a>示例

下表显示了每个 Web 角色的用户可以在系统中查看的销售订单。

| 销售订单 | 管理员 | 客户&nbsp;X 的客户代表 | 授权用户：Jane | 授权用户：Sam | 未授权用户：May |
|---|---|---|---|---|---|
| 客户&nbsp;X 订货人：Jane&nbsp; | 是 | 是 | 是 | 无 | 无 |
| 客户&nbsp;X 订货人：Sam&nbsp; | 是 | 是 | 无 | 是 | 无 |
| 客户&nbsp;Y 订货人：May&nbsp; | 是 | 无 | 无 | 无 | 无 |

> [!NOTE]
> 即使 Sam 和 Jane 都是为客户 X 工作的联系人，他们也只能查看他们自己下的订单，而看不到其他信息。 尽管 May 在系统中有一个订单，但由于她是未授权用户，因此她无法在客户门户中查看该订单。 （而且，她一定是通过客户门户以外的某个渠道下的订单。）


[!INCLUDE[footer-include](../../includes/footer-banner.md)]