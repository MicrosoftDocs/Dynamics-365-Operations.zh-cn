---
title: 研究或解析异常
description: 在您通过使用供应商发票页面过帐供应商发票，以及打开供应商发票政策违规页面时，将运行供应商发票政策。
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32ff53198f61e1d1af3c437e9488c2a246cf820a
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2022
ms.locfileid: "8110011"
---
# <a name="research-or-resolve-exceptions"></a>研究或解析异常

[!include [banner](../../includes/banner.md)]

在您通过使用 **供应商发票** 页面过帐供应商发票，以及打开供应商发票 **政策违规** 页面时，将运行供应商发票政策。 您还可以配置供应商发票工作流每次运行供应商发票策略发票您提交到工作流。 

供应商发票此策略不适用于在 **发票登记簿** 或 **发票日记帐** 中创建的发票。 

发票匹配验证并不使用供应商发票政策，但是，需在 **应付帐款参数** 页面进行设置。

此记录使用 USMF 公司演示。 应付帐款经理或会计经理将执行以下步骤。 在您开始前，请确保选择 **发票匹配配置** 键。


## <a name="prepare-to-create-vendor-invoice-policies"></a>准备为供应商发票策略
1. 转到 **应付帐款 > 设置 > 应付帐款参数**。
2. 单击 **发票验证** 选项卡。
3. 选中或清除 **自动更新发票抬头状态** 复选框。
4. 单击 **确定**。
5. 在 **过帐发票差异** 字段中，选择一个选项。
6. 关闭该页面。
7. 转到 **应付帐款 > 政策设置 > 供应商发票政策**。
8. 单击 **参数**。
9. 单击 **添加**。
10. 关闭该页面。

## <a name="create-policy-rule-types-for-vendor-invoices"></a>创建或更新供应商发票政策规则类型
1. 转到 **应付帐款 > 政策设置 > 供应商发票政策规则类型**。
2. 单击 **新建**。
3. 在 **规则名称** 字段中，输入一个值。
4. 在 **描述** 字段中，键入一个值。
5. 在 **查询名称** 字段中，单击下拉按钮以打开查找。
6. 在列表中，找到并选择所需记录。
7. 在列表中，单击所选行中的链接。
8. 单击 **保存**。
9. 关闭该页面。

## <a name="define-a-vendor-invoice-policy"></a>定义一个供应商发票策略
1. 转到 **应付帐款 > 政策设置 > 供应商发票政策**。
2. 单击 **新建**。
3. 在 **名称** 字段中，键入一个值。
4. 在 **描述** 字段中，键入一个值。
5. 展开或折叠 **策略组织** 部分。
6. 在树结构中，选择“美国 Contoso 娱乐系统”。
7. 单击 **添加**。
8. 展开或折叠 **策略规则** 部分。
9. 单击 **创建政策规则**。
10. 在 **策略规则描述** 字段中，输入一项描述。
11. 单击 **筛选器**。
12. 单击 **添加**。
13. 在列表中，标记所选的行。
14. 在 **表** 字段中，单击下拉按钮以打开查找。
15. 在列表中，单击所选行中的链接。
16. 在 **派生表** 字段中，单击下拉按钮以打开查找。
17. 在列表中，单击所选行中的链接。
18. 在名为 **字段** 的字段中，单击下拉按钮以打开查找。
19. 在名为 **字段** 的字段中，输入一个值。
20. 关闭该页面。
21. 在 **条件** 字段中，输入一个值。
22. 单击 **确定**。
23. 单击 **确定**。
24. 关闭该页面。
25. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
