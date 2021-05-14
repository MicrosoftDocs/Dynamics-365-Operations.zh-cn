---
title: 当事方和全球通讯簿
description: 本主题介绍双重写入的当事方和全球通讯簿功能。
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: e2b0abb2826f81ed87b4f0f37dba32c1d8d749c2
ms.sourcegitcommit: 194d68b24cd36db21e9029044bed18983fd9810c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937878"
---
# <a name="party-and-global-address-book"></a>当事方和全球通讯簿

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

*当事方* 和 *全球通讯簿* 是 Finance and Operations 应用程序中的概念。 当事方可以是组织或个人。 在全球范围内存储和管理当事方的属性（如姓名、语言、联系人和地址）非常方便。 然后，当某个属性值在一个地方更改时，更改将反映在涉及当事方的所有地方。

## <a name="party"></a>当事方

当事方是企业中涉及的个人或组织。 使用当事方概念时，个人或组织可以在企业中扮演多个角色（例如，工作人员、客户、供应商或联系人）。 该角色基于环境和目的。 下面是来自两个虚拟公司（Contoso 和 Fabrikam）的角色的一些示例：

+ **工作人员** – 员工。 例如，Contoso 的员工。
+ **供应商** – 为企业提供商品或服务的供应商组织或独立经营者。 例如，如果 Fabrikam 将供应品出售给 Contoso，Fabrikam 就是 Contoso 的供应商。
+ **联系人** – 要联系的人员。 例如，如果 Contoso 从 Fabrikam 购买供应品，Contoso 的员工将与 Fabrikam 的联系人联系。
+ **客户** – 从公司购买商品的个人或公司。 例如，如果 Contoso 从 Fabrikam 购买供应品，Contoso 就是 Fabrikam 的客户。

当事方模型通常用于表示组织和个人之间中等到复杂的关系，特别是在当事方扮演多个角色时。 下面是一些常见示例：

+ 当事方可以是客户，也可以是供应商。 例如，在北美，Fabrikam 向 Contoso 出售电线，并从 Contoso 购买装配后的扬声器。 在欧洲，Fabrikam 向 Contoso 出售零件，但没有从 Contoso 购买任何商品。
+ 当事方可以是员工，也可以是客户。 例如，Contoso 的员工从 Contoso 购买电子产品供个人使用。
+ 个人和组织之间可能存在多对多 (N:N) 关系。 例如，Fabrikam 向服务专家提供服务并雇用安置协调员。 安置协调员针对一些 Fabrikam 客户的工作请求匹配服务专家。 Contoso 是 Fabrikam 的客户之一。 当 Contoso 需要服务专家时，它与安置协调员联系，然后由协调员进行请求。 由于安置协调员处理所有客户的请求，因此涉及 N:N 关系。

下图显示了当事方的数据模型。

![当事方的数据模型](media/party-gab-image1.png)

> [!TIP]
> 当您尝试创建新的客户记录时，请使用 **当事方** 字段按名称搜索记录。 这样，如果找到记录，只需选择它。 系统然后将自动填充当事方的所有数据。 您不必手动设置所有必填字段。 可以在现成的 **客户**、**联系人** 和 **供应商** 页面上找到此行为。

双重写入不能支持 Finance and Operations 应用的所有当事方角色。 有关当事方角色的完整列表，请参阅[全球通讯簿概览](../../../fin-ops/organization-administration/overview-global-address-book.md)。

### <a name="global-address-book"></a>全球通讯簿

全球通讯簿是参与企业的组织和个人的邮寄地址和电子地址的目录。

全球通讯簿根据需要存储和处理尽可能多的邮寄地址和电子地址。 例如，Fabrikam 在 50 个地点设有加油站。 每个地点都有不同的邮寄地址、电子邮件地址和电话号码。 所有企业采购都向主要加油站计费，但会直接运送到请求采购的特定加油站。 全球通讯簿将主要加油站存储为 Fabrikam 的帐单地址，将每个加油站存储为装运地址。 这些地址可以存储一次，然后可以在报价单和订单需要提供地址时对这些地址进行检索。

