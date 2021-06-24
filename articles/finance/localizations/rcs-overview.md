---
title: Regulatory Configuration Service
description: 本主题提供 Regulatory Configuration Service (RCS) 功能的概述并说明如何访问服务。
author: JaneA07
ms.date: 06/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 7f946988f124c814452e1774c700d5c7354f39b0
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216554"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="a6504-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="a6504-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6504-104">Regulatory Configuration Service (RCS) 是用于无代码/低代码全球化功能的独立设计器和生命周期管理服务。</span><span class="sxs-lookup"><span data-stu-id="a6504-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="a6504-105">通过 RCS，全球化利益相关者可以扩展和自定义税务、电子开票、监管报告、银行和业务文档的关键全球化区域，而无需开发人员的参与。</span><span class="sxs-lookup"><span data-stu-id="a6504-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="a6504-106">此无代码/低代码全球化方法支持更简单、更快且更具成本效益地创建或扩展全球化。</span><span class="sxs-lookup"><span data-stu-id="a6504-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="a6504-107">RCS 提供以下功能：</span><span class="sxs-lookup"><span data-stu-id="a6504-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="a6504-108">支持电子报告 (ER) 提供的所有功能。</span><span class="sxs-lookup"><span data-stu-id="a6504-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="a6504-109">配置新全球化微服务的先决条件。</span><span class="sxs-lookup"><span data-stu-id="a6504-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="a6504-110">支持电子开票。</span><span class="sxs-lookup"><span data-stu-id="a6504-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="a6504-111">有关详细信息，请参阅[电子开票](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga)。</span><span class="sxs-lookup"><span data-stu-id="a6504-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="a6504-112">支持税务计算。</span><span class="sxs-lookup"><span data-stu-id="a6504-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="a6504-113">有关详细信息，请参阅[税务服务](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview)。</span><span class="sxs-lookup"><span data-stu-id="a6504-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="a6504-114">支持新全球化功能，用于简化多组件功能的生命周期管理，并提供额外的功能来配置操作和设置功能参数。</span><span class="sxs-lookup"><span data-stu-id="a6504-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="a6504-115">有关详细信息，请参阅 [Regulatory Configuration Service – 全球化服务的简化全球化功能管理](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)。</span><span class="sxs-lookup"><span data-stu-id="a6504-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="a6504-116">支持在全局存储库中集中发布、存储和共享自定义配置以简化配置管理，而无需使用 Microsoft Dynamics Lifecycle Services (LCS)。</span><span class="sxs-lookup"><span data-stu-id="a6504-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="a6504-117">访问 RCS</span><span class="sxs-lookup"><span data-stu-id="a6504-117">Access RCS</span></span>

