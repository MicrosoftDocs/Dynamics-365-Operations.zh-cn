---
title: 通过 Power Apps 和 Power Automate 扩展 Talent
description: 本文介绍 Microsoft Dynamics 365 Human Resources 的一些使用 Microsoft Power Apps 和 Microsoft Power Automate 的可扩展性方案示例。
author: negudava
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5b1ebe17063d954b52a0607d39e3ea08518adb89
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057590"
---
# <a name="extend-with-power-apps-and-power-automate"></a><span data-ttu-id="5b186-103">通过 Power Apps 和 Power Automate 扩展</span><span class="sxs-lookup"><span data-stu-id="5b186-103">Extend with Power Apps and Power Automate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5b186-104">本文介绍 Microsoft Dynamics 365 Human Resources 的一些使用 Microsoft Power Apps 和 Microsoft Power Automate 的可扩展性方案示例。</span><span class="sxs-lookup"><span data-stu-id="5b186-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Human Resources that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="5b186-105">可以将与各示例关联的解决方案包导入到您的 Power Apps 环境中。</span><span class="sxs-lookup"><span data-stu-id="5b186-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="5b186-106">然后可以将这些包用作指南或起点来实施适用于贵组织的方案。</span><span class="sxs-lookup"><span data-stu-id="5b186-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5b186-107">如果要“照原样”使用本主题中介绍的模板和应用，请务必测试这些模板和应用，以确保其涵盖特定于您的实施的所有方案。</span><span class="sxs-lookup"><span data-stu-id="5b186-107">If you want to use the templates and apps that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5b186-108">先决条件</span><span class="sxs-lookup"><span data-stu-id="5b186-108">Prerequisites</span></span>

- <span data-ttu-id="5b186-109">若要导入包，用户必须具有 **环境制造者** 权限。</span><span class="sxs-lookup"><span data-stu-id="5b186-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="5b186-110">若要导出或导入应用，用户必须拥有 Power Apps 计划 2 许可证或 Power Apps 计划 2 试用许可证。</span><span class="sxs-lookup"><span data-stu-id="5b186-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="integration-with-microsoft-365-power-automate"></a><span data-ttu-id="5b186-111">与 Microsoft 365 Power Automate 集成</span><span class="sxs-lookup"><span data-stu-id="5b186-111">Integration with Microsoft 365, Power Automate</span></span>

<span data-ttu-id="5b186-112">**与 Microsoft 365 集成** 应用可用于从 Microsoft 365 为已登录用户提取团队信息。</span><span class="sxs-lookup"><span data-stu-id="5b186-112">The **Integration with Microsoft 365** app can be used to extract team information for signed-in users from Microsoft 365.</span></span> <span data-ttu-id="5b186-113">它引用 Human Resources 中的工作人员来提取员工身份证明类型。</span><span class="sxs-lookup"><span data-stu-id="5b186-113">It references workers in Human Resources to extract employee identification types.</span></span> <span data-ttu-id="5b186-114">经理可以检查员工 ID 类型的到期日期。</span><span class="sxs-lookup"><span data-stu-id="5b186-114">Managers can check expiration dates of employee ID types.</span></span> <span data-ttu-id="5b186-115">如果员工 ID 类型即将到期，他们还可以发送电子邮件提醒。</span><span class="sxs-lookup"><span data-stu-id="5b186-115">They can also send an email reminder if the employee ID type is expiring.</span></span> <span data-ttu-id="5b186-116">Power Automate 与 Power Apps 集成来发送此提醒。</span><span class="sxs-lookup"><span data-stu-id="5b186-116">Power Automate integrates with Power Apps to send this reminder.</span></span> <span data-ttu-id="5b186-117">发送提醒后，确认将从 Power Automate 发送回 Power Apps。</span><span class="sxs-lookup"><span data-stu-id="5b186-117">Confirmation will be sent back to Power Apps from Power Automate when the reminder is sent.</span></span> <span data-ttu-id="5b186-118">身份证明类型包括驾照、护照和其他可接受的 ID 形式。</span><span class="sxs-lookup"><span data-stu-id="5b186-118">Identification types include driver's license, passport, and other acceptable forms of ID.</span></span>

<span data-ttu-id="5b186-119">您可以扩展此应用来处理其他场景。</span><span class="sxs-lookup"><span data-stu-id="5b186-119">You can extend this app for other scenarios.</span></span> <span data-ttu-id="5b186-120">例如，可以使用它来显示团队休假信息、日历事件和团队特定的任何事件。</span><span class="sxs-lookup"><span data-stu-id="5b186-120">For example, you can use it to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="5b186-121">若要下载 **与 Microsoft 365 Power Automate 集成** 应用，请转到 Microsoft 下载中心中的[与 Microsoft 365 集成](https://go.microsoft.com/fwlink/?linkid=2081787)。</span><span class="sxs-lookup"><span data-stu-id="5b186-121">To download the **Integration with Microsoft 365, Power Automate** app, go to [Integration with Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="5b186-122">Power Automate – SQL 连接和执行</span><span class="sxs-lookup"><span data-stu-id="5b186-122">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="5b186-123">**Power Automate – SQL 连接和执行** 模板连接到 Microsoft SQL Server 并让 SQL 查询运行。</span><span class="sxs-lookup"><span data-stu-id="5b186-123">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="5b186-124">虽然此模板读取和更新 SQL 表，但是您可以对其进行扩展，然后将其用于其他场景。</span><span class="sxs-lookup"><span data-stu-id="5b186-124">Although this template reads and updates SQL tables, you can extend it and use it for other scenarios.</span></span> <span data-ttu-id="5b186-125">例如，可将其用于使用来自 SQL Server 的记录填充 Dataverse 中的暂存表，以及通过使用来自 SQL Server 的增量推送定期同步暂存表。</span><span class="sxs-lookup"><span data-stu-id="5b186-125">For example, you can use it to fill a staging table in Dataverse with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="5b186-126">“高级查询”已与 Flow 集成，以实现数据转换和增量推送。</span><span class="sxs-lookup"><span data-stu-id="5b186-126">Advanced Query is integrated with Flow to enable Data transformation and incremental push.</span></span>

<span data-ttu-id="5b186-127">若要下载 **Power Automate – SQL 连接和执行** 模板和自定义实体结构，请转至 Microsoft 下载中心中的 [Power Automate – SQL 连接和执行](https://go.microsoft.com/fwlink/?linkid=2081789)。</span><span class="sxs-lookup"><span data-stu-id="5b186-127">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5b186-128">其他资源</span><span class="sxs-lookup"><span data-stu-id="5b186-128">Additional resources</span></span>

[<span data-ttu-id="5b186-129">该 Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="5b186-129">The Microsoft Power Platform</span></span>](/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]