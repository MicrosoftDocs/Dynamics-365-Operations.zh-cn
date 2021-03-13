---
title: 更新流程
description: Microsoft Dynamics 365 Human Resources 是一款真正的服务型软件 (SaaS)，可为应用程序和平台更改提供连续的非接触式服务更新。
author: andreabichsel
manager: tfehr
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bb5f7dc17c8f4f3a54bd285cb55088f2176db4a
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111607"
---
# <a name="update-process"></a><span data-ttu-id="ba8de-103">更新流程</span><span class="sxs-lookup"><span data-stu-id="ba8de-103">Update process</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ba8de-104">Microsoft Dynamics 365 Human Resources 是一款真正的服务型软件 (SaaS)，可提供连续的非接触式服务更新。</span><span class="sxs-lookup"><span data-stu-id="ba8de-104">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="ba8de-105">这些更新包含应用程序和平台更改，通常会对服务进行重大改进，包括监管更新。</span><span class="sxs-lookup"><span data-stu-id="ba8de-105">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="ba8de-106">更新策略</span><span class="sxs-lookup"><span data-stu-id="ba8de-106">Update policy</span></span>

<span data-ttu-id="ba8de-107">更新定期针对所有环境发布。</span><span class="sxs-lookup"><span data-stu-id="ba8de-107">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="ba8de-108">对 Human Resources 的支持根据 [Microsoft 生命周期策略](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy)提供，该策略为支持的可用性提供一致且可预测的指南。</span><span class="sxs-lookup"><span data-stu-id="ba8de-108">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="ba8de-109">发布频率</span><span class="sxs-lookup"><span data-stu-id="ba8de-109">Release cadence</span></span> 

