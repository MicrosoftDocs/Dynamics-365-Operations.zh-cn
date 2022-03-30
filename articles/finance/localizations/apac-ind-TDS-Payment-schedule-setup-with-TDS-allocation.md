---
title: 设置包含 TDS 分配的付款计划
description: 本主题说明如何设置包含从源扣缴税款 (TDS) 分配的付款计划。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 31ecf2e6fa4d3d37c3d5332dc1d5592bf1a99bad
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/12/2022
ms.locfileid: "8408082"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a>设置包含 TDS 分配的付款计划

[!include [banner](../includes/banner.md)]

本主题说明如何设置包含从源扣缴税款 (TDS) 分配的付款计划。

1. 转到 **应付帐款 \> 付款设置 \> 付款计划**。

    [![付款计划页面。](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)

2. 在操作窗格上，选择 **新建** 以创建付款计划，然后输入所需的详细信息。
3. 在 **分配** 字段中，选择要用于为付款计划分配付款的方法。

    - 合计
    - 固定金额
    - 固定数量
    - 指定

    **预缴税金分配** 字段显示付款计划的 TDS 分配方法。 如果在 **分配** 字段中选择 **合计**，**预缴税金分配** 字段将自动设置为 **合计**。 如果在 **分配** 字段中选择 **固定金额**、**固定数量** 或 **指定**，**预缴税金分配** 字段将自动设置为 **按比例**。

    > [!NOTE]
    > 如果 **预缴税金分配** 字段设置为 **合计**，将基于包括 TDS 金额的总额计算分期付款。 如果 **预缴税金分配** 字段设置为 **按比例**，将基于扣除 TDS 金额后的净发票金额计算分期付款。

4. 输入其他所需的详细信息，然后关闭页面。
