---
title: 完工入库到非牌照控制的库位（申请表，2016 年 5 月）
description: 此任务指南显示报告为完工入库到非牌照控制的位置的示例。
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f891b2e3b20993a08138dfac1aed4f4bab33c6b1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576704"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a>完工入库到非牌照控制的库位（申请表，2016 年 5 月）

[!include [banner](../../includes/banner.md)]

此任务指南显示报告为完工入库到非牌照控制的位置的示例。 一个适用的工作策略是此任务的先决条件。 以前的任务指南显示工作策略的设置。 此任务指南需要 Dynamics AX 应用程序 7.0.1 或更高版本。




## <a name="set-up-an-output-location"></a>设置输出库位
1. 转到“组织管理”>“资源”>“资源组”。
2. 在列表中选择资源组 '5102'。
3. 单击“编辑”。
4. 在“输出仓库”字段中，输入 '51'。
5. 在“输出库位”字段中，输入 '001'。
    * 库位 001 不是牌照控制的位置。 只有当库位存在适用的工作策略时，您才可以设置非牌照控制的输出位置。  

## <a name="create-a-production-order-and-report-it-as-finished"></a>创建生产订单并报告为已完工入库
1. 关闭该页面。
2. 转到“生产控制”>“生产订单”>“全部生产订单”。
3. 单击“新建生产订单”。
4. 在“物料编号”字段中输入 'L0101'。
5. 单击“创建”。
6. 在“操作窗格”中，单击“生产订单”。
7. 单击“估计”。
8. 单击“确定”。
9. 单击“开始”。
10. 单击“常规”选项卡。
11. 在“自动物料清单消耗量”字段中，选择“从不”。
12. 单击“确定”。
13. 单击“完工入库”。
14. 单击“常规”选项卡。
15. 在“接受错误”字段中选择“是”。
16. 单击“确定”。
17. 在“操作窗格”中，单击“仓库”。
18. 单击“工作详细信息”。
    * 在生产订单报告为完工入库时，尚未为储存生成工作。 发生这种情况是因为将工作策略定义为在产品 L0101 报告为已完工入库到库位 001 时阻止生成工作。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]