<span data-ttu-id="ba8de-110">Human Resources 更新将自动应用于所有环境。</span><span class="sxs-lookup"><span data-stu-id="ba8de-110">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="ba8de-111">Human Resources 提供两种类型的发布：</span><span class="sxs-lookup"><span data-stu-id="ba8de-111">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="ba8de-112">**服务更新**：每两周更新一次，其中包括缺陷修复和新功能。</span><span class="sxs-lookup"><span data-stu-id="ba8de-112">**Service updates**: Updates occur every two weeks that include bug fixes and new features.</span></span> <span data-ttu-id="ba8de-113">服务更新在发布时还包括适用的平台更新。</span><span class="sxs-lookup"><span data-stu-id="ba8de-113">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="ba8de-114">要了解何时发布平台更新，请参阅[表 3：平台发布](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases)。</span><span class="sxs-lookup"><span data-stu-id="ba8de-114">To get an idea of when Platform updates are released, see [Table 3: Platform releases](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span></span> <span data-ttu-id="ba8de-115">每两周更新跨区域在全球分期推出。</span><span class="sxs-lookup"><span data-stu-id="ba8de-115">Biweekly updates have a staged global rollout across regions.</span></span> <span data-ttu-id="ba8de-116">有关每两周更新的详细信息，请参阅 [Dynamics 365 Human Resources 的新增功能或更改](hr-admin-whats-new.md)。</span><span class="sxs-lookup"><span data-stu-id="ba8de-116">For more information about biweekly updates, see [What's new or changed in Dynamics 365 Human Resources](hr-admin-whats-new.md).</span></span>

    <span data-ttu-id="ba8de-117">除非另有说明，否则所有受支持的数据中心都会每两周更新一次。</span><span class="sxs-lookup"><span data-stu-id="ba8de-117">All supported data centers update every two weeks, unless otherwise noted.</span></span> <span data-ttu-id="ba8de-118">每两周更新中包括美国、澳大利亚、欧洲、英国、亚洲和加拿大地区。</span><span class="sxs-lookup"><span data-stu-id="ba8de-118">US, Australia, Europe, UK, Asia, and Canada regions are included in biweekly updates.</span></span> 

- <span data-ttu-id="ba8de-119">**Dataverse 解决方案更新**：根据需要，这些更新大约每六周进行一次。</span><span class="sxs-lookup"><span data-stu-id="ba8de-119">**Dataverse solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="ba8de-120">这些更新包括 Dataverse 中的新实体和对现有实体的更改。</span><span class="sxs-lookup"><span data-stu-id="ba8de-120">They include new entities and changes to existing entities in Dataverse.</span></span> <span data-ttu-id="ba8de-121">这些更新与每两周更新发布在相同的区域，需要大约六周时间在所有数据中心完成复制。</span><span class="sxs-lookup"><span data-stu-id="ba8de-121">These updates release to the same regions as the biweekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="ba8de-122">解决方案更新可能与每两周服务更新一致，也可能不一致。</span><span class="sxs-lookup"><span data-stu-id="ba8de-122">Solution updates may or may not align with biweekly service updates.</span></span>

> [!NOTE]
> <span data-ttu-id="ba8de-123">解决方案更新发布后，将在所有数据中心可用。</span><span class="sxs-lookup"><span data-stu-id="ba8de-123">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="ba8de-124">如果不想等待更新自动复制，可以在任何数据中心的任何环境中手动应用这些更新。</span><span class="sxs-lookup"><span data-stu-id="ba8de-124">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="ba8de-125">如果需要，Human Resources 还会提供以下类型的修复：</span><span class="sxs-lookup"><span data-stu-id="ba8de-125">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="ba8de-126">**修订（修补程序）**：可能随每两周服务更新发布进行或独立进行的缺陷修复</span><span class="sxs-lookup"><span data-stu-id="ba8de-126">**Revision (hotfix)**: Bug fixes that can occur either with or apart from a biweekly service update release</span></span>

- <span data-ttu-id="ba8de-127">**紧急修复**：本质上是独立的主动和被动修补程序，可能包括仅配置或代码更改以解决实时的站点问题，可能在每两周服务更新发布之外进行</span><span class="sxs-lookup"><span data-stu-id="ba8de-127">**Emergency fix**: Proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a biweekly service update release</span></span>

<span data-ttu-id="ba8de-128">在内部环境中对发布进行审查、测试和验证。</span><span class="sxs-lookup"><span data-stu-id="ba8de-128">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="ba8de-129">版本签核后，将被部署到生产中。</span><span class="sxs-lookup"><span data-stu-id="ba8de-129">After builds are signed off, they're then deployed to production.</span></span>

## <a name="release-cadence-exceptions-in-2020"></a><span data-ttu-id="ba8de-130">2020 年的发布频率例外情况</span><span class="sxs-lookup"><span data-stu-id="ba8de-130">Release cadence exceptions in 2020</span></span>

<span data-ttu-id="ba8de-131">因为考虑到了假期，所以 2020 年 11 月和 12 月的发布计划如下所示：</span><span class="sxs-lookup"><span data-stu-id="ba8de-131">To account for holidays, the release schedule for November and December 2020 is as follows:</span></span>

- <span data-ttu-id="ba8de-132">11 月发布：11 月 2 日 - 11 月 13 日</span><span class="sxs-lookup"><span data-stu-id="ba8de-132">November release: November 2 - November 13</span></span>
- <span data-ttu-id="ba8de-133">12 月发布：11 月 30 日 - 12 月 11 日</span><span class="sxs-lookup"><span data-stu-id="ba8de-133">December release: November 30 - December 11</span></span>
 
<span data-ttu-id="ba8de-134">将在 2021 年 1 月 11 日恢复两周制发布节奏。</span><span class="sxs-lookup"><span data-stu-id="ba8de-134">The two-week release cadence will resume as usual on January 11, 2021.</span></span>

## <a name="communications"></a><span data-ttu-id="ba8de-135">通信</span><span class="sxs-lookup"><span data-stu-id="ba8de-135">Communications</span></span>

<span data-ttu-id="ba8de-136">您可以在以下位置了解 Human Resources 正在开发的功能以及已经发布的功能：</span><span class="sxs-lookup"><span data-stu-id="ba8de-136">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="ba8de-137">Dynamics 365 Human Resources 路线图</span><span class="sxs-lookup"><span data-stu-id="ba8de-137">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/human-resources/)

- [<span data-ttu-id="ba8de-138">Dynamics 365 版本计划</span><span class="sxs-lookup"><span data-stu-id="ba8de-138">Dynamics 365 Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans/)

- [<span data-ttu-id="ba8de-139">Dynamics 365 Human Resources 新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="ba8de-139">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="ba8de-140">[Lifecycle Services (LCS) 中的问题搜索](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs)（仅适用于平台相关漏洞）</span><span class="sxs-lookup"><span data-stu-id="ba8de-140">[Issue search in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="ba8de-141">Human Resources 博客</span><span class="sxs-lookup"><span data-stu-id="ba8de-141">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="ba8de-142">Human Resources Yammer 社区</span><span class="sxs-lookup"><span data-stu-id="ba8de-142">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="ba8de-143">沙盒环境中的预览功能</span><span class="sxs-lookup"><span data-stu-id="ba8de-143">Preview features in a sandbox environment</span></span>

<span data-ttu-id="ba8de-144">您可以先在沙盒环境中验证预览功能，然后再在生产环境中启用。</span><span class="sxs-lookup"><span data-stu-id="ba8de-144">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="ba8de-145">有关启用功能的详细信息，请参阅[功能管理概述](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)。</span><span class="sxs-lookup"><span data-stu-id="ba8de-145">For more information about enabling features, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

<span data-ttu-id="ba8de-146">所有新功能都会在预览阶段提供至少 30 天，通常为 30-60 天。</span><span class="sxs-lookup"><span data-stu-id="ba8de-146">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="ba8de-147">主要功能通常在预览期之后的每年 10 月和 4 月公开发布。</span><span class="sxs-lookup"><span data-stu-id="ba8de-147">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="ba8de-148">在功能管理工作区中看到新功能后，即可将其打开。</span><span class="sxs-lookup"><span data-stu-id="ba8de-148">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="ba8de-149">有些功能可能默认已启用。</span><span class="sxs-lookup"><span data-stu-id="ba8de-149">Some features may be on by default.</span></span>

<span data-ttu-id="ba8de-150">有时，完整功能默认启用，并且无法关闭（例如，功能管理工作区）。</span><span class="sxs-lookup"><span data-stu-id="ba8de-150">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="ba8de-151">某项功能公开发布后，即可以在生产环境中将其打开或关闭。</span><span class="sxs-lookup"><span data-stu-id="ba8de-151">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="ba8de-152">功能管理工作区指示何时将强制使用某项预览功能。</span><span class="sxs-lookup"><span data-stu-id="ba8de-152">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="ba8de-153">此日期通常是 10 月 1 日或 4 月 1 日，以与半年发布计划保持一致。</span><span class="sxs-lookup"><span data-stu-id="ba8de-153">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="ba8de-154">您无法关闭强制功能。</span><span class="sxs-lookup"><span data-stu-id="ba8de-154">You can't turn off mandatory features.</span></span> <span data-ttu-id="ba8de-155">在强制使用之前，您可以在所有环境中打开和关闭功能。</span><span class="sxs-lookup"><span data-stu-id="ba8de-155">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="ba8de-156">我们强烈建议在沙盒或试用环境中预览功能。</span><span class="sxs-lookup"><span data-stu-id="ba8de-156">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="ba8de-157">最好将当前生产环境或数据库的副本创建到沙盒环境中，以便您可以利用您的数据获得新功能的完整体验。</span><span class="sxs-lookup"><span data-stu-id="ba8de-157">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="ba8de-158">有关预配沙盒环境的详细信息，请参阅[预配 Human Resources 项目](hr-admin-setup-provision.md)。</span><span class="sxs-lookup"><span data-stu-id="ba8de-158">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="ba8de-159">要删除测试环境，请参阅[删除实例](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment)。</span><span class="sxs-lookup"><span data-stu-id="ba8de-159">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="ba8de-160">报告 bug</span><span class="sxs-lookup"><span data-stu-id="ba8de-160">Report bugs</span></span>

<span data-ttu-id="ba8de-161">在测试预览功能或尝试新功能时，您可能会发现无法正常使用的项目。</span><span class="sxs-lookup"><span data-stu-id="ba8de-161">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="ba8de-162">请通过 [Microsoft Dynamics 365 支持](https://dynamics.microsoft.com/support/)报告任何一个 bug。</span><span class="sxs-lookup"><span data-stu-id="ba8de-162">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="ba8de-163">请参阅</span><span class="sxs-lookup"><span data-stu-id="ba8de-163">See also</span></span>

[<span data-ttu-id="ba8de-164">Dynamics 365 和 Power Platform 版本计划</span><span class="sxs-lookup"><span data-stu-id="ba8de-164">Dynamics 365 and Power Platform Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans)</br>
[<span data-ttu-id="ba8de-165">Dynamics 365 Human Resource 的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="ba8de-165">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="ba8de-166">软件生命周期策略</span><span class="sxs-lookup"><span data-stu-id="ba8de-166">Software lifecycle policy</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

