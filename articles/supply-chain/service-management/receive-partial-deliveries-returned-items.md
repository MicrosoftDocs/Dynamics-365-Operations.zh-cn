---
title: 接收退回物料的部分交货
description: 部分交货根据退货单行（而非退货单装运）定义。
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cff714de8b06142fe4c6911db110d707ba7f86584793c73fa54dddf23498f41
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721215"
---
# <a name="receive-partial-deliveries-of-returned-items"></a>接收退回物料的部分交货    

[!include [banner](../includes/banner.md)]


部分交货根据退货单行（而非退货单装运）定义。

这意味着如果您收到在一个退货单行上指示的完整数量、但在退货单的其他行中未指示任何数量，则该交货不是部分交货。 但是，如果某一退货单行要求退回 10 个单位的特定物料，但您只收到四个单位，则该交货是部分交货。

如果退货装运包含的数量少于退货单行的完整数量，则您可以暂不考虑该装运，并且等待其余退回数量到达，或者您可以登记和过帐部分数量。

## <a name="register-and-post-a-partial-quantity"></a>登记和过帐部分数量

1.  在 **到达概览 - 仓库: %1、码头: %2、日记帐名称: %3** 窗体中为到达选择退货单后，单击 **开始到达** 创建到达日记帐，然后单击 **日记帐** \> **显示收货的到达** 打开 **库位日记帐** 窗体。

2.  选择您要处理的日志行，然后单击 **行** 以打开 **日记帐行，库位** 窗体。

3.  选择只有部分数量到达的物料编号的行，然后单击 **功能** \> **拆分** 以打开 **拆分** 窗体。

4.  在 **待拆分数量** 字段中，输入已收到的物料的总数量，然后单击 **确定**。

5.  在 **日记帐行，库位** 窗体上，选择已到达的物料数量的行，然后单击 **过帐**。 您可以在物料已到达后过帐额外的数量行。






[!INCLUDE[footer-include](../../includes/footer-banner.md)]