---
title: 复制实例
description: 您可以使用 Microsoft Dynamics Lifecycle Services (LCS) 将 Microsoft Dynamics 365 Human Resources 数据库复制到沙盒环境。
author: andreabichsel
manager: AnnBe
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 40ca0a4d9733fc2a163daa4ea1c27a3bfae6d3bf
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527829"
---
# <a name="copy-an-instance"></a><span data-ttu-id="daab7-103">复制实例</span><span class="sxs-lookup"><span data-stu-id="daab7-103">Copy an instance</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="daab7-104">您可以使用 Microsoft Dynamics Lifecycle Services (LCS) 将 Microsoft Dynamics 365 Human Resources 数据库复制到沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="daab7-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="daab7-105">如果您有另一个沙盒环境，还可以将数据库从该环境复制到目标沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="daab7-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="daab7-106">要复制实例，请牢记以下提示：</span><span class="sxs-lookup"><span data-stu-id="daab7-106">To copy an instance, keep the following tips in mind:</span></span>

- <span data-ttu-id="daab7-107">您要覆盖的 Human Resources 实例必须是沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="daab7-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="daab7-108">您要从中复制或向其复制的环境必须位于同一区域。</span><span class="sxs-lookup"><span data-stu-id="daab7-108">The environments you're copying from and to must be in the same region.</span></span> <span data-ttu-id="daab7-109">不能跨区域复制。</span><span class="sxs-lookup"><span data-stu-id="daab7-109">You can't copy across regions.</span></span>

