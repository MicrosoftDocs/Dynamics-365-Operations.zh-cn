---
title: 启用现金流预测
description: 本主题说明如何在 Finance Insights 中开启现金流预测功能。
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: cfcdbe76d640d1786b4622febf9157f5fb1c42f9
ms.sourcegitcommit: 133aa728b8a795eaeaef22544f76478da2bd1df9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/13/2022
ms.locfileid: "7969129"
---
# <a name="enable-cash-flow-forecasting"></a>启用现金流预测

[!include [banner](../includes/banner.md)]

本主题说明如何在 Finance Insights 中开启现金流预测功能。

> [!NOTE]
> 若要在现金流中使用付款预测，您必须按照[启用客户付款预测](enable-cust-paymnt-prediction.md)中的说明设置客户付款预测功能。
  
1. 打开 **功能管理** 工作区，然后执行以下步骤：

    1. 选择 **检查更新**。
    2. 在 **所有** 选项卡上，搜索 **现金流预测**。 如果您没有找到该功能，搜索 **（预览）现金流预测**。 
    3. 启用此功能。

2. 转到 **现金和银行管理 \> 现金流与预测设置**，然后添加预测中应该包含的流动性科目。 另外在 **应收帐款** 和 **应付帐款** 选项卡上设置用于付款的流动性帐户。 请务必重新计算现金流预测。

    > [!NOTE]
    > 如果未设置流动性科目，则无法产生现金流。
    >
    > 有关如何设置现金流预测的详细信息，请参阅[现金流预测](../cash-bank-management/cash-flow-forecasting.md)。

3. 转到 **现金和银行管理 \> 设置 \> Finance Insights（预览）\> 现金流预测（预览）**，然后执行以下步骤：

    1. 在 **现金流预测** 选项卡上，选择 **启用功能**。
    2. 选择 **创建预测模型**。

有关现金流预测功能的详细信息，请参阅[现金流预测](cash-flow-forecast-intro.md)。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
