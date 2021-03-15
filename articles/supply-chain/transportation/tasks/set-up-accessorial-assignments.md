---
title: 设置附属分配
description: 此过程显示如何设置附属分配。
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAccessorialAssignment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28562772c52d06fbb2004bd3a01a7bfa32f58a4e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974027"
---
# <a name="set-up-accessorial-assignments"></a>设置附属分配

[!include [banner](../../includes/banner.md)]

此过程显示如何设置附属分配。 这通常由运输协调员完成。 您需要运行“设置运输中心附加费用和附属主数据”指南才能使用该指南。


## <a name="set-up-accessorial-assignment"></a>设置附属分配
1. 转到“运输管理”>“设置”>“分级”>“附属分配”。
2. 单击“新建”。
3. 在“名称”字段中，键入一个值。
4. 切换“详细信息”部分的展开项。
5. 在“中心”字段中，单击下拉按钮以打开查找。
6. 在列表中，选择您在“设置中心附加费用和附属主数据”指南中为附属主数据创建的中心。 
7. 在“中心附属 ID”字段中，单击下拉按钮以打开查找。
8. 在列表中，单击所选行中的链接。
9. 切换“标准”部分的展开项。
    * 在“条件”部分，您可以根据所提供的不同值，选择费用适用时的确切标准。  
10. 将“始终应用”选项设为“是”。
11. 在“附属分配水平”字段中，选择一个选项。
12. 切换“计算”部分的展开项。
13. 在“附加费用类型”字段中，选择“统一”。
    * 附加费用类型确定如何计算实际成本。 在此示例中，此为统一收费。  
14. 在“附加费用”字段中，输入一个数字。
15. 单击“保存”。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]