- <span data-ttu-id="daab7-110">您必须是目标环境中的管理员，这样您才能在复制实例后登录环境。</span><span class="sxs-lookup"><span data-stu-id="daab7-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="daab7-111">复制 Human Resources 数据库时，不复制 Microsoft Power Apps 环境中包含的元素（应用或数据）。</span><span class="sxs-lookup"><span data-stu-id="daab7-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft Power Apps environment.</span></span> <span data-ttu-id="daab7-112">有关如何在 Power Apps 环境中复制元素的信息，请参阅[复制环境](https://docs.microsoft.com/power-platform/admin/copy-environment)。</span><span class="sxs-lookup"><span data-stu-id="daab7-112">For information about how to copy elements in a Power Apps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="daab7-113">您要覆盖的 Power Apps 环境必须是沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="daab7-113">The Power Apps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="daab7-114">您必须是全局租户管理员才能将 Power Apps 生产环境更改为沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="daab7-114">You must be a global tenant admin to change a Power Apps production environment to a sandbox environment.</span></span> <span data-ttu-id="daab7-115">有关更改 Power Apps 环境的详细信息，请参阅[切换实例](https://docs.microsoft.com/dynamics365/admin/switch-instance)。</span><span class="sxs-lookup"><span data-stu-id="daab7-115">For more information about changing a Power Apps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

- <span data-ttu-id="daab7-116">如果将实例复制到沙盒环境中，并想要将沙盒环境与 Common Data Service 集成，必须将自定义字段重新应用于 Common Data Service 实体。</span><span class="sxs-lookup"><span data-stu-id="daab7-116">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Common Data Service, you must reapply custom fields to Common Data Service entities.</span></span> <span data-ttu-id="daab7-117">请参阅[将自定义字段应用于 Common Data Service](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service)。</span><span class="sxs-lookup"><span data-stu-id="daab7-117">See [Apply custom fields to Common Data Service](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="daab7-118">复制 Human Resources 数据库的影响</span><span class="sxs-lookup"><span data-stu-id="daab7-118">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="daab7-119">复制 Human Resources 数据库时，会发生以下事件：</span><span class="sxs-lookup"><span data-stu-id="daab7-119">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="daab7-120">复制过程将擦除目标环境中的现有数据库。</span><span class="sxs-lookup"><span data-stu-id="daab7-120">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="daab7-121">复制过程完成后，您将无法恢复现有数据库。</span><span class="sxs-lookup"><span data-stu-id="daab7-121">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="daab7-122">在复制过程完成之前，目标环境将不可用。</span><span class="sxs-lookup"><span data-stu-id="daab7-122">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="daab7-123">Microsoft Azure Blob 存储中的文档不会从一个环境复制到另一个环境。</span><span class="sxs-lookup"><span data-stu-id="daab7-123">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="daab7-124">因此，附加的所有文档和模板都不会被复制，并将保留在源环境中。</span><span class="sxs-lookup"><span data-stu-id="daab7-124">As a result, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="daab7-125">除管理员用户和其他内部服务用户帐户之外的所有用户将不可用。</span><span class="sxs-lookup"><span data-stu-id="daab7-125">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="daab7-126">在允许其他用户返回到系统之前，管理员用户可以删除或打乱数据。</span><span class="sxs-lookup"><span data-stu-id="daab7-126">The Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="daab7-127">管理员用户必须进行必要的配置更改，例如将集成终结点重新连接到特定服务或 URL。</span><span class="sxs-lookup"><span data-stu-id="daab7-127">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="daab7-128">复制 Human Resources 数据库</span><span class="sxs-lookup"><span data-stu-id="daab7-128">Copy the Human Resources database</span></span>

<span data-ttu-id="daab7-129">要完成此任务，您首先要复制一个实例，然后登录到 Microsoft Power Platform 管理中心以复制 Power Apps 环境。</span><span class="sxs-lookup"><span data-stu-id="daab7-129">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your Power Apps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="daab7-130">复制实例时，目标实例中的数据库将被擦除。</span><span class="sxs-lookup"><span data-stu-id="daab7-130">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="daab7-131">在此过程中，目标实例不可用。</span><span class="sxs-lookup"><span data-stu-id="daab7-131">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="daab7-132">登录到 LCS，然后选择包含要复制的实例的 LCS 项目。</span><span class="sxs-lookup"><span data-stu-id="daab7-132">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="daab7-133">在您的 LCS 项目中，选择 **Human Resources 应用管理** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="daab7-133">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="daab7-134">选择要复制的实例，然后选择 **复制**。</span><span class="sxs-lookup"><span data-stu-id="daab7-134">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="daab7-135">在 **复制实例** 任务窗格中，选择要覆盖的实例，然后选择 **复制**。</span><span class="sxs-lookup"><span data-stu-id="daab7-135">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="daab7-136">等待 **复制状态** 字段的值更新为 **已完成**。</span><span class="sxs-lookup"><span data-stu-id="daab7-136">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="daab7-137">选择要覆盖的实例</span><span class="sxs-lookup"><span data-stu-id="daab7-137">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="daab7-138">选择 **Power Platform**，然后登录到 Microsoft Power Platform 管理中心。</span><span class="sxs-lookup"><span data-stu-id="daab7-138">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="daab7-139">选择 Power Platform</span><span class="sxs-lookup"><span data-stu-id="daab7-139">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="daab7-140">选择要复制的 Power Apps 环境，然后选择 **复制**。</span><span class="sxs-lookup"><span data-stu-id="daab7-140">Select the Power Apps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="daab7-141">复制过程完成后，登录到目标实例，然后启用 Common Data Service 集成。</span><span class="sxs-lookup"><span data-stu-id="daab7-141">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="daab7-142">有关详细信息和说明，请参阅[配置 Common Data Service 集成](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration)。</span><span class="sxs-lookup"><span data-stu-id="daab7-142">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="daab7-143">数据元素和状态</span><span class="sxs-lookup"><span data-stu-id="daab7-143">Data elements and statuses</span></span>

<span data-ttu-id="daab7-144">复制 Human Resources 实例时，不会复制以下数据元素：</span><span class="sxs-lookup"><span data-stu-id="daab7-144">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="daab7-145">**LogisticsElectronicAddress** 表中的电子邮件地址</span><span class="sxs-lookup"><span data-stu-id="daab7-145">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="daab7-146">**BatchJobHistory**、**BatchHistory** 和 **BatchConstraintHistory** 表中的批处理作业历史记录</span><span class="sxs-lookup"><span data-stu-id="daab7-146">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="daab7-147">**SysEmailSMTPPassword** 表中的简单邮件传输协议 (SMTP) 密码</span><span class="sxs-lookup"><span data-stu-id="daab7-147">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="daab7-148">**SysEmailParameters** 表中的 SMTP 中继服务器</span><span class="sxs-lookup"><span data-stu-id="daab7-148">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="daab7-149">**PrintMgmtSettings** 和 **PrintMgmtDocInstance** 表中的“打印管理”设置</span><span class="sxs-lookup"><span data-stu-id="daab7-149">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="daab7-150">**SysServerConfig**、**SysServerSessions**、**SysCorpNetPrinters**、**SysClientSessions**、**BatchServerConfig** 和 **BatchServerGroup** 表中的特定于环境的记录</span><span class="sxs-lookup"><span data-stu-id="daab7-150">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="daab7-151">DocuValue 表中的文档附件。</span><span class="sxs-lookup"><span data-stu-id="daab7-151">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="daab7-152">这些附件包括在源环境中被覆盖的所有 Microsoft Office 模板</span><span class="sxs-lookup"><span data-stu-id="daab7-152">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="daab7-153">**PersonnelIntegrationConfiguration** 表中的连接字符串</span><span class="sxs-lookup"><span data-stu-id="daab7-153">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="daab7-154">这些元素中的某些元素是特定于环境的，因此不会被复制。</span><span class="sxs-lookup"><span data-stu-id="daab7-154">Some of these elements aren't copied because they're environment-specific.</span></span> <span data-ttu-id="daab7-155">示例包括 **BatchServerConfig** 和 **SysCorpNetPrinters** 记录。</span><span class="sxs-lookup"><span data-stu-id="daab7-155">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="daab7-156">其他元素由于支持票证的数量，不会被复制。</span><span class="sxs-lookup"><span data-stu-id="daab7-156">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="daab7-157">例如:</span><span class="sxs-lookup"><span data-stu-id="daab7-157">For example:</span></span>

- <span data-ttu-id="daab7-158">可能由于在用户接受测试（沙盒）环境中仍启用 SMTP 而发送了重复的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="daab7-158">Duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment.</span></span>

- <span data-ttu-id="daab7-159">可能由于仍启用了批处理作业而发送了无效的集成消息。</span><span class="sxs-lookup"><span data-stu-id="daab7-159">Invalid integration messages might be sent because batch jobs are still enabled.</span></span>

- <span data-ttu-id="daab7-160">可能在管理员可以执行刷新后清理操作之前启用了用户。</span><span class="sxs-lookup"><span data-stu-id="daab7-160">Users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="daab7-161">此外，复制实例时，以下状态也会更改：</span><span class="sxs-lookup"><span data-stu-id="daab7-161">Also, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="daab7-162">除管理员以外的所有用户均设置为 **已禁用**。</span><span class="sxs-lookup"><span data-stu-id="daab7-162">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="daab7-163">除某些系统作业外，所有批处理作业均设置为 **预扣**。</span><span class="sxs-lookup"><span data-stu-id="daab7-163">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="daab7-164">环境管理员</span><span class="sxs-lookup"><span data-stu-id="daab7-164">Environment admin</span></span>

<span data-ttu-id="daab7-165">目标沙盒环境中的所有用户（包括管理员）都将被替换为源环境的用户。</span><span class="sxs-lookup"><span data-stu-id="daab7-165">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="daab7-166">复制实例之前，请确保您是源环境中的管理员。</span><span class="sxs-lookup"><span data-stu-id="daab7-166">Before you copy an instance, be sure that you're an Administrator in the source environment.</span></span> <span data-ttu-id="daab7-167">如果不是，则复制完成后您将无法登录到目标沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="daab7-167">If you aren't, you can't sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="daab7-168">目标沙盒环境中的所有非管理员用户均会被禁用，以防止在沙盒环境中进行不必要的登录。</span><span class="sxs-lookup"><span data-stu-id="daab7-168">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="daab7-169">管理员可以根据需要重新启用用户。</span><span class="sxs-lookup"><span data-stu-id="daab7-169">Administrators can reenable users if needed.</span></span>

## <a name="apply-custom-fields-to-common-data-service"></a><span data-ttu-id="daab7-170">将自定义字段应用于 Common Data Service</span><span class="sxs-lookup"><span data-stu-id="daab7-170">Apply custom fields to Common Data Service</span></span>

<span data-ttu-id="daab7-171">如果将实例复制到沙盒环境中，并想要将沙盒环境与 Common Data Service 集成，必须将自定义字段重新应用于 Common Data Service 实体。</span><span class="sxs-lookup"><span data-stu-id="daab7-171">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Common Data Service, you must reapply custom fields to Common Data Service entities.</span></span>

<span data-ttu-id="daab7-172">对于在 Common Data Service 实体上公开的每个自定义字段，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="daab7-172">For each custom field that's exposed on Common Data Service entities, do the following steps:</span></span>

1. <span data-ttu-id="daab7-173">转到自定义字段，然后选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="daab7-173">Go to the custom field and select **Edit**.</span></span>

2. <span data-ttu-id="daab7-174">为启用了自定义字段的每个 cdm_\* 实体取消选择 **已启用** 字段。</span><span class="sxs-lookup"><span data-stu-id="daab7-174">Unselect the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

3. <span data-ttu-id="daab7-175">选择 **应用更改**。</span><span class="sxs-lookup"><span data-stu-id="daab7-175">Select **Apply Changes**.</span></span>

4. <span data-ttu-id="daab7-176">再次选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="daab7-176">Select **Edit** again.</span></span>

5. <span data-ttu-id="daab7-177">为启用了自定义字段的每个 cdm_\* 实体选择 **已启用** 字段。</span><span class="sxs-lookup"><span data-stu-id="daab7-177">Select the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

6. <span data-ttu-id="daab7-178">再次选择 **应用更改**。</span><span class="sxs-lookup"><span data-stu-id="daab7-178">Select **Apply Changes** again.</span></span>

<span data-ttu-id="daab7-179">取消选择、应用更改、重新选择和应用更改的流程会提示架构在 Common Data Service 中进行更新以包含自定义字段。</span><span class="sxs-lookup"><span data-stu-id="daab7-179">The process of unselecting, applying changes, reselecting, and reapplying changes prompts the schema to update in Common Data Service to include the custom fields.</span></span>

<span data-ttu-id="daab7-180">有关自定义字段的详细信息，请参阅[创建并使用自定义字段](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields)。</span><span class="sxs-lookup"><span data-stu-id="daab7-180">For more information about custom fields, see [Create and work with custom fields](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).</span></span>

## <a name="see-also"></a><span data-ttu-id="daab7-181">请参阅</span><span class="sxs-lookup"><span data-stu-id="daab7-181">See also</span></span>

[<span data-ttu-id="daab7-182">设置 Human Resources</span><span class="sxs-lookup"><span data-stu-id="daab7-182">Provision Human Resources</span></span>](hr-admin-setup-provision.md)</br>
[<span data-ttu-id="daab7-183">删除实例</span><span class="sxs-lookup"><span data-stu-id="daab7-183">Remove an instance</span></span>](hr-admin-setup-remove-instance.md)</br>
[<span data-ttu-id="daab7-184">更新流程</span><span class="sxs-lookup"><span data-stu-id="daab7-184">Update process</span></span>](hr-admin-setup-update-process.md)

