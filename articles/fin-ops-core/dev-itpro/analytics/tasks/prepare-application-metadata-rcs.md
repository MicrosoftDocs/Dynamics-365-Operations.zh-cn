---
title: 准备要在 RCS 中使用的应用程序元数据
description: 本主题介绍如何创建包含应用程序元数据的新报告配置。
author: NickSelin
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5fe475bd0fceea7e1e8edf7c375d34a4be6d92a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751026"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a><span data-ttu-id="99782-103">准备要在 RCS 中使用的应用程序元数据</span><span class="sxs-lookup"><span data-stu-id="99782-103">Prepare application metadata to be used in RCS</span></span>
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="99782-104">以下步骤演示系统管理员或电子申报开发人员角色的用户如何创建其中包含应用程序元数据的新电子申报 (ER) 配置文件，以便在 Regulatory Configuration Service (RCS) 中设计 ER 模型映射配置。</span><span class="sxs-lookup"><span data-stu-id="99782-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains application metadata for designing ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="99782-105">此配置将用于设计示例 ER 模型映射配置，以便访问外贸交易。</span><span class="sxs-lookup"><span data-stu-id="99782-105">This configuration will be used for designing a sample ER model mapping configuration to access foreign trade transactions.</span></span> <span data-ttu-id="99782-106">在此示例中，您将创建示例公司 Litware 公司的配置。这些步骤可以在任何公司执行。</span><span class="sxs-lookup"><span data-stu-id="99782-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company.</span></span> <span data-ttu-id="99782-107">为了完成这些步骤，您必须首先完成[创建配置提供程序并标记为当前运行的](er-configuration-provider-mark-it-active-2016-11.md)主题中的步骤。</span><span class="sxs-lookup"><span data-stu-id="99782-107">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="99782-108">先决条件</span><span class="sxs-lookup"><span data-stu-id="99782-108">Prerequisites</span></span>
1.    <span data-ttu-id="99782-109">转到 **组织管理** > **工作区** > **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="99782-109">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2.    <span data-ttu-id="99782-110">确保示例公司 Litware 公司的配置提供程序可用且标记为 **有效**。</span><span class="sxs-lookup"><span data-stu-id="99782-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="99782-111">如果没有看到此配置提供程序，请首先完成[创建配置提供程序并标记为当前运行的](er-configuration-provider-mark-it-active-2016-11.md)这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="99782-111">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3.    <span data-ttu-id="99782-112">单击 **元数据配置**。</span><span class="sxs-lookup"><span data-stu-id="99782-112">Click **Metadata configurations**.</span></span> 
4.    <span data-ttu-id="99782-113">假设将使用 RCS 为 Finance and Operations 应用程序设计 ER 解决方案，用于生成其中包含来自外贸业务域的信息的电子单据。</span><span class="sxs-lookup"><span data-stu-id="99782-113">Assume that RCS will be used to design an ER solution for a Finance and Operation application that will generate electronic documents that contain information from foreign trade business domain.</span></span> <span data-ttu-id="99782-114">若要 ER 数据模型与所需数据源之间的映射，需要在 RCS 中访问 Finance and Operations 应用程序的元数据。</span><span class="sxs-lookup"><span data-stu-id="99782-114">To specify the mapping between ER data model and sources of required data, in RCS we need to have access to metadata of the Finance and Operation application.</span></span> <span data-ttu-id="99782-115">因此，在 ER 解决方案的设计过程中，将新建一个 ER 元数据配置，其中包含为所选业务域生成 ER 报表当前所需全部元数据。</span><span class="sxs-lookup"><span data-stu-id="99782-115">Therefore, as part of designing ER solution we configure a new ER metadata configuration containing all metadata that is currently required for generation ER reports for selected business domain.</span></span> 

## <a name="add-metadata-configuration"></a><span data-ttu-id="99782-116">添加元数据配置</span><span class="sxs-lookup"><span data-stu-id="99782-116">Add metadata configuration</span></span> 
1.    <span data-ttu-id="99782-117">单击 **创建配置**，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="99782-117">Click **Create configuration** to open the drop dialog.</span></span> 
2.    <span data-ttu-id="99782-118">在 **名称** 字段中键入“外贸元数据”。</span><span class="sxs-lookup"><span data-stu-id="99782-118">In the **Name** field, type 'Foreign trade metadata'.</span></span> 
3.    <span data-ttu-id="99782-119">单击 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="99782-119">Click **Create configuration**.</span></span> 
4.    <span data-ttu-id="99782-120">单击 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="99782-120">Click **Designer**.</span></span> 
5.    <span data-ttu-id="99782-121">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="99782-121">Click **Add**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="99782-122">可选择整个应用程序、所选模型或所选模块的所有元数据。</span><span class="sxs-lookup"><span data-stu-id="99782-122">You can select all metadata for the entire application or selected models or selected modules.</span></span> <span data-ttu-id="99782-123">请注意，在此情况下将自动添加以下元数据：记录表、枚举和扩展数据类型。</span><span class="sxs-lookup"><span data-stu-id="99782-123">Be aware that in this case the following metadata will be automatically added: tables of records, enumerations, and extended data types.</span></span> <span data-ttu-id="99782-124">如果需要更多元数据类型，则必须手动添加。</span><span class="sxs-lookup"><span data-stu-id="99782-124">When additional types of metadata are needed, they must be added manually.</span></span> 
 
<span data-ttu-id="99782-125">我们已通过手动选择元数据项获得了一些与外贸交易有关的元数据。</span><span class="sxs-lookup"><span data-stu-id="99782-125">We have some foreign trade transactions related metadata by selecting metadata items manually.</span></span> 
  