根据业务环境，个人或组织可能扮演多个角色，所有角色可能使用相同的邮寄地址和电子地址。 在这种情况下，一个角色的地址更改应该体现在所有其他角色中。 全球通讯簿在全球范围内存储和处理地址。

下图显示了全球通讯簿的数据模型。

![全球通讯簿的数据模型](media/party-gab-image2.png)

## <a name="contact"></a>联系人

在 Customer Engagement 应用中，联系人是个人。 但是，已重载 **联系人** 表以表示个人、门户用户、企业对消费者 (B2C) 客户或供应商。 该表示形式是隐式的，除非检查相关交易，否则无法分辨差异。 **联系人** 表已限制为与 **客户** 表具有一对一 (1:1) 关系。 作为当事方和全球通讯簿模型的一部分，双重写入为分类引入显式属性，并且允许个人联系人和组织（**客户** 实体或 **供应商** 实体）之间有 N:N 关系。

有两种类型的 **联系人** 行：

+ **出售联系人** – **公司** 字段有必填值的 **联系人** 行。
+ **非出售联系人** – **公司** 字段为空的 **联系人** 行。

**联系人** 表可以存储以下类型的行。

| 行类型 | 说明 |
|----------|-------------|
| 作为客户的个人（例如，可出售联系人或 B2C 客户） | **公司** 字段不为空并且 **是客户** 字段设置为 **是** 的出售联系人记录。 |
| 作为供应商的个人（例如，诸如供应商的独立经营者） | **公司** 字段不为空并且 **是供应商** 字段设置为 **是** 的出售联系人记录。 |
| 既是客户又是供应商的个人 | **公司** 字段不为空，**是客户** 字段设置为 **是** 并且 **是供应商** 字段设置为 **是** 的出售联系人记录。 个人既可以是一个产品的生产者，也可以是另一个产品的消费者。 Finance and Operations 应用和双重写入支持此关系。 |
| 作为组织联系人的个人不能是客户或供应商 | **公司** 字段为空，**是客户** 字段设置为 **否** 并且 **是供应商** 字段设置为 **否** 的非出售联系人记录。 |

## <a name="contact-for-party-table"></a>当事方的联系人表

**当事方的联系人** 表在 **客户** 行和 **联系人** 行之间存储和处理 N:N 关系。 它可以从非出售行中筛选出售 **联系人** 行，并仅将非出售 **联系人** 行与 **客户** 或 **供应商** 行关联。

例如，Natasha Jones 和 Miguel Reyes 是当地的兽医，负责照料农场。 Natasha 负责西雅图地区，而 Miguel 负责肯特地区。 在 Customer Engagement 应用中，农场表示为客户，而兽医则表示为联系人。 Natasha 的一个 **联系人** 记录将与 Natasha 合作的所有农场相关联。 同样，Miguel 的一个 **联系人** 记录将与 Miguel 合作的所有农场相关联。

这些关系存储在 **当事方的联系人** 表中。 您可以在现成的 **客户**、**联系人** 和 **供应商** 页面上找到此信息：

+ 在 **客户** 页上，您可以使用 **关联的联系人** 选项卡将一个或多个联系人与 **客户** 行关联。 这样，您将为组织分配联系人。 然后，您可以选择一个联系人作为客户的主要联系人。 如果您使用 **快速创建** 页，则只能选择一个联系人。 此行为与使用 **供应商** 页时相同，记录类型为 **组织**。
+ 在 **联系人** 页上，当行是客户、供应商或两者（出售联系人）时，您可以使用 **关联的联系人** 选项卡关联一个或多个联系人。 这样，您将为 B2C 客户或供应商分配联系人。 然后，您可以选择一个联系人作为主要联系人。 如果您使用 **快速创建** 页，则只能选择一个联系人。
+ 在 **联系人** 页上，当行是联系人（非出售联系人）时，您可以使用 **关联的组织** 选项卡关联一个或多个客户或供应商。 这样，您将为基础联系人分配客户或供应商。 客户或供应商可以是组织、个人或二者均可。 您一次只能在四个字段的其中一个字段中选择值：

    + 如果您在 **当事方 ID** 字段中选择值，基础联系人将分配给所选当事方的所有角色。
    + 如果您在 **关联的联系人** 字段中选择值，您将选择属于 **个人** 类型的出售联系人。
    + 如果您在 **关联的客户** 或 **关联的供应商** 字段中选择值，您将选择组织。

    ![联系人页上的“关联的组织”选项卡](media/party-gab-image3.png)

    无论您的选择如何，将在当事方级别创建关联，此关联将应用于当事方的所有角色，存储在 **当事方的联系人** 实体中。

