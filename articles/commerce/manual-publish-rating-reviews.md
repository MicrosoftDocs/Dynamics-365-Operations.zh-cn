---
title: 启用审查者手动发布评分和评价
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 中启用审查者手动发布评分和评价，以及如何手动发布评分和评价。
author: gvrmohanreddy
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
manager: annbe
ms.openlocfilehash: 6591e18ff8e83ec9030d91d8348271b8113e453f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276767"
---
# <a name="enable-manual-publishing-of-ratings-and-reviews-by-a-moderator"></a>启用审查者手动发布评分和评价

[!include [banner](includes/banner.md)]

本文介绍如何在 Microsoft Dynamics 365 Commerce 中启用审查者手动发布评分和评价，以及如何手动发布评分和评价。

Dynamics 365 Commerce 的评分和评价解决方案使用 Azure Cognitive Services 自动修正评价的标题和内容中的侮辱性内容和发布评分和评价。 因此，无需手动干预即可审阅评分和评价和将其发布到您的电子商务站点。

但是，某些企业可能更希望审查者先手动审阅和审核评价，再发布。 若要启用审查者手动发布评分和评价，必须在站点生成器中启用 **评分和评价需要审查者** 功能。

## <a name="enable-the-require-moderator-for-ratings-and-reviews-feature-in-commerce-site-builder"></a>在 Commerce 站点生成器中启用“评级和评论需要审查者”功能

若要在 Commerce 站点生成器中启用 **评分和评价需要审查者** 功能，请执行以下步骤。

1. 转到 **主页 \> 审阅 \> 设置**。
1. 将 **评分和评价需要审查者** 选项设置为 **开**。

> [!NOTE]
> 启用 **评分和评价需要审查者** 功能即停止评分和评价自动发布功能，因此现在需要手动发布。 但是，Azure Cognitive Services 将继续修正评论的标题和内容中的侮辱性内容。

<!--![Require moderator for ratings and reviews setting in Commerce site builder.](media/Ratings-reviews-settings-human-moderation.png)-->

## <a name="publish-ratings-and-reviews"></a>发布评分和评价

启用 **评分和评价需要审查者** 功能后，评分和评价必须先由审查者手动审阅并发布，才会在您的电子商务站点中显示。

若要在 Commerce 站点生成器中审阅和发布评分和评价，请执行以下步骤。

1. 转到 **审阅 \> 审查**。
1. 在此网格中，如果行的 **状态** 字段设置为 **未发布**，说明该行中的评分和评价尚未发布。 若要仅查看未发布的评分和评论，请在网格上方的状态筛选器中选择 **状态: 需要审阅**。
1. 选择一个或多个状态为 **未发布** 的评分和评论，然后在命令栏上选择 **发布**。 所选评分和评论将添加到发布队列中，并将在发布后显示在电子商务站点中。

> [!NOTE]
> - 评分和评价发布后，状态值将从 **未发布** 更改为空值（空白字段）。
> - 如果选择多个混合状态的评分和评价，然后选择 **发布**，将发布尚未发布的评分和评价。 但是，不会再次发布已发布的评分和评价。

下图显示了一个示例，其中在 Commerce 站点生成器的 **审查** 页面上选择了三个未发布的评分和评价。

![Commerce 站点生成器的“审查”页面中选择了三个未发布的评分和评价。](media/Ratings-reviews-publishing-reviews.png)

<!--![Dynamics 365 Commerce - Ratings and Review configuration 2](media/Ratings-reviews-published-reviews.png)-->
<!--![Status filter](media/Ratings-reviews-published-reviews-status-filter.png)-->

## <a name="additional-resources"></a>其他资源

[评分和评价概览](ratings-reviews-overview.md)

[选择使用评分和评价](opt-in-ratings-reviews.md)

[管理评分和评价](manage-reviews.md)

[配置评分和评价](configure-ratings-reviews.md)

[同步产品评分](sync-product-ratings.md)

[导入和导出评分和评价](import-export-reviews.md)

[配置服务对服务身份验证](service-to-service-auth.md)

[评分和评价常见问题解答](ratings-reviews-faq.md)
