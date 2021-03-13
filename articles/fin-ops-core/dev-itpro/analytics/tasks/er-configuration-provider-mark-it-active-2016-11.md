---
title: 创建配置提供程序并将其标记为有效
description: 本主题介绍获分配“系统管理员”或者“电子报告开发人员”角色的用户如何创建配置提供程序。
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 835e35ef233ba5734e5a4d47f624629e95ae5b89
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092052"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="3cbf4-103">创建配置提供程序并将其标记为有效</span><span class="sxs-lookup"><span data-stu-id="3cbf4-103">Create configuration providers and mark them as active</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3cbf4-104">本主题介绍获分配“系统管理员”或者“电子报表开发人员”角色的用户如何为“电子申报 (ER)”创建配置提供程序。</span><span class="sxs-lookup"><span data-stu-id="3cbf4-104">This topic explains how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="3cbf4-105">每个 ER 配置都将把该提供程序归类为其作者。</span><span class="sxs-lookup"><span data-stu-id="3cbf4-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="3cbf4-106">以样本公司 Litware，Inc. 为例，新建一个配置提供程序。这些步骤适用于所有公司，因为所有公司都共享 ER 配置提供程序。</span><span class="sxs-lookup"><span data-stu-id="3cbf4-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>

## <a name="create-a-provider"></a><span data-ttu-id="3cbf4-107">新建一个提供程序</span><span class="sxs-lookup"><span data-stu-id="3cbf4-107">Create a provider</span></span>
1. <span data-ttu-id="3cbf4-108">转到 **导航窗格** 的左上角，然后选择 **组织管理**。</span><span class="sxs-lookup"><span data-stu-id="3cbf4-108">Go to the **navigation pane** in the upper left corner and select **Organization administration**.</span></span>
2. <span data-ttu-id="3cbf4-109">转到 **工作区 > 电子申报**</span><span class="sxs-lookup"><span data-stu-id="3cbf4-109">Go to **Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="3cbf4-110">转到 **相关链接 > 配置提供程序**。</span><span class="sxs-lookup"><span data-stu-id="3cbf4-110">Go to **Related links > Configuration providers**.</span></span>
4. <span data-ttu-id="3cbf4-111">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="3cbf4-111">Select **New**.</span></span>
    - <span data-ttu-id="3cbf4-112">提供程序具有唯一名称和 URL。</span><span class="sxs-lookup"><span data-stu-id="3cbf4-112">A provider record has a unique name and URL.</span></span> <span data-ttu-id="3cbf4-113">如果已存在 Litware 公司 (https://www.litware.com) 的记录，则查看此页内容并跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="3cbf4-113">Review the content of this page and skip this procedure if a record for Litware, Inc. (https://www.litware.com) already exists.</span></span>  
5. <span data-ttu-id="3cbf4-114">在“名称”字段中，键入 `Litware, Inc.`。</span><span class="sxs-lookup"><span data-stu-id="3cbf4-114">In the Name field, type `Litware, Inc.`.</span></span>
6. <span data-ttu-id="3cbf4-115">在”Internet 地址“字段中，键入 `https://www.litware.com`。</span><span class="sxs-lookup"><span data-stu-id="3cbf4-115">In the Internet address field, type `https://www.litware.com`.</span></span>
7. <span data-ttu-id="3cbf4-116">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="3cbf4-116">Select **Save**.</span></span>
8. <span data-ttu-id="3cbf4-117">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3cbf4-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="3cbf4-118">选择为当前运行的提供程序</span><span class="sxs-lookup"><span data-stu-id="3cbf4-118">Select as an active provider</span></span>
1. <span data-ttu-id="3cbf4-119">选择 Litware 提供商。</span><span class="sxs-lookup"><span data-stu-id="3cbf4-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="3cbf4-120">选择 **设置有效**。</span><span class="sxs-lookup"><span data-stu-id="3cbf4-120">Select **Set active**.</span></span>

![电子申报工作区概览](../media/GER-Task-ActiveProvider-1.png)
