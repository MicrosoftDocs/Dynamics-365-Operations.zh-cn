---
title: 物料清单模板
description: 使用物料清单模板提供定期提供服务的服务对象组件的标准化列表。
author: ShylaThompson
manager: tfehr
ms.date: 09/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8842a293a50efb24590784cc52ef0254eca10e3a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206534"
---
# <a name="template-boms"></a><span data-ttu-id="38274-103">物料清单模板</span><span class="sxs-lookup"><span data-stu-id="38274-103">Template BOMs</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="38274-104">使用物料清单模板为您提供定期提供服务的服务对象组件的标准化列表。</span><span class="sxs-lookup"><span data-stu-id="38274-104">A template bill of materials (BOM) provides you with a standardized list of components for service objects that are serviced regularly.</span></span> <span data-ttu-id="38274-105">物料清单模板中所列的组件表示服务对象的各个子组件。</span><span class="sxs-lookup"><span data-stu-id="38274-105">The components that are listed in the template BOM represent the individual subcomponents of the service object.</span></span> <span data-ttu-id="38274-106">当您将物料清单模板应用到某服务对象时，您可以记录为该服务对象更换了哪些子组件。</span><span class="sxs-lookup"><span data-stu-id="38274-106">By applying a template BOM to a service object, you can keep a record of the subcomponents that have been replaced on the service object.</span></span>

<span data-ttu-id="38274-107">为了将物料清单模板应用到某一服务协议或服务订单，您将它附加到某一服务对象关系。</span><span class="sxs-lookup"><span data-stu-id="38274-107">To apply a template BOM to a service agreement or a service order, you attach it to a service object relation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="38274-108">每个服务对象只能应用一个物料清单模板。</span><span class="sxs-lookup"><span data-stu-id="38274-108">You can apply only one template BOM to a service object.</span></span></P>

## <a name="create-a-template-bom"></a><span data-ttu-id="38274-109">创建物料清单模板</span><span class="sxs-lookup"><span data-stu-id="38274-109">Create a template BOM</span></span>

<span data-ttu-id="38274-110">下表包含可用于创建物料清单模板的各种方式的信息。</span><span class="sxs-lookup"><span data-stu-id="38274-110">The following table contains information about the various methods that you can use to create a template BOM.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="38274-111">方法</span><span class="sxs-lookup"><span data-stu-id="38274-111">Method</span></span></p></th>
<th><p><span data-ttu-id="38274-112"> 描述</span><span class="sxs-lookup"><span data-stu-id="38274-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38274-113">生产</span><span class="sxs-lookup"><span data-stu-id="38274-113">Production</span></span></p></td>
<td><p><span data-ttu-id="38274-114">物料清单模板基于生产订单。</span><span class="sxs-lookup"><span data-stu-id="38274-114">The template BOM is based on a production order.</span></span> <span data-ttu-id="38274-115">如果仅在生产环境中操作，将适用此选项。</span><span class="sxs-lookup"><span data-stu-id="38274-115">This option is applicable only if you operate in a production environment.</span></span> <span data-ttu-id="38274-116">它的好处是提供构成物料的组件的当前详细清单。</span><span class="sxs-lookup"><span data-stu-id="38274-116">The benefit is that you have a current, detailed listing of the components that make up an item.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38274-117">物料 BOM</span><span class="sxs-lookup"><span data-stu-id="38274-117">Item BOM</span></span></p></td>
<td><p><span data-ttu-id="38274-118">该物料清单模板基于某一物料的物料清单。</span><span class="sxs-lookup"><span data-stu-id="38274-118">The template BOM is based on an item BOM.</span></span> <span data-ttu-id="38274-119">该物料的物料清单与生产物料清单不同，为构成物料的组件的一个静态列表。</span><span class="sxs-lookup"><span data-stu-id="38274-119">The item BOM, unlike the production BOM, is a static list of the components that make up an item.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38274-120">现有的模板</span><span class="sxs-lookup"><span data-stu-id="38274-120">Existing template</span></span></p></td>
<td><p><span data-ttu-id="38274-121">该模板基于现有物料清单的模版。</span><span class="sxs-lookup"><span data-stu-id="38274-121">The template is based on an existing template BOM.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38274-122">手动</span><span class="sxs-lookup"><span data-stu-id="38274-122">Manual</span></span></p></td>
<td><p><span data-ttu-id="38274-123">如果了解通常要为服务对象更换哪些备件，您可能创建自己的物料清单模板。</span><span class="sxs-lookup"><span data-stu-id="38274-123">If you know what spare parts are typically replaced on a service object, you can create your template BOM manually.</span></span> <span data-ttu-id="38274-124">此方法可以帮助您确保模板中包括的组件反映工作场所的实际需求。</span><span class="sxs-lookup"><span data-stu-id="38274-124">This method helps make sure that the components that are included in the template reflect the actual requirements of your workplace.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a><span data-ttu-id="38274-125">将物料清单模板应用到某一服务协议或服务订单</span><span class="sxs-lookup"><span data-stu-id="38274-125">Apply the template BOM to a service agreement or service order</span></span>

