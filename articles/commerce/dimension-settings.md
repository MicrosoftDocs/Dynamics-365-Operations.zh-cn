---
title: 应用产品维度的显示设置
description: 本文介绍产品维度的显示设置，并介绍如何在 Microsoft Dynamics 365 Commerce 中应用这些设置。
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 9324518fff35d357f845c08cba25e2faded2f381
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269962"
---
# <a name="apply-display-settings-for-product-dimensions"></a>应用产品维度的显示设置

[!include [banner](includes/banner.md)]


本文介绍产品维度的显示设置，并介绍如何在 Microsoft Dynamics 365 Commerce 中应用这些设置。

Dynamics 365 Commerce 支持使用尺寸、样式和颜色维度来区分产品变型。 维度通常显示为文本值，如“小”、“中”和“大”是尺寸，“黑色”和“棕色”是颜色。 但是，如果产品支持很多变体，浏览产品变型可能很难，因为需要多次选择才能查看每个变型的图像。 为了使浏览产品变型更加容易，Commerce 的 10.0.20 版本可以使用图像和十六进制 (hex) 代码将维度显示为样本。

在 Commerce 站点构建器中，维度设置在 **站点设置 \> 扩展 \> 维度设置** 处定义。 下图显示了站点构建器中维度设置的示例。

![Commerce 站点构建器中站点设置的示例。](./dev-itpro/media/swatch_site_settings.PNG)

有两个维度设置可用：

- **显示为图像的维度** – 指定应在电子商务站点页面（如产品详细信息页面 (PDP) 和搜索结果列表页面）上显示为样本的维度。 颜色、尺寸和样式维度的任何组合都可以显示为一个样本。 如果选择了一个维度要将其显示为样本，Commerce 模块呈现将查找可用的十六进制代码样本配置。 如果未配置十六进制代码，系统逻辑将查找图像 URL 样本的配置。 如果既未配置十六进制代码，也未配置图像 URL，将显示文本。

    下图显示了一个示例，其中电子商务站点上的 PDP 包含颜色和尺寸样本。 在此示例中，为颜色维度配置了十六进制代码。 因此，样本显示为颜色。 但是，没有为尺寸维度配置十六进制代码和图像 URL。 因此，显示文本。

    ![在电子商务产品详细信息页面上显示为样本的颜色维度的示例。](./dev-itpro/media/swatch_pdp.png)

- **在产品卡中显示的维度** – 指定应在列表和列表页上显示的产品卡上显示哪些维度。 必须为维度启用此设置，维度才能够显示在产品卡上。 **显示为图像的维度** 设置也应启用。 产品卡上的样本选择行为针对颜色维度进行了优化。 对于其他维度，可能需要扩展视图来自定义样本选择行为。

    下图显示了一个示例，其中电子商务站点上的列表页包含包括颜色样本的产品卡。

    ![在电子商务列表页面上显示为样本的颜色维度的示例。](./dev-itpro/media/swatch_searchresults.PNG)

有关如何配置产品维度以使其在站点页面上显示为样本的信息，请参阅[将产品维度值配置为作为样本显示](./dev-itpro/dimensions-swatch.md)。

## <a name="additional-resources"></a>其他资源

[模块库概览](starter-kit-overview.md)

[搜索结果模块](search-result-module.md)

[购买框模块](add-buy-box.md)

[将产品维度值配置为作为样本显示](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