> [!NOTE]
> 客户互动应用中 **当事方的联系人** 表的显示名称是 **客户/供应商的联系人**。

当您打开 **是客户** 字段和 **是供应商** 都设置为 **否** 的 **联系人** 行时，**关联的组织** 选项卡将显示。 使用此选项卡可以将一个或多个客户或供应商组织与联系人关联。

当您打开 **是客户** 字段或 **是供应商** 字段设置为 **是** 的 **联系人** 行时，**关联的联系人** 选项卡将显示。 使用此选项卡关联一个或多个联系人。

## <a name="postal-addresses"></a>邮寄地址

已在 **客户**、**联系人** 和 **供应商** 页引入了新的 **地址** 选项卡。 此选项卡使用网格支持多个邮寄地址，如下图所示。

![邮寄地址的网格](media/party-gab-image4.png)

此网格包括以下列：

+ **邮寄地址角色** – 邮寄地址的用途。
+ **是主要** – 指示地址是否为主要地址的值。
+ **地址编号** – 地址顺序。

您可以使用网格上方的 **新建地址** 按钮创建任意数量的邮寄地址。

**客户** 页的 **摘要** 选项卡上的 **地址 1** 和 **地址 2** 字段分别对应于 **交货** 和 **发票** 地址。

![邮寄地址的“摘要”选项卡](media/party-gab-image5.png)

**联系人** 页的 **摘要** 选项卡上的 **地址 1**、**地址 2** 和 **地址 3** 字段分别对应于 **企业**、**交货** 和 **发票** 地址。

## <a name="electronic-addresses"></a>电子地址

已在 **客户**、**联系人** 和 **供应商** 页引入了新的 **电子地址** 选项卡。 此选项卡使用网格支持多个电子地址，如下图所示。

![电子地址的网格](media/party-gab-image6.png)

此网格包括以下列：

+ **类型** – 电子地址的类型。
+ **是主要** 指示地址是否为主要地址的值。
+ **用途** – 电子地址的用途。

您可以使用网格上方的 **新建电子地址** 按钮创建任意数量的地址。

电子地址仅在此网格中可用。 在将来的版本中，所有邮寄地址和电子地址字段将从其他选项卡中删除（例如，**摘要** 和 **详细信息** 选项卡）。

## <a name="setup"></a>设置

