--- 
title: "设置装运承运人"
description: "此过程显示如何设置装运承运人和定义详细信息，诸如服务、装运方式、运输招标、运输约束和装运费用。"
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: eec121859b7135741ccf204fd507ef0790f1c8d4
ms.contentlocale: zh-cn
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-shipping-carriers"></a>设置装运承运人

[!include[task guide banner](../../includes/task-guide-banner.md)]

此过程显示如何设置装运承运人和定义详细信息，诸如服务、装运方式、运输招标、运输约束和装运费用。 运输协调员可将装运承运人分配给某个入站或出站装载。


## <a name="create-a-new-shipping-carrier"></a>创建新装运承运人
1. 转到“运输管理”>“设置”>“承运人”>“装运承运人”。
2. 单击“新建”。
3. 在“装运承运人”字段中，键入一个值。
4. 在“名称”字段中，键入一个值。
5. 在“模式”字段中，单击下拉按钮以打开查找。
6. 在列表中，找到并选择所需记录。
7. 在列表中，单击所选行中的链接。

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>填写装运承运人的一般信息
1. 切换“概览”部分的展开项。
2. 勾选或不勾选“启用承运装运人”复选框。
3. 在“供应商”字段中，单击下拉按钮以打开查找。
    * 选择向其分配装运承运人的供应商帐户。  
4. 在列表中，找到并选择所需记录。
5. 在列表中，单击所选行中的链接。
6. 在“运输招标类型”字段中，选择一个选项。
    * 选择“手动使用运输招标”页面，或通过使用电子数据交换 (EDI) 选择 EDI 来更新招标信息。  
7. 勾选或不勾选“启用承运评级”复选框。

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>创建装运承运人的必需服务
1. 切换“服务”部分的展开项。
2. 单击“新建”。
3. 在列表中，标记所选的行。
4. 在“承运人服务”字段中，键入一个值。
5. 在“名称”字段中，键入一个值。
6. 在“运输方法”字段中，单击下拉按钮以打开查找。
7. 在列表中，找到并选择所需记录。
8. 在列表中，单击所选行中的链接。

## <a name="set-up-the-address-for-the-carrier-optional"></a>设置承运人的地址（可选）
1. 切换“地址”部分的扩展项。
2. 单击“新建”。
3. 在“名称”或“描述”字段中，键入一个值。
4. 在“国家/地区”字段中，单击下拉按钮以打开查找。
5. 在列表中，单击所选行中的链接。
6. 在“邮政编码”字段中，单击下拉按钮以打开查找。
7. 在列表中，找到并选择所需记录。
8. 在列表中，单击所选行中的链接。
9. 在“街道”字段中，键入一个值。
10. 单击“确定”。

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>设置装运承运人的评级资料。
1. 切换“评级资料”部分的展开项。
2. 单击“新建”。
3. 在列表中，标记所选的行。
4. 在“评级资料”字段中，键入一个值。
5. 在“名称”字段中，键入一个值。
6. 在“位置”字段中，单击下拉按钮打开查询。
7. 在列表中，找到并选择所需记录。
8. 在列表中，单击所选行中的链接。
9. 在“仓库”字段，单击下拉按钮以打开查找。
10. 在列表中，找到并选择所需记录。
11. 在列表中，单击所选行中的链接。
12. 在“费率引擎”字段中，单击下拉按钮以打开查找。
    * 选择根据合同，您与承运人订立的费率引擎。  
13. 在列表中，找到并选择所需记录。
14. 在列表中，单击所选行中的链接。
15. 在“费率主数据”字段中，单击下拉按钮以打开查找。
16. 在列表中，找到并选择所需记录。
17. 在列表中，单击所选行中的链接。
18. 在“运输时间引擎”字段中，单击下拉按钮以打开查找。
19. 在列表中，单击所选行中的链接。
20. 单击“保存”。


