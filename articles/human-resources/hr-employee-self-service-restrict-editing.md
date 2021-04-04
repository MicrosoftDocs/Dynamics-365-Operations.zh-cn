---
title: 限制对个人信息的编辑
description: 限制员工在 Dynamics 365 Human Resources 中编辑联系人详细信息。
author: andreabichsel
manager: tfehr
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d4785232dbb21c5f8a800497fb0cfd3c64dea2d8
ms.sourcegitcommit: 45d10d0c25b3ec585323709bb97ba1895b500429
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2021
ms.locfileid: "5503028"
---
# <a name="restrict-editing-of-personal-information"></a><span data-ttu-id="f25c6-103">限制对个人信息的编辑</span><span class="sxs-lookup"><span data-stu-id="f25c6-103">Restrict editing of personal information</span></span>

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

<span data-ttu-id="f25c6-104">本主题介绍如何限制员工在 Dynamics 365 Human Resources 中编辑联系人详细信息。</span><span class="sxs-lookup"><span data-stu-id="f25c6-104">This topic describes how to restrict employees from editing contact details in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="f25c6-105">您可能希望阻止员工编辑某些联系人详细信息，如他们的营业地点或电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="f25c6-105">You might want to prevent employees from editing certain contact details, such as their business location or email address.</span></span>

> [!NOTE]
> <span data-ttu-id="f25c6-106">要使用此功能，必须首先在“功能管理”中启用 **(预览)限制员工出于选择目的添加或编辑地址和联系信息**。</span><span class="sxs-lookup"><span data-stu-id="f25c6-106">To use this feature, you must first enable **(Preview) Restrict employees from adding or editing address and contact information for select purposes** in Feature management.</span></span> <span data-ttu-id="f25c6-107">有关启用预览功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。</span><span class="sxs-lookup"><span data-stu-id="f25c6-107">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span><br><br><span data-ttu-id="f25c6-108">![启用预览功能](./media/hr-employee-self-service-restrict-enable.png)</span><span class="sxs-lookup"><span data-stu-id="f25c6-108">![Enable preview feature](./media/hr-employee-self-service-restrict-enable.png)</span></span>

## <a name="choose-the-information-an-employee-can-add-or-edit"></a><span data-ttu-id="f25c6-109">选择员工可以添加或编辑的信息</span><span class="sxs-lookup"><span data-stu-id="f25c6-109">Choose the information an employee can add or edit</span></span>

1. <span data-ttu-id="f25c6-110">在 Human Resources 中，选择 **人事管理**，选择 **链接**，然后选择 **人力资源参数**。</span><span class="sxs-lookup"><span data-stu-id="f25c6-110">In Human Resources, select **Personnel management**, select **Links**, and then select **Human resources parameters**.</span></span>

   ![转到“人力资源参数”](./media/hr-employee-self-service-human-resources-parameters.png)

2. <span data-ttu-id="f25c6-112">在 **人力资源参数** 页上，选择 **员工自助服务** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="f25c6-112">On the **Human resources parameters** page, select the **Employee self service** tab.</span></span>

   ![选择“员工自助服务”](./media/hr-employee-self-service-tab.png)

3. <span data-ttu-id="f25c6-114">在 **员工自助服务** 选项卡上，取消选中 **地址和联系信息** 部分您不希望员工添加或编辑的所有信息。</span><span class="sxs-lookup"><span data-stu-id="f25c6-114">On the **Employee self service** tab, uncheck all information in the **Address and contact information** section that you don't want employees to add or edit.</span></span> <span data-ttu-id="f25c6-115">在此示例中，我们取消选中了 **业务** 联系人信息。</span><span class="sxs-lookup"><span data-stu-id="f25c6-115">In this example, we've unchecked **Business** contact information.</span></span>

   ![限制编辑业务联系人信息](./media/hr-employee-self-service-restrict-business.png)

4. <span data-ttu-id="f25c6-117">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="f25c6-117">Select **Save**.</span></span>

   ![保存更改](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a><span data-ttu-id="f25c6-119">员工体验</span><span class="sxs-lookup"><span data-stu-id="f25c6-119">Employee experience</span></span>

<span data-ttu-id="f25c6-120">限制员工添加或编辑联系人详细信息后，他们可以查看信息，但不能更改。</span><span class="sxs-lookup"><span data-stu-id="f25c6-120">After you've restricted employees from adding or editing contact details, they can see the information, but can't change it.</span></span>

<span data-ttu-id="f25c6-121">在此示例中，在限制员工编辑 **业务** 联系人详细信息时，他们仍然可以在员工自助服务中看到该信息：</span><span class="sxs-lookup"><span data-stu-id="f25c6-121">In this example, where employees are restricted from editing **Business** contact details, they can still see the information in Employee self service:</span></span>

![查看业务联系人详细信息](./media/hr-employee-self-service-restrict-view.png)

<span data-ttu-id="f25c6-123">但是，当他们选择业务联系人详细信息时，**编辑地址** 窗格显示为只读，他们无法更改任何字段。</span><span class="sxs-lookup"><span data-stu-id="f25c6-123">However, when they select the business contact details, the **Edit address** pane appears as read-only, and they can't change any of the fields.</span></span>

![业务联系人详细信息显示为只读](./media/hr-employee-self-service-restrict-read-only.png)

<span data-ttu-id="f25c6-125">而且，如果他们选择 **添加** 来添加新地址，也无法从 **用途** 下拉框中选择 **业务**。</span><span class="sxs-lookup"><span data-stu-id="f25c6-125">In addition, if they select **Add** to add a new address, they can't select **Business** from the **Purpose** dropdown box.</span></span>

![员工无法添加业务地址](./media/hr-employee-self-service-restrict-add.png)

<span data-ttu-id="f25c6-127">当员工在 **个人信息** 页选择 **联系人详细信息** 和添加新地址时，他们将获得相同的体验。</span><span class="sxs-lookup"><span data-stu-id="f25c6-127">Employees get the same experience when they select **Contact details** on the **Personal information** page and add a new address.</span></span> <span data-ttu-id="f25c6-128">**用途** 下拉框仅显示他们可以添加的信息类型。</span><span class="sxs-lookup"><span data-stu-id="f25c6-128">The **Purpose** dropdown box only displays the types of information they can add.</span></span> 

![员工无法在“用途”下拉框中选择“业务”](./media/hr-employee-self-service-restrict-purpose.png)

<span data-ttu-id="f25c6-130">**联系人详细信息** 现在在网格中显示 **用途**。</span><span class="sxs-lookup"><span data-stu-id="f25c6-130">**Contact details** now shows **Purpose** in the grid.</span></span>

![在联系人详细信息网格中显示用途](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a><span data-ttu-id="f25c6-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="f25c6-132">See also</span></span>

[<span data-ttu-id="f25c6-133">员工和经理自助服务概览</span><span class="sxs-lookup"><span data-stu-id="f25c6-133">Employee and Manager self service overview</span></span>](hr-employee-manager-self-service-overview.md)<br>
[<span data-ttu-id="f25c6-134">配置 Human Resources 参数</span><span class="sxs-lookup"><span data-stu-id="f25c6-134">Configure Human resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="f25c6-135">编辑个人信息</span><span class="sxs-lookup"><span data-stu-id="f25c6-135">Edit personal information</span></span>](hr-employee-manager-self-service-edit-personal-information.md)