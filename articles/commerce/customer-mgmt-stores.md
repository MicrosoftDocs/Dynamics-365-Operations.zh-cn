---
title: 商店中的客户管理
description: 本主题说明零售商如何在 Microsoft Dynamics 365 Commerce 中启用销售点 (POS) 客户管理功能。
author: josaw1
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e43f8f5b91f729dc93eccb9e9e4ee21b5a5d1596
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019979"
---
# <a name="customer-management-in-stores"></a>商店中的客户管理

[!include [banner](includes/banner.md)]

本主题说明零售商如何在 Microsoft Dynamics 365 Commerce 中启用销售点 (POS) 客户管理功能。

店员必须可以在 POS 上创建和编辑客户记录，这一点很重要。 这样，他们可以捕获诸如电子邮件地址、电话号码和地址之类的客户信息的任何更新。 此信息对于下游系统（如市场营销）很有用，因为这些系统的有效性取决于其客户数据的准确性。

销售助理可以从两个 POS 入口点触发客户创建工作流。 他们可以选择一个映射到 **添加客户** 操作的按钮，或者他们可以在搜索结果页面上的应用栏中选择 **创建客户**。 在这两种情况下，**新客户** 对话框都会出现，销售助理可以在其中输入所需的客户详细信息，例如客户的姓名、电子邮件地址、电话号码、地址，以及与业务相关的任何其他信息。 可以使用与客户相关联的客户属性来捕获这些附加信息。 有关客户属性的更多信息，请参见[客户属性](dev-itpro/customer-attributes.md)。

销售助理还可以捕获备用电子邮件地址和电话号码。 此外，他们可以捕获关于通过这些备用电子邮件地址或电话号码中的任何一个来接收营销信息的客户偏好。 要启用此功能，零售商必须在 Commerce Headquarters 内的 **功能管理** 工作区（**系统管理 \> 工作区 \> 功能管理**）中开启 **捕获多个电子邮件和电话号码，并同意对这些联系人进行营销** 功能。

## <a name="default-customer-properties"></a>默认客户属性

零售商可以使用 Commerce Headquarters 中的 **所有商店** 页面（**Retail 和 Commerce \> 渠道 \> 商店**），以将默认客户与每个商店相关联。 然后，Commerce 将为默认客户定义的属性复制到创建的所有新客户记录中。 例如，**创建客户** 对话框会显示从与商店关联的默认客户继承的属性。 这些属性包括客户类型、客户组、收据首选项、货币和语言。 任何隶属关系（客户组）也将从默认客户那里继承。 但是，财务维度从与默认客户关联的客户组那里继承，而不是从默认客户本身继承。

销售助理可以捕获客户的多个地址。 客户的姓名和电话号码是从与每个地址关联的联系信息中继承的。 客户记录的 **地址** 快速选项卡包括销售助理可以编辑的 **目的** 字段。 如果客户类型是 **人员**，则默认值为 **家庭**。 如果客户类型是 **组织**，则默认值为 **公司**。 此字段支持的其他值包括 **家庭**、**办公室** 和 **邮政信箱**。 地址中的 **国家/地区** 字段的值继承自 Commerce Headquarters 内 **运营单位** 页（**组织管理 \> 组织 \> 运营单位**）上指定的主要地址。

## <a name="sync-customers-and-async-customers"></a>同步客户和异步客户

在 Commerce 中，有两种客户创建模式：同步和异步。 默认情况下，系统会同步创建客户。 换句话说，客户是在 Commerce Headquarters 中实时创建的。 同步客户创建模式很有用，因为可以跨渠道立即搜索新客户。 但是，它也有一个缺点。 因为它会向 Commerce Headquarters 发出 [Commerce Data Exchange：实时服务](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service)请求，如果同时发出许多客户创建请求，则性能可能会受到影响。

如果在商店的功能配置文件（**Retail 和 Commerce \> 渠道设置 \> 在线商店设置 \> 功能配置文件**）中将 **以异步模式创建客户** 选项设置为 **是**，则实时服务请求不会用于在渠道数据库中创建客户记录。 异步客户创建模式不会影响 Commerce Headquarters 的性能。 临时全局唯一标识符 (GUID) 会分配给每个新的异步客户记录，并用作客户帐户 ID。 该 GUID 不会显示给 POS 用户。 相反，这些用户看到的客户帐户 ID 为 **待同步**。 尽管此配置会强制异步创建客户，但是请注意，对客户记录所做的编辑始终会同步完成。

### <a name="convert-async-customers-to-sync-customers"></a>将异步客户转换为同步客户

要将异步客户转换为同步客户，必须首先运行 P 作业将异步客户发送到 Commerce Headquarters。 然后运行 **从异步模式同步客户和业务合作伙伴** 作业，以创建客户帐户 ID。 最后，运行 **1010** 作业，以将新客户帐户 ID 同步到渠道。

### <a name="async-customer-limitations"></a>异步客户限制

异步客户功能当前具有以下限制：

- 除非已在 Commerce Headquarters 中创建了客户，并且新客户帐户 ID 已被重新同步到渠道，否则无法编辑异步客户记录。
- 隶属关系不能与异步客户关联。 因此，新的异步客户不会继承默认客户的隶属关系。
- 除非新客户帐户 ID 已被重新同步到渠道，否则不能将会员卡发给异步客户。
- 无法对异步客户捕获备用电子邮件地址和电话号码。

### <a name="customer-creation-in-pos-offline-mode"></a>在 POS 脱机模式下创建客户

如果在启用异步客户创建模式时 POS 脱机，则会异步创建新客户记录。 如果在禁用异步客户创建模式时 POS 脱机，系统将自动切换到异步客户创建模式。 换句话说，即使禁用了异步客户创建模式，也可能会异步创建客户记录。 因此，Commerce Headquarters 管理员必须为 P 作业、**从异步模式同步客户和业务合作伙伴** 作业和 **1010** 作业创建并计划一个重复执行的批处理作业，以便在 Commerce Headquarters 中将任何异步客户转换为同步客户。

> [!NOTE]
> 如果在 **商业渠道架构** 页（**Retail 和 Commerce \> Headquarters 设置 \> 商业调度 \> 渠道数据库组**）上将 **筛选共享的客户数据表** 选项设置为 **是**，则不会在 POS 联机模式下创建客户记录。 有关详细信息，请参阅[脱机数据排除](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)。

## <a name="additional-resources"></a>其他资源

[客户属性](dev-itpro/customer-attributes.md)

[脱机数据排除](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
