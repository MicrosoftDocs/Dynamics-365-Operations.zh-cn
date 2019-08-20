---
title: 转移固定资产
description: 此任务指南将一个固定资产帐簿的财务信息从一个财务维度转移到一个新的财务维度集。
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 167591cf160916f256e2d10f122eca312ba07639
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839729"
---
# <a name="transfer-a-fixed-asset"></a>转移固定资产

[!include [task guide banner](../../includes/task-guide-banner.md)]

此任务指南将一个固定资产帐簿的财务信息从一个财务维度转移到一个新的财务维度集。  它为 USMF 法人实体使用会计角色和演示数据。

1. 在导航窗格中，转到**模块 > 固定资产 > 固定资产 > 固定资产**。
2. 在列表中，查找并选择要转移的固定资产。
3. 在操作窗格上，单击**固定资产**。
4. 单击**转移固定资产**。
5. 在**转移日期**字段中，输入日期。
6. 输入注释以对转移进行描述。
    
    此列表显示固定资产所有帐簿。  
7. 标记要转移到新财务维度集的帐簿。
    * 此列表显示所选帐簿的现有财务维度值。  
    * 选择要为所选固定资产帐簿更新的财务维度。  
8. 在**财务维度**字段中，单击下拉按钮以打开查找。
    * 根据需要设置其他财务维度值。  
    * 当交易发生时，无论是否输入值，所有财务维度值都会更改。 例如，如果您为 BusinessUnit 输入了值，而将 CostCenter 和财务维度留为空白。 如果您的科目结构允许将 CostCenter 和部门值留为空白，交易发生后，每个价值模型中的 BusinessUnit 都会有新值，而 CostCenter 和部门则仍为空值。  
9. 单击**更新**。
    * 您可以在完成交易前预览所做更改。  
    * 在转移固定资产帐簿之前查看结果。  
10. 单击**转移**。

