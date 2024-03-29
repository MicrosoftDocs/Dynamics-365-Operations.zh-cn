---
title: 财务维度
description: 本文介绍财务维度的不同类型以及如何设置。
author: aprilolson
ms.date: 03/07/2022
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: adfa2c1164550e32b07da25de0d96aa82430b980
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799618"
---
# <a name="financial-dimensions"></a>财务维度

[!include [banner](../includes/banner.md)]

本文说明财务维度的不同类型以及如何设置。

使用 **财务维度** 页可创建可用作会计科目表的科目段的财务维度。 有两类财务维度：自定义维度和实体支持的维度。 自定义维度在法人之间共享，并且值由用户输入和维护。 对于实体支持的维度，其值在系统的其他地方进行定义，如客户或商店实体中。 有些实体支持的维度在法人间共享，而有些实体支持的维度则特定于公司。

在您创建了财务维度之后，使用 **财务维度值** 页给每个财务维度分配附加属性。

您可以使用财务维度代表法人。 您不必在 Dynamics 365 Finance 中创建实体。 但是，财务维度不用来解决法人的运营或业务需求。 将 Finance 中的单位间核算功能设计成仅满足由每个交易记录创建的会计条目。

在将财务维度设置为法人之前，评估您的业务流程中的以下区域以确定此设置是否适用于您的组织：

- 库存
- 财务维度和法人之间的销售和采购
- 计算和申报销售税
- 操作报告

这是一些限制：

- 您只可以以法人身份使用销售纳税仅功能，但是不可以凭财务维度使用此功能。
- 有些报表不包括财务维度。 因此，要按财务维度进行报告，您可能必须修改报表。

## <a name="custom-dimensions"></a>自定义维度

若要创建用户定义的财务维度，在 **使用以下来源中的值** 字段中，选择 **自定义维度**。

