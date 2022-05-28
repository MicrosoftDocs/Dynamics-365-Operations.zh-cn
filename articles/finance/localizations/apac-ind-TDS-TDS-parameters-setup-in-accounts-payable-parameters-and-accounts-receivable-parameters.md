---
title: 在应付帐款和应收帐款中设置 TDS 参数
description: 本主题说明如何在应付帐款和应收帐款中设置参数以支持从源扣缴税款 (TDS) 扣除。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: d2cb434346dbbe5487522fe9f7110716c3a8c761
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725140"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a>在应付帐款和应收帐款中设置 TDS 参数

[!include [banner](../includes/banner.md)]

本主题说明如何在应付帐款和应收帐款中设置参数以支持从源扣缴税款 (TDS) 扣除。

1. 转到 **税务 \> 设置 \> 参数 \> 应收帐款参数**。
2. 在 **更新** 选项卡上，选择 **更新订单行** 以打开 **更新订单行** 对话框。
3. 在 **TDS 组** 部分的 **更新 TDS 组** 字段中，指定用于在行级别更新 TDS 组的方法。 在订单头上更新 TDS 组时，将使用此设置。 选项如下：

    - **从不** – 当在订单头上更新 TDS 组时，不在订单行上更新它。
    - **始终** – 当在订单头上更新 TDS 组时，将在订单行上自动更新它。
    - **提示** – 用户收到一条消息，提示他们在订单行上更新 TDS 组。
4. 选择 **确定**。

    [![更新订单行对话框。](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)

5. 转到 **税务 \> 设置 \> 参数 \> 应付帐款参数**。
6. 在 **常规** 选项卡的 **基于交货信息拆分** 快速选项卡上，将 **产品收据** 设置为 **是**，以过帐和拆分具有不同交货地址和税务帐号 (TAN) 的产品收据。 如果此选项设置为 **否**，则不能过帐具有不同交货地址和 TAN 的采购装箱单。
7. 将 **发票** 选项设置为 **是**，以过帐和拆分具有不同交货地址和 TAN 的采购发票。

    [![基于交货信息拆分快速选项卡。](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)

8. 关闭该页面。
