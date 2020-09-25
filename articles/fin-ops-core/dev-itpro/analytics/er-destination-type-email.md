---
title: 电子邮件 ER 目标类型
description: 本主题提供相关信息，介绍如何为配置为生成出站文档的电子报告 (ER) 格式的每个文件夹或文件组件配置电子邮件目标。
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
ms.openlocfilehash: 72f67ad915ba2acc90ecb52bdb97e42504450a03
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745553"
---
# <a name="email-destination"></a><span data-ttu-id="2434f-103">电子邮件目标</span><span class="sxs-lookup"><span data-stu-id="2434f-103">Email destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2434f-104">您可以为配置为生成出站文档的电子报告 (ER) 格式的每个文件夹或文件组件配置电子邮件目标。</span><span class="sxs-lookup"><span data-stu-id="2434f-104">You can configure an email destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="2434f-105">根据目标设置，将生成的文档作为电子邮件的附件进行传递。</span><span class="sxs-lookup"><span data-stu-id="2434f-105">Based on the destination setting, a generated document is delivered as an attachment of an electronic mail.</span></span>

<span data-ttu-id="2434f-106">设置**已启用**为**是**以通过电子邮件发送输出文件。</span><span class="sxs-lookup"><span data-stu-id="2434f-106">Set **Enabled** to **Yes** to send an output file by email.</span></span> <span data-ttu-id="2434f-107">启用此选项后，您可以指定电子邮件收件人，以及编辑电子邮件的主题和正文。</span><span class="sxs-lookup"><span data-stu-id="2434f-107">After this option is enabled, you can specify the email recipients and edit the subject and body of the email message.</span></span> <span data-ttu-id="2434f-108">可以为电子邮件主题和正文设置固定文本，或者使用 ER [公式](er-formula-language.md)动态创建电子邮件文本。</span><span class="sxs-lookup"><span data-stu-id="2434f-108">You can set up constant texts for the email subject and body, or you can use ER [formulas](er-formula-language.md) to dynamically create email texts.</span></span> 

<span data-ttu-id="2434f-109">可以通过两种方法为 ER 配置电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="2434f-109">You can configure email addresses for ER in two ways.</span></span> <span data-ttu-id="2434f-110">可以用打印管理功能完成配置所用的相同方式来完成此配置，或者可以通过公式使用 ER 配置的直接引用来解析电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="2434f-110">The configuration can be completed in the same way that the Print management feature completes it, or you can resolve an email address by using a direct reference to the ER configuration through a formula.</span></span>