<span data-ttu-id="a6504-118">您可以从 [Regulatory Configuration Service 页面](https://marketing.configure.global.dynamics.com/)注册或登录到 RCS。</span><span class="sxs-lookup"><span data-stu-id="a6504-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![RCS 注册/登录](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="a6504-120">在 **Regulatory Configuration Service** 页面上，查看并接受使用服务的补充条款和条件，然后选择以下按钮之一：</span><span class="sxs-lookup"><span data-stu-id="a6504-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="a6504-121">**注册**，如果您是首次使用服务的用户，并且您要使用公司电子邮件地址为您的组织预配服务环境</span><span class="sxs-lookup"><span data-stu-id="a6504-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="a6504-122">**登录**，如果您之前已经注册了服务，并且想要访问您的组织环境</span><span class="sxs-lookup"><span data-stu-id="a6504-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="a6504-123">区域可用性</span><span class="sxs-lookup"><span data-stu-id="a6504-123">Regional availability</span></span>

<span data-ttu-id="a6504-124">RCS 在以下地区正式发布：</span><span class="sxs-lookup"><span data-stu-id="a6504-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="a6504-125">美国</span><span class="sxs-lookup"><span data-stu-id="a6504-125">United States</span></span>
- <span data-ttu-id="a6504-126">印度</span><span class="sxs-lookup"><span data-stu-id="a6504-126">India</span></span>
- <span data-ttu-id="a6504-127">法国</span><span class="sxs-lookup"><span data-stu-id="a6504-127">France</span></span>
- <span data-ttu-id="a6504-128">欧洲</span><span class="sxs-lookup"><span data-stu-id="a6504-128">Europe</span></span>

<span data-ttu-id="a6504-129">有关地区的完整列表，请参阅 [Dynamics 365 和 Power Platform：可用性、数据位置、语言和本地化](https://aka.ms/dynamics_365_international_availability_deck)。</span><span class="sxs-lookup"><span data-stu-id="a6504-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="rcs-default-company"></a><span data-ttu-id="a6504-130">RCS 默认公司</span><span class="sxs-lookup"><span data-stu-id="a6504-130">RCS default company</span></span>

<span data-ttu-id="a6504-131">跨所有公司共享在 RCS 中使用的设计时功能。</span><span class="sxs-lookup"><span data-stu-id="a6504-131">Design time functionality that is used in RCS is shared across all companies.</span></span> <span data-ttu-id="a6504-132">没有特定于公司的功能。</span><span class="sxs-lookup"><span data-stu-id="a6504-132">There is no company-specific functionality.</span></span> <span data-ttu-id="a6504-133">因此，我们建议您将一家公司 **DAT** 与您的 RCS 环境结合使用。</span><span class="sxs-lookup"><span data-stu-id="a6504-133">Therefore, we recommend that you use one company, **DAT**, with your RCS environment.</span></span>

<span data-ttu-id="a6504-134">但是，在某些情况下，您可能希望使 ER 格式使用与特定法人相关的参数。</span><span class="sxs-lookup"><span data-stu-id="a6504-134">However, in some scenarios, you might want to make ER formats use parameters that are related to a specific legal entity.</span></span> <span data-ttu-id="a6504-135">仅在这些情况下，您应该使用默认的公司切换器。</span><span class="sxs-lookup"><span data-stu-id="a6504-135">In these scenarios only, you should use the default company switcher.</span></span> <span data-ttu-id="a6504-136">有关示例，请参阅[配置 ER 格式以使用针对每个法人指定的参数](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md)。</span><span class="sxs-lookup"><span data-stu-id="a6504-136">For an example, see [Configure ER format to use parameters that are specified per legal entity](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="a6504-137">相关的 RCS 文档</span><span class="sxs-lookup"><span data-stu-id="a6504-137">Related RCS documentation</span></span>

<span data-ttu-id="a6504-138">有关相关组件的详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="a6504-138">For more information about related components, see the following topics:</span></span>

- <span data-ttu-id="a6504-139">**RCS：**</span><span class="sxs-lookup"><span data-stu-id="a6504-139">**RCS:**</span></span>

    - [<span data-ttu-id="a6504-140">在 RCS 中创建电子报告配置并将其上传到全局存储库</span><span class="sxs-lookup"><span data-stu-id="a6504-140">Create ER configurations in RCS and upload them to the Global repository</span></span>](rcs-global-repo-upload.md)

- <span data-ttu-id="a6504-141">**全局存储库：**</span><span class="sxs-lookup"><span data-stu-id="a6504-141">**Global repository:**</span></span>

    - [<span data-ttu-id="a6504-142">创建 ER 配置并上传到全局存储库</span><span class="sxs-lookup"><span data-stu-id="a6504-142">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="a6504-143">全局存储库中的共享配置</span><span class="sxs-lookup"><span data-stu-id="a6504-143">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="a6504-144">全局存储库中的增强筛选</span><span class="sxs-lookup"><span data-stu-id="a6504-144">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="a6504-145">从全局存储库中下载 ER 配置</span><span class="sxs-lookup"><span data-stu-id="a6504-145">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="a6504-146">终止全局存储库中的配置</span><span class="sxs-lookup"><span data-stu-id="a6504-146">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)
    - [<span data-ttu-id="a6504-147">Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) 存储弃用</span><span class="sxs-lookup"><span data-stu-id="a6504-147">Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation</span></span>](rcs-lcs-repo-dep-faq.md)

- <span data-ttu-id="a6504-148">**全球化功能：**</span><span class="sxs-lookup"><span data-stu-id="a6504-148">**Globalization feature:**</span></span>

    - [<span data-ttu-id="a6504-149">Regulatory Configuration Service (RCS) - 全球化功能</span><span class="sxs-lookup"><span data-stu-id="a6504-149">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a><span data-ttu-id="a6504-150">RCS 注册故障排除</span><span class="sxs-lookup"><span data-stu-id="a6504-150">Troubleshooting RCS sign-up</span></span>

<span data-ttu-id="a6504-151">当您从服务页面注册 RCS 时，可能会遇到与 Azure Active Directory (Azure AD) 相关的问题。</span><span class="sxs-lookup"><span data-stu-id="a6504-151">When you sign up for RCS from the service page, you might encounter an issue that is related to Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="a6504-152">您收到的错误消息表明 RCS 的注册当前已关闭，必须先打开，然后才能完成注册流程。</span><span class="sxs-lookup"><span data-stu-id="a6504-152">The error message that you receive indicates that sign-up for RCS is currently turned off and must be turned on before you can complete the sign-up process.</span></span>

![RCS 注册错误消息](media/01_RCSSignUpError.jpg)

<span data-ttu-id="a6504-154">出现此问题是因为您阻止注册临时订阅，并且必须在您的租户中启用 `AllowAdHocSubscriptions` 属性。</span><span class="sxs-lookup"><span data-stu-id="a6504-154">The issue occurs because you're blocked from signing up for ad-hoc subscriptions, and the `AllowAdHocSubscriptions` property must be enabled in your tenant.</span></span> 

- <span data-ttu-id="a6504-155">如果您的 IT 部门管理组织的 Azure 租户，请联系该部门以报告问题。</span><span class="sxs-lookup"><span data-stu-id="a6504-155">If your IT department manages your organization's Azure tenants, contact that department to report the issue.</span></span>
- <span data-ttu-id="a6504-156">如果您负责管理 Azure 租户，可以通过执行 [Azure Active Directory 的自助服务注册是什么](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings)中的步骤修复问题。</span><span class="sxs-lookup"><span data-stu-id="a6504-156">If you're responsible for managing your Azure tenants, you can fix the issues by following the steps in [What is self-service sign-up for Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).</span></span>
