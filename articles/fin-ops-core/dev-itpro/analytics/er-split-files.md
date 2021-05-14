---
title: 基于文件大小和内容数量拆分生成的 XML 文件
description: 本主题提供有关如何基于文件大小和内容项数量拆分生成的文件的信息。
author: NickSelin
ms.date: 04/23/2021
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
ms.openlocfilehash: 9b0c8d215d1932a4c897488cb9c6ed7fa2127d82
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944333"
---
# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a><span data-ttu-id="34b91-103">基于文件大小和内容数量拆分生成的 XML 文件</span><span class="sxs-lookup"><span data-stu-id="34b91-103">Split generated XML files based on file size and content quantity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="34b91-104">可以设计电子申报 (ER) 格式以生成 XML 格式的传出单据。</span><span class="sxs-lookup"><span data-stu-id="34b91-104">You can design Electronic reporting (ER) formats to generate outgoing documents in XML format.</span></span> <span data-ttu-id="34b91-105">有时，仅当这些单据满足特定条件（如最大文件大小或某些 XML 节点的最大数量）时，才能被接受。</span><span class="sxs-lookup"><span data-stu-id="34b91-105">Sometimes, those documents can be accepted only when they meet specific criteria, such a maximum file size or a maximum number of some XML nodes.</span></span> <span data-ttu-id="34b91-106">可设计 ER 格式以生成满足这些单据指定的收货要求的电子单据。</span><span class="sxs-lookup"><span data-stu-id="34b91-106">You can design ER formats to generate electronic documents that satisfy the requirements that the recipients of those documents specify.</span></span>

- <span data-ttu-id="34b91-107">对于 FILE 格式元素，可以以 ER 表达式的形式定义文件大小限制。</span><span class="sxs-lookup"><span data-stu-id="34b91-107">For the FILE format element, you can define a limit on the file size as an ER expression.</span></span> <span data-ttu-id="34b91-108">如果在生成 ER 报表时超过了定义的限制，ER 将完成当前文件的创建，然后继续创建下一个文件。</span><span class="sxs-lookup"><span data-stu-id="34b91-108">If the defined limit is exceeded when an ER report is generated, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="34b91-109">对于任何 XML ELEMENT 格式，可以以 ER 表达式的形式定义元素数量限制。</span><span class="sxs-lookup"><span data-stu-id="34b91-109">For any XML ELEMENT format, you can define a limit on the number of elements as an ER expression.</span></span> <span data-ttu-id="34b91-110">如果在运行 ER 报表时生成的文件中的 XML 节点数量超过了定义的限制，ER 将完成当前文件的创建，然后继续创建下一个文件。</span><span class="sxs-lookup"><span data-stu-id="34b91-110">If the number of XML nodes in the file that is generated exceeds the defined limit when an ER report is run, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="34b91-111">对于任何 XML SEQUENCE 格式元素，可以以 ER 表达式的形式定义子元素数量限制。</span><span class="sxs-lookup"><span data-stu-id="34b91-111">For any XML SEQUENCE format element, you can define a limit on the number of child elements as an ER expression.</span></span> <span data-ttu-id="34b91-112">如果在运行 ER 报表时生成的文件中的格式元素的嵌套 XML 节点数量超过了定义的限制，ER 将完成当前文件的创建，然后继续创建下一个文件。</span><span class="sxs-lookup"><span data-stu-id="34b91-112">If the number of nested XML nodes of the format element in the generated file exceeds the defined limit when an ER report is run, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="34b91-113">可将任何 XML ELEMENT 格式元素标记为不可拆分。</span><span class="sxs-lookup"><span data-stu-id="34b91-113">You can mark any XML ELEMENT format element as non-breakable.</span></span> <span data-ttu-id="34b91-114">这样就可以将生成的 XML 节点的嵌套项保留在生成的单个文件的格式元素下。</span><span class="sxs-lookup"><span data-stu-id="34b91-114">In this way, you can keep the nested items of XML nodes that are generated under the format element in a single generated file.</span></span>

