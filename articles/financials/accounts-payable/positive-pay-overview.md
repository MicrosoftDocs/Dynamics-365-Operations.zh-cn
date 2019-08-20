---
title: 付款确认概览
description: 本文提供有关付款确认的信息，其用于生成一份可以呈现给银行的支票电子列表。
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 2ba23cf5afe9f007f5e32a75e918595929ad79a1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834601"
---
# <a name="positive-pay-overview"></a><span data-ttu-id="b7611-103">付款确认概览</span><span class="sxs-lookup"><span data-stu-id="b7611-103">Positive pay overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7611-104">本文提供有关付款确认的信息，其用于生成一份可以呈现给银行的支票电子列表。</span><span class="sxs-lookup"><span data-stu-id="b7611-104">This article provides information about positive pay, which is used to generate an electronic list of checks that can be presented to a bank.</span></span> 

<span data-ttu-id="b7611-105">付款确认用于生成一份可以呈现给银行的支票电子列表。</span><span class="sxs-lookup"><span data-stu-id="b7611-105">Positive pay is used to generate an electronic list of checks that can be presented to a bank.</span></span> <span data-ttu-id="b7611-106">付款确认文件可以帮助银行防止支票欺诈。</span><span class="sxs-lookup"><span data-stu-id="b7611-106">Positive pay files can help banks prevent check fraud.</span></span> <span data-ttu-id="b7611-107">每次打印支票时，您设置付款确认以生成支票电子列表。</span><span class="sxs-lookup"><span data-stu-id="b7611-107">You set up positive pay to generate an electronic list of checks every time that checks are printed.</span></span> <span data-ttu-id="b7611-108">然后，当将支票提交给银行时，银行将支票与您以前提交的支票列表进行对比。</span><span class="sxs-lookup"><span data-stu-id="b7611-108">Then, when a check is presented to the bank, the bank compares the check with the list of checks that you previously submitted.</span></span> <span data-ttu-id="b7611-109">如果支票与列表中的支票相匹配，银行将清算支票。</span><span class="sxs-lookup"><span data-stu-id="b7611-109">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="b7611-110">如果支票与列表中的支票不匹配，银行将保留支票以供审查。</span><span class="sxs-lookup"><span data-stu-id="b7611-110">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

<span data-ttu-id="b7611-111">付款确认也称为 SafePay。</span><span class="sxs-lookup"><span data-stu-id="b7611-111">Positive pay is also known as SafePay.</span></span> 

<span data-ttu-id="b7611-112">付款确认文件可以包含有关收款人和支票金额的敏感信息。</span><span class="sxs-lookup"><span data-stu-id="b7611-112">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="b7611-113">因此，请您务必自文件生成时便使用相应的安全措施，直到它们由银行接收。</span><span class="sxs-lookup"><span data-stu-id="b7611-113">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="b7611-114">付款确认文件根据 Web 浏览器的下载说明下载。</span><span class="sxs-lookup"><span data-stu-id="b7611-114">Positive pay files are downloaded according to the download instructions for the web browser.</span></span> 

<span data-ttu-id="b7611-115">通过使用数据实体创建付款确认文件。</span><span class="sxs-lookup"><span data-stu-id="b7611-115">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="b7611-116">在您生成付款确认文件前，必须为将数据转换为银行可以使用的格式的 XML 设置转换格式。</span><span class="sxs-lookup"><span data-stu-id="b7611-116">Before you generate a positive pay file, you must set up the transformation formats for the XML that translates the data into a format that the bank can consume.</span></span> 

<span data-ttu-id="b7611-117">对于您想要生成付款确认信息的每个银行帐户，您必须分配付款确认格式。</span><span class="sxs-lookup"><span data-stu-id="b7611-117">For each bank account that you want to generate positive pay information for, you must assign the positive pay format.</span></span> <span data-ttu-id="b7611-118">在生成付款后，您可以生成用于一个法人和一个银行帐户的付款确认文件。</span><span class="sxs-lookup"><span data-stu-id="b7611-118">After you generate payments, you can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="b7611-119">或者，您可以同时为多个法人和银行帐户生成付款确认文件</span><span class="sxs-lookup"><span data-stu-id="b7611-119">Alternatively, you can generate positive pay files for multiple legal entities and bank accounts at the same time.</span></span> 

<span data-ttu-id="b7611-120">当付款确认文件中列出的支票支付后，您将从银行收到一个确认编号。</span><span class="sxs-lookup"><span data-stu-id="b7611-120">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="b7611-121">然后，您可以在 Microsoft Dynamics 365 for Finance and Operations 中确认付款确认文件。</span><span class="sxs-lookup"><span data-stu-id="b7611-121">You can then confirm the positive pay file in Microsoft Dynamics 365 for Finance and Operations.</span></span> 

<span data-ttu-id="b7611-122">如果您必须更改付款确认文件，您可以撤消它。</span><span class="sxs-lookup"><span data-stu-id="b7611-122">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="b7611-123">然后，对于付款确认文件中的每一张支票，将重置指示该支票是否包括在一个付款确认文件中的字段。</span><span class="sxs-lookup"><span data-stu-id="b7611-123">Then, for each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span>

<span data-ttu-id="b7611-124">有关详细信息，请参阅[设置和生成先对单再支付文件](set-up-generate-positive-pay-files.md)。</span><span class="sxs-lookup"><span data-stu-id="b7611-124">For more information, see [Set up and generate positive pay files](set-up-generate-positive-pay-files.md).</span></span>



