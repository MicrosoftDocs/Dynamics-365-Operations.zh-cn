---
title: 在 RCS 全局知识库中停用配置
description: 本主题描述如何在 RCS 全局知识库中停用配置。
author: JaneA07
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 2bd22e991de376cfd93f75158f1f29716d2559e1
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018725"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a><span data-ttu-id="048b4-103">在 RCS 全局知识库中停用配置</span><span class="sxs-lookup"><span data-stu-id="048b4-103">Discontinue configurations in the RCS Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="048b4-104">本主题描述如何在 RCS 全局知识库中停用配置。</span><span class="sxs-lookup"><span data-stu-id="048b4-104">This topic describes how to discontinue configuration in the RCS Global repository.</span></span> <span data-ttu-id="048b4-105">以前，只能删除不再需要的配置。</span><span class="sxs-lookup"><span data-stu-id="048b4-105">Previously, it was possible only to delete configurations that were no longer required.</span></span> <span data-ttu-id="048b4-106">但是，您现在可以在 RCS 全局知识库中将已发布的配置标记为 **已停用**。</span><span class="sxs-lookup"><span data-stu-id="048b4-106">However now you can mark a released configuration as **Discontinued** in the RCS Global repository.</span></span> <span data-ttu-id="048b4-107">使用此功能，您还可以执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="048b4-107">With this functionality, you can also do the following:</span></span> 
 
 - <span data-ttu-id="048b4-108">计划停用配置时提供预先通知。</span><span class="sxs-lookup"><span data-stu-id="048b4-108">Provide up front notifications when a configuration is planned to be discontinued.</span></span>
 - <span data-ttu-id="048b4-109">包括有关替换配置的适用详细信息。</span><span class="sxs-lookup"><span data-stu-id="048b4-109">Include applicable details about the replacement configuration.</span></span>
 - <span data-ttu-id="048b4-110">为特定配置设置一个 **支持截止日期**，以通知用户何时停用该配置。</span><span class="sxs-lookup"><span data-stu-id="048b4-110">Set a **Supported until** date for the specific configuration to inform the user when it will be discontinued.</span></span>

<span data-ttu-id="048b4-111">停用配置版本时，可以指定以下可选信息：</span><span class="sxs-lookup"><span data-stu-id="048b4-111">When you discontinue a configuration version, you can specify the following optional information:</span></span>

  - <span data-ttu-id="048b4-112">**替换配置**</span><span class="sxs-lookup"><span data-stu-id="048b4-112">**Replacement configuration**</span></span>
  - <span data-ttu-id="048b4-113">**替换配置版本**</span><span class="sxs-lookup"><span data-stu-id="048b4-113">**Replacement configuration version**</span></span>
  - <span data-ttu-id="048b4-114">**自由文本注释**：使用此字段可提供文档链接或参考</span><span class="sxs-lookup"><span data-stu-id="048b4-114">**Free text note**: Use this field to provide documentation links or references</span></span>
  - <span data-ttu-id="048b4-115">**支持截止日期**：此字段提供当前配置/版本的建议支持截止日期。</span><span class="sxs-lookup"><span data-stu-id="048b4-115">**Supported until**: This field provides the proposed date up to which the current configuration/version will be supported.</span></span> <span data-ttu-id="048b4-116">此日期必须手动更新。</span><span class="sxs-lookup"><span data-stu-id="048b4-116">This date must be updated manually.</span></span>
  
<span data-ttu-id="048b4-117">要停用配置，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="048b4-117">To discontinue the configuration, complete the following steps.</span></span> 

