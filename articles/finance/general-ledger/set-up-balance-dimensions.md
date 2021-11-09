---
title: 如何设置平衡财务维度？
description: 本主题介绍用于设置和使用平衡财务维度的选项。
author: kweekley
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-08-17
ms.dyn365.ops.version: 10.0.210
ms.openlocfilehash: 188c15c4cb0c295a9fcbb08273ddb391fbc29e24
ms.sourcegitcommit: b4c78655f2ab4b0e7ead96dfb9cf087a18014253
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/02/2021
ms.locfileid: "7468932"
---
# <a name="how-do-i-set-up-balancing-financial-dimensions"></a>如何设置平衡财务维度？

[!include [banner](../includes/banner.md)]

本主题介绍用于设置和使用平衡财务维度的选项。

## <a name="symptom"></a>问题

可以选择两种方法设置平衡财务维度。 第一种选择是使用 **分类帐** 页面（**总帐 \> 分类帐设置 \> 分类帐**）中的 **平衡财务维度** 字段。 第二种选择是使用 **财务维度** 页面（**总帐 > 会计科目表 \> 维度 \> 财务维度**）中的 **要求维度平衡** 选项。 本主题介绍这两种选择之间的区别。

## <a name="resolution"></a>解决方法

组织通常使用平衡维度生成在财务维度级别平衡的资产负债表。 启用这些功能不会将已过帐的未平衡维度导入到余额中。 在其中这些功能之前，必须先手动输入调整条目，以便将资产负债表导入余额中。

这两种选择彼此排斥。 组织使用的选择应该基于业务要求。 我们经常听说客户同时在日记帐设置和财务维度设置中定义平衡维度，然后完成所需部分或全部额外设置。 但是，由于财务维度级别不平衡，他们还是不能过帐。

以下部分描述这两种选择及其设置方法。

### <a name="ledger--balancing-financial-dimension"></a>分类帐 - 平衡财务维度

**分类帐** 设置页中的平衡维度用于启用单位间核算。 若要开启此功能，请执行以下步骤。

1. 确定哪个财务维度将充当平衡维度。

    - 此功能仅允许您选择一个财务维度充当平衡维度。
    - 尚未在 **分类帐** 设置页中选择维度。
    - 请确保所选财务维度的资产负债表已平衡。

2. 更新平衡财务维度的科目结构。

    - 分配给分类帐的所有科目结构中都必须包含此平衡财务维度。
    - 财务维度不得允许科目结构中有空白。 此项限制可以确保过帐到总帐的每个会计条目中都包含财务维度值。 如果使用平衡维度，则空白维度无效。

3. 在 **自动交易科目** 页面（**总帐 \> 过帐设置 \> 自动交易科目**）中，定义单位间借方和贷方主科目。
4. 在 **分类帐** 设置页（**总帐 \> 分类帐设置 \> 分类帐**）的 **平衡财务维度** 字段中，选择用于平衡的财务维度。

如果因为输入和过帐了交易记录，导致所选财务维度不平衡，系统将自动添加在过帐期间用于平衡会计条目的借方或贷方条目。 将在总帐中过帐的凭证中显示单位间交易记录的借方和贷方分类帐科目。 但是，不会在为其过帐了会计条目的日记帐或源单据中显示这些科目。

### <a name="financial-dimensions--require-the-dimension-to-be-balanced"></a>财务维度 - 需要平衡维度

虽然 **财务维度** 页中的平衡维度通常由公共部门公司使用，此功能却不链接到任何公共部门 Configuration Key。 由于系统中无限制，因此即使您的组织不是公共部门实体，也可以使用此功能。

此功能通常在公共部门客户群中使用，因为它要求使用过帐定义自动平衡每个交易记录。 其不使用在 **自动交易科目** 页面中定义的单位间借方和贷方科目自动平衡会计条目。 如果应用过帐定义之后，某个会计条目在维度级别不平衡，将不过帐交易记录，即使定义了单位间借方和贷方科目。

我们经常听说客户同时在日记帐设置和财务维度设置中定义平衡维度。 在此情况下，系统将使用财务维度功能。 过帐期间，优先设置财务维度级别的平衡维度。 如果过帐定义不创建财务维度级别的平衡会计条目，过帐将失败。

若要开启财务维度级别的平衡维度使用，请执行以下步骤。

1. 确定哪些财务维度将充当平衡维度。

    - 可以将多个财务维度设置为平衡维度。
    - 尚未在 **财务维度** 页中设置平衡交易记录所需财务维度。

2. 定义组织所用各种日记帐或源单据的过帐定义。 过帐定义将未过帐日记帐或源单据中的会计科目用作“匹配条件”。 然后，过帐定义返回将成为会计条目的“生成的条目”。 如果正确设置了过帐定义，则生成的条目中将包含匹配条件分类帐科目，以及更多用于在维度级别平衡会计条目的科目。 有关详细信息，请参阅[过帐定义](posting-definitions.md)。 
   
   并非每种交易记录都支持过帐定义。 例如，不能为通过总帐或固定资产日记帐输入的任何交易记录定义过帐定义。 如果不能为日记帐或源单据定义过帐定义，则必须使用财务维度值手动平衡交易记录。 例如，如果创建了总帐条目，并且“部门”维度为平衡维度，则必须确保每个部门值都平衡。  如果该维度对每个部门值都不平衡，将不过帐凭证，直到通过向凭证手动添加单位间借方或贷方更正了不平衡。 

    > [!IMPORTANT]
    > 如果必须手动平衡过多交易记录，则 **不** 应在 **财务维度** 页中使用平衡维度功能。 请改为在 **分类帐** 设置页中使用平衡维度功能。

3. 定义过帐定义之后，可以将财务维度标记为平衡必需。

在输入和过帐交易记录时，过帐期间将调用过帐定义以确定会计条目。 如果财务维度已平衡，则会在确定了会计条目之后进行验证。 如果财务维度未平衡，则不过帐交易记录，而您会收到一条消息，说明特定维度的借项与贷项不相等。