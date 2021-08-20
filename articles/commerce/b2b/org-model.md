---
title: 为 B2B 组织创建组织建模层次结构
description: 本主题介绍如何为企业到企业 (B2B) 组织创建组织建模层次结构。
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0602e0f4e36beda06f47314f40b59967272469755d1b9959432e86f407c098e7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738069"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a>为 B2B 组织创建组织建模层次结构

[!include [banner](../../includes/banner.md)]

本主题介绍如何在 Microsoft Dynamics 365 Commerce 中为企业到企业 (B2B) 组织创建组织建模层次结构。

在 Commerce headquarters 中，业务合作伙伴组织由客户和客户层次结构实体表示。 业务合作伙伴组织及其用户表示为客户，客户层次结构用于将这些客户彼此关联。

批准加入 B2B 电子商务站点的业务合作伙伴请求后，将执行以下操作：

- 在系统中创建两个新的客户记录：业务合作伙伴组织的 **组织类型** 客户记录和请求者（即提交请求的业务合作伙伴用户）的 **个人类型** 客户记录。
- 在 **客户 \> 客户层次结构** 下创建新的客户层次结构记录。 此记录具有以下标头属性：

    - **客户层次结构 ID** – 客户层次结构的唯一 ID。 此 ID 使用在 Commerce headquarters 中的 Commerce 共享参数中定义的编号规则。
    - **名称** – 加入请求中指定的业务合作伙伴的组织名称。
    - **目的** – 此属性设置为预定义值 **B2B 组织**。
    - **组织** – 业务合作伙伴的客户 ID。

以下是客户层次结构记录的详细信息：

- 请求者的客户记录与客户层次结构相关联。
- 管理员角色与请求者关联。

当管理员将更多用户添加到 B2B 站点上的业务合作伙伴组织时，将在 Commerce headquarters 中为每个用户创建新的客户记录。 此客户记录也将被添加到业务合作伙伴的相关客户层次结构记录中，具有“用户”的角色。

> [!NOTE]
> 在大多数情况下，层次结构中所有客户记录的相应属性值应是匹配的。 例如，由于所有业务合作伙伴用户都应该获得相似的产品价格，因此他们的价格组和关联的配置应该是匹配的。 但是，系统不强制要求此一致性。 因此，相关的 Commerce headquarters 用户负责确保属性值和配置与给定层次结构中的所有客户匹配。

Commerce headquarters 用户可以并排查看层次结构中所有客户记录的属性值。 通过选择下拉菜单上中选项卡名称，选择相关的客户记录属性。 用户可以从此视图直接查看和编辑属性值。 或者，如果您要将管理员客户记录中的所有值应用于所有用户客户记录，选择客户层次结构详细信息中的 **替代**。

## <a name="additional-resources"></a>其他资源

[建立 B2B 电子商务站点](set-up-b2b-site.md)

[在 B2B 电子商务站点上管理业务合作伙伴用户](manage-b2b-users.md)

[配置 B2B 电子商务站点的客户帐户付款方式](payment-method.md)

[设置 B2B 电子商务站点的产品数量限制](quantity-limits.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]