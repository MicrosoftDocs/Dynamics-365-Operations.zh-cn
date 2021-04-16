---
title: 当事方和全球通讯簿
description: 本主题介绍双重写入的当事方和全球通讯簿功能。
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: e7bec58f8094a1448017822e7d8840368cc482b8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750780"
---
# <a name="party-and-global-address-book"></a>当事方和全球通讯簿

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

当事方和全球通讯簿是 Finance and Operations 应用程序中的概念。 当事方可以是组织或个人。 在全球范围内存储和管理 **当事方** 的属性（例如姓名、语言、联系人和地址）非常方便。 当某个属性值在一个地方更改时，它将反映在涉及 **当事方** 的所有地方中。

## <a name="party"></a>当事方

*当事方* 是企业中涉及的个人或组织。 通过使用“当事方”概念，个人或组织可以在企业中扮演多个角色（工作人员、客户、供应商或联系人）。 该角色基于环境和目的。 下面是来自两个虚拟公司（Contoso 和 Fabrikam）的一些示例。

+ **工作人员**：员工。 例如，Contoso 的员工。
+ **供应商**：为企业提供商品或服务的供应商组织或独立经营者。 例如，如果 Fabrikam 向 Contoso 出售供应品，则 Fabrikam 充当供应商角色。
+ **联系人**：要联系的人员。 例如，如果 Contoso 从 Fabrikam 购买供应品，则 Contoso 的员工将与 Fabrikam 的联系人联系。
+ **客户**：客户是指从公司购买商品的个人或公司。 例如，如果 Contoso 从 Fabrikam 购买供应品，则 Contoso 是 Fabrikam 的客户。

当事方模型通常用于表示组织和个人之间中等到复杂的关系，特别是在当事方扮演多个角色时。 下面是一些常见示例：

+ 当事方可以是客户，也可以是供应商。 例如，在北美，Fabrikam 向 Contoso 出售电线，并从 Contoso 购买装配后的扬声器。 在欧洲，Fabrikam 向 Contoso 出售零件，但没有从 Contoso 购买任何商品。
+ 当事方可以是员工，也可以是客户。 例如，Contoso 的员工从 Contoso 购买电子产品供个人使用。
+ 个人和组织之间可能存在多对多关系。 例如，Fabrikam 向服务专家提供服务并雇用安置协调员。 协调员针对一些 Fabrikam 客户的工作请求匹配服务专家。 Contoso 是客户帐户之一。 当 Contoso 需要专家时，Contoso 与协调员联系，然后由协调员进行请求。 协调员处理所有客户的请求，从而建立多对多关系。

下图显示了当事方的数据模型：

![当事方的数据模型](media/party-gab-image1.png)

> [!Tip]
> 当您尝试创建新的帐户记录时，请使用“当事方”字段按名称搜索记录。 如果找到记录，则只需选择该记录。 系统将自动填充当事方中的所有数据。 您无需手动输入所有必填字段。 可以在现成的“帐户”、“联系人”和“供应商”窗体上找到此行为。

双重写入并非支持 Finance and Operations 应用的所有当事方角色。 有关当事方角色的完整列表，请参阅[全球通讯簿概览](../../../fin-ops/organization-administration/overview-global-address-book.md)。

### <a name="global-address-book"></a>全球通讯簿

全球通讯簿是参与企业的组织和个人的邮寄地址和电子地址的目录。

全球通讯簿根据需要存储和处理尽可能多的邮寄地址和电子地址。 例如，假设 Fabrikam 在 50 个地点设有加油站。 每个地点都有不同的邮寄地址、电子邮件和电话号码。 所有企业采购都向主要加油站计费，但采购会直接运送到请求采购的特定加油站。 全球通讯簿将主要加油站存储为帐单地址，将每个加油站存储为 Fabrikam 的装运地址。 这些地址可以存储一次，并可以根据需要获取报价单和订单。

根据企业环境，个人或组织可以扮演多个角色。 当扮演多个角色时，其邮寄地址和电子地址可能相同。 在这种情况下，一个角色的地址更改也应该体现在其他角色上，反之亦然。 全球通讯簿在全球范围内存储和处理地址。

![全球通讯簿的数据模型](media/party-gab-image2.png)

## <a name="contacts"></a>联系人

在 Customer Engagement 应用中，*联系人* 是个人。 但是，已重载 **联系人** 表以表示个人、门户用户、B2C 客户或供应商。 该表示形式是隐式的，您必须先调查相关交易才能分辨差异。 **联系人** 表已限制为与 **帐户** 表具有 1:1 关系。 作为当事方和全球通讯簿模型的一部分，双重写入为分类引入显式属性，并且双重写入允许 **联系人** 个人和组织（帐户实体或供应商实体）之间的 N:N 关系。

有两种类型的 **联系人** 行：

+ 出售联系人 – **公司** 字段中具有必填值的联系人行。
+ 非出售联系人 – **公司** 字段为空的联系人行。

**联系人** 表可以存储这些类型的行：

