---
title: 导入和导出评分和评价
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 中导入和导出产品评分和评价。
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: f369e3cd208cdfba816f817ead75374ee6982912
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271927"
---
# <a name="import-and-export-ratings-and-reviews"></a>导入和导出评分和评价

[!include [banner](includes/banner.md)]

本文介绍如何在 Microsoft Dynamics 365 Commerce 中导入和导出产品评分和评价。

Dynamics 365 Commerce 提供[评分和评价](ratings-reviews-overview.md)作为全渠道解决方案。 当您切换到 Dynamics 365 Commerce 评分和评价解决方案时，您可能需要将现有的评分和评价数据移至 Commerce 平台。 您可能还希望根据业务要求从 Commerce 导出评分和评价数据。 通过 Power Automate 连接器，您可以将评分和评价导入 Commerce 并从 Commerce 中导出。

> [!NOTE]
> 有关如何在 Power Automate 中开始使用逻辑流的信息，请参阅[在 Power Automate 中创建云端流](/power-automate/get-started-logic-flow)。

## <a name="prerequisites"></a>先决条件

在导入和导出评分和评价之前，必须满足以下先决条件：

- 必须在 Commerce 平台上为您的电子商务站点启用评分和评价解决方案。 有关详细信息，请参阅[选择使用评分和评价](opt-in-ratings-reviews.md)。
- 必须配置 Dynamics 365 评分和评价 Power App 连接器，才能在 Power Automate 中启用“提交评价”或“导出评价”操作。 有关详细信息，请参阅 [Dynamics 365 Commerce - 评分和评价（预览版）](/connectors/dynamics365ratingsre/)。
- 必须配置服务对服务 (S2S) 身份验证，才能从 Commerce 外部安全地调用评分和评价应用编程接口 (API)。 有关详细信息，请参阅[配置服务对服务身份验证](service-to-service-auth.md)。

## <a name="import-ratings-and-reviews"></a>导入评分和评价

若要将评分和评价数据从现有系统导入到 Commerce，您必须将 Dynamics 365 评分和评价 Power Automate 连接器添加到现有的 Power Automate 流或新流。 有关详细信息，请参阅 [Dynamics 365 Commerce - 评分和评价（预览版）](/connectors/dynamics365ratingsre/)。

> [!IMPORTANT]
> 在完成此过程之前，您必须[配置 S2S 身份验证](service-to-service-auth.md)。

要使用 Dynamics 365 评分和评价 Power Automate 连接器将评分和评价导入到 Commerce，请按照以下步骤进行操作。

1. 选择 **提交提交用户评价** 操作。
1. 使用配置 S2S 身份验证时创建的 Azure Active Directory (Azure AD) 应用信息建立连接。 有关详细信息，请参阅[配置服务对服务身份验证](service-to-service-auth.md)。
1. **提交用户评价** 操作一次提交一个评价。 因此，请重复此操作。 使用源评价作为列表提交批量评价。
    
## <a name="export-ratings-and-reviews"></a>导出评分和评价

若要从 Commerce 导出评分和评价数据，您必须将 Dynamics 365 评分和评价 Power Automate 连接器添加到现有的 Power Automate 流或新流。 有关详细信息，请参阅 [Dynamics 365 Commerce - 评分和评价（预览版）](/connectors/dynamics365ratingsre/)。

要使用 Dynamics 365 评分和评价 Power Automate 连接器从 Commerce 中导出评分和评价，请按照以下步骤进行操作。

1. 选择 **导出所有评价** 操作。
1. 完成此操作。 

## <a name="additional-resources"></a>其他资源

[评分和评价概览](ratings-reviews-overview.md)

[选择使用评分和评价](opt-in-ratings-reviews.md)

[管理评分和评价](manage-reviews.md)

[配置评分和评价](configure-ratings-reviews.md)

[同步产品评分](sync-product-ratings.md)

[启用审查者手动发布评分和评价](manual-publish-rating-reviews.md)

[配置服务对服务身份验证](service-to-service-auth.md)

[评分和评价常见问题解答](ratings-reviews-faq.md)
