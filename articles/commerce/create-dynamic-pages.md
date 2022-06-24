---
title: 根据 URL 参数创建动态电子商务页面
description: 本文介绍如何基于 URL 参数设置可以提供动态内容的 Microsoft Dynamics 365 Commerce 电子商务页面。
author: StuHarg
ms.date: 05/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.openlocfilehash: e2b13403ffb316059476a03857c849b4f9f8cb9c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884655"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a>根据 URL 参数创建动态电子商务页面

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

本文介绍如何基于 URL 参数设置可以提供动态内容的 Microsoft Dynamics 365 Commerce 电子商务页面。

可以基于 URL 路径中的段将电子商务页面配置为提供不同的内容。 因此，该页面称为动态页面。 段用作检索页面内容的参数。 例如，在站点生成器中创建并命名为 **博客\_查看者** 的页面被映射到 URL `https://fabrikam.com/blog`。 然后可以基于 URL 路径中的最后一个段使用此页面来显示不同的内容。 例如，URL `https://fabrikam.com/blog/article-1` 中的最后一个段是 **article-1**。

您还可以使用站点生成器页面替代参数化的 URL 段。 例如，在站点生成器中创建并命名为 **博客\_摘要** 的页面可映射到 URL `https://fabrikam.com/blog/about-this-blog`。 当请求末尾带有 `/about-this-blog` 段的 `https://fabrikam.com/blog` URL 时，将返回 **博客\_摘要** 页面内容，而不是返回被解释为 `https://fabrikam.com/blog` 页面使用的参数的 `/about-this-blog` 段。 

在为要传递给动态页面的参数选择名称时，动态页面在 URL 中显示的名称（上例中的 `/blog`）不能用作参数名称或参数名称子字符串。 

> [!NOTE]
> 托管、检索和显示动态页面内容的功能通过使用自定义模块实现。 有关详细信息，请参阅[在线渠道可扩展性](e-commerce-extensibility/overview.md)。

## <a name="set-up-a-dynamic-e-commerce-page"></a>设置动态电子商务页面

要设置动态电子商务页面，必须创建动态页面，创建基本 URL，并配置到达动态页面的路由。

### <a name="create-the-page-that-will-serve-dynamic-content"></a>创建将提供动态内容的页面

要创建将提供动态内容的页面，请按照[添加新的站点页面](add-new-page.md)中的步骤操作。 您创建的页面将需要实现一个模块，该模块使用 URL 路径中的最后一个段来从外部数据源检索内容。 有关自定义模块开发的详细信息，请参阅[在线渠道可扩展性](e-commerce-extensibility/overview.md)。

### <a name="create-the-base-url-for-the-dynamic-page"></a>创建动态页面的基本 URL

要在 Commerce 站点构建器中为动态页面创建基本 URL，请按照下列步骤操作。

1. 转到 **URL**，选择 **新建 \> 新建 URL**。
1. 在 **创建新 URL** 对话框中，选择 **内部页面**。 在 **URL 路径** 下，输入将用作动态页面根目录的路径（在此示例中为 **/blog**）。 然后选择 **下一步**。
1. 在 **选择页面** 对话框中，选择您创建的要用作动态页面的页面，然后选择 **保存**。
1. 选择 **发布**。

### <a name="configure-the-route-to-the-dynamic-page"></a>配置到达动态页面的路由

要在 Commerce 站点构建器中配置到达动态页面的路由，请按照下列步骤操作。

1. 转到 **站点设置 \> 扩展**。
1. 在 **参数化 URL 路径** 下，选择 **添加**，然后输入您在创建 URL 时输入的 URL 路径（在本示例中为 **/blog**）。
1. 选择 **保存并发布**。

配置路由后，对参数化 URL 路径的所有请求都将返回与该 URL 关联的页面。 如果任何请求包含附加段，将返回关联的页面，并将该段用作参数来检索页面内容。 例如，`https://fabrikam.com/blog/article-1` 将返回 `https://fabrikam.com/blog` 页面，此页面显示它使用 **/article-1** 参数检索到的内容。

## <a name="override-a-parameterized-url-with-a-custom-page"></a>使用自定义页面替代参数化 URL

要在 Commerce 站点构建器中使用自定义页面替代参数化 URL，请按照下列步骤操作。

1. 转到 **URL**，选择 **新建 \> 新建 URL**。
1. 在 **创建新 URL** 对话框中，选择 **内部页面**。 在 **URL 路径** 下，输入包含要替代的段的路径（在此示例中为 **/blog/about-this-blog**）。 然后选择 **下一步**。
1. 在 **选择页面** 对话框中，选择自定义页面，然后选择 **保存**。
1. 选择 **发布**。
1. 如果自定义页面尚未发布，转到 **页面**，选择自定义页面，然后选择 **发布**。

自定义页面发布后，将提供该页面，而不是包含参数化内容的动态页面。

## <a name="additional-resources"></a>其他资源

[修改现有的站点页面](modify-existing-page.md)

[添加新的站点页面](add-new-page.md)

[选择页面布局](select-page-layouts.md)

[管理 SEO 元数据](manage-seo-metadata.md)

[保存、预览和发布页面](save-preview-publish-page.md)

[丰富产品页面](enrich-product-page.md)

[丰富类别登陆页面](enrich-category-page.md)

[验证页面内容的可访问性](verify-accessibility.md)

[在线渠道可扩展性](e-commerce-extensibility/overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