您还可以指定科目掩码以限制您为维度值输入的金额和信息类型。 您可以输入保持不变的每个维度值的信息，例如字母或连字符 (-)。 还可以输入数字标志 (\#) 和和符号 (&) 作为每次要更改的字符的占位符创建维度值。 使用一个数字标志 (\#) 作为编号占位符和符号 (&) 作为信函的占位符。 只有在 **使用以下来源中的值** 字段中选择 **自定义维度** 后，用于格式掩码的字段才可用。

**示例**

若要限制维度值到“CC”和三个数字，输入 **CC-\#\#\#** 作为格式掩码。

## <a name="entity-backed-dimensions"></a>实体支持的维度

若要创建实体支持的财务维度，在 **使用以下来源中的值** 字段中，选择财务维度所基于的系统定义的实体。 随后将从此实体创建财务维度值。 例如，要为项目创建维度值，请选择 **项目**。 将为每个项目名称将创建维度值。 **财务维度值** 页显示实体的值。 如果这些值是公司特定的，则页面上还显示公司。

## <a name="activating-dimensions"></a>激活维度

在您启用财务维度时，表进行更新，使其包含财务维度的名称。 删除被移除的维度。 启用财务维度前，您可以输入维度值。 不过，在启用财务维度前，无法在任何地方使用财务维度。 例如，到启用财务维度以前，您不能将财务维度添加到科目结构。 在您选择 **启用** 后，所有维度更新并显示状态更改。

## <a name="translations"></a>翻译

在 **文本翻译** 页，可为所选财务维度输入不同语言的文本。 在 **主科目翻译** 页，可为主科目输入不同语言的文本。 

## <a name="legal-entity-overrides"></a>法人覆盖

并非所有的维度都对所有法人有效。 此外，某些维度可能仅针对特定的期间有关。 在这些情况下，您可以使用 **法人覆盖** 部分指定将为其暂停维度的公司、所有者以及维度有效的期间。

## <a name="deleting-financial-dimensions"></a>删除财务维度

为了帮助维护数据的引用完整性，很少删除财务维度。 如果要删除财务维度，则评估以下条件：

- 财务维度是否在已过帐或未过帐的交易记录上或任何类型的维度值组合中使用？
- 财务维度是否在任何活动的科目结构、高级规则结构或财务维度集中使用？
- 财务维度是否是默认维度集成格式的一部分？
- 财务维度是否已设置为默认维度？
- 是否已从 Financial Reporting 设置中取消选择了财务维度？ 

如果满足任何条件，则不能删除财务维度。

> [!NOTE]
> 从 Finance 版本 10.0.27 开始，在创建财务维度时，将不再自动选择财务维度以进行财务报告设置。

## <a name="default-dimension-values"></a>默认维度值

可将主记录（如客户和供应商）中的值用作新维度中的缺省值。 创建新维度时，将在这些主记录的维度值中输入主记录 ID。 例如，创建新客户时，将在客户维度中输入客户 ID。 创建销售订单、发票或其他需要客户 ID 的单据时，将使用现有缺省规则，并将客户 ID 添加到单据中。

此功能由维度中的设置控制。 此设置的名称为 **在创建的每个新 DimensionName 上将值复制到此维度**，其中 **DimensionName** 是维度的名称。 默认情况下，已关闭此功能。 但是，随时可以打开。

如果维度已经有记录，打开此功能时，将更新主记录。 但是，不更新现有单据和交易记录。

如果您使用模板创建主记录，请确保主维度的模板值为空。 例如，如果您从模板创建客户，则请确保模板中的客户维度为空。 当您创建新客户时，客户维度值将默认为新客户编号。  

## <a name="derived-dimensions"></a>派生的维度

可配置维度，以便在单据中输入该维度时自动输入其他维度的信息。 例如，如果输入成本中心 10，可能在部门维度中自动输入值 **20**。

可以在维度页中设置派生值。

1. 选择维度，然后选择 **派生维度**。

    **派生维度** 页中有一个网格。 所选维度部分是该网格中的第一个列。

2. 添加应派生的段。 每段显示为一列。

在第一列中输入应从维度派生的维度组合。 例如，要将成本中心用作部门和库位的派生来源，请输入成本中心 10，部门 20 和库位 30。 然后，在主记录中或交易记录页上输入成本中心 10 时，将缺省输入部门 20 和库位 30。

### <a name="overriding-existing-values-with-derived-dimensions"></a>使用派生维度覆盖现有值
 
默认情况下，派生维度过程不会覆盖派生维度的现有值。 例如，如果输入成本中心 10，但不输入其他任何维度，将缺省输入部门 20 和库位 30。 但是，如果更改成本中心，将不更改已建立的值。 因此，可基于主记录建立缺省维度，而派生维度不会更改这些维度。

您可以更改派生维度的行为以通过选择 **派生的维度** 页的 **将现有维度值替换为派生值** 复选框覆盖现有值。 如果选中此字段，您可以输入具有派生的维度值的维度，这些派生的维度值将覆盖已存在的所有值。 使用上一个示例，如果输入成本中心 10，但不输入其他任何维度，将缺省输入部门 20 和库位 30。 但是，如果值已经是部门 50 和库位 60 值，这些值现在将更改为部门 20 和库位 30。
 
具有此设置的派生的维度在维度值是默认值时不会自动替换现有的默认维度值。 只有当您在页面上输入新维度值并且页面上的维度有现有的派生值时，维度值才会被覆盖。

### <a name="preventing-changes-with-derived-dimensions"></a>防止更改派生的维度
 
在您使用 **派生的维度页面** 上的 **添加科目段** 将科目段添加为派生的维度时，将在 **添加科目段** 页面的底部提供一个选项，用于允许您防止维度在页面上派生时被更改。 默认设置是关闭的，因此它不会阻止派生的维度值被更改。 如果您希望阻止维度在派生后被更改，请将此设置更改为 **是**。 例如，如果部门维度的值从成本中心维度值派生，当 **阻止更改** 设置为 **是** 时，部门值将无法更改。 
 
如果维度值有效但未在派生的维度列表中列出，此设置不会阻止更改。 例如，如果部门 20 从成本中心 10 派生，并且您输入了成本中心 10，那么您将无法编辑部门 20。 但是，如果输入成本中心 20，而它不在成本中心派生维度的列表中，那么您可以编辑部门值。 
 
在所有情况下，在应用派生的维度值后，科目值和所有维度值仍会根据科目结构进行验证。 如果您使用派生的维度，而它们在页面上使用时验证失败，那么您必须更改派生的维度值页面上的派生的维度值，然后您才能够在交易记录中使用它们。 
 
在您更改 **财务维度** 快速选项卡上的维度时，标记为阻止更改的维度不可编辑。 如果您在页面上将科目和维度输入 Segmented Entry 控件，维度将可编辑。 但是，在您将突出显示从 Segmented Entry 控件移开，并移至其他字段或执行操作，科目和维度将根据派生的维度和科目结构进行验证，以确保您输入了适当值。 

### <a name="derived-dimensions-and-entities"></a>派生维度和实体

可通过使用实体设置派生维度段和值。

- 派生维度实体设置驱动维度和用于这些维度的段。
- 可通过派生的维度值实体导入应该为每个驱动维度派生的值。

使用实体导入数据时，如果该实体导入维度，则除非实体特意覆盖这些维度，否则导入期间将应用派生维度规则。

## <a name="financial-dimension-service"></a>财务维度服务

财务维度服务加载项在您的 Microsoft Dynamics Lifecycle Services 环境中可用。 当您使用数据管理框架导入具有大量行的日记帐时，它会提供改进的性能。 要使用此服务，您必须在 **财务维度服务参数** 页面启用。 目前，此服务仅适用于 500 行或更多行的导入日记帐。 此外，目前它只能处理在日记帐行上设置了 **分类帐** 科目类型的普通日记帐。 当前不支持日记帐行上的其他科目类型，如 **客户**、**供应商** 和 **银行**。 系统中设置了派生维度时不会调用此服务。

当使用与数据导入并行运行的新服务导入日记帐时，财务维度服务将提供改进的性能。 它仅在日记帐中的主科目和财务维度数据上运行，将生成在日记帐行的分类帐科目字符串字段中指定的维度组合。 处理过程会将此字符串转换为结构化数据存储，财务维度框架在产品的其余部分使用此结构化数据存储进行验证、汇总报告和查询。 有关财务维度数据摘要报告的更多信息，请参阅[财务维度集](financial-dimension-sets.md)。

有关详细信息，请参阅以下主题：

- [定义财务维度](tasks/define-financial-dimensions.md)
- [维护财务维度默认模板](tasks/maintain-financial-dimension-default-templates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
