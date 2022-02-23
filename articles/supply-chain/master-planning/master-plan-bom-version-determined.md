---
title: 确定物料清单版本
description: 在需求分解过程中，如果某一物料具有“生产”这一默认订单类型，计划引擎将基于站点查找有效的物料清单版本。
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a90a257debe8f24e149ddca1738d8376b2124012
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966972"
---
# <a name="determine-the-bom-version"></a>确定物料清单版本

[!include [banner](../includes/banner.md)]

在需求分解过程中，如果某一物料具有“生产”这一默认订单类型，计划引擎将基于站点查找有效的物料清单版本。 

此站点维度始终是已知的，并且已在需求交易记录上指明。 用于确定要使用的物料清单版本的如下流程：

-   如果在需求站点为物料定义了物料清单版本，将使用特定于站点的物料清单。
-   如果在需求站点为物料定义了不特定于站点的物料清单版本，将使用通用物料清单。 通用物料清单不指明站点，对多个站点都有效。 如果存在通用物料清单，则使用。
-   如果没有可供使用的通用物料清单，需求分解将到此为止。

有效的物料清单版本，不论是特定于站点还是通用，都必须符合要求的日期和数量条件。