<span data-ttu-id="38274-126">您可以将物料清单模板应用到服务协议、服务订单或两者同时应用。</span><span class="sxs-lookup"><span data-stu-id="38274-126">You can apply a template BOM to a service agreement, a service order, or both.</span></span> <span data-ttu-id="38274-127">服务协议通常涉及与客户的长期关系。</span><span class="sxs-lookup"><span data-stu-id="38274-127">The service agreement usually covers a long-term relationship with a customer.</span></span> <span data-ttu-id="38274-128">服务物料清单上记录的更换历史信息对服务协议是有用的数据。</span><span class="sxs-lookup"><span data-stu-id="38274-128">The history of replacements that is recorded in the service BOM is useful data to have for the service agreement.</span></span>

<span data-ttu-id="38274-129">您还可以将物料清单模板应用到某服务订单记录为该服务对象执行的服务的历史记录。</span><span class="sxs-lookup"><span data-stu-id="38274-129">You can also apply a template BOM to a service order to record the history of the service that has been performed on a service object.</span></span>

## <a name="copy-the-history-of-a-service-bom"></a><span data-ttu-id="38274-130">复制服务物料清单的历史记录</span><span class="sxs-lookup"><span data-stu-id="38274-130">Copy the history of a service BOM</span></span>

<span data-ttu-id="38274-131">可以将服务物料清单行的历史记录从一个服务协议复制到另一个服务协议。</span><span class="sxs-lookup"><span data-stu-id="38274-131">You can copy the history of a service BOM line from one service agreement to another service agreement.</span></span> <span data-ttu-id="38274-132">通过在服务协议间复制服务历史记录，可以保存物料的更换记录。</span><span class="sxs-lookup"><span data-stu-id="38274-132">By copying the service history between service agreements, you can preserve the record of replacements for an item.</span></span>

<span data-ttu-id="38274-133">**示例**</span><span class="sxs-lookup"><span data-stu-id="38274-133">**Example**</span></span>

<span data-ttu-id="38274-134">您为客户的小汽车设置了三年的服务协议。</span><span class="sxs-lookup"><span data-stu-id="38274-134">You have set up a three-year service agreement for a customer's car.</span></span> <span data-ttu-id="38274-135">在该期间，客户已习惯公司提供的优良服务。</span><span class="sxs-lookup"><span data-stu-id="38274-135">During that period, the customer becomes accustomed to the good service that the company provides.</span></span> <span data-ttu-id="38274-136">因此，在协议到期后，客户想要设置新的协议。</span><span class="sxs-lookup"><span data-stu-id="38274-136">Therefore, after the agreement expires, the customer wants to set up a new one.</span></span> <span data-ttu-id="38274-137">您现在可以寻求通过谈判签订对公司更有利的协议。</span><span class="sxs-lookup"><span data-stu-id="38274-137">You are now able to negotiate a more favorable agreement for the company.</span></span> <span data-ttu-id="38274-138">因为更换组件的记录在将来可能有用，您将服务物料清单的历史记录复制到新协议。</span><span class="sxs-lookup"><span data-stu-id="38274-138">Because the record of replaced components might be useful in the future, you copy the history of the service BOM to the new agreement.</span></span>

