---
title: "导入和维护信用卡交易记录"
description: "本主题说明如何导入和维护与费用相关的信用卡交易记录。 这些交易记录可以设置为对重复执行的计划自动导入或根据需要手动导入。"
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 3379e2f850653cb99231d4ab030b64beb72b626a
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="import-and-maintain-credit-card-transactions"></a>导入和维护信用卡交易记录

[!include[banner](../includes/banner.md)]

与费用相关的信用卡交易记录可以设置为对重复执行的计划自动导入。 或者根据需要手动导入。 信用卡交易记录通过信用卡交易记录数据实体进行导入。

有关数据实体的详细信息，请参阅[数据实体](../../dev-itpro/data-entities/data-entities.md)。

## <a name="import-credit-card-transactions"></a>导入信用卡交易记录

1. 在**信用卡交易记录**页，选择**导入交易记录**。 如果您是首次打开数据管理，系统必须更新数据实体的列表后，您才可以继续。
2. 在**名称**字段中，输入导入的作业的唯一描述。
3. 在**源数据格式**字段中，选择包含要导入的信用卡交易记录的文件格式。
4. 选择**上载**，然后查找并选择要导入的文件。
5. 在上载文件后，通过选择磁贴上的**查看映射**链接验证信用卡交易记录文件与信用卡交易记录数据实体列的映射。 如果出现映射错误，或如果必须更改映射，则从**映射可视化**选项卡或**映射详细信息**选项卡更改映射。
6. 若要自动执行信用卡交易记录，请选择**创建重复性数据作业**。 随后可以设置定义导入信用卡交易记录的频率的重复项。 当您完成时，选择**确定**。
7. 若想要现在导入所选文件，选择**导入**。
8. 如果在导入期间出现错误，您可以查看执行日志或暂存数据以查看必须修复的错误，以帮助保证导入成功。

> [!NOTE]
> 如果必须导入多个文件格式，则必须为每种格式类型创建单独的导入作业。

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>重新分配离职员工的信用卡交易记录

终止员工记录后，员工的 Active Directory 域服务 (AD DS) 帐户被禁用。 但是，可能还存在仍然必须支出和偿还的有效信用卡交易记录。 从**信用卡交易记录**页可以在相关员工已离职时为任何信用卡交易记录重新分配员工。

选择一个或多个信用卡交易记录，然后选择**重新分配交易记录**。 您可以随后选择要分配信用卡交易记录的其他员工。 重新分配信用卡交易记录后，可以为费用报表选择该交易记录，并通过费用报表报销的正常流程进行支付。

