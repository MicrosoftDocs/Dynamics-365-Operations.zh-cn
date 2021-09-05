---
title: 启用现金流预测
description: 本主题说明如何在 Finance Insights 中开启现金流预测功能。
author: ShivamPandey-msft
ms.date: 07/16/2021
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
ms.openlocfilehash: b5e54772b132b4098df8259e954a484a0838ee38
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386703"
---
# <a name="enable-cash-flow-forecasting"></a>启用现金流预测

[!include [banner](../includes/banner.md)]

本主题说明如何在 Finance Insights 中开启现金流预测功能。

> [!NOTE]
> 若要在现金流中使用付款预测，您必须按照[启用客户付款预测](enable-cust-paymnt-prediction.md)中的说明设置客户付款预测功能。

1. 按照 Microsoft Dynamics Lifecycle Services (LCS) 中环境页面内的信息连接到该环境的 Azure SQL 主实例。 运行以下 Transact-SQL (T-SQL) 命令为沙盒环境开启外部测试版。 （可能必须先在 LCS 中为 IP 地址开启访问权限，才能远程连接到应用程序对象服务器 \[AOS\]。）

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > 如果您使用的是 10.0.20 或更高版本，或者如果您使用的是 Service Fabric 部署，请跳过此步骤。 Finance Insights 团队应该已经为您开启了外部测试版。 如果在 **功能管理** 工作区中看不到此功能，或者如果在尝试打开该功能时遇到问题，请联系 <fiap@microsoft.com>。
  
2. 打开 **功能管理** 工作区，然后执行以下步骤：

    1. 选择 **检查更新**。
    2. 开启以下功能：

        - 新建网格控件
        - 在网格中分组（预览） 
        - 客户付款预测(预览版)
        - 现金流量预测(预览版)

3. 转到 **现金和银行管理 \> 现金流与预测设置**，然后添加预测中应该包含的流动性科目。

    > [!NOTE]
    > 如果未设置流动性科目，则无法产生现金流。

4. 转到 **现金和银行管理 \> 设置 \> Finance Insights（预览）\> 现金流预测（预览）**，然后执行以下步骤：

    1. 在 **现金流预测** 选项卡上，选择 **启用功能**。
    2. 选择 **创建预测模型**。

有关现金流预测功能的详细信息，请参阅[现金流预测](cash-flow-forecast-intro.md)。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
