---
title: 初始部署期间无法为 Commerce 站点构建器配置安全组
description: 本主题提供了故障排除指南，初始部署新电子商务租户期间，在 Microsoft Dynamics Lifecycle Services (LCS) 中创建电子商务组件时，如果 Commerce 站点构建器的 Microsoft Azure Active Directory (Azure AD) 安全组未显示为选项，此指南可提供帮助。
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 36ea43e19f395e3914d3eda1a9b8f5487b0926c5
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585216"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a><span data-ttu-id="ec8cf-103">初始部署期间无法为 Commerce 站点构建器配置安全组</span><span class="sxs-lookup"><span data-stu-id="ec8cf-103">Can't configure a security group for Commerce site builder during initial deployment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ec8cf-104">本主题提供了故障排除指南，初始部署新电子商务租户期间，在 Microsoft Dynamics Lifecycle Services (LCS) 中创建电子商务组件时，如果 Commerce 站点构建器的 Microsoft Azure Active Directory (Azure AD) 安全组未显示为选项，此指南可提供帮助。</span><span class="sxs-lookup"><span data-stu-id="ec8cf-104">This topic provides troubleshooting guidance that can help when the Microsoft Azure Active Directory (Azure AD) security group for Commerce site builder doesn't appear as an option when you create e-commerce components in Microsoft Dynamics Lifecycle Services (LCS) during initial deployment of a new e-commerce tenant.</span></span>

## <a name="description"></a><span data-ttu-id="ec8cf-105">说明</span><span class="sxs-lookup"><span data-stu-id="ec8cf-105">Description</span></span>

<span data-ttu-id="ec8cf-106">在部署包括 Commerce 站点构建器组件的新电子商务租户的过程中创建电子商务组件时，Azure AD 安全组不会在对话框中显示为选项。</span><span class="sxs-lookup"><span data-stu-id="ec8cf-106">When you create the e-commerce components as part of the process of deploying a new e-commerce tenant that includes the Commerce site builder component, the Azure AD security group doesn't appear as an option in the dialog box.</span></span>

## <a name="resolution"></a><span data-ttu-id="ec8cf-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="ec8cf-107">Resolution</span></span>

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a><span data-ttu-id="ec8cf-108">在正确的租户中为用户预配电子商务站点</span><span class="sxs-lookup"><span data-stu-id="ec8cf-108">Provision the e-commerce site with a user in the correct tenant</span></span>

1. <span data-ttu-id="ec8cf-109">转到 [Azure 门户](https://portal.azure.com/)。</span><span class="sxs-lookup"><span data-stu-id="ec8cf-109">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="ec8cf-110">在预配电子商务站点 LCS 项目所针对的租户下，请按照[使用 Azure Active Directory 创建一个基本组并添加成员](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="ec8cf-110">Under the tenant that the LCS project for your e-commerce site was provisioned for, follow the instructions in [Create a basic group and add members using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span></span>
1. <span data-ttu-id="ec8cf-111">转到 [LCS](https://lcs.dynamics.com/)，然后使用帐户登录，此帐户与您刚创建的 Azure AD 安全组共享相同租户。</span><span class="sxs-lookup"><span data-stu-id="ec8cf-111">Go to [LCS](https://lcs.dynamics.com/), and sign in by using an account that shares the same tenant as the Azure AD security group that you just created.</span></span> <span data-ttu-id="ec8cf-112">该帐户必须有权查看 Azure AD 安全组。</span><span class="sxs-lookup"><span data-stu-id="ec8cf-112">The account must have access to view the Azure AD security group.</span></span>
1. <span data-ttu-id="ec8cf-113">完成设置步骤以配置电子商务站点。</span><span class="sxs-lookup"><span data-stu-id="ec8cf-113">Complete the setup steps to configure the e-commerce site.</span></span> <span data-ttu-id="ec8cf-114">在预配电子商务组件时，安全组现在应作为一个选项出现在对话框中。</span><span class="sxs-lookup"><span data-stu-id="ec8cf-114">When you provision the e-commerce components, the security group should now appear as an option in the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="ec8cf-115">为确保对话框中的字段填充了安全组列表，您必须在输入您创建的 Azure AD 安全组的名称后选择 **输入**。</span><span class="sxs-lookup"><span data-stu-id="ec8cf-115">To ensure that the field in the dialog box is filled with the list of security groups, you must select **Enter** after you enter the name of the Azure AD security group that you created.</span></span> <span data-ttu-id="ec8cf-116">搜索结果将列出所有以搜索文本开头且用户有权访问的 Azure AD 安全组。</span><span class="sxs-lookup"><span data-stu-id="ec8cf-116">The search results will list all the Azure AD security groups that start with the search text, and that the user has access to.</span></span> <span data-ttu-id="ec8cf-117">您可以使用较短的搜索词来获得更广泛的搜索结果。</span><span class="sxs-lookup"><span data-stu-id="ec8cf-117">You can use a shorter search term to allow for broader search results.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ec8cf-118">其他资源</span><span class="sxs-lookup"><span data-stu-id="ec8cf-118">Additional resources</span></span>

[<span data-ttu-id="ec8cf-119">使用 Azure Active Directory 创建一个基本组并添加成员</span><span class="sxs-lookup"><span data-stu-id="ec8cf-119">Create a basic group and add members using Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[<span data-ttu-id="ec8cf-120">部署新的电子商务租户</span><span class="sxs-lookup"><span data-stu-id="ec8cf-120">Deploy a new e-commerce tenant</span></span>](../deploy-ecommerce-site.md)
