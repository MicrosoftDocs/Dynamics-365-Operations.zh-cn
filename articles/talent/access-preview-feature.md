---
title: 管理功能
description: 此主题介绍管理员可如何启用 Microsoft Dynamics 365 Talent 中的预览功能，并且列出了当前可预览的功能。
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
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.1.0, Talent
ms.openlocfilehash: d818e9e04ce88e5ab285ef8176334809447fb477
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124788"
---
# <a name="manage-features"></a><span data-ttu-id="2c95e-103">管理功能</span><span class="sxs-lookup"><span data-stu-id="2c95e-103">Manage features</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2c95e-104">在持续推出适用于 Microsoft Dynamics 365 Human Resources 的人力资本管理 (HCM) 功能时，我们希望让客户尽快体验新功能。</span><span class="sxs-lookup"><span data-stu-id="2c95e-104">As part of our continuous rollout of human capital management (HCM) capabilities for Microsoft Dynamics 365 Human Resources, we want to let customers experience new features as soon as possible.</span></span> <span data-ttu-id="2c95e-105">管理员可以在自己的环境中查看和使用预览功能。</span><span class="sxs-lookup"><span data-stu-id="2c95e-105">Administrators can see and use preview features in their environments.</span></span> <span data-ttu-id="2c95e-106">这些功能几乎已针对普通使用准备就绪，并经过了大量测试。</span><span class="sxs-lookup"><span data-stu-id="2c95e-106">These features are almost ready for general availability and have gone through extensive testing.</span></span> <span data-ttu-id="2c95e-107">我们正在征求最后一轮的客户反馈和验证，之后就会公开发布。</span><span class="sxs-lookup"><span data-stu-id="2c95e-107">We're just looking for a final round of customer feedback and validation before we release them for general availability.</span></span>

