---
title: "使用电子申报工具生成电子文档并更新申请表数据"
description: "您可以设计可在 Finance and Operations 应用中用来生成传出电子文档的电子申报 (ER) 格式。 您还可以设计用于分析传入电子文档并使用这些文档中的内容更新应用程序数据的 ER 格式。"
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: af7f9a373496eee4df354d5dd9e5a25c51317c43
ms.openlocfilehash: e2447274016f517db3ec0eb8f55c6b3163822f50
ms.contentlocale: zh-cn
ms.lasthandoff: 02/27/2018

---

# <a name="generate-electronic-documents-and-update-application-data-using-the-electronic-reporting-tool"></a><span data-ttu-id="e7f29-104">使用电子申报工具生成电子文档并更新申请表数据</span><span class="sxs-lookup"><span data-stu-id="e7f29-104">Generate electronic documents and update application data using the Electronic reporting tool</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e7f29-105">您可以设计可在 Finance and Operations 应用中用来生成传出电子文档的电子申报 (ER) 格式。</span><span class="sxs-lookup"><span data-stu-id="e7f29-105">You can design Electronic reporting (ER) formats that can be used in the Finance and Operations application to generate outgoing electronic documents.</span></span> <span data-ttu-id="e7f29-106">您还可以设计用于分析传入电子文档并使用这些文档中的内容更新应用程序数据的 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="e7f29-106">You can also design ER formats that parse incoming electronic documents and use the content in those documents to update application data.</span></span> 

<span data-ttu-id="e7f29-107">借助此功能，可使用单个 ER 格式生成传出电子文档后再更新应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="e7f29-107">With this functionality, a single ER format can be used to generate outgoing electronic documents and then update the application data.</span></span> <span data-ttu-id="e7f29-108">此功能还可用于以下方案：</span><span class="sxs-lookup"><span data-stu-id="e7f29-108">This feature can be used in the following scenarios:</span></span>

- <span data-ttu-id="e7f29-109">为了防止在后续流程中重复使用应用程序数据，您可以在使用应用程序数据生成电子文档后立即标记该数据。</span><span class="sxs-lookup"><span data-stu-id="e7f29-109">To prevent repeated usage of application data in subsequent processes you can mark an application’s data immediately after it is used to generate electronic documents.</span></span> <span data-ttu-id="e7f29-110">例如，您可以将付款交易记录包含在生成的付款消息中后立即将其标记为已处理。</span><span class="sxs-lookup"><span data-stu-id="e7f29-110">For example, you can mark payment transactions as already processed immediately after they have been included in a generated payment message.</span></span>
- <span data-ttu-id="e7f29-111">使用 ER 逻辑存储已生成的电子文档的处理详细信息。</span><span class="sxs-lookup"><span data-stu-id="e7f29-111">To store the processing details of electronic documents that have been generated using ER logic.</span></span> <span data-ttu-id="e7f29-112">例如，使用 ER 表达式生成的唯一付款消息标识符。</span><span class="sxs-lookup"><span data-stu-id="e7f29-112">For example, a unique payment message identification that is generated using the ER expression.</span></span> <span data-ttu-id="e7f29-113">该表达式基于在运行 ER 格式生成文档时在 ER 对话框中输入的信息。</span><span class="sxs-lookup"><span data-stu-id="e7f29-113">The expression is based on information entered in the ER dialog box when the ER format is run to generate documents.</span></span>

<span data-ttu-id="e7f29-114">要了解有关此功能的更多信息，请播放一组 ER 生成带应用程序数据更新的文档任务指南（7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677) 业务流程的一部分），这些任务指南将带您浏览内部统计报告和存档的详细信息。</span><span class="sxs-lookup"><span data-stu-id="e7f29-114">To learn more about this feature, play the set of ER Generate documents with application data update Task guides (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process), which walk you through the details of Intrastat reporting and archiving.</span></span> <span data-ttu-id="e7f29-115">完成这些任务指南中的特定步骤需要以下文件。</span><span class="sxs-lookup"><span data-stu-id="e7f29-115">The following files are required to complete certain steps in these Task guides.</span></span> <span data-ttu-id="e7f29-116">将这些文件下载和保存到您的本地计算机。</span><span class="sxs-lookup"><span data-stu-id="e7f29-116">Download and save these files to your local machine.</span></span>

- [<span data-ttu-id="e7f29-117">ER 数据模型配置：内部统计（模型）</span><span class="sxs-lookup"><span data-stu-id="e7f29-117">ER data model configuration: Intrastat (model)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="e7f29-118">ER 模型映射配置：内部统计（映射）</span><span class="sxs-lookup"><span data-stu-id="e7f29-118">ER model mapping configuration: Intrastat (mapping)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="e7f29-119">ER 格式配置：内部统计（格式）</span><span class="sxs-lookup"><span data-stu-id="e7f29-119">ER format configuration: Intrastat (format)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)

