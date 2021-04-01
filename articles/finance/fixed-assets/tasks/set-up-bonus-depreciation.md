---
title: 设置额外折旧
description: 此过程显示如何创建特殊折旧补偿并将其与固定资产帐簿关联。
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6627e7fa9a1eb1a9131ec7e2c3cc823b49b286cc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257553"
---
# <a name="set-up-bonus-depreciation"></a>设置额外折旧

[!include [banner](../../includes/banner.md)]

此过程显示如何创建特殊折旧补偿并将其与固定资产帐簿关联。 它为 USMF 法人实体使用会计角色和演示数据。


## <a name="create-a-special-depreciation-allowance"></a>创建特殊折旧补偿
1. 转到“固定资产”>“设置”>“特殊折旧补偿”。
2. 单击“新建”。
3. 在“特殊折旧补偿”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 在“百分比”字段中，输入一个数字。
    * 如果尚未指示百分比，则设置金额。  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a>将特殊折旧补偿与固定资产组帐簿关联
1. 转到“固定资产”>“设置”>“固定资产组”。
2. 在列表中，选择与特殊折旧补偿关联的固定资产组。
3. 单击“帐簿”。
4. 在列表中，选择与特殊折旧补偿关联的帐簿。
5. 单击特殊折旧补偿。
6. 单击“新建”。
7. 在“特殊折旧补偿”字段中，输入或选择一个值。
    * 百分比或金额默认值来自特殊折旧补偿设置。  
8. 在“优先”字段，输入一个数字。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]