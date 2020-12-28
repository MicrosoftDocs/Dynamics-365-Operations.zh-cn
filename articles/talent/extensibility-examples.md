---
title: 通过 Power Apps 和 Power Automate 扩展 Talent
description: 本文介绍 Microsoft Dynamics 365 Talent - Attract 的一些使用 Microsoft Power Apps 和 Microsoft Power Automate 的可扩展性方案示例。
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: cfdf36e9486aa4853d3bf674afa73ec3a4d1c161
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529626"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="23924-103">通过 Power Apps 和 Power Automate 扩展 Talent</span><span class="sxs-lookup"><span data-stu-id="23924-103">Extend Talent with Power Apps and Power Automate</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="23924-104">本文介绍 Microsoft Dynamics 365 Talent: Attract 的一些使用 Microsoft Power Apps 和 Microsoft Power Automate 的可扩展性方案示例。</span><span class="sxs-lookup"><span data-stu-id="23924-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent: Attract that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="23924-105">可以将与各示例关联的解决方案包导入到您的 Power Apps 环境中。</span><span class="sxs-lookup"><span data-stu-id="23924-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="23924-106">然后可以将这些包用作指南或起点来实施适用于贵组织的方案。</span><span class="sxs-lookup"><span data-stu-id="23924-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="23924-107">如果要“照原样”使用本文中介绍的模板和应用，请务必测试这些模板和应用，以确保其涵盖特定于您的实施的所有方案。</span><span class="sxs-lookup"><span data-stu-id="23924-107">If you want to use the templates and app that are described in this article "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="23924-108">先决条件</span><span class="sxs-lookup"><span data-stu-id="23924-108">Prerequisites</span></span>

- <span data-ttu-id="23924-109">若要导入包，用户必须具有 **环境制造者** 权限。</span><span class="sxs-lookup"><span data-stu-id="23924-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="23924-110">若要导出或导入应用，用户必须拥有 Power Apps 计划 2 许可证或 Power Apps 计划 2 试用许可证。</span><span class="sxs-lookup"><span data-stu-id="23924-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="23924-111">Power Automate – 表连接</span><span class="sxs-lookup"><span data-stu-id="23924-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="23924-112">**Power Automate – 表连接** 模板可用于从 Microsoft Forms 读取数据并存储到 Common Data Service 实体中。</span><span class="sxs-lookup"><span data-stu-id="23924-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="23924-113">可扩展此模板，以使其可用于其他方案。</span><span class="sxs-lookup"><span data-stu-id="23924-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="23924-114">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="23924-114">Here are some examples:</span></span>

- <span data-ttu-id="23924-115">捕获应聘者评估。</span><span class="sxs-lookup"><span data-stu-id="23924-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="23924-116">捕获课程调查表的结果。</span><span class="sxs-lookup"><span data-stu-id="23924-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="23924-117">为人力资源 (HR) 管理员编译面试问题库。</span><span class="sxs-lookup"><span data-stu-id="23924-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="23924-118">捕获应聘者的面试流程评估</span><span class="sxs-lookup"><span data-stu-id="23924-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="23924-119">在 Microsoft Dynamics 365: Attract 中，可以使用应聘者门户中的窗体，应聘者将在其中填写详细信息。</span><span class="sxs-lookup"><span data-stu-id="23924-119">In Microsoft Dynamics 365: Attract, you can use forms in the candidate portal, where candidates fill in details.</span></span> <span data-ttu-id="23924-120">也可以将窗体作为活动嵌入到工作模板中。</span><span class="sxs-lookup"><span data-stu-id="23924-120">You can also embed forms as activities in a job template.</span></span>

