---
title: 公式和公式版本
description: 本文提供有关配方和配方版本的信息。 配方定义流程制造中的特定流程的物料、成分和结果。 配方用于计划和生产流程制造中的产品。
author: johanhoffmann
ms.date: 09/12/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PlanActivity, ReqSupplyDemandSchedule, EcoResProductProdTypeFormulaNoActiveFormulaFormPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 236a283736078e80506a1ecaab53c013a91c3721
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844139"
---
# <a name="formulas-and-formula-versions"></a>配方和配方版本

[!include [banner](../includes/banner.md)]

配方定义流程制造中的特定流程的物料、成分和结果。 配方与相应的工艺路线一起定义流程制造中的整个流程。 配方用于计划和生产流程制造中的产品。

配方由生产特定数量的配方物料所需的成分和数量构成。 根据您执行的任务，可以从“库存和仓库管理”或“产品信息管理”中访问配方功能。

## <a name="formulas-and-formula-lines"></a>配方和配方行
配方由确定组成配方的成分或物料的一个或多个配方行构成。 配方行可以包含物料清单 (BOM) 物料、配方物料、非定重物料、采购的物料、联产品或副产品。 由于许多物料在多个产品中使用，因此一个物料可以在多个配方中使用。

例如巧克力豆饼干的配方。 此配方的成分使用多个行，如面粉、糖、鸡蛋、黄油和巧克力豆。 巧克力豆饼干的配方包含的成分有可能在其他配方中使用。 当您制作巧克力豆饼干时，可能会有剩余物料，如饼干屑，或者有一些饼干可能烘烤过度或烘烤不足。 可以根据生产工序将这些物料设置为联产品或副产品。

当您创建配方行时，使用行类型指示系统在您运行主计划和生产批次订单时如何处理行。 每种行类型都提供不同的结果。 下表介绍可以选择的行类型。 

| 行类型     | 说明  |
|---------------|--------------|
| 项目          | 在物料是从库存中领取的原材料或半成品时，或者在物料是服务时，选择 **物料**。 |
| 虚拟       | 当您想要展开在配方行上包含的任何更低级别的配方物料时，选择 **虚拟**。 当您估算批次订单，且展开配方物料时，构成物料在批次订单上被列为配方行。 此外，相应的工艺路线被添加到生产工艺路线中。 使用当前配置展开配方物料。 使用 **虚拟** 行类型时，可以处理在不同配方级别发生的生产和测量配置。 如果为 **已发布产品详细信息** 页的 **工程师** 快速选项卡上的产品选择 **虚拟**，然后在配方中使用该产品，则配方行的行类型更改为 **虚拟**。 不能为非定重物料或生产类型为 **联产品**、**副产品** 或 **计划物料** 的物料选择 **虚拟**。 |
| 限定供应 | 选择 **限定供应** 为配方行中包含的成分创建批次订单、生产订单、看板、转移单或采购订单。 相关订单基于默认订单设置和成分的生产类型予以确定，并且在您估算批次订单时创建。 为批次订单预留所需的成分数量。 |
| 供应商        | 如果生产流程使用分包商，且您希望为该分包商创建子生产或采购订单，则选择 **供应商**。 必须使用配方物料或服务项创建该分包商执行的服务或工作。 您可以将该物料作为配方行附加到父物料。 工艺路线必须包含分配给转包商的运营资源。 可以使用 **操作号** 将该操作附加到配方行。 字段中），则将自动选中此复选框。 |

## <a name="formula-versions"></a>配方版本
当您创建新配方时，必须先创建配方版本，然后才能添加配方行物料及其特定特性。 每个配方都必须至少有一个版本。 在成功保存了版本记录之后，对配方版本上的 **审核** 按钮将可用。 每个配方版本记录与一个或多个可以在生产成品时的联产品和副产品相关联。 许多产品可由不同的批次规模、倍数或使用多个不同产出中相同的成分产出。 您可以创建所需数量的配方版本。

若要管理多个有效配方版本，则使用有效日期范围或“起始”数量字段。 仅当日期范围和“起始”数量不重叠时，才能存在多个有效配方版本。

与 BOM 不同，一个 BOM 通常与许多 BOM 版本相关联，但每个配方通常只存在一个配方版本。 记住，只能为一个给定产品的覆盖范围维度和数量启用一个配方版本。 但是，可能因为其他原因存在许多配方版本，当您创建批次订单时，您可以手动选择它们。

## <a name="approve-and-activate-formulas-and-formula-versions"></a>审核和启用配方和配方版本
配方和配方版本在用于计划和生产之前必须已经过审核。 配方通常在使用前启用。 但是，在生产期间，可以选择已审核的配方版本，但该版本未启用。

为了帮助获得配方或配方版本，您可以在 **生产控制参数** 页上设置 **锁定编辑** 和 **锁定审核删除** 参数。

如果您选择 **锁定编辑**，并且配方已审核，配方行的字段不能删除或编辑。 但是，如果您撤销对配方的审核，您则可以修改和删除配方行。 您还可以创建新的配方和新的配方版本。

如果您选择 **锁定审核删除**，则不能删除已审核的配方或配方版本的审核。 但是，您可以创建新的配方和新的配方版本，并且您可以删除配方版本的开始日期。

通过使用电子签名功能，您可以添加更多的控制级别。 当用户设置为要求在审核配方时进行电子签名，则当启用配方时会显示 **签名** 页。 用户必须获得授权才能进行电子签名，并且在提交更改前必须成功验证证书。 如果无法对签名进行身份验证，则会拒绝审核或审核删除，并会使启动审核或审核删除的更改返回原始状态。

## <a name="use-the-scalable-feature"></a>使用可扩展的功能
只有在配方中的所有物料构成设置为 **可变消耗** 时，可扩展字段才可用。 如果物料构成设置为 **固定消耗量** 或 **步骤消耗量**，则此功能不可用。 使用可扩展功能时，如果您更改配方中的成分，则您选择的其他成分的数量会进行调整。 还调整配方的范围。 同样，如果您更改配方大小，则所有可扩展成分的数量都会更改。 此功能专门用于创建和维护配方。 它并不指示批次订单上的成分的数量是否会按比例增加或减少。

## <a name="use-step-consumption"></a>使用步骤消耗量
步骤消耗量清除必须在 **配方行** 选项卡上输入成分数量的要求。 相反，将步骤消耗量配置为具有 **开始系列** 值和 **数量** 值。 从每系列记录的步骤消耗量选择满足批次订单上的数量的信息。 当消耗率与批次订单的大小不呈线性关系且仅增加满足特定数量阈值的要求时，步骤消耗量非常有用。 若要对新配方启用此功能，在 **消耗计算** 组下，将适用成分的配方设置从 **标准** 更改为 **步骤**。 在 **配方行** 页的 **设置** 选项卡上指定此工作量法。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]