<span data-ttu-id="34b91-115">除了使用 XML ELEMENT 和 XML SEQUENCE 格式元素向生成的文件添加 XML 节点，还可以使用原始 XML 格式元素。</span><span class="sxs-lookup"><span data-stu-id="34b91-115">In addition to using the XML ELEMENT and XML SEQUENCE format elements to add XML nodes to the generated file, you can use the RAW XML format element.</span></span> <span data-ttu-id="34b91-116">但是，计算节点数量以便为元素数量限制求值时，将不考虑使用原始 RAW XML 格式元素添加的节点。</span><span class="sxs-lookup"><span data-stu-id="34b91-116">However, nodes that you add by using the RAW XML format element aren't considered when the number of nodes is calculated to evaluate the limits on the number of elements.</span></span>

<span data-ttu-id="34b91-117">如果为已配置为只要超过了特定限制就拆分生成的输出的 FILE 格式元素配置了文件目标，则将生成的输出的每一段作为单个文件发送到配置的文件目标。</span><span class="sxs-lookup"><span data-stu-id="34b91-117">If you configured file destinations for a FILE format element that has been configured to split the generated output whenever specific limits are exceeded, each piece of generated output is sent to the configured file destination as an individual file.</span></span> <span data-ttu-id="34b91-118">若要为通过拆分输出创建的文件唯一命名，必须为 FILE 格式元素配置 ER 表达式。</span><span class="sxs-lookup"><span data-stu-id="34b91-118">To uniquely name the files that are created by splitting the output, you must configure an ER expression for the FILE format element.</span></span> <span data-ttu-id="34b91-119">如果添加 NUMBER SEQUENCE 类型的 ER 数据源，拆分的输出的每一段的编号规则将采用递增方式。</span><span class="sxs-lookup"><span data-stu-id="34b91-119">If you include an ER data source of the NUMBER SEQUENCE type, the number sequence will be incremented for each piece of the split output.</span></span>

<span data-ttu-id="34b91-120">若要了解此功能的详细信息，请播放 **ER 基于文件大小或内容项数量拆分 XML 文件** 任务指南，该任务指南属于 **7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)** 业务流程，可从 [Microsoft 下载中心](https://go.microsoft.com/fwlink/?linkid=874684)下载。</span><span class="sxs-lookup"><span data-stu-id="34b91-120">To learn more about this feature, play the **ER Split XML files based on the file size or content item quantity** task guide, which is part of the **7.5.4.3 Acquire/Develop IT service/solution components (10677)** business process and can be downloaded from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="34b91-121">此任务指南可以引导您完成配置 ER 格式以根据文件大小和内容项数量拆分生成的文件这一过程。</span><span class="sxs-lookup"><span data-stu-id="34b91-121">This task guide walks you through the process of configuring an ER format to split generated files based on limits on the file size and content item quantity.</span></span> <span data-ttu-id="34b91-122">若要完成此任务指南，必须下载以下文件：</span><span class="sxs-lookup"><span data-stu-id="34b91-122">To complete the task guide, you must download the following files:</span></span>

- [<span data-ttu-id="34b91-123">ER 模型配置 - XmlFilesSplittingModel.xml</span><span class="sxs-lookup"><span data-stu-id="34b91-123">ER model configuration - XmlFilesSplittingModel.xml</span></span>](https://download.microsoft.com/download/e/a/f/eaffe96a-22ec-4a32-898a-f4328c91c387/XmlFilesSplittingModel.xml)
- [<span data-ttu-id="34b91-124">ER 格式配置 - XmlFilesSplittingFormat.xml</span><span class="sxs-lookup"><span data-stu-id="34b91-124">ER format configuration - XmlFilesSplittingFormat.xml</span></span>](https://download.microsoft.com/download/e/9/c/e9c5849b-8254-4cdf-bb00-4c2ebc72ddec/XmlFilesSplittingFormat.xml)

## <a name="additional-resources"></a><span data-ttu-id="34b91-125">其他资源</span><span class="sxs-lookup"><span data-stu-id="34b91-125">Additional resources</span></span>
[<span data-ttu-id="34b91-126">电子申报 (ER) 目标</span><span class="sxs-lookup"><span data-stu-id="34b91-126">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)

[<span data-ttu-id="34b91-127">电子申报中 (ER) 的配方设计器</span><span class="sxs-lookup"><span data-stu-id="34b91-127">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
