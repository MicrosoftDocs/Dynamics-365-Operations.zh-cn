---
title: 同步导入作业中的日期和时间
description: 在导入作业中使用 UTC 时区来避免时区转换出现问题。
author: Sunil-Garg
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41c0ec805a20a525989e0133e5dffb29ce3fed39
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748661"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a><span data-ttu-id="cca49-103">同步导入作业中的日期和时间</span><span class="sxs-lookup"><span data-stu-id="cca49-103">Synchronize date and time in import jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cca49-104">将导入作业的时区设置为协调世界时 (UTC) 很重要。</span><span class="sxs-lookup"><span data-stu-id="cca49-104">It's important to set the time zone for your import job to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="cca49-105">如果使用其他设置，您可能会在导入的数据中看到意外的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="cca49-105">You might see unexpected dates and times in your imported data if you use a different setting.</span></span> <span data-ttu-id="cca49-106">没有正确的设置，导入流程会将 UTC 日期转换为本地格式，然后系统设置会将其再次转换。</span><span class="sxs-lookup"><span data-stu-id="cca49-106">Without the correct setting, the import process converts the UTC date to the local format, and then system settings converts it again.</span></span>

<span data-ttu-id="cca49-107">这种双重转换会导致日期在应用程序之间更改。</span><span class="sxs-lookup"><span data-stu-id="cca49-107">This dual conversion causes dates to change between applications.</span></span> <span data-ttu-id="cca49-108">例如，由于本地时区的差异，双重转换可能导致 Dynamics 365 Human Resources 和 Dynamics 365 Finance 之间的员工开始日期不同。</span><span class="sxs-lookup"><span data-stu-id="cca49-108">For example, the dual conversion could cause an employee's start date to be different between Dynamics 365 Human Resources and Dynamics 365 Finance due to differences in local time zones.</span></span> <span data-ttu-id="cca49-109">将导入作业设置为 UTC 可以解决此问题。</span><span class="sxs-lookup"><span data-stu-id="cca49-109">Setting the import job to UTC resolves this problem.</span></span>

1. <span data-ttu-id="cca49-110">在 Dynamics 365 Finance and Operations 中，选择 **数据管理**。</span><span class="sxs-lookup"><span data-stu-id="cca49-110">In Dynamics 365 Finance and Operations, select **Data management**.</span></span>

2. <span data-ttu-id="cca49-111">选择 **导入项目**，然后选择项目。</span><span class="sxs-lookup"><span data-stu-id="cca49-111">Select **Import projects**, and then select the project.</span></span>

3. <span data-ttu-id="cca49-112">在 **源日期格式** 下，选择 **CSV-Unicode**。</span><span class="sxs-lookup"><span data-stu-id="cca49-112">Under **Source date format**, select **CSV-Unicode**.</span></span>

   <span data-ttu-id="cca49-113">[![将源日期格式更改为 UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span><span class="sxs-lookup"><span data-stu-id="cca49-113">[![Change source date format to UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span></span>

4. <span data-ttu-id="cca49-114">将 **时区** 更改为 **协调世界时区**，将 **语言** 更改为 **En-US**。</span><span class="sxs-lookup"><span data-stu-id="cca49-114">Change **Timezone** to **Coordinated Universal Timezone**, and change **Language** to **En-US**.</span></span>




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]