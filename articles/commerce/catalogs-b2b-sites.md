---
title: 为 B2B 站点创建 Commerce 目录
description: 本主题介绍如何为 Microsoft Dynamics 365 Commerce 企业到企业 (B2B) 站点创建 Commerce 目录。
author: ashishmsft
ms.date: 04/28/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 868f6bbeefeb1698bb136d52c09cebf293c95731
ms.sourcegitcommit: 0abc777986112ea2332f5bf0e815b303b952356c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/29/2022
ms.locfileid: "8656833"
---
# <a name="create-commerce-catalogs-for-b2b-sites"></a>为 B2B 站点创建 Commerce 目录

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

本主题介绍如何为 Microsoft Dynamics 365 Commerce 企业到企业 (B2B) 站点创建 Commerce 产品目录。 有关 B2B 站点的 Commerce 目录的常见问题的解答，请参阅 [B2B 的 Commerce 目录常见问题解答](catalogs-b2b-sites-FAQ.md)。

> [!NOTE]
> 此主题适用于 Dynamics 365 Commerce 版本 10.0.26 及更高版本。

可以使用 Commerce 目录来标识您想要在您的 B2B 在线商店提供的产品。 创建类别时，确定提供产品的在线商店，添加要包括的产品，并通过添加商品促销详细信息提高产品供应。 可以为每个 B2B 在线商店创建多个目录。

Commerce 产品目录允许您定义以下信息：

- **特定于目录的导航层次结构** - 组织可以为其特定目录创建不同的类别结构。
- **特定于目录的属性元数据** - 属性包含有关产品的详细信息。 通过将属性分配给导航层次结构的类别，您可以在分配给该类别的产品级别定义这些属性的值。 然后组织可以完成以下任务：

    - 定义特定于目录的属性值。
    - 在目录级别控制属性的可见性。
    - 选择特定于单个目录的优化器。

