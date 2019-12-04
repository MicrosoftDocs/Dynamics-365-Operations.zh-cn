---
title: 在供应商设计之间切换
description: ''
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772356"
---
# <a name="switch-between-vendor-designs"></a>在供应商设计之间切换

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a>供应商数据流 

如果您使用其他 Dynamics 365 应用进行供应商主控，并且希望隔离供应商信息与客户信息，请使用此基本供应商设计。  

![基本供应商流](media/dual-write-switch-1.png)
 
如果您使用其他 Dynamics 365 应用进行供应商主控，并且希望继续使用**客户**实体存储供应商信息，请使用此扩展供应商设计。 在此设计中，扩展的供应商信息（如供应商暂停状态和供应商配置文件）存储在 Common Data Service 中的**供应商**实体中。 

![扩展供应商流](media/dual-write-switch-2.png)
 
请按照以下步骤使用扩展供应商设计： 
 
1. **SupplyChainCommon** 解决方案包包含工作流程模板，如下图所示。
    > [!div class="mx-imgBorder"]
    > ![工作流程模板](media/dual-write-switch-3.png)
2. 使用工作流程模板创建新的工作流程： 
    1. 使用**在客户实体中创建供应商**工作流程模板为**供应商**实体创建新的工作流程，然后单击**确定**。 此工作流处理**客户**实体的供应商创建方案。
        > [!div class="mx-imgBorder"]
        > ![在客户实体中创建供应商](media/dual-write-switch-4.png)
    2. 使用**更新客户实体**工作流程模板为**供应商**实体创建新的工作流程，然后单击**确定**。 此工作流处理**客户**实体的供应商更新方案。 
        > [!div class="mx-imgBorder"]
        > ![更新客户实体](media/dual-write-switch-5.png)
    3. 从在**客户**实体上创建的模板创建新工作流程。 
        > [!div class="mx-imgBorder"]
        > ![在供应商实体中创建供应商](media/dual-write-switch-6.png)
        > [!div class="mx-imgBorder"]
        > ![更新供应商实体](media/dual-write-switch-7.png)
    4. 您可以根据需要将工作流配置为实时或后台工作流。 
        > [!div class="mx-imgBorder"]
        > ![转换为后台工作流程](media/dual-write-switch-8.png)
    5. 启用您在**客户**和**供应商**实体上创建的工作流，以开始使用 Customer Engagement **客户**实体存储供应商信息。 
 
