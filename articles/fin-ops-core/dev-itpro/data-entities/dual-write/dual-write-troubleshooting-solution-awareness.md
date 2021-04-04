---
title: 解决与解决方案意识相关的问题
description: 本主题提供故障排除信息，可以帮助您解决与解决方案意识有关的问题。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f9e02a6a5afe965a1707f0b04e1b4daedd4ec1df
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566781"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a><span data-ttu-id="64812-103">解决与解决方案意识相关的问题</span><span class="sxs-lookup"><span data-stu-id="64812-103">Troubleshoot issues related to solution awareness</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="64812-104">本主题提供 Finance and Operations 应用与 Dataverse 之间的双写入集成的故障排除信息。</span><span class="sxs-lookup"><span data-stu-id="64812-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="64812-105">具体来说，提供可以帮助您解决与解决方案意识有关的问题的信息。</span><span class="sxs-lookup"><span data-stu-id="64812-105">Specifically, it provides information that can help you fix issues that are related to solution awareness.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="64812-106">本主题解决的某些问题可能需要系统管理员角色或 Microsoft Azure Active Directory (Azure AD) 租户管理员凭据。</span><span class="sxs-lookup"><span data-stu-id="64812-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="64812-107">介绍每个问题的每一节说明了是否需要特定角色或凭据。</span><span class="sxs-lookup"><span data-stu-id="64812-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="error-on-the-dual-write-page"></a><span data-ttu-id="64812-108">双写入页面上的错误</span><span class="sxs-lookup"><span data-stu-id="64812-108">Error on the Dual-write page</span></span>

<span data-ttu-id="64812-109">在 **双写入** 页面上，您可能会收到类似于以下示例的错误消息：</span><span class="sxs-lookup"><span data-stu-id="64812-109">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="64812-110">*在 MetadataCache 中找不到名称为“msdyn\_dualwriteentitymap' with namemapping='Logical”的实体。*</span><span class="sxs-lookup"><span data-stu-id="64812-110">*The entity with a name 'msdyn\_dualwriteentitymap' with namemapping='Logical' was not found in the MetadataCache.*</span></span>

<span data-ttu-id="64812-111">要解决此问题，请确保已在 Dataverse 中安装了双写入核心解决方案。</span><span class="sxs-lookup"><span data-stu-id="64812-111">To fix the issue, make sure that the dual-write core solution is installed in Dataverse.</span></span> <span data-ttu-id="64812-112">双写入核心解决方案是处理解决方案意识问题的前提。</span><span class="sxs-lookup"><span data-stu-id="64812-112">The dual-write core solution is a prerequisite for solution awareness.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]