---
title: 快照概述（预览）
description: 本主题介绍快照功能，该功能使您可以保存现金流预测以供以后分析或与实际情况进行比较。 生成现金流预测时，可以将该预测另存为“快照”。 然后，您可以使用该快照来编辑预测中包含的科目，或者将快照中的预测与实际值进行比较。
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 23df01603e74847f6f01a1eaa84b8fd3bb1d6e59
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/03/2021
ms.locfileid: "6337199"
---
# <a name="snapshots-overview-preview"></a>快照概述（预览）

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

快照使组织可以编辑和保存有关某个时间点其现金头寸和现金预测的信息。 您可以将快照与实际财务状况进行比较，检查差异，并使用该信息改进随时间变化的现金流预测。 更特别的是，可通过以下方式使用快照：

- 跟踪现金头寸和现金预测。
- 筛选数据以显示为其创建快照的法人的子集。
- 编辑系统生成的现金头寸和现金预测。
- 进行假设分析，以考虑现金流的乐观，悲观和最可能的观点。
- 将实际财务绩效与快照中保存的预测进行比较。

可以通过选择 **现金流预测** 工作区上 **现金头寸** 选项卡或 **现金预测** 选项卡上的 **新建快照** 创建快照。 创建快照后，可以编辑和保存快照中的流入和流出。 **快照** 选项卡中包含所有保存的快照。要打开快照，请选择其名称。

随时可以编辑快照中的现金流入和流出。 编辑流入金额或流出金额时，更新后的金额将按比例分配给创建原始余额的流动性科目中。 快照编辑完毕后，请选择 **保存** 以保存更改。

要比较多个快照，请选择 **比较快照**。 您可以一次比较两个快照。 选择要比较的两个快照，然后选择 **确定**。 **比较快照** 页面将显示所选快照的比较。 页面上部的图表显示了两个快照的重合期间的现金流入、现金流出和银行余额的比较。 下部的网格显示了每个流动性金额的两项预测的详细比较。 网格中的 **差异** 列显示一个期间内余额之间的差异。

要将实际财务结果与保存为快照的预测进行比较，请选择 **与实际值比较**。 **比较快照** 页面将显示实际金额与预测的比较。 页面上部的图表显示了两个快照的重合期间的现金流入、现金流出和银行余额的比较。 下部的网格显示了每个流动性金额的每个期间的实际余额和预测的余额的详细比较。 网格中的 **差异** 列显示一个期间内的实际余额与预测余额之间的差异。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
