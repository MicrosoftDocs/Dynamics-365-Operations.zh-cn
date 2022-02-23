---
title: 负荷模板
description: 本主题介绍如何设置负荷模板以及如何将负荷模板与新负荷关联。
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1ea7f5244b483a1b9d6c55227c676a3878a71d83
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646364"
---
# <a name="load-templates"></a>负荷模板

创建新负荷时，您可以分配负荷模板。 负荷模板包含有关设备以及度量（例如负荷的高度、宽度、深度和体积）的信息。

本主题介绍如何设置负荷模板以及如何将负荷模板与新负荷关联。

## <a name="set-up-a-load-template"></a>设置负荷模板

1. 转到 **运输管理 \> 设置 \> 负荷构建 \> 负荷模板**。
1. 在操作窗格上，选择 **新建** 以添加新模板，或选择 **编辑** 以编辑现有模板。
1. 在新模板或现有模板的行中，设置以下字段：

    - **负荷模板 ID** – 输入负荷模板的唯一标识符 (ID)。
    - **设备** – 选择应该用于装运负荷的设备。
    - **负荷高度**、**负荷宽度** 和 **负荷深度** – 输入负荷的维度。
    - **允许的最大负荷体积** 和 **允许的最大负荷重量** – 输入允许的最大负荷体积和重量。
    - **允许的最大毛重** – 输入允许的最大负荷毛重。 负荷的毛重包括其皮重和负荷重量。
    - **允许的最大货运件数** – 输入负荷可包含的最大货运件数。
    - **地面堆叠负荷** – 选中此复选框以使用地面负荷。 在地面负荷方案中，箱子从地面到天花板，从一面墙到另一面墙堆叠在集装箱内，以最大化容量。

1. 在操作窗格上，选择 **保存**。

## <a name="associate-a-load-template-with-a-new-load"></a>将负荷模板与新负荷关联

1. 转到 **运输管理 \> 计划 \> 负荷计划工作台**。
1. 在页面的上部，根据要为其创建负荷的源单据的类型，选择以下选项卡之一：**装运**、**销售行**、**转移行** 或 **采购订单行**。 
1. 选择要为其计划负荷的特定单据。
1. 在操作窗格上 **供应与需求** 选项卡上 **添加** 组中，选择 **至新负荷**。
1. 在 **负荷模板** 对话框中，在 **负荷模板 ID** 字段中，选择要应用的模板。
1. 选择 **确定** 以应用模板。
