---
title: ER 配置目标
description: 此过程演示如何设置和使用不同的电子申报 (ER) 输出组件的目标，例如文件夹或文件。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERFormatDestinationTable, SysLookupPicklist, ERFormatDestinationSettings, ERFormatDestinationEmailSettings, ERExpressionDesignerFormula, SRSPrintDestinationTokens
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cbef5410d0e6f15fbb5025f3831486d55cd06216
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185052"
---
# <a name="er-configure-destinations"></a><span data-ttu-id="5454d-103">ER 配置目标</span><span class="sxs-lookup"><span data-stu-id="5454d-103">ER Configure destinations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5454d-104">此过程演示如何设置和使用不同的电子申报 (ER) 输出组件的目标，例如文件夹或文件。</span><span class="sxs-lookup"><span data-stu-id="5454d-104">This procedure demonstrates how to set up and use different destinations for Electronic reporting (ER) output components, such as a folder or a file.</span></span> <span data-ttu-id="5454d-105">用于创建此过程的演示数据公司是 DEMF。</span><span class="sxs-lookup"><span data-stu-id="5454d-105">The demo data company used to create this procedure is DEMF.</span></span> <span data-ttu-id="5454d-106">德国为法人主要地址的国家\地区，但您可以为此过程使用任何法人。</span><span class="sxs-lookup"><span data-stu-id="5454d-106">Germany is the country\region of the legal entity’s primary address, however you can use any legal entity for this procedure.</span></span> 

<span data-ttu-id="5454d-107">此示例使用的格式是 ISO20022 贷方转帐，不过，您可以使用您已经导入的任何格式。</span><span class="sxs-lookup"><span data-stu-id="5454d-107">The format used in this example is ISO20022 Credit transfer, but you can use any format that you have already imported.</span></span> <span data-ttu-id="5454d-108">请注意，此过程是单个文件和单个目标设置的示例。</span><span class="sxs-lookup"><span data-stu-id="5454d-108">Note, this procedure is an example of a single file and a single destination setup.</span></span> <span data-ttu-id="5454d-109">有关电子申报目标管理的详细信息可以在 Dynamics 365 Finance 帮助中找到。</span><span class="sxs-lookup"><span data-stu-id="5454d-109">More information about Electronic reporting destination management can be found in the Dynamics 365 Finance Help.</span></span>

1. <span data-ttu-id="5454d-110">转到“组织管理”>“电子申报”>“电子申报目标”。</span><span class="sxs-lookup"><span data-stu-id="5454d-110">Go to Organization administration > Electronic reporting > Electronic reporting destination.</span></span>
2. <span data-ttu-id="5454d-111">单击“新建”为格式创建一组新目标。</span><span class="sxs-lookup"><span data-stu-id="5454d-111">Click New to create a new set of destinations for a format.</span></span>
3. <span data-ttu-id="5454d-112">在“引用”字段中，选择要为其配置目标的格式。</span><span class="sxs-lookup"><span data-stu-id="5454d-112">In the Reference field, select a format for which you want to configure destinations.</span></span>
    * <span data-ttu-id="5454d-113">如果您没有要选择的值，则表明您尚未导入任何电子申报格式配置。</span><span class="sxs-lookup"><span data-stu-id="5454d-113">If you don't have a value to select, it means that you have not imported any Electronic reporting format configurations.</span></span> <span data-ttu-id="5454d-114">您必须在设置目标前导入格式配置。</span><span class="sxs-lookup"><span data-stu-id="5454d-114">You must import a format configuration before setting up destinations.</span></span>  
4. <span data-ttu-id="5454d-115">单击“新建”创建新文件目标。</span><span class="sxs-lookup"><span data-stu-id="5454d-115">Click New to create a new file destination.</span></span>
    * <span data-ttu-id="5454d-116">请注意，您可以为相同格式的每个输出组件创建一个文件目标，如文件夹或文件。</span><span class="sxs-lookup"><span data-stu-id="5454d-116">Note, you can create one file destination for each output component of the same format, such as a folder or a file.</span></span> <span data-ttu-id="5454d-117">您可以在设置中单独启用和禁用目标。</span><span class="sxs-lookup"><span data-stu-id="5454d-117">You will be able to enable and disable destinations separately in the settings.</span></span>  
5. <span data-ttu-id="5454d-118">在“名称”字段中，输入用户易识别的输出组件的名称。</span><span class="sxs-lookup"><span data-stu-id="5454d-118">In the Name field, enter the user-friendly name of output component.</span></span>
    * <span data-ttu-id="5454d-119">我们建议您使用有意义的名称，如“付款文件“或“控制报表”。</span><span class="sxs-lookup"><span data-stu-id="5454d-119">We recommend that you use meaningful names, such as "Payment file" or "Control report".</span></span> <span data-ttu-id="5454d-120">这些名称将在配置运行时间与目标设置一同呈现给用户。</span><span class="sxs-lookup"><span data-stu-id="5454d-120">These names will be presented to users at configuration runtime along with the destination settings.</span></span>  
