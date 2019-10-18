---
title: 在 Microsoft Dynamics 365 Talent - Attract 中启用 Broadbean 集成
description: 本主题说明如何配置 Microsoft Dynamics 365 Talent - Attract 以将工作发布到外部招聘网站（如 Broadbean）。
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 808f91fb4b68ba9b5cee54d86423d23232df23a4
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008585"
---
# <a name="enable-broadbean-integration"></a><span data-ttu-id="65251-103">启用 Broadbean 集成</span><span class="sxs-lookup"><span data-stu-id="65251-103">Enable Broadbean integration</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="65251-104">您可能希望尽可能多的合格应聘者可以看到您的开放职位。</span><span class="sxs-lookup"><span data-stu-id="65251-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="65251-105">Broadbean 之类招聘站点可以帮助您达成这个目标。</span><span class="sxs-lookup"><span data-stu-id="65251-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="65251-106">Microsoft Dynamics 365 Talent: Attract 现在允许您将工作发布到 Broadbean，Microsoft 正在不断提供此领域的新服务/产品。</span><span class="sxs-lookup"><span data-stu-id="65251-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

> [!NOTE]
> - <span data-ttu-id="65251-107">若要将工作发布到外部站点，必须安装[综合招聘加载项](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring)。</span><span class="sxs-lookup"><span data-stu-id="65251-107">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="65251-108">要通过 Attract 向 Broadbean 发布工作，必须订阅 Broadbean。</span><span class="sxs-lookup"><span data-stu-id="65251-108">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="65251-109">此功能现在处于预览阶段。</span><span class="sxs-lookup"><span data-stu-id="65251-109">This feature is currently in preview.</span></span> <span data-ttu-id="65251-110">如果要尝试，必须[在 Attract 管理员设置中开启](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature)。</span><span class="sxs-lookup"><span data-stu-id="65251-110">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

## <a name="configure-broadbean-integration"></a><span data-ttu-id="65251-111">配置 Broadbean 集成</span><span class="sxs-lookup"><span data-stu-id="65251-111">Configure Broadbean integration</span></span>

1. <span data-ttu-id="65251-112">以管理员身份登录 Attract。</span><span class="sxs-lookup"><span data-stu-id="65251-112">Sign in to Attract as an admin.</span></span>

2. <span data-ttu-id="65251-113">选择页面右上角的**设置**按钮（齿轮符号），然后选择**管理员中心**。</span><span class="sxs-lookup"><span data-stu-id="65251-113">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>

3. <span data-ttu-id="65251-114">联系 Broadbean，并在**用户名**、**客户 ID** 和**加密令牌**字段中输入您的信息。</span><span class="sxs-lookup"><span data-stu-id="65251-114">Contact Broadbean, and enter your information in the **Username**, **Client ID**, and **Encryption Token** fields.</span></span>

4. <span data-ttu-id="65251-115">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="65251-115">Select **Save**.</span></span>

> [!WARNING]
> <span data-ttu-id="65251-116">您的 Broadbean 凭证是敏感的机密信息。</span><span class="sxs-lookup"><span data-stu-id="65251-116">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="65251-117">因此，请妥善保存和共享。</span><span class="sxs-lookup"><span data-stu-id="65251-117">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="65251-118">Attract 中的所有拥有管理员角色的人员都可以查看这些凭证。</span><span class="sxs-lookup"><span data-stu-id="65251-118">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="65251-119">Microsoft 和 Attract 不会参与这些值的创建和维护。</span><span class="sxs-lookup"><span data-stu-id="65251-119">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="65251-120">您负责使其在 Attract 中保持最新并与 Broadbean 合作解决涉及您的配置的所有问题。</span><span class="sxs-lookup"><span data-stu-id="65251-120">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>
