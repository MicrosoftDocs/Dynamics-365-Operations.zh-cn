---
title: 异步客户创建模式
description: 本文介绍 Microsoft Dynamics 365 Commerce 中的异步客户创建模式。
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 4ca63fe06a804035e976a3432454078c1cca0020
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880132"
---
# <a name="asynchronous-customer-creation-mode"></a>异步客户创建模式

[!include [banner](includes/banner.md)]

本文介绍 Microsoft Dynamics 365 Commerce 中的异步客户创建模式。

在 Commerce 中，有两种客户创建模式：同步和异步。 默认情况下，系统会同步创建客户。 换句话说，客户是在 Commerce Headquarters 中实时创建的。 同步客户创建模式很有用，因为可以跨渠道立即搜索新客户。 但是，它也有一个缺点。 因为它会向 Commerce Headquarters 发出 [Commerce Data Exchange：实时服务](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service)请求，如果同时发出许多客户创建请求，则性能可能会受到影响。

如果在商店的功能配置文件（**Retail 和 Commerce \> 渠道设置 \> 在线商店设置 \> 功能配置文件**）中将 **以异步模式创建客户** 选项设置为 **是**，则实时服务请求不会用于在渠道数据库中创建客户记录。 异步客户创建模式不会影响 Commerce Headquarters 的性能。 临时全局唯一标识符 (GUID) 会分配给每个新的异步客户记录，并用作客户帐户 ID。 该 GUID 不会显示给销售点 (POS) 用户。 相反，这些用户看到的客户帐户 ID 为 **待同步**。

> [!IMPORTANT]
> 只要 POS 脱机，系统都将自动异步创建客户，即使禁用了异步客户创建模式也不例外。 因此，无论您在同步客户创建与异步客户创建之间作何选择，Commerce Headquarters 管理员都必须为 **P 作业**、**从异步模式同步客户和业务合作伙伴** 作业（以前称为 **从异步模式同步客户和业务合作伙伴**）和 **1010** 作业创建和计划定期批处理作业，以便在 Commerce Headquarters 中将所有异步客户转换为同步客户。

## <a name="async-customer-limitations"></a>异步客户限制

异步客户功能当前具有以下限制：

- 除非已在 Commerce Headquarters 中创建了客户，并且新客户帐户 ID 已被重新同步到渠道，否则无法编辑异步客户记录。
- 除非新客户帐户 ID 已被重新同步到渠道，否则不能将会员卡发给异步客户。

## <a name="async-customer-enhancements"></a>异步客户增强

从 Commerce 版本 10.0.24 版本开始，您可以在 **功能管理** 工作区中启用 **启用增强的异步客户创建** 功能。 此功能通过以下方式弥合了 POS 和电子商务中异步和同步客户创建模式之间的差距：

- 隶属关系不能与异步客户关联。
- 职务可添加到异步客户。
- 无法对异步客户捕获备用电子邮件地址和电话号码。

从 Commerce 版本 10.0.22 版本开始，您可以在 **功能管理** 工作区中启用 **启用客户地址异步创建** 功能。 此功能支持为同步客户和异步客户异步保存新创建的客户地址。

启用前面提到的功能后，您必须为 **P 作业**、**从异步模式同步客户和业务合作伙伴** 作业和 **1010** 作业计划一个重复执行的批处理作业，以便在 Commerce Headquarters 中将任何异步客户转换为同步客户。

### <a name="customer-creation-in-pos-offline-mode"></a>在 POS 脱机模式下创建客户

正如前面提到的，只要 POS 脱机，系统都将自动异步创建客户，即使禁用了异步客户创建模式也不例外。 因此，Commerce Headquarters 管理员必须为 **P 作业**、**从异步模式同步客户和业务合作伙伴** 作业和 **1010** 作业创建并计划一个重复执行的批处理作业，以便在 Commerce Headquarters 中将任何异步客户转换为同步客户。

> [!NOTE]
> 如果在 **商业渠道架构** 页（**Retail 和 Commerce \> Headquarters 设置 \> 商业调度 \> 渠道数据库组**）上将 **筛选共享的客户数据表** 选项设置为 **是**，则不会在 POS 联机模式下创建客户记录。 有关详细信息，请参阅[脱机数据排除](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)。

## <a name="additional-resources"></a>其他资源

[商店中的客户管理](customer-mgmt-stores.md)

[将异步客户转换为同步客户](convert-async-to-sync.md)

[客户属性](dev-itpro/customer-attributes.md)

[脱机数据排除](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