<span data-ttu-id="2c95e-108">此主题介绍如何启用预览功能，并且列出了当前可预览的功能。</span><span class="sxs-lookup"><span data-stu-id="2c95e-108">This topic describes how you can enable preview features, and it lists the features that are currently available for preview.</span></span> <span data-ttu-id="2c95e-109">发布功能以公开推出和发布新功能以预览时，将更新此列表。</span><span class="sxs-lookup"><span data-stu-id="2c95e-109">This list will be updated as features are released to general availability and as new features are released to preview.</span></span> <span data-ttu-id="2c95e-110">发布新功能以预览时，不提供通知。</span><span class="sxs-lookup"><span data-stu-id="2c95e-110">No notification is given when new features are released to preview.</span></span> <span data-ttu-id="2c95e-111">用户只需启动即可查看这些功能。</span><span class="sxs-lookup"><span data-stu-id="2c95e-111">Users will just start to see the features.</span></span> <span data-ttu-id="2c95e-112">有关 Talent 中的新功能的详细信息，请参阅 [Dynamics 365 Talent 新增功能或更改](./whats-new.md)和 [Dynamics 365 和 Power Platform 发行说明](https://docs.microsoft.com/business-applications-release-notes)。</span><span class="sxs-lookup"><span data-stu-id="2c95e-112">For more information about new features in Talent, see [What's new or changed in Dynamics 365 Talent](./whats-new.md) and [Dynamics 365 and Power Platform Release Notes](https://docs.microsoft.com/business-applications-release-notes).</span></span>

## <a name="enable-or-disable-preview-features"></a><span data-ttu-id="2c95e-113">启用或禁用预览功能</span><span class="sxs-lookup"><span data-stu-id="2c95e-113">Enable or disable preview features</span></span>

<span data-ttu-id="2c95e-114">若要访问预览功能，必须首先在您的环境中启用。</span><span class="sxs-lookup"><span data-stu-id="2c95e-114">To access preview features, you must first enable them in your environment.</span></span> <span data-ttu-id="2c95e-115">预览功能的启用或禁用特定于环境。</span><span class="sxs-lookup"><span data-stu-id="2c95e-115">Enabling or disabling preview features is environment-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2c95e-116">开启**预览功能**设置时，即对组织中该环境的所有用户启用了预览功能。</span><span class="sxs-lookup"><span data-stu-id="2c95e-116">When you turn on the **Preview Features** setting, you enable preview features for all users in your organization who are in that environment.</span></span> <span data-ttu-id="2c95e-117">关闭此设置时，即禁用了预览功能，并且您的用户不能访问这些功能。</span><span class="sxs-lookup"><span data-stu-id="2c95e-117">When you turn off the setting, you disable preview features and make them inaccessible to your users.</span></span> <span data-ttu-id="2c95e-118">在 Talent 中，对预览功能的支持受限。</span><span class="sxs-lookup"><span data-stu-id="2c95e-118">Preview features have limited support in Talent.</span></span> <span data-ttu-id="2c95e-119">预览功能可以使用的隐私和安全措施更少，并且 Talent 服务级别协议 (SLA) 中不涵盖预览功能。</span><span class="sxs-lookup"><span data-stu-id="2c95e-119">They might use fewer privacy and security measures, and they aren't included in the Talent service level agreement (SLA).</span></span> <span data-ttu-id="2c95e-120">不应使用预览功能处理个人数据（即可能用于确认您的身份的所有信息），也不应处理其他与法律或法规遵从性要求有关的数据。</span><span class="sxs-lookup"><span data-stu-id="2c95e-120">You should not use preview features to process personal data (that is, any information that could identify you), or to process other data that is subject to legal or regulatory compliance requirements.</span></span>

### <a name="attract"></a><span data-ttu-id="2c95e-121">Attract</span><span class="sxs-lookup"><span data-stu-id="2c95e-121">Attract</span></span>

1. <span data-ttu-id="2c95e-122">登录到 Microsoft Dynamics 365 Talent: Attract。</span><span class="sxs-lookup"><span data-stu-id="2c95e-122">Sign in to Microsoft Dynamics 365 Talent: Attract.</span></span>
2. <span data-ttu-id="2c95e-123">在右上角的**设置**菜单（齿轮符号）中，选择**管理中心**。</span><span class="sxs-lookup"><span data-stu-id="2c95e-123">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span>
3. <span data-ttu-id="2c95e-124">在**功能管理**选项卡上，选择**预览功能**旁边的选项，使其变为蓝色，然后说出**打开**。</span><span class="sxs-lookup"><span data-stu-id="2c95e-124">On the **Feature management** tab, select the option next to **Preview features** so that it turns blue and says **On**.</span></span>

    ![启用 Attract 中的预览功能](./media/attract-enable-preview-features.png)

4. <span data-ttu-id="2c95e-126">选择或取消单个预览功能的选择。</span><span class="sxs-lookup"><span data-stu-id="2c95e-126">Select or cancel the selection of individual preview features.</span></span> <span data-ttu-id="2c95e-127">如果不执行任何操作，则启用所有可用预览功能。</span><span class="sxs-lookup"><span data-stu-id="2c95e-127">If you do nothing, all available preview features are enabled.</span></span>
5. <span data-ttu-id="2c95e-128">刷新浏览器以开始查看新功能。</span><span class="sxs-lookup"><span data-stu-id="2c95e-128">Refresh your browser to start to see the new features.</span></span> <span data-ttu-id="2c95e-129">所有已登录用户都会在下次登录时看到这些功能，这些用户也可以刷新浏览器以立即查看这些功能。</span><span class="sxs-lookup"><span data-stu-id="2c95e-129">Any users who are already signed in will see the features the next time they sign in, or they can refresh their browser to see the features immediately.</span></span>

> [!NOTE]
> <span data-ttu-id="2c95e-130">可能需要为某些预览功能执行更多配置。</span><span class="sxs-lookup"><span data-stu-id="2c95e-130">Some preview features might require additional configuration.</span></span> <span data-ttu-id="2c95e-131">单击预览功能旁边的链接完成该功能的设置。</span><span class="sxs-lookup"><span data-stu-id="2c95e-131">Follow the links next to the preview feature to complete the setup for it.</span></span>

## <a name="feedback"></a><span data-ttu-id="2c95e-132">反馈</span><span class="sxs-lookup"><span data-stu-id="2c95e-132">Feedback</span></span>

<span data-ttu-id="2c95e-133">希望您提供有关以上任何预览功能的体验信息。</span><span class="sxs-lookup"><span data-stu-id="2c95e-133">We want to hear from you about your experience with any of these preview features.</span></span> <span data-ttu-id="2c95e-134">希望您在使用这些功能或其他功能时，定期在以下站点上发布反馈：</span><span class="sxs-lookup"><span data-stu-id="2c95e-134">We encourage you to regularly post your feedback on the following sites as you use these or any other features:</span></span>

- <span data-ttu-id="2c95e-135">[社区](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – 此站点是很好的资源，用户可在这里讨论使用案例，提问和获得社区帮助。</span><span class="sxs-lookup"><span data-stu-id="2c95e-135">[Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – This site is a great resource where users can discuss use cases, ask questions, and get community help.</span></span>
- <span data-ttu-id="2c95e-136">告知我们您希望在产品中看到的功能，或您认为我们应对现有功能进行的任何更改。</span><span class="sxs-lookup"><span data-stu-id="2c95e-136">Let us know about features that you want to see in the product, or let us know about any changes you think we should make to existing features.</span></span> <span data-ttu-id="2c95e-137">请在以下站点提供产品观点方面的建议：</span><span class="sxs-lookup"><span data-stu-id="2c95e-137">Suggest product ideas on the following sites:</span></span>

    - [<span data-ttu-id="2c95e-138">Attract 观点</span><span class="sxs-lookup"><span data-stu-id="2c95e-138">Attract ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [<span data-ttu-id="2c95e-139">Onboard 观点</span><span class="sxs-lookup"><span data-stu-id="2c95e-139">Onboard ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

<span data-ttu-id="2c95e-140">切勿在提交反馈或产品评论时包含个人数据（可用于确认您的身份的任何信息）。</span><span class="sxs-lookup"><span data-stu-id="2c95e-140">Make sure that you don't include personal data (any information that could identify you) in your feedback or product review submissions.</span></span> <span data-ttu-id="2c95e-141">可能会对收集的信息进行更深入的分析，但在适用的隐私法律下不会用于回应申请。</span><span class="sxs-lookup"><span data-stu-id="2c95e-141">Collected information might be analyzed further and isn't used to answer requests under applicable privacy laws.</span></span> <span data-ttu-id="2c95e-142">在这些计划下单独收集的个人数据应遵守 [Microsoft 隐私声明](https://privacy.microsoft.com/privacystatement)。</span><span class="sxs-lookup"><span data-stu-id="2c95e-142">Personal data that is collected separately under these programs is subject to the [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement).</span></span>

> [!TIP]
> <span data-ttu-id="2c95e-143">将本主题加入书签，并经常回访以在我们发布新预览功能后随时掌握相关数据。</span><span class="sxs-lookup"><span data-stu-id="2c95e-143">Bookmark this topic, and check back often to stay up to date about new preview features as we release them.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c95e-144">请参阅</span><span class="sxs-lookup"><span data-stu-id="2c95e-144">See also</span></span>

- [<span data-ttu-id="2c95e-145">试用或购买 Talent 应用</span><span class="sxs-lookup"><span data-stu-id="2c95e-145">Try or buy Talent apps</span></span>](https://dynamics.microsoft.com/talent/overview/)
- [<span data-ttu-id="2c95e-146">Dynamics 365 Talent 新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="2c95e-146">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="2c95e-147">发布计划</span><span class="sxs-lookup"><span data-stu-id="2c95e-147">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="2c95e-148">获取 Microsoft Dynamics 365 Talent 支持</span><span class="sxs-lookup"><span data-stu-id="2c95e-148">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
