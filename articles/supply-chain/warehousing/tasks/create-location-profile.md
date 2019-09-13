---
title: 创建库位模板
description: 本主题说明如何在 Dynamics 365 for Finance and Operations 中创建库位模板。
author: ShylaThompson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46aa1001c21ae39c158062444303ca02c0f41a45
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/08/2019
ms.locfileid: "1866971"
---
# <a name="create-a-location-profile"></a>创建库位模板

[!include [task guide banner](../../includes/task-guide-banner.md)]

本主题说明如何在 Dynamics 365 for Finance and Operations 中创建库位模板。 仓库中的每个库位都需要关联一个库位模板，用于描述库位的属性，例如，库位是否允许混合物料。 在此过程中，我们将为不需要牌照控制的库位创建模板。 我们将启用混合物料和混合库存状态，并允许周期盘点。 您可以在 USMF 演示数据公司中使用此过程。


1. 在导航窗格中，转到**模块 > 仓库管理 > 设置 > 仓库 > 库位模板**。
2. 选择**新建**。
3. 在**库位模板 ID** 字段中，键入一个值。
4. 在**名称**字段中，键入一个值。
5. 在**位置格式**字段中，输入或选择一个值。
6. 在**位置类型**字段中，输入或选择一个值。
7. 在**码头管理模板 ID** 字段中，输入或选择一个值。
8. 选择**允许混合物料**字段中的**是**。
9. 选择**允许混合库存状态**字段中的**是**。
10. 在**允许周期盘点**字段中选择**是**。
11. 选择**保存**。

