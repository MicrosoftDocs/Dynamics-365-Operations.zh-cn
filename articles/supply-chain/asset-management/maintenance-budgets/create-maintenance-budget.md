---
title: 创建维护预算
description: 本主题说明如何在资产管理中创建维护预算。
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: aa373a1a15c19154e6c822c3a962c2b43b8d9e10
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205291"
---
# <a name="create-maintenance-budgets"></a>创建维护预算

[!include [banner](../../includes/banner.md)]

 



维护预算用于创建预防性维护的预计成本概览。 预算行基于预计开始日期在预算期间内的维护安排行计算。

维护预算基于资产管理中使用的成本类型：**预防性**、**纠正**和**投资**。 将包括其更换日期在预算期间内且具有关联的更换值的有效资产的投资维护预算成本。 如果预算计算中包括过去的纠正日期，则包括纠正维护的预算成本。 在此情况下，将为要计算的维护成本的相同将来期间计算早期期间的纠正成本。

## <a name="create-a-maintenance-budget"></a>创建维护预算

1. 选择**资产管理** \> **查询**\> **维护预算**\> **预算**。
2. 选择**创建预算**。
3. 在**维护预算**字段中，输入预算 ID。
4. 在**描述**字段中，输入描述。
4. 在**期间**快速选项卡上的**开始日期**和**结束日期**字段中，输入预算期间的开始日期和结束日期。
5. 若要包括以之前期间的实际成本为基础进行计算的纠正预算成本，请在**纠正开始日期**字段中输入应包括这些成本的期间的开始日期。
6. 根据预算中需要的详细程度，设置五个**分组依据**快速选项卡上的相关选项。
7. 选择**确定**。
8. 选择**预算行**打开**维护预算行**页，可在其中查看已经为期间创建的所有预算行。
9. 若要审核预算，请在**维护预算**页选择预算，然后选择**审核**。 然后在**审核预算**对话框中选择**确定**。 将把您的姓名输入到**维护预算**页中的**审核人**字段中。

    > [!NOTE]
    > 您审核维护预算之后，除非先删除审核，否则不能在**维护预算行**页中重新计算或调整关联的行。 若要删除维护预算的审核，请在**维护预算**页选择预算，然后选择**审核**。 然后在**审核预算**对话框中选择**确定**。

![维护预算](media/01-maintenance-budgets.png)

还可以通过复制现有预算来创建新的维护预算。 在**维护预算**页选择要复制的预算，然后选择**复制**。 这种方法在如下情况下非常有用：已经为一个月创建了预算，希望将其复制到其他月份。

> [!NOTE]
> 维护预算基于维护安排行仅计算预算成本。 若要计算同一期间的实际成本，可以在**实际成本控制**页中执行该项计算。 
