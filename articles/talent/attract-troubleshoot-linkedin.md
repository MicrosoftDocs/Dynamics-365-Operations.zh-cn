---
title: 与 LinkedIn 和 Microsoft Dynamics 365 Talent - Attract 集成疑难解答
description: 本主题说明如何解决在您尝试从 Microsoft Dynamics 365 Talent - Attract 将工作发布到 LinkedIn 时遇到的问题。
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 42065f3d6b7ae9e7ad99b26c7692e41f8c36934d
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832969"
---
# <a name="troubleshoot-integration-with-linkedin-and-microsoft-dynamics-365-talent---attract"></a><span data-ttu-id="a2d0d-103">与 LinkedIn 和 Microsoft Dynamics 365 Talent - Attract 集成疑难解答</span><span class="sxs-lookup"><span data-stu-id="a2d0d-103">Troubleshoot integration with LinkedIn and Microsoft Dynamics 365 Talent - Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a2d0d-104">请使用以下信息来帮助解决在您尝试从 Microsoft Dynamics 365 Talent: Attract 将工作发布到 LinkedIn 时可能遇到的问题。</span><span class="sxs-lookup"><span data-stu-id="a2d0d-104">Use the following information to help troubleshoot issues that you might have when you try to post jobs to LinkedIn from Microsoft Dynamics 365 Talent: Attract.</span></span>

## <a name="you-cant-sign-in-to-linkedin-from-attract"></a><span data-ttu-id="a2d0d-105">您无法从 Attract 登录 LinkedIn</span><span class="sxs-lookup"><span data-stu-id="a2d0d-105">You can't sign in to LinkedIn from Attract</span></span>

<span data-ttu-id="a2d0d-106">如果您在从 Attract 登录 LinkedIn 时遇到问题，请尝试以下步骤：</span><span class="sxs-lookup"><span data-stu-id="a2d0d-106">If you're having trouble signing in to LinkedIn from Attract, try these steps:</span></span>

