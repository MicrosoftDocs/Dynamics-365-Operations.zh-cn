---
title: Regulatory Configuration Service
description: 本文提供 Regulatory Configuration Service (RCS) 功能的概述并说明如何访问服务。
author: kfend
ms.date: 06/04/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
ms.openlocfilehash: 01614aec0da097ee5c0c90bcbe9c7e0065f1d4fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277168"
---
# <a name="regulatory-configuration-service"></a>Regulatory Configuration Service

[!include [banner](../includes/banner.md)]

Regulatory Configuration Service (RCS) 是用于无代码/低代码全球化功能的独立设计器和生命周期管理服务。 通过 RCS，全球化利益相关者可以扩展和自定义税务、电子开票、监管报告、银行和业务文档的关键全球化区域，而无需开发人员的参与。 此无代码/低代码全球化方法支持更简单、更快且更具成本效益地创建或扩展全球化。

RCS 提供以下功能：

- 支持电子报告 (ER) 提供的所有功能。
- 配置新全球化微服务的先决条件。
- 支持电子开票。 有关详细信息，请参阅[电子开票](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga)。
- 支持税务计算。 有关详细信息，请参阅[税务服务](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview)。
- 支持新全球化功能，用于简化多组件功能的生命周期管理，并提供额外的功能来配置操作和设置功能参数。 有关详细信息，请参阅 [Regulatory Configuration Service – 全球化服务的简化全球化功能管理](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)。
- 支持在全局存储库中集中发布、存储和共享自定义配置以简化配置管理，而无需使用 Microsoft Dynamics Lifecycle Services (LCS)。

## <a name="access-rcs"></a>访问 RCS

您可以从 [Regulatory Configuration Service 页面](https://marketing.configure.global.dynamics.com/)注册或登录到 RCS。

![RCS 注册/登录。](media/202103_RCS%20Marketing%20page_updated_1.jpg)

在 **Regulatory Configuration Service** 页面上，查看并接受使用服务的补充条款和条件，然后选择以下按钮之一：

- **注册**，如果您是首次使用服务的用户，并且您要使用公司电子邮件地址为您的组织预配服务环境
- **登录**，如果您之前已经注册了服务，并且想要访问您的组织环境

> [!NOTE] 
> 注册后，我们建议您将其他 SysAdmin 用户添加到 RCS 环境。 此用户将设置为环境的联合管理员。 这将有助于为访问 RCS 环境提供稳定性，因为 SysAdmin 角色用于管理该环境的用户。 您可以使用 **RCS 工作区 > 系统管理** 添加用户。

## <a name="regional-availability"></a>区域可用性

RCS 在以下地区正式发布：

- 美国
- 印度
- 法国
- 欧洲

有关地区的完整列表，请参阅 [Dynamics 365 和 Power Platform：可用性、数据位置、语言和本地化](https://aka.ms/dynamics_365_international_availability_deck)。

## <a name="rcs-default-company"></a>RCS 默认公司

跨所有公司共享在 RCS 中使用的设计时功能。 没有特定于公司的功能。 因此，我们建议您将一家公司 **DAT** 与您的 RCS 环境结合使用。

但是，在某些情况下，您可能希望使 ER 格式使用与特定法人相关的参数。 仅在这些情况下，您应该使用默认的公司切换器。 有关示例，请参阅[配置 ER 格式以使用针对每个法人指定的参数](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md)。

## <a name="related-rcs-documentation"></a>相关的 RCS 文档

有关相关组件的详细信息，请参阅以下主题：

- **RCS：**

    - [在 RCS 中创建电子报告配置并将其上传到全局存储库](rcs-global-repo-upload.md)

- **全局存储库：**

    - [创建 ER 配置并上传到全局存储库](rcs-global-repo-upload.md)
    - [全局存储库中的共享配置](rcs-global-repo-share-configuration.md)
    - [全局存储库中的增强筛选](enhanced-filtering-global-repo.md)
    - [从全局存储库中下载 ER 配置](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [终止全局存储库中的配置](discontinuing-configurations-rcs-global-repo.md)
    - [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) 存储弃用](rcs-lcs-repo-dep-faq.md)

- **全球化功能：**

    - [Regulatory Configuration Service (RCS) - 全球化功能](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a>RCS 注册故障排除

当您从服务页面注册 RCS 时，可能会遇到与 Azure Active Directory (Azure AD) 相关的问题。 您收到的错误消息表明 RCS 的注册当前已关闭，必须先打开，然后才能完成注册流程。

![RCS 注册错误消息。](media/01_RCSSignUpError.jpg)

出现此问题是因为您阻止注册临时订阅，并且必须在您的租户中启用 `AllowAdHocSubscriptions` 属性。 

- 如果您的 IT 部门管理组织的 Azure 租户，请联系该部门以报告问题。
- 如果您负责管理 Azure 租户，可以通过执行 [Azure Active Directory 的自助服务注册是什么](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings)中的步骤修复问题。
