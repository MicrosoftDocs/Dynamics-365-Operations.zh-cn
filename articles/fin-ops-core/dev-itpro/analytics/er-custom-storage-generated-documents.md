---
title: 为生成的单据指定自定义存储位置
description: 本主题介绍如何扩展电子申报 (ER) 格式生成的单据的存储位置列表。
author: NickSelin
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: dab70b213efc7e7a3537aa2b47b9edf38d492d34
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753712"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a><span data-ttu-id="2637f-103">为生成的单据指定自定义存储位置</span><span class="sxs-lookup"><span data-stu-id="2637f-103">Specify a custom storage location for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2637f-104">电子申报 (ER) 框架的应用程序编程接口 (API) 可用于扩展 ER 格式生成的单据的存储位置列表。</span><span class="sxs-lookup"><span data-stu-id="2637f-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="2637f-105">本主题中包含有关必须完成才能添加自定义存储位置的主要任务的概述。</span><span class="sxs-lookup"><span data-stu-id="2637f-105">This topic includes an overview of the main tasks that you must complete to add a custom storage location.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2637f-106">先决条件</span><span class="sxs-lookup"><span data-stu-id="2637f-106">Prerequisites</span></span>

<span data-ttu-id="2637f-107">必须部署支持连续生成的拓扑。</span><span class="sxs-lookup"><span data-stu-id="2637f-107">You must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="2637f-108">（有关详细信息，请参阅[部署支持连续生成和测试自动化的拓扑](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation)。）必须可以访问以下角色之一的此拓扑：</span><span class="sxs-lookup"><span data-stu-id="2637f-108">(For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="2637f-109">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="2637f-109">Electronic reporting developer</span></span>
- <span data-ttu-id="2637f-110">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="2637f-110">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="2637f-111">系统管理员</span><span class="sxs-lookup"><span data-stu-id="2637f-111">System administrator</span></span>

<span data-ttu-id="2637f-112">还必须可以访问此拓扑的开发环境。</span><span class="sxs-lookup"><span data-stu-id="2637f-112">You must also have access to the development environment for this topology.</span></span>

## <a name="create-or-import-an-er-format-configuration"></a><span data-ttu-id="2637f-113">创建或导入 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="2637f-113">Create or import an ER format configuration</span></span>

<span data-ttu-id="2637f-114">在当前拓扑中，[创建新的 ER 格式](tasks/er-format-configuration-2016-11.md)以生成计划添加的自定义存储位置所属单据。</span><span class="sxs-lookup"><span data-stu-id="2637f-114">In the current topology, [create a new ER format](tasks/er-format-configuration-2016-11.md) to generate documents that you plan to add a custom storage location for.</span></span> <span data-ttu-id="2637f-115">也可以[在此拓扑中导入现有 ER 格式](general-electronic-reporting-manage-configuration-lifecycle.md)。</span><span class="sxs-lookup"><span data-stu-id="2637f-115">Alternatively, [import an existing ER format into this topology](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![“格式设计器”页面](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> <span data-ttu-id="2637f-117">创建或导入的 ER 格式中必须包含至少一个下面的格式元素：</span><span class="sxs-lookup"><span data-stu-id="2637f-117">The ER format that you create or import must contain at least one of the following format elements:</span></span>
>
> - <span data-ttu-id="2637f-118">文件</span><span class="sxs-lookup"><span data-stu-id="2637f-118">File</span></span>
> - <span data-ttu-id="2637f-119">文件夹</span><span class="sxs-lookup"><span data-stu-id="2637f-119">Folder</span></span>
> - <span data-ttu-id="2637f-120">合并器</span><span class="sxs-lookup"><span data-stu-id="2637f-120">Merger</span></span>
> - <span data-ttu-id="2637f-121">附件</span><span class="sxs-lookup"><span data-stu-id="2637f-121">Attachment</span></span>

## <a name="create-a-new-document-type"></a><span data-ttu-id="2637f-122">创建新的单据类型</span><span class="sxs-lookup"><span data-stu-id="2637f-122">Create a new document type</span></span>

<span data-ttu-id="2637f-123">若要指定如何路由 ER 格式生成的单据，必须配置[电子申报 (ER) 目标](electronic-reporting-destinations.md)。</span><span class="sxs-lookup"><span data-stu-id="2637f-123">To specify how documents that an ER format generates are routed, you must configure [Electronic reporting (ER) destinations](electronic-reporting-destinations.md).</span></span> <span data-ttu-id="2637f-124">在配置为将生成的单据作为文件存储的每个 ER 目标中，必须指定单据管理框架的单据类型。</span><span class="sxs-lookup"><span data-stu-id="2637f-124">In each ER destination that is configured to store generated documents as files, you must specify a document type of the Document management framework.</span></span> <span data-ttu-id="2637f-125">可使用不同单据类型路由不同 ER 格式生成的单据。</span><span class="sxs-lookup"><span data-stu-id="2637f-125">Different document types can be used to route documents that different ER formats generate.</span></span>

1. <span data-ttu-id="2637f-126">为之前创建或导入的 ER 格式添加新的[单据类型](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management)。</span><span class="sxs-lookup"><span data-stu-id="2637f-126">Add a new [document type](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) for the ER format that you created or imported earlier.</span></span> <span data-ttu-id="2637f-127">在下图中，单据类型为 **FileX**。</span><span class="sxs-lookup"><span data-stu-id="2637f-127">In the illustration that follows, the document type is **FileX**.</span></span>
2. <span data-ttu-id="2637f-128">若要区分此单据类型和其他单据类型，请在其名称中包含特定关键词。</span><span class="sxs-lookup"><span data-stu-id="2637f-128">To differentiate this document type from other document types, include a specific keyword in its name.</span></span> <span data-ttu-id="2637f-129">例如，在下图中，名称为 **(LOCAL) 文件夹**。</span><span class="sxs-lookup"><span data-stu-id="2637f-129">For example, in the illustration that follows, the name is **(LOCAL) folder**.</span></span>
3. <span data-ttu-id="2637f-130">在 **类** 字段中，指定 **附加文件**。</span><span class="sxs-lookup"><span data-stu-id="2637f-130">In the **Class** field, specify **Attach file**.</span></span>
4. <span data-ttu-id="2637f-131">在 **组** 字段中，指定 **文件**。</span><span class="sxs-lookup"><span data-stu-id="2637f-131">In the **Group** field, specify **File**.</span></span>

![“单据类型”页面](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> <span data-ttu-id="2637f-133">单据类型特定于公司。</span><span class="sxs-lookup"><span data-stu-id="2637f-133">Document types are company-specific.</span></span> <span data-ttu-id="2637f-134">若要在多个公司中使用某个 ER 格式和配置的目标，必须在每个公司中配置一个单独的单据类型。</span><span class="sxs-lookup"><span data-stu-id="2637f-134">To use an ER format with a configured destination in multiple companies, you must configure a separate document type in each company.</span></span>

## <a name="review-source-code"></a><span data-ttu-id="2637f-135">查看源代码</span><span class="sxs-lookup"><span data-stu-id="2637f-135">Review source code</span></span>

<span data-ttu-id="2637f-136">可查看 **ERDocuManagement** 类的 **insertFile()** 方法的代码。</span><span class="sxs-lookup"><span data-stu-id="2637f-136">Review the code of the **insertFile()** method of the **ERDocuManagement** class.</span></span> <span data-ttu-id="2637f-137">请注意，如果将生成的文件附加到记录，将引发 **AttachingFile()** 事件。</span><span class="sxs-lookup"><span data-stu-id="2637f-137">Notice that the **AttachingFile()** event is raised while the generated file is attached to a record.</span></span>


```xpp
/// <summary>
/// Inserts file as attachment in Document Management.
/// </summary>
/// <param name = "_owner">A record as the attachment owner.</param>
/// <param name = "_stream">The file stream.</param>
/// <param name = "_filePath">The file path with name.</param>
/// <param name = "_attachmentName">The name of file attachment.</param>
/// <returns>The reference to inserted file.</returns>
[Hookable(false)]
public DocuRef insertFile(
    Common _owner, 
    System.IO.Stream _stream, 
    str _filePath, 
    str _attachmentName, 
    DocuTypeId _docuTypeId)
{
    DocuRef docuRef;
    if (_stream)
    {
        DocuType::createDefaults();
        if (!this.isDocuTypeValid(_docuTypeId))
        {
            throw error(strFmt("@ElectronicReporting:DocuTypeIsNotValid", _docuTypeId));
        }
        var args = ERDocuManagementAttachingFileEventArgs::construct(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        ERDocuManagementEvents::onAttachingFile(args);
        if (args.isHandled())
        {
            docuRef = args.getDocuRef();
        }
        else
        {
            docuRef = this.attachFile(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        }
    }
    return docuRef;
}
```

<span data-ttu-id="2637f-138">如果处理以下 ER 目标，将引发 **AttachingFile()** 事件。</span><span class="sxs-lookup"><span data-stu-id="2637f-138">The **AttachingFile()** event is raised when the following ER destinations are processed:</span></span>

- <span data-ttu-id="2637f-139">**存档** – 如果使用此目标，将在 ERFormatMappingRunJobTable 表中为运行的 ER 格式创建一个新记录。</span><span class="sxs-lookup"><span data-stu-id="2637f-139">**Archive** – When this destination is used, a new record for the ER format that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="2637f-140">此记录的 **已存档** 字段设置为 **False**。</span><span class="sxs-lookup"><span data-stu-id="2637f-140">The **Archived** field in this record is set to **False**.</span></span> <span data-ttu-id="2637f-141">如果 ER 格式运行成功，将把生成的单据附加到此记录，并引发 **AttachingFile()** 事件。</span><span class="sxs-lookup"><span data-stu-id="2637f-141">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="2637f-142">此 ER 目标中选择的单据类型决定附加的文件的存储位置（Microsoft Azure 存储或 Microsoft SharePoint 文件夹）。</span><span class="sxs-lookup"><span data-stu-id="2637f-142">The document type that is selected in this ER destination determines the storage location for the attached file (Microsoft Azure Storage or a Microsoft SharePoint folder).</span></span>
- <span data-ttu-id="2637f-143">**作业存档** – 如果使用此目标，将在 ERFormatMappingRunJobTable 表中为运行的 ER 窗体创建一个新记录。</span><span class="sxs-lookup"><span data-stu-id="2637f-143">**Job archive** – When this destination is used, a new record for the ER form that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="2637f-144">此记录的 **已存档** 字段设置为 **True**。</span><span class="sxs-lookup"><span data-stu-id="2637f-144">The **Archived** field in this record is set to **True**.</span></span> <span data-ttu-id="2637f-145">如果 ER 格式运行成功，将把生成的单据附加到此记录，并引发 **AttachingFile()** 事件。</span><span class="sxs-lookup"><span data-stu-id="2637f-145">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="2637f-146">此 ER 参数中配置的单据类型决定附加的文件的存储位置（Azure 存储或 Microsoft SharePoint 文件夹）。</span><span class="sxs-lookup"><span data-stu-id="2637f-146">The document type that is configured in the ER parameters determines the storage location for the attached file (Azure Storage or a SharePoint folder).</span></span>

![“电子申报参数”页面](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a><span data-ttu-id="2637f-148">配置 ER 目标</span><span class="sxs-lookup"><span data-stu-id="2637f-148">Configure an ER destination</span></span>

1. <span data-ttu-id="2637f-149">为创建或导入的 ER 格式的之前介绍的一个元素（文件、文件夹、合并器或附件）配置存档目标。</span><span class="sxs-lookup"><span data-stu-id="2637f-149">Configure the archived destination for one of the previously mentioned elements (file, folder, merger, or attachment) of the ER format that you created or imported.</span></span> <span data-ttu-id="2637f-150">有关指南，请参阅 [ER 配置目标](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11)。</span><span class="sxs-lookup"><span data-stu-id="2637f-150">For guidance, see [ER Configure destinations](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span></span>
2. <span data-ttu-id="2637f-151">请使用前面为配置的目标添加的单据类型。</span><span class="sxs-lookup"><span data-stu-id="2637f-151">Use the document type that you added earlier for the configured destination.</span></span> <span data-ttu-id="2637f-152">（例如，在本主题中，单据类型为 **FileX**。）</span><span class="sxs-lookup"><span data-stu-id="2637f-152">(For the example in this topic, the document type is **FileX**.)</span></span>

![“目标设置”对话框](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a><span data-ttu-id="2637f-154">修改源代码</span><span class="sxs-lookup"><span data-stu-id="2637f-154">Modify source code</span></span>

1. <span data-ttu-id="2637f-155">可向 Microsoft Visual Studio 项目添加新类，并编写代码以订阅前面介绍的 **AttachingFile()** 事件。</span><span class="sxs-lookup"><span data-stu-id="2637f-155">Add a new class to your Microsoft Visual Studio project, and write code to subscribe to the **AttachingFile()** event that was mentioned earlier.</span></span> <span data-ttu-id="2637f-156">（有关所用可扩展性模式的详细信息，请参阅[使用 EventHandlerResult 响应](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result)。）例如，编写用于执行以下操作的代码：</span><span class="sxs-lookup"><span data-stu-id="2637f-156">(For more information about the extensibility pattern that is used, see [Respond by using EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) For example, in the new class, write code that performs the following actions:</span></span>

    1. <span data-ttu-id="2637f-157">将生成的文件存储到运行应用程序对象服务器 (AOS) 服务的服务器的本地系统的文件夹中。</span><span class="sxs-lookup"><span data-stu-id="2637f-157">Store generated files in a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    2. <span data-ttu-id="2637f-158">仅当在将文件附加到 ER 执行作业日志中的记录时使用新的单据类型（例如，名称中包含“(LOCAL)”关键字的 **FileX** 类型），才存储这些生成的文件。</span><span class="sxs-lookup"><span data-stu-id="2637f-158">Store these generated files only when the new document type (for example, the **FileX** type that has the "(LOCAL)" keyword in its name) is used while a file is attached to the record in the ER execution job log.</span></span>

    ```xpp
    class ERDocuSubscriptionSample
    {
        void new()
        {
        }
        [SubscribesTo(classStr(ERDocuManagementEvents), 
        staticDelegateStr(ERDocuManagementEvents, 
        attachingFile))]
        public static void ERDocuManagementEvents_attachingFile(ERDocuManagementAttachingFileEventArgs _args)
        {
            if (!_args.isHandled())
            {
                DocuType docuType = DocuType::find(_args.getDocuTypeId());
                if (strContains(docuType.Name, '(LOCAL)'))
                {
                    _args.markAsHandled();
                    var stream = _args.getStream();
                    if (stream.CanSeek)
                    {
                        stream.Seek(0, System.IO.SeekOrigin::Begin);
                    }
                    using (var localStream = System.IO.File::OpenWrite(@'c:\0\' + _args.getAttachmentName()))
                    {
                        stream.CopyTo(localStream);
                    }
                }
            }
        }
    }
    ```

2. <span data-ttu-id="2637f-159">重新生成您的项目。</span><span class="sxs-lookup"><span data-stu-id="2637f-159">Rebuild your project.</span></span>

## <a name="run-the-er-format-that-you-created-or-imported"></a><span data-ttu-id="2637f-160">运行创建或导入的 ER 格式</span><span class="sxs-lookup"><span data-stu-id="2637f-160">Run the ER format that you created or imported</span></span>

1. <span data-ttu-id="2637f-161">执行创建或导入的 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="2637f-161">Execute the ER format that you created or imported.</span></span>
2. <span data-ttu-id="2637f-162">转到 **组织管理 \> 电子报表 \> 电子报表作业**。</span><span class="sxs-lookup"><span data-stu-id="2637f-162">Go to **Organization administration \> Electronic reporting \> Electronic reporting jobs**.</span></span> <span data-ttu-id="2637f-163">找到为此执行作业创建且生成的文件附加到的记录。</span><span class="sxs-lookup"><span data-stu-id="2637f-163">Find the record that was created for this execution job, and that has the generated file attached to it.</span></span>
3. <span data-ttu-id="2637f-164">浏览本地 **C:\\0** 文件夹以查找同一个生成的文件。</span><span class="sxs-lookup"><span data-stu-id="2637f-164">Explore the local **C:\\0** folder to find same generated file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2637f-165">其他资源</span><span class="sxs-lookup"><span data-stu-id="2637f-165">Additional resources</span></span>

- [<span data-ttu-id="2637f-166">电子申报 (ER) 目标</span><span class="sxs-lookup"><span data-stu-id="2637f-166">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="2637f-167">可扩展性主页</span><span class="sxs-lookup"><span data-stu-id="2637f-167">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]