1. <span data-ttu-id="048b4-118">通过将 **所有版本** 设置为 **是**，选择在一次操作中是要停用单个版本，还是要停用具有相同设置的所有版本。</span><span class="sxs-lookup"><span data-stu-id="048b4-118">Select whether you want to discontinue a single version or all versions with the same settings in one operation by setting **All versions** to **Yes**.</span></span> 
2. <span data-ttu-id="048b4-119">将 **停用** 参数设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="048b4-119">Set the **Discontinue** parameter to **Yes**.</span></span>
3. <span data-ttu-id="048b4-120">选择 **确定** 以停用配置。</span><span class="sxs-lookup"><span data-stu-id="048b4-120">Select **OK** to discontinue the configurations.</span></span> <span data-ttu-id="048b4-121">保存更改时，将填充 **停用日期** 字段。</span><span class="sxs-lookup"><span data-stu-id="048b4-121">The **Discontinued date** field will be populated when you save the changes.</span></span>

![停用配置信息](media/Discontinue-details-2.png)
  
<span data-ttu-id="048b4-123">您可以将配置恢复为 **共享**，或者可以随时调整停用信息。</span><span class="sxs-lookup"><span data-stu-id="048b4-123">You can revert configuration back to **Shared** or adjust discontinuation information at any time.</span></span> <span data-ttu-id="048b4-124">如果您共享配置，请指定 **支持截止日期** 以及与停用有关的所有其他信息，以表明您计划将来停用。</span><span class="sxs-lookup"><span data-stu-id="048b4-124">If you share a configuration, specify the **Supported until** date and all other information related to the discontinuation to indicate your plans for future discontinuation.</span></span>

<span data-ttu-id="048b4-125">如果您要共享有关计划停用的信息，则在实际停用配置之前，用户可以预填写与替换有关的所有字段，但可以将 **停用** 参数设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="048b4-125">If you want to share information about a planned discontinuation, prior to actually discontinuing the configuration, user is able to prefill all fields related to replacement but leave the **Discontinue** parameter set to **No**.</span></span>

> [!NOTE]
> <span data-ttu-id="048b4-126">停用不限制配置的相关操作。</span><span class="sxs-lookup"><span data-stu-id="048b4-126">Discontinuation doesn't limit operations with configurations.</span></span> <span data-ttu-id="048b4-127">您可以继续导入、运行或导出配置，这些字段仅供参考。</span><span class="sxs-lookup"><span data-stu-id="048b4-127">You can continue to import, run, or derive the configurations, these fields are informational.</span></span>

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a><span data-ttu-id="048b4-128">财务支持从版本 10.0.14 开始显示此信息</span><span class="sxs-lookup"><span data-stu-id="048b4-128">Finance supports displaying this information starting in version 10.0.14</span></span>

<span data-ttu-id="048b4-129">从版本 10.0.14 开始，Dynamics 365 Finance 支持显示停用信息。</span><span class="sxs-lookup"><span data-stu-id="048b4-129">Starting in version 10.0.14, Dynamics 365 Finance supports displaying discontinuation information.</span></span> <span data-ttu-id="048b4-130">在 **全局知识库** 页面上，您可以查看与停用有关的最新信息。</span><span class="sxs-lookup"><span data-stu-id="048b4-130">On the **Global repository** page, you can view up to date information related to discontinuation.</span></span> <span data-ttu-id="048b4-131">默认情况下，停用的配置会被过滤掉。</span><span class="sxs-lookup"><span data-stu-id="048b4-131">By default, configurations that are discontinued are filtered out.</span></span>
  
<span data-ttu-id="048b4-132">**导入的配置** (ERSolutionTable) 页面显示导入时已经停用的配置。</span><span class="sxs-lookup"><span data-stu-id="048b4-132">The **Imported configurations** (ERSolutionTable) page, shows configurations that were already discontinued when there were imported.</span></span> <span data-ttu-id="048b4-133">对于在导入后停用的那些配置，可以通过运行 **导入配置更新** 作业来同步停用信息。</span><span class="sxs-lookup"><span data-stu-id="048b4-133">For those configurations that were discontinued after import, the discontinuation information can be synchronized by running the **Import configurations updates** job.</span></span>


