---
title: 转移固定资产
description: 此任务指南将一个固定资产帐簿的财务信息从一个财务维度转移到一个新的财务维度集。
author: moaamer
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c8428467d6e12b6d6af9023980b8cf8738d9294
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726996"
---
# <a name="transfer-a-fixed-asset"></a>转移固定资产

[!include [banner](../../includes/banner.md)]

此任务指南将一个固定资产帐簿的财务信息从一个财务维度转移到一个新的财务维度集。  

1. 在导航窗格中，转到 **模块 > 固定资产 > 固定资产 > 固定资产**。
2. 在列表中，查找并选择要转移的固定资产。
3. 在操作窗格上，单击 **固定资产**。
4. 单击 **转移固定资产**。
5. 在 **转移日期** 字段中，输入日期。
6. 输入注释以对转移进行描述。
    
    此列表显示固定资产所有帐簿。  
7. 标记要转移到新财务维度集的帐簿。
    * 此列表显示所选帐簿的现有财务维度值。  
    * 选择要为所选固定资产帐簿更新的财务维度。  
8. 在 **财务维度** 字段中，单击下拉按钮以打开查找。
    * 根据需要设置其他财务维度值。  
    * 当交易发生时，无论是否输入值，所有财务维度值都会更改。 例如，如果您为 BusinessUnit 输入了值，而将 CostCenter 和财务维度留为空白。 如果您的科目结构允许将 CostCenter 和部门值留为空白，交易发生后，每个价值模型中的 BusinessUnit 都会有新值，而 CostCenter 和部门则仍为空值。  
9. 单击 **更新**。
    * 您可以在完成交易前预览所做更改。  
    * 在转移固定资产帐簿之前查看结果。  
10. 单击 **转移**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
