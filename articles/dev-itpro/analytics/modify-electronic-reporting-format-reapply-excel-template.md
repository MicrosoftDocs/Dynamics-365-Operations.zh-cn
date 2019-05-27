---
title: 通过重新应用 Excel 模板修改电子申报格式
description: 此主题提供有关如何通过重新应用经修改的 Excel 模板修改用于生成业务文档的电子报告 (ER) 格式的信息。
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8707f7b184bb66648edd0e48672c5514a0a5caf1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544999"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a><span data-ttu-id="7a266-103">通过重新应用 Excel 模板修改电子申报格式</span><span class="sxs-lookup"><span data-stu-id="7a266-103">Modify Electronic reporting formats by reapplying Excel templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a266-104">电子报告 (ER) 工具用于生成电子格式的业务文档。</span><span class="sxs-lookup"><span data-stu-id="7a266-104">The Electronic reporting (ER) tool is used to generate business documents in an electronic format.</span></span> <span data-ttu-id="7a266-105">若要生成业务文档，您必须创建 ER 格式，然后使用 ER 设计器来定义业务文档的布局并指定其应包括的数据。</span><span class="sxs-lookup"><span data-stu-id="7a266-105">To generate a business document, you must create an ER format, and then use the ER designer to define the layout of the business document and specify the data that should be included in it.</span></span> <span data-ttu-id="7a266-106">随后您可以运行 ER 格式以生成业务文档。</span><span class="sxs-lookup"><span data-stu-id="7a266-106">You can then run the ER format to generate the business document.</span></span>

<span data-ttu-id="7a266-107">ER 工具可用于将业务文档生成为 Microsoft Excel 文件。</span><span class="sxs-lookup"><span data-stu-id="7a266-107">The ER tool can be used to generate business documents as Microsoft Excel files.</span></span> <span data-ttu-id="7a266-108">可以使用 Excel 文档作为这些文档的模板。</span><span class="sxs-lookup"><span data-stu-id="7a266-108">You can use an Excel document as a template for these documents.</span></span> <span data-ttu-id="7a266-109">若要在 ER 设计器中定义文档布局，可以将您要用作模板的 Excel 文档的内容导入到定义的 ER 格式中。</span><span class="sxs-lookup"><span data-stu-id="7a266-109">To define the document layout in the ER designer, you can import the contents of the Excel document that you want to use as a template into the defined ER format.</span></span> <span data-ttu-id="7a266-110">若要了解详细信息并实践此方案，播放任务指南 **ER 设计用于生成 OPENXML 格式的报表的配置**（7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677) 业务流程的一部分）。</span><span class="sxs-lookup"><span data-stu-id="7a266-110">For more details, and to practice this scenario, play the task guide **ER Design a configuration for generating reports in OPENXML format** (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span>

<span data-ttu-id="7a266-111">如果编辑用作业务文档模板的 Excel 文档，新的 ER 功能让您可以将更新的模板应用到 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="7a266-111">If you edit the Excel document that is used as a template for a business document, new ER functionality lets you reapply the updated template to the ER format.</span></span> <span data-ttu-id="7a266-112">ER 格式然后会更新，以便符合更新的模板。</span><span class="sxs-lookup"><span data-stu-id="7a266-112">The ER format is then updated so that it adheres to the updated template.</span></span> <span data-ttu-id="7a266-113">有关此功能的更多详细信息，请播放任务指南 **ER 通过重新应用 Excel 模板修改格式**（7.5.5.3 获取/开发 IT 服务/解决方案组件 (10683) 业务流程的一部分）。</span><span class="sxs-lookup"><span data-stu-id="7a266-113">For more details about this functionality, play the task guide **ER Modify a format by reapplying an Excel template** (part of the 7.5.5.3 Acquire/Develop IT service/solution components (10683) business process).</span></span> <span data-ttu-id="7a266-114">在导入更新的模板的任务指南步骤中，请使用付款报表 Excel 文件 SampleVendPaymWsReport2 修改后的模板作为模板。</span><span class="sxs-lookup"><span data-stu-id="7a266-114">In the task guide step where you import an updated template, use the modified template of the Payment Report Excel file, SampleVendPaymWsReport2, as a template.</span></span>
