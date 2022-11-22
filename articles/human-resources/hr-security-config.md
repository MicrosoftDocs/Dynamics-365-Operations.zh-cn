---
title: 基于虚拟表的集成的安全配置概念
description: 本文介绍在 Microsoft Dynamics 365 Human Resources 和其他系统之间构建集成的体系结构。
author: twheeloc
ms.date: 11/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 219ceb0adae0cee5f74a39140ab74af9fdac1eb6
ms.sourcegitcommit: ea79bf014bbf495ac8e28db29502c8bd85a75f32
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2022
ms.locfileid: "9759647"
---
# <a name="security-configuration-concepts-for-virtual-table-based-integrations"></a>基于虚拟表的集成的安全配置概念

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本文介绍一种使用 [Microsoft Dataverse 虚拟表（实体）](/dev-itpro/power-platform/virtual-entities-overview)在 Dynamics 365 Human Resources 和第三方系统之间构建集成的体系结构。 本文的重点是安全配置，以及在系统边界之间构建功能性的安全系统所需的身份验证和授权相关任务。

## <a name="prerequisite-reference-articles"></a>先决条件参考文章

以下文章提供有关本文中的概念的更多信息：

- [虚拟实体概览](/dev-itpro/power-platform/virtual-entities-overview)
- [开始使用虚拟表（实体）](/developer/data-platform/virtual-entities/get-started-ve)
- [使用多租户服务器到服务器身份验证 (Microsoft Dataverse)](/developer/data-platform/use-multi-tenant-server-server-authentication)
- [通过 Microsoft Dataverse (Dataverse) 使用 OAuth 身份验证](/developer/data-platform/authenticate-oauth)
- [Microsoft 标识平台上的 OAuth 2.0 客户端凭据流](/azure/active-directory/develop/v2-oauth2-client-creds-grant-flow)
- [身份验证和授权](/dev-itpro/power-platform/authentication-and-authorization)

## <a name="architecture"></a>体系结构 

以下体系结构图显示了使用虚拟表（实体）的集成中涉及的主要概念。

![基于虚拟表的集成。](./media/Hosts.jpg)

以下是对上图中某些元素的解释：

- **Microsoft** – Microsoft 代表客户托管和运行不同的 Dynamics 365 产品。

    - **Azure Active Directory (Azure AD) 租户 C** – Microsoft 负责的 Azure AD 租户。 它是注册 Dynamics 365 应用程序的租户。

- **集成合作伙伴**

    - **集成系统** – 与 Dynamics 365 集成的系统。 可能是工资系统或依赖于存储在 Dynamics 365 中的数据的任何系统。
    - **适配器** – 负责与 Dynamics 365 和集成系统交互的软件或服务。

        > [!NOTE]
        > 如果一个适配器打算由多个 Dynamics 365 客户使用，预期它将在 Azure AD 中注册为多租户应用程序。

    - **Azure AD 租户 A** – 集成合作伙伴负责的 Azure AD 租户。 它是注册适配器的应用程序 ID 的租户。

- **共同客户** – 实施 Dynamics 365 Human Resources 和集成合作伙伴解决方案的客户。

    - **Dynamics 365 Finance 或 Human Resources** – Dynamics 365 Finance 或 Human Resources 的客户特定实例，其中包含集成系统所需的客户数据。
    - **Dataverse** – 与 Finance 或 Human Resources 连接的客户特定 Dataverse 环境。 Dataverse 提供用于与 Dynamics 365 数据交互的 Web API。
    - **Azure AD 租户 B** – 客户的 Azure AD 租户。 它充当标识提供程序（授权服务器），并发放令牌，授权调用方调用客户的 Dataverse 实例。

## <a name="basic-request-flow"></a>基本请求流

此节介绍集成中涉及的典型请求的基本流。 其中引用了本文前面的体系结构图。

一个典型的请求需要适配器在 Dynamics 365 中查询数据，然后将该数据保存并同步到集成系统。