## <a name="modify-the-template-bom"></a><span data-ttu-id="38274-139">修改物料清单模板</span><span class="sxs-lookup"><span data-stu-id="38274-139">Modify the template BOM</span></span>

<span data-ttu-id="38274-140">如果尚未将物料清单模板附加到服务对象，可以修改或删除其中的行。</span><span class="sxs-lookup"><span data-stu-id="38274-140">If a template BOM has not been attached to a service object, you can modify or delete lines in it.</span></span> <span data-ttu-id="38274-141">将物料清单模板附加到某服务对象后，只能修改物料清单的本地版本。</span><span class="sxs-lookup"><span data-stu-id="38274-141">After the template BOM is attached to a service object, you can modify only the local version of the BOM.</span></span> <span data-ttu-id="38274-142">如果要复制物料清单模板本地版本的设置，可以基于本地版本创建新的物料清单模板。</span><span class="sxs-lookup"><span data-stu-id="38274-142">If you want to duplicate the setup of a local version of a template BOM, you can create a new template BOM based on the local version.</span></span> <span data-ttu-id="38274-143">有关服务间隔的详细信息，请参阅[修改物料清单模板](modify-service-bom.md)。</span><span class="sxs-lookup"><span data-stu-id="38274-143">For more information, see [Modify a Service BOM](modify-service-bom.md).</span></span>

<span data-ttu-id="38274-144">如果更换物料清单中的某个物料，可以在物料清单设计器中的物料清单行上登记更换情况。</span><span class="sxs-lookup"><span data-stu-id="38274-144">If you replace an item in the BOM, you can register the replacement on the BOM line in the BOM designer.</span></span> <span data-ttu-id="38274-145">或者，您可以为更换对象创建服务订单行。</span><span class="sxs-lookup"><span data-stu-id="38274-145">Optionally, you can create a service order line for the replacement object.</span></span> <span data-ttu-id="38274-146">如果创建服务订单行，您可以为更换物料开发票。</span><span class="sxs-lookup"><span data-stu-id="38274-146">If you create a service order line, you can invoice the replacement item.</span></span> <span data-ttu-id="38274-147">如果不为更换创建服务订单行，将保留更换登记跟踪服务对象的历史记录。</span><span class="sxs-lookup"><span data-stu-id="38274-147">If you do not create a service order line for a replacement, the replacement registration is kept to track the history of the service object.</span></span>

## <a name="change-how-information-on-the-bom-line-is-displayed"></a><span data-ttu-id="38274-148">更改任何显示物料清单行信息</span><span class="sxs-lookup"><span data-stu-id="38274-148">Change how information on the BOM line is displayed</span></span>

<span data-ttu-id="38274-149">可以更改所有模板和服务物料清单显示物料清单行信息的方式。</span><span class="sxs-lookup"><span data-stu-id="38274-149">You can change the way that information on the BOM line is displayed for all template and service BOMs.</span></span> <span data-ttu-id="38274-150">更改应用于所有物料清单模板和服务物料清单。</span><span class="sxs-lookup"><span data-stu-id="38274-150">The changes are applied to all template BOMs and service BOMs.</span></span> <span data-ttu-id="38274-151">这包括附加到服务对象的物料。</span><span class="sxs-lookup"><span data-stu-id="38274-151">This includes those that are attached to service objects.</span></span>

