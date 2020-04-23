---
title: 资产文档
description: 本主题介绍资产管理中的资产文档。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f994e519e354a766a2437f182d2ade39155749b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216543"
---
# <a name="asset-documents"></a><span data-ttu-id="e0760-103">资产文档</span><span class="sxs-lookup"><span data-stu-id="e0760-103">Asset documents</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e0760-104">本主题介绍资产管理中的资产文档。</span><span class="sxs-lookup"><span data-stu-id="e0760-104">This topic explains asset documents in Asset Management.</span></span>

<span data-ttu-id="e0760-105">在资产管理中，可设置文档，以便将其与作业类型、资产制造商、资产类型或资产之类自动关联。</span><span class="sxs-lookup"><span data-stu-id="e0760-105">In Asset Management, you can set up documents so that they are automatically related to job types, asset manufacturers, asset types, or assets, for example.</span></span> <span data-ttu-id="e0760-106">此功能在发布了更新后的文档版本时非常有用。</span><span class="sxs-lookup"><span data-stu-id="e0760-106">This functionality is useful when updated document versions are released.</span></span> <span data-ttu-id="e0760-107">在此情况下，只需将更新后的文档放到您的 Supply Chain Management 文档所用标准位置，然后将该文档附加到您已创建的资产文档记录。</span><span class="sxs-lookup"><span data-stu-id="e0760-107">In that case, you just have to put the updated document in the standard location that you use for your Supply Chain Management documents, and attach the document to the asset document record that you've created.</span></span> <span data-ttu-id="e0760-108">然后可以从**所有资产**、**有效资产**、**我的有效资产**、**所有工作订单**和**有效工作订单作业**菜单项访问更新后的文档。</span><span class="sxs-lookup"><span data-stu-id="e0760-108">The updated document can then be accessed from the **All assets**, **Active assets**, **My active assets**, **All work orders**, and **Active work order jobs** menu items.</span></span> <span data-ttu-id="e0760-109">将文档附加到资产文档记录的过程使用标准文档处理系统。</span><span class="sxs-lookup"><span data-stu-id="e0760-109">The process for attaching documents to an asset document record uses the standard document handling system.</span></span>

<span data-ttu-id="e0760-110">**示例 1：** 与作业类型关联的文档可能介绍该作业类型的过程。</span><span class="sxs-lookup"><span data-stu-id="e0760-110">**Example 1:** A document that is related to a job type might describe a procedure for that job type.</span></span>

<span data-ttu-id="e0760-111">**示例 2：** 与资产类型、制造商和模型关联的文档可以是所选资产制造商模型的标准手册。</span><span class="sxs-lookup"><span data-stu-id="e0760-111">**Example 2:** A document that is related to a combination of an asset type, manufacturer, and model might be the standard manual for the selected asset manufacturer model.</span></span>

## <a name="create-asset-document-relation"></a><span data-ttu-id="e0760-112">创建资产文档关联</span><span class="sxs-lookup"><span data-stu-id="e0760-112">Create asset document relation</span></span>

1. <span data-ttu-id="e0760-113">选择**资产管理** \> **设置** \> **资产文档**。</span><span class="sxs-lookup"><span data-stu-id="e0760-113">Select **Asset management** \> **Setup** \> **Asset documents**.</span></span>
2. <span data-ttu-id="e0760-114">选择**新建**创建资产文档记录。</span><span class="sxs-lookup"><span data-stu-id="e0760-114">Select **New** to create an asset document record.</span></span>
3. <span data-ttu-id="e0760-115">根据所需文档关联的具体程度，在下面的一个或多个字段中进行相关选择：**资产类型**、**制造商**、**模型**、**资产**、**作业类型类别**、**作业类型**、**作业类型变体**和**作业要求**。</span><span class="sxs-lookup"><span data-stu-id="e0760-115">Depending on how specific you want the document relation to be, make relevant selections in one or more of the following fields: **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement**.</span></span> <span data-ttu-id="e0760-116">**作业类型变体**和**作业要求**字段中的可用选项取决于在**作业类型**字段中进行的选择。</span><span class="sxs-lookup"><span data-stu-id="e0760-116">The options that are available in the **Job type variant** and **Job requirement** fields depend on your selection in the **Job type** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e0760-117">系统搜索应该与资产或工作订单关联的文档时，资产管理检查所有资产文档记录以查找是否有可能的匹配项。</span><span class="sxs-lookup"><span data-stu-id="e0760-117">When the system searches for documents that should be related to an asset or a work order, Asset Management goes through all asset document records to check for a possible match.</span></span> <span data-ttu-id="e0760-118">始终先检查最具体的组合。</span><span class="sxs-lookup"><span data-stu-id="e0760-118">It always checks the most specific combination first.</span></span> <span data-ttu-id="e0760-119">换句话说，资产管理首先会检查**作业要求**字段的匹配项。</span><span class="sxs-lookup"><span data-stu-id="e0760-119">In other words, Asset Management first checks for a match for the **Job requirement** field.</span></span> <span data-ttu-id="e0760-120">如果未找到匹配项，将检查**作业类型变体**字段的匹配项。</span><span class="sxs-lookup"><span data-stu-id="e0760-120">If no match is found, it checks for a match for the **Job type variant** field.</span></span> <span data-ttu-id="e0760-121">如果未找到匹配项，将检查**作业类型**字段的匹配项，以此类推。</span><span class="sxs-lookup"><span data-stu-id="e0760-121">If no match is found, it checks for a match for the **Job type** field, and so on.</span></span> <span data-ttu-id="e0760-122">如**资产文档**页面布局中显示，此行为表示为了找到最具体的组合，资产管理从右到左检查每个记录以查找匹配项。</span><span class="sxs-lookup"><span data-stu-id="e0760-122">As you can see in the layout of the **Asset documents** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="e0760-123">可以将多个文档与一个资产或工作订单关联。</span><span class="sxs-lookup"><span data-stu-id="e0760-123">Several documents might be related to an asset or a work order.</span></span> <span data-ttu-id="e0760-124">可按照需要编辑维护请求或工作订单中的服务级别。</span><span class="sxs-lookup"><span data-stu-id="e0760-124">You can edit the service level on a maintenance request or a work order as you require.</span></span>

4. <span data-ttu-id="e0760-125">选择**附件**。</span><span class="sxs-lookup"><span data-stu-id="e0760-125">Select **Attachments**.</span></span> <span data-ttu-id="e0760-126">将显示标准**文档处理**页。</span><span class="sxs-lookup"><span data-stu-id="e0760-126">The standard **Document handling** page appears.</span></span>
5. <span data-ttu-id="e0760-127">设置应该附加到资产文档记录的文档或注释。</span><span class="sxs-lookup"><span data-stu-id="e0760-127">Set up the documents or notes that should be attached to the asset document record.</span></span> <span data-ttu-id="e0760-128">附加文档之后，**附件**字段显示与记录关联的文档数量。</span><span class="sxs-lookup"><span data-stu-id="e0760-128">After you attach documents, the **Attachments** field shows the number of documents that are related to the record.</span></span>
