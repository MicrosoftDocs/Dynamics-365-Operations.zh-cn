---
title: 分析 Excel 格式的传入文档
description: 本主题提供有关设计电子申报 (ER) 格式以分析传入的 Microsoft Excel 文件中包含的内容的信息。
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 847b3309a3e0daf7b341c4ba4a58a8ea0902e61c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564511"
---
# <a name="parse-incoming-documents-in-excel-format"></a><span data-ttu-id="a1458-103">分析 Excel 格式的传入文档</span><span class="sxs-lookup"><span data-stu-id="a1458-103">Parse incoming documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a1458-104">您可以设计电子申报 (ER) 格式以分析传入的以 Microsoft Excel 工作簿的形式表示数据的 Microsoft Excel 文件（XLSX 格式的文件）。</span><span class="sxs-lookup"><span data-stu-id="a1458-104">You can design Electronic reporting (ER) formats to parse incoming Microsoft Excel files that represent data in Microsoft Excel workbooks (files in XLSX format).</span></span> <span data-ttu-id="a1458-105">然后可以使用这些文件中的内容更新申请表数据。</span><span class="sxs-lookup"><span data-stu-id="a1458-105">You can then use the content from these files to update application data.</span></span> <span data-ttu-id="a1458-106">这在以下情况下非常有用：</span><span class="sxs-lookup"><span data-stu-id="a1458-106">This is useful if you:</span></span>

- <span data-ttu-id="a1458-107">设计新的模型和格式并希望在运行时进行测试。</span><span class="sxs-lookup"><span data-stu-id="a1458-107">Design a new model and format and want to test them at run-time.</span></span> <span data-ttu-id="a1458-108">在这种情况下，Excel 将模拟实际的申请表数据。</span><span class="sxs-lookup"><span data-stu-id="a1458-108">In this case, Excel will simulate the actual application data.</span></span>
- <span data-ttu-id="a1458-109">不使用您的应用程序，而是在 Excel 中管理数据，并希望导入这些数据以提交特定报表。</span><span class="sxs-lookup"><span data-stu-id="a1458-109">Manage data beyond your application in Excel and want to import this data to submit a specific report.</span></span>

<span data-ttu-id="a1458-110">若要了解此功能的详细信息，请播放任务指南 **ER 从 Microsoft Excel 文件导入数据（第 1 部分：设计格式）** 和 **ER 从 Microsoft Excel 文件导入数据（第 2 部分：导入数据）**（这些任务指南属于 7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677) 业务流程）。</span><span class="sxs-lookup"><span data-stu-id="a1458-110">To learn more about this feature, play the task guides **ER Import data from a Microsoft Excel file (Part 1: Design format)** and **ER Import data from a Microsoft Excel file (Part 2: Import data)** (parts of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span> <span data-ttu-id="a1458-111">这些任务指南演练如何通过使用 ER 格式从传入的文档导入信息并更新申请表数据来分析传入的 Excel 文件。</span><span class="sxs-lookup"><span data-stu-id="a1458-111">These task guides walk through how the incoming Excel file can be parsed by using the ER format to import information from incoming documents and update application data.</span></span> <span data-ttu-id="a1458-112">可从 [Microsoft 下载中心](https://go.microsoft.com/fwlink/?linkid=874684)下载这些任务指南。</span><span class="sxs-lookup"><span data-stu-id="a1458-112">You can download the task guide files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

<span data-ttu-id="a1458-113">请下载以下文件以完成上面提到的任务指南。</span><span class="sxs-lookup"><span data-stu-id="a1458-113">Download the following files to complete the task guides mentioned above.</span></span>

| <span data-ttu-id="a1458-114">内容描述</span><span class="sxs-lookup"><span data-stu-id="a1458-114">Content description</span></span>                         | <span data-ttu-id="a1458-115">文件</span><span class="sxs-lookup"><span data-stu-id="a1458-115">File</span></span>                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="a1458-116">.XLSX 格式的传入文件 - 模板</span><span class="sxs-lookup"><span data-stu-id="a1458-116">Incoming file in .XLSX format - template</span></span>    | [<span data-ttu-id="a1458-117">1099import-template.xlsx</span><span class="sxs-lookup"><span data-stu-id="a1458-117">1099import-template.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
| <span data-ttu-id="a1458-118">.XLSX 格式的传入文件 - 示例数据</span><span class="sxs-lookup"><span data-stu-id="a1458-118">Incoming file in .XLSX format - sample data</span></span> | [<span data-ttu-id="a1458-119">1099import-data.xlsx</span><span class="sxs-lookup"><span data-stu-id="a1458-119">1099import-data.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)     |

<span data-ttu-id="a1458-120">如果尚未在当前 Finance and Operations 应用程序中播放任务指南 [ER 创建要从外部文件导入数据所需的配置](./tasks/er-required-configurations-import-data.md)，请下载以下文件。</span><span class="sxs-lookup"><span data-stu-id="a1458-120">If you have not yet played the following task guide, [ER Create required configurations to import data from an external file](./tasks/er-required-configurations-import-data.md) in the current Finance and Operations application, download the following file.</span></span>

| <span data-ttu-id="a1458-121">内容描述</span><span class="sxs-lookup"><span data-stu-id="a1458-121">Content description</span></span>    | <span data-ttu-id="a1458-122">文件</span><span class="sxs-lookup"><span data-stu-id="a1458-122">File</span></span>                                                            |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="a1458-123">ER 模型配置</span><span class="sxs-lookup"><span data-stu-id="a1458-123">ER model configuration</span></span> | [<span data-ttu-id="a1458-124">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="a1458-124">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]