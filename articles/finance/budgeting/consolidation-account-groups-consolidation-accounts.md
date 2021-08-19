---
title: 合并科目组和其他合并科目
description: 此主题提供有关合并科目组和其他合并科目的信息，并说明其在 Microsoft Dynamics 365 Finance 中的使用方法。
author: aprilolson
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3e6671e5f3ceff671210011913a3a91194613c7c0e4e1d8e8063e4e27e5f3cf5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727412"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>合并科目组和其他合并科目

[!include [banner](../includes/banner.md)]

此主题提供有关合并科目组和其他合并科目的信息，并说明其在 Microsoft Dynamics 365 Finance 中的使用方法。

## <a name="consolidation-account-groups"></a>合并帐户组

可通过合并科目组创建要用于合并数据的科目组。 通常，合并科目组表示政府规定的会计科目表，或将科目映射到公司总部定义的组。 可以在 **合并** 模块的 **设置** 区域中找到合并科目组。 添加新组时，请为科目组输入唯一标识和名称。

## <a name="additional-consolidation-accounts"></a>其他合并帐户
可通过其他合并科目将现有会计科目表中的科目分配给合并科目组。 然后可以指定合并科目值和名称。 

可以在 **合并** 模块的 **设置** 区域中找到其他合并科目。 在创建新的合并科目时，至少必须指定以下信息：

-   **主科目** – 此字段是查询，用于显示基于您在页面中选择的会计科目表的所有主科目。 在您选择科目时，将在 **主科目名称** 字段中自动输入名称。
-   **合并科目组** – 此字段用于指定要将科目分配给的组。 如果以两种不同方式合并，则必须将同一个科目添加到所有四个合并科目组。
-   **合并科目** – 输入合并科目的值。 此值可以不是会计科目表中的科目。 它可以是您需要的任何值。
-   **合并科目名称** – 输入您希望在查询和报表中显示的科目名称。
-   **SAT 级别** – 此字段用于向墨西哥税务部门报告帐户对账单。 

创建合并科目组和其他合并科目完毕后，可以在“在线合并流程”中选择该组。


有关详细信息，请参阅[创建合并组和其他合并帐户](../general-ledger/tasks/create-consolidation-groups.md)。 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]