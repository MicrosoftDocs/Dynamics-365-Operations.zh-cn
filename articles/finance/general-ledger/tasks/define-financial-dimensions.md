---
title: 定义财务维度
description: 此任务指南演示如何添加实体支持的财务维度和自定义的财务维度。
author: aprilolson
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c93a67d0c4a8443eaf40b094770ed6ce29da527b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834444"
---
# <a name="define-financial-dimensions"></a>定义财务维度

[!include [banner](../../includes/banner.md)]

此任务指南演示如何添加实体支持的财务维度和自定义的财务维度。  此指南使用演示公司 USMF。


## <a name="create-an-entity-backed-financial-dimension"></a>创建实体支持的财务维度
1. 转到 **导航窗格 > 模块 > 总帐 > 会计科目表 > 维度 > 财务维度**。
2. 单击 **新建**。
3. 在 **用户值窗体** 字段中，选择系统中定义的实体作为财务维度的基础。 
4. 在 **维度名称** 字段中，输入描述财务维度的值。 该名称可与系统定义的实体名称不同，但不能含有空格或特殊字符。
5. 单击 **启用**。 “启用财务维度”更新带有财务维度名称的表格，并移除已删除的维度。 在启用财务维度前，您可以输入维度值，但是财务维度在启用后才能使用。  
6. 在启用消息上，单击 **关闭**。
7. 单击 **启用**。 维度启用可安排在特定日期和时间批量运行。  
8. 在 **操作窗格** 上，单击 **维度值**。 一些维度值是公司特定的。 您可以通过验证公司名称是否在维度值列表中来验证是否是特定于公司的维度值。  

## <a name="create-a-custom-financial-dimension"></a>创建自定义的财务维度
1. 关闭该页面。
2. 单击 **新建**。
3. 在 **使用以下来源中的值** 字段中，选择 **自定义维度**。
4. 在 **维度名称** 字段中，输入描述财务维度的值。
    - 名称不能含有空格或特殊字符。  
    - 您还可以指定科目掩码以限制您为维度值输入的金额和信息类型。   
    - 您可以输入保持不变的每个维度值的信息，例如的字符的字母或连字符。 还可以输入数字标志 (#) 和和符号 (&) 作为每次要更改的字母和数字的占位符创建维度值。 使用一个数字标志 (#) 作为编号占位符和符号 (&) 作为信函的占位符。  示例：若要限制维度值为字母 CC 和三个数字，您要输入 CC-### 作为格式掩码。  
5. 单击 **启用**。 “启用财务维度”更新带有财务维度名称的表格，并移除已删除的维度。 在启用财务维度前，您可以输入维度值，但是财务维度在启用后才能使用。     
6. 单击 **启用**。 维度启用可安排在特定日期和时间批量运行。      
7. 在 **操作窗格** 上，单击 **维度值**。
8. 单击 **新建**。
9. 在 **维度值** 字段中，输入描述财务维度值的名称。
10. 在 **描述** 字段中，输入描述您的财务维度值的描述。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]