---
title: 从现有配方版本中复制联产品
description: 该过程展示如何为发布的产品从现有配方版本向不同的配方版本中复制联产品。
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 527fd94613d53a3f0ae81834d5bdaad30dca2833
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579224"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a>从现有配方版本中复制联产品

[!include [banner](../../includes/banner.md)]

该过程展示如何为发布的产品从现有配方版本向不同的配方版本中复制联产品。 它是与联产品关联至少一个配方版本的先决条件。 用于创建该过程的是演示数据公司 USP2。


## <a name="find-a-released-product"></a>查找一个已发布产品
1. 转至“产品发布”。
2. 单击“显示筛选器”。
    * 您即将在筛选器对话框中添加字段“生产类型”。  
3. 单击“添加筛选器”字段将添加字段“生产类型”。
    * 在下一步中，您需要在选择“应用”前在“生产类型”字段中手动输入配方。 这设置已发布产品列表的筛选器。  
4. 在“生产类型”字段中手动输入配方。
5. 单击“应用”。

## <a name="select-a-released-product"></a>选择一个已发布产品。
1. 在列表中，找到并选择所需记录。
2. 单击“配方版本”。
    * 在“工程操作窗格”上单击“配方版本”。  

## <a name="copy-co-products"></a>复制联产品: 
1. 在“操作窗格”上单击“配方版本”。
2. 单击“联产品”。
3. 单击“复制”。
4. 在“物料编号”字段中，输入或选择一个值。
5. 在“配方版本”字段中，输入或选择一个值。
6. 单击“确定”。
7. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]