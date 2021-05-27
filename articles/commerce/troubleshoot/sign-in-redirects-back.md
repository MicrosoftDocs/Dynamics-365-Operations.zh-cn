---
title: 登录链接重定向回电子商务站点
description: 本主题提供故障排除指南，当登录链接重定向回电子商务站点而不是转到登录页面时，该指南可以提供帮助。
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
ms.openlocfilehash: a1d0ae4e487c391020947c607d5d7cb5d1ba6af4
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020595"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a><span data-ttu-id="f4855-103">登录链接重定向回电子商务站点</span><span class="sxs-lookup"><span data-stu-id="f4855-103">Sign-in link redirects back to an e-commerce site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f4855-104">本主题提供故障排除指南，当登录链接重定向回电子商务站点而不是转到登录页面时，该指南可以提供帮助。</span><span class="sxs-lookup"><span data-stu-id="f4855-104">This topic provides troubleshooting guidance that can help when a sign-in link redirects back to the e-commerce site instead of going to the sign-in page.</span></span>

## <a name="description"></a><span data-ttu-id="f4855-105">说明</span><span class="sxs-lookup"><span data-stu-id="f4855-105">Description</span></span>

<span data-ttu-id="f4855-106">在 Commerce 站点构建器中配置新的 Microsoft Azure Active Directory B2C (Azure AD B2C) 租户后，选择 **登录** 链接的用户被重定向回电子商务主登陆页面，而不是转到登录页面。</span><span class="sxs-lookup"><span data-stu-id="f4855-106">After you configure a new Microsoft Azure Active Directory B2C (Azure AD B2C) tenant in Commerce site builder, users who select the **Sign in** link are redirected back to the main e-commerce landing page without going to the sign-in page.</span></span>

## <a name="resolution"></a><span data-ttu-id="f4855-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="f4855-107">Resolution</span></span>

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a><span data-ttu-id="f4855-108">确认是否已在 Azure AD B2C 应用中正确配置了回复 URL</span><span class="sxs-lookup"><span data-stu-id="f4855-108">Confirm that the reply URL is correctly configured in the Azure AD B2C application</span></span>

<span data-ttu-id="f4855-109">要确认是否已在 Azure AD B2C 应用中正确配置了回复 URL，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="f4855-109">To confirm that the reply URL is correctly configured in the Azure AD B2C application, follow these steps.</span></span>

1. <span data-ttu-id="f4855-110">转到 [Azure 门户](https://portal.azure.com/)。</span><span class="sxs-lookup"><span data-stu-id="f4855-110">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="f4855-111">选择您为站点访问而创建的 Azure AD B2C 应用程序。</span><span class="sxs-lookup"><span data-stu-id="f4855-111">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="f4855-112">选择您在 Azure AD B2C 设置期间创建的应用程序。</span><span class="sxs-lookup"><span data-stu-id="f4855-112">Select the application that you created during the Azure AD B2C setup.</span></span>
1. <span data-ttu-id="f4855-113">在 **回复 URL** 下面，请确保该列表同时包含站点域 URL 和电子商务生成的 URL 的条目，如以下插图中的示例所示。</span><span class="sxs-lookup"><span data-stu-id="f4855-113">Under **Reply URL**, make sure that the list includes entries for both the site domain URL and the e-commerce-generated URL, as shown in the example in the following illustration.</span></span>

    ![Azure AD B2C 回复 URL 条目](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> <span data-ttu-id="f4855-115">站点域 URL 和电子商务生成的 URL 都必须采用有效的 URL 格式，此格式不包含前导斜杠或尾随斜杠。</span><span class="sxs-lookup"><span data-stu-id="f4855-115">Both the site domain URL and the e-commerce-generated URL must be in a valid URL format that doesn't include leading or trailing slashes.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4855-116">其他资源</span><span class="sxs-lookup"><span data-stu-id="f4855-116">Additional resources</span></span>

[<span data-ttu-id="f4855-117">在 Azure Active Directory B2C 中注册 Web 应用程序</span><span class="sxs-lookup"><span data-stu-id="f4855-117">Register a web application in Azure Active Directory B2C</span></span>](/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[<span data-ttu-id="f4855-118">在 Commerce 中设置 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="f4855-118">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)