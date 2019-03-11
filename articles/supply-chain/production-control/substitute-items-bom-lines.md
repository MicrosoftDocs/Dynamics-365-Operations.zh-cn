---
title: 生产中的物料替换
description: 本主题描述如何在生产流程中替换物料。
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdBOM
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 70171
ms.assetid: ce3b11ef-550e-49b7-8942-2607c2ec3c5c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 461b717acafb5ccf37acae23a1564069cea6828a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "327611"
---
# <a name="material-substitution-in-manufacturing"></a>生产中的物料替换

[!include [banner](../includes/banner.md)]

本主题描述如何在生产流程中替换物料。 

有三种方法可用于在生产流程中替换物料：

-   按照日期，即，在特定日期之后将一个物料替换为另一个物料时
-   在主计划期间，即，因为物料的库存不足，将其替换为不同的物料时
-   在生产期间，即，当物料意外地库存不足并且被替换为不同物料时

## <a name="substituting-material-by-date"></a>按日期替换物料
请考虑以下方案：公司正在制造的机器包含将要在两个月内从供应商的目录到期的组件。 从到期日期开始，供应商将提供可替换旧组件的新组件。 开始日期和结束日期可以在物料清单行上设置。 对于本示例，您通过在**结束日期**字段中输入到期日期将旧组件设置为到期。 然后，在物料清单上，您设置新的替换组件，以便它从旧组件到期那天后生效。 为此，请在**开始日期**字段中输入开始日期。

## <a name="substituting-material-by-planning"></a>按计划替换物料
只有当您使用配方时，而不是当您使用物料清单时，您才可以在计划期间替换物料。 请考虑以下方案：食品制造公司正在根据具有 20 种成分的配方制造调味汁。 配方中的一种成分可由其他两种成分之一替换。 但是，因为这两种成分比首选成分贵，所以只有当这种首选成分的库存不足时，才使用替换。 可以被替换的物料叫做 A，而可以替换它的两个物料叫做 B 和 C。按计划的物料替换是由配方行上的**计划组**和**优先级**字段控制的。 对于本示例，您可为三个物料创建配方行，并将配方行与相同计划组关联。 在设置中，物料 A 的配方行具有最高优先级（编号最小），物料 C 的配方行具有最低优先级，物料 B 的配方行具有介于其他两行的优先级之间的优先级。 如果您对成品有要求，则主计划首先确定是否可以满足物料 A 的需求。 如果无法满足该需求，则主计划按优先级别顺序查看物料 B 和 C。 如果物料 B 是现有库存物料，则在为配方形成计划批次订单后会使用它。 如果这些物料都不是现有库存物料，主计划会为物料 A 创建一个计划订单。**注释：** 当您在计划组中设置配方行时，应仅在具有最高优先级的物料上指定数量。 此数量将用于计算计划中的所有物料的需求，甚至具有更低优先级的物料。 您不能在计划组中的更低优先级物料上指定不同的数量。

## <a name="substituting-material-during-production"></a>在生产期间替换物料
请考虑以下情况：一块金属板是焊接操作所必需的。 在操作期间，仓库工作人员通知机器操作员板子的库存不足。 但是，板子可替换为稍厚的板子是确定无疑的。 这样，操作就可以完成。 物料可以添加到未结生产订单的物料清单中。 如果生产订单具有状态**已开始**，则在用户向生产物料清单中添加新物料时，系统会要求用户重新估计该订单。 在添加物料后，可以为新物料创建新的领料单。 您不必向生产物料清单中添加新的物料。 相反，您可以直接将其添加到生产领料单。 然后，当过帐领料单时，系统会将物料添加到生产物料清单中。



