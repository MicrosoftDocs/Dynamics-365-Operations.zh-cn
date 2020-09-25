---
title: 存档 ER 目标类型
description: 本主题提供相关信息，介绍如何为配置为生成出站文档的电子报告 (ER) 格式的每个文件夹或文件组件配置存档目标。
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
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
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8797a68507a5116c6adbf1f2d805838fa507958c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745577"
---
# <a name="archive-destination"></a><span data-ttu-id="3d7c6-103">归档目标</span><span class="sxs-lookup"><span data-stu-id="3d7c6-103">Archive destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d7c6-104">您可以为配置为生成出站文档的电子报告 (ER) 格式的每个文件夹或文件组件配置存档目标。</span><span class="sxs-lookup"><span data-stu-id="3d7c6-104">You can configure an archive destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="3d7c6-105">根据目标设置，将生成的文档存储为 ER 作业列表的记录附件。</span><span class="sxs-lookup"><span data-stu-id="3d7c6-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span>

<span data-ttu-id="3d7c6-106">您可以使用此选项将生成的文档发送到 Microsoft SharePoint 文件夹或 Microsoft Azure Storage。</span><span class="sxs-lookup"><span data-stu-id="3d7c6-106">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="3d7c6-107">将**已启用**设置为**是**以将输出发送到由所选文档类型定义的目标。</span><span class="sxs-lookup"><span data-stu-id="3d7c6-107">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="3d7c6-108">仅组设置为**文件**的文档类型可供选择。</span><span class="sxs-lookup"><span data-stu-id="3d7c6-108">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="3d7c6-109">您在**组织管理** \> **文档管理** \> **文档类型**中定义文档[类型](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types)。</span><span class="sxs-lookup"><span data-stu-id="3d7c6-109">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="3d7c6-110">ER 目标的配置与文档管理系统的配置相同。</span><span class="sxs-lookup"><span data-stu-id="3d7c6-110">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="3d7c6-111">[![文档类型页面](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="3d7c6-111">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="3d7c6-112">位置确定文件保存的位置。</span><span class="sxs-lookup"><span data-stu-id="3d7c6-112">The location determines where the file is saved.</span></span> <span data-ttu-id="3d7c6-113">启用**存档**目标之后，可将结果保存到作业存档中。</span><span class="sxs-lookup"><span data-stu-id="3d7c6-113">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="3d7c6-114">可以在**组织管理** \> **电子申报** \> **电子申报存档作业**中查看结果。</span><span class="sxs-lookup"><span data-stu-id="3d7c6-114">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="3d7c6-115">通过导航到**组织管理** \> **工作区** \> **电子报告** \> **电子报告参数**，为作业存档选择票据类型。</span><span class="sxs-lookup"><span data-stu-id="3d7c6-115">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="3d7c6-116">有关详细信息，请参阅[配置电子报告 (ER) 框架](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup)。</span><span class="sxs-lookup"><span data-stu-id="3d7c6-116">For more information, [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="3d7c6-117">SharePoint</span><span class="sxs-lookup"><span data-stu-id="3d7c6-117">SharePoint</span></span>

<span data-ttu-id="3d7c6-118">您可以在指定的 SharePoint 文件夹中保存文件。</span><span class="sxs-lookup"><span data-stu-id="3d7c6-118">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="3d7c6-119">要定义默认的 SharePoint 服务器，请转到**组织管理** \> **文档管理** \> **文档管理参数**。</span><span class="sxs-lookup"><span data-stu-id="3d7c6-119">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="3d7c6-120">在 **SharePoint** 选项卡上，配置 SharePoint 件夹。</span><span class="sxs-lookup"><span data-stu-id="3d7c6-120">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="3d7c6-121">然后，您可以选择它作为保存 ER 输出的文件夹。</span><span class="sxs-lookup"><span data-stu-id="3d7c6-121">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="3d7c6-122">必须在此文档类型中选择 **SharePoint** 位置。</span><span class="sxs-lookup"><span data-stu-id="3d7c6-122">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="3d7c6-123">[![选择 SharePoint 文件夹](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="3d7c6-123">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="3d7c6-124">Azure 储存</span><span class="sxs-lookup"><span data-stu-id="3d7c6-124">Azure Storage</span></span>

<span data-ttu-id="3d7c6-125">将文档类型位置设置为 **Azure 存储**时，您可以将文件保存到 Azure 存储中。</span><span class="sxs-lookup"><span data-stu-id="3d7c6-125">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3d7c6-126">其他资源</span><span class="sxs-lookup"><span data-stu-id="3d7c6-126">Additional resources</span></span>

- [<span data-ttu-id="3d7c6-127">电子报告 (ER) 概览</span><span class="sxs-lookup"><span data-stu-id="3d7c6-127">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="3d7c6-128">电子报告 (ER) 目标</span><span class="sxs-lookup"><span data-stu-id="3d7c6-128">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="3d7c6-129">配置文档管理</span><span class="sxs-lookup"><span data-stu-id="3d7c6-129">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)
