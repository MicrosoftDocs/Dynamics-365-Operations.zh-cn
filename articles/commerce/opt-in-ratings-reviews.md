---
title: 选择使用评分和评价
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 站点中选择使用评分和评价。
author: gvrmohanreddy
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fd6715539693389f25800a40c0beffcdc1b0de72
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/13/2022
ms.locfileid: "7967995"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>选择使用评分和评价

[!include [banner](includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics 365 Commerce 站点中选择使用评分和评价。

评分和评价解决方案是可通过使用 Microsoft Dynamics Lifecycle Services (LCS) 在 Dynamics 365 Commerce 中启用的全渠道解决方案。 LCS 是零售商用于管理环境（从预配到停用）的管理门户。

如果要在 Commerce 网站中使用评分和评价解决方案，您必须在 Dynamics 365 Commerce 上部署电子商务站点期间选择使用评分和评价。

## <a name="opt-in-to-use-ratings-and-reviews"></a>选择使用评分和评价

若要在站点中选择使用评分和评价，请执行以下步骤。

1. 执行[部署新电子商务站点](deploy-ecommerce-site.md)中的步骤。
1. 还在 LCS 中时，转到 **Retail 部署设置 \> 其他设置**。
1. 将 **启用评分和评价服务** 选项设置为 **是**。
1. 在 **评分和评价审查者的 AAD 安全组(安全组对象 ID)** 字段中，输入其中包含评分和评价审查者的 Microsoft Azure Active Directory (Azure AD) 安全组的 ID。

    ![选择使用评分和评价。](media/LCS_RnR_Preference.png)

1. 完成电子商务初始化流程。

> [!NOTE] 
> 如果您是现有的 Dynamics 365 Commerce 客户，已经部署了电子商务站点而未选择使用评分和评价，但现在想要使用 Dynamics 365 Commerce 包中的评分和评价，请提交服务请求。 有关如何提交服务请求的信息，请参阅[提交服务请求流程](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json)。 

## <a name="additional-resources"></a>其他资源

[评分和评价概览](ratings-reviews-overview.md)

[管理评分和评价](manage-reviews.md)

[配置评分和评价](configure-ratings-reviews.md)

[在 Dynamics 365 Commerce 中同步产品评分](sync-product-ratings.md)

[启用审查者手动发布评分和评价](manual-publish-rating-reviews.md)

[导入和导出评分和评价](import-export-reviews.md)

[配置服务对服务身份验证](service-to-service-auth.md)

[评分和评价常见问题解答](ratings-reviews-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