<span data-ttu-id="23924-121">应聘者提交窗体时，Microsoft Power Automate 捕获窗体提交，读取数据，然后将其存储到 Common Data Service 实体中。</span><span class="sxs-lookup"><span data-stu-id="23924-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="23924-122">若要下载 **Power Automate – 表连接** 模板和自定义实体结构，请转至 Microsoft 下载中心中的 [Power Automate – 表连接](https://go.microsoft.com/fwlink/?linkid=2081988)。</span><span class="sxs-lookup"><span data-stu-id="23924-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="23924-123">Power Automate – SharePoint 集成</span><span class="sxs-lookup"><span data-stu-id="23924-123">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="23924-124">**Power Automate – SharePoint 集成** 模板可用于从 Microsoft SharePoint 列表读取数据，将该列表与任何 Common Data Service 实体的字段值进行比较，以及将比较结果以通知电子邮件的形式发送。</span><span class="sxs-lookup"><span data-stu-id="23924-124">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="23924-125">组织可能有一组急需的技能。</span><span class="sxs-lookup"><span data-stu-id="23924-125">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="23924-126">这些技能可以以 SharePoint 列表的形式存储在 SharePoint 中。</span><span class="sxs-lookup"><span data-stu-id="23924-126">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="23924-127">当应聘者申请列出了一组必需技能的任何工作时，如果应聘者的技能与 SharePoint 中存储的技能之间匹配度极高，将发送通知电子邮件。</span><span class="sxs-lookup"><span data-stu-id="23924-127">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="23924-128">这有助于更快填充急需职位，因为通知会帮助招聘人员联系应聘者和在整个组织中交叉招聘应聘者。</span><span class="sxs-lookup"><span data-stu-id="23924-128">This helps fill positions that are urgently required faster, because the notifications help recruiters cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="23924-129">可扩展此模板，以便其可用于涉及 SharePoint 集成的任何方案。</span><span class="sxs-lookup"><span data-stu-id="23924-129">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="23924-130">若要下载 **Power Automate – SharePoint 集成** 模板，请转到 Microsoft 下载中心中的 [Power Automate – SharePoint 集成](https://go.microsoft.com/fwlink/?linkid=2082109)。</span><span class="sxs-lookup"><span data-stu-id="23924-130">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="23924-131">Referral 应用</span><span class="sxs-lookup"><span data-stu-id="23924-131">Referral App</span></span>

<span data-ttu-id="23924-132">您可以使用 Referral 应用将应聘者添加到共享人才池。</span><span class="sxs-lookup"><span data-stu-id="23924-132">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="23924-133">引荐人在提交应聘者时可以输入 **名字**、**姓氏**、**电子邮件** 和 **LinkedIn URL**。</span><span class="sxs-lookup"><span data-stu-id="23924-133">The referrer can enter **Firstname**, **Lastname**, **Email**, and **LinkedIn URL** when submitting a candidate.</span></span> <span data-ttu-id="23924-134">应聘者源元数据然后会使用引荐人的信息填充。</span><span class="sxs-lookup"><span data-stu-id="23924-134">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="23924-135">您可以将此应用嵌入到员工自助服务中来提交引荐，或者可以将其用作企业门户中的超链接，也可以作为独立应用运行。</span><span class="sxs-lookup"><span data-stu-id="23924-135">You can embed this app in Employee self service for submitting referrals, or you can use it as a hyperlink in the corporate portal and run it as a stand-alone app.</span></span>

<span data-ttu-id="23924-136">要下载 **Referral 应用**，在 Microsoft 下载中心转到 [Dynamics 365 Talent 可扩展性解决方案：Referral 应用](https://www.microsoft.com/download/details.aspx?id=58497)。</span><span class="sxs-lookup"><span data-stu-id="23924-136">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](https://www.microsoft.com/download/details.aspx?id=58497) on the Microsoft Download Center.</span></span> <span data-ttu-id="23924-137">您可以导入此应用并对其进行自定义来添加其他功能。</span><span class="sxs-lookup"><span data-stu-id="23924-137">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="23924-138">其他资源</span><span class="sxs-lookup"><span data-stu-id="23924-138">Additional resources</span></span>

[<span data-ttu-id="23924-139">该 Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="23924-139">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[<span data-ttu-id="23924-140">在租户与环境之间迁移应用</span><span class="sxs-lookup"><span data-stu-id="23924-140">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
