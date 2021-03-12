---
title: 将子公司数据导出到文件
description: 本主题说明如何为从 Microsoft Dynamics 365 Finance 导出数据，然后将其导入到合并的法人作准备。
author: jinniew
manager: AnnBe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 179a401178935b8a76d6718a7fb1f63e08344f50
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968671"
---
# <a name="export-subsidiary-data-to-files"></a><span data-ttu-id="97690-103">将子公司数据导出到文件</span><span class="sxs-lookup"><span data-stu-id="97690-103">Export subsidiary data to files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97690-104">您使用 **导出** 页（**系统管理 \> 工作区 \> 导入/导出**）来准备将子公司数据导出到文件，然后再将其导入到合并的法人。</span><span class="sxs-lookup"><span data-stu-id="97690-104">You use the **Export** page (**System administration \> Workspaces \> Import/Export**) to prepare to export subsidiary data to files that can then be imported into a consolidated legal entity.</span></span> <span data-ttu-id="97690-105">有关导入和导出流程的详细信息，请参阅[数据导入和导出作业概述](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)。</span><span class="sxs-lookup"><span data-stu-id="97690-105">For more information about the import and export processes, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>

1. <span data-ttu-id="97690-106">为合并流程创建一个法人。</span><span class="sxs-lookup"><span data-stu-id="97690-106">Create a legal entity for the consolidation process.</span></span> <span data-ttu-id="97690-107">有关如何创建法人的信息，请参阅[创建法人](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md)。</span><span class="sxs-lookup"><span data-stu-id="97690-107">For information about how to create legal entities, see [Create a legal entity](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span></span> <span data-ttu-id="97690-108">有关详细信息，请参阅[准备一个法人以供在合并流程中使用](prepare-company-for-consolidation.md)和[设置要合并的子公司法人](set-up-subsidiary-company-for-consolidation.md)。</span><span class="sxs-lookup"><span data-stu-id="97690-108">For more information, see [Prepare a legal entity for use in the consolidation process](prepare-company-for-consolidation.md) and [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span> 

2. <span data-ttu-id="97690-109">转到 **合并 \> 导出公司余额**。</span><span class="sxs-lookup"><span data-stu-id="97690-109">Go to **Consolidations \> Export company balances**.</span></span> <span data-ttu-id="97690-110">在 **导出公司余额** 页上的 **条件** 选项卡上，通过设置以下字段指定合并的详细信息。</span><span class="sxs-lookup"><span data-stu-id="97690-110">On the **Export company balances** page, on the **Criteria** tab, specify the details of the consolidation by setting the following fields.</span></span>

    | <span data-ttu-id="97690-111">字段</span><span class="sxs-lookup"><span data-stu-id="97690-111">Field</span></span>                             | <span data-ttu-id="97690-112">说明</span><span class="sxs-lookup"><span data-stu-id="97690-112">Description</span></span> |
    |-----------------------------------|-------|
    | <span data-ttu-id="97690-113">主帐户</span><span class="sxs-lookup"><span data-stu-id="97690-113">Main account</span></span>                      | <span data-ttu-id="97690-114">指定要合并的帐户。</span><span class="sxs-lookup"><span data-stu-id="97690-114">Specify the accounts to consolidate.</span></span> <span data-ttu-id="97690-115">要包括所有帐户，请将此字段留空。</span><span class="sxs-lookup"><span data-stu-id="97690-115">To include all accounts, leave this field blank.</span></span> |
    | <span data-ttu-id="97690-116">使用合并帐户</span><span class="sxs-lookup"><span data-stu-id="97690-116">Use consolidation account</span></span>         | <span data-ttu-id="97690-117">如果您指定了合并帐户，请将此选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="97690-117">If you've specified consolidation accounts, set this option to **Yes**.</span></span> |
    | <span data-ttu-id="97690-118">选择合并帐户的来源</span><span class="sxs-lookup"><span data-stu-id="97690-118">Select consolidation account from</span></span> | <span data-ttu-id="97690-119">选择 **主帐户** 或 **合并帐户组**。</span><span class="sxs-lookup"><span data-stu-id="97690-119">Select either **Main account** or **Consolidation account group**.</span></span> |
    | <span data-ttu-id="97690-120">合并帐户组</span><span class="sxs-lookup"><span data-stu-id="97690-120">Consolidation account group</span></span>       | <span data-ttu-id="97690-121">为您选择的合并帐户选择合并帐户组。</span><span class="sxs-lookup"><span data-stu-id="97690-121">Select a consolidation account group for the consolidation account that you selected.</span></span> |
    | <span data-ttu-id="97690-122">合并期间</span><span class="sxs-lookup"><span data-stu-id="97690-122">Consolidation period</span></span>              | <span data-ttu-id="97690-123">为合并指定“开始”和“结束”日期。</span><span class="sxs-lookup"><span data-stu-id="97690-123">Specify "from" and "to" dates for the consolidation.</span></span> |
    | <span data-ttu-id="97690-124">包括实际金额</span><span class="sxs-lookup"><span data-stu-id="97690-124">Include actual amounts</span></span>            | <span data-ttu-id="97690-125">将此选项设置为 **是** 将包括实际金额。</span><span class="sxs-lookup"><span data-stu-id="97690-125">Set this option to **Yes** to include actual amounts.</span></span> |
    | <span data-ttu-id="97690-126">包括预算金额</span><span class="sxs-lookup"><span data-stu-id="97690-126">Include budget amounts</span></span>            | <span data-ttu-id="97690-127">将此选项设置为 **是** 将在合并中包括预算金额。</span><span class="sxs-lookup"><span data-stu-id="97690-127">Set this option to **Yes** to include budget amounts in consolidations.</span></span> |
    | <span data-ttu-id="97690-128">预算模型</span><span class="sxs-lookup"><span data-stu-id="97690-128">Budget models</span></span>                     | <span data-ttu-id="97690-129">指定要包括的预算模型。</span><span class="sxs-lookup"><span data-stu-id="97690-129">Specify the budget model to include.</span></span> |

3. <span data-ttu-id="97690-130">在 **财务维度** 选项卡上，指定合并的详细信息：</span><span class="sxs-lookup"><span data-stu-id="97690-130">On the **Financial dimensions** tab, specify the details of the consolidation:</span></span>

    - <span data-ttu-id="97690-131">指定应从子公司帐户交易记录转移到合并法人中的交易记录的财务维度信息。</span><span class="sxs-lookup"><span data-stu-id="97690-131">Specify the financial dimension information that should be transferred from the transactions in the subsidiary accounts to the transactions in the consolidated legal entity.</span></span>
    - <span data-ttu-id="97690-132">在列表中选择财务维度。</span><span class="sxs-lookup"><span data-stu-id="97690-132">Select financial dimensions in the list.</span></span>
    - <span data-ttu-id="97690-133">为合并的每个财务维度确定正确的规范。</span><span class="sxs-lookup"><span data-stu-id="97690-133">Identify the correct specification for each financial dimension that is consolidated.</span></span> <span data-ttu-id="97690-134">可用选项包括 **维度**、**组维度**、**公司帐户** 和 **帐户**。</span><span class="sxs-lookup"><span data-stu-id="97690-134">The available options include **Dimension**, **Group dimension**, **Company accounts**, and **Account**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="97690-135">**组维度** 选项可让您定义要合并的公司组使用的维度值。</span><span class="sxs-lookup"><span data-stu-id="97690-135">The **Group dimension** option lets you define the dimension value that is used by the group of companies that is being consolidated.</span></span>

    - <span data-ttu-id="97690-136">指定合并的段顺序。</span><span class="sxs-lookup"><span data-stu-id="97690-136">Specify the segment order to consolidate in.</span></span>

4. <span data-ttu-id="97690-137">在 **法人** 选项卡上，按照以下步骤指定要导出的法人实体：</span><span class="sxs-lookup"><span data-stu-id="97690-137">On the **Legal entities** tab, follow these steps to specify the legal entity that you're exporting:</span></span>

    1. <span data-ttu-id="97690-138">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="97690-138">Select **New**.</span></span>
    2. <span data-ttu-id="97690-139">在 **源法人** 字段中，输入法人。</span><span class="sxs-lookup"><span data-stu-id="97690-139">In the **Source legal entity** field, enter the legal entity.</span></span>

        <span data-ttu-id="97690-140">如果将相同的条件应用于同一数据卡中的若干子公司，您可以在一个操作中将这些子公司的数据转移到单独的导出文件中：</span><span class="sxs-lookup"><span data-stu-id="97690-140">If the same criteria apply to several subsidiaries that are in the same database, you can transfer data from those subsidiaries to separate export files in a single operation:</span></span>

        1. <span data-ttu-id="97690-141">为帐户应导出到文件的每个子公司法人创建一行。</span><span class="sxs-lookup"><span data-stu-id="97690-141">Create a line for each subsidiary legal entity for which accounts should be exported to files.</span></span> <span data-ttu-id="97690-142">这些文件以后将导入到合并的法人中。</span><span class="sxs-lookup"><span data-stu-id="97690-142">These files will be imported into the consolidated legal entity later.</span></span>
        2. <span data-ttu-id="97690-143">对于每个子公司，输入该子公司名称和在导出作业期间将创建的导出文件的名称。</span><span class="sxs-lookup"><span data-stu-id="97690-143">For each subsidiary, enter the subsidiary name and the name of the export file that will be created during the export job.</span></span>

    3. <span data-ttu-id="97690-144">在 **换算差额的科目类型** 字段中，选择 **损益** 或 **资产负债表**。</span><span class="sxs-lookup"><span data-stu-id="97690-144">In **Account type of conversion differences** field, Select **Profit and loss** or **Balance sheet**.</span></span>
    4. <span data-ttu-id="97690-145">为将要创建的导出文件输入文件名。</span><span class="sxs-lookup"><span data-stu-id="97690-145">Enter a file name for the export file that will be created.</span></span>

5. <span data-ttu-id="97690-146">选择 **确定** 运行导出。</span><span class="sxs-lookup"><span data-stu-id="97690-146">Select **OK** to run the export.</span></span>

<span data-ttu-id="97690-147">在导出完成后，您将收到一则消息，其中显示已在各文件中保存的记录的数目。</span><span class="sxs-lookup"><span data-stu-id="97690-147">When the export is completed, you receive a message that shows the number of records that were saved in each file.</span></span> <span data-ttu-id="97690-148">然后您可以将文件导入到合并的法人。</span><span class="sxs-lookup"><span data-stu-id="97690-148">You can then import the files into the consolidated legal entity.</span></span>