- **渠道** - 组织可以将多个 B2B 在线渠道与目录相关联。 对目录的端到端支持目前仅适用于 B2B 在线商店。
- **客户层次结构** - 对于给定的 B2B 渠道，组织可以通过将客户层次结构与该目录相关联来为选定的 B2B 合作伙伴提供特定目录。
- **价格组** - 您可以配置特定于给定目录的价格和促销。 此功能是为 B2B 渠道定义目录的核心原因。 目录的价格组使组织能够向其预期的 B2B 组织提供产品并应用其首选定价和折扣。 从配置目录订购的 B2B 客户在登录 Commerce B2B 站点后可以从特价和促销中受益。 若要配置目录特定的价格，请在 **目录** 选项卡上选择 **价格组**，以便将一个或多个价格组链接到该目录。 客户通过该目录订购时，将应用已链接到同一个价格组的所有贸易协议、价格调整日记帐和提前折扣。 （高级折扣包括阈值、数量和组合购买折扣。）有关价格组的详细信息，请参阅[价格组](price-management.md#price-groups)。

> [!NOTE]
> 从 Dynamics 365 Commerce 版本 10.0.26 起提供此功能。 要配置特定于目录的配置，例如导航层次结构和客户层次结构，请在 Commerce Headquarters 中打开 **功能管理** 工作区（**系统管理 \> 工作区 \> 功能管理**），启用 **允许对零售渠道使用多个目录** 功能，然后运行 **1110 CDX** 作业。

## <a name="catalog-process-flow"></a>目录流程流

创建和处理目录的过程具有四个常规步骤。 下一节将详细解释每个步骤。

1. **[配置](#configure-the-catalog)**

    - 关联导航层次结构。
    - 指定时间限制和到期日期（如果适用）。
    - 添加产品并对其进行分类。
    - 关联价格组。
    - 关联特定于您的 B2B 组织的客户层次结构。 
    - 关联优化器的默认维度属性组，如尺寸、样式和颜色。
    - 设置属性元数据。

1. **[验证](#validate-the-catalog)** - 在此步骤中，您将运行强制执行特定行为的验证规则。 下面举了一些示例加以说明：

    - 确保没有未分类的产品。
    - 确保分类到每个渠道的所有项都与目录相关联。

1. **[审批](#approve-the-catalog)**
1. **[正在发布](#publish-the-catalog)**

## <a name="set-up-the-catalog"></a>设置目录

使用此部分中的信息设置目录。

### <a name="configure-the-catalog"></a>配置目录

在 Commerce Headquarters 中，转到 **Retail 和 Commerce \> 目录和分类 \> 所有目录** 以配置您的目录。

创建新目录时，首先必须将其与一个或多个渠道关联。 创建目录时，只能使用已链接到您选择的渠道[分类](/dynamics365/unified-operations/retail/assortments)的项。 若要将目录与一个或多个渠道关联，请选择 **目录设置** 页面的 **Commerce 渠道** 快速选项卡上的 **添加**。

#### <a name="associate-the-navigation-hierarchy"></a>关联导航层次结构

若要向目录添加产品，必须选择导航层次结构。 导航层次结构将为目录的类别结构提供支持。 您必须选择一个已与 **目录设置** 页面 **Commerce 渠道** 快速选项卡中所选渠道关联的导航层次结构。 要将默认导航层次结构与每个渠道关联，请转到 **Retail 和 Commerce \> 渠道设置 \> 渠道类别和产品属性**。

#### <a name="specify-time-effective-and-expiration-dates"></a>指定时间限制和到期日期

若要指定目录的时间限制和到期日期，请选择目录层次结构的顶部节点以返回到主目录标题视图。 然后，根据需要在 **常规** 快速选项卡中配置生效日期和到期日期。

#### <a name="add-and-categorize-products"></a>添加产品并对其进行分类

若要配置要添加到目录中的产品，请在 Commerce Headquarters 中，转到 **Retail 和 Commerce \> 目录和分类 \> 所有目录**。 然后，在 **目录** 选项卡上，选择 **添加产品**。

或者，选择导航层次结构中的节点。 然后，您将能够将产品直接添加到目录中的类别。

#### <a name="associate-price-groups"></a>关联价格组

若要配置特定于目录的价格，您必须将一个或多个价格组链接到目录。 若要将价格组与目录关联，请在 Commerce Headquarters 中，转到 **Retail 和 Commerce \> 目录和分类 \> 所有目录**。 然后，在 **目录** 选项卡上的 **定价** 下面，选择 **价格组**。 客户通过此目录订购时，将应用已链接到同一个价格组的所有贸易协议、价格调整日记帐、和零售提前折扣（阈值、数量和组合购买折扣）。

有关价格组的详细信息，请参阅[价格组](price-management.md#price-groups)。

> [!NOTE]
> 无法从 **所有目录** 页面创建新的价格组。 相反，您必须从 **所有价格组** 页面创建它。 然后，必须将其与 **所有目录** 页面上的目录相关联。

#### <a name="associate-a-customer-hierarchy"></a>关联客户层次结构

要关联客户层次结构，请在 Commerce Headquarters 中，转到 **Retail 和 Commerce \> 目录和分类 \> 所有目录**。 然后，在 **目录** 选项卡上的 **客户层次结构** 下面，选择 **分配层次结构** 以将一个或多个客户层次结构链接到目录。

> [!NOTE]
> 无法从 **所有目录** 页面创建新的客户层次结构。 相反，您必须从 **客户层次结构** 页面创建它。 然后，必须将其与 **所有目录** 页面上的目录相关联。

#### <a name="associate-default-dimension-attribute-group-for-refiners-such-as-size-style-and-color"></a>关联优化器的默认维度属性组，如尺寸、样式和颜色

要关联优化器的默认维度属性组，例如尺寸、样式和颜色，请在 Commerce Headquarters 中，转到 **Retail 和 Commerce \> 目录和分类 \> 所有目录**。 然后，在 **目录** 选项卡上的 **属性** 下面，选择 **属性组**。

#### <a name="set-attribute-metadata"></a>设置属性元数据

要配置属性元数据，请在 Commerce Headquarters 中，转到 **Retail 和 Commerce \> 目录和分类 \> 所有目录** 以配置您的目录。 然后，在 **目录** 选项卡上的 **属性** 下面，选择 **设置属性元数据**。 要选择应可查看和可优化的属性，请在关联的目录特定导航层次结构中选择一个类别，然后在 **目录产品属性** 下选择一个属性。 然后选择 **在渠道上显示属性**。 默认情况下，所有可查看属性也是可搜索的。 要选择性地使属性可优化，请选择 **可优化**。

### <a name="validate-the-catalog"></a>验证目录

在新目录可供使用之前，必须对其进行验证和发布。

若要验证目录，请遵从这些步骤。

1. 在 **所有目录** 页面的 **目录** 选项卡上，在 **验证** 下选择 **验证目录** 以运行验证。 需要执行此步骤。 该操作将验证所需设置是否准确。
1. 选择 **查看结果** 以查看验证的详细信息。 如果发现了错误，必须更正数据，然后再次运行验证，直到通过验证。

### <a name="approve-the-catalog"></a>审核目录

目录经过验证后，必须得到批准。

要启动目录审批工作流，请执行以下步骤。

1. 在 **所有目录** 页面的操作窗格中，选择 **工作流 \> 提交**。
1. 转到 **Retail 和 Commerce \> Headquarters 设置 \> Commerce 工作流**，以配置工作流的步骤和授权用户。 此工作流将定义把目录设置为 **已审批** 状态需要执行的步骤。

### <a name="publish-the-catalog"></a>发布目录

目录处于 **已批准** 状态后，您可以通过选择 **目录** 菜单上的 **发布** 来发布目录。 目录处于 **已发布** 状态后，可在呼叫中心订单录入和发送目录流程中使用该目录。 可以手动或通过使用批处理发布目录。 您为目录定义的生效日期决定了何时产品在在线商店中可用。 您定义的到期日期决定了何时从在线商店中删除产品。

> [!NOTE]
> 可以发布包含具有警告的产品的目录。 但是，这些产品不会出现在在线商店中。

## <a name="additional-resources"></a>其他资源

[Commerce 目录对 B2B 自定义的可扩展性影响](catalogs-b2b-sites-dev.md)

[B2B 常见问题解答的 Commerce 目录](catalogs-b2b-sites-FAQ.md)
