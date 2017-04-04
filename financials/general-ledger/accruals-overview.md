---
title: "应计概览"
description: "本文介绍应计项目，并且提供有关如何设置和创建交易记录的信息。"
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 328a4a7bef32ee8634e4a9f4854ebe78fcc99f6d
ms.lasthandoff: 03/31/2017


---

# <a name="accruals-overview"></a>应计概览

本文介绍应计项目，并且提供有关如何设置和创建交易记录的信息。

应计用于在权责发生制中跟踪在取得收入的期间中识别的收入，而不是接收付款时，和跟踪支出（成本）发生时识别的支出（成本），而不是在进行付款时。

## <a name="accrual-schemes"></a>应计架构
应计架构用于设置递延收入和成本，并且，同一个应计架构可以为收入和成本使用。 分类帐应计重新分摊日志行的成本或收入，以便成本和收入具结在相应的期间中。 在**应计架构**页上，您指定在应计架构应用时使用的借方科目和贷方科目。

-   **借方** – 您定义的将替换日记帐凭证行的借方主科目的主科目。 此科目也用于延期的冲销，基于分类帐应计交易记录。
-   **贷方** – 您定义的将替换日记帐凭证行的贷方主科目的主科目。 此科目也用于延期的冲销，基于分类帐应计交易记录。

在您确定使用哪些科目后，您可以指定在交易记录创建时如何创建凭证号。 您还可以指定交易记录发生的频率，交易记录创建的次数和交易记录过帐的时间。 在应计架构创建后，可以在某些日记帐中通过使用分类帐应计功能使用它。

## <a name="ledger-accruals"></a>分类帐应计
当您输入日记帐时，您可以单击**功能**菜单中的**分类帐应计**。 然后，在您选择应计架构时，将看到将在期间内分布的日记帐的基准额，如应计架构所确定的。 例如，您结算，则员工的保险整年度的在 1 月和金额是 12,000，则必须个月识别该每个支出。 您可以选择一个开始日期。 您还可以指定应计的金额是否基于此科目或对方科目。 在您进行选择后**，查看基于应计方案创建的所有交易单击**记录的交易记录。 例如，如果您在 12,000，分配保险支出年度，则为每个将看到 1,000 个月。 在您过帐某一日志后，通过** **凭证交易记录查询页的链接，然后可以查看交易记录。 如果应计架构可以不应用 (例如，发票，在销售订单或采购发票) 的订单是包含，您可以贷记预付的金额以及支出借记金额。 然后您可以在应用应计架构时选择**对方**。


