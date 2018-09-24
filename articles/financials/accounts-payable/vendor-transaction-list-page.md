---
title: "供应商交易记录列表页"
description: "此主题提供有关 Microsoft Dynamics 365 for Finance and Operations 的“供应商交易记录列表”页的信息。"
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: 1ef7d97f059801f2fb2c0d451546b57055208f81
ms.contentlocale: zh-cn
ms.lasthandoff: 08/31/2018

---

# <a name="vendor-transaction-list-page"></a>供应商交易记录列表页

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>查看结算

可通过操作窗格上的**查看结算**选项卡快速访问结算历史记录和有关整个结算交易记录的详细信息。 还可以显示与所选交易记录有关的其他交易记录，因为这些交易记录属于相同结算，或因为这些交易记录是同一个付款日记帐中创建的付款。

1. 选择**应付帐款 \> 所有供应商**。
2. 选择具有交易记录的供应商，然后选择 **供应商 \> 交易记录**。
3. 选择要研究的交易记录。
4. 在操作窗格上选择**查看结算**选项卡。

    将打开**查看结算**对话框，其中显示所选交易记录以及为其结算的所有单据。 此对话框类似结算历史记录视图，不过其中包含所有相关单据。

5. 可以通过此对话框执行多种任务。 选择一个或多个凭证，然后选择以下菜单之一：

   - **查看记帐** – 将显示与所选单据相关的所有凭证。 选择**关闭**关闭对话框。
   - **导出** – 将所选凭证导出到 Microsoft Excel。
   - –**查看相关付款**  – 将显示在与所选单据关联的付款日记帐中创建的所有付款日记帐交易记录。 此外，还将显示与这些付款有关的所有结算。 此菜单的标签还会变为**查看结算**。 选择**查看结算**将仅显示首次打开**查看结算**对话框时显示的交易记录。
    - **结算交易记录** – 如果未完全结算选择的原始单据，将显示此菜单。 选择后，将显示**结算交易记录**对话框，可在此处选择要结算的交易记录。
    - **撤消结算** – 如果已完全结算选择的原始单据，将显示此菜单。 选择后，将显示**撤消结算**对话框，可在此处撤消已对该单据执行的结算。

