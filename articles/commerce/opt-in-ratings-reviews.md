---
title: 选择使用评分和评价
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 站点中选择使用评分和评价。
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
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
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10e3c33af232fa46df09a103b2e73eae09a909eb
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697972"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>选择使用评分和评价

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics 365 Commerce 站点中选择使用评分和评价。

## <a name="overview"></a>概览

评分和评价解决方案是可通过使用 Microsoft Dynamics Lifecycle Services (LCS) 在 Dynamics 365 Commerce 中启用的全渠道解决方案。 LCS 是零售商用于管理环境（从预配到停用）的管理门户。

如果要在 Commerce 网站中使用评分和评价解决方案，必须先选择使用。

## <a name="opt-in-to-use-ratings-and-reviews"></a>选择使用评分和评价

若要在站点中选择使用评分和评价，请执行以下步骤。

1. 执行[部署新电子商务站点](deploy-ecommerce-site.md)中的步骤。
1. 还在 LCS 中时，转到 **Retail 部署设置 \> 其他设置**。
1. 将**启用评分和评价服务**选项设置为**是**。
1. 在**评分和评价审查者的 AAD 安全组(安全组对象 ID)** 字段中，输入其中包含评分和评价审查者的 Microsoft Azure Active Directory (Azure AD) 安全组的 ID。

    ![选择使用评分和评价](media/LCS_RnR_Preference.png)

1. 完成电子商务初始化流程。

## <a name="additional-resources"></a>其他资源

[评分和评价概览](ratings-reviews-overview.md)

[管理评分和评价](manage-reviews.md)

[配置评分和评价](configure-ratings-reviews.md)

[在 Dynamics 365 Retail 中同步产品评分](sync-product-ratings.md)
