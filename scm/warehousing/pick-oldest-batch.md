---
title: "在移动设备上领取最早的批次"
description: "此主题描述如何从移动设备设置和应用领取最早批次的选项。"
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: ee45fed40b10dbe913c73e1186b726a39831816d
ms.contentlocale: zh-cn
ms.lasthandoff: 06/20/2017

---

# <a name="pick-oldest-batch-on-a-mobile-device"></a>在移动设备上领取最早的批次

[!include[banner](../includes/banner.md)]

您可以通过移动设备菜单访问配置**领取最早的批次**，它将允许您强制或警告仓库工作人员领取其当前库位中的最早批次。  

## <a name="where-it-applies"></a>适用情况
领取最早的批次在移动设备菜单项上配置并影响领取物料下的批次。

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a>如何设置领取最早的批次配置 
对于设置为使用现有工作的物料，可以从移动设备菜单将**领取最早的批次**设置为**无**、**警告**或**强制**。

**无**：工作人员不会收到任何消息，且允许他们领取其库位中的任何批次。

**警告**和**强制**：当工作人员选择批次时，具有最早到期日期的批次的列表将显示在批次控制上方。 如果库位受牌照控制，具有最早批次的牌照的列表将显示在牌照控制上方。 
-   **警告**：如果工作人员选择显示的列表中没有的牌照或批次，控制将为空白，且将显示具有更早的批次可供选择的警告。 要允许继续执行工作，工作人员可以再次选择同一个牌照或批次。  
-   **强制**：工作人员将继续收到具有更早的批次可供领取的消息。

