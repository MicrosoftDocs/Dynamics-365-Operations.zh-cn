---
title: 在测试或开发过程中限制访问店面
description: 本主题说明在进行内部测试或开发时如何限制访问 Microsoft Dynamics 365 Commerce 店面。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: cdc9b6af55bcba98f5ea7607bb1847f61a707778
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018330"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a><span data-ttu-id="b5757-103">在测试或开发过程中限制访问店面</span><span class="sxs-lookup"><span data-stu-id="b5757-103">Restrict access to a storefront during testing or development</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b5757-104">本主题说明在进行内部测试或开发时如何限制访问 Microsoft Dynamics 365 Commerce 店面。</span><span class="sxs-lookup"><span data-stu-id="b5757-104">This topic explains how to restrict access to a Microsoft Dynamics 365 Commerce storefront while internal testing or development is occurring.</span></span>

## <a name="description"></a><span data-ttu-id="b5757-105">说明</span><span class="sxs-lookup"><span data-stu-id="b5757-105">Description</span></span>

<span data-ttu-id="b5757-106">在内部测试或主动开发期间，您可能希望限制对站点的访问，以防止外部用户访问已发布的店面页面。</span><span class="sxs-lookup"><span data-stu-id="b5757-106">During internal testing or active development, you might want to restrict access to your site to prevent external users from accessing the published storefront pages.</span></span>

## <a name="resolution"></a><span data-ttu-id="b5757-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="b5757-107">Resolution</span></span>

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a><span data-ttu-id="b5757-108">使用标准用户流设置 Azure AD B2C</span><span class="sxs-lookup"><span data-stu-id="b5757-108">Set up Azure AD B2C by using standard user flows</span></span>

<span data-ttu-id="b5757-109">有关如何为电子商务站点配置 Azure Active Directory B2C (Azure AD B2C) 的信息，请参见[在 Commerce 中设置 B2C 租户](../set-up-b2c-tenant.md)。</span><span class="sxs-lookup"><span data-stu-id="b5757-109">For information about how to configure Azure Active Directory B2C (Azure AD B2C) for your e-commerce site, see [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md).</span></span>

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a><span data-ttu-id="b5757-110">限制用户访问店面页面并阻止创建新用户</span><span class="sxs-lookup"><span data-stu-id="b5757-110">Restrict user access to storefront pages and block the creation of new users</span></span>

<span data-ttu-id="b5757-111">要限制用户访问 Commerce 站点构建器中的店面页面，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="b5757-111">To restrict user access to storefront pages in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="b5757-112">转到您的站点。</span><span class="sxs-lookup"><span data-stu-id="b5757-112">Go to your site.</span></span>
1. <span data-ttu-id="b5757-113">选择 **页面**，然后选择限制用户访问的页面。</span><span class="sxs-lookup"><span data-stu-id="b5757-113">Select **Pages**, and then select the page to restrict user access for.</span></span>
1. <span data-ttu-id="b5757-114">选择模块或片段插槽，然后选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="b5757-114">Select the module or fragment slot, and then select **Edit**.</span></span>
1. <span data-ttu-id="b5757-115">在属性窗格中，选择 **需要登录？**，然后选择 **完成编辑**。</span><span class="sxs-lookup"><span data-stu-id="b5757-115">In the properties pane, select **Requires sign-in?**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="b5757-116">选择 **发布**。</span><span class="sxs-lookup"><span data-stu-id="b5757-116">Select **Publish**.</span></span>

<span data-ttu-id="b5757-117">若要阻止在 Azure AD 中创建新用户，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="b5757-117">To block the creation of new users in Azure AD, follow these steps.</span></span>

1. <span data-ttu-id="b5757-118">转到 [Azure 门户](https://portal.azure.com/)。</span><span class="sxs-lookup"><span data-stu-id="b5757-118">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="b5757-119">选择您为站点访问而创建的 Azure AD B2C 应用程序。</span><span class="sxs-lookup"><span data-stu-id="b5757-119">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="b5757-120">在左侧导航中，选择 **用户流**。</span><span class="sxs-lookup"><span data-stu-id="b5757-120">In the left navigation, select **User flows**.</span></span>
1. <span data-ttu-id="b5757-121">在 **用户流** 页面顶部，选择 **新建用户流**。</span><span class="sxs-lookup"><span data-stu-id="b5757-121">At the top of the **User Flows** page, select **New user flow**.</span></span>
1. <span data-ttu-id="b5757-122">在 **选择用户流类型** 页面上，选择 **预览**。</span><span class="sxs-lookup"><span data-stu-id="b5757-122">On the **Select a user flow type** page, select **Preview**.</span></span>
1. <span data-ttu-id="b5757-123">在页面中间，选择 **登录 v2**。</span><span class="sxs-lookup"><span data-stu-id="b5757-123">In the middle of the page, select **Sign in v2**.</span></span> <span data-ttu-id="b5757-124">然后，在测试或开发过程中，按照[在 Commerce 中设置 B2C 租户](../set-up-b2c-tenant.md)中的步骤，将流配置为站点的 Azure AD B2C 标准用户流。</span><span class="sxs-lookup"><span data-stu-id="b5757-124">Then follow the steps in [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md) to configure the flow as your site's standard user flow for Azure AD B2C during testing or development.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b5757-125">其他资源</span><span class="sxs-lookup"><span data-stu-id="b5757-125">Additional resources</span></span>

[<span data-ttu-id="b5757-126">在 Commerce 中设置 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="b5757-126">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)

[<span data-ttu-id="b5757-127">设置用户登录自定义页面</span><span class="sxs-lookup"><span data-stu-id="b5757-127">Set up custom pages for user sign-ins</span></span>](../custom-pages-user-logins.md)
