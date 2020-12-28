---
title: 身份验证
description: 本文提供有关如何通过 Microsoft Dynamics 365 Human Resources 数据应用程序编程接口 (API) 进行身份验证的概述信息。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a0509ce99205d49d516e180203ffb65a1dc09a7c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417390"
---
# <a name="authentication"></a><span data-ttu-id="591c0-103">身份验证</span><span class="sxs-lookup"><span data-stu-id="591c0-103">Authentication</span></span>

<span data-ttu-id="591c0-104">本文提供有关如何通过 Microsoft Dynamics 365 Human Resources 数据应用程序编程接口 (API) 进行身份验证的概述信息。</span><span class="sxs-lookup"><span data-stu-id="591c0-104">This article provides overview information about how to authenticate with the Microsoft Dynamics 365 Human Resources data application programming interface (API).</span></span>

## <a name="overview"></a><span data-ttu-id="591c0-105">概览</span><span class="sxs-lookup"><span data-stu-id="591c0-105">Overview</span></span>

<span data-ttu-id="591c0-106">Human Resources 的数据 API 是一个 OData 实现。</span><span class="sxs-lookup"><span data-stu-id="591c0-106">The data API for Human Resources is an OData implementation.</span></span> <span data-ttu-id="591c0-107">有关详细信息，请参阅[开放数据协议 (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md)。</span><span class="sxs-lookup"><span data-stu-id="591c0-107">For more information, see [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span></span>

<span data-ttu-id="591c0-108">在 API 为来自您的应用程序的请求提供服务之前，您的应用程序必须先作为授权调用方进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="591c0-108">Your application must authenticate as an authorized caller before the API will service requests from your application.</span></span>

## <a name="fundamentals"></a><span data-ttu-id="591c0-109">基本原理</span><span class="sxs-lookup"><span data-stu-id="591c0-109">Fundamentals</span></span>

<span data-ttu-id="591c0-110">要调用数据 API，您的应用程序必须从 Microsoft 身份平台获取访问令牌。</span><span class="sxs-lookup"><span data-stu-id="591c0-110">To call the data API, your application must acquire an access token from the Microsoft identity platform.</span></span> <span data-ttu-id="591c0-111">访问令牌包含有关您的应用程序的信息，以及它必须具有的调用 Human Resources 中的资源的权限。</span><span class="sxs-lookup"><span data-stu-id="591c0-111">The access token contains information about your application and the permission that it has to call resources in Human Resources.</span></span>

### <a name="access-token"></a><span data-ttu-id="591c0-112">访问令牌</span><span class="sxs-lookup"><span data-stu-id="591c0-112">Access token</span></span>

<span data-ttu-id="591c0-113">Microsoft 身份平台发布的访问令牌是 base64 编码的 JavaScript Object Notation (JSON) Web 令牌 (JWT)。</span><span class="sxs-lookup"><span data-stu-id="591c0-113">Access tokens issued by the Microsoft identity platform are base64–encoded JavaScript Object Notation (JSON) Web Tokens (JWTs).</span></span> <span data-ttu-id="591c0-114">它们包含数据 API（以及 Microsoft 身份平台保护的其他 Web API）用来验证调用方并确保调用方具有执行他们所请求的操作的正确权限的信息（声明）。</span><span class="sxs-lookup"><span data-stu-id="591c0-114">They contain information (claims) that the data API (and other web APIs that are secured by the Microsoft identity platform) use to validate the caller and make sure that the caller has the correct permissions to perform the operation they're requesting.</span></span> <span data-ttu-id="591c0-115">调用期间，您可以将访问令牌视为不透明。</span><span class="sxs-lookup"><span data-stu-id="591c0-115">During calls, you can treat access tokens as opaque.</span></span> <span data-ttu-id="591c0-116">您应该始终通过安全通道传输访问令牌，例如传输层安全性 (TLS) 和安全超文本传输协议 (HTTPS)。</span><span class="sxs-lookup"><span data-stu-id="591c0-116">You should always transmit access tokens over a secure channel, such as Transport Layer Security (TLS) and Hypertext Transfer Protocol Secure (HTTPS).</span></span>

<span data-ttu-id="591c0-117">这里是 Microsoft 身份平台发布的访问令牌的示例。</span><span class="sxs-lookup"><span data-stu-id="591c0-117">Here is an example of an access token that is issued by the Microsoft identity platform.</span></span>

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

<span data-ttu-id="591c0-118">要调用数据 API，请将访问令牌作为不记名令牌附加到 HTTP 请求中的授权标头中。</span><span class="sxs-lookup"><span data-stu-id="591c0-118">To call the data API, you attach the access token as a bearer token to the authorization header in your HTTP request.</span></span> <span data-ttu-id="591c0-119">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="591c0-119">Here is an example.</span></span>

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a><span data-ttu-id="591c0-120">使用 Azure 门户注册新应用程序</span><span class="sxs-lookup"><span data-stu-id="591c0-120">Register a new application by using the Azure portal</span></span>

1. <span data-ttu-id="591c0-121">使用工作或学校帐户或个人 Microsoft 帐户登录 [Microsoft Azure 门户](https://portal.azure.com)。</span><span class="sxs-lookup"><span data-stu-id="591c0-121">Sign in to the [Microsoft Azure portal](https://portal.azure.com) with a work or school account, or a personal Microsoft account.</span></span>

2. <span data-ttu-id="591c0-122">如果您的帐户允许您访问多个租户，请在右上角选择您的帐户，然后将门户会话设置为您需要的 Azure Active Directory (Azure AD) 租户。</span><span class="sxs-lookup"><span data-stu-id="591c0-122">If your account gives you access to more than one tenant, select your account in the upper-right corner, and set your portal session to the Azure Active Directory (Azure AD) tenant that you want.</span></span>

3. <span data-ttu-id="591c0-123">在左窗格中，选择 **Azure Active Directory** 服务，然后选择 **应用注册 \> 新注册**。</span><span class="sxs-lookup"><span data-stu-id="591c0-123">In the left pane, select the **Azure Active Directory** service, and then select **App registrations \> New registration**.</span></span>

4. <span data-ttu-id="591c0-124">当 **注册应用程序** 页面出现时，输入您的应用程序的注册信息：</span><span class="sxs-lookup"><span data-stu-id="591c0-124">When the **Register an application** page appears, enter your application's registration information:</span></span>

    - <span data-ttu-id="591c0-125">**名称**：输入一个有意义的应用程序名称，它将显示给应用用户。</span><span class="sxs-lookup"><span data-stu-id="591c0-125">**Name**: Enter a meaningful application name that will be shown to users of the app.</span></span>
    - <span data-ttu-id="591c0-126">**支持的帐户类型**：选择您的应用应该支持的帐户类型。</span><span class="sxs-lookup"><span data-stu-id="591c0-126">**Supported account types**: Select the types of accounts that your app should support.</span></span>

        | <span data-ttu-id="591c0-127">支持的科目类型</span><span class="sxs-lookup"><span data-stu-id="591c0-127">Supported account types</span></span> | <span data-ttu-id="591c0-128">说明</span><span class="sxs-lookup"><span data-stu-id="591c0-128">Description</span></span> |
        |-------------------------|-------------|
        | <span data-ttu-id="591c0-129">仅此组织目录中的帐户</span><span class="sxs-lookup"><span data-stu-id="591c0-129">Accounts in this organizational directory only</span></span> | <span data-ttu-id="591c0-130">如果要构建行业应用，请选择此选项。</span><span class="sxs-lookup"><span data-stu-id="591c0-130">Select this option if you're building a line-of-business app.</span></span> <span data-ttu-id="591c0-131">除非您在目录中注册应用，否则此选项不可用。</span><span class="sxs-lookup"><span data-stu-id="591c0-131">This option isn't available unless you're registering the app in a directory.</span></span><p><span data-ttu-id="591c0-132">此选项将映射到 **仅 Azure AD 单租户**。</span><span class="sxs-lookup"><span data-stu-id="591c0-132">This option is mapped to **Azure AD only single-tenant**.</span></span></p><p><span data-ttu-id="591c0-133">除非您在目录外部注册应用，否则此选项是默认选项。</span><span class="sxs-lookup"><span data-stu-id="591c0-133">This option is the default option unless you're registering the app outside a directory.</span></span> <span data-ttu-id="591c0-134">在这种情况下，默认选项是 **Azure AD 多租户和个人 Microsoft 帐户**。</span><span class="sxs-lookup"><span data-stu-id="591c0-134">In that case, the default option is **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p> |
        | <span data-ttu-id="591c0-135">任何组织目录中的帐户</span><span class="sxs-lookup"><span data-stu-id="591c0-135">Accounts in any organizational directory</span></span> | <span data-ttu-id="591c0-136">选择此选项以定位所有商业和教育客户。</span><span class="sxs-lookup"><span data-stu-id="591c0-136">Select this option to target all business and educational customers.</span></span><p><span data-ttu-id="591c0-137">此选项将映射到 **仅 Azure AD 多租户**。</span><span class="sxs-lookup"><span data-stu-id="591c0-137">This option is mapped to **Azure AD only multi-tenant**.</span></span></p><p><span data-ttu-id="591c0-138">如果您将应用注册为 **仅 Azure AD 单租户**，您可以使用 **身份验证** 边栏选项卡将应用更新为 **仅 Azure AD 多租户**，然后返回 **仅 Azure AD 单租户**。</span><span class="sxs-lookup"><span data-stu-id="591c0-138">If you registered the app as **Azure AD only single-tenant**, you can use the **Authentication** blade to update it to **Azure AD only multi-tenant** and then back to **Azure AD only single-tenant**.</span></span></p> |
        | <span data-ttu-id="591c0-139">任何组织目录中的帐户和个人 Microsoft 帐户</span><span class="sxs-lookup"><span data-stu-id="591c0-139">Accounts in any organizational directory and personal Microsoft accounts</span></span> | <span data-ttu-id="591c0-140">选择此选项可定位最广泛一组的客户。</span><span class="sxs-lookup"><span data-stu-id="591c0-140">Select this option to target the widest set of customers.</span></span><p><span data-ttu-id="591c0-141">此选项将映射到 **Azure AD 多租户和个人 Microsoft 帐户**。</span><span class="sxs-lookup"><span data-stu-id="591c0-141">This option is mapped to **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p><p><span data-ttu-id="591c0-142">如果您将应用注册为 **Azure AD 多租户和个人 Microsoft 帐户**，将无法在用户界面 (UI) 中更改此设置。</span><span class="sxs-lookup"><span data-stu-id="591c0-142">If you registered the app as **Azure AD multi-tenant and personal Microsoft accounts**, you can't change this setting in the user interface (UI).</span></span> <span data-ttu-id="591c0-143">而是必须使用应用程序清单编辑器来更改支持的帐户类型。</span><span class="sxs-lookup"><span data-stu-id="591c0-143">Instead, you must use the application manifest editor to change the supported account types.</span></span></p> |

    - <span data-ttu-id="591c0-144">**重定向 URI（可选）**– 选择要构建的应用的类型：**Web** 或 **公共客户端(移动和桌面)**。</span><span class="sxs-lookup"><span data-stu-id="591c0-144">**Redirect URI (optional)** – Select the type of app that you're building: **Web** or **Public client (mobile & desktop)**.</span></span> <span data-ttu-id="591c0-145">然后输入应用的重定向 URI（或回复 URL）。</span><span class="sxs-lookup"><span data-stu-id="591c0-145">Then enter the redirect URI (or reply URL) for the app.</span></span>

        - <span data-ttu-id="591c0-146">对于 Web 应用，提供应用的基本 URL。</span><span class="sxs-lookup"><span data-stu-id="591c0-146">For web apps, provide the base URL of the app.</span></span> <span data-ttu-id="591c0-147">例如，`http://localhost:31544` 可能是在本地计算机上运行的 Web 应用的 URL。</span><span class="sxs-lookup"><span data-stu-id="591c0-147">For example, `http://localhost:31544` might be the URL for a web app that runs on your local machine.</span></span> <span data-ttu-id="591c0-148">然后，用户使用此 URL 登录到 Web 客户端应用。</span><span class="sxs-lookup"><span data-stu-id="591c0-148">Users then use this URL to sign in to a web client app.</span></span>
        - <span data-ttu-id="591c0-149">对于公共客户端应用，提供 Azure AD 用于返回令牌响应的 URI。</span><span class="sxs-lookup"><span data-stu-id="591c0-149">For public client apps, provide the URI that Azure AD uses to return token responses.</span></span> <span data-ttu-id="591c0-150">输入特定于您的应用的值，例如 `myapp://auth`。</span><span class="sxs-lookup"><span data-stu-id="591c0-150">Enter a value that is specific to your app, such as `myapp://auth`.</span></span>

        <span data-ttu-id="591c0-151">要查看 Web 应用或本地应用的特定示例，请参阅 [Microsoft 身份平台（以前的面向开发人员的 Azure Active Directory）](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts)中的快速入门。</span><span class="sxs-lookup"><span data-stu-id="591c0-151">To see specific examples for web apps or native apps, see the quickstarts in [Microsoft identity platform (formerly Azure Active Directory for developers)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span></span>

5. <span data-ttu-id="591c0-152">在 **API 权限** 下，选择 **添加权限**。</span><span class="sxs-lookup"><span data-stu-id="591c0-152">Under **API permissions**, select **Add a permission**.</span></span> <span data-ttu-id="591c0-153">然后，在 **我的组织使用的 API** 选项卡上，搜索 **Dynamics 365 Human Resources**，并将 **user\_impersonation** 权限添加到您的应用。</span><span class="sxs-lookup"><span data-stu-id="591c0-153">Then, on the **APIs my organization uses** tab, search for **Dynamics 365 Human Resources**, and add the **user\_impersonation** permission to your app.</span></span> <span data-ttu-id="591c0-154">Human Resources 的应用程序 ID 是 f9be0c49-aa22-4ec6-911a-c5da515226ff。</span><span class="sxs-lookup"><span data-stu-id="591c0-154">The Application ID for Human Resources is f9be0c49-aa22-4ec6-911a-c5da515226ff.</span></span> <span data-ttu-id="591c0-155">使用此 ID 来确保您选择了正确的应用程序。</span><span class="sxs-lookup"><span data-stu-id="591c0-155">Use this ID to ensure you have chosen the correct application.</span></span>

6. <span data-ttu-id="591c0-156">选择 **注册**。</span><span class="sxs-lookup"><span data-stu-id="591c0-156">Select **Register**.</span></span>

   <span data-ttu-id="591c0-157">[![在 Azure 门户中注册新应用](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="591c0-157">[![Registering a new app in the Azure portal](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span></span>

<span data-ttu-id="591c0-158">Azure AD 为您的应用分配唯一的应用程序 ID（客户端 ID），并将您转到您的应用的 **概览** 页面。</span><span class="sxs-lookup"><span data-stu-id="591c0-158">Azure AD assigns a unique application ID (client ID) to your app, and takes you to the **Overview** page for your app.</span></span> <span data-ttu-id="591c0-159">要为您的应用添加更多功能，您可以选择其他配置选项，例如品牌选项以及证书和密钥选项。</span><span class="sxs-lookup"><span data-stu-id="591c0-159">To add more capabilities to your app, you can select other configuration options, such as options for branding and for certificates and secrets.</span></span>

## <a name="retrieving-an-access-token"></a><span data-ttu-id="591c0-160">检索访问令牌</span><span class="sxs-lookup"><span data-stu-id="591c0-160">Retrieving an access token</span></span>

<span data-ttu-id="591c0-161">您如何检索用于调用 Human Resources 数据 API 的访问令牌的具体细节，将取决于您用于开发客户端应用程序的技术。</span><span class="sxs-lookup"><span data-stu-id="591c0-161">The specifics of how you retrieve an access token for calling the Human Resources data API will depend on what technologies you're using to develop your client application.</span></span> <span data-ttu-id="591c0-162">例如，您可能[使用第三方实用程序进行测试](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md)（例如 Postman）、开发 C# 控制台应用程序或 Web 服务，或构建 javascript/TypeScript 客户端。</span><span class="sxs-lookup"><span data-stu-id="591c0-162">For example, you might be [testing with a third party utility](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (such as Postman), developing a C# console application or web service, or building a javascript/TypeScript client.</span></span>

<span data-ttu-id="591c0-163">示例 C# 客户端应用程序：</span><span class="sxs-lookup"><span data-stu-id="591c0-163">Example C# client application:</span></span>
```C#
using System;
using System.Net.Http;
using System.Threading.Tasks;

// requires appropriate NuGet package references in the project
using Microsoft.IdentityModel.Clients.ActiveDirectory;

namespace TalentODataPoC
{
    class Program
    {
        // prereq: This client app must be registered in Azure Active Directory. The app must be
        // registered as requiring permission to the Dynamics 365 for Talent API (with the Dynamics
        // HCM Workload delegated permission).
        static string clientId = "4fc703ef-672c-4e2c-813f-2f9d29d726db"; // This value should be obtained from AAD and must match your registered app
        static string talentNamespaceUri = "";

        public static async Task CallTalentODataService()
        {
            // authority URI
            UriBuilder uri = new UriBuilder("https://login.microsoftonline.com/common");
            AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

            // request token for the resource we want to access (Human Resources). This will authenticate
            // the user and return an access token containing claims for the authenticated user.
            var authResult = await authenticationContext.AcquireTokenAsync(
                "http://hr.talent.dynamics.com", /*Talent app id or resource URI*/
                clientId, /*registered client app id*/
                new Uri("https://localhost"), /*redirect URI, as registered in your AAD app*/
                new PlatformParameters(PromptBehavior.SelectAccount));

            // create the authorization header, which needs to be passed in the Header of the HTTP Requests to Talent
            string authHeader = authResult.CreateAuthorizationHeader();

            // HINT: paste the JWT into https://jwt.ms to decode and view it
            Console.Write("authHeader: ");
            Console.WriteLine(authHeader);
            Console.WriteLine();

            HttpClient client = new HttpClient();
            client.DefaultRequestHeaders.Add("Authorization", authHeader);

            string s;

            Console.Write("Talent Namespace URI: ");
            Console.WriteLine(talentNamespaceUri);
            Console.WriteLine();

            // call the OData service to get JobType data from Talent
            var resultOdata = await client.GetAsync(talentNamespaceUri + "data/JobTypes");
            s = await resultOdata.Content.ReadAsStringAsync();
            Console.WriteLine(s);
            Console.WriteLine();
        }

        static void Main(string[] args)
        {
            Console.WriteLine();

            // if the user passes in a single parameter, assume it is the namespaceUri for Talent
            if (args.Length == 1)
            {
                talentNamespaceUri = args[0];
            } else if (args.Length == 0)
            {
                Console.WriteLine("Enter Talent URL including namespace.");
                Console.WriteLine("Example: https://aos-rts-sf-21454f9d830-prod-westus2.hr.talent.dynamics.com/namespaces/2328af1a-2d45-4c6a-99e3-12a4c3867dcf/");
                Console.Write("> ");
                talentNamespaceUri = Console.ReadLine();
                if (!talentNamespaceUri.EndsWith("/"))
                {
                    talentNamespaceUri = talentNamespaceUri + "/";
                }
            } else
            {
                Console.WriteLine("Unexpected Arguments");
                System.Environment.Exit(1);
            }

            Task t = Program.CallTalentODataService();
            t.Wait();
        }
    }
}
```

<span data-ttu-id="591c0-164">检索访问令牌后，您将在发送到数据 API 的每个请求中将令牌作为不记名令牌传递到授权标头中，如上所述。</span><span class="sxs-lookup"><span data-stu-id="591c0-164">Once you've retrieved an access token, you'll pass the token in the Authorization header as a bearer token with each request you send to the data API, as described above.</span></span>
