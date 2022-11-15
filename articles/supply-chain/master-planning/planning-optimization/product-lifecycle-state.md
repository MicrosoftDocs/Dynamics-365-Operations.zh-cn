---
title: 排除具有特定产品生命周期状态的产品
description: 本文介绍如何根据产品的生命周期状态排除产品。
author: t-benebo
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 647e2cf4f14dbdfc3e7f04f43dcbd7115f19e8dc
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740757"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a>排除具有特定产品生命周期状态的产品

[!include [banner](../../includes/banner.md)]

已发布产品和已发布产品版本包括 **产品生命周期状态** 字段。 此字段让您可以控制主计划期间包括哪些产品以及其他一些方面。 您可以转到 **产品信息管理 \> 设置 \> 产品生命周期状态**，根据需要添加、删除和编辑生命周期状态。 对于每个产品生命周期状态，如果在主计划期间应包括具有该状态的产品，则将 **对于计划有效** 选项设置为 *是*。 当此选项设置为 *否* 时，关联的产品和变型将在物料清单 (BOM) 级别从所有主计划和所有计算中排除。

**产品生命周期状态** 字段留为空白的已发布产品和变型，将被作为他们的产品生命周期状态的 **对于计划有效** 选项设置为 *是* 来处理。 换言之，它们将包括在主计划中。

> [!NOTE]
> 为帮助避免不必要的供应建议，我们强烈建议您将所有过时的已发布产品和变型与产品生命周期状态关联，并将 **对于计划有效** 选项设置为 *否*。 当您使用不可重用的产品配置变型时，此方法特别重要，因为它可以帮助防止浪费。

## <a name="related-resources"></a>相关资源

有关产品生命周期状态的详细信息，请参阅[产品生命周期状态概述](../../pim/product-lifecycle.md)。

有关包括使用产品生命周期状态将产品从主计划和物料清单级别计算中排除的步骤的详细信息，请参阅[创建产品生命周期状态以从主计划中排除产品](../../pim/tasks/exclude-products-master-planning.md)。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]