## <a name="set-up-number-sequences-for-template-boms"></a><span data-ttu-id="38274-152">设置物料清单模板的编号规则</span><span class="sxs-lookup"><span data-stu-id="38274-152">Set up number sequences for template BOMs</span></span>

<span data-ttu-id="38274-153">若要使用物料清单模板，您必须设置两个编号规则。</span><span class="sxs-lookup"><span data-stu-id="38274-153">To use template BOMs, you must set up two number sequences.</span></span> <span data-ttu-id="38274-154">设置一个编号规则用于物料清单模板，一个用于物料清单历史记录行号。</span><span class="sxs-lookup"><span data-stu-id="38274-154">Set up one number sequence for the template BOM and one for the BOM history line number.</span></span>


> [!NOTE]
> <P><span data-ttu-id="38274-155">编号规则用于分配标识到需要它们的记录。</span><span class="sxs-lookup"><span data-stu-id="38274-155">Number sequences are used to allocate identifiers to records that require them.</span></span> <span data-ttu-id="38274-156">在您可以将某一编号规则分配给物料清单模板或物料清单历史记录行编号之前，必须设置编号规则代码。</span><span class="sxs-lookup"><span data-stu-id="38274-156">Before you can assign a number sequence to a template BOM or a BOM history line number, you must set up number sequences codes.</span></span></P>


## <a name="set-up-number-sequences"></a><span data-ttu-id="38274-157">设置编号规则</span><span class="sxs-lookup"><span data-stu-id="38274-157">Set up number sequences</span></span>

1.  <span data-ttu-id="38274-158">在**编号规则**列表页，创建物料清单模板和物料清单历史记录行编号的编号规则。</span><span class="sxs-lookup"><span data-stu-id="38274-158">On the **Number sequences** list page, create number sequences for template BOMs and the BOM history line number.</span></span> 

2.  <span data-ttu-id="38274-159">单击**服务管理** \> **设置**\> **服务管理参数**。</span><span class="sxs-lookup"><span data-stu-id="38274-159">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

3.  <span data-ttu-id="38274-160">单击**编号规则** ，然后为您在**编号规则**窗体中创建的编号规则引用的编号规则代码。</span><span class="sxs-lookup"><span data-stu-id="38274-160">Click **Number sequences**, and then select a number sequence code for the number sequence references that you created in the **Number sequences** form.</span></span>

4.  <span data-ttu-id="38274-161">关闭窗体以保存您所做更改。</span><span class="sxs-lookup"><span data-stu-id="38274-161">Close the form to save your changes.</span></span>


> [!NOTE]
> <P><span data-ttu-id="38274-162">系统使用物料清单历史记录行编号将物料清单历史记录中的交易记录与某一服务协议或服务订单关联。</span><span class="sxs-lookup"><span data-stu-id="38274-162">The BOM history line number is used by the system to associate the transactions in the BOM history with a service agreement or service order.</span></span> <span data-ttu-id="38274-163">编号不显示在用户界面上。</span><span class="sxs-lookup"><span data-stu-id="38274-163">The number is not displayed in the user interface.</span></span></P>



## <a name="see-also"></a><span data-ttu-id="38274-164">请参阅</span><span class="sxs-lookup"><span data-stu-id="38274-164">See also</span></span>

[<span data-ttu-id="38274-165">创建物料清单模板</span><span class="sxs-lookup"><span data-stu-id="38274-165">Create a template BOM</span></span>](create-template-bom.md)

[<span data-ttu-id="38274-166">管理针对对象关系的物料清单模板</span><span class="sxs-lookup"><span data-stu-id="38274-166">Manage template BOMs on object relations</span></span>](manage-template-boms-on-object-relations.md)

[<span data-ttu-id="38274-167">修改服务项清单</span><span class="sxs-lookup"><span data-stu-id="38274-167">Modify a Service BOM</span></span>](modify-service-bom.md)

 


