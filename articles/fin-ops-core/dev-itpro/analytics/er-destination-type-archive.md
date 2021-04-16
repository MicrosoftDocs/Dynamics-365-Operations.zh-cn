---
title: 存档 ER 目标类型
description: 本主题提供有关如何为电子报告 (ER) 格式的每个文件夹或文件组件配置存档目标的信息。
author: NickSelin
ms.date: 11/30/2020
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
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 18c662fee0cedaa55f63ffeb25b0d61ee7baffda
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753520"
---
# <a name="archive-er-destination-type"></a><span data-ttu-id="ce448-103">存档 ER 目标类型</span><span class="sxs-lookup"><span data-stu-id="ce448-103">Archive ER destination type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce448-104">您可以为配置为生成出站文档的电子报告 (ER) 格式的每个 **文件夹** 或 **文件** 组件配置存档目标。</span><span class="sxs-lookup"><span data-stu-id="ce448-104">You can configure an archive destination for each **Folder** or **File** component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="ce448-105">根据目标设置，将生成的文档存储为 ER 作业列表的记录附件。</span><span class="sxs-lookup"><span data-stu-id="ce448-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span> <span data-ttu-id="ce448-106">若要查看结果，请转到 **组织管理** \> **电子申报** \> **电子申报作业**。</span><span class="sxs-lookup"><span data-stu-id="ce448-106">To view the results, go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting jobs**.</span></span>

<span data-ttu-id="ce448-107">您可以使用此选项将生成的文档发送到 Microsoft SharePoint 文件夹或 Microsoft Azure Storage。</span><span class="sxs-lookup"><span data-stu-id="ce448-107">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="ce448-108">将 **已启用** 设置为 **是** 以将输出发送到由所选文档类型定义的目标。</span><span class="sxs-lookup"><span data-stu-id="ce448-108">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="ce448-109">仅组设置为 **文件** 的文档类型可供选择。</span><span class="sxs-lookup"><span data-stu-id="ce448-109">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="ce448-110">您在 **组织管理** \> **文档管理** \> **文档类型** 中定义文档[类型](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types)。</span><span class="sxs-lookup"><span data-stu-id="ce448-110">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="ce448-111">ER 目标的配置与文档管理系统的配置相同。</span><span class="sxs-lookup"><span data-stu-id="ce448-111">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="ce448-112">[![文档类型页面](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="ce448-112">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="ce448-113">位置确定文件保存的位置。</span><span class="sxs-lookup"><span data-stu-id="ce448-113">The location determines where the file is saved.</span></span> <span data-ttu-id="ce448-114">启用 **存档** 目标之后，可将结果保存到作业存档中。</span><span class="sxs-lookup"><span data-stu-id="ce448-114">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="ce448-115">可以在 **组织管理** \> **电子申报** \> **电子申报存档作业** 中查看结果。</span><span class="sxs-lookup"><span data-stu-id="ce448-115">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="ce448-116">通过导航到 **组织管理** \> **工作区** \> **电子报告** \> **电子报告参数**，为作业存档选择票据类型。</span><span class="sxs-lookup"><span data-stu-id="ce448-116">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="ce448-117">有关详细信息，请参阅[配置电子报告 (ER) 框架](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup)。</span><span class="sxs-lookup"><span data-stu-id="ce448-117">For more information, see [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="ce448-118">SharePoint</span><span class="sxs-lookup"><span data-stu-id="ce448-118">SharePoint</span></span>

<span data-ttu-id="ce448-119">您可以在指定的 SharePoint 文件夹中保存文件。</span><span class="sxs-lookup"><span data-stu-id="ce448-119">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="ce448-120">要定义默认的 SharePoint 服务器，请转到 **组织管理** \> **文档管理** \> **文档管理参数**。</span><span class="sxs-lookup"><span data-stu-id="ce448-120">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="ce448-121">在 **SharePoint** 选项卡上，配置 SharePoint 件夹。</span><span class="sxs-lookup"><span data-stu-id="ce448-121">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="ce448-122">然后，您可以选择它作为保存 ER 输出的文件夹。</span><span class="sxs-lookup"><span data-stu-id="ce448-122">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="ce448-123">必须在此文档类型中选择 **SharePoint** 位置。</span><span class="sxs-lookup"><span data-stu-id="ce448-123">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="ce448-124">[![选择 SharePoint 文件夹](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="ce448-124">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="ce448-125">Azure 储存</span><span class="sxs-lookup"><span data-stu-id="ce448-125">Azure Storage</span></span>

<span data-ttu-id="ce448-126">将文档类型位置设置为 **Azure 存储** 时，您可以将文件保存到 Azure 存储中。</span><span class="sxs-lookup"><span data-stu-id="ce448-126">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

> [!NOTE] 
> <span data-ttu-id="ce448-127">ER 框架将文件永久存储在 Azure Blob 存储中，这与数据管理框架不同，后者对必须处理的文档实施 7 天保留策略。</span><span class="sxs-lookup"><span data-stu-id="ce448-127">The ER framework permanently stores files in Azure Blob storage unlike the Data management framework that applies the seven-day retention policy for documents that must be processed.</span></span> <span data-ttu-id="ce448-128">有关详细信息，请参阅[用于获取消息状态的 API](../data-entities/recurring-integrations.md#api-for-getting-message-status) 和 [状态检查 API](../data-entities/data-management-api.md#status-check-api)。</span><span class="sxs-lookup"><span data-stu-id="ce448-128">For more information, see [API for getting message status](../data-entities/recurring-integrations.md#api-for-getting-message-status) and [Status check API](../data-entities/data-management-api.md#status-check-api).</span></span> <span data-ttu-id="ce448-129">只要必须，与 ER 相关的文件都将作为应用程序表记录的附件存储在 Azure Blob 存储中。</span><span class="sxs-lookup"><span data-stu-id="ce448-129">The ER-related files will be stored in Azure Blob storage as attachments of application table records as long as necessary.</span></span> <span data-ttu-id="ce448-130">单个文件将与该文件附加到的应用程序表记录一起从 Azure Blob 存储中删除。</span><span class="sxs-lookup"><span data-stu-id="ce448-130">A single file will be deleted from Azure Blob storage along with the application table record that this file was attached to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ce448-131">其他资源</span><span class="sxs-lookup"><span data-stu-id="ce448-131">Additional resources</span></span>

- [<span data-ttu-id="ce448-132">电子报告 (ER) 概览</span><span class="sxs-lookup"><span data-stu-id="ce448-132">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="ce448-133">电子报告 (ER) 目标</span><span class="sxs-lookup"><span data-stu-id="ce448-133">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="ce448-134">配置文档管理</span><span class="sxs-lookup"><span data-stu-id="ce448-134">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]