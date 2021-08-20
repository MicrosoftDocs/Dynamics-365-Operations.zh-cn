---
title: 验证页面内容的可访问性
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中验证页面内容的可访问性。
author: josaw1
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6f92d5c34896e284a40a4806cd83e469c2db4c9181c919d2d967dacc84076201
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748440"
---
# <a name="verify-page-content-accessibility"></a>验证页面内容的可访问性

[!include [banner](includes/banner.md)]

本主题介绍如何在 Microsoft Dynamics 365 Commerce 中验证页面内容的可访问性。

完成页面更改后，应确保内容可供 Web 上的所有人访问。 在 Commerce 创作工具中，您可以使用集成的 [Microsoft Accessibility Insights](https://accessibilityinsights.io/) 服务轻松地验证页面内容的可访问性。 此服务可根据最新的[万维网联合会 (W3C) 可访问性](https://www.w3.org/standards/webdesign/accessibility)准则验证您的页面内容。

[Microsoft Accessibility Insights](https://accessibilityinsights.io/) 集成必须先在租户或站点级别打开，然后才能使用。

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a>为租户中的所有站点打开 Microsoft Accessibility Insights

要为租户中的所有 Commerce 站点打开 [Microsoft Accessibility Insights](https://accessibilityinsights.io/) 集成，请按照以下步骤操作。

> [!NOTE]
> 要访问租户设置，您必须以系统管理员身份登录到 Commerce。

1. 以系统管理员身份登录到 Commerce。
1. 在左侧导航窗格中，选择 **租户设置**（在齿轮符号旁边）将其展开。
1. 在 **租户设置** 下，选择 **功能**。
1. 将 **可访问性检查** 选项设置为 **开**。

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a>为单个站点打开 Microsoft Accessibility Insights

要为单个 Commerce 站点打开 [Microsoft Accessibility Insights](https://accessibilityinsights.io/) 集成，请按照以下步骤操作。

1. 在 **站点** 下，选择 **Fabrikam**（或您的站点的名称）。
1. 在左侧导航窗格中，选择 **站点设置** 将其展开。
1. 在 **站点设置** 下，选择 **功能**。
1. 将 **可访问性检查** 选项设置为 **开**。

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a>验证主页上内容的可访问性

要使用集成的 [Microsoft Accessibility Insights](https://accessibilityinsights.io/) 服务扫描和验证 Commerce 中主页的内容，请按照下列步骤操作。

1. 在 **站点** 下，选择 **Fabrikam**（或您的站点的名称）。
1. 在左侧导航窗格中，选择 **页面**。
1. 转到并选择主页在页面编辑器中将其打开。
1. 在命令栏中，选择 **检查可访问性**。 **检查可访问性** 页面将出现。
1. 扫描完成后，查看报告内容。
1. 如果有任何检查失败，请选择每个失败的检查项目将其展开，这样可以查看更多详细信息。
1. 要在查看完后关闭报告，滚动到 **检查可访问性** 页面的底部，然后选择 **确定**。

## <a name="additional-resources"></a>其他资源

[修改现有的站点页面](modify-existing-page.md)

[添加新的站点页面](add-new-page.md)

[选择页面布局](select-page-layouts.md)

[管理 SEO 元数据](manage-seo-metadata.md)

[保存、预览和发布页面](save-preview-publish-page.md)

[丰富产品页面](enrich-product-page.md)

[丰富类别登陆页面](enrich-category-page.md)

[基于 URL 参数创建动态电子商务页面](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
