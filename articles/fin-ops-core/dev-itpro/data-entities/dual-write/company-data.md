---
title: Dataverse 中的公司概念
description: 本主题介绍 Finance and Operations 与 Dataverse 之间的公司数据集成。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 2f0e3950f2b35dd8b8dbf50601b7d6b6d624863e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683667"
---
# <a name="company-concept-in-dataverse"></a>Dataverse 中的公司概念

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


在 Finance and Operations 中，*公司* 的概念既是法律构造，又是业务构造。 还是数据的安全和可见性界限。 用户始终在单个公司的上下文中工作，并且大多数数据已剥离了公司的性质。

Dataverse 没有同等概念。 最接近的概念是 *业务单位*，这主要是用户数据的安全和可见性界限。 此概念没有公司概念具有的同样法律或业务含义。

因为业务单位和公司不是同等概念，所以不能为了 Dataverse 集成而在两者之间强制执行一对一 (1:1) 的映射。 但是，因为默认情况下用户必须可以在应用程序和 Dataverse 中查看相同的行，所以 Microsoft 在 Dataverse 中引入了一个新实体，名称为 cdm\_Company。 这个实体与应用程序中的公司实体等同。 为了帮助确保应用程序与 Dataverse 之间行的原始可见性等同，所以我们建议在 Dataverse 中对数据进行以下设置：

+ 为启用了双写入的每个 Finance and Operations Company 行创建一个关联的 cdm\_Company 行。
+ 创建一个 cdm\_Company 行并为其启用双写入时，将创建一个同名的默认业务单位。 尽管会为这个业务单位自动创建一个默认团队，但是不会使用该业务单位。
+ 将单独创建一个同名的负责团队。 还会将其与该业务单位关联。
+ 默认情况下，创建的并双写入 Dataverse 的所有行的负责人都将设置为与关联业务单位链接的“DW 负责人”团队。

下图显示 Dataverse 中这种数据设置的示例。

![Dataverse 中的数据设置](media/dual-write-company-1.png)

因为此配置，所以与 USMF 公司有关的所有行都将由与 Dataverse 中的 USMF 业务单位链接的团队负责。 因此，所有可以通过设置为业务单位级可见性的安全角色访问该业务单位的用户现在都可以查看这些行。 以下示例显示如何使用团队正确访问这些行。

+ 将为“USMF 销售”团队的成员分配“销售经理”角色。
+ 具有“销售经理”角色的用户可以访问担任所属同一个业务单位的成员的所有帐户行。
+ “USMF 销售”团队已链接至前面介绍的 USMF 业务单位。
+ 因此，“USMF 销售”团队的成员可以查看“USMF DW”用户负责的所有客户，这些客户来自 Finance and Operations 中的 USMF 公司实体。

![如何使用团队](media/dual-write-company-2.png)

上图显示，业务单位、公司和团队之间的这种 1:1 映射还只是开始。 在此示例中，在 Dataverse 中手动新建了“欧洲”业务单位，同时充当 DEMF 和 ESMF 的父级。 这个新的根业务单位未与双写入关联。 但是，可用于为“EUR 销售”团队的成员提供 DEMF 和 ESMF 中的客户数据的访问权限，方法是在关联的安全角色中将数据可用性设置为 **父级/子级 BU**。

最后要介绍的是双写入如何确定应该将行分配给哪个负责团队。 此行为由 cdm\_Company 行中的 **默认负责团队** 控制。 如果为 cdm\_Company 行启用双写入，一个插件将自动创建关联的业务单位和负责团队（如果还没有），并设置 **默认负责团队** 字段。 管理员可以将此字段更改为其他值。 但是，只要为该实体启用了双写入，管理员就不能清除该字段。

> [!div class="mx-imgBorder"]
![默认负责团队字段](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>公司剥离和自扩展

Dataverse 集成通过使用公司标识符剥离数据来为公司提供奇偶校验。 如下图所示，已扩展了特定于公司的所有表，以使其与 cdm\_Company 实体之间存在多对一 (N:1) 关系。

> [!div class="mx-imgBorder"]
![特定于公司的实体与 cdm_Company 实体之间的 N:1 关系](media/dual-write-bootstrapping.png)

+ 对于行，添加并保存公司之后，该值变为只读。 因此，用户应确保选择正确的公司。
+ 只有包含公司数据的行才符合应用程序与 Dataverse 之间的双写入的资格。
+ 对于现有 Dataverse 数据，很快将提供管理员引导的自扩展体验。


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a>在 Customer Engagement 应用中自动填充公司名称

有几种方法可以在 Customer Engagement 应用中自动填充公司名称。

+ 如果您是系统管理员，可以通过导航到 **高级设置 > 系统 > 安全性 > 用户** 来设置默认公司。 打开 **用户** 窗体，然后在 **组织信息** 部分，设置 **窗体中的默认公司** 值。

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="在“组织信息”部分设置默认公司。":::

+ 如果您对 **业务单位** 级别的 **SystemUser** 实体具有 **写入** 访问权限，可以通过从 **公司** 下拉菜单中选择公司来更改任何一个窗体上的默认公司。

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="更改新客户中的公司名称。":::

+ 如果您对多个公司中的数据具有 **写入** 访问权限，可以通过选择属于不同公司的行来更改默认公司。

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="通过选择行更改默认公司。":::

+ 如果您是系统配置者或管理员，想要在自定义窗体上自动填充公司数据，可以使用[窗体事件](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids)。 将 JavaScript 引用添加到 **msdyn_/DefaultCompany.js** 并使用以下事件。 您可以使用任何现成的窗体，例如，**客户** 窗体。

    + 窗体的 **OnLoad** 事件：设置 **defaultCompany** 字段。
    + **公司** 字段的 **OnChange** 事件：设置 **updateDefaultCompany** 字段。

## <a name="apply-filtering-based-on-the-company-context"></a>基于公司上下文应用筛选

要在自定义窗体或添加到标准窗体的自定义查找字段中基于公司上下文应用筛选，请打开窗体，然后使用 **相关记录筛选** 部分应用公司筛选器。 您必须为每个需要基于给定行中的基础公司来筛选的查找字段设置此项。 下图中显示了 **客户** 的设置。

:::image type="content" source="media/apply-company-context.png" alt-text="应用公司上下文":::

