--- 
title: "创建新仓库布局"
description: "该程序将向您说明如何设置有关仓库库位的信息。"
author: perlynne
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 253440d81edd6f71b52ae349398e3c6a895bf05c
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-new-warehouse-layout"></a>创建新仓库布局

[!include [task guide banner](../../includes/task-guide-banner.md)]

该程序将向您说明如何设置有关仓库库位的信息。 此程序仅适用于仓库中“库存管理模块”的“基本仓储”，不适用于“仓库管理模块”。 您可以使用演示数据公司 USMF 或您自己的数据使用该程序。


## <a name="set-the-default-location-capacity"></a>设置默认库位容量
1. 转到“库存管理”>“设置”>“库存和仓库管理参数”。
2. 单击“库位”选项卡。
3. 在“标准宽度”字段中，输入一个数字。
4. 在“标准深度”字段中，输入一个数字。
5. 在“标准高度”字段中，输入一个数字。
6. 单击“保存”。
7. 关闭该页面。

## <a name="define-the-location-name-format"></a>定义库位名称格式
1. 转到库存管理 > 设置 > 库存细分 > 仓库。
2. 单击“新建”。
3. 在“仓库”字段中，键入一个值。
4. 在“名称”字段中，键入一个值。
5. 在“位置”字段中，单击下拉按钮打开查询。
6. 在列表中，找到并选择所需记录。
7. 切换到“库位名称”部分的扩展项。
    * 此部分中的选项定义库位名称的默认格式。 在我们的示例中，我们增加了通道编号、货架编号和货位编号。  
8. 将“包括通道”选项设置为“是”。
9. 将“包括货架”选项设置为“是”。 
10. 在货架的“格式”字段中，键入一个值。
    * 例如：-##  
11. 将“包括货位”选项设置为“是”。
12. 在货架的“格式”字段中，键入一个值。
    * 例如：-##  

## <a name="define-warehouse-locations"></a>定义仓库库位
1. 在“操作窗格”中，单击“仓库”。
2. 单击“库位向导”。
3. 单击“下一步”。
4. 取消选择“出货台”选项
5. 取消选择“堆放库位”选项
6. 单击“下一步”。
7. 单击“下一步”。
8. 单击“下一步”。
9. 单击“下一步”。
10. 单击“下一步”。
11. 单击“下一步”。
12. 单击“下一步”。
    * 请注意在此页上显示的物理维度是您在启动该程序时所设置的。  
13. 单击“下一步”。
14. 单击“完成”。
15. 关闭该页面。
16. 刷新该页面。


