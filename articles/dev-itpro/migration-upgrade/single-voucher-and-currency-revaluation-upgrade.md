---
title: 升级单一凭证日记帐和货币重估
description: 某些组织输入的日记帐中包含有多位客户或供应商的单一凭证，并且还运行应收账款或应付账款外币重估流程。 此主题描述这些组织在升级到 Microsoft Dynamics 365 for Operations 版本 1611 时应执行的步骤。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 343fa226e1cf9072696082e9ebf0a1629e553ae9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "328140"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="0a4c8-104">升级单一凭证日记帐和货币重估</span><span class="sxs-lookup"><span data-stu-id="0a4c8-104">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a4c8-105">某些组织输入的日记帐中包含有多位客户或供应商的单一凭证，并且还运行应收账款或应付账款外币重估流程。</span><span class="sxs-lookup"><span data-stu-id="0a4c8-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="0a4c8-106">此主题描述这些组织在升级到 Microsoft Dynamics 365 for Operations 版本 1611 时应执行的步骤。</span><span class="sxs-lookup"><span data-stu-id="0a4c8-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="0a4c8-107">升级到 Microsoft Dynamics 365 for Operations 版本 1611 时，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="0a4c8-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="0a4c8-108">升级到 Dynamics 365 for Operations 之前，请为应收账款和应付账款运行外币重估流程。</span><span class="sxs-lookup"><span data-stu-id="0a4c8-108">Before you upgrade to Dynamics 365 for Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="0a4c8-109">将**方法**字段设置为**发票日期**。</span><span class="sxs-lookup"><span data-stu-id="0a4c8-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="0a4c8-110">将创建一条重估交易记录，用于冲销上一笔外币重估。</span><span class="sxs-lookup"><span data-stu-id="0a4c8-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="0a4c8-111">因此，将以原始会计币种计算这笔未结交易记录的价值。</span><span class="sxs-lookup"><span data-stu-id="0a4c8-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="0a4c8-112">升级到 Dynamics 365 for Operations 版本 1611。</span><span class="sxs-lookup"><span data-stu-id="0a4c8-112">Upgrade to Dynamics 365 for Operations version 1611.</span></span>
3.  <span data-ttu-id="0a4c8-113">再次运行应付账款和应收账款外币重估流程。</span><span class="sxs-lookup"><span data-stu-id="0a4c8-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="0a4c8-114">此时，将**方法**字段设置为**标准**。</span><span class="sxs-lookup"><span data-stu-id="0a4c8-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="0a4c8-115">将根据当前汇率创建一条新的重估交易记录。</span><span class="sxs-lookup"><span data-stu-id="0a4c8-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="0a4c8-116">此交易记录记录或有利润/损失和正确的汇总会计科目。</span><span class="sxs-lookup"><span data-stu-id="0a4c8-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>




