---
title: 设置供应商发票策略
description: 本主题说明如何设置供应商发票策略。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 678ef8f0b7df00aec615af26cbcadec984331060
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220051"
---
# <a name="set-up-vendor-invoice-policies"></a>设置供应商发票策略

[!include [banner](../../includes/banner.md)]

本主题说明如何设置供应商发票策略。 在您通过使用供应商发票页面过帐供应商发票，以及打开供应商发票政策违规页面时，将运行供应商发票政策。 您还可以配置供应商发票工作流每次运行供应商发票策略发票您提交到工作流。 

- 供应商发票此策略不适用于在发票登记簿或发票日志中创建的发票。  
- 发票匹配验证并不使用供应商发票政策，但是，需在应付帐款参数页面进行设置。  
- 此记录使用 USMF 公司演示。 应付帐款经理或会计经理将执行以下步骤。 在您开始前，请确保选择发票匹配 Configuration Key。


## <a name="prepare-to-create-vendor-invoice-policies"></a>准备为供应商发票策略
1. 转到 **导航窗格 > 应付帐款 > 设置 > 应付帐款参数**。
2. 选择 **发票验证** 选项卡。
3. 选中或清除 **自动更新发票抬头状态** 复选框。
4. 选择 **确定**。
5. 在 **过帐发票差异** 字段中，选择一个选项。
6. 关闭该页面。
7. 找到 **导航窗格 > 模块 > 应付帐款 > 策略设置 > 供应商发票策略**。
8. 选择 **参数**。
9. 选择 **添加**。
10. 关闭此页面将返回到主页。

## <a name="create-policy-rule-types-for-vendor-invoices"></a>创建或更新供应商发票政策规则类型
1. 找到 **导航窗格 > 模块 > 应付帐款 > 策略设置 > 供应商发票策略规则类型**。
2. 选择 **新建**。
3. 在 **规则名称** 和 **说明** 字段中输入值。
4. 在 **查询名称** 字段中，选择下拉按钮以打开查找，然后选择所需记录。
5. 选择 **保存**。
6. 关闭此页面将返回到主页。

## <a name="define-a-vendor-invoice-policy"></a>定义一个供应商发票策略
1. 找到 **导航窗格 > 模块 > 应付帐款 > 策略设置 > 供应商发票策略**。
2. 选择 **新建**。
3. 在 **名称** 和 **说明** 字段中输入值。
4. 展开或折叠 **策略组织** 部分。
5. 在树结构中，选择 **美国 Contoso 娱乐系统**。
6. 选择 **添加**。
7. 展开或折叠 **策略规则** 部分。
8. 选择 **创建策略规则**。
9. 在 **策略规则描述** 字段中，输入一项描述。
10. 选择 **筛选器**。
11. 选择 **添加**。 选择所需记录。
12. 在 **表**、**派生表** 和 **字段** 字段中，从下拉菜单选择选项或输入选项。
13. 关闭该页面。
14. 在 **条件** 字段中，输入一个值。
15. 选择 **确定**。
16. 选择 **确定**。
17. 关闭页面将返回到主页。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]