---
title: 使用客户层次结构管理 B2B 业务合作伙伴
description: 本主题介绍如何使用客户层次结构来管理 Microsoft Dynamics 365 Commerce 企业到企业 (B2B) 电子商务网站的业务合作伙伴。
author: josaw1
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d6e594cbb824a8b823912118e99b819585adc45e
ms.sourcegitcommit: 8bcb9c13eccb14e61c39ca6578d135b64090fad2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2022
ms.locfileid: "8313825"
---
# <a name="manage-b2b-business-partners-using-customer-hierarchies"></a>使用客户层次结构管理 B2B 业务合作伙伴

[!include [banner](../../includes/banner.md)]

本主题介绍如何使用客户层次结构来管理 Microsoft Dynamics 365 Commerce 企业到企业 (B2B) 电子商务网站的业务合作伙伴。

在 Commerce Headquarters 中，*客户层次结构* 实体用于代表将使用您的 B2B 电子商务站点的业务合作伙伴组织。 在开始使用客户层次结构管理业务合作伙伴之前，您必须在 Commerce headquarters 中启用 B2B 电子商务功能，然后为客户层次结构定义编号规则。

## <a name="enable-the-b2b-e-commerce-feature-in-commerce-headquarters"></a>在 Commerce headquarters 中启用 B2B 电子商务功能

要使用 B2B 电子商务功能，您必须首先在 Commerce Headquarters 中启用 **启用 B2B 电子商务功能** 功能。

1. 转到 **工作区 \> 功能管理**。
1. 在 **全部** 选项卡上，使用筛选框搜索 **模块：Retail 和 Commerce**。
1. 找到 **启用 B2B 电子商务功能** 功能，选择它，然后选择右下角的 **立即启用**。

## <a name="define-a-number-sequence-for-the-customer-hierarchy"></a>定义客户层次结构的编号规则

编号规则用于为需要标识符的主数据记录和交易记录生成可读的唯一标识符。 您必须定义将用于为客户层次结构生成 ID 的编号规则。 有关编号规则的详细信息，请参阅[编号规则概览](/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview)。

要在 Commerce Headquarters 中定义客户层次结构的编号规则，请按照下列步骤操作。

1. 转到 **Retail 和 Commerce \> Headquarters 设置 \> 编号规则 \> 编号规则**。
1. 创建一个新的编号规则，或选择一个现有的编号规则重复使用它。
1. 转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数 \> Commerce 共享参数**。
1. 在 **编号规则** 选项卡上，将您之前创建或选择的编号规则添加到 **客户层次结构 ID** 引用。

![添加到客户层次结构 ID 引用的编号规则。](../media/NumberSequenceCustHierarchy.png)

## <a name="how-the-approval-process-works"></a>审批流程如何工作

当业务合作伙伴请求加入 B2B 电子商务站点时，系统会将请求保存为 *目标客户*。 Commerce Headquarters 角色（如零售运营经理）可以批准或拒绝合作伙伴请求。 有关如何管理业务合作伙伴请求和目标客户审批的详细信息，请参阅[在 B2B 电子商务网站上管理业务合作伙伴用户](manage-b2b-users.md)。

当目标客户获得批准时，系统会创建两个新的客户记录：

- 一个 **组织** 类型的客户记录代表请求成为业务合作伙伴的组织。
- 一个 **个人** 类型的客户记录代表提交请求的人员。

此外，将在 **Retail 和 Commerce \> 客户 \> 客户层次结构** 创建新的客户层次结构记录。 此客户层次结构记录具有以下属性：

- **客户层次结构 ID** – 客户层次结构的唯一 ID。 此 ID 使用您在 Commerce 共享参数中定义的编号规则。
- **名称** – 加入请求中指定的业务合作伙伴的组织名称。 此字段是可编辑的。
- **目的** – 此属性设置为预定义值 **B2B 组织**。
- **组织** – 业务合作伙伴组织的客户 ID。

提交加入请求的人员将被添加到 **层次结构** 快速选项卡，并为他们分配 **管理员** 角色。 当管理员将更多用户添加到 B2B 站点上的业务合作伙伴组织时，将为每个用户创建新的客户记录。 客户记录也将被添加到业务合作伙伴的相关客户层次结构记录中，并被分配 **用户** 角色。

### <a name="examples"></a>示例

姓名为 Sam J. 的人员代表 Microsoft 组织提交加入请求。 请求获得批准后，将创建两个新客户帐户：一个是为 Sam J. 创建的 **个人** 类型，一个是为 Microsoft 创建的 **组织** 类型。

如下图中的示例所示，还将创建一个新的客户层次结构记录。 此记录与组织 (**Microsoft**) 同名，将向 Sam J. 分配 **管理员** 角色。作为管理员，Sam J. 将 B2B 站点的任何其他 Microsoft 用户添加到此层次结构中，并将 **用户** 分配给他们。 在此示例中，Sush R. 被添加为用户。

![客户层次结构记录的示例。](../media/CustomerHierarchy2.png)

要确定客户是否与客户层次结构关联，打开客户记录。 如下图中的示例所示，**零售** 快速选项卡 **B2B** 部分的 **客户层次结构 ID** 字段显示客户是否属于某个客户层次结构，**B2B 管理员** 选项指示客户是否是该层次结构的管理员。

![客户记录的“零售”快速选项卡上的 B2B 部分示例，其中客户与层次结构相关联，被指定为管理员。](../media/CustomerHierarchyMapping2.png)

在大多数情况下，层次结构中所有客户记录的属性值应是匹配的。 例如，由于所有业务合作伙伴用户都应该获得相似的产品价格，因此他们的价格组和关联的配置应该是匹配的。 但是，系统不强制要求此一致性。 因此，相关的 Commerce headquarters 用户负责确保属性值和配置与给定层次结构中的所有客户匹配。

Commerce headquarters 用户可以并排检查层次结构中所有客户记录的属性值。 如下图示例所示，您可以使用 **层次结构** 快速选项卡上下拉列表中的 **常规** 选项，然后选择客户记录的任何部分以显示相关属性。 用户可以直接在此视图中编辑属性值。 要将管理员客户记录中的所有值复制到所有用户，在 **层次结构** 快速选项卡上选择 **替代**。

![客户层次结构记录示例，显示“替代”按钮和下拉列表中的选项。](../media/HierarchyDetails2.png)

[!include [footer-include](../../includes/footer-banner.md)]
