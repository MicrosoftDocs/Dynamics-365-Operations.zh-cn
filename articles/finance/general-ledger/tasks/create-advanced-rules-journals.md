---
title: 创建日记帐高级规则
description: 该过程介绍创建日记帐高级规则的步骤。
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea6ca24d27bb5b00bbe31060ce2f7e40bf2fb335
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440830"
---
# <a name="create-advanced-rules-for-journals"></a>创建日记帐高级规则

[!include [banner](../../includes/banner.md)]

该过程介绍创建日记帐高级规则的步骤。 这包括设置日记帐控制和用户过帐限制。 此过程使用演示数据公司 USMF。


## <a name="set-up-journal-control"></a>设置日记帐控制
1. 在 **导航窗格** 中，转到 **模块 > 总帐 > 日记帐设置 > 日记帐名称**。
2. 在列表中，找到并选择所需记录。
3. 在 **操作窗格** 中，单击 **日记帐控制**。
4. 在 **哪些科目类型可以过帐** 快速选项卡上，单击 **添加**。
5. 在 **公司帐户** 字段中，单击下拉按钮以打开查找。
6. 在列表中，找到并选择所需记录。
7. 在列表中，单击所选行中的链接。
8. 在 **对于此日记帐，哪些段落值是有效的** 快速选项卡上，单击 **添加**。
9. 在 **科目结构** 字段中，单击下拉按钮以打开查找。
10. 在列表中，找到并选择所需记录。
11. 在列表中，单击所选行中的链接。
12. 在 **分部** 字段中，单击下拉按钮以打开查找。
13. 在列表中，单击所选行中的链接。
14. 在 **起始值** 字段中，单击下拉按钮以打开查找。
15. 在列表中，找到并选择所需记录。
16. 在列表中，单击所选行中的链接。
17. 在 **目标值** 字段中，单击下拉按钮以打开查找。
18. 在列表中，找到并选择所需记录。
19. 在列表中，单击所选行中的链接。

## <a name="set-up-posting-restrictions"></a>设置过帐限制
1. 关闭该页面。
2. 单击 **过帐限制**。
3. 在 **如何设置过帐限制** 字段中，选择“按用户组”。
4. 在树形图中，单击“您允许该日记帐过帐的组”。
5. 单击 **确定**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]