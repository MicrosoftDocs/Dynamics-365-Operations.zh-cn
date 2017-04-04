---
title: "Microsoft Dynamics 365 的唯一凭证和货币升值升级版本 1611 的工序"
description: "某些组织输入包含单个凭证有多个客户或供应商的日志，以及还运行，应收帐款或应付帐款外币重新计算流程。 此主题描述这些组织是否应跟随的步骤，在升级到版本工序 365 的 Microsoft Dynamics 1611 时。"
author: twheeloc
manager: AnnBe
ms.date: 2016-12-28 16 - 04 - 17
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d42c753d0dc8b8efc2a0d2a26da32a4951d85503
ms.lasthandoff: 03/31/2017


---

# <a name="single-voucher-and-currency-revaluation-upgrade-for-microsoft-dynamics-365-for-operations-version-1611"></a>Microsoft Dynamics 365 的唯一凭证和货币升值升级版本 1611 的工序

某些组织输入包含单个凭证有多个客户或供应商的日志，以及还运行，应收帐款或应付帐款外币重新计算流程。 此主题描述这些组织是否应跟随的步骤，在升级到版本工序 365 的 Microsoft Dynamics 1611 时。

当您升级到版本工序 365 的 Microsoft Dynamics 1611 后，请执行以下步骤。

1.  在升级到工序的之前，请运行 Dynamics 365 应收帐款和应付帐款配合的外币重新计算流程。 **设置方法**字段** **发票日期。 撤消上一外币重估的重估交易创建记录。 因此，未结交易记录将按在其原始记帐币种。
2.  升级到版本工序 Dynamics 365 的 1611。
3.  运行应收帐款和应付帐款，外币将再次处理重新计算。 此时，安装**字段方法** ** **标准。 基于当前汇率的新创建重估交易记录。 此交易记录或有损益和正确的汇总会计科目。



