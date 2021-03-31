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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a9db8e0081a0d47ec8d74680fe99a0934b99bb5c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223354"
---
# <a name="troubleshoot-product-information"></a>产品信息疑难解答

此主题介绍如何解决处理产品信息时可能遇到的问题。

## <a name="i-cant-delete-a-released-product"></a>我无法删除已发布的产品。

### <a name="issue-description"></a>问题描述

仅当发布的产品没有任何相关交易时，才能删除发布的产品及其所有变型。

### <a name="issue-resolution"></a>解决问题

请按照以下步骤删除已发布的产品或基础产品。

1. 关闭物料的所有未结交易。
1. 将库存减少到 0（零）。
1. 执行库存结转。
1. 删除要删除的基础产品的所有产品变型。

## <a name="can-i-change-the-item-number-of-a-released-product"></a>我可以更改已发布产品的物料编号吗？

在大多数情况下，您无法编辑已发布产品的物料编号，因为这种更改会导致数据损坏。 仅当您必须修复由于之前对该已发布产品的主键进行重命名而导致的数据损坏时，才可以编辑物料编号，如[带平台更新 24 的 Finance and Operations 10.0.0 的已删除或已弃用功能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24)列表中所提到的。

如果您希望能够编辑已发布产品的物料编号，请[在思想门户为此想法投票](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25)。

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a>产品的默认耗用原则未在物料清单行中输入。

### <a name="issue-description"></a>问题描述

当您将物料添加到物料清单 (BOM) 行时，系统不会使用为物料设置的默认耗用原则信息。 换言之，物料的耗用原则不会出现在 **物料清单行** 页上。

### <a name="issue-resolution"></a>解决问题

如果在物料清单行上指定耗用原则，它将应用于该物料清单行。 但是，如果耗用原则为空白，或者未在物料清单行上设置，即使未在物料清单行上显示，在物料上设置的耗用原则仍会应用于该物料清单行。

 Microsoft Dynamics 365 Supply Chain Management 中其他功能的默认逻辑通常不会以这种方式工作。 但是，当前行为不能更改。 否则，依赖它的部分现有自定义可能会被破坏。

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a>系统允许我为不同的物料或具有不同维度的同一物料保存重复的条码。

系统当前不强制使用唯一条码，添加此限制将是一次中断性变更。 实际上，Microsoft 有证据表明此更改将破坏一些现有的客户安装。 不过，我们会考虑进行更广泛的设计更改来在将来启用此功能。

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a>我在编辑物料记录模板时收到以下错误消息：“无法创建仓库位置，因为该物料未贮存。 要贮存物料，必须在关联的物料模型组上选择‘贮存的产品’选项。”

### <a name="issue-description"></a>问题描述

如果您按照以下步骤尝试为未贮存的物料创建模板，会出现此问题。

1. 打开未贮存的已发布产品。
1. 在操作窗格上的 **选项** 选项卡中，选择 **记录信息**。
1. 在 **记录信息** 对话框中，选择 **公司帐户模板**。

这时，您将收到以下错误消息：

> 无法创建仓库位置，因为该物料未贮存。 要贮存物料，必须在关联的物料模型组上选择“贮存的产品”选项。

### <a name="issue-resolution"></a>解决问题

创建产品模板的流程需要额外的特定于产品的逻辑。 因此，您不能使用通用的 **公司帐户模板** 按钮来实现此目的。 而应执行以下步骤。

1. 打开一个已发布产品。
1. 在操作窗格的 **产品** 选项卡上的 **新建** 组中，选择 **模板 \> 创建共享模板**。

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a>产品属性中添加的默认帮助文本未在已发布产品中输入。

默认情况下，产品属性中添加的说明和帮助文本不会在已发布产品中显示或输入。 此为有意行为。

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a>输入的默认数量在从物料清单注册与从物料清单版本注册时不同。

### <a name="issue-description"></a>问题描述

默认情况下，将物料添加到物料清单时，数量设置为 1，而不是所选产品的 **默认订单设置** 页上 **最小订单数量** 字段中定义的数量。 但是，如果您从物料清单版本添加物料，在选择物料和变型时，输入的数量默认会考虑在默认订单设置中为特定维度设置的最小数量。

### <a name="issue-resolution"></a>解决问题

此行为是预期的。 但是，物料清单和物料清单版本中的逻辑不同这一事实是一个已知问题。 不过，此行为不会更改，因为更改可能会影响许多不同的客户场景。

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a>在已发布产品详细信息中，我无法更改从产品文档附件数据实体上载的附件图像。

### <a name="issue-description"></a>问题描述

当您使用 *产品文档附件* 数据实体在物料中附加图像时，可能会发生此问题。 在这种情况下，将为物料显示物料图像。 但是，如果您选择 **更改图像**，上载的图像列表中不会显示任何内容。 而且，不会为物料显示附件。

### <a name="issue-resolution"></a>解决问题

*EcoResProductDocumentAttachmentEntity* 实体（*产品文档附件*）导入 *产品* 的文档附件，但不能导入 *已发布产品* 的文档附件。 （已发布产品也称为 *物料*。）要在 **已发布产品详细信息** 页上查看物料的附件，您必须改为使用 *EcoResReleasedProductDocumentAttachmentEntity* 实体（*已发布产品文档附件*）。

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a>Microsoft Flow 连接器显示以下错误消息：“不允许更新字段‘ProductNumber’。”

### <a name="issue-description"></a>问题描述

如果您尝试使用 *已发布产品* 实体 V2 和 Microsoft Flow 更新 **产品编号** 字段，会出现此问题。

### <a name="issue-resolution"></a>解决问题

此行为是预期的。 已发布产品的产品编号编辑功能在带平台更新 24 的 Dynamics 365 Finance and Operations 10.0.0 中已移除，以帮助防止数据损坏。 在特殊情况下，您必须修复由于之前对已发布产品的主键进行重命名而导致的数据损坏时，您可以让 Microsoft 支持部门临时移除此限制。

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a>我无法在另一个法人中创建已发布产品变型。

### <a name="issue-description"></a>问题描述

如果您尝试发布没有变型的基础产品，然后根据需要在每个法人（公司）中创建变型，您将无法使用变型建议来发布变型。 您也将无法手动创建变型。

### <a name="issue-resolution"></a>解决问题

此为有意行为。 基础产品的关系和基础产品可以采用的维度在共享级别保留。 因此，您无法在发布这些维度的特定法人中为共享基础产品创建可用维度，然后在需要这些维度的每个法人中复制流程。 而是必须更改发布流程以适应设计的流程。

这里是发布产品的流程。

1. 创建共享基础产品以及可以发布给法人的维度。
1. 使用变型建议或通过手动添加应该发布的组合，将产品发布到法人。

或者，您可以直接创建已发布产品。

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a>我在另一个公司发布变型时收到以下错误消息：“具有指定维度的产品变型已创建。”

### <a name="issue-description"></a>问题描述

如果某个产品变型已经在公司 A 中发布，当您尝试使用 **已发布产品变型** 页上的 **新建** 按钮在公司 B 中发布该变型时，会收到以下错误消息：

> 已创建具有指定维度的产品变型。

### <a name="issue-resolution"></a>解决问题

**已发布产品变型** 页上的 **新建** 按钮在公司上下文中创建变型并发布。 如果变型已创建，则无法使用 **新建** 按钮将其发布到另一个公司。

要解决此问题，请打开 **基础产品** 页，选择 **发布产品** 在所需公司中发布现有变型。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]