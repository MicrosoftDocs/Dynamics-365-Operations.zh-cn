---
title: 子分类帐转移到总帐
description: 本主题描述 Microsoft Dynamics 365 Finance 中与总帐内的子分类帐转移过程有关的功能。
author: roschlom
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: d43b96176c51d12c35383da75bf65a1ad92f84c6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815276"
---
# <a name="subledger-transfer-to-the-general-ledger"></a><span data-ttu-id="69d71-103">子分类帐转移到总帐</span><span class="sxs-lookup"><span data-stu-id="69d71-103">Subledger transfer to the General ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="69d71-104">本主题描述 Microsoft Dynamics 365 Finance 中与用于转移子分类日记帐分录批次的规则有关的功能。</span><span class="sxs-lookup"><span data-stu-id="69d71-104">This topic describes capabilities in Microsoft Dynamics 365 Finance that are related to the rules for transferring batches of subledger journal entries.</span></span>

<span data-ttu-id="69d71-105">在版本 8.1 中，进行了更改以允许使用已弃用 **同步** 选项的转移规则。</span><span class="sxs-lookup"><span data-stu-id="69d71-105">In version 8.1, changes were made to allow the transfer of rules, which deprecated the **Synchronous** option.</span></span> <span data-ttu-id="69d71-106">有关详细信息，请参阅[已删除或弃用 Finance and Operations 的功能](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20)。</span><span class="sxs-lookup"><span data-stu-id="69d71-106">For more information, see [Removed or deprecated features for Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).</span></span>

<span data-ttu-id="69d71-107">以下选项可用于传输子分类帐批次。</span><span class="sxs-lookup"><span data-stu-id="69d71-107">The following options are available for transferring subledger batches.</span></span> 

 - <span data-ttu-id="69d71-108">异步 – 此选项将立即安排将子分类帐会计条目转移到总分类帐。</span><span class="sxs-lookup"><span data-stu-id="69d71-108">Asynchronous – This option will immediately schedule the transfer of the subledger accounting entries to the general ledger.</span></span> <span data-ttu-id="69d71-109">只要有资源可自由地在服务器上处理此请求，就会记录总帐凭证。</span><span class="sxs-lookup"><span data-stu-id="69d71-109">The general ledger voucher will be recorded as soon as resources are free to process this request on the server.</span></span> 

- <span data-ttu-id="69d71-110">计划批处理 – 此选项将添加要转移到总帐中的处理队列的子分类帐会计分录，在该队列中将按接收顺序处理分录。</span><span class="sxs-lookup"><span data-stu-id="69d71-110">Scheduled batch – This option will add the subledger accounting entries that are being transferred to the processing queue in the general ledger, where the entries will be processed in order received.</span></span> <span data-ttu-id="69d71-111">如果有资源可自由地在服务器上处理此批处理作业，就会在计划的时间记录总帐凭证。</span><span class="sxs-lookup"><span data-stu-id="69d71-111">The general ledger voucher will be recorded at the scheduled time if resources are free to process this batch job on the server.</span></span> 
 
<span data-ttu-id="69d71-112">在 10.0.8 版本中，进行了改进以增强“异步”选项的性能。</span><span class="sxs-lookup"><span data-stu-id="69d71-112">In version 10.0.8, improvements were made to enhance the performance of the Asynchronous option.</span></span> <span data-ttu-id="69d71-113">在功能名称 **子分类帐转移到总帐性能优化** 下启用了此功能。</span><span class="sxs-lookup"><span data-stu-id="69d71-113">This feature is enabled under the feature name **Subledger transfer to General Ledger performance optimization**.</span></span> 
 
<span data-ttu-id="69d71-114">此功能改善了从子分类帐到总分类帐的数据转移。</span><span class="sxs-lookup"><span data-stu-id="69d71-114">This functionality improves the transfer of data from the subledger to the general ledger.</span></span> <span data-ttu-id="69d71-115">它使流程更加高效，并将更小的交易集组合在一起进行转移。</span><span class="sxs-lookup"><span data-stu-id="69d71-115">It allows the process to be more efficient, and it groups together sets of smaller transactions to transfer.</span></span> <span data-ttu-id="69d71-116">这样可以更有效地使用批处理服务器。</span><span class="sxs-lookup"><span data-stu-id="69d71-116">This allows for a more efficient use of the batch server.</span></span> <span data-ttu-id="69d71-117">此功能要求批处理服务器已设置、联机并正常运行，以使“异步转移”选项起作用。</span><span class="sxs-lookup"><span data-stu-id="69d71-117">This functionality requires that the batch server be set up, online, and functioning in order for the Asynchronous transfer option to work.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]