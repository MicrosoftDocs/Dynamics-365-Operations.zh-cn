---
title: 创建新仓库布局
description: 此主题描述如何在仓库中设置有关库位的信息。
author: perlynne
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 399c87c2e5ad26d5ccc1618cfb6520de3fcdc644
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145655"
---
# <a name="create-a-new-warehouse-layout"></a>创建新仓库布局

[!include [banner](../../includes/banner.md)]

此主题描述如何在仓库中设置有关库位的信息。 此程序仅适用于仓库中“库存管理模块”的“基本仓储”，不适用于“仓库管理模块”。 您可以使用演示数据公司 USMF 或您自己的数据使用该程序。


## <a name="set-the-default-location-capacity"></a>设置默认库位容量
1. 在导航窗格中，转到**模块 > 库存管理 > 设置 > 库存和仓库管理参数**。
2. 选择**库位**选项卡。
3. 在**标准宽度**字段中，输入一个数字。
4. 在**标准深度**字段中，输入一个数字。
5. 在**标准高度**字段中，输入一个数字。
6. 选择**保存**。
7. 关闭该页面。

## <a name="define-the-location-name-format"></a>定义库位名称格式
1. 在导航窗格中，转到**模块 > 库存管理 > 设置 > 库存细分 > 仓库**。
2. 选择**新建**。
3. 在**仓库**字段中，键入一个值。
4. 在**名称**字段中，键入一个值。
5. 在**站点**字段中，在查找中选择所需记录。
6. 切换到**库位名称**部分的扩展项。 此部分中的选项定义库位名称的默认格式。 在我们的示例中，我们增加了通道编号、货架编号和货位编号。  
7. 将**包括通道**选项设置为**是**。
8. 将**包括货架**选项设置为**是**。 
9. 在货架的**格式**字段中，键入一个值。
10. 将**包括货位**选项设置为**是**。
11. 在货架的**格式**字段中，键入一个值。

## <a name="define-warehouse-locations"></a>定义仓库库位
1. 在操作窗格上，选择**仓库**。
2. 选择**库位向导**。
3. 选择**下一步**。
4. 取消选择**出货台**选项
5. 取消选择**堆放库位**选项
6. 选择**下一步**，直到用于选择**完成**的选项。
7. 关闭该页面。
8. 刷新该页面。

