---
title: 库存感知产品列表
description: 本文介绍组织如何在其 Microsoft Dynamics 365 Commerce 电子商务网站上配置产品列表页，使其具有库存感知能力。
author: boycez
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2022-08-23
ms.openlocfilehash: 2a65dedf2da62fcd92169077d75a0f3b7832a86d
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473725"
---
# <a name="inventory-aware-product-listing"></a>库存感知产品列表

[!include [banner](../includes/banner.md)]

本文介绍组织如何在其 Microsoft Dynamics 365 Commerce 电子商务网站上配置产品列表页，使其具有库存感知能力。 产品列表页包括类别登陆页面和搜索结果页面。

购物者通常希望整个电子商务网站的产品发现体验都能感知库存，以便他们可以决定在产品库存不足时该怎么办。 [Commerce 模块库](starter-kit-overview.md)类别和搜索结果模块可以配置为包含库存数据。 通过这种方式，它们可以提供以下体验：

- 在产品旁边显示库存水平标签。
- 从产品列表中隐藏库存不足的产品。
- 将库存不足的产品移到产品列表页的底部。
- 支持基于库存的产品筛选。

要启用这些体验，您必须首先在 Commerce headquarters 中启用 **用于了解库存的增强型电子商务产品发现** 功能。

> [!NOTE]
> 在 Commerce 版本 10.0.29 及更高版本中，**用于了解库存的增强型电子商务产品发现** 功能默认启用。

## <a name="set-up-product-attribute-for-inventory-availability"></a>为库存可用性设置产品属性

库存感知产品列表使用产品属性框架。 作为先决条件，必须创建一个专用产品属性来捕获库存可用性数据。

要在 Commerce headquarters 中为库存可用性设置产品属性，请按照下列步骤操作。

1. 转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 产品和库存 \> 使用库存水平填充产品属性**。
1. 在 **使用库存水平填充产品属性** 对话框中，在 **产品属性和类型名称** 字段中，将要创建用于捕获库存数据的专用产品属性输入自定义名称。
1. 在 **库存可用性依据** 字段中，选择库存水平计算应基于的数量类型：**实际可用** 或 **可用总计**。
1. 将 **批处理** 选项设置为 **是**。
1. 选择 **确定**。

> [!NOTE]
> 为了在您的电子商务网站的页面之间一致地计算库存水平，确保在 **使用库存水平填充产品属性** 作业的 **库存可用性依据** 字段和 Commerce 站点构建器中的 **库存水平依据** 设置中选择相同的数量类型。

创建专用产品属性后，下一步是为在线渠道配置属性。

要在 Commerce headquarters 中为在线渠道配置属性，请按照下列步骤操作。

1. 转到 **Retail 和 Commerce \> 渠道设置 \> 渠道类别和产品属性**。
1. 选择要为其启用库存感知产品列表体验的在线渠道。
1. 选择并打开关联的属性组，然后将新的产品属性添加到其中。
1. 转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 配送计划**，运行 **1150**（**目录**）作业。 我们建议您将此作业计划为批处理，运行频率与 **使用库存水平填充产品属性** 作业相同。

> [!NOTE]
> 在 Commerce 版本 10.0.26 及更早版本中，将库存可用性产品属性添加到属性组后，还必须选择 **设置属性元数据**，然后为新产品属性打开 **在渠道上显示属性**、**可检索**、**可细化** 和 **可查询** 选项。

## <a name="configure-the-display-behavior-for-out-of-stock-products-on-product-listing-pages"></a>在产品列表页上配置库存不足产品的显示行为

完成上述所有配置步骤后，类别和搜索结果页面上的精简项将具有基于库存的筛选器选项。 将为页面上显示的每个产品磁贴显示库存水平标签。

类别和搜索结果页面将在基础产品级别显示产品，而不是产品变型级别。 每个产品旁边显示的库存水平是由所有产品变型的库存水平确定的聚合库存水平。 变型的库存水平根据该变型在 Commerce headquarters 中在线渠道的默认仓库中的现有库存量计算。 基础产品的库存水平有两个可能值，分别代表有存货和库存不足状态。 当基础产品的所有变型都库存不足时，将其视为库存不足。 否则，该产品将被视为有存货。 此值的标签从[库存水平](inventory-buffers-levels.md)定义中检索。 如果未定义库存水平，默认标签（英文）为 **Available** 和 **Out of stock**。

您可以在 Commerce 站点构建器中配置 **产品列表页的库存设置** 设置，来控制类别和搜索结果页面如何显示库存不足产品。 有关详细信息，请参阅[应用库存设置](inventory-settings.md)。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
