--- 
title: "创建新的贸易协议"
description: "该过程会显示如何创建贸易协议，您可在其中登记您与特定客户达成的新产品销售价格。"
author: omulvad
manager: AnnBe
ms.date: 11/16/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f7df0a91948a494465fbd55af99757e3890357ce
ms.openlocfilehash: e132cd20437b7929e81fcaa123d70bb57fb320c8
ms.contentlocale: zh-cn
ms.lasthandoff: 12/04/2018

---
# <a name="create-a-new-trade-agreement"></a>创建新的贸易协议

[!include [task guide banner](../../includes/task-guide-banner.md)]

该过程会显示如何创建贸易协议，您可在其中登记您与特定客户达成的新产品销售价格。 您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。 如果您正在使用您自己的数据，在您开始本指南之前，您需要确保贸易协议日记帐名称存在，且其中的默认关系被设置为“价格（售价）”。


## <a name="create-and-post-a-new-trade-agreement-journal"></a>创建和发表新的贸易协议日记帐
1. 转至“销售和营销”>“价格和折扣”>“贸易协议日记帐”。
2. 单击“新建”。
3. 在“名称”字段中，单击下拉按钮以打开查找。
4. 在列表中，找到并选择所需记录。
5. 在列表中，单击所选行中的链接。
6. 单击“行”。
7. 在“帐户代码”字段中，选择“表格”。
    * 在此示例中，您正在更新特定客户的价格，这意味着您需要选择表格。 如果您正在更新产品的目录价格，您可以选择“全部”，如此新价格将对所有客户有效。 如果您正在区分不同客户细分的价格，则您可以选择组。 若要选择“组”，您必须设置“客户价格组”。  
8. 在“帐户选择”字段中，单击下拉按钮以打开查找。
9. 在列表中，找到并选择所需记录。
10. 在“物料”字段中，选择“表格”。
    * 在输入贸易协议类型“价格（售价）”时，您仅可选择“物料代码”字段中的“表格”。 原因在于价格是绝对值，所有产品或一组产品的价格不能完成相同。  
11. 在“物料关系”字段中，单击下拉按钮以打开查找。
12. 在列表中，选择您想要包括在协议中的产品。
    * 记下您已选中的产品。  
13. 在列表中，单击所选行中的链接。
14. 在“从”字段中，输入最小数量。
    * 如果客户必须订购最小数量的产品，然后才能有资格获得新价格，则您需要在此指定最小数量。  
    * 在“至”字段中输入一个值以指定最大数量，高于该数量的协议价格将无效。 如果您基于多个数量分段提供价格和折扣，则指定每个数量等级段为一对最小和最大数量，分别在“从”和“至”字段中输入最小数量和最大数量。  
15. 在“货币金额”字段中，输入价格。
16. 在“开始日期”字段中，输入本协议开始生效的日期。
17. 单击“保存”。
18. 单击“验证”。
19. 单击“验证”选定的行。
20. 单击“确定”。
21. 单击“过帐”。
22. 单击“确定”。

## <a name="view-trade-agreements-for-a-product"></a>查看某一产品的贸易协议
1. 转到“产品信息管理”>“产品”>“已发布产品”。
2. 在列表中，查找并选择您刚更新价格的产品。
3. 在“操作窗格”上，单击“销售”。
4. 单击“查看贸易协议”。
    * 审查您刚创建的价格贸易协议的详情。    
5. 关闭该页面。

## <a name="additional-resources"></a>其他资源
### <a name="community-blogs"></a>社区博客
- [Dynamics 365 for Finance and Operations 中的销售价](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)

