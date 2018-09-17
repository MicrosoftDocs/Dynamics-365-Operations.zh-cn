--- 
title: "启用牌照标签打印"
description: "销售领料工作流程的最后一项工作是库存拣货，此程序适用于在此之后的串行装运集装箱码 (SSCC) 标签的自动打印。"
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
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
ms.openlocfilehash: 6d186bf7e4aee8cfa97adbd90b9090085e842f9b
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="enable-license-plate-label-printing"></a>启用牌照标签打印

[!include [task guide banner](../../includes/task-guide-banner.md)]

销售领料工作流程的最后一项工作是库存拣货，此程序适用于在此之后的串行装运集装箱码 (SSCC) 标签的自动打印。 您可以使用演示数据公司 USMF 运行此程序。 如果您使用自己的数据运行，则须为牌照设置一个数序。 在您开始此任务前，需要装配一台标签打印机。 转到“组织管理”>“设置”>“网络打印机”。 在“操作窗格”中，单击“选项”，然后单击“下载文档路由代理安装程序”按钮。 运行此安装程序并确认工作网络打印机设置为“主动”，方可继续该程序。


## <a name="set-up-the-gs1-company-prefix"></a>设置 GS1 公司字头。
1. 转到“仓库管理”>“设置”>“仓库管理参数”。
2. 在 GS1 公司的字头字段中，输入一个 7 位数字的个人 GS1 公司编号。
3. 单击“保存”。
4. 关闭该页面。

## <a name="setup-the-sscc-license-plate-number-sequence"></a>设置 SSCC 牌照数序
1. 转到“组织管理”>“标号规则”>“编号规则”。
2. 在“区域”字段中，选择一个选项。
3. 在“参考”字段中，选择一个选项。
4. 在“公司”字段中，键入一个值。
5. 在列表中，标记所选的行。
6. 在列表中，单击所选行中的链接。
7. 展开“分段”部分。
8. 单击“编辑”。
9. 在“区段”表中，选择第一行
10. 单击“移除”。
11. 单击“移除”。
12. 单击“保存”。
13. 关闭该页面。

## <a name="create-the-document-route-layout"></a>创建文档路径布局
1. 转到“仓库管理”>“设置”>“设置”>“文档路径布局”。
    * 启用 SSCC 布局。  
2. 单击“新建”。
3. 在“布局 ID”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 在列表中，找到并选择所需记录。
6. 单击文本结尾处的“插入”。
7. 单击“保存”。
8. 关闭该页面。

## <a name="set-up-the-document-routing"></a>设置文档路径
1. 转到“仓库管理”>“设置”>“文档路径”>“文档路径”。
2. 在“工作订单类型”字段中，选择一个选项。
3. 单击“新建”。
4. 在“仓库”字段中，键入一个值。
5. 在“名称”字段中，键入一个值。
6. 单击“新建”。
7. 在“布局 ID”字段中，输入或选择一个值。
8. 在“名称”字段中，输入您要使用的打印机名称。
9. 单击“保存”。
10. 关闭该页面。

## <a name="create-mobile-device-menu"></a>创建移动设备菜单
1. 转到“仓库管理”>“设置”>“移动设备”>“移动设备菜单项”。
2. 单击“新建”。
3. 在“菜单项名称”字段中，键入一个值。
4. 在“标题”字段中，键入一个值。
5. 在“模式”字段中，选择一个选项。
6. 在“使用现有工作”字段中选择“是”。
7. 在“生成牌照”字段中选择”是“。
8. 展开“工作类”部分。
9. 单击“新建”。
10. 在“工作类 ID”字段中，键入一个值。
11. 单击“保存”。
12. 关闭该页面。
13. 转到“仓库管理”>“设置”>“设置”>“移动设备菜单”。
14. 在列表中，找到并选择所需记录。
15. 在此树上，选择“在树上，选择之前创建的菜单项”。
16. 单击“编辑”。
17. 单击箭头在此菜单中添加菜单项。
18. 单击“保存”。
19. 关闭该页面。

## <a name="update-a-work-template"></a>更新工作模板
1. 转到“仓库管理”>“设置”>“工作”>“工作模板”。
2. 在列表中，找到并选择所需记录。
3. 单击“编辑”。
4. 单击“新建”。
5. 在列表中，标记所选的行。
6. 在“工作类型”字段中，选择“打印”。
7. 在“工作类 ID”字段中，输入或选择一个值。
8. 在列表中，单击所选行中的链接。
9. 单击“上移”。
10. 单击“保存”。
11. 关闭该页面。


