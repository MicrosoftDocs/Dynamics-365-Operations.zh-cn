---
title: 启用牌照标签打印
description: 此主题显示如何在销售领料工作流程中从库存对最后一个物料拣货之后，对串行装运集装箱码 (SSCC) 标签启用自动打印。
author: perlynne
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d5580edb3324f76f04140bd6793bddaace5fadcf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977105"
---
# <a name="enable-license-plate-label-printing"></a>启用牌照标签打印

[!include [banner](../../includes/banner.md)]

此主题显示如何在销售领料工作流程中从库存对最后一个物料拣货之后，对串行装运集装箱码 (SSCC) 标签启用自动打印。 您可以使用演示数据公司 USMF 运行此程序。 如果您使用自己的数据运行，则须为牌照设置一个数序。 在您开始此任务前，需要装配一台标签打印机。 转到“组织管理”>“设置”>“网络打印机”。 在“操作窗格”中，单击“选项”，然后单击“下载文档路由代理安装程序”按钮。 运行此安装程序并确认工作网络打印机设置为“主动”，方可继续该程序。


## <a name="set-up-the-gs1-company-prefix"></a>设置 GS1 公司字头。
1. 转到 **导航窗格 > 模块 > 仓库管理 > 设置 > 仓库管理参数**。
2. 在 **GS1 公司前缀** 字段中，输入一个 7 位数字的个人 GS1 公司编号。
3. 选择 **保存**。
4. 关闭该页面。

## <a name="setup-the-sscc-license-plate-number-sequence"></a>设置 SSCC 牌照数序
1. 转到 **导航窗格 > 模块 > 组织管理 > 标号规则 > 编号规则**。
2. 在 **区域** 字段中，选择一个选项。
3. 在 **参考** 字段中，选择一个选项。
4. 在 **公司** 字段中，键入一个值。
5. 展开 **分段** 部分。
6. 选择 **编辑**。
7. 在 **区段** 表中，选择第一行
8. 选择 **删除**。
9. 选择 **删除**。
10. 选择 **保存**。
11. 关闭该页面。

## <a name="create-the-document-route-layout"></a>创建文档路径布局
1. 转到 **导航窗格 > 模块 > 仓库管理 > 设置 > 文档路线选择 > 文档路线选择布局**。 启用 SSCC 布局。  
2. 选择 **新建**。
3. 在 **布局 ID** 字段中，键入一个值。
4. 在 **描述** 字段中，键入一个值。
5. 选择 **在文本结尾处插入**。
6. 选择 **保存**。
7. 关闭该页面。

## <a name="set-up-the-document-routing"></a>设置文档路径
1. 转到 **导航窗格 > 模块 > 仓库管理 > 设置 > 文档路线选择 > 文档路线选择**。
2. 在 **工作订单类型** 字段中，选择一个选项。
3. 选择 **新建**。
4. 在 **仓库** 字段中，键入一个值。
5. 在 **名称** 字段中，键入一个值。
6. 选择 **新建**。
7. 在 **布局 ID** 字段中，输入或选择一个值。
8. 在 **名称** 字段中，输入您要使用的打印机名称。
9. 选择 **保存**。
10. 关闭该页面。

## <a name="create-mobile-device-menu"></a>创建移动设备菜单
1. 转到 **导航窗格 > 模块 > 仓库管理 > 设置 > 移动设备 > 移动设备菜单项**。
2. 选择 **新建**。
3. 在 **菜单项名称** 字段中，键入一个值。
4. 在 **标题** 字段中，键入一个值。
5. 在 **模式** 字段中，选择一个选项。
6. 在 **使用现有工作** 字段中选择 **是**。
7. 在 **生成牌照** 字段中选择 **是**。
8. 展开 **工作类** 部分。
9. 选择 **新建**。
10. 在 **工作类 ID** 字段中，键入一个值。
11. 选择 **保存**。
12. 关闭该页面。
13. 转到 **导航窗格 > 模块 > 仓库管理 > 设置 > 移动设备 > 移动设备菜单**。
14. 在树形图中，选择您之前已创建的菜单项。
15. 选择 **编辑**。
16. 选择箭头以将该菜单项添加到菜单中。
17. 选择 **保存**。
18. 关闭该页面。

## <a name="update-a-work-template"></a>更新工作模板
1. 转到 **导航窗格 > 模块 > 仓库管理 > 设置 > 工作 > 工作模板**。
2. 选择 **编辑**。
3. 选择 **新建**。
4. 在 **工作类型** 字段中，选择 **打印**。
5. 在 **工作类 ID** 字段中，输入或选择一个值。
6. 选择 **上移**。
7. 选择 **保存**。
8. 关闭该页面。

