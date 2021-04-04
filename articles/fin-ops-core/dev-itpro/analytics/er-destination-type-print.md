---
title: 打印机 ER 目标类型
description: 本主题说明如何为电子报告 (ER) 格式的每个文件夹或文件组件配置打印机目标。
author: NickSelin
manager: AnnBe
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 19613d9dfba21d591d96a2df45bedb80c043b3a7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561942"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a><span data-ttu-id="df5a9-103">打印机目标</span><span class="sxs-lookup"><span data-stu-id="df5a9-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df5a9-104">您可以将生成的文档直接发送到网络打印机以进行直接打印。</span><span class="sxs-lookup"><span data-stu-id="df5a9-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="df5a9-105">先决条件</span><span class="sxs-lookup"><span data-stu-id="df5a9-105">Prerequisites</span></span>

<span data-ttu-id="df5a9-106">在开始之前，您必须安装和配置文档路线选择代理，然后注册网络打印机。</span><span class="sxs-lookup"><span data-stu-id="df5a9-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="df5a9-107">有关详细信息，请参阅[安装文档路线选择代理以启用网络打印](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent)。</span><span class="sxs-lookup"><span data-stu-id="df5a9-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="df5a9-108">使打印机目标可用</span><span class="sxs-lookup"><span data-stu-id="df5a9-108">Make the Printer destination available</span></span>

<span data-ttu-id="df5a9-109">为了使 **打印机** 目标在 Microsoft Dynamics 365 Finance 的当前实例中可用，请转到 **功能管理** 工作区，并按以下顺序打开以下功能：</span><span class="sxs-lookup"><span data-stu-id="df5a9-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="df5a9-110">将电子申报传出文档从 Microsoft Office 格式转换为 PDF</span><span class="sxs-lookup"><span data-stu-id="df5a9-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="df5a9-111">将文档路线选择代理作为传出文档的电子申报目标</span><span class="sxs-lookup"><span data-stu-id="df5a9-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="df5a9-112">[![在功能管理中打开 ER 打印机目标功能](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="df5a9-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="df5a9-113">适用性</span><span class="sxs-lookup"><span data-stu-id="df5a9-113">Applicability</span></span>

<span data-ttu-id="df5a9-114">只能对用于以可打印 PDF 格式（PDF 合并器或 PDF 文件格式元素）或 Microsoft Office Excel/Word 格式（Excel 文件）生成输出的文件组件配置 **打印机** 目标。</span><span class="sxs-lookup"><span data-stu-id="df5a9-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="df5a9-115">以 PDF 格式生成输出时，会将其发送到打印机。</span><span class="sxs-lookup"><span data-stu-id="df5a9-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="df5a9-116">以 Microsoft Office 格式生成输出时，它会自动转换为 PDF 格式，然后发送到打印机。</span><span class="sxs-lookup"><span data-stu-id="df5a9-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="df5a9-117">限制</span><span class="sxs-lookup"><span data-stu-id="df5a9-117">Limitations</span></span>

<span data-ttu-id="df5a9-118">系统仅针对云部署实施了 **打印机** 目标。</span><span class="sxs-lookup"><span data-stu-id="df5a9-118">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="df5a9-119">使用打印机目标</span><span class="sxs-lookup"><span data-stu-id="df5a9-119">Use the Printer destination</span></span>

1. <span data-ttu-id="df5a9-120">将 **已启用** 选项设置为 **是** 以将生成的文档发送到打印机。</span><span class="sxs-lookup"><span data-stu-id="df5a9-120">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="df5a9-121">在 **打印机名称** 字段中，选择所需的网络打印机。</span><span class="sxs-lookup"><span data-stu-id="df5a9-121">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="df5a9-122">将 **是否在打印存档文件中保存?** 设置为 **是**，以将生成的输出存储在打印存档文件中，以便将来可以进行打印。</span><span class="sxs-lookup"><span data-stu-id="df5a9-122">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="df5a9-123">要稍后访问存档的输出，请转到 **组织管理** \> **查询和报告** \> **报表存档**。</span><span class="sxs-lookup"><span data-stu-id="df5a9-123">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="df5a9-124">[![使用打印机目标](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="df5a9-124">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="df5a9-125">如果配置 **打印机** 目标，则不必打开 **转换成 PDF** 选项。</span><span class="sxs-lookup"><span data-stu-id="df5a9-125">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="df5a9-126">即使关闭该选项，也会进行用于打印用途的 PDF 转换。</span><span class="sxs-lookup"><span data-stu-id="df5a9-126">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

<span data-ttu-id="df5a9-127">要在以 Excel 格式打印传出文档时使用特定的 [页面方向](electronic-reporting-destinations.md#SelectPdfPageOrientation)，必须打开 **转换为 PDF** 选项。</span><span class="sxs-lookup"><span data-stu-id="df5a9-127">To use a specific [page orientation](electronic-reporting-destinations.md#SelectPdfPageOrientation) when you print an outbound document in Excel format, you must turn on the **Convert to PDF** option.</span></span> <span data-ttu-id="df5a9-128">当您将 **转换为 PDF** 选项设置为 **是** 时，**页面方向** 字段将可用。</span><span class="sxs-lookup"><span data-stu-id="df5a9-128">When you set the **Convert to PDF** option to **Yes**, the **Page orientation** field becomes available.</span></span> <span data-ttu-id="df5a9-129">在 **页面方向** 字段中，您可以选择页面方向。</span><span class="sxs-lookup"><span data-stu-id="df5a9-129">In the **Page orientation** field, you can select a page orientation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df5a9-130">其他资源</span><span class="sxs-lookup"><span data-stu-id="df5a9-130">Additional resources</span></span>

- [<span data-ttu-id="df5a9-131">电子报告 (ER) 概览</span><span class="sxs-lookup"><span data-stu-id="df5a9-131">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="df5a9-132">电子报告 (ER) 目标</span><span class="sxs-lookup"><span data-stu-id="df5a9-132">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
