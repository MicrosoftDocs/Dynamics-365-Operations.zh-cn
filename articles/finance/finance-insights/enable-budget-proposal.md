---
title: 启用预算提案（预览）
description: 本主题说明如何在 Finance Insights 中开启预算提案功能。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 59cf40e8bf69734c5f3645997ff0b07c29d4f40e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995132"
---
# <a name="enable-budget-proposals-preview"></a>启用预算提案（预览）

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

本主题说明如何在 Finance Insights 中开启预算提案功能。

1. 按照 Microsoft Dynamics Lifecycle Services (LCS) 中环境页面内的信息连接到该环境的 Azure SQL 主实例。 运行以下 Transact-SQL (T-SQL) 命令为沙盒环境开启外部测试版。 （可能必须先在 LCS 中为 IP 地址开启访问权限，才能远程连接到应用程序对象服务器 \[AOS\]。）

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > 如果您的 Microsoft Dynamics 365 Finance 部署是 Service Fabric 部署，则可跳过此步骤。 Finance Insights 团队应该已经为您开启了外部测试版。 如果在 **功能管理** 工作区中未看到此功能，或者在尝试开启时遇到问题，请向 [Finance Insights App Preview 团队](mailto:fiap@microsoft.com)发送电子邮件。

2. 打开 **功能管理** 工作区，然后执行以下步骤：

    1. 选择 **检查更新**。
    2. 搜索 **预算提案**，然后启用该功能。

3. 转到 **预算 \> 设置 \> 基本预算 \> 预算提案(预览)**，然后选择 **启用功能**。

#### <a name="privacy-notice"></a>隐私声明
预览版 (1) 采用的隐私和安全措施可能比 Dynamics 365 Finance and Operations 服务少，(2) 不包含在该服务的服务级别协议 (SLA) 中，(3) 不应用于处理应遵守法律或法规合规性要求的个人数据或其他数据，以及 (4) 享受有限支持。
