---
title: 定义生产流版本的到期日期
description: 若要在给定日期终止某个生产流版本的有效性和处理，或计划将某个有效版本替换为新版本，必须为该版本设置到期日期。
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 97ac33d28a49ad0f2a3956ad65b159e4ec4785c7
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983246"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a><span data-ttu-id="80134-103">定义生产流版本的到期日期</span><span class="sxs-lookup"><span data-stu-id="80134-103">Define an expiry date for a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="80134-104">若要在给定日期终止某个生产流版本的有效性和处理，或计划将某个有效版本替换为新版本，必须为该版本设置到期日期。</span><span class="sxs-lookup"><span data-stu-id="80134-104">To end the validity and the processing of a production flow version on a given date, or to plan replacement of an active version with a new version, you have to set an expiry date on the version.</span></span> <span data-ttu-id="80134-105">不必停用该版本。</span><span class="sxs-lookup"><span data-stu-id="80134-105">It is not necessary to deactivate the version.</span></span>


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a><span data-ttu-id="80134-106">设置到期日期以结束生产流版本</span><span class="sxs-lookup"><span data-stu-id="80134-106">Set an expiration date to end a production flow version</span></span>
1. <span data-ttu-id="80134-107">转到“生产控制”>“设置”>“精益生产流程”>“生产流程”。</span><span class="sxs-lookup"><span data-stu-id="80134-107">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="80134-108">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="80134-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="80134-109">选择已为其定义了版本的任何生产流。</span><span class="sxs-lookup"><span data-stu-id="80134-109">Select any production flow that has a version that is already defined.</span></span>  
3. <span data-ttu-id="80134-110">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="80134-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="80134-111">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="80134-111">Click Edit.</span></span>
5. <span data-ttu-id="80134-112">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="80134-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="80134-113">在“到期日期”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="80134-113">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="80134-114">对于到期日期，新版本将不启动或进入已激活状态。</span><span class="sxs-lookup"><span data-stu-id="80134-114">For the expiration date, a new version will not start or become activated.</span></span> <span data-ttu-id="80134-115">并且还不能为此生产流创建或启动作业。</span><span class="sxs-lookup"><span data-stu-id="80134-115">It will also no longer be possible to create or start jobs for this production flow.</span></span> <span data-ttu-id="80134-116">到期日期后，仍然可以完成已开始的作业。</span><span class="sxs-lookup"><span data-stu-id="80134-116">You can still complete started jobs after the expiration date.</span></span>  