1. <span data-ttu-id="a2d0d-107">验证您在 Attract 中输入的 LinkedIn 凭据是否有效且正确。</span><span class="sxs-lookup"><span data-stu-id="a2d0d-107">Verify that the LinkedIn credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="a2d0d-108">如果凭据有效且正确，请联系 [LinkedIn 支持](https://www.linkedin.com/help/linkedin)。</span><span class="sxs-lookup"><span data-stu-id="a2d0d-108">If the credentials are valid and correct, contact [LinkedIn support](https://www.linkedin.com/help/linkedin).</span></span>
3. <span data-ttu-id="a2d0d-109">如果问题仍然存在，请联系 [Microsoft 支持](./talent-support.md)。</span><span class="sxs-lookup"><span data-stu-id="a2d0d-109">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>

## <a name="job-posts-from-attract-dont-appear-on-linkedin"></a><span data-ttu-id="a2d0d-110">来自 Attract 的工作发布不出现在 LinkedIn 上</span><span class="sxs-lookup"><span data-stu-id="a2d0d-110">Job posts from Attract don't appear on LinkedIn</span></span>

<span data-ttu-id="a2d0d-111">如果您的工作在 24 小时后未在 LinkedIn 上显示，请尝试以下步骤：</span><span class="sxs-lookup"><span data-stu-id="a2d0d-111">If your job hasn't appeared on LinkedIn after 24 hours, try these steps:</span></span>

1. <span data-ttu-id="a2d0d-112">确保您的 LinkedIn 公司 ID 映射到您的 LinkedIn 公司页面，并在 Attract 管理中心正确输入。</span><span class="sxs-lookup"><span data-stu-id="a2d0d-112">Make sure that your LinkedIn Company ID maps to your LinkedIn company page and is correctly entered in the Attract Admin center.</span></span> <span data-ttu-id="a2d0d-113">有关如何在“管理中心”更改 LinkedIn 设置的详细信息，请参阅[为 Microsoft Dynamics 365 Talent - Attract 设置与 LinkedIn 的集成](attract-admin-linkedin.md)。</span><span class="sxs-lookup"><span data-stu-id="a2d0d-113">For more information about how to change LinkedIn settings in the Admin center, see [Set up integration with LinkedIn for Microsoft Dynamics 365 Talent - Attract](attract-admin-linkedin.md).</span></span> <span data-ttu-id="a2d0d-114">有关 LinkedIn 公司 ID 的详细信息，请参阅[将您的 LinkedIn 公司 ID 与 LinkedIn Job Board 关联 - 常见问题](https://www.linkedin.com/help/linkedin/answer/98972)。</span><span class="sxs-lookup"><span data-stu-id="a2d0d-114">For more information about LinkedIn Company IDs, see [Associating your LinkedIn Company ID with the LinkedIn Job Board - Frequently Asked Questions](https://www.linkedin.com/help/linkedin/answer/98972).</span></span>
2. <span data-ttu-id="a2d0d-115">检查 LinkedIn 上的工作详细信息，确保地址完整。</span><span class="sxs-lookup"><span data-stu-id="a2d0d-115">Check the job details on LinkedIn to make sure that the address is complete.</span></span> <span data-ttu-id="a2d0d-116">要成功发布工作，LinkedIn 至少需要工作的城市、国家或地区。</span><span class="sxs-lookup"><span data-stu-id="a2d0d-116">To post a job successfully, LinkedIn needs at least the city and country or region of the job.</span></span>
3. <span data-ttu-id="a2d0d-117">确保工作不会与 LinkedIn 上已经发布的其他工作重复。</span><span class="sxs-lookup"><span data-stu-id="a2d0d-117">Make sure that the job doesn't duplicate another job that has been posted on LinkedIn.</span></span> <span data-ttu-id="a2d0d-118">LinkedIn 不会发布与其他来源的 LinkedIn Premium Job Slots（高级职位空缺）或 Limited Listings（有限列表）重复的工作。</span><span class="sxs-lookup"><span data-stu-id="a2d0d-118">LinkedIn won't post jobs that are duplicates of either LinkedIn Premium Job Slots or Limited Listings from another source.</span></span> <span data-ttu-id="a2d0d-119">确认您公司的其他人员尚未手动发布该工作。</span><span class="sxs-lookup"><span data-stu-id="a2d0d-119">Verify that another person at your company didn't already post the job manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="a2d0d-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="a2d0d-120">See also</span></span>

[<span data-ttu-id="a2d0d-121">Attract 与 LinkedIn 集成的常见问题</span><span class="sxs-lookup"><span data-stu-id="a2d0d-121">Attract integration with LinkedIn FAQ</span></span>](./attract-linkedin-faq.md)

[<span data-ttu-id="a2d0d-122">将工作从 Microsoft Dynamics 365 Talent - Attract 发布到 LinkedIn</span><span class="sxs-lookup"><span data-stu-id="a2d0d-122">Post jobs to LinkedIn from Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-post-jobs-to-linkedin.md)

[<span data-ttu-id="a2d0d-123">在 Microsoft Dynamics 365 Talent - Attract 中使用 LinkedIn Recruiter 寻求应聘者</span><span class="sxs-lookup"><span data-stu-id="a2d0d-123">Source candidates with LinkedIn Recruiter in Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-linkedin-recruiter.md)

[<span data-ttu-id="a2d0d-124">在 Attract 中创建、审核和发布工作</span><span class="sxs-lookup"><span data-stu-id="a2d0d-124">Create, approve, and post jobs in Attract</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="a2d0d-125">与 LinkedIn 和 Microsoft Dynamics 365 Talent - Attract 集成疑难解答</span><span class="sxs-lookup"><span data-stu-id="a2d0d-125">Troubleshooting integration with LinkedIn and Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-troubleshoot-linkedin.md)
