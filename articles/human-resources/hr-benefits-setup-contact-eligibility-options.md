---
title: 配置个人联系人资格选项
description: 在 Microsoft Dynamics 365 Human Resources 中为个人联系人配置资格选项。 个人联系人可以是受益人或依赖方。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a50c5e54d224a2f8607284eb105381ffb6ef7ad9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008245"
---
# <a name="configure-personal-contact-eligibility-options"></a><span data-ttu-id="cb16b-104">配置个人联系人资格选项</span><span class="sxs-lookup"><span data-stu-id="cb16b-104">Configure personal contact eligibility options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="cb16b-105">本文向您展示如何在 Microsoft Dynamics 365 Human Resources 中配置要在福利中使用的个人联系人的类型。</span><span class="sxs-lookup"><span data-stu-id="cb16b-105">This article shows you how to configure types of personal contacts to use in benefits in Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="cb16b-106">个人联系人可以是受益人或依赖方。</span><span class="sxs-lookup"><span data-stu-id="cb16b-106">Personal contacts can be beneficiaries or dependents.</span></span> 

1. <span data-ttu-id="cb16b-107">在**福利管理**工作区中，在**设置**下，选择**个人联系人资格选项**。</span><span class="sxs-lookup"><span data-stu-id="cb16b-107">In the **Benefits management** workspace, under **Setup**, select **Personal contact eligibility options**.</span></span>

2. <span data-ttu-id="cb16b-108">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="cb16b-108">Select **New**.</span></span>

3. <span data-ttu-id="cb16b-109">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="cb16b-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="cb16b-110">字段</span><span class="sxs-lookup"><span data-stu-id="cb16b-110">Field</span></span> | <span data-ttu-id="cb16b-111">说明</span><span class="sxs-lookup"><span data-stu-id="cb16b-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="cb16b-112">**资格选项**</span><span class="sxs-lookup"><span data-stu-id="cb16b-112">**Eligibility option**</span></span> | <span data-ttu-id="cb16b-113">用于标识资格选项的唯一资格选项名称或代码。</span><span class="sxs-lookup"><span data-stu-id="cb16b-113">A unique eligibility option name or code to identify the eligibility option.</span></span> |
   | <span data-ttu-id="cb16b-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="cb16b-114">**Description**</span></span> | <span data-ttu-id="cb16b-115">资格选项的简短描述。</span><span class="sxs-lookup"><span data-stu-id="cb16b-115">A brief description of the eligibility option.</span></span> |
   | <span data-ttu-id="cb16b-116">**联系人资格代码**</span><span class="sxs-lookup"><span data-stu-id="cb16b-116">**Contact eligibility code**</span></span> | <span data-ttu-id="cb16b-117">最准确描述个人资格选项的系统代码。</span><span class="sxs-lookup"><span data-stu-id="cb16b-117">The system code that best describes the personal eligibility option.</span></span> <span data-ttu-id="cb16b-118">您可以从以下各项中选择：</span><span class="sxs-lookup"><span data-stu-id="cb16b-118">You can choose from:</span></span> <ul><li><span data-ttu-id="cb16b-119">关系</span><span class="sxs-lookup"><span data-stu-id="cb16b-119">Relationship</span></span></li><li><span data-ttu-id="cb16b-120">学生</span><span class="sxs-lookup"><span data-stu-id="cb16b-120">Student</span></span></li><li><span data-ttu-id="cb16b-121">超龄依赖方</span><span class="sxs-lookup"><span data-stu-id="cb16b-121">Overage dependent</span></span></li><li><span data-ttu-id="cb16b-122">超出年限的禁用依赖方</span><span class="sxs-lookup"><span data-stu-id="cb16b-122">Over-aged disabled dependent</span></span></li></ul> |
   | <span data-ttu-id="cb16b-123">**状态**</span><span class="sxs-lookup"><span data-stu-id="cb16b-123">**Status**</span></span> | <span data-ttu-id="cb16b-124">资格选项的状态。</span><span class="sxs-lookup"><span data-stu-id="cb16b-124">The status of the eligibility option.</span></span> <span data-ttu-id="cb16b-125">如果资格选项的状态设置为无效，那么您不能为个人联系人选择该个人联系人资格选项。</span><span class="sxs-lookup"><span data-stu-id="cb16b-125">If the status for an eligibility option is set to inactive, then you can’t select that personal contact eligibility option for personal contacts.</span></span> |
   | <span data-ttu-id="cb16b-126">**关系**</span><span class="sxs-lookup"><span data-stu-id="cb16b-126">**Relationship**</span></span> | <span data-ttu-id="cb16b-127">指定个人联系人和员工之间的关系。</span><span class="sxs-lookup"><span data-stu-id="cb16b-127">Specifies the relationship between the personal contact and the employee.</span></span> <span data-ttu-id="cb16b-128">仅当联系人资格代码设置为“关系”时，此字段才有效。</span><span class="sxs-lookup"><span data-stu-id="cb16b-128">This field is only active if the contact eligibility code is set to Relationship.</span></span> |
   | <span data-ttu-id="cb16b-129">**帐龄**</span><span class="sxs-lookup"><span data-stu-id="cb16b-129">**Age**</span></span> | <span data-ttu-id="cb16b-130">福利计划的合格个人联系人的最大年龄。</span><span class="sxs-lookup"><span data-stu-id="cb16b-130">The maximum age of an eligible personal contact for the benefit plan.</span></span> <span data-ttu-id="cb16b-131">仅在选择关系时此字段才有效。</span><span class="sxs-lookup"><span data-stu-id="cb16b-131">This field is only active if you select a relationship.</span></span> <span data-ttu-id="cb16b-132">此年龄将与计算出的个人联系人的年龄进行比较。</span><span class="sxs-lookup"><span data-stu-id="cb16b-132">This age is compared with the calculated age of the personal contact.</span></span> <span data-ttu-id="cb16b-133">计算的年龄为：（覆盖范围日期 – 个人联系人的出生日期/365）。</span><span class="sxs-lookup"><span data-stu-id="cb16b-133">Calculated age is: (Coverage date – personal contact birth date / 365).</span></span> <span data-ttu-id="cb16b-134">此数字始终是整数。</span><span class="sxs-lookup"><span data-stu-id="cb16b-134">This number is always an integer.</span></span> |

4. <span data-ttu-id="cb16b-135">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="cb16b-135">Select **Save**.</span></span> 