1. 安装[双重写入应用程序业务流程解决方案](https://aka.ms/dual-write-app)的最新版本（2.2.2.60 或更高版本）。

2. 安装[双重写入当事方和全球通讯簿解决方案](https://aka.ms/dual-write-gab)。

3. 停止以下映射，因为不再需要它们。 改为运行 `Contacts V2 (msdyn_contactforparties)` 映射。

    + CDS 联系人 V2 和联系人（指客户联系人）
    + CDS 联系人 V2 和联系人（指供应商联系人）

4. 针对当事方功能更新以下实体映射，因此必须将最新版本应用到这些映射。

    映射 | 更新到此版本 | 更改
    ---|---|---
    `CDS Parties (msdyn_parties)`| 1.0.0.0 | 这是作为此版本的一部分添加的新映射。
    `Contacts V2 (msdyn_contactforparties)`| 1.0.0.5 | 这是作为此版本的一部分添加的新映射。
    `Customers V3 (accounts)` | 1.0.0.5 |删除了 `PartyNumber` 和与其他当事方相关字段，如姓名、个人详细信息、邮寄地址字段和电子联系人地址。
    `Customer V3 (contacts)` | 1.0.0.5 | 删除了 `PartyNumber` 和与其他当事方相关字段，如姓名、个人详细信息、邮寄地址字段和电子联系人地址。
    `Vendors V2 (msdyn_vendors)` | 1.0.0.6 | 删除了 `PartyNumber` 和与其他当事方相关字段，如姓名、个人详细信息、邮寄地址字段和电子联系人地址。
    `CDS Sales quotation headers (quotes)` | 1.0.0.7 | 已将联系人替换为 `ContactforParty` 引用。
    `Sales invoice headers V2 (invoices)` | 1.0.0.4 | 已将联系人替换为 `ContactforParty` 引用。
    `CDS Sales order headers (salesorders)` | 1.0.0.5 | 已将联系人替换为 `ContactforParty` 引用。
    `CDS Party postal address locations (msdyn_partypostaladdresses)` | 1.0.0.1  | 这是作为此版本的一部分添加的新映射。
    `CDS postal address history V2 (msdyn_postaladdresses)` | 1.0.0.1 | 这是作为此版本的一部分添加的新映射。
    `CDS postal address locations (msdyn_postaladdresscollections)` | 1.0.0.0 | 这是作为此版本的一部分添加的新映射。
    `Party Contacts V3 (msdyn_partyelectronicaddresses)` | 1.0.0.0 | 这是作为此版本的一部分添加的新映射。
    `Complimentary Closings ( msdyn_compliemntaryclosings)` | 1.0.0.0 | 这是作为此版本的一部分添加的新映射。
    `Decision making roles (msdyn_decisionmakingroles)` | 1.0.0.0 | 这是作为此版本的一部分添加的新映射。
    `Loyalty levels (msdyn_loyaltylevels)` | 1.0.0.0 | 这是作为此版本的一部分添加的新映射。
    `Contact person titles (msdyn_salescontactpersontitles)` | 1.0.0.0 | 这是作为此版本的一部分添加的新映射。
    `Personal character types (msdyn_personalcharactertypes)` | 1.0.0.0 | 这是作为此版本的一部分添加的新映射。
    `Salutations (msdyn_salutations)` | 1.0.0.0 | 这是作为此版本的一部分添加的新映射。
    `Employment job functions (msdyn_employmentjobfunctions)` | 1.0.0.0 | 这是作为此版本的一部分添加的新映射。

5. 在运行上述映射之前，您必须按照以下步骤中的说明手动更新集成键。 然后选择 **保存**。

    | 映射 | 键 |
    |-----|------|
    | 科目 |  accountnumber [客户编号]<br>msdyn_company.cdm_companycode [公司（公司代码）] |
    | 联系人 | msdyn_contactpersonid [客户编号/联系人 ID]<br>msdyn_company.cdm_companycode [公司（公司代码）] |
    | 客户/供应商的联系人 | msdyn_contactforpartynumber [当事方的联系人编号]<br>msdyn_associatedcompanyid.cdm_companycode [关联的公司（公司代码）] |
    | 供应商 | msdyn_vendoraccountnumber [供应商帐号]<br>msdyn_company.cdm_companycode [公司（公司代码）]|

6. 在 Dataverse 中，重复检测规则的字符数限制已从 450 个增加到 700 个字符。 此限制让您可以将一个或多个键添加到重复检测规则中。 通过设置以下字段扩展 **客户** 表的重复检测规则。

    | 字段 | 值 |
    |-------|-------|
    | 姓名 | 具有相同客户名称的客户。 |
    | 说明 | 检测在“客户名称”属性中具有相同值的客户记录。 |
    | 基本记录类型 | 科目 |
    | 匹配记录类型 | 科目 |
    | 客户名称（字段） | 完全匹配 |
    | 公司（字段） | 完全匹配 |
    | 关系类型（字段） | 完全匹配 |
    | 当事方 ID（字段） | 完全匹配 |
    | 选择（字段） | （空白） |

    ![客户重复规则](media/duplicate-rule-1.PNG)

7. 通过设置以下字段扩展 **联系人** 表的重复检测规则。

    | 字段 | 值 |
    |-------|-------|
    | 姓名 | 具有相同名字和姓氏的联系人。 |
    | 说明 | 检测在“名字”和“姓氏”字段具有相同值的联系人记录。 |
    | 基本记录类型 | 联系人 |
    | 匹配记录类型 | 联系人 |
    | 名字（字段） | 完全匹配 |
    | 姓氏（字段） | 完全匹配 |
    | 公司（字段） | 完全匹配 |
    | 当事方 ID（字段） | 完全匹配 |
    | 选择（字段） | （空白） |

    ![联系人重复规则](media/duplicate-rule-2.PNG)

8. 如果您是现有双重写入用户，请按照[升级到当事方和全球通讯簿模型](upgrade-party-gab.md)中的说明操作升级数据。

9. 按照以下顺序运行映射。 如果收到错误，指示“项目验证失败。 缺少目标字段...”，打开映射，选择 **刷新表**。 然后运行映射。

    Finance and Operations 应用 | Customer engagement 应用  
    ----------------------------|------------------------
    [CDS 当事方](mapping-reference.md#220) | msdyn_parties
    [CDS 邮政地址位置](mapping-reference.md#234) | msdyn_postaladdresscollections
    [CDS 邮寄地址历史记录 V2](mapping-reference.md#235) | msdyn_postaladdresses
    [CDS 当事方邮政地址位置](mapping-reference.md#233) | msdyn_partypostaladdresses
    [当事方联系人 V3](mapping-reference.md#236) | msdyn_partyelectronicaddresses
    [客户 V3](mapping-reference.md#101) | 帐户
    [客户 V3](mapping-reference.md#116) | 联系人
    [供应商 V2](mapping-reference.md#202) | msdyn_vendors
    [联系人职务](mapping-reference.md#223) | msdyn_salescontactpersontitles
    [结束语](mapping-reference.md#222) | msdyn_complimentaryclosings
    [称呼](mapping-reference.md#228) | msdyn_salutations
    [决策角色](mapping-reference.md#224) | msdyn_decisionmakingroles
    [雇用工作职能](mapping-reference.md#225) | msdyn_employmentjobfunctions
    [忠诚度级别](mapping-reference.md#226) | msdyn_loyaltylevels
    [人员特点类型](mapping-reference.md#227) | msdyn_personalcharactertypes
    [联系人 V2](mapping-reference.md#221) | msdyn_contactforparties
    [CDS 销售报价标题](mapping-reference.md#215) | 询价
    [CDS 销售订单标题](mapping-reference.md#217) | salesorders
    [销售账单抬头 V2](mapping-reference.md#118) | 发票

> [!Note]
> `CDS Contacts V2 (contacts)` 映射是您在步骤 1 中停止的映射。 当您尝试运行其他映射时，这 2 个映射可能会显示在依赖项列表中。 不要运行这些映射。

> [!Note]
> 如果安装了当事方和全球通讯簿解决方案，则必须禁用名为 `Microsoft.Dynamics.SCMExtended.Plugins.Plugins.LeadPrimaryContactPostCreate: QualifyLead of lead` 的插件。 如果卸载当事方和全球通讯簿解决方案，则必须重新启用该插件。

> [!Note]
> **客户**、**联系人** 和 **供应商** 表中包含的 `msdyn_*partynumber` 字段（单行文本字段）不应该继续使用。 为了清楚起见，标签名称带有 **(Deprecated)** 前缀。 而应改为使用 **msdyn_partyid** 字段。 此字段是对 **msdyn_party** 表的查找。

> 表名 | 旧字段 | 新字段
> --------|-------|--------
> 科目 | `msdyn_partynumber` | `msdyn_partyid`
> 联系人 | `msdyn_partynumber` | `msdyn_partyid`
> msdyn_vendor | `msdyn_vendorpartynumber` | `msdyn_partyid`

## <a name="templates"></a>模板

对于当事方和全球通讯簿交互，表映射集合协同工作，如下表中所示。

| Finance and Operations 应用 | Customer engagement 应用 | 说明 |
|----------------------------|-------------------------|-------------|
| [联系人职务](mapping-reference.md#223) | msdyn\_salescontactpersontitles |
| [客户 V3](mapping-reference.md#101) | 帐户 |
| [客户 V3](mapping-reference.md#116) | 联系人 |
| [CDS 当事方](mapping-reference.md#220) | msdyn\_parties |
| [CDS 当事方邮政地址位置](mapping-reference.md#233) | msdyn\_partypostaladdresses |
| [CDS 邮寄地址历史记录 V2](mapping-reference.md#235) | msdyn\_postaladdresses |
| [CDS 邮政地址位置](mapping-reference.md#234) | msdyn\_postaladdresscollections |
| [CDS 销售报价标题](mapping-reference.md#215) | 询价 |
| [CDS 销售订单标题](mapping-reference.md#217) | salesorders |
| [结束语](mapping-reference.md#222) | msdyn\_complimentaryclosings |
| [联系人 V2](mapping-reference.md#221) | msdyn\_contactforparties |
| [决策角色](mapping-reference.md#224) | msdyn\_decisionmakingroles |
| [雇用工作职能](mapping-reference.md#225) | msdyn\_employmentjobfunctions |
| [忠诚度级别](mapping-reference.md#226) | msdyn\_loyaltylevels |
| [当事方联系人 V3](mapping-reference.md#236) | msdyn\_partyelectronicaddresses |
| [人员特点类型](mapping-reference.md#227) | msdyn\_personalcharactertypes |
| [销售账单抬头 V2](mapping-reference.md#118) | 发票 |
| [称呼](mapping-reference.md#228) | msdyn\_salutations |
| [供应商 V2](mapping-reference.md#202) | msdyn\_vendors |

有关更多信息，请参见[双重写入映射参考](mapping-reference.md)。

## <a name="known-issues-and-limitations"></a>已知问题和限制

+ 在n Finance and Operations 应用中，当您创建客户以及地址并进行保存时，地址可能不会同步到 **地址** 表。 这是由于双重写入平台排序问题。 解决方法是，先创建客户并进行保存。 然后添加地址。
+ 在 Finance and Operations 应用中，如果客户记录具有主要地址，当您为该客户创建新联系人时，联系人记录将从关联的客户记录继承主要地址。 供应商联系人也是如此。 Dataverse 目前不支持此行为。 如果启用了双重写入，从 Finance and Operations 应用通过主要地址继承的客户联系人将随其地址一起同步到 Dataverse。
+ 来自 `msdyn_partyelectronicaddress` 表的电子地址不会流向 **客户** 和 **联系人** 表的电子地址字段。 我们计划在增量版本中解决此问题。 **客户** 和 **联系人** 表中电子地址字段上的现有数据不会被覆盖。
+ 在 **客户**、**联系人** 和 **供应商** 窗体的电子地址选项卡上设置的电子地址来自 `msdyn_partyelectronicaddress` 表。 此信息不会流向其关联交易，如销售订单、报价单和采购订单。 我们计划在增量版本中解决此问题。 客户和联系人记录上电子地址字段中的现有数据将继续用于销售订单、报价单和采购订单之类的交易。
+ 在 Finance and Operations 应用中，您可以从 **添加联系人** 窗体创建联系人记录。 当您尝试从 **查看联系人** 窗体创建新联系人时，操作将失败。 这是一个已知问题。

    ![添加联系人的已知问题](media/party-gab-contact-issue.png)

+ **初始同步** 不支持 **ContactForParty** 上的 **Available From** 和 **Available To** 时间字段，因为 DIXF 会将值转换为字符串而不是整数。 转换将触发错误 `Cannot convert the literal '<say 08:00:00>’ to the expected type edm.int32`。
+ 当出于多种原因使用邮寄地址时，例如，业务通信地址和帐单地址，它应显示为 `Business;Invoice`，如下图所示。 如果在两个值之间添加空格，会出现错误。

    ![地址的已知问题](media/party-gab-address-issue.png)

+ 您不能使用具有双重写入功能的 Finance and Operations 应用输入将来的邮寄地址，因为 Dataverse 不支持日期有效期。 如果您使用 Finance and Operations 应用输入将来的邮寄地址，它将完全同步到 Dataverse，您会在用户界面立即看到该地址。 此记录的任何更新都将导致错误，因为它在 Finance and Operations 应用中是将来的日期，而不是当前日期。
