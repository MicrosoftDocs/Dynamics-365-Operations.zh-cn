---
title: "使用快速导入/导出"
description: "快速导入导出的目的是让您使用较少的步骤导入和导出。"
author: margoc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Application User
ms.reviewer: margoc
ms.search.scope: AX 2012 R3 CU8, UnifiedOperations
ms.custom: 89041
ms.assetid: 990d64e6-d436-4c79-9bb5-bf8c5c5a048f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 
ms.dyn365.ops.version: AX 2012 R3 CU8
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5c54d0590856755e208ada9d97af7790a6de95ec
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="run-the-test-data-transfer-tool-beta-for-dynamics-ax-ax-2012"></a><span data-ttu-id="e082a-103">运行 Dynamics AX (AX 2012) 的数据传输工具（beta 版）</span><span class="sxs-lookup"><span data-stu-id="e082a-103">Run the Test Data Transfer Tool (beta) for Dynamics AX (AX 2012)</span></span>

[!include[banner](../../includes/banner.md)]


<span data-ttu-id="e082a-104">快速导入导出的目的是让您使用较少的步骤导入和导出。</span><span class="sxs-lookup"><span data-stu-id="e082a-104">The purpose of Quick import export is to let you import and export with fewer steps.</span></span>

<span data-ttu-id="e082a-105">我们添加了快速导入导出功能以使用户可以导入或导出他们希望迅速执行的简单作业。</span><span class="sxs-lookup"><span data-stu-id="e082a-105">We added the Quick Import Export feature to let users import or export simple jobs that they want to execute quickly.</span></span> <span data-ttu-id="e082a-106">理想情况下，在文件自动映射到系统，且用户不需要经过高级映射或创建重复导入或导出作业的情况下使用此功能。</span><span class="sxs-lookup"><span data-stu-id="e082a-106">Ideally this feature is used in scenarios in which a file automatically maps to the system and user does not need to go through advanced mapping or create repeated import or export jobs.</span></span>

-   <span data-ttu-id="e082a-107">此功能支持使用现成和自定义实体。</span><span class="sxs-lookup"><span data-stu-id="e082a-107">This feature supports working with both out-of-the-box and custom entities.</span></span>
-   <span data-ttu-id="e082a-108">您可以从文件导入，如果使用 ODBC 数据源，您可以选择要用于定义导入的查询。</span><span class="sxs-lookup"><span data-stu-id="e082a-108">You can import from files, and if you are using an ODBC data source, you can select a query to use to define your import.</span></span>
-   <span data-ttu-id="e082a-109">您必须以前已为 AX 或文件定义了源数据格式，并知道它们的位置。</span><span class="sxs-lookup"><span data-stu-id="e082a-109">You must have previously defined source data formats for either AX or File, and know where they are located.</span></span>
-   <span data-ttu-id="e082a-110">您不需要创建一个处理组来使用快速导入/导出，在执行导入或导出作业时系统将自动创建。</span><span class="sxs-lookup"><span data-stu-id="e082a-110">You do not need to create a processing group to use quick import/export, one will be automatically created by the system when executing the import or export job.</span></span> <span data-ttu-id="e082a-111">您也可以选择保留由快速导入/导出导入的数据的历史记录。</span><span class="sxs-lookup"><span data-stu-id="e082a-111">You can also choose keep the history of the data imported by the quick import/export.</span></span>

  <span data-ttu-id="e082a-112">请注意，快速导入导出假定您熟悉 DIXF 的概念。</span><span class="sxs-lookup"><span data-stu-id="e082a-112">Note that Quick import export assumes that you are familiar with the concepts of DIXF.</span></span>