<span data-ttu-id="2434f-111">[![启用电子邮件目标](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span><span class="sxs-lookup"><span data-stu-id="2434f-111">[![Enable email destination](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span></span>

## <a name="email-address-types"></a><span data-ttu-id="2434f-112">电子邮件地址类型</span><span class="sxs-lookup"><span data-stu-id="2434f-112">Email address types</span></span>

<span data-ttu-id="2434f-113">选择**收件人**或**抄送**字段中的**编辑**时，将显示**电子邮件收件人**对话框。</span><span class="sxs-lookup"><span data-stu-id="2434f-113">When you select **Edit** in the **To** or **Cc** fields, the **Email to** dialog box appears.</span></span> <span data-ttu-id="2434f-114">然后可以选择要使用的电子邮件地址类型。</span><span class="sxs-lookup"><span data-stu-id="2434f-114">You can then select the type of email address to use.</span></span> <span data-ttu-id="2434f-115">当前支持**配置电子邮件**和**打印管理**电子邮件类型。</span><span class="sxs-lookup"><span data-stu-id="2434f-115">The **Configuration email** and **Print Management** email types are currently supported.</span></span>

<span data-ttu-id="2434f-116">[![选择电子邮件类型](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span><span class="sxs-lookup"><span data-stu-id="2434f-116">[![Select email type](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span></span>

### <a name="print-management"></a><span data-ttu-id="2434f-117">打印管理</span><span class="sxs-lookup"><span data-stu-id="2434f-117">Print management</span></span>

<span data-ttu-id="2434f-118">如果选择**打印管理**电子邮件类型，则可以在**收件人**字段中输入固定电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="2434f-118">If you select the **Print Management** email type, you can enter fixed email addresses in the **To** field.</span></span> 

<span data-ttu-id="2434f-119">[![配置固定的电子邮件地址](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span><span class="sxs-lookup"><span data-stu-id="2434f-119">[![Configure fixed email addresses](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span></span>

<span data-ttu-id="2434f-120">若要使用非固定电子邮件地址，您必须选择文件目标的电子邮件源类型。</span><span class="sxs-lookup"><span data-stu-id="2434f-120">To use email addresses that aren't fixed, you must select the email source type for a file destination.</span></span> <span data-ttu-id="2434f-121">支持下列值：**客户**、**供应商**、**目标客户**、**联系人**、**竞争对手**、**工作人员**、**申请人**、**潜在供应商**和**非许可供应商**。</span><span class="sxs-lookup"><span data-stu-id="2434f-121">The following values are supported: **Customer**, **Vendor**, **Prospect**, **Contact**, **Competitor**, **Worker**, **Applicant**, **Prospective vendor**, and **Disallowed vendor**.</span></span> <span data-ttu-id="2434f-122">选择电子邮件源类型后，请使用**电子邮件源帐户**字段旁边的按钮打开**公式设计器**窗体。</span><span class="sxs-lookup"><span data-stu-id="2434f-122">After you select an email source type, use the button next to the **Email source account** field to open the **Formula designer** form.</span></span> <span data-ttu-id="2434f-123">您可以使用此窗体附加一个公式，以在运行时将已处理文档中选定源类型的**当事方帐户**返回到电子邮件目标。</span><span class="sxs-lookup"><span data-stu-id="2434f-123">You can use this form to attach a formula that returns at runtime, the **party account** of the selected source type from the processed document to the email destination.</span></span>

<span data-ttu-id="2434f-124">[![配置电子邮件源帐户](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span><span class="sxs-lookup"><span data-stu-id="2434f-124">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span></span>

<span data-ttu-id="2434f-125">公式特定于 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="2434f-125">Formulas are specific to the ER configuration.</span></span> <span data-ttu-id="2434f-126">在**公式**中，输入客户或供应商当事方类型的文档特定引用。</span><span class="sxs-lookup"><span data-stu-id="2434f-126">In the **Formula** field, enter a document-specific reference to a customer or vendor party type.</span></span> <span data-ttu-id="2434f-127">您可以查找表示客户或供应商帐户的数据源节点（而不是键入），然后选择**添加数据源**来更新公式。</span><span class="sxs-lookup"><span data-stu-id="2434f-127">Instead of typing, you can find the data source node that represents the customer or vendor account, and then select **Add data source** to update the formula.</span></span> <span data-ttu-id="2434f-128">例如，如果您使用 **ISO 20022 贷方转帐**配置，则表示供应商帐户的节点是 `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`。</span><span class="sxs-lookup"><span data-stu-id="2434f-128">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents a vendor account is `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span></span>

<span data-ttu-id="2434f-129">如果输入字符串值，例如 `"DE-001"`，并保存公式，系统会将电子邮件发送给供应商的联系人，**DE-001**。</span><span class="sxs-lookup"><span data-stu-id="2434f-129">If you enter a string value, such as `"DE-001"`, and save a formula, an email will be sent to the contact person of the vendor, **DE-001**.</span></span>


<span data-ttu-id="2434f-130">[![ER 公式设计器页](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span><span class="sxs-lookup"><span data-stu-id="2434f-130">[![ER formula designer page](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span></span>

<span data-ttu-id="2434f-131">[![配置电子邮件源属性帐户](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span><span class="sxs-lookup"><span data-stu-id="2434f-131">[![Configure email source attributes account](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span></span>



### <a name="configuration-email"></a><span data-ttu-id="2434f-132">配置电子邮件</span><span class="sxs-lookup"><span data-stu-id="2434f-132">Configuration email</span></span>

<span data-ttu-id="2434f-133">如果所用配置在数据源中有一个返回**电子邮件地址**的节点，请使用此电子邮件类型。</span><span class="sxs-lookup"><span data-stu-id="2434f-133">Use this email type if the configuration that you use has a node in the data sources that returns an **email address**.</span></span> <span data-ttu-id="2434f-134">可使用公式设计器中的数据源和功能获取格式正确的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="2434f-134">You can use data sources and functions in the formula designer to get a correctly formatted email address.</span></span> <span data-ttu-id="2434f-135">例如，如果您使用 **ISO 20022 贷方转帐**配置，则表示供应商联系人电子邮件地址的节点是 `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`。</span><span class="sxs-lookup"><span data-stu-id="2434f-135">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents an email address of a vendor's contact person is `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span></span>

<span data-ttu-id="2434f-136">[![配置电子邮件地址源](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span><span class="sxs-lookup"><span data-stu-id="2434f-136">[![Configure email address source](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2434f-137">其他资源</span><span class="sxs-lookup"><span data-stu-id="2434f-137">Additional resources</span></span>

- [<span data-ttu-id="2434f-138">电子报告 (ER) 概览</span><span class="sxs-lookup"><span data-stu-id="2434f-138">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="2434f-139">电子报告 (ER) 目标</span><span class="sxs-lookup"><span data-stu-id="2434f-139">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="2434f-140">电子申报中 (ER) 的配方设计器</span><span class="sxs-lookup"><span data-stu-id="2434f-140">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
