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
# <a name="authentication"></a>身份验证

本文提供有关如何通过 Microsoft Dynamics 365 Human Resources 数据应用程序编程接口 (API) 进行身份验证的概述信息。

## <a name="overview"></a>概览

Human Resources 的数据 API 是一个 OData 实现。 有关详细信息，请参阅[开放数据协议 (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md)。

在 API 为来自您的应用程序的请求提供服务之前，您的应用程序必须先作为授权调用方进行身份验证。

## <a name="fundamentals"></a>基本原理

要调用数据 API，您的应用程序必须从 Microsoft 身份平台获取访问令牌。 访问令牌包含有关您的应用程序的信息，以及它必须具有的调用 Human Resources 中的资源的权限。

### <a name="access-token"></a>访问令牌

Microsoft 身份平台发布的访问令牌是 base64 编码的 JavaScript Object Notation (JSON) Web 令牌 (JWT)。 它们包含数据 API（以及 Microsoft 身份平台保护的其他 Web API）用来验证调用方并确保调用方具有执行他们所请求的操作的正确权限的信息（声明）。 调用期间，您可以将访问令牌视为不透明。 您应该始终通过安全通道传输访问令牌，例如传输层安全性 (TLS) 和安全超文本传输协议 (HTTPS)。

这里是 Microsoft 身份平台发布的访问令牌的示例。

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

要调用数据 API，请将访问令牌作为不记名令牌附加到 HTTP 请求中的授权标头中。 下面是一个示例。

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a>使用 Azure 门户注册新应用程序

1. 使用工作或学校帐户或个人 Microsoft 帐户登录 [Microsoft Azure 门户](https://portal.azure.com)。

2. 如果您的帐户允许您访问多个租户，请在右上角选择您的帐户，然后将门户会话设置为您需要的 Azure Active Directory (Azure AD) 租户。

3. 在左窗格中，选择 **Azure Active Directory** 服务，然后选择 **应用注册 \> 新注册**。

4. 当 **注册应用程序** 页面出现时，输入您的应用程序的注册信息：

    - **名称**：输入一个有意义的应用程序名称，它将显示给应用用户。
    - **支持的帐户类型**：选择您的应用应该支持的帐户类型。

        | 支持的科目类型 | 说明 |
        |-------------------------|-------------|
        | 仅此组织目录中的帐户 | 如果要构建行业应用，请选择此选项。 除非您在目录中注册应用，否则此选项不可用。<p>此选项将映射到 **仅 Azure AD 单租户**。</p><p>除非您在目录外部注册应用，否则此选项是默认选项。 在这种情况下，默认选项是 **Azure AD 多租户和个人 Microsoft 帐户**。</p> |
        | 任何组织目录中的帐户 | 选择此选项以定位所有商业和教育客户。<p>此选项将映射到 **仅 Azure AD 多租户**。</p><p>如果您将应用注册为 **仅 Azure AD 单租户**，您可以使用 **身份验证** 边栏选项卡将应用更新为 **仅 Azure AD 多租户**，然后返回 **仅 Azure AD 单租户**。</p> |
        | 任何组织目录中的帐户和个人 Microsoft 帐户 | 选择此选项可定位最广泛一组的客户。<p>此选项将映射到 **Azure AD 多租户和个人 Microsoft 帐户**。</p><p>如果您将应用注册为 **Azure AD 多租户和个人 Microsoft 帐户**，将无法在用户界面 (UI) 中更改此设置。 而是必须使用应用程序清单编辑器来更改支持的帐户类型。</p> |

    - **重定向 URI（可选）**– 选择要构建的应用的类型：**Web** 或 **公共客户端(移动和桌面)**。 然后输入应用的重定向 URI（或回复 URL）。

        - 对于 Web 应用，提供应用的基本 URL。 例如，`http://localhost:31544` 可能是在本地计算机上运行的 Web 应用的 URL。 然后，用户使用此 URL 登录到 Web 客户端应用。
        - 对于公共客户端应用，提供 Azure AD 用于返回令牌响应的 URI。 输入特定于您的应用的值，例如 `myapp://auth`。

        要查看 Web 应用或本地应用的特定示例，请参阅 [Microsoft 身份平台（以前的面向开发人员的 Azure Active Directory）](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts)中的快速入门。

5. 在 **API 权限** 下，选择 **添加权限**。 然后，在 **我的组织使用的 API** 选项卡上，搜索 **Dynamics 365 Human Resources**，并将 **user\_impersonation** 权限添加到您的应用。 Human Resources 的应用程序 ID 是 f9be0c49-aa22-4ec6-911a-c5da515226ff。 使用此 ID 来确保您选择了正确的应用程序。

6. 选择 **注册**。

   [![在 Azure 门户中注册新应用](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)

Azure AD 为您的应用分配唯一的应用程序 ID（客户端 ID），并将您转到您的应用的 **概览** 页面。 要为您的应用添加更多功能，您可以选择其他配置选项，例如品牌选项以及证书和密钥选项。

## <a name="retrieving-an-access-token"></a>检索访问令牌

您如何检索用于调用 Human Resources 数据 API 的访问令牌的具体细节，将取决于您用于开发客户端应用程序的技术。 例如，您可能[使用第三方实用程序进行测试](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md)（例如 Postman）、开发 C# 控制台应用程序或 Web 服务，或构建 javascript/TypeScript 客户端。

示例 C# 客户端应用程序：
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

检索访问令牌后，您将在发送到数据 API 的每个请求中将令牌作为不记名令牌传递到授权标头中，如上所述。
