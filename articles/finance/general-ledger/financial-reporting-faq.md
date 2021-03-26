---
title: 财务报告常见问题解答
description: 本主题列出了与其他用户已有的财务报告相关的问题。
author: jiwo
manager: tfehr
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2d49213ea18e09f04b026559bdca49fee1de0ef7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249293"
---
# <a name="financial-reporting-faq"></a>财务报告常见问题解答 

本主题列出了与其他用户已有的财务报告相关的问题。 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>如何使用树安全限制对报表的访问？

场景：USMF 演示公司有一个资产负债表报表，它不希望所有财务报告用户都可以在 D365 中查看它。 解决方案：您可以利用树安全来限制对单个报表的访问，以便只有某些用户可以访问该报表。 

1.  登录到 Financial Reporter 报表设计器

2.  创建一个新的树定义（文件 | 新建 | 树定义）a.    双击 **单位安全性** 列中的 **摘要** 行。
  i.    单击“用户和组”。  
          1. 选择要访问此报表的用户或组。 
          
[![用户屏幕](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)

[![安全性屏幕](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)

  b.    单击 **保存**。
  
[![“保存”按钮](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)

3.  在报表定义中添加新的树定义

[![树定义窗体](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)

A.  在“树定义”中单击“设置”并在“报告单位选择”下选中“包括所有单位”时

[![报告单位选择窗体](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)

**之前：**[![屏幕截图前](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)

**之后：**[![屏幕截图后](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)

注意：出现上述消息的原因是我的用户在应用单位安全性后无权访问该报表



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a>如何确定哪些帐户与 D365 中的余额不匹配？

如果您的报表与 D365 中的期望不符，则可以采取以下步骤来确定这些帐户和差异。 

### <a name="in-financial-reporter-report-designer"></a>在 Financial Reporter 报表设计器中

1.  创建一个新的行定义 a.    单击“编辑”|“插入维度中的行”i.  选择 MainAccount [![选择主帐户屏幕](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)
    
    ii. 单击“确定”b.    保存行定义

2.  创建一个新的列定义     [![创建一个新的列定义](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)

3.  创建一个新的报表定义 a.    单击“设置”并取消选中[![设置窗体](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)
   
4.  生成报表。 

5.  将报表导出到 Excel。

### <a name="in-d365"></a>在 D365 中： 
1.  单击“总帐”|“查询和报表”|“试算平衡表”a.    参数 i.  开始日期：会计年度的开始日期 ii. 结束日期：生成报表的日期 iii.    财务维度集“主帐户集”[![“主帐户”窗体](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)
      
  b.    单击“计算”

2.  将报表导出到 Excel

您现在应该能够将 FR Excel 报表中的数据复制到 D365 试算平衡表报表，并比较“期末余额”列。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]