6.    <span data-ttu-id="99782-126">单击 **添加数据源**。</span><span class="sxs-lookup"><span data-stu-id="99782-126">Click **Add data source**.</span></span> 
7.    <span data-ttu-id="99782-127">单击 **表记录**。</span><span class="sxs-lookup"><span data-stu-id="99782-127">Click **Table records**.</span></span> 
8.    <span data-ttu-id="99782-128">使用“快速筛选器”以筛选一个值为“内部统计”的 **名称** 字段。</span><span class="sxs-lookup"><span data-stu-id="99782-128">Use the Quick Filter to filter on the **Name** field with a value of 'Intrastat'.</span></span> 
9.    <span data-ttu-id="99782-129">选择 **内部统计** 表记录。</span><span class="sxs-lookup"><span data-stu-id="99782-129">Select the **Intrastat** table record.</span></span> 
10.    <span data-ttu-id="99782-130">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="99782-130">Click **OK**.</span></span>
  
<span data-ttu-id="99782-131">已添加了有关“内部统计”记录表的元数据信息。</span><span class="sxs-lookup"><span data-stu-id="99782-131">We added metadata information about the Intrastat table of records.</span></span> 
  
11.    <span data-ttu-id="99782-132">在树中，展开 **表记录内部统计**\>**关系**。</span><span class="sxs-lookup"><span data-stu-id="99782-132">In the tree, expand **Table records Intrastat**\>**Relations**.</span></span> 
12.    <span data-ttu-id="99782-133">在树中，选择 **表记录内部统计**\>**关系\IntrastatCommodity (表记录 EcoResCategory)**。</span><span class="sxs-lookup"><span data-stu-id="99782-133">In the tree, select **Table records Intrastat**\>**Relations\IntrastatCommodity (Table records EcoResCategory)**.</span></span>     
13.    <span data-ttu-id="99782-134">单击 **添加元数据**。</span><span class="sxs-lookup"><span data-stu-id="99782-134">Click **Add metadata**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="99782-135">必须手动添加有关所选记录表的所需关系的元数据。</span><span class="sxs-lookup"><span data-stu-id="99782-135">Metadata about required relations for selected table of records must be added manually.</span></span> 
  
16.    <span data-ttu-id="99782-136">单击 **添加数据源**。</span><span class="sxs-lookup"><span data-stu-id="99782-136">Click **Add data source**.</span></span> 
17.    <span data-ttu-id="99782-137">单击 **枚举**。</span><span class="sxs-lookup"><span data-stu-id="99782-137">Click **Enumeration**.</span></span> 
18.    <span data-ttu-id="99782-138">使用“快速筛选器”以筛选一个值为“IntrastatDirection”的 **名称** 字段。</span><span class="sxs-lookup"><span data-stu-id="99782-138">Use the Quick Filter to filter on the **Name** field with a value of 'IntrastatDirection'.</span></span> 
19.    <span data-ttu-id="99782-139">选择 **IntrastatDirection 枚举** 记录。</span><span class="sxs-lookup"><span data-stu-id="99782-139">Select the **IntrastatDirection enumeration** record.</span></span> 
20.    <span data-ttu-id="99782-140">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="99782-140">Click **OK**.</span></span> 
21.    <span data-ttu-id="99782-141">单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="99782-141">Click **Save**.</span></span>  
22.    <span data-ttu-id="99782-142">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="99782-142">Close the page.</span></span> 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a><span data-ttu-id="99782-143">完成元数据配置的草稿版本</span><span class="sxs-lookup"><span data-stu-id="99782-143">Complete the draft version of metadata configuration</span></span>
1.    <span data-ttu-id="99782-144">单击 **更改状态**。</span><span class="sxs-lookup"><span data-stu-id="99782-144">Click **Change status**.</span></span> 
2.    <span data-ttu-id="99782-145">单击 **完成**。</span><span class="sxs-lookup"><span data-stu-id="99782-145">Click **Complete**.</span></span> 
3.    <span data-ttu-id="99782-146">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="99782-146">Click **OK**.</span></span> 
4.    <span data-ttu-id="99782-147">选择已完成版本 **1**。</span><span class="sxs-lookup"><span data-stu-id="99782-147">Select the completed version **1**.</span></span> 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a><span data-ttu-id="99782-148">将元数据配置的已完成版本作为 XML 文件从应用程序导出</span><span class="sxs-lookup"><span data-stu-id="99782-148">Export the completed version of metadata configuration from application as XML file</span></span>
1.    <span data-ttu-id="99782-149">单击 **交换**。</span><span class="sxs-lookup"><span data-stu-id="99782-149">Click **Exchange**.</span></span> 
2.    <span data-ttu-id="99782-150">单击 **导出为 XML 文件**。</span><span class="sxs-lookup"><span data-stu-id="99782-150">Click **Export as XML file**.</span></span> 
3.    <span data-ttu-id="99782-151">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="99782-151">Click **OK**.</span></span> 
    
<span data-ttu-id="99782-152">已将创建的 ER 元数据配置保存为 XML 文件，可将此文件导入到 RCS，并用作有关外贸业务域的元数据的信息的来源。</span><span class="sxs-lookup"><span data-stu-id="99782-152">The created ER metadata configuration has been saved as XML file that can be imported to RCS and used as the source of information about metadata for the foreign trade business domain.</span></span> <span data-ttu-id="99782-153">可根据此信息指定应用程序元数据与 ER 数据模型之间的映射。</span><span class="sxs-lookup"><span data-stu-id="99782-153">Based on this information, we can specify the mapping between application metadata and ER data model.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]