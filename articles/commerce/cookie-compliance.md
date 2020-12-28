---
title: Cookie 合规
description: 本主题介绍 Cookie 合规注意事项以及 Microsoft Dynamics 365 Commerce 中包含的默认政策。
author: BrianShook
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4f54b9b8130a167dbecdb13fccd7039f827f6ed0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410386"
---
# <a name="cookie-compliance"></a><span data-ttu-id="ec0fa-103">Cookie 合规</span><span class="sxs-lookup"><span data-stu-id="ec0fa-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ec0fa-104">本主题介绍 Cookie 合规注意事项以及 Microsoft Dynamics 365 Commerce 中包含的默认政策。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ec0fa-105">概览</span><span class="sxs-lookup"><span data-stu-id="ec0fa-105">Overview</span></span>

<span data-ttu-id="ec0fa-106">当跟踪影响电子商务客户的技术时，隐私是一个重要因素。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-106">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="ec0fa-107">由于诸如欧盟 (EU) 的一般数据保护条例 (GDPR) 等隐私合规标准，今天处于活动状态的任何站点都必须考虑电子隐私准则。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-107">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="ec0fa-108">由于默认情况下许多电子商务站点在全球范围内都可以访问，因此审查电子商务站点的合规标准很重要。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-108">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="ec0fa-109">要了解有关 Microsoft 针对 Cookie 合规使用的基本原则的详细信息，请访问 [Microsoft 信任中心](https://www.microsoft.com/trust-center)。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-109">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="ec0fa-110">在该站点上，您还可以获得有关合规和隐私区域的更多信息。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-110">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="ec0fa-111">下表显示了 Dynamics 365 Commerce 站点放置的 cookie 的当前参考列表。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-111">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="ec0fa-112">Cookie 名称</span><span class="sxs-lookup"><span data-stu-id="ec0fa-112">Cookie name</span></span>                               | <span data-ttu-id="ec0fa-113">用法</span><span class="sxs-lookup"><span data-stu-id="ec0fa-113">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="ec0fa-114">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="ec0fa-114">.AspNet.Cookies</span></span>                             | <span data-ttu-id="ec0fa-115">存储用于单点登录的 (SSO) 的 Microsoft Azure Active Directory (Azure AD) 身份验证 cookie。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-115">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="ec0fa-116">存储加密的用户主体信息（名字、姓氏、电子邮件）。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-116">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="ec0fa-117">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="ec0fa-117">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="ec0fa-118">存储用于获取已添加到购物车实例的产品列表的购物车 ID。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-118">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="ec0fa-119">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="ec0fa-119">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="ec0fa-120">Cookie 合规性同意跟踪。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-120">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="ec0fa-121">ai_session</span><span class="sxs-lookup"><span data-stu-id="ec0fa-121">ai_session</span></span>                                  | <span data-ttu-id="ec0fa-122">检测有多少用户活动会话已包含应用的某些页面和功能。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-122">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="ec0fa-123">ai_user</span><span class="sxs-lookup"><span data-stu-id="ec0fa-123">ai_user</span></span>                                     | <span data-ttu-id="ec0fa-124">检测有多少人使用了应用及其功能。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-124">Detects how many people used the app and its features.</span></span> <span data-ttu-id="ec0fa-125">使用匿名 ID 对用户进行计数。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-125">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="ec0fa-126">b2cru</span><span class="sxs-lookup"><span data-stu-id="ec0fa-126">b2cru</span></span>                                       | <span data-ttu-id="ec0fa-127">动态存储重定向 URL。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-127">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="ec0fa-128">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="ec0fa-128">JSESSIONID</span></span>                                  | <span data-ttu-id="ec0fa-129">由付款连接器 Adyen 用来存储用户会话。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-129">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="ec0fa-130">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="ec0fa-130">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="ec0fa-131">身份验证</span><span class="sxs-lookup"><span data-stu-id="ec0fa-131">Authentication</span></span>                                               |
| <span data-ttu-id="ec0fa-132">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="ec0fa-132">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="ec0fa-133">用于维护请求状态。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-133">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="ec0fa-134">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="ec0fa-134">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="ec0fa-135">用于防御 CRSF 的跨网站请求伪造 (CRSF) 令牌。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-135">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="ec0fa-136">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="ec0fa-136">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="ec0fa-137">用于将请求路由到适当的生产身份验证服务器实例。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-137">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="ec0fa-138">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="ec0fa-138">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="ec0fa-139">用于将请求路由到适当的生产身份验证服务器实例。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-139">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="ec0fa-140">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="ec0fa-140">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="ec0fa-141">用于将请求路由到适当的生产身份验证服务器实例。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-141">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="ec0fa-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="ec0fa-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="ec0fa-143">用于维护 SSO 会话。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-143">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="ec0fa-144">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="ec0fa-144">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="ec0fa-145">用于跟踪事务（对企业对消费者 (B2C) 站点进行身份验证的打开选项卡的数量），包括当前事务。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-145">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a><span data-ttu-id="ec0fa-146">电子商务站点中的站点用户 cookie 同意</span><span class="sxs-lookup"><span data-stu-id="ec0fa-146">Site user cookie consent on an e-Commerce site</span></span> 

<span data-ttu-id="ec0fa-147">如果模块中的电子商务站点功能使用非基本 cookie，则必须先获取站点用户的同意，然后才能跟踪 cookie。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-147">If an e-Commerce site feature or module uses a non-essential cookie, a site user's consent must be obtained before the cookie is tracked.</span></span> <span data-ttu-id="ec0fa-148">若要允许站点用户在电子商务站点中提供 cookie 同意，站点作者必须在页面的页眉中添加和配置 cookie 同意模块，以确保提示提供和接收同意。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-148">To allow site users to provide cookie consent on the e-Commerce site, a site author must add and configure a cookie consent module in the page's header module to ensure that the consent is prompted for and received.</span></span> <span data-ttu-id="ec0fa-149">必须先提供站点用户同意，然后才能在站点页面中显示使用非基本 cookie 的功能或模块。</span><span class="sxs-lookup"><span data-stu-id="ec0fa-149">Site user consent must be given before a feature or module using a non-essential cookie can be rendered on a site page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ec0fa-150">其他资源</span><span class="sxs-lookup"><span data-stu-id="ec0fa-150">Additional resources</span></span>

[<span data-ttu-id="ec0fa-151">辅助功能和功能</span><span class="sxs-lookup"><span data-stu-id="ec0fa-151">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="ec0fa-152">合规性概览</span><span class="sxs-lookup"><span data-stu-id="ec0fa-152">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="ec0fa-153">添加隐私政策页面</span><span class="sxs-lookup"><span data-stu-id="ec0fa-153">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="ec0fa-154">替换与所跟踪内容更改相关联的用户 ID</span><span class="sxs-lookup"><span data-stu-id="ec0fa-154">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

[<span data-ttu-id="ec0fa-155">Cookie 同意模块</span><span class="sxs-lookup"><span data-stu-id="ec0fa-155">Cookie consent module</span></span>](cookie-consent-module.md) 
 
[<span data-ttu-id="ec0fa-156">标题模块</span><span class="sxs-lookup"><span data-stu-id="ec0fa-156">Header module</span></span>](author-header-module.md)