6. <span data-ttu-id="5454d-121">在“文件名”中，选择特定于格式的文件或文件夹。</span><span class="sxs-lookup"><span data-stu-id="5454d-121">In the File name, select a file or folder that is specific to the format.</span></span>
7. <span data-ttu-id="5454d-122">单击“设置”。</span><span class="sxs-lookup"><span data-stu-id="5454d-122">Click Settings.</span></span>
8. <span data-ttu-id="5454d-123">在“已启用”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="5454d-123">Select Yes in the Enabled field.</span></span>
    * <span data-ttu-id="5454d-124">每个选项卡的“已启用”复选框可以单独启用和禁用每个目标。</span><span class="sxs-lookup"><span data-stu-id="5454d-124">The Enabled check box on each tab enables and disables each destination separately.</span></span> <span data-ttu-id="5454d-125">在此示例中，在生成文件时，您将启用将输出文件发送到邮件收件人。</span><span class="sxs-lookup"><span data-stu-id="5454d-125">In this example, you'll enable sending an output file to a mail recipient when the file is generated.</span></span>  
9. <span data-ttu-id="5454d-126">单击"编辑"设置电子邮件收件人。</span><span class="sxs-lookup"><span data-stu-id="5454d-126">Click Edit, to set up email recipients.</span></span>
10. <span data-ttu-id="5454d-127">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="5454d-127">Click Add.</span></span>
11. <span data-ttu-id="5454d-128">单击“打印管理电子邮件”。</span><span class="sxs-lookup"><span data-stu-id="5454d-128">Click Print Management email.</span></span>
12. <span data-ttu-id="5454d-129">在“电子邮件源”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="5454d-129">In the Email source  field, select an option.</span></span>
    * <span data-ttu-id="5454d-130">您可以选择不同的电子邮件源类型，如客户或供应商类型。</span><span class="sxs-lookup"><span data-stu-id="5454d-130">You can select different email source types, such as a customer or a vendor type.</span></span> <span data-ttu-id="5454d-131">这定义将由电子邮件源帐户公式返回的参数的类型。</span><span class="sxs-lookup"><span data-stu-id="5454d-131">This defines the type of argument that will be returned by the Email source account formula.</span></span> <span data-ttu-id="5454d-132">电子邮件源帐户公式（在下列步骤中描述）是您要绑定电子邮件源的位置。</span><span class="sxs-lookup"><span data-stu-id="5454d-132">The Email source account formula, described in a following step, is the place where you bind an email source.</span></span> <span data-ttu-id="5454d-133">如果您的公式将返回供应商帐户，则选择“供应商”。</span><span class="sxs-lookup"><span data-stu-id="5454d-133">Select Vendor if your formula will return a vendor account.</span></span> <span data-ttu-id="5454d-134">如果您使用 ISO 20022 贷方转帐配置示例，同使用“供应商”。</span><span class="sxs-lookup"><span data-stu-id="5454d-134">Use Vendor if you are using the ISO 20022 Credit Transfer configuration example.</span></span>  
13. <span data-ttu-id="5454d-135">单击“电子邮件源绑定”按钮。</span><span class="sxs-lookup"><span data-stu-id="5454d-135">Click Email source bind button.</span></span>
14. <span data-ttu-id="5454d-136">在“公式”中，输入您在前面选择的当事方类型的票据特定引用。</span><span class="sxs-lookup"><span data-stu-id="5454d-136">In the Formula, enter a document-specific reference to a party type that you selected earlier.</span></span>
    * <span data-ttu-id="5454d-137">不是键入，您可以查找表示当事方帐户的数据源节点，然后单击“添加数据源”按钮来更新公式。</span><span class="sxs-lookup"><span data-stu-id="5454d-137">Instead of typing, you can find a data source node that represents the party account, and click the Add data source button to update the formula.</span></span> <span data-ttu-id="5454d-138">例如，如果您使用 ISO 20022 贷方转帐配置，表示供应商帐户的节点是 '$PaymentsForCoveringLetter'.Creditor.Identification.SourceID。</span><span class="sxs-lookup"><span data-stu-id="5454d-138">For example, if you use the ISO 20022 Credit Transfer configuration, the node representing a vendor account is '$PaymentsForCoveringLetter'.Creditor.Identification.SourceID.</span></span> <span data-ttu-id="5454d-139">否则，输入任何字符串值，例如 "DE-001" 来保存公式。</span><span class="sxs-lookup"><span data-stu-id="5454d-139">Otherwise, enter any string value, such as "DE-001", to save a formula.</span></span>  
15. <span data-ttu-id="5454d-140">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="5454d-140">Click Save.</span></span>
16. <span data-ttu-id="5454d-141">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="5454d-141">Close the page.</span></span>
17. <span data-ttu-id="5454d-142">单击“编辑”为当事方配置联系人详细信息。</span><span class="sxs-lookup"><span data-stu-id="5454d-142">Click Edit to configure contact details for the party.</span></span>
18. <span data-ttu-id="5454d-143">在“主要联系人”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="5454d-143">Select Yes in the Primary contact field.</span></span>
    * <span data-ttu-id="5454d-144">可以使用不同选项指示应将当事方的哪种联系人类型用作此目标的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="5454d-144">You may use different options to indicate what contact type of the party should be used as an email address for this destination.</span></span> <span data-ttu-id="5454d-145">此示例中，我们使用主要联系人。</span><span class="sxs-lookup"><span data-stu-id="5454d-145">We use primary contact in this example.</span></span>  
19. <span data-ttu-id="5454d-146">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="5454d-146">Click OK.</span></span>
20. <span data-ttu-id="5454d-147">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="5454d-147">Click OK.</span></span>
21. <span data-ttu-id="5454d-148">在“主题”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="5454d-148">In the Subject field, type a value.</span></span>
22. <span data-ttu-id="5454d-149">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="5454d-149">Click OK.</span></span>

