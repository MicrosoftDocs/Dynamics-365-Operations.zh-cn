---
title: RCS/全局知识库中的 RCS 增强筛选
description: 此主题介绍 RCS 全局知识库的增强筛选功能，已经改进了这些功能，以便包含更多筛选器。
author: JaneA07
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 1913b661c46af5e34da1a2939cb2a5d5b4e46411
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440629"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a><span data-ttu-id="2bf3d-103">RCS 增强筛选选项，用于在 RCS/全局知识库中查找配置</span><span class="sxs-lookup"><span data-stu-id="2bf3d-103">RCS enhanced filtering options for finding configurations in the RCS/Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2bf3d-104">此主题介绍 Regulatory Configuration Service (RCS) 全局知识库的增强筛选功能，经过改进，包括了具有以下条件的筛选功能：</span><span class="sxs-lookup"><span data-stu-id="2bf3d-104">This topic describes enhanced filtering capabilities for Regulatory Configuration Services (RCS) Global repository, which have been improved to include the ability to filter with the following criteria:</span></span> 
- <span data-ttu-id="2bf3d-105">**国家/地区** - 基于 ISO 国家/地区代码</span><span class="sxs-lookup"><span data-stu-id="2bf3d-105">**Country/region** - Based on ISO country codes</span></span>  
- <span data-ttu-id="2bf3d-106">以下 **标记** 类型：</span><span class="sxs-lookup"><span data-stu-id="2bf3d-106">**Tags** types for:</span></span>
  - <span data-ttu-id="2bf3d-107">功能区域</span><span class="sxs-lookup"><span data-stu-id="2bf3d-107">Functional area</span></span>
  - <span data-ttu-id="2bf3d-108">特征区域</span><span class="sxs-lookup"><span data-stu-id="2bf3d-108">Feature area</span></span>
  - <span data-ttu-id="2bf3d-109">行业</span><span class="sxs-lookup"><span data-stu-id="2bf3d-109">Industry</span></span> 
  - <span data-ttu-id="2bf3d-110">业务文档</span><span class="sxs-lookup"><span data-stu-id="2bf3d-110">Business document</span></span> 

<span data-ttu-id="2bf3d-111">为了更容易发现特定或相关的配置，您可以单独或成组应用筛选器。</span><span class="sxs-lookup"><span data-stu-id="2bf3d-111">To make it easier to discover specific or related configurations you can apply filters, either individually or as a group.</span></span> <span data-ttu-id="2bf3d-112">例如，要查找与供应商发票相关的单一类型的“可配置业务文档”，可以应用 **业务文档类型** 筛选器来搜索该类型的文档。</span><span class="sxs-lookup"><span data-stu-id="2bf3d-112">For example, to find a single type of 'configurable business documents that are related to vendor invoices, you could apply a **Business document type** filter to search for that type of document.</span></span> 

<span data-ttu-id="2bf3d-113">[![全局知识库的“筛选器”部分](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span><span class="sxs-lookup"><span data-stu-id="2bf3d-113">[![Filter section for Global repository](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span></span> 

<span data-ttu-id="2bf3d-114">您可以通过选择文档类型（例如，“供应商发票”）并单击 **应用筛选器** 来进一步细化搜索。</span><span class="sxs-lookup"><span data-stu-id="2bf3d-114">You can further refine the search by selecting document type, for example 'vendor invoice' and clicking **Apply filter**.</span></span> <span data-ttu-id="2bf3d-115">以下示例显示基于添加了文档类型的 **业务文档类型** 进行筛选时的结果。</span><span class="sxs-lookup"><span data-stu-id="2bf3d-115">The following example shows the results when filtering on **Business document type** with the document type added.</span></span> 

<span data-ttu-id="2bf3d-116">[![为业务文档类型应用的筛选器和导入](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span><span class="sxs-lookup"><span data-stu-id="2bf3d-116">[![Applied filter and Import for business document type](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span></span> 

<span data-ttu-id="2bf3d-117">可以将筛选结果单独或作为一组导入到用户 RCS 存储库或 Dynamics 365 Finance 环境中。</span><span class="sxs-lookup"><span data-stu-id="2bf3d-117">Filtered results can be imported into a users RCS repository or a Dynamics 365 Finance environment, either individually or as a set.</span></span> <span data-ttu-id="2bf3d-118">为此，请选择配置组，然后单击 **导入**。</span><span class="sxs-lookup"><span data-stu-id="2bf3d-118">To do this, select the group of configurations, and click **Import**.</span></span>
