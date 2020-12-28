---
title: 产品信息疑难解答
description: 此主题介绍如何解决处理产品信息时可能遇到的问题。
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 87b04998889b86a79fd8dabde422147c5494b003
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516737"
---
# <a name="troubleshoot-product-information"></a><span data-ttu-id="af4b2-103">产品信息疑难解答</span><span class="sxs-lookup"><span data-stu-id="af4b2-103">Troubleshoot product information</span></span>

<span data-ttu-id="af4b2-104">此主题介绍如何解决处理产品信息时可能遇到的问题。</span><span class="sxs-lookup"><span data-stu-id="af4b2-104">This topic describes how to fix issues that you might encounter while you work with product information.</span></span>

## <a name="i-cant-delete-a-released-product"></a><span data-ttu-id="af4b2-105">我无法删除已发布的产品。</span><span class="sxs-lookup"><span data-stu-id="af4b2-105">I can't delete a released product.</span></span>

### <a name="issue-description"></a><span data-ttu-id="af4b2-106">问题描述</span><span class="sxs-lookup"><span data-stu-id="af4b2-106">Issue description</span></span>

<span data-ttu-id="af4b2-107">仅当发布的产品没有任何相关交易时，才能删除发布的产品及其所有变型。</span><span class="sxs-lookup"><span data-stu-id="af4b2-107">You can delete a released product and all its variants only if the released product doesn't have any related transactions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="af4b2-108">解决问题</span><span class="sxs-lookup"><span data-stu-id="af4b2-108">Issue resolution</span></span>

<span data-ttu-id="af4b2-109">请按照以下步骤删除已发布的产品或基础产品。</span><span class="sxs-lookup"><span data-stu-id="af4b2-109">Follow these steps to delete a released product or product master.</span></span>

1. <span data-ttu-id="af4b2-110">关闭物料的所有未结交易。</span><span class="sxs-lookup"><span data-stu-id="af4b2-110">Close all open transactions for the items.</span></span>
1. <span data-ttu-id="af4b2-111">将库存减少到 0（零）。</span><span class="sxs-lookup"><span data-stu-id="af4b2-111">Reduce the inventory to 0 (zero).</span></span>
1. <span data-ttu-id="af4b2-112">执行库存结转。</span><span class="sxs-lookup"><span data-stu-id="af4b2-112">Perform inventory closing.</span></span>
1. <span data-ttu-id="af4b2-113">删除要删除的基础产品的所有产品变型。</span><span class="sxs-lookup"><span data-stu-id="af4b2-113">Delete all product variants for the product master that you want to delete.</span></span>

## <a name="can-i-change-the-item-number-of-a-released-product"></a><span data-ttu-id="af4b2-114">我可以更改已发布产品的物料编号吗？</span><span class="sxs-lookup"><span data-stu-id="af4b2-114">Can I change the item number of a released product?</span></span>

<span data-ttu-id="af4b2-115">在大多数情况下，您无法编辑已发布产品的物料编号，因为这种更改会导致数据损坏。</span><span class="sxs-lookup"><span data-stu-id="af4b2-115">In most cases, you can't edit item numbers for released products, because that change will cause data to become corrupted.</span></span> <span data-ttu-id="af4b2-116">仅当您必须修复由于之前对该已发布产品的主键进行重命名而导致的数据损坏时，才可以编辑物料编号，如[带平台更新 24 的 Finance and Operations 10.0.0 的已删除或已弃用功能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24)列表中所提到的。</span><span class="sxs-lookup"><span data-stu-id="af4b2-116">You can edit the item number only if you must repair data corruption that was caused by a previous rename of the primary key of that released product, as mentioned in the list of [removed or deprecated features for Finance and Operations 10.0.0 with Platform update 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).</span></span>