行类型 | 说明
---|---
作为客户的个人，例如可出售联系人或 B2C 客户。 | **公司** 字段不为空并且 **是客户** 字段设置为 **是** 的出售联系人记录。
作为供应商的个人，例如诸如供应商的独立经营者。 | **公司** 字段不为空并且 **是供应商** 字段设置为 **是** 的出售联系人记录。
既是客户又是供应商的个人。 | **公司** 字段不为空，**是客户** 字段设置为 **是** 并且 **是供应商** 字段设置为 **是** 的出售联系人记录。 个人既可以是一个产品的生产者，也可以是另一个产品的消费者。 Finance and Operations 应用和双重写入支持此关系。
作为组织联系人的个人不能是客户，也不能是供应商。 | **公司** 字段为空，**是客户** 字段设置为 **否** 并且 **是供应商** 字段设置为 **否** 的非出售联系人记录。

## <a name="contact-for-party"></a>当事方的联系人

**当事方的联系人** 在 **帐户** 行和 **联系人** 行之间存储和处理 N:N 关系。 它可以从非出售行中筛选出售 **联系人** 行，并仅将非出售 **联系人** 行关联到 **帐户** 或 **供应商** 行。

例如，Natasha Jones 和 Miguel Reyes 是当地的兽医，负责照料农场。 Natasha 负责西雅图地区，而 Miguel 负责肯特地区。 在 Customer Engagement 应用中，农场表示为客户，而兽医则是联系人。 Natasha 的一个 **联系人** 记录将与 Natasha 合作的所有农场相关联。 类似地，Miguel 的一个 **联系人** 记录将与 Miguel 合作的所有农场相关联。

这些关系存储在 **当事方的联系人** 表中。 您可以在现成的窗体中找到信息：

+ 当您在 **帐户** 窗体中时，有一个名为 **关联的联系人** 的选项卡。 使用此选项卡将一个或多个联系人关联到 **帐户** 行。 在此窗体上，您将为组织分配联系人。 分配联系人后，您可以选择一个联系人作为该帐户的主要联系人。 使用 **快速创建** 窗体，您仅可以选择一个联系人。 此行为与使用 **供应商** 窗体时相同，记录类型为 **组织**。
+ 当您在 **联系人** 窗体中，并且该行是客户或供应商或二者（出售联系人）时，有一个名为 **关联的联系人** 的选项卡。 使用此选项卡关联一个或多个联系人。 在此窗体上，您将为 B2C 客户或供应商分配联系人。 分配联系人后，您可以选择一个联系人作为主要联系人。 使用 **快速创建** 窗体，您仅可以选择一个联系人。
+ 当您在 **联系人** 窗体中，并且该行是联系人（非出售联系人）时，有一个名为 **关联的组织** 的选项卡。 使用此选项卡关联一个或多个客户或供应商。 在此窗体上，您将为基础联系人分配客户或供应商。 客户或供应商可以是组织、个人或二者均可。 在给定的时间，您仅可以从四个字段中选择一个值。

    ![“关联的组织”选项卡](media/party-gab-image3.png)

    + 如果您选择 **当事方 ID**，基础联系人将分配给所选当事方的所有角色。
    + 如果您选择 **关联的联系人**，您将选择属于个人类型的出售联系人。
    + 如果您选择 **关联的帐户** 或 **供应商**，您将选择组织。

    无论您的选择如何，将在当事方级别创建关联，并该关联适用于当事方的所有角色并此处在“当事方的联系人”实体中。

> [!Note]
> Customer Engagement 应用中 **当事方的联系人** 表的显示名称是 **客户/供应商的联系人**。

当您打开 **是客户** 为 **否** 且 **是供应商** 为 **否** 的 **联系人** 行时，将看到 **关联的组织** 选项卡。使用此选项卡将一个或多个客户或供应商组织关联到联系人。

当您打开 **是客户** 为 **是** 或 **是供应商** 为 **是** 的 **联系人** 行时，将看到 **关联的联系人** 选项卡。使用此选项卡关联一个或多个联系人。

## <a name="postal-address"></a>邮寄地址

已在 **帐户**、**联系人** 和 **供应商** 窗体上引入了名为 **地址** 的新选项卡。 使用网格支持 N 个地址的 **地址**，如下图所示：

![邮寄地址的网格](media/party-gab-image4.png)

+ **邮寄地址角色** 列可列出地址的用途。
+ **是主要** 列可列出主要地址。
+ **地址编号** 列可列出地址顺序。
+ **+ 新建地址** 按钮允许您创建新地址。 您可以根据需要创建任意多的地址。

**帐户** 窗体的 **摘要** 选项卡上的 **地址 1** 和 **地址 2** 字段分别对应于 **交货** 和 **发票** 地址。

![邮寄地址的“摘要”选项卡](media/party-gab-image5.png)

**联系人** 窗体的 **摘要** 选项卡上的 **地址 1**、**地址 2** 和 **地址 3** 字段分别对应于 **企业**、**交货** 和 **发票** 地址。