1. 适配器调用 Dataverse Web API 来查询相关数据。

    > [!NOTE]
    > 身份验证是一个先决条件，获取令牌是此过程的主要部分。 身份验证在[系统边界的身份验证和授权](#authentication-and-authorization-at-system-boundaries)一节中加以介绍。

    此调用针对 Dataverse Web API 进行，查询通过虚拟表公开的应用程序数据。 （参见图中的“2. 初始同步”和“3. 增量同步”。）

2. Dataverse 通过使用虚拟实体插件（图中的“虚拟表代理”）查询虚拟表来处理请求。 Dataverse 请求被转发到 Finance 或 Human Resources 虚拟实体服务，查询实际存储在 Finance 或 Human Resources 数据库中的数据。
3. Finance 或 Human Resources 虚拟实体服务将针对虚拟实体的请求转换为针对支持 Dataverse 虚拟实体的 Finance 或 Human Resources 实体的查询。 数据从数据库中检索，转换回 Dataverse 实体表示形式，并返回给调用方。
4. 适配器完成所有所需的映射和数据转换，并对集成系统发起调用，将数据保存在集成系统数据库中。 （参见图中的“4. 保存数据”。）

## <a name="authentication-and-authorization-at-system-boundaries"></a>系统边界的身份验证和授权

*身份验证* 验证用户或应用程序的身份是否已被证明，并确认用户或应用程序是他们所说的身份。 *授权* 授予用户或应用程序访问特定应用程序级权限的权限。 有关详细信息，请参阅[身份验证与授权](/azure/active-directory/develop/authentication-vs-authorization)。

本文前面的体系结构图中的大多数跨系统调用都涉及适配器。 适配器必须对自身进行身份验证才能进行以下调用：

- 对 Dataverse 的调用
- 对集成系统的调用

查看图中的系统边界。 系统之间的每个 Web 请求都必须经过身份验证，并且必须在将数据返回给调用方之前通过应用程序级别的授权检查。 对于针对由 Finance 或 Human Resources 支持的 Dynamics 365 虚拟表的请求，将在以下系统边界强制执行身份验证和授权检查：

- 适配器与 Dataverse Web API (OData) 终结点之间的调用
- Dataverse 虚拟实体插件与 Finance 或 Human Resources 虚拟实体服务之间的调用

在这两种情况下，都会先进行身份验证检查。 然后进行应用程序级授权检查，以确保经过身份验证的用户或应用程序具有正确的应用程序级权限来检索请求的数据。

调用 Dataverse 的身份验证通过持有者令牌来处理，该令牌必须作为 HTTP 标头包含在对 Dataverse 的 Web 请求中。 适配器必须从租户 B Azure AD 实例获取令牌。 （参见图中的“1. 获取令牌”。）Azure AD 在身份验证流中充当标识提供程序。

适配器通过提供应用程序标识（非机密，在 Azure AD 租户 A 中注册）和只有适配器应用程序所有的应用程序机密或证书来进行身份验证。

在用户或应用程序已通过身份验证，可以对 Dataverse 发起调用后，将对每个请求进行 Dataverse 级授权检查。 这些检查确保调用方（适配器应用程序的标识，图中指定为“\<guid A\>”）具有适当的应用程序权限。 应用程序级授权在 Dataverse 中通过代表适配器的应用程序 ID 的应用程序用户进行管理。 应用程序级权限通过授予对特定 Dataverse 定义的应用程序角色的访问权限来进行管理。 这些角色为应用程序提供细化的权限。

如需更详细的指南，请参阅[使用多租户服务器到服务器身份验证](/power-apps/developer/data-platform/use-multi-tenant-server-server-authentication)。

如果通过了 Dataverse 级应用程序权限检查，虚拟实体插件将对 Finance 或 Human Resources 环境中的虚拟实体服务终结点发起调用。 服务器到服务器 (S2S) 身份验证用于进行此调用。 它使用在财务和运营虚拟数据源配置记录中配置的标识和机密。

![沙盒环境中的财务和运营虚拟数据源配置记录。](./media/sandbox.jpg)

有关详细信息，请参阅[配置 Dataverse 虚拟实体](/dev-itpro/power-platform/admin-reference)。

从 Dataverse 虚拟实体插件到 Finance 或 Human Resources 的调用包括适配器对 Dataverse 的原始调用的适配器标识（在体系结构图中指定为“\<guid A\>”的标识）。 如果虚拟实体数据源配置正确，并且通过了 S2S 身份验证检查，Finance 或 Human Resources 中的虚拟实体服务将在原始调用方（适配器，\<guid A\>）的上下文中运行查询。 将在 Finance 或 Human Resources 级别执行应用程序权限检查（授权），以确保适配器具有访问通过查询请求的数据实体所需的权限。

Finance 和 Human Resources 安全通过以下方式进行管理：

1. 通过将适配器标识 (\<guid A\>) 映射到特定的 Finance 和 Human Resources 用户。 此映射在 **Azure active directory 应用程序** 页面上完成。 有关详细信息，请参阅[注册外部应用程序](/dev-itpro/data-entities/services-home-page.md#register-your-external-application)。
2. 通过授予 Finance 或 Human Resources 用户适当的应用程序级角色、责任和权限。 有关详细信息，请参阅[基于角色的安全性](/dev-itpro/sysadmin/role-based-security)。

如果适配器应用程序 (\<guid A\>) 被授予访问所请求数据所需的权限，会发生以下事件：

1. 查询运行。
2. 数据被转换回其 Dataverse 实体页面。
3. 数据被返回到适配器。

> [!IMPORTANT]
> 开发期间，可以使用具有管理员角色的 Finance 或 Human Resources 用户来运行适配器。 但是，在生产环境中，适配器永远不应以管理员权限运行。

## <a name="key-takeaways"></a>关键要点

以下是虚拟表或实体体系结构的一些重要含义：

- 由 Human Resources 支持的虚拟表的安全配置在 Human Resources 中进行管理。
- 客户（本文前面的体系结构图中的“共同客户”）完全控制授予集成适配器标识的权限（图中指定为“\<guid A\>”）。
- 客户负责其 Human Resources 环境的正确安全配置。 创建适配器的集成合作伙伴必须提供有关适配器所需权限的指导。
