---
title: Cookie 同意模块
description: 此主题介绍 cookie 同意模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 60ce530575841c22355e4a14e8b0bbec6c0e35ab
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410385"
---
# <a name="cookie-consent-module"></a>Cookie 同意模块

[!include [banner](includes/banner.md)]

此主题介绍 cookie 同意模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

## <a name="overview"></a>概览

cookie 同意模块提示站点用户明确提供同意，以便允许跟踪浏览器 cookie 的任何功能或模块的 cookie。 站点用户在新浏览器会话中浏览站点时，需要此同意。 收到同意后，将进行跟踪，并且不会再次提示站点用户提供同意。 有关详细信息，请参阅 [Cookie 合规性](cookie-compliance.md)。

如果未收到用户 cookie 同意，页面中将不显示需要 cookie 同意的任何功能或模块。 例如，结帐模块、社交共享模块和首选商店模块全都需要 cookie 同意，并且如果未收到站点用户同意，将不显示。 

可以在页面的页眉片段中配置 cookie 同意模块，以便在页面加载时实施该模块。 cookie 同意模块中应该包含明确的消息，以便告知站点用户站点中的 cookie 使用情况，还应提供站点隐私页面的链接。

下图突出显示了 cookie 同意消息和站点页面中显示的站点隐私政策页面的链接的示例。
![cookie 同意模块的示例](./media/ecommerce-cookieconsent.png)

## <a name="cookie-consent-module-properties"></a>Cookie 同意模块属性

| 属性名称             | 值                 | 说明 |
|---------------------------|-----------------------|-------------|
| 富文本                  | 富文本 | 指定富文本通知，以便通知用户，说明站点在使用浏览器 cookie，并且用户应该接受使用 cookie，站点才能完全正常运行。 |
| 链接 | URL | 可以将一个或多个链接添加到站点的隐私页面，以介绍站点中跟踪的 cookie 的类型。 |

## <a name="add-a-cookie-consent-module-to-site-pages"></a>向站点页面添加 cookie 同意模块

若要有效地将一个 cookie 同意模块添加到多个站点页面，可以将其添加到共享页面标题片段。 将标题片段添加到所有站点页面之后，站点用户首次浏览到任何站点页面时，将自动显示 cookie 同意通知。

有关标题片段和模块的详细信息，请参阅[标题模块](author-header-module.md)。

## <a name="additional-resources"></a>其他资源

[模块库概述](starter-kit-overview.md)

[标题模块](author-header-module.md) 

[Cookie 合规性](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]