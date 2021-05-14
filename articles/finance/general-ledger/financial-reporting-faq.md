---
title: 财务报告常见问题
description: 本主题列出了与其他用户已有的财务报告相关的问题。
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923017"
---
# <a name="financial-reporting-faq"></a>财务报告常见问题 

本主题提供有关财务报告的常见问题的解答。 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>如何使用树安全限制对报表的访问？

以下示例说明了如何使用树安全来限制对报表的访问。

USMF 演示公司有一个资产负债报表，并非所有财务报告用户都应具有对该报表的访问权限。 要限制访问，可以使用树安全来限制对单个报表的访问，以便只有某些用户可以访问该报表。 请按照以下步骤操作以限制访问： 

1. 登录到 Financial Reporter Report Designer。
2. 创建一个新的树定义。 转到 **文件 > 新建 > 树定义**。
3. 双击 **单位安全性** 列中的 **摘要** 行。
4. 选择 **用户和组**。  
5. 选择需要访问此报表的用户或组。 
6. 选择 **保存**。
7. 在报表定义中，添加您的新树定义。
8. 在树定义中，选择 **设置**。 在 **报告单位选择** 下，选择 **包括所有单位**。

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a>如何确定哪些帐户与我的余额不匹配？

如果您的报表没有匹配的余额，则可以采取以下步骤来确定每一个帐户及差异。 

**Financial Reporter Report Designer**
1. 在 Financial Reporter Report Designer 中，创建一个新的行定义。 
2. 选择 **编辑 > 插入维度中的行**。
3. 选择 **主帐户**。  
4. 选择 **确定**。
5. 保存行定义。
6. 创建一个新的列定义
7. 创建一个新的报表定义。
8. 选择 **设置** 并取消标记此选项。  
9. 生成报表。 
10. 将报表导出到 Microsoft Excel。

**Dynamics 365 Finance** 
1. 在 Dynamics 365 Finance 中，转到 **总帐 > 查询和报表 > 试算平衡表**。
2. 设置以下参数：
   - **开始日期** - 输入会计年度的开始日期。
   - **结束日期** - 输入报表的生成日期。
   - **财务维度** - 将此字段设置为 **主帐户集**。
 3. 选择 **计算**。
 4. 将报表导出到 Microsoft Excel。

您现在应该能够将 Financial Reporter Excel 报表中的数据复制到试算平衡表报表，因此可以比较 **期末余额** 列。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]