<span data-ttu-id="af4b2-117">如果您希望能够编辑已发布产品的物料编号，请[在思想门户为此想法投票](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25)。</span><span class="sxs-lookup"><span data-stu-id="af4b2-117">If you want to be able to edit item numbers for released products, [vote for this idea in Ideas portal](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span></span>

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a><span data-ttu-id="af4b2-118">产品的默认耗用原则未在物料清单行中输入。</span><span class="sxs-lookup"><span data-stu-id="af4b2-118">The default flushing principle from the product isn't being entered on the bill of materials line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="af4b2-119">问题描述</span><span class="sxs-lookup"><span data-stu-id="af4b2-119">Issue description</span></span>

<span data-ttu-id="af4b2-120">当您将物料添加到物料清单 (BOM) 行时，系统不会使用为物料设置的默认耗用原则信息。</span><span class="sxs-lookup"><span data-stu-id="af4b2-120">When you add an item to a bill of materials (BOM) line, the system doesn't use the default flushing principle information that is set up for the item.</span></span> <span data-ttu-id="af4b2-121">换言之，物料的耗用原则不会出现在 **物料清单行** 页上。</span><span class="sxs-lookup"><span data-stu-id="af4b2-121">In other words, the flushing principle from the item doesn't appear on the **BOM line** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="af4b2-122">解决问题</span><span class="sxs-lookup"><span data-stu-id="af4b2-122">Issue resolution</span></span>

<span data-ttu-id="af4b2-123">如果在物料清单行上指定耗用原则，它将应用于该物料清单行。</span><span class="sxs-lookup"><span data-stu-id="af4b2-123">If you specify a flushing principle on a BOM line, it will apply to that BOM line.</span></span> <span data-ttu-id="af4b2-124">但是，如果耗用原则为空白，或者未在物料清单行上设置，即使未在物料清单行上显示，在物料上设置的耗用原则仍会应用于该物料清单行。</span><span class="sxs-lookup"><span data-stu-id="af4b2-124">However, if the flushing principle is blank, or if it isn't set on a BOM line, the flushing principle that is set on the item will still apply to that BOM line, even though it isn't shown on the BOM line.</span></span>

<span data-ttu-id="af4b2-125"> Microsoft Dynamics 365 Supply Chain Management 中其他功能的默认逻辑通常不会以这种方式工作。</span><span class="sxs-lookup"><span data-stu-id="af4b2-125">The defaulting logic for other features in Microsoft Dynamics 365 Supply Chain Management doesn't usually work in this way.</span></span> <span data-ttu-id="af4b2-126">但是，当前行为不能更改。</span><span class="sxs-lookup"><span data-stu-id="af4b2-126">However, the current behavior can't be changed.</span></span> <span data-ttu-id="af4b2-127">否则，依赖它的部分现有自定义可能会被破坏。</span><span class="sxs-lookup"><span data-stu-id="af4b2-127">Otherwise, some existing customizations that rely on it might be broken.</span></span>

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a><span data-ttu-id="af4b2-128">系统允许我为不同的物料或具有不同维度的同一物料保存重复的条码。</span><span class="sxs-lookup"><span data-stu-id="af4b2-128">The system lets me save duplicate bar codes for different items or for the same item that has different dimensions.</span></span>

<span data-ttu-id="af4b2-129">系统当前不强制使用唯一条码，添加此限制将是一次中断性变更。</span><span class="sxs-lookup"><span data-stu-id="af4b2-129">The system doesn't currently enforce unique bar codes, and the addition of this restriction would be a breaking change.</span></span> <span data-ttu-id="af4b2-130">实际上，Microsoft 有证据表明此更改将破坏一些现有的客户安装。</span><span class="sxs-lookup"><span data-stu-id="af4b2-130">In fact, Microsoft has evidence that some existing customer installations would be broken by this change.</span></span> <span data-ttu-id="af4b2-131">不过，我们会考虑进行更广泛的设计更改来在将来启用此功能。</span><span class="sxs-lookup"><span data-stu-id="af4b2-131">However, we will consider a broader design change to enable this feature in the future.</span></span>

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a><span data-ttu-id="af4b2-132">我在编辑物料记录模板时收到以下错误消息：“无法创建仓库位置，因为该物料未贮存。</span><span class="sxs-lookup"><span data-stu-id="af4b2-132">I receive the following error message when I edit item record templates: "The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="af4b2-133">要贮存物料，必须在关联的物料模型组上选择‘贮存的产品’选项。”</span><span class="sxs-lookup"><span data-stu-id="af4b2-133">To stock items, the Stocked product option on the associated item model group must be selected."</span></span>

### <a name="issue-description"></a><span data-ttu-id="af4b2-134">问题描述</span><span class="sxs-lookup"><span data-stu-id="af4b2-134">Issue description</span></span>

<span data-ttu-id="af4b2-135">如果您按照以下步骤尝试为未贮存的物料创建模板，会出现此问题。</span><span class="sxs-lookup"><span data-stu-id="af4b2-135">This issue occurs if you follow these steps to try to create a template for an item that isn't stocked.</span></span>

1. <span data-ttu-id="af4b2-136">打开未贮存的已发布产品。</span><span class="sxs-lookup"><span data-stu-id="af4b2-136">Open a released product that isn't stocked.</span></span>
1. <span data-ttu-id="af4b2-137">在操作窗格上的 **选项** 选项卡中，选择 **记录信息**。</span><span class="sxs-lookup"><span data-stu-id="af4b2-137">On the Action Pane, on the **Options** tab, select **Record info**.</span></span>
1. <span data-ttu-id="af4b2-138">在 **记录信息** 对话框中，选择 **公司帐户模板**。</span><span class="sxs-lookup"><span data-stu-id="af4b2-138">In the **Record information** dialog box, select **Company accounts template**.</span></span>

<span data-ttu-id="af4b2-139">这时，您将收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="af4b2-139">In this case, you receive the following error message:</span></span>

> <span data-ttu-id="af4b2-140">无法创建仓库位置，因为该物料未贮存。</span><span class="sxs-lookup"><span data-stu-id="af4b2-140">The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="af4b2-141">要贮存物料，必须在关联的物料模型组上选择“贮存的产品”选项。</span><span class="sxs-lookup"><span data-stu-id="af4b2-141">To stock items, the Stocked product option on the associated item model group must be selected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="af4b2-142">解决问题</span><span class="sxs-lookup"><span data-stu-id="af4b2-142">Issue resolution</span></span>

<span data-ttu-id="af4b2-143">创建产品模板的流程需要额外的特定于产品的逻辑。</span><span class="sxs-lookup"><span data-stu-id="af4b2-143">The process of creating product templates requires extra product-specific logic.</span></span> <span data-ttu-id="af4b2-144">因此，您不能使用通用的 **公司帐户模板** 按钮来实现此目的。</span><span class="sxs-lookup"><span data-stu-id="af4b2-144">Therefore, you can't use the generic **Company accounts template** button for this purpose.</span></span> <span data-ttu-id="af4b2-145">而应执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="af4b2-145">Instead, follow these steps.</span></span>

1. <span data-ttu-id="af4b2-146">打开一个已发布产品。</span><span class="sxs-lookup"><span data-stu-id="af4b2-146">Open a released product.</span></span>
1. <span data-ttu-id="af4b2-147">在操作窗格的 **产品** 选项卡上的 **新建** 组中，选择 **模板 \> 创建共享模板**。</span><span class="sxs-lookup"><span data-stu-id="af4b2-147">On the Action Pane, on the **Product** tab, in the **New** group, select **Template \> Create shared template**.</span></span>

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a><span data-ttu-id="af4b2-148">产品属性中添加的默认帮助文本未在已发布产品中输入。</span><span class="sxs-lookup"><span data-stu-id="af4b2-148">Default Help text that is added in product attributes isn't entered in a released product.</span></span>

<span data-ttu-id="af4b2-149">默认情况下，产品属性中添加的说明和帮助文本不会在已发布产品中显示或输入。</span><span class="sxs-lookup"><span data-stu-id="af4b2-149">A description and Help text that are added in the product attributes aren't visible or entered by default in the released products.</span></span> <span data-ttu-id="af4b2-150">此为有意行为。</span><span class="sxs-lookup"><span data-stu-id="af4b2-150">This behavior is by design.</span></span>

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a><span data-ttu-id="af4b2-151">输入的默认数量在从物料清单注册与从物料清单版本注册时不同。</span><span class="sxs-lookup"><span data-stu-id="af4b2-151">The default quantity that is entered differs when it's registered from a BOM and when it's registered from a BOM version.</span></span>

### <a name="issue-description"></a><span data-ttu-id="af4b2-152">问题描述</span><span class="sxs-lookup"><span data-stu-id="af4b2-152">Issue description</span></span>

<span data-ttu-id="af4b2-153">默认情况下，将物料添加到物料清单时，数量设置为 1，而不是所选产品的 **默认订单设置** 页上 **最小订单数量** 字段中定义的数量。</span><span class="sxs-lookup"><span data-stu-id="af4b2-153">By default, when you add an item to a BOM, the quantity is set to 1 instead of the quantity that is defined in the **Min. order quantity** field on the **Default order settings** page for a selected product.</span></span> <span data-ttu-id="af4b2-154">但是，如果您从物料清单版本添加物料，在选择物料和变型时，输入的数量默认会考虑在默认订单设置中为特定维度设置的最小数量。</span><span class="sxs-lookup"><span data-stu-id="af4b2-154">However, when you add an item from a BOM version, and the item and variant are selected, the quantity that is entered by default takes into account the minimum quantity that is set in the default order settings for the specific dimensions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="af4b2-155">解决问题</span><span class="sxs-lookup"><span data-stu-id="af4b2-155">Issue resolution</span></span>

<span data-ttu-id="af4b2-156">此行为是预期的。</span><span class="sxs-lookup"><span data-stu-id="af4b2-156">This behavior is expected.</span></span> <span data-ttu-id="af4b2-157">但是，物料清单和物料清单版本中的逻辑不同这一事实是一个已知问题。</span><span class="sxs-lookup"><span data-stu-id="af4b2-157">However, the fact that the logic differs in the BOM and the BOM version is a known issue.</span></span> <span data-ttu-id="af4b2-158">不过，此行为不会更改，因为更改可能会影响许多不同的客户场景。</span><span class="sxs-lookup"><span data-stu-id="af4b2-158">Nevertheless, this behavior won't be changed, because a change could affect many different customer scenarios.</span></span>

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a><span data-ttu-id="af4b2-159">在已发布产品详细信息中，我无法更改从产品文档附件数据实体上载的附件图像。</span><span class="sxs-lookup"><span data-stu-id="af4b2-159">In the released product details, I can't change the attached images that were uploaded from the Product document attachments data entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="af4b2-160">问题描述</span><span class="sxs-lookup"><span data-stu-id="af4b2-160">Issue description</span></span>

<span data-ttu-id="af4b2-161">当您使用 *产品文档附件* 数据实体在物料中附加图像时，可能会发生此问题。</span><span class="sxs-lookup"><span data-stu-id="af4b2-161">This issue can occur when you attach an image to an item by using the *Product document attachments* data entity.</span></span> <span data-ttu-id="af4b2-162">在这种情况下，将为物料显示物料图像。</span><span class="sxs-lookup"><span data-stu-id="af4b2-162">In this case, the item image is shown for the item.</span></span> <span data-ttu-id="af4b2-163">但是，如果您选择 **更改图像**，上载的图像列表中不会显示任何内容。</span><span class="sxs-lookup"><span data-stu-id="af4b2-163">However, if you select **Change image**, nothing is shown in the list of uploaded images.</span></span> <span data-ttu-id="af4b2-164">而且，不会为物料显示附件。</span><span class="sxs-lookup"><span data-stu-id="af4b2-164">Additionally, no attachments are shown for the item.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="af4b2-165">解决问题</span><span class="sxs-lookup"><span data-stu-id="af4b2-165">Issue resolution</span></span>

<span data-ttu-id="af4b2-166">*EcoResProductDocumentAttachmentEntity* 实体（*产品文档附件*）导入 *产品* 的文档附件，但不能导入 *已发布产品* 的文档附件。</span><span class="sxs-lookup"><span data-stu-id="af4b2-166">The *EcoResProductDocumentAttachmentEntity* entity (*Product document attachments*) imports document attachments for *products* but not for *released products*.</span></span> <span data-ttu-id="af4b2-167">（已发布产品也称为 *物料*。）要在 **已发布产品详细信息** 页上查看物料的附件，您必须改为使用 *EcoResReleasedProductDocumentAttachmentEntity* 实体（*已发布产品文档附件*）。</span><span class="sxs-lookup"><span data-stu-id="af4b2-167">(Released products are also known as *items*.) To view the attachments for an item on the **Released product details** page, you must use the *EcoResReleasedProductDocumentAttachmentEntity* entity (*Released product document attachments*) instead.</span></span>

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a><span data-ttu-id="af4b2-168">Microsoft Flow 连接器显示以下错误消息：“不允许更新字段‘ProductNumber’。”</span><span class="sxs-lookup"><span data-stu-id="af4b2-168">The Microsoft Flow connector shows the following error message: "Update not allowed for field 'ProductNumber'."</span></span>

### <a name="issue-description"></a><span data-ttu-id="af4b2-169">问题描述</span><span class="sxs-lookup"><span data-stu-id="af4b2-169">Issue description</span></span>

<span data-ttu-id="af4b2-170">如果您尝试使用 *已发布产品* 实体 V2 和 Microsoft Flow 更新 **产品编号** 字段，会出现此问题。</span><span class="sxs-lookup"><span data-stu-id="af4b2-170">This issue occurs if you try to update the **Product number** field by using the *Released products* entity V2 and Microsoft Flow.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="af4b2-171">解决问题</span><span class="sxs-lookup"><span data-stu-id="af4b2-171">Issue resolution</span></span>

<span data-ttu-id="af4b2-172">此行为是预期的。</span><span class="sxs-lookup"><span data-stu-id="af4b2-172">This behavior is expected.</span></span> <span data-ttu-id="af4b2-173">已发布产品的产品编号编辑功能在带平台更新 24 的 Dynamics 365 Finance and Operations 10.0.0 中已移除，以帮助防止数据损坏。</span><span class="sxs-lookup"><span data-stu-id="af4b2-173">The ability to edit the product number for a released product was removed in Dynamics 365 Finance and Operations 10.0.0 with platform update 24 to help prevent data corruption.</span></span> <span data-ttu-id="af4b2-174">在特殊情况下，您必须修复由于之前对已发布产品的主键进行重命名而导致的数据损坏时，您可以让 Microsoft 支持部门临时移除此限制。</span><span class="sxs-lookup"><span data-stu-id="af4b2-174">In exceptional cases, where you must repair data corruption that was caused by a previous rename of the primary key of a released product, you can ask Microsoft Support to temporarily remove this restriction.</span></span>

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a><span data-ttu-id="af4b2-175">我无法在另一个法人中创建已发布产品变型。</span><span class="sxs-lookup"><span data-stu-id="af4b2-175">I can't create a released product variant in another legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="af4b2-176">问题描述</span><span class="sxs-lookup"><span data-stu-id="af4b2-176">Issue description</span></span>

<span data-ttu-id="af4b2-177">如果您尝试发布没有变型的基础产品，然后根据需要在每个法人（公司）中创建变型，您将无法使用变型建议来发布变型。</span><span class="sxs-lookup"><span data-stu-id="af4b2-177">If you try to release a product master without variants, and then create the variants in each legal entity (company) as they are required, you won't be able to release the variants by using variant suggestions.</span></span> <span data-ttu-id="af4b2-178">您也将无法手动创建变型。</span><span class="sxs-lookup"><span data-stu-id="af4b2-178">You also won't be able to manually create the variants.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="af4b2-179">解决问题</span><span class="sxs-lookup"><span data-stu-id="af4b2-179">Issue resolution</span></span>

<span data-ttu-id="af4b2-180">此为有意行为。</span><span class="sxs-lookup"><span data-stu-id="af4b2-180">This behavior is by design.</span></span> <span data-ttu-id="af4b2-181">基础产品的关系和基础产品可以采用的维度在共享级别保留。</span><span class="sxs-lookup"><span data-stu-id="af4b2-181">The relations of a product master and the dimensions that the master can take are kept at a shared level.</span></span> <span data-ttu-id="af4b2-182">因此，您无法在发布这些维度的特定法人中为共享基础产品创建可用维度，然后在需要这些维度的每个法人中复制流程。</span><span class="sxs-lookup"><span data-stu-id="af4b2-182">Therefore, you can't create the available dimensions for a shared product master in the specific legal entity where those dimensions are released and then replicate the process in each legal entity where the dimensions are required.</span></span> <span data-ttu-id="af4b2-183">而是必须更改发布流程以适应设计的流程。</span><span class="sxs-lookup"><span data-stu-id="af4b2-183">Instead, you must change your release process to adapt to the designed process.</span></span>

<span data-ttu-id="af4b2-184">这里是发布产品的流程。</span><span class="sxs-lookup"><span data-stu-id="af4b2-184">Here is the process for releasing products.</span></span>

1. <span data-ttu-id="af4b2-185">创建共享基础产品以及可以发布给法人的维度。</span><span class="sxs-lookup"><span data-stu-id="af4b2-185">Create the shared product master and the dimensions that can be released to the legal entities.</span></span>
1. <span data-ttu-id="af4b2-186">使用变型建议或通过手动添加应该发布的组合，将产品发布到法人。</span><span class="sxs-lookup"><span data-stu-id="af4b2-186">Release the products to the legal entities either by using variant suggestions or by manually adding the combinations that should be released.</span></span>

<span data-ttu-id="af4b2-187">或者，您可以直接创建已发布产品。</span><span class="sxs-lookup"><span data-stu-id="af4b2-187">Alternatively, you can directly create the released product.</span></span>

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a><span data-ttu-id="af4b2-188">我在另一个公司发布变型时收到以下错误消息：“具有指定维度的产品变型已创建。”</span><span class="sxs-lookup"><span data-stu-id="af4b2-188">When I release a variant in another company, I receive the following error message: "Product variant with specified dimensions has already been created."</span></span>

### <a name="issue-description"></a><span data-ttu-id="af4b2-189">问题描述</span><span class="sxs-lookup"><span data-stu-id="af4b2-189">Issue description</span></span>

<span data-ttu-id="af4b2-190">如果某个产品变型已经在公司 A 中发布，当您尝试使用 **已发布产品变型** 页上的 **新建** 按钮在公司 B 中发布该变型时，会收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="af4b2-190">If a product variant has already been released in a company A, and you try to release it in company B by using the **New** button on the **Released product variants** page, you will receive the following error message:</span></span>

> <span data-ttu-id="af4b2-191">已创建具有指定维度的产品变型。</span><span class="sxs-lookup"><span data-stu-id="af4b2-191">Product variant with specified dimensions has already been created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="af4b2-192">解决问题</span><span class="sxs-lookup"><span data-stu-id="af4b2-192">Issue resolution</span></span>

<span data-ttu-id="af4b2-193">**已发布产品变型** 页上的 **新建** 按钮在公司上下文中创建变型并发布。</span><span class="sxs-lookup"><span data-stu-id="af4b2-193">The **New** button on the **Released product variants** page creates the variant and releases it in the company context.</span></span> <span data-ttu-id="af4b2-194">如果变型已创建，则无法使用 **新建** 按钮将其发布到另一个公司。</span><span class="sxs-lookup"><span data-stu-id="af4b2-194">If the variant has already been created, you can't use the **New** button to release it in another company.</span></span>

<span data-ttu-id="af4b2-195">要解决此问题，请打开 **基础产品** 页，选择 **发布产品** 在所需公司中发布现有变型。</span><span class="sxs-lookup"><span data-stu-id="af4b2-195">To fix the issue, open the **Product master** page, and select **Release product** to release the existing variant in the desired company.</span></span>
