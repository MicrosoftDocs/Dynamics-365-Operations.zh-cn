---
title: Regulatory Configuration Service (RCS) - 删除 RCS 环境
description: 本主题说明了 Regulatory Configuration Service (RCS) 系统管理员可以如何删除 RCS 环境和相关数据。
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 637962cf63bfd8c2330726f33545f939ec91d58d
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295810"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a><span data-ttu-id="6b7c9-103">Regulatory Configuration Service (RCS) - 删除 RCS 环境</span><span class="sxs-lookup"><span data-stu-id="6b7c9-103">Regulatory Configuration Service (RCS) - Delete an RCS environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b7c9-104">本主题说明了 Regulatory Configuration Service (RCS) 系统管理员可以如何删除 RCS 环境和相关数据。</span><span class="sxs-lookup"><span data-stu-id="6b7c9-104">This topic explains how a Regulatory Configuration Service (RCS) system administrator can delete an RCS environment and related data.</span></span>

<span data-ttu-id="6b7c9-105">在完成本主题中的过程之前，必须满足以下先决条件：</span><span class="sxs-lookup"><span data-stu-id="6b7c9-105">Before you can complete the procedure in this topic, the following prerequisites must be met:</span></span>

- <span data-ttu-id="6b7c9-106">您必须拥有为 RCS 环境分配给您的 **系统管理员** 角色。</span><span class="sxs-lookup"><span data-stu-id="6b7c9-106">You must have the **System Admin** role assigned to you for the RCS environment.</span></span>
- <span data-ttu-id="6b7c9-107">**系统管理员** 角色必须具有分配给它的 **RCSDeleteEnvironmentDuty** 角色。</span><span class="sxs-lookup"><span data-stu-id="6b7c9-107">The **System Admin** role must have the **RCSDeleteEnvironmentDuty** role assigned to it.</span></span>

## <a name="delete-an-rcs-environment"></a><span data-ttu-id="6b7c9-108">删除 RCS 环境</span><span class="sxs-lookup"><span data-stu-id="6b7c9-108">Delete an RCS environment</span></span>

1. <span data-ttu-id="6b7c9-109">打开 RCS，然后选择 **电子申报** 工作区磁贴。</span><span class="sxs-lookup"><span data-stu-id="6b7c9-109">Open RCS, and select the **Electronic reporting** workspace tile.</span></span>
2. <span data-ttu-id="6b7c9-110">在 **相关链接** 部分中，选择 **删除 RCS 环境**。</span><span class="sxs-lookup"><span data-stu-id="6b7c9-110">In the **Related links** section, select **Delete RCS environment**.</span></span>

    ![相关链接部分中的删除 RCS 环境链接](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. <span data-ttu-id="6b7c9-112">在显示的对话框中，查看有关环境删除的范围的消息。</span><span class="sxs-lookup"><span data-stu-id="6b7c9-112">In the dialog box that appears, review the messages about the scope of environment deletion.</span></span>

    ![删除 RCS 环境对话框中的消息](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > <span data-ttu-id="6b7c9-114">无法撤销 RCS 环境的删除。</span><span class="sxs-lookup"><span data-stu-id="6b7c9-114">Deletion of an RCS environment can't be reversed.</span></span>
    >
    > <span data-ttu-id="6b7c9-115">该操作会删除选定的 RCS 环境和任何相关数据，包括存储在全局存储库中的功能和配置。</span><span class="sxs-lookup"><span data-stu-id="6b7c9-115">The operation deletes the selected RCS environment and any related data, including features and configurations that are stored in the Global repository.</span></span> <span data-ttu-id="6b7c9-116">如果没有依赖关系，与其他组织共享的功能和配置将取消共享并删除。</span><span class="sxs-lookup"><span data-stu-id="6b7c9-116">Features and configurations that are shared with other organizations will be unshared and deleted if they have no dependencies.</span></span> <span data-ttu-id="6b7c9-117">具有依赖关系的功能和配置将标记为已停用。</span><span class="sxs-lookup"><span data-stu-id="6b7c9-117">Features and configurations that have dependencies will be marked as discontinued.</span></span>

4. <span data-ttu-id="6b7c9-118">在提供的字段中，输入 RCS 环境的全局唯一标识符 (GUID) 以确认您要删除它。</span><span class="sxs-lookup"><span data-stu-id="6b7c9-118">In the field that is provided, enter the globally unique identifier (GUID) of the RCS environment to confirm that you want to delete it.</span></span> <span data-ttu-id="6b7c9-119">环境的 GUID 包含在删除消息中。</span><span class="sxs-lookup"><span data-stu-id="6b7c9-119">The environment's GUID is included in the deletion message.</span></span>
5. <span data-ttu-id="6b7c9-120">选择 **删除环境**。</span><span class="sxs-lookup"><span data-stu-id="6b7c9-120">Select **Delete environment**.</span></span>
    
<span data-ttu-id="6b7c9-121">现在将删除您的 RCS 环境和任何相关数据。</span><span class="sxs-lookup"><span data-stu-id="6b7c9-121">Your RCS environment and any related data are now deleted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b7c9-122">删除 RCS 环境后，将无法恢复数据。</span><span class="sxs-lookup"><span data-stu-id="6b7c9-122">After you delete an RCS environment, there is no way to recover the data.</span></span> <span data-ttu-id="6b7c9-123">可以在任何可用的 RCS 区域中创建新的 RCS 环境。</span><span class="sxs-lookup"><span data-stu-id="6b7c9-123">A new RCS environment can be created in any available RCS region.</span></span>
