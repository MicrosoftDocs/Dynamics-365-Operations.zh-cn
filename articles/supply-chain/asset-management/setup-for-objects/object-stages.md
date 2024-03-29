---
title: 资产生命周期状态
description: 本文介绍资产管理中的资产生命周期状态和生命周期模型。
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetLifecycleModelStateNext, EntAssetObjectLifecycleState, EntAssetLifecycleStateUpdate, EntAssetObjectLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43b1ff9438437e6c1ff33bab9a7ba0361029cb6d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901051"
---
# <a name="asset-lifecycle-states"></a>资产生命周期状态

[!include [banner](../../includes/banner.md)]

 

本文介绍资产管理中的资产生命周期状态和生命周期模型。 资产生命周期状态用于定义资产有效还是无效。 例如，可将资产生命周期状态设置为 **已创建**、**有效** 和 **已终止**。

> [!NOTE]
> - 请求生命周期状态与资产生命周期状态关联。 因此，如果将请求更改为新的请求生命周期状态，与该请求关联的资产将更改为新的资产生命周期状态。 例如，如果将一个请求的生命周期状态更改为 **入站**，则关联资产的生命周期状态将更改为 **资产生命周期状态模型** 页 **资产生命周期状态** 快速选项卡上 **入站生命周期状态** 字段中选择的生命周期状态。 


可在资产生命周期模型（其中定义各种资产类型需要的生命周期状态）中设置资产生命周期状态。 设置第一个生命周期状态。 然后创建一个生命周期模型，并为该生命周期模型选择这个生命周期状态。

1. 选择 **资产管理** \> **设置** \> **资产** \> **生命周期状态**。
2. 选择 **新建** 以创建新资产生命周期状态。
3. 在 **生命周期状态** 字段中，输入生命周期状态 ID。
4. 在 **名称** 字段中，输入描述。

    **生命周期模型** 字段显示使用此资产生命周期状态的资产生命周期模型的数量。

5. 如果此生命周期状态应该为无效生命周期状态（换句话说，可以为此生命周期状态的资产创建工作订单），请将 **有效** 选项设置为 **是**。
6. 如果应该在处于此生命周期状态时删除资产生命周期状态为 **已创建** 的未结束资产日历行，请将 **删除未结束日历行** 选项设置为 **是**。 如果要清除资产的所有不再相关的未结束维护计划（例如，如果资产不再有效），此设置非常有用。

> [!NOTE]
> 资产生命周期状态、资产生命周期模型和资产类型相互关联。 其使用方法与工作订单生命周期状态、工作订单生命周期模型和工作订单类型的使用方法相同。 


创建所需资产生命周期状态之后，可以在资产生命周期模型中设置生命周期状态。

1. 选择 **资产管理** \> **设置** \> **资产** \> **生命周期模型**。
2. 选择 **新建** 以创建新资产生命周期模型。
3. 在 **生命周期模型** 字段中，输入生命周期模型 ID。
4. 在 **名称** 字段中，输入描述。

    **生命周期状态** 字段显示生命周期模型中选择的资产生命周期状态的数量。 **资产类型** 字段显示使用此生命周期模型的资产类型的数量。

5. 在 **生命周期状态** 快速选项卡上，选择资产生命周期模型中应包含的资产生命周期状态。

    - 若要为模型使用生命周期状态，请在 **其余生命周期状态** 部分中选择它，然后选择向右箭头按钮 ![向右箭头。](media/15-setup-for-objects.png) 以将其移到 **所选生命周期状态** 部分。
    - 若要为模型使用所有可用生命周期状态，请选择 **所有可用生命周期状态** 按钮 ![所有可用生命周期状态。](media/20-setup-for-objects.png)。 将把所有生命周期状态移到 **所选生命周期状态** 部分。
    - 若要从模型中删除生命周期状态，请在 **所选生命周期状态** 部分中选择它，然后选择向左箭头按钮 ![向左箭头。](media/16-setup-for-objects.png) 以将其移到 **其余生命周期状态** 部分。

6. 要定义可采用所选生命周期状态的资产生命周期状态，选择 **生命周期状态更新**。
7. 如果要处理收到待维修的资产，请使用 **资产状态** 快速选项卡。 在 **入站/出站** 部分中，可选择资产生命周期状态以指示收到待维修的资产的工作流。 如果为客户或部门提供出借资产，可在 **借出** 部分中为出借资产选择生命周期状态。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]