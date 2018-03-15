---
title: "从包含多个工作表的 Excel 数据实体模板中导入数据"
description: "此主题介绍如何使用 Excel 数据实体模板将数据导入 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition。"
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: af7f9a373496eee4df354d5dd9e5a25c51317c43
ms.openlocfilehash: b314a649829dd14a525923802e19b847dc5a115e
ms.contentlocale: zh-cn
ms.lasthandoff: 02/27/2018

---

# <a name="excel-templates-with-multiple-worksheets"></a><span data-ttu-id="cb03d-103">包含多个工作表的 Excel 模板</span><span class="sxs-lookup"><span data-stu-id="cb03d-103">Excel templates with multiple worksheets</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cb03d-104">Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中的数据管理支持基于 Microsoft Excel 的数据实体模板。</span><span class="sxs-lookup"><span data-stu-id="cb03d-104">Data management in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition supports Microsoft Excel-based templates for data entities.</span></span> <span data-ttu-id="cb03d-105">这些模板可能包含一个或多个工作表。</span><span class="sxs-lookup"><span data-stu-id="cb03d-105">These templates can contain one or more worksheets.</span></span> <span data-ttu-id="cb03d-106">使用包含多个工作表的模板通常是为了方便在一个文件中管理数据并将其导入到多个数据实体中。</span><span class="sxs-lookup"><span data-stu-id="cb03d-106">Templates with multiple worksheets are often used when it is convenient to manage data in a single file and import it to multiple data entities.</span></span> <span data-ttu-id="cb03d-107">例如站点和仓库。</span><span class="sxs-lookup"><span data-stu-id="cb03d-107">An example would be sites and warehouses.</span></span>

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a><span data-ttu-id="cb03d-108">一次性上传文件，并将其映射到所有实体</span><span class="sxs-lookup"><span data-stu-id="cb03d-108">Upload a file once and map it to all entities</span></span>
<span data-ttu-id="cb03d-109">举个例子，有一个 Excel 文件包含名称为**站点**和**仓库**的工作表。</span><span class="sxs-lookup"><span data-stu-id="cb03d-109">Let’s take an example where there is one Excel file with worksheets called **Sites** and **Warehouses**.</span></span> <span data-ttu-id="cb03d-110">若要设置数据导入项目，则添加第一个数据实体**站点**，然后上传文件。</span><span class="sxs-lookup"><span data-stu-id="cb03d-110">To set up the data import project, you would add the first data entity, **Sites** and then upload the file.</span></span> <span data-ttu-id="cb03d-111">您可以选择**站点**作为要对该实体使用的工作表。</span><span class="sxs-lookup"><span data-stu-id="cb03d-111">You will be able to select **Sites** as the worksheet to be used for this entity.</span></span>

<span data-ttu-id="cb03d-112">如果您在不离开**添加文件**窗体的情况下添加第二个实体**仓库**，您可以通过工作表查找功能选择**仓库**工作表，无需再一次上传文件。</span><span class="sxs-lookup"><span data-stu-id="cb03d-112">If you add the second entity **Warehouses** without leaving the **Add file** form, the worksheet lookup will let you select the **Warehouses** worksheet without having to upload the file again.</span></span> <span data-ttu-id="cb03d-113">若要上传新文件，唯一的原因是**仓库**数据位于不同的文件中。</span><span class="sxs-lookup"><span data-stu-id="cb03d-113">The only reason to upload a new file would be if the **Warehouses** data was in a different file.</span></span>

![多个工作表](./media/AddFileMultipleWorkSheets.png) 

## <a name="fix-worksheet-to-entity-mapping"></a><span data-ttu-id="cb03d-115">将工作表固定到实体映射</span><span class="sxs-lookup"><span data-stu-id="cb03d-115">Fix worksheet to entity mapping</span></span>

