---
title: 财务维度集
description: 本主题介绍了财务维度集并提供一些优化其用法的提示。
author: yukonpeegs
ms.date: 03/07/2022
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 9274e7f85005ab27d9f2b35fbb0be42e216941c9
ms.sourcegitcommit: 411874545d7c326fc4aa877948a059371f0ccb3c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/07/2022
ms.locfileid: "8392928"
---
# <a name="financial-dimension-sets"></a>财务维度集

[!include [banner](../includes/banner.md)]

本主题介绍了财务维度集并提供一些优化其用法的提示。

维度集是财务维度的已排序列表，可用于以用户定义的方式汇总总帐数据。 维度集的主要用途是定义试算平衡表。

唯一的标准维度集是仅包含主科目的维度集。

使用 **财务维度集** 页面创建和管理财务维度集。

## <a name="dimension-set-balances"></a>维度集平衡表

维度集可以具有基于其财务维度的平衡表。 平衡表存在于总帐中，并且基于维集集定义。 汇总总帐数据中的平衡表以帮助在检索平衡表时（例如，当生成试算平衡表时）提高性能。

## <a name="create-balances"></a>创建余额

使用 **创建平衡表** 按钮初始化当前没有平衡表的维度集的平衡表。

> [!NOTE]
> 我们建议您限制具有平衡表的维度集的数量，因为平衡表更新会影响所有总帐过帐活动。

## <a name="update-balances"></a>更新余额

使用 **更新平衡表** 按钮将最新的总帐过帐活动包括在平衡表中。 平衡表更新是简单的操作。 它们必须仅处理自上次更新以来发生的总帐过帐活动。

> [!NOTE]
> 显示试算平衡表会强制进行更新，以确保显示的平衡表是最新的。 考虑使用定期批处理作业，以便快速更新最常用的维度集。 通过这种方式，您可以最大程度地减少试用平衡表用户必须等待的时间。

## <a name="rebuild-balances"></a>重建余额

使用 **重建平衡表** 按钮从头开始重新创建平衡表。 通过这种方式，您可以帮助确保它们与总帐中的数据匹配。 重建平衡表需要大量处理，通常不需要这样做。

> [!NOTE]
> 如果您有需要定期重建平衡表的场景，我们建议您与客户支持联系。 客户支持可以帮助您确定为什么平衡表与总帐中的数据不匹配。

## <a name="clear-balances"></a>结算余额

使用 **清除平衡表** 按钮删除平衡表并停止任何进一步更新。 维度集将不再对总帐过帐活动产生影响。

## <a name="delete-a-dimension-set"></a>删除维度集

无论采用任何解决方法来解决特定维度集的余额数据的潜在问题，请勿 **删除并重新创建** 维度集。 重新创建维度集成本高昂。 有关问题的进一步帮助，请与客户支持联系。 


有关详细信息，请参阅[财务维度](financial-dimensions.md)。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
