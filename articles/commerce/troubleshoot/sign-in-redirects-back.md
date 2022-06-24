---
title: 登录链接重定向回电子商务站点
description: 本文提供故障排除指南，当登录链接重定向回电子商务站点而不是转到登录页面时，该指南可以提供帮助。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5274599ee5ea23c18648d95431b2e79ebca12dea
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860210"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a>登录链接重定向回电子商务站点

[!include [banner](../../includes/banner.md)]

本文提供故障排除指南，当登录链接重定向回电子商务站点而不是转到登录页面时，该指南可以提供帮助。

## <a name="description"></a>说明

在 Commerce 站点构建器中配置新的 Microsoft Azure Active Directory B2C (Azure AD B2C) 租户后，选择 **登录** 链接的用户被重定向回电子商务主登陆页面，而不是转到登录页面。

## <a name="resolution"></a>解决方法

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a>确认是否已在 Azure AD B2C 应用中正确配置了回复 URL

要确认是否已在 Azure AD B2C 应用中正确配置了回复 URL，请按照以下步骤操作。

1. 转到 [Azure 门户](https://portal.azure.com/)。
1. 选择您为站点访问而创建的 Azure AD B2C 应用程序。
1. 选择您在 Azure AD B2C 设置期间创建的应用程序。
1. 在 **回复 URL** 下面，请确保该列表同时包含站点域 URL 和电子商务生成的 URL 的条目，如以下插图中的示例所示。

    ![Azure AD B2C 回复 URL 条目。](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> 站点域 URL 和电子商务生成的 URL 都必须采用有效的 URL 格式，此格式不包含前导斜杠或尾随斜杠。

## <a name="additional-resources"></a>其他资源

[在 Azure Active Directory B2C 中注册 Web 应用程序](/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[在 Commerce 中设置 B2C 租户](../set-up-b2c-tenant.md)