<span data-ttu-id="cb03d-116">可以从网格固定在导入作业中将工作表映射到数据实体。</span><span class="sxs-lookup"><span data-stu-id="cb03d-116">The mapping of the worksheet to a data entity in the import job can be fixed from the grid.</span></span> <span data-ttu-id="cb03d-117">网格中的**工作表**列显示进行映射的文件的工作表。</span><span class="sxs-lookup"><span data-stu-id="cb03d-117">The **Worksheet** column in the grid shows the worksheets from the file that was mapped.</span></span> <span data-ttu-id="cb03d-118">您可以从下拉菜单中选择不同的工作表。</span><span class="sxs-lookup"><span data-stu-id="cb03d-118">You can choose a different worksheet from the drop-down menu.</span></span> <span data-ttu-id="cb03d-119">如果选中的工作表已经映射到数据项目中的实体，系统将要求您确认更改。</span><span class="sxs-lookup"><span data-stu-id="cb03d-119">If the chosen worksheet is already mapped to an entity in the data project, the system asks you to confirm the change.</span></span> <span data-ttu-id="cb03d-120">我们建议您固定网格中的所有映射。</span><span class="sxs-lookup"><span data-stu-id="cb03d-120">We recommend that you fix all mappings in the grid.</span></span>

![更新工作表映射](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a><span data-ttu-id="cb03d-122">重新映射到新文件</span><span class="sxs-lookup"><span data-stu-id="cb03d-122">Re-map to a new file</span></span>

<span data-ttu-id="cb03d-123">如果必须为数据项目中的现有实体上传相同文件的新版本或全新文件，必须使用**添加文件**体验再次添加实体，如同是第一次添加这些实体一样。</span><span class="sxs-lookup"><span data-stu-id="cb03d-123">In cases where a new version of the same file or a completely new file must be uploaded for existing entities in a data project, you must use the **Add file** experience, and add the entities again as if they were being added for the first time.</span></span> <span data-ttu-id="cb03d-124">在继续执行下一步操作之前，系统将询问您是否确定要覆盖数据项目中的现有实体。</span><span class="sxs-lookup"><span data-stu-id="cb03d-124">The system will confirm that you want to overwrite the existing entities in the data project before proceeding.</span></span> <span data-ttu-id="cb03d-125">未再次添加（或覆盖）的实体将继续保留之前来自上一个文件的映射。</span><span class="sxs-lookup"><span data-stu-id="cb03d-125">Entities that are not added again (or overwritten) will continue to hold the previous mappings from the previous file.</span></span>

## <a name="upload-a-file-using-run-project"></a><span data-ttu-id="cb03d-126">使用“运行项目”上传文件</span><span class="sxs-lookup"><span data-stu-id="cb03d-126">Upload a file using Run project</span></span>

<span data-ttu-id="cb03d-127">您可以在使用**运行项目**选项执行导入项目时上传 Excel 文件。</span><span class="sxs-lookup"><span data-stu-id="cb03d-127">You can upload an Excel file while using the **Run project** option to execute an import project.</span></span> <span data-ttu-id="cb03d-128">您必须注意，上传的文件仅包含与数据项目中的数据实体的现有映射相同的工作表。</span><span class="sxs-lookup"><span data-stu-id="cb03d-128">You must be careful to upload only files that have the same worksheets as the existing mappings on the data entities in the data project.</span></span> <span data-ttu-id="cb03d-129">如果在新上传的文件中找不到某个工作表，系统将显示错误，并停止导入。</span><span class="sxs-lookup"><span data-stu-id="cb03d-129">If a worksheet is not found in the newly uploaded file, the system displays an error and will stop the import.</span></span> <span data-ttu-id="cb03d-130">如果必须对某个实体更改到工作表的映射，必须先从数据项目内部更新数据项目中的映射，然后在**运行项目**体验中使用文件。</span><span class="sxs-lookup"><span data-stu-id="cb03d-130">If the mapping to the worksheet must be changed for an entity, then the mappings in the data project must be first updated from within the data project before using the file in the **Run project** experience.</span></span>


