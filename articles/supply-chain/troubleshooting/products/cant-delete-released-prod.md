---
title: 无法删除已发布的产品
description: 仅当发布的产品没有任何相关交易时，才能删除发布的产品及其所有变型。
author: SmithaNataraj
ms.date: 06/11/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2f03d45a36401314a4b02ff354fabb474568c48b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475720"
---
# <a name="you-cant-delete-a-released-product"></a>无法删除已发布的产品

## <a name="symptoms"></a>故障特征

仅当发布的产品没有任何相关交易时，才能删除发布的产品及其所有变型。

## <a name="resolution"></a>解决方法

请按照以下步骤删除已发布的产品或基础产品。

1. 关闭物料的所有未结交易。
1. 将库存减少到 0（零）。
1. 执行库存结转。
1. 删除要删除的基础产品的所有产品变型。
