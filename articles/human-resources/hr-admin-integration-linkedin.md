---
title: 与 LinkedIn Talent Hub 集成
description: 本主题介绍了如何设置 Microsoft Dynamics 365 Human Resources 与 LinkedIn Talent Hub 之间的集成。
author: jaredha
manager: tfehr
ms.date: 10/20/2020
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
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4fda9d85b459d233e6239f3fcffbb48e596d4085
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111699"
---
# <a name="integrate-with-linkedin-talent-hub"></a><span data-ttu-id="cfe1c-103">与 LinkedIn Talent Hub 集成</span><span class="sxs-lookup"><span data-stu-id="cfe1c-103">Integrate with LinkedIn Talent Hub</span></span>

[!include [banner](includes/preview-feature.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="cfe1c-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) 是申请人跟踪系统 (ATS) 平台。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) is an applicant tracking system (ATS) platform.</span></span> <span data-ttu-id="cfe1c-105">通过此一体式平台，您可以找到、管理和雇用员工。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-105">It lets you source, manage, and hire employees all in one place.</span></span> <span data-ttu-id="cfe1c-106">通过将 Microsoft Dynamics 365 Human Resources 与 LinkedIn Talent Hub 集成，您可以轻松地在 Human Resources 中为已被聘请担任某职位的申请人创建员工记录。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-106">By integrating Microsoft Dynamics 365 Human Resources with LinkedIn Talent Hub, you can easily create employee records in Human Resources for applicants who have been hired for a position.</span></span>

## <a name="setup"></a><span data-ttu-id="cfe1c-107">设置</span><span class="sxs-lookup"><span data-stu-id="cfe1c-107">Setup</span></span>

<span data-ttu-id="cfe1c-108">系统管理员必须完成设置任务才能与 LinkedIn Talent Hub 集成。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-108">A system administrator must complete setup tasks to enable integration with LinkedIn Talent Hub.</span></span> <span data-ttu-id="cfe1c-109">首先，在 Power Apps 环境中，您必须设置用户和安全角色，以授予 LinkedIn Talent Hub 适当的权限来将数据写入 Human Resources 中。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-109">First, in the Power Apps environment, you must set up a user and security role to grant LinkedIn Talent Hub the appropriate permissions to write data into Human Resources.</span></span>

### <a name="link-your-environment-to-linkedin-talent-hub"></a><span data-ttu-id="cfe1c-110">将您的环境链接到 LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="cfe1c-110">Link your environment to LinkedIn Talent Hub</span></span>

1. <span data-ttu-id="cfe1c-111">打开 [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub)。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-111">Open [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span></span>

2. <span data-ttu-id="cfe1c-112">在用户下拉菜单上，选择 **产品设置**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-112">On the user drop-down menu, select **Product Settings**.</span></span>

3. <span data-ttu-id="cfe1c-113">在左侧导航窗格的 **高级** 部分中，选择 **集成**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-113">In the left navigation pane, in the **Advanced** section, select **Integrations**.</span></span>

4. <span data-ttu-id="cfe1c-114">针对 Microsoft Dynamics 365 Human Resources 集成选择 **授权**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-114">Select **Authorize** for the Microsoft Dynamics 365 Human Resources integration.</span></span>

5. <span data-ttu-id="cfe1c-115">在 **Dynamics 365 Human Resources** 页面上，选择 LinkedIn Talent Hub 要链接到的环境，然后选择 **链接**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-115">On the **Dynamics 365 Human Resources** page, select the environment to link LinkedIn Talent Hub to, and then select **Link**.</span></span>

    ![LinkedIn Talent Hub 入职](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > <span data-ttu-id="cfe1c-117">您只能链接到用户帐户对 Human Resources 环境以及关联的 Power Apps 环境具有管理员访问权限的环境。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-117">You can link only to environments where your user account has administrator access to both the Human Resources environment and the associated Power Apps environment.</span></span> <span data-ttu-id="cfe1c-118">如果 Human Resources 链接页面上未列出任何环境，请确保已在租户上获得了 Human Resources 环境的许可，并且您以该身份登录到链接页面的用户对 Human Resources 环境和 Power Apps 环境具有管理员权限。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-118">If no environments are listed on the Human Resources link page, make sure that you have licensed Human Resources environments on the tenant, and that the user that you signed in to the link page as has administrator permissions to both the Human Resources environment and the Power Apps environment.</span></span>

### <a name="create-a-power-apps-security-role"></a><span data-ttu-id="cfe1c-119">创建 Power Apps 安全角色</span><span class="sxs-lookup"><span data-stu-id="cfe1c-119">Create a Power Apps security role</span></span>

1. <span data-ttu-id="cfe1c-120">打开 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com)。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="cfe1c-121">在 **环境** 列表中，选择与您要将 LinkedIn Talent Hub 实例链接到的 Human Resources 环境相关联的环境。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-121">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="cfe1c-122">选择 **设置**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-122">Select **Settings**.</span></span>

4. <span data-ttu-id="cfe1c-123">展开 **用户 + 权限** 节点，然后选择 **安全角色**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-123">Expand the **Users + Permissions** node, and select **Security Roles**.</span></span>

5. <span data-ttu-id="cfe1c-124">在 **安全角色** 页面的工具栏上，选择 **新建角色**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-124">On the **Security Roles** page, on the toolbar, select **New role**.</span></span>

6. <span data-ttu-id="cfe1c-125">在 **详细信息** 选项卡上，输入角色名称，例如 **LinkedIn Talent Hub HRIS 集成**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-125">On the **Details** tab, enter a name for the role, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>

7. <span data-ttu-id="cfe1c-126">在 **自定义** 选项卡上，为以下实体选择组织级别的 **读取** 权限：</span><span class="sxs-lookup"><span data-stu-id="cfe1c-126">On the **Customization** tab, select organization-level **Read** permission for the following entities:</span></span>

    - <span data-ttu-id="cfe1c-127">实体</span><span class="sxs-lookup"><span data-stu-id="cfe1c-127">Entity</span></span>
    - <span data-ttu-id="cfe1c-128">字段</span><span class="sxs-lookup"><span data-stu-id="cfe1c-128">Field</span></span>
    - <span data-ttu-id="cfe1c-129">关系</span><span class="sxs-lookup"><span data-stu-id="cfe1c-129">Relationship</span></span>

8. <span data-ttu-id="cfe1c-130">保存并关闭安全角色。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-130">Save and close the security role.</span></span>

### <a name="create-a-power-apps-application-user"></a><span data-ttu-id="cfe1c-131">创建 Power Apps 申请用户</span><span class="sxs-lookup"><span data-stu-id="cfe1c-131">Create a Power Apps application user</span></span>

<span data-ttu-id="cfe1c-132">必须为 LinkedIn Talent Hub 适配器创建申请用户，以授予该适配器的权限来将应聘者记录写入 Power Apps 环境中。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-132">An application user must be created for the LinkedIn Talent Hub adapter to grant permissions to the adapter to write candidate records into the Power Apps environment.</span></span>

1. <span data-ttu-id="cfe1c-133">打开 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com)。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-133">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="cfe1c-134">在 **环境** 列表中，选择与您要将 LinkedIn Talent Hub 实例链接到的 Human Resources 环境相关联的环境。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-134">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="cfe1c-135">选择 **设置**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-135">Select **Settings**.</span></span>

4. <span data-ttu-id="cfe1c-136">展开 **用户 + 权限** 节点，然后选择 **用户**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-136">Expand the **Users + Permissions** node, and select **Users**.</span></span>

5. <span data-ttu-id="cfe1c-137">选择 **管理 Dynamics 365 中的用户**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-137">Select **Manage users in Dynamics 365**.</span></span>

6. <span data-ttu-id="cfe1c-138">使用列表上方的下拉菜单将视图从默认的 **已启用用户** 视图更改为 **申请用户**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-138">Use the drop-down menu above the list to change the view from the default **Enabled Users** view to **Application Users**.</span></span>

    ![申请用户视图](./media/hr-admin-integration-power-apps-application-users.jpg)

7. <span data-ttu-id="cfe1c-140">在工具栏上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-140">On the toolbar, select **New**.</span></span>

8. <span data-ttu-id="cfe1c-141">在 **新建用户** 页面上，执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="cfe1c-141">On the **New user** page, follow these steps:</span></span>

    1. <span data-ttu-id="cfe1c-142">将 **用户类型** 字段的值更改为 **申请用户**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-142">Change the value of the **User type** field to **Application User**.</span></span>
    2. <span data-ttu-id="cfe1c-143">将 **用户名** 字段设置为 **Dynamics365 HR LinkedIn HRIS 集成**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-143">Set the **User Name** field to **Dynamics365 HR LinkedIn HRIS Integration**.</span></span>
    3. <span data-ttu-id="cfe1c-144">将 **申请 ID** 字段设置为 **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-144">Set the **Application ID** field to **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    4. <span data-ttu-id="cfe1c-145">在 **名字**、**姓氏** 和 **主要电子邮件** 字段中输入任何值。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-145">Enter any value in the **First Name**, **Last Name**, and **Primary Email** fields.</span></span>
    5. <span data-ttu-id="cfe1c-146">在工具栏上，选择 **保存 \& 关闭**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-146">On the toolbar, select **Save \& Close**.</span></span>

### <a name="assign-a-security-role-to-the-new-user"></a><span data-ttu-id="cfe1c-147">为新用户分配安全角色</span><span class="sxs-lookup"><span data-stu-id="cfe1c-147">Assign a security role to the new user</span></span>

<span data-ttu-id="cfe1c-148">保存并关闭上一部分中的新申请用户后，您将返回到 **用户列表** 页面。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-148">After you save and close the new application user in the previous section, you're returned to the **Users list** page.</span></span>

1. <span data-ttu-id="cfe1c-149">在 **用户列表** 页面上，将视图更改为 **申请用户**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-149">On the **Users list** page, change the view to **Application Users**.</span></span>

2. <span data-ttu-id="cfe1c-150">选择在上一部分中创建的申请用户。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-150">Select the application user that you created in the previous section.</span></span>

3. <span data-ttu-id="cfe1c-151">在工具栏上，选择 **管理角色**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-151">On the toolbar, select **Manage Roles**.</span></span>

4. <span data-ttu-id="cfe1c-152">选择您之前为集成创建的安全角色。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-152">Select the security role that you created earlier for the integration.</span></span>

5. <span data-ttu-id="cfe1c-153">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-153">Select **OK**.</span></span>

### <a name="add-an-azure-active-directory-app-in-human-resources"></a><span data-ttu-id="cfe1c-154">在 Human Resources 中添加 Azure Active Directory 应用</span><span class="sxs-lookup"><span data-stu-id="cfe1c-154">Add an Azure Active Directory app in Human Resources</span></span>

1. <span data-ttu-id="cfe1c-155">在 Dynamics 365 Human Resources 中，打开 **Azure Active Directory 应用程序** 页面。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-155">In Dynamics 365 Human Resources, open the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="cfe1c-156">将新记录添加到列表，然后设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="cfe1c-156">Add a new record to the list, and set the following fields:</span></span>

    - <span data-ttu-id="cfe1c-157">**客户端 ID**：输入 **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-157">**Client ID**: Enter **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    - <span data-ttu-id="cfe1c-158">**名称**：输入您之前创建的 Power Apps 安全角色的名称，例如 **LinkedIn Talent Hub HRIS 集成**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-158">**Name**: Enter the name of the Power Apps security role that you created earlier, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>
    - <span data-ttu-id="cfe1c-159">**用户 ID**：选择具有在“人员管理”中写入数据的权限的用户。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-159">**User ID**: Select a user who has permissions to write data in Personnel Management.</span></span>

### <a name="create-the-table-in-dataverse"></a><span data-ttu-id="cfe1c-160">在 Dataverse 中创建表</span><span class="sxs-lookup"><span data-stu-id="cfe1c-160">Create the table in Dataverse</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cfe1c-161">与 LinkedIn Talent Hub 的集成取决于适用于 Human Resources 的 Dataverse 中的虚拟表。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-161">The integration with LinkedIn Talent Hub depends on virtual tables in Dataverse for Human Resources.</span></span> <span data-ttu-id="cfe1c-162">作为设置中此步骤的先决条件，必须配置虚拟表。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-162">As a prerequisite for this step in the setup, you must configure virtual tables.</span></span> <span data-ttu-id="cfe1c-163">有关如何配置虚拟表的信息，请参阅[配置 Dataverse 虚拟表](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities)。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-163">For information about how to configure virtual tables, see [Configure Dataverse virtual tables](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span></span>

1. <span data-ttu-id="cfe1c-164">在 Human Resources 中，打开 **Dataverse 集成** 页面。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-164">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="cfe1c-165">选择 **虚拟表** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-165">Select the **Virtual tables** tab.</span></span>

3. <span data-ttu-id="cfe1c-166">按实体标签筛选实体列表以查找 **LinkedIn 导出的应聘者**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-166">Filter the entity list by entity label to find **LinkedIn exported candidate**.</span></span>

4. <span data-ttu-id="cfe1c-167">选择实体，然后选择 **生成/刷新**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-167">Select the entity, and then select **Generate/refresh**.</span></span>

## <a name="exporting-candidate-records"></a><span data-ttu-id="cfe1c-168">导出应聘者记录</span><span class="sxs-lookup"><span data-stu-id="cfe1c-168">Exporting candidate records</span></span>

<span data-ttu-id="cfe1c-169">完成设置后，招聘人员和人力资源 (HR) 专业人员可以使用 LinkedIn Talent Hub 中的 **导出到 HRIS** 功能，将雇用的应聘者记录从 LinkedIn Talent Hub 导出到 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-169">After the setup is completed, recruiters and human resources (HR) professionals can use the **Export to HRIS** function in LinkedIn Talent Hub to export hired candidate records from LinkedIn Talent Hub to Human Resources.</span></span>

### <a name="export-records-from-linkedin-talent-hub"></a><span data-ttu-id="cfe1c-170">从 LinkedIn Talent Hub 导出记录</span><span class="sxs-lookup"><span data-stu-id="cfe1c-170">Export records from LinkedIn Talent Hub</span></span>

<span data-ttu-id="cfe1c-171">在应聘者完成招聘流程并被录用后，您可以将应聘者记录从 LinkedIn Talent Hub 导出到 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-171">After a candidate has moved through the recruiting process and has been hired, you can export the candidate record from LinkedIn Talent Hub to Human Resources.</span></span>

1. <span data-ttu-id="cfe1c-172">在 LinkedIn Talent Hub 中，打开您为其雇用了新员工的项目。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-172">In LinkedIn Talent Hub, open the project that you hired the new employee for.</span></span>

2. <span data-ttu-id="cfe1c-173">选择应聘者记录。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-173">Select a candidate record.</span></span>

3. <span data-ttu-id="cfe1c-174">选择 **更改阶段**，然后选择 **雇用**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-174">Select **Change stage**, and then select **Hired**.</span></span>

4. <span data-ttu-id="cfe1c-175">在应聘者的省略号菜单 (**...**) 上，选择 **导出到 HRIS**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-175">On the ellipsis menu (**...**) for the candidate, select **Export to HRIS**.</span></span>

5. <span data-ttu-id="cfe1c-176">在 **导出到 HRIS** 窗格中，输入必须导出的信息：</span><span class="sxs-lookup"><span data-stu-id="cfe1c-176">In the **Export to HRIS** pane, enter the information that must be exported:</span></span>

    - <span data-ttu-id="cfe1c-177">在 **HRIS 提供商** 字段中，选择 **Microsoft Dynamics 365 Human Resources**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-177">In the **HRIS provider** field, select **Microsoft Dynamics 365 Human Resources**.</span></span>
    - <span data-ttu-id="cfe1c-178">在 **开始日期** 字段中，为新员工选择一个值。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-178">In the **Start date** field, select a value for the new employee.</span></span>
    - <span data-ttu-id="cfe1c-179">在 **职务** 字段中，输入新员工的工作的职务。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-179">In the **Job title** field, enter a job title for the new employee's job.</span></span>
    - <span data-ttu-id="cfe1c-180">在 **位置** 字段中，输入员工的所在地。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-180">In the **Location** field, enter the location where the employee will be based.</span></span>
    - <span data-ttu-id="cfe1c-181">输入或验证员工的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-181">Enter or verify the employee's email address.</span></span>

![LinkedIn Talent Hub 中的“导出到 HRIS”窗格](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a><span data-ttu-id="cfe1c-183">在 Human Resources 中完成入职</span><span class="sxs-lookup"><span data-stu-id="cfe1c-183">Complete onboarding in Human Resources</span></span>

<span data-ttu-id="cfe1c-184">从 LinkedIn Talent Hub 导出到 Human Resources 的应聘者记录将显示在 **人员管理** 页面的 **可雇用的应聘者** 部分中。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-184">Candidate records that are exported from LinkedIn Talent Hub to Human Resources appear in the **Candidates to hire** section of the **Personnel management** page.</span></span>

1. <span data-ttu-id="cfe1c-185">在 Human Resources 中，打开 **人员管理** 页面。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-185">In Human Resources, open the **Personnel management** page.</span></span>

2. <span data-ttu-id="cfe1c-186">在 **可雇用的应聘者** 部分中，对于选定的应聘者选择 **雇用**。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-186">In the **Candidates to hire** section, select **Hire** for the selected candidate.</span></span>

3. <span data-ttu-id="cfe1c-187">在 **雇用新工作人员** 对话框中，查看记录，然后添加所有必需的信息。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-187">In the **Hire new worker** dialog box, review the record, and add any required information.</span></span> <span data-ttu-id="cfe1c-188">您还可以选择已雇用的应聘者的职位编号。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-188">You can also select the position number that the candidate has been hired for.</span></span>

<span data-ttu-id="cfe1c-189">输入所需的信息后，您可以继续执行创建员工记录和员工入职的标准流程。</span><span class="sxs-lookup"><span data-stu-id="cfe1c-189">After the required information has been entered, you can continue with your standard processes for creating employee records and onboarding employees.</span></span>

<span data-ttu-id="cfe1c-190">以下详细信息将导入并包括在新员工记录上：</span><span class="sxs-lookup"><span data-stu-id="cfe1c-190">The following details are imported and included on the new employee record:</span></span>

- <span data-ttu-id="cfe1c-191">名</span><span class="sxs-lookup"><span data-stu-id="cfe1c-191">First name</span></span>
- <span data-ttu-id="cfe1c-192">姓</span><span class="sxs-lookup"><span data-stu-id="cfe1c-192">Last name</span></span>
- <span data-ttu-id="cfe1c-193">雇用开始日期</span><span class="sxs-lookup"><span data-stu-id="cfe1c-193">Employment start date</span></span>
- <span data-ttu-id="cfe1c-194">电子邮件地址</span><span class="sxs-lookup"><span data-stu-id="cfe1c-194">Email address</span></span>
- <span data-ttu-id="cfe1c-195">电话号码</span><span class="sxs-lookup"><span data-stu-id="cfe1c-195">Phone number</span></span>

## <a name="see-also"></a><span data-ttu-id="cfe1c-196">请参阅</span><span class="sxs-lookup"><span data-stu-id="cfe1c-196">See also</span></span>

[<span data-ttu-id="cfe1c-197">配置 Dataverse 虚拟表</span><span class="sxs-lookup"><span data-stu-id="cfe1c-197">Configure Dataverse virtual tables</span></span>](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="cfe1c-198">什么是 Microsoft Dataverse？</span><span class="sxs-lookup"><span data-stu-id="cfe1c-198">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)
