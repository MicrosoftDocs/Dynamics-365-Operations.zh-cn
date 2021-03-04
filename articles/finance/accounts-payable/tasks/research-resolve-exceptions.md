---
title: 研究或解析异常
description: 在您通过使用供应商发票页面过帐供应商发票，以及打开供应商发票政策违规页面时，将运行供应商发票政策。
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 995d68f6224b6dfbb1928c907ad991b86fc47668
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440697"
---
# <a name="research-or-resolve-exceptions"></a>研究或解析异常

[!include [banner](../../includes/banner.md)]

在您通过使用供应商发票页面过帐供应商发票，以及打开供应商发票政策违规页面时，将运行供应商发票政策。 您还可以配置供应商发票工作流每次运行供应商发票策略发票您提交到工作流。 

供应商发票此策略不适用于在发票登记簿或发票日志中创建的发票。 

发票匹配验证并不使用供应商发票政策，但是，需在应付帐款参数页面进行设置。

此记录使用 USMF 公司演示。 应付帐款经理或会计经理将执行以下步骤。 在您开始前，请确保选择发票匹配 Configuration Key。


## <a name="prepare-to-create-vendor-invoice-policies"></a>准备为供应商发票策略
1. 转到“应付帐款”>“设置”>“应付帐款参数”。
2. 单击“发票验证”选项卡。
3. 选择或清除“自动更新发票抬头状态”复选框。
4. 单击“确定”。
5. 在“过帐发票差异”字段中，选择一个选项。
6. 关闭该页面。
7. 转到“应付帐款”>“政策设置”>“供应商发票政策”。
8. 单击“参数”。
9. 单击“btnAdd”。
10. 关闭该页面。

## <a name="create-policy-rule-types-for-vendor-invoices"></a>创建或更新供应商发票政策规则类型
1. 转到“应付帐款”>“政策设置”>“供应商发票政策规则类型”。
2. 单击“新建”。
3. 在“规则名称”字段中，输入一个值。
4. 在“描述”字段中，键入一个值。
5. 在“查询名称”字段中，单击下拉按钮以打开查找。
6. 在列表中，找到并选择所需记录。
7. 在列表中，单击所选行中的链接。
8. 单击“保存”。
9. 关闭该页面。

## <a name="define-a-vendor-invoice-policy"></a>定义一个供应商发票策略
1. 转到“应付帐款”>“政策设置”>“供应商发票政策”。
2. 单击“新建”。
3. 在“名称”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 展开或折叠“政策组织”部分。
6. 在树结构中，选择“美国 Contoso 娱乐系统”。
7. 单击“添加”。
8. 展开或折叠“政策规则”部分。
9. 单击“创建政策规则”。
10. 在“政策规则描述”字段中，输入一项描述。
11. 单击“筛选器”。
12. 单击“添加”。
13. 在列表中，标记所选的行。
14. 在“表格”字段中，单击下拉按钮以打开查找。
15. 在列表中，单击所选行中的链接。
16. 在“派生表”字段中，单击下拉按钮以打开查找。
17. 在列表中，单击所选行中的链接。
18. 在名为“字段”的字段中，单击下拉按钮以打开查找。
19. 在名为“字段”的字段中，输入一个值。
20. 关闭该页面。
21. 在“标准”字段中，输入一个值。
22. 单击“确定”。
23. 单击“确定”。
24. 关闭该页面。
25. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]