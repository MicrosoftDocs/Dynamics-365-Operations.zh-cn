---
title: 创建和维护库存锁定
description: 此过程显示如何通过使用库存锁定防止实际现有库存由其他出货原始凭证预留。
author: perlynne
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 12c6e047e15aaab157e6de70f4a09f500af2965f
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383450"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>创建和维护库存锁定

[!include [banner](../../includes/banner.md)]

此过程显示如何通过使用库存锁定防止实际现有库存由其他出货原始凭证预留。 您可以使用所示的示例值运行 USMF 公司演示数据的过程。 在开始此过程前，需要有物料和可用的实际现有库存。


## <a name="create-an-inventory-blocking"></a>创建库存锁定
1. 在**导航窗格**中，转到**模块 > 库存管理 > 定期任务 > 库存锁定**。
2. 单击**新建**。
3. 在**物料编号**字段中，单击下拉按钮以打开查找。
4. 在列表中，选择您想选的物料。 选择物料编号以及您想要锁定的实际现有库存。 如果您使用 USMF，您可以选择物料 M9201。  
5. 在**数量**字段中，输入一个数字。 如果您使用物料 M9201，需要选择少于 200。
6. 展开**库存维度**快速选项卡。
7. 在**仓库**字段，单击下拉按钮以打开查找。
8. 在列表中，找到并选择所需记录。 如果您使用物料 M9201，您可以选择仓库 51。  
9. 单击**保存**。

## <a name="update-the-conditions-of-the-inventory-blocking"></a>更新库存锁定的条件
1. 在**常规**快速选项卡的**数量**字段中，输入一个数字。 更新“库存数量”字段以反映锁定数量。  
2. 在**预期日期**字段中输入日期。 您可能希望通过分配预期日期，指定锁定的库存什么时候可供使用。 如果为库存锁定选择所需的收据选项，由于在您手动创建锁定时为默认显示，该日期将出现在预期事务中。  
3. 单击**保存**。

## <a name="remove-the-inventory-blocking"></a>取消库存锁定
1. 在**操作窗格**上，单击**删除**。
2. 单击**是**。
3. 关闭该页面。

