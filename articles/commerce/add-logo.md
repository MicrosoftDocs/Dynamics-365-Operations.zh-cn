---
title: 添加徽标
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中向您的站点添加徽标。
author: bicyclingfool
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 143c1ab33547119ceab0a4fba165669bc8b22bf4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207571"
---
# <a name="add-a-logo"></a>添加徽标

[!include [banner](includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics 365 Commerce 中向您的站点添加徽标。

## <a name="overview"></a>概览

建立站点时，您可能要做的第一件事就是将公司或品牌徽标添加到站点页眉中。 Dynamics 365 Commerce 在线模块库提供了让此任务轻松实现的模块。

您可以将徽标直接添加到模板、布局或页面中。 这样，您可以轻松地更改出现在特定页面或页面组上的徽标。 但本主题介绍最常见的场景：您将徽标添加到可以在站点的所有页面上重复使用的页眉片段中。

## <a name="prerequisites"></a>先决条件

您必须先完成以下任务，才能将徽标添加到站点的所有页面。

1. 将徽标上传到媒体库。
1. 创建页眉片段。 有关如何创建和使用片段的详细信息，请参阅[使用片段](work-with-fragments.md)。
1. 在站点的页面用来建立布局和模块选项的模板中包含页眉片段。 有关模板的详细信息，请参阅[使用模板](work-with-templates.md)。

## <a name="add-a-logo-to-a-header-fragment"></a>将徽标添加到页眉片段

要将徽标添加到您的站点的页眉片段，请按照下列步骤操作。

1. 在左侧的导航窗格中，选择 **片段**。
1. 选择前面创建的页眉片段，然后选择 **编辑**。
1. 展开页眉模块。
1. 在页眉模块的属性窗格中，提供徽标的图像和链接。 
1. 保存页眉片段，完成编辑，然后发布。

发布更新的页眉片段后，所有使用包含页眉片段的模板的站点页面都将显示您的徽标。

## <a name="additional-resources"></a>其他资源

[选择站点主题](select-site-theme.md)

[处理 CSS 覆盖文件](css-override-files.md)

[添加收藏夹图标](add-favicon.md)

[添加欢迎消息](add-welcome-message.md)

[添加版权声明](add-copyright-notice.md)

[向站点添加语言](add-languages-to-site.md)

[将脚本代码添加到站点页面以支持遥测](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]