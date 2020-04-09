---
title: 估计生产订单
description: 您可以使用演示数据公司 USMF 或使用您自己的数据运行该过程。
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f1e99d7c84171e4affe59fb896a7e93c2a328740
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146759"
---
# <a name="estimate-a-production-order"></a>估计生产订单

[!include [banner](../../includes/banner.md)]

您可以使用演示数据公司 USMF 或使用您自己的数据运行该过程。 在这两种情况下，您需要有一个状态为“已创建”的未结生产订单。 这是解释生产订单周期的七个步骤中的第二步。


## <a name="estimate-a-production-order"></a>估计生产订单
1. 转到“生产控制”>“生产订单”>“全部生产订单”。
2. 选择网格中状态为“已创建”的某个订单。
3. 在操作窗格上单击“生产订单”。
4. 单击“估计”。
    * 通过此步骤可以计算出单个生产订单的预估成本。   
5. 单击“确定”。

## <a name="view-the-calculation-details"></a>查看计算明细
1. 在“操作窗格”中，单击“管理成本”。
2. 单击“查看计算明细”。
    * 此页显示了成本分解情况。 例如，您可以查看第一成品行的单位总成本价。 根据物料清单、生产工艺路线和间接成本，后续行还包括很多成本。  
