---
title: 创建借出物品
description: 借出物品是帮助您跟踪您的公司借出给工作人员的实际物品（如手机或电脑）的记录。
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26bf5a83a6d25e99996ec4219c5fbbeed806e22d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693715"
---
# <a name="create-loan-items"></a>创建借出物品


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



借出物品是帮助您跟踪您的公司借出给工作人员的实际物品（如手机或电脑）的记录。 每个实际物品都必须具有相应的借出物品。 每个借出物品记录都应描述所借物品，负责借出的员工和物品可以借出的天数。 您可以同时创建多个借出物品，例如钥匙、门卡或制服等。 创建此程序的演示数据公司是 USMF。


## <a name="create-loan-types"></a>创建“借出类型”
1. 转到 **人力资源** > **工作人员** > **借出物品** > **借出类型**。
2. 单击 **新建**。
3. 在 **借出类型** 字段中，键入一个值。
4. 在 **描述** 字段中，键入一个值。
5. 输入指派给此借出类型的物品可逾期返还的天数。 
6. 单击 **保存**。
7. 关闭该页面。
8. 刷新该页面。

## <a name="create-loan-items"></a>创建“借出物品”
1. 转到 **人力资源** > **工作人员** > **借出物品** > **借出物品**。
2. 单击 **创建借出物品**。
3. 在 **数量** 字段中，输入一个数字。
4. 在 **描述** 字段中，键入一个值。
5. 在 **借出类型** 字段中，单击下拉按钮以打开查找。
6. 在列表中，找到并选择所需记录。
7. 在列表中，单击所选行中的链接。
8. 输入允许物品借出的天数。
    * 借出设备的“预定归还日期”字段的默认值计算为当前日期加上此数字。  
9. 在 **负责人** 字段中，单击下拉按钮以打开查找。
10. 单击 **选择**。
11. 在 **起始值** 字段中，输入一个数字。
12. 在 **间隔** 字段中，输入一个数字。
13. 在 **格式** 字段中，键入一个值。
    * 例如，借出物品的起始编号为 10，则在 **格式** 字段中输入两个数字符号。  
14. 单击 **确定**。
15. 刷新该页面。



[!INCLUDE[footer-include](../includes/footer-banner.md)]