## <a name="electronic-address"></a>电子地址

已在 **帐户**、**联系人** 和 **供应商** 窗体上引入了名为 **电子地址** 的新选项卡。 使用网格支持 N 个地址的 **地址**，如下图所示：

![电子地址的网格](media/party-gab-image6.png)

+ **类型** 列可列出地址的类型。
+ **是主要** 列可列出主要地址。
+ **用途** 列可列出电子地址的用途。
+ **+ 新建电子地址** 按钮允许您创建新地址。 您可以根据需要创建任意多的地址。

电子地址仅在此网格上可用。 在将来的版本中，所有电子和邮寄地址字段将从其他选项卡中删除，例如 **摘要** 和 **详细信息** 选项卡。

## <a name="setup-instructions"></a>设置说明

如果您是现有的双重写入客户，则需要以下设置说明。 否则，您可以跳过此部分。

1. 停止以下映射，因为不再需要它们。 相反，运行联系人 V2 (msdyn_contactforparties) 映射。

    + CDS 联系人 V2 和联系人（指客户联系人）
    + CDS 联系人 V2 和联系人（指供应商联系人）

2. 针对当事方功能更新以下实体映射，因此必须将最新版本应用到这些映射。

映射 | 更新到此版本 | 更改
---|---|---
客户 V3 (accounts) | 1.0.0.5 |删除了当事方编号和与其他当事方相关的字段，例如姓名、个人详细信息、邮寄地址字段、电子联系人地址字段等。
客户 V3 (contacts) | 1.0.0.5 | 删除了当事方编号和与其他当事方相关的字段，例如姓名、个人详细信息、邮寄地址字段、电子联系人地址字段等。
供应商 V2 (msdyn_vendors) | 1.0.0.6 | 删除了当事方编号和与其他当事方相关的字段，例如姓名、个人详细信息、邮寄地址字段、电子联系人地址字段等。
CDS 销售报价单标题 (quotes) | 1.0.0.6 | 已将联系人替换为 ContactforParty 引用。
销售发票标题 V2 (invoices) | 1.0.0.4 | 已将联系人替换为 ContactforParty 引用。
CDS 销售订单标题 (salesorders) | 1.0.0.5 | 已将联系人替换为 ContactforParty 引用。
联系人 V2 (msdyn_contactforparties) | 1.0.0.2 | 这是新映射。 如果您有以前版本的当事方解决方案，请确保如前所述将此映射更新到最新版本。
CDS 当事方邮寄地址位置 (msdyn_partypostaladdresses) | 1.0.0.1  | 这是作为以前的当事方预览版本一部分添加的新映射。
CDS 邮寄地址历史记录 V2 (msdyn_postaladdresses) | | 这是作为以前的当事方预览版本一部分添加的新映射。
CDS 邮寄地址位置 (msdyn_postaladdresscollections) | | 这是作为以前的当事方预览版本一部分添加的新映射。
当事方联系人 V3 (msdyn_partyelectronicaddresses) | | 这是作为此版本的一部分添加的新映射。

## <a name="templates"></a>模板

对于当事方和全球通讯簿交互，表映射集合协同工作，如下表中所示。

Finance and Operations 应用 | Customer engagement 应用     | 说明
----------------------------|-----------------------------|------------
[联系人职务](mapping-reference.md#223) | msdyn_salescontactpersontitles |
[客户 V3](mapping-reference.md#101) | 帐户 |
[客户 V3](mapping-reference.md#116) | 联系人 |
[CDS 当事方](mapping-reference.md#220) | msdyn_parties |
[CDS 当事方邮政地址位置](mapping-reference.md#233) | msdyn_partypostaladdresses |
[CDS 邮寄地址历史记录 V2](mapping-reference.md#235) | msdyn_postaladdresses |
[CDS 邮政地址位置](mapping-reference.md#234) | msdyn_postaladdresscollections |
[CDS 销售报价标题](mapping-reference.md#215) | 询价 |
[CDS 销售订单标题](mapping-reference.md#217) | salesorders |
[结束语](mapping-reference.md#222) | msdyn_complimentaryclosings |
[联系人 V2](mapping-reference.md#221) | msdyn_contactforparties |
[决策角色](mapping-reference.md#224) | msdyn_decisionmakingroles |
[雇用工作职能](mapping-reference.md#225) | msdyn_employmentjobfunctions |
[忠诚度级别](mapping-reference.md#226) | msdyn_loyaltylevels |
[当事方联系人 V3](mapping-reference.md#236) | msdyn_partyelectronicaddresses |
[人员特点类型](mapping-reference.md#227) | msdyn_personalcharactertypes |
[销售账单抬头 V2](mapping-reference.md#118) | 发票 |
[称呼](mapping-reference.md#228) | msdyn_salutations |
[供应商 V2](mapping-reference.md#202) | msdyn_vendors |

有关更多信息，请参见[双重写入映射参考](mapping-reference.md)。
