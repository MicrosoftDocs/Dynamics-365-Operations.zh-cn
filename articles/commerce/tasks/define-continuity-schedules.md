---
title: 定义连续性计划
description: 本文逐步演示如何设置连续性计划（也称为重复订单）。
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: faa55c844c8ee8742fbb0868b55a520cec6686aa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885076"
---
# <a name="define-continuity-schedules"></a>定义连续性计划

[!include [banner](../includes/banner.md)]

本文逐步演示如何设置连续性计划（也称为重复订单）。 本文在演示数据中使用 USRT 公司。


## <a name="create-continuity-program"></a>创建连续性计划
1. 转至“Retail 和 Commerce”>“连续性”>“连续性计划”。
2. 单击“新建”。
3. 在“计划 ID”字段中，键入连续性计划 ID。
4. 在“订单开始”字段中，选择“第一个事件”。
    * 如果客户为连续性计划下一个新订单，产品将有两个装运选项：1. 第一个事件：将装运连续性计划中的第一个产品。  2 当前事件：将装运当前产品。 例如， 计划中三个月，客户将收到计划中的第三个产品。  
5. 选择“是”提示输入订单的开始日期。
6. 单击“添加行”。
7. 在“物料编号”字段中，键入第一个产品的物料编号（“0013”）。
8. 键入“CP”。
9. 输入第一个产品可供订购的日期。
10. 单击“添加行”。
11. 在“物料编号”字段中，键入“0014”。
12. 在“日期间隔代码”字段中，清除值，使该字段为空。
    * 对于此过程，请清除日期间隔。 您将把该日期设置为从第一个物料的开始日期的增量。  
13. 在这里输入产品的装运间隔。 键入“30”。
    * 对于每月计划，将为间隔输入 30 天。  
14. 单击“添加行”。
15. 在“物料编号”字段中，键入“0015”。
16. 键入“结束”。
17. 单击“保存”。

## <a name="assign-to-continuity-item"></a>分配给连续性物料
1. 转到“产品信息管理”>“产品”>“已发布产品”。
2. 选择物料“0016”。
    * 对于此过程，将选择物料编号 0016。 通常您将已经创建了一个已发布产品，在呼叫中心中为该产品下销售订单时应用了更多连续性业务逻辑。  
3. 在列表中，单击所选行中的链接。
4. 单击“编辑”。
5. 展开或折叠“销售”部分。
6. 在这里输入此物料代表的连续性计划。 键入您之前创建的计划 ID。
    * 此物料在呼叫中心售出时，将从所选连续性计划应用更多业务逻辑。  
7. 单击“保存”。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]