---
title: 商店中的客户管理
description: 本主题说明零售商如何在 Microsoft Dynamics 365 Commerce 中启用销售点 (POS) 客户管理功能。
author: gvrmohanreddy
ms.date: 12/10/2021
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
ms.openlocfilehash: 5a352ba479ca5e635ef521b99f31bd26d5d837ac
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687325"
---
# <a name="customer-management-in-stores"></a>商店中的客户管理

[!include [banner](includes/banner.md)]

本主题说明零售商如何在 Microsoft Dynamics 365 Commerce 中启用销售点 (POS) 客户管理功能。

店员必须可以在 POS 上创建和编辑客户记录，这一点很重要。 这样，他们可以捕获诸如电子邮件地址、电话号码和地址之类的客户信息的任何更新。 此信息对于下游系统（如市场营销）很有用，因为这些系统的有效性取决于其客户数据的准确性。

销售助理可以从两个 POS 入口点触发客户创建工作流。 他们可以选择一个映射到 **添加客户** 操作的按钮，或者他们可以在搜索结果页面上的应用栏中选择 **创建客户**。 在这两种情况下，**新客户** 对话框都会出现，销售助理可以在其中输入所需的客户详细信息，例如客户的姓名、电子邮件地址、电话号码、地址，以及与业务相关的任何其他信息。 可以使用与客户相关联的客户属性来捕获这些附加信息。 有关客户属性的更多信息，请参见[客户属性](dev-itpro/customer-attributes.md)。

销售助理还可以捕获备用电子邮件地址和电话号码。 此外，他们可以捕获关于通过这些备用电子邮件地址或电话号码中的任何一个来接收营销信息的客户偏好。 要启用此功能，零售商必须在 Commerce Headquarters 内的 **功能管理** 工作区（**系统管理 \> 工作区 \> 功能管理**）中开启 **捕获多个电子邮件和电话号码，并同意对这些联系人进行营销** 功能。

## <a name="default-customer-properties"></a>默认客户属性

零售商可以使用 Commerce Headquarters 中的 **所有商店** 页面（**Retail 和 Commerce \> 渠道 \> 商店**），以将默认客户与每个商店相关联。 然后，Commerce 将为默认客户定义的属性复制到创建的所有新客户记录中。 例如，**创建客户** 对话框会显示从与商店关联的默认客户继承的属性。 这些属性包括 **客户类型**、**客户组**、**收据选项**、**收据电子邮件**、**货币** 和 **语言**。 任何 **隶属关系**（客户组）也将从默认客户那里继承。 但是，**财务维度** 从与默认客户关联的客户组那里继承，而不是从默认客户本身继承。

> [!NOTE]
> 仅当未为新创建的客户提供收据电子邮件 ID 时，才会从默认客户复制 **收据电子邮件** 值。 这意味着，如果默认客户中存在收据电子邮件 ID，则从电子商务站点创建的所有客户都将获得相同的收据电子邮件 ID，因为没有用户界面可以从客户那里捕获收据电子邮件 ID。 我们建议您将商店的默认客户的 **收据电子邮件** 字段保留为空，仅在您有依赖于存在的收据电子邮件地址的业务流程时使用它。 

销售助理可以捕获客户的多个地址。 客户的姓名和电话号码是从与每个地址关联的联系信息中继承的。 客户记录的 **地址** 快速选项卡包括销售助理可以编辑的 **目的** 字段。 如果客户类型是 **人员**，则默认值为 **家庭**。 如果客户类型是 **组织**，则默认值为 **公司**。 此字段支持的其他值包括 **家庭**、**办公室** 和 **邮政信箱**。 地址中的 **国家/地区** 字段的值继承自 Commerce Headquarters 内 **运营单位** 页（**组织管理 \> 组织 \> 运营单位**）上指定的主要地址。



## <a name="additional-resources"></a>其他资源

[异步客户创建模式](async-customer-mode.md)

[将异步客户转换为同步客户](convert-async-to-sync.md)

[客户属性](dev-itpro/customer-attributes.md)

[脱机数据排除](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
