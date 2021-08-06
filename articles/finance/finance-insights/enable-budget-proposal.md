---
title: 启用预算提案（预览）
description: 本主题说明如何在 Finance Insights 中开启预算提案功能。
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
ms.openlocfilehash: d3fac4cbb80493c7cf94e3d9f4a4f544a749fb64
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638601"
---
# <a name="enable-budget-proposals-preview"></a>启用预算提案（预览）

[!include [banner](../includes/banner.md)]

本主题说明如何在 Finance Insights 中开启预算提案功能。

1. 按照 Microsoft Dynamics Lifecycle Services (LCS) 中环境页面内的信息连接到该环境的 Azure SQL 主实例。 运行以下 Transact-SQL (T-SQL) 命令为沙盒环境开启外部测试版。 （可能必须先在 LCS 中为 IP 地址开启访问权限，才能远程连接到应用程序对象服务器 \[AOS\]。）

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > 如果您使用的是 10.0.20 或更高版本，或者如果您使用的是 Service Fabric 部署，请跳过此步骤。 Finance Insights 团队应该已经为您开启了外部测试版。 如果在 **功能管理** 工作区中看不到此功能，或者如果在尝试打开该功能时遇到问题，请联系 <fiap@microsoft.com>。

2. 打开 **功能管理** 工作区，然后执行以下步骤：

    1. 选择 **检查更新**。
    2. 搜索 **预算提案**，然后启用该功能。

3. 转到 **预算 \> 设置 \> 基本预算 \> 预算提案(预览)**，然后选择 **启用功能**。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
