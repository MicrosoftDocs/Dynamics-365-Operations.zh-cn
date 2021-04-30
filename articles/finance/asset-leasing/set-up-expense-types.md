---
title: 设置费用类型
description: 本主题介绍如何在资产租赁中设置费用类型。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseExpenseTypeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a1d6667a7c6fe1cd44196f2e753ca72b2ca97649
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880976"
---
# <a name="set-up-expense-types"></a>设置费用类型

[!include [banner](../includes/banner.md)]

本主题介绍如何在资产租赁中设置费用类型。 付款计划中未包含的费用称为 *费用成本*。 这些成本的示例包括财产税、公共区域维护成本和保险费用。

## <a name="add-an-administrative-expense-type"></a>添加管理费用类型

1. 转到 **资产租赁 \> 设置 \> 费用类型**。
2. 选择 **新建**。
3. 在相应字段中，输入新的费用类型和说明。

## <a name="assign-accounts-to-administrative-costs"></a>将科目分配给管理费用

接下来，您应该将科目与费用类型关联。 过帐费用计划条目时，将借记这些科目。 对方科目在每个租赁的 **执行费用付款计划** 行中指定。

1. 转到 **资产租赁 \> 设置 \> 资产租赁参数**。
2. 在 **科目** 选项卡的 **执行成本** 快速选项卡上 **费用类型** 字段中，选择费用类型。
3. 选择 **添加**。
4. 在 **帐簿类型** 字段中，选择要链接到管理费用的帐簿类型。

    > [!NOTE]
    > 可以将多种帐簿类型链接到同一个费用科目。

5. 在 **科目代码** 字段中，指定帐簿应该应用于的租赁：

    - **所有** – 将帐簿应用于所有租赁。
    - **组** – 将帐簿应用于特定租赁组。
    - **表** – 将帐簿应用于特定租赁。

6. 如果在 **帐户编码** 字段中选择了 **组** 或 **表**，请在 **科目/组编号** 字段中选择科目编号或组编号。
7. 在相应字段中，选择金融租赁主科目和经营性租赁主科目。

完成这些步骤后，您可以通过所选租赁的 **租赁详细信息** 页上的 **执行成本付款计划** 行添加费用。 或者，也可以在创建新租赁时增加费用。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
