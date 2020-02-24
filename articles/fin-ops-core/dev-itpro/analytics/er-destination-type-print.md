---
title: 打印机 ER 目标类型
description: 本主题说明如何为配置为以 PDF 或 Microsoft Office 格式 (Excel\Word) 生成出站文档的电子报告 (ER) 格式的每个文件夹或文件组件配置打印机目标。
author: NickSelin
manager: AnnBe
ms.date: 01/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 58e067baa130458e3a8e788d978604f208140a03
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019647"
---
# <a name="PrinterDestinationType"></a> <span data-ttu-id="bcdaf-103">打印机目标</span><span class="sxs-lookup"><span data-stu-id="bcdaf-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bcdaf-104">您可以将生成的文档直接发送到网络打印机以进行直接打印。</span><span class="sxs-lookup"><span data-stu-id="bcdaf-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bcdaf-105">先决条件</span><span class="sxs-lookup"><span data-stu-id="bcdaf-105">Prerequisites</span></span>

<span data-ttu-id="bcdaf-106">在开始之前，您必须安装和配置文档路线选择代理，然后注册网络打印机。</span><span class="sxs-lookup"><span data-stu-id="bcdaf-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="bcdaf-107">有关详细信息，请参阅[安装文档路线选择代理以启用网络打印](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent)。</span><span class="sxs-lookup"><span data-stu-id="bcdaf-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="bcdaf-108">使打印机目标可用</span><span class="sxs-lookup"><span data-stu-id="bcdaf-108">Make the Printer destination available</span></span>

<span data-ttu-id="bcdaf-109">为了使**打印机**目标在 Microsoft Dynamics 365 Finance 的当前实例中可用，请转到**功能管理**工作区，并按以下顺序打开以下功能：</span><span class="sxs-lookup"><span data-stu-id="bcdaf-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="bcdaf-110">将电子申报传出文档从 Microsoft Office 格式转换为 PDF</span><span class="sxs-lookup"><span data-stu-id="bcdaf-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="bcdaf-111">将文档路线选择代理作为传出文档的电子申报目标</span><span class="sxs-lookup"><span data-stu-id="bcdaf-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="bcdaf-112">[![在功能管理中打开 ER 打印机目标功能](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="bcdaf-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="bcdaf-113">适用性</span><span class="sxs-lookup"><span data-stu-id="bcdaf-113">Applicability</span></span>

<span data-ttu-id="bcdaf-114">只能对用于以可打印 PDF 格式（PDF 合并器或 PDF 文件格式元素）或 Microsoft Office Excel/Word 格式（Excel 文件）生成输出的文件组件配置**打印机**目标。</span><span class="sxs-lookup"><span data-stu-id="bcdaf-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="bcdaf-115">以 PDF 格式生成输出时，会将其发送到打印机。</span><span class="sxs-lookup"><span data-stu-id="bcdaf-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="bcdaf-116">以 Microsoft Office 格式生成输出时，它会自动转换为 PDF 格式，然后发送到打印机。</span><span class="sxs-lookup"><span data-stu-id="bcdaf-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="bcdaf-117">限制</span><span class="sxs-lookup"><span data-stu-id="bcdaf-117">Limitations</span></span>

<span data-ttu-id="bcdaf-118">此功能是预览功能，并受 [Microsoft Dynamics 365 Previews 补充使用条款](https://go.microsoft.com/fwlink/?linkid=2105274)中所描述的使用条款约束。</span><span class="sxs-lookup"><span data-stu-id="bcdaf-118">This feature is a preview feature and is subject to the terms of use that are described in [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://go.microsoft.com/fwlink/?linkid=2105274).</span></span>

<span data-ttu-id="bcdaf-119">系统仅针对云部署实施了**打印机**目标。</span><span class="sxs-lookup"><span data-stu-id="bcdaf-119">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="bcdaf-120">使用打印机目标</span><span class="sxs-lookup"><span data-stu-id="bcdaf-120">Use the Printer destination</span></span>

1. <span data-ttu-id="bcdaf-121">将**已启用**选项设置为**是**以将生成的文档发送到打印机。</span><span class="sxs-lookup"><span data-stu-id="bcdaf-121">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="bcdaf-122">在**打印机名称**字段中，选择所需的网络打印机。</span><span class="sxs-lookup"><span data-stu-id="bcdaf-122">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="bcdaf-123">将**是否在打印存档文件中保存?** 设置为**是**，以将生成的输出存储在打印存档文件中，以便将来可以进行打印。</span><span class="sxs-lookup"><span data-stu-id="bcdaf-123">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="bcdaf-124">要稍后访问存档的输出，请转到**组织管理** \> **查询和报告** \> **报表存档**。</span><span class="sxs-lookup"><span data-stu-id="bcdaf-124">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="bcdaf-125">[![使用打印机目标](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="bcdaf-125">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="bcdaf-126">如果配置**打印机**目标，则不必打开**转换成 PDF** 选项。</span><span class="sxs-lookup"><span data-stu-id="bcdaf-126">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="bcdaf-127">即使关闭该选项，也会进行用于打印用途的 PDF 转换。</span><span class="sxs-lookup"><span data-stu-id="bcdaf-127">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bcdaf-128">其他资源</span><span class="sxs-lookup"><span data-stu-id="bcdaf-128">Additional resources</span></span>

- [<span data-ttu-id="bcdaf-129">电子报告 (ER) 概览</span><span class="sxs-lookup"><span data-stu-id="bcdaf-129">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="bcdaf-130">电子报告 (ER) 目标</span><span class="sxs-lookup"><span data-stu-id="bcdaf-130">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
