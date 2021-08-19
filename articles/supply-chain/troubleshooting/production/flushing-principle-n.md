---
title: 未遵从物料清单行上的耗用原则设置
description: 未采用物料清单 (BOM) 行上的耗用原则设置。
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ee40eff53efd920ebe43a7b2dd28129f01e6ebb5e75bd480a91f758529f77fc5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716948"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a>未遵从物料清单行上的耗用原则设置

知识库编号：4612725

## <a name="symptoms"></a>故障特征

当 **生产控制参数** 页的 **自动更新** 选项卡上的 **自动物料清单消耗量** 字段设置为 *耗用原则* 时，会发生此问题。 此设置指示在接收采购订单时所有物料清单 (BOM) 行应自动消耗。 如果物料清单行上的 **耗用原则** 字段明确设置为 *手动*，您可能会预期物料清单行不会自动消耗。 但是，发生此问题时，**耗用原则** 字段设置为 *手动* 的物料清单行还是会自动消耗。

## <a name="resolution"></a>解决方法

如果遇到此问题，可以将生产控制参数设置为替代物料清单行上的 **耗用原则** 设置。 在 **生产控制参数** 页上的 **自动更新** 选项卡上，检查 **自动物料清单消耗量** 字段的值。 如果设置为 *始终*，系统将忽略所有物料清单行上的 **耗用原则** 设置，会始终耗用行。 要让系统遵从物料清单行上的 **耗用原则** 设置，将 **自动物料清单消耗量** 字段的值更改为 *耗用原则*。
