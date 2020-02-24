---
title: 复制实例
description: ''
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
ms.openlocfilehash: 0bbe325edb65cad0c1912e0a6ade559e5675dc58
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008176"
---
# <a name="copy-an-instance"></a><span data-ttu-id="85787-102">复制实例</span><span class="sxs-lookup"><span data-stu-id="85787-102">Copy an instance</span></span>

<span data-ttu-id="85787-103">您可以使用 Microsoft Dynamics Lifecycle Services (LCS) 将 Microsoft Dynamics 365 Human Resources 数据库复制到沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="85787-103">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="85787-104">如果您有另一个沙盒环境，还可以将数据库从该环境复制到目标沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="85787-104">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="85787-105">要复制实例，您需要确保：</span><span class="sxs-lookup"><span data-stu-id="85787-105">To copy an instance, you need to ensure the following:</span></span>

- <span data-ttu-id="85787-106">您要覆盖的 Human Resources 实例必须是沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="85787-106">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="85787-107">您要从中复制或向其复制的环境必须位于同一区域。</span><span class="sxs-lookup"><span data-stu-id="85787-107">The environments you are copying from and to must be in the same region.</span></span> <span data-ttu-id="85787-108">不能跨区域复制。</span><span class="sxs-lookup"><span data-stu-id="85787-108">You can't copy across regions.</span></span>

- <span data-ttu-id="85787-109">您必须是目标环境中的管理员，这样您才能在复制实例后登录环境。</span><span class="sxs-lookup"><span data-stu-id="85787-109">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="85787-110">复制 Human Resources 数据库时，不复制 Microsoft PowerApps 环境中包含的元素（应用或数据）。</span><span class="sxs-lookup"><span data-stu-id="85787-110">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft PowerApps environment.</span></span> <span data-ttu-id="85787-111">有关如何在 PowerApps 环境中复制元素的信息，请参阅[复制环境](https://docs.microsoft.com/power-platform/admin/copy-environment)。</span><span class="sxs-lookup"><span data-stu-id="85787-111">For information about how to copy elements in a PowerApps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="85787-112">您要覆盖的 PowerApps 环境必须是沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="85787-112">The PowerApps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="85787-113">您必须是全局租户管理员才能将 PowerApps 生产环境更改为沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="85787-113">You must be a global tenant admin to change a PowerApps production environment to a sandbox environment.</span></span> <span data-ttu-id="85787-114">有关更改 PowerApps 环境的详细信息，请参阅[切换实例](https://docs.microsoft.com/dynamics365/admin/switch-instance)。</span><span class="sxs-lookup"><span data-stu-id="85787-114">For more information about changing a PowerApps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="85787-115">复制 Human Resources 数据库的影响</span><span class="sxs-lookup"><span data-stu-id="85787-115">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="85787-116">复制 Human Resources 数据库时，会发生以下事件：</span><span class="sxs-lookup"><span data-stu-id="85787-116">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="85787-117">复制过程将擦除目标环境中的现有数据库。</span><span class="sxs-lookup"><span data-stu-id="85787-117">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="85787-118">复制过程完成后，您将无法恢复现有数据库。</span><span class="sxs-lookup"><span data-stu-id="85787-118">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="85787-119">在复制过程完成之前，目标环境将不可用。</span><span class="sxs-lookup"><span data-stu-id="85787-119">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="85787-120">Microsoft Azure Blob 存储中的文档不会从一个环境复制到另一个环境。</span><span class="sxs-lookup"><span data-stu-id="85787-120">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="85787-121">因此，附加的所有文档和模板都不会被复制，并将保留在源环境中。</span><span class="sxs-lookup"><span data-stu-id="85787-121">Therefore, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="85787-122">除管理员用户和其他内部服务用户帐户之外的所有用户将不可用。</span><span class="sxs-lookup"><span data-stu-id="85787-122">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="85787-123">因此，在允许其他用户返回到系统之前，管理员用户可以删除或打乱数据。</span><span class="sxs-lookup"><span data-stu-id="85787-123">Therefore, the Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="85787-124">管理员用户必须进行必要的配置更改，例如将集成终结点重新连接到特定服务或 URL。</span><span class="sxs-lookup"><span data-stu-id="85787-124">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="85787-125">复制 Human Resources 数据库</span><span class="sxs-lookup"><span data-stu-id="85787-125">Copy the Human Resources database</span></span>

<span data-ttu-id="85787-126">要完成此任务，您首先要复制一个实例，然后登录到 Microsoft Power Platform 管理中心以复制 PowerApps 环境。</span><span class="sxs-lookup"><span data-stu-id="85787-126">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your PowerApps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="85787-127">复制实例时，目标实例中的数据库将被擦除。</span><span class="sxs-lookup"><span data-stu-id="85787-127">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="85787-128">在此过程中，目标实例不可用。</span><span class="sxs-lookup"><span data-stu-id="85787-128">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="85787-129">登录到 LCS，然后选择包含要复制的实例的 LCS 项目。</span><span class="sxs-lookup"><span data-stu-id="85787-129">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="85787-130">在您的 LCS 项目中，选择 **Human Resources 应用管理**磁贴。</span><span class="sxs-lookup"><span data-stu-id="85787-130">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="85787-131">选择要复制的实例，然后选择**复制**。</span><span class="sxs-lookup"><span data-stu-id="85787-131">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="85787-132">在**复制实例**任务窗格中，选择要覆盖的实例，然后选择**复制**。</span><span class="sxs-lookup"><span data-stu-id="85787-132">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="85787-133">等待**复制状态**字段的值更新为**已完成**。</span><span class="sxs-lookup"><span data-stu-id="85787-133">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="85787-134">选择要覆盖的实例</span><span class="sxs-lookup"><span data-stu-id="85787-134">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="85787-135">选择 **Power Platform**，然后登录到 Microsoft Power Platform 管理中心。</span><span class="sxs-lookup"><span data-stu-id="85787-135">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="85787-136">选择 Power Platform</span><span class="sxs-lookup"><span data-stu-id="85787-136">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="85787-137">选择要复制的 PowerApps 环境，然后选择**复制**。</span><span class="sxs-lookup"><span data-stu-id="85787-137">Select the PowerApps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="85787-138">复制过程完成后，登录到目标实例，然后启用 Common Data Service 集成。</span><span class="sxs-lookup"><span data-stu-id="85787-138">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="85787-139">有关详细信息和说明，请参阅[配置 Common Data Service 集成](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration)。</span><span class="sxs-lookup"><span data-stu-id="85787-139">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="85787-140">数据元素和状态</span><span class="sxs-lookup"><span data-stu-id="85787-140">Data elements and statuses</span></span>

<span data-ttu-id="85787-141">复制 Human Resources 实例时，不会复制以下数据元素：</span><span class="sxs-lookup"><span data-stu-id="85787-141">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="85787-142">**LogisticsElectronicAddress** 表中的电子邮件地址</span><span class="sxs-lookup"><span data-stu-id="85787-142">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="85787-143">**BatchJobHistory**、**BatchHistory** 和 **BatchConstraintHistory** 表中的批处理作业历史记录</span><span class="sxs-lookup"><span data-stu-id="85787-143">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="85787-144">**SysEmailSMTPPassword** 表中的简单邮件传输协议 (SMTP) 密码</span><span class="sxs-lookup"><span data-stu-id="85787-144">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="85787-145">**SysEmailParameters** 表中的 SMTP 中继服务器</span><span class="sxs-lookup"><span data-stu-id="85787-145">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="85787-146">**PrintMgmtSettings** 和 **PrintMgmtDocInstance** 表中的“打印管理”设置</span><span class="sxs-lookup"><span data-stu-id="85787-146">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="85787-147">**SysServerConfig**、**SysServerSessions**、**SysCorpNetPrinters**、**SysClientSessions**、**BatchServerConfig** 和 **BatchServerGroup** 表中的特定于环境的记录</span><span class="sxs-lookup"><span data-stu-id="85787-147">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="85787-148">DocuValue 表中的文档附件。</span><span class="sxs-lookup"><span data-stu-id="85787-148">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="85787-149">这些附件包括在源环境中被覆盖的所有 Microsoft Office 模板</span><span class="sxs-lookup"><span data-stu-id="85787-149">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="85787-150">**PersonnelIntegrationConfiguration** 表中的连接字符串</span><span class="sxs-lookup"><span data-stu-id="85787-150">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="85787-151">这些元素中的某些元素是特定于环境的，因此不会被复制。</span><span class="sxs-lookup"><span data-stu-id="85787-151">Some of these elements aren't copied because they are environment-specific.</span></span> <span data-ttu-id="85787-152">示例包括 **BatchServerConfig** 和 **SysCorpNetPrinters** 记录。</span><span class="sxs-lookup"><span data-stu-id="85787-152">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="85787-153">其他元素由于支持票证的数量，不会被复制。</span><span class="sxs-lookup"><span data-stu-id="85787-153">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="85787-154">例如，可能由于在用户接受测试（沙盒）环境中仍启用 SMTP 而发送了重复的电子邮件，可能由于仍启用了批处理作业而发送了无效的集成消息，或者可能在管理员可以执行刷新后清理操作之前启用了用户。</span><span class="sxs-lookup"><span data-stu-id="85787-154">For example, duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment, invalid integration messages might be sent because batch jobs are still enabled, and users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="85787-155">此外，复制实例时，以下状态也会更改：</span><span class="sxs-lookup"><span data-stu-id="85787-155">In addition, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="85787-156">除管理员以外的所有用户均设置为**已禁用**。</span><span class="sxs-lookup"><span data-stu-id="85787-156">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="85787-157">除某些系统作业外，所有批处理作业均设置为**预扣**。</span><span class="sxs-lookup"><span data-stu-id="85787-157">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="85787-158">环境管理员</span><span class="sxs-lookup"><span data-stu-id="85787-158">Environment admin</span></span>

<span data-ttu-id="85787-159">目标沙盒环境中的所有用户（包括管理员）都将被替换为源环境的用户。</span><span class="sxs-lookup"><span data-stu-id="85787-159">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="85787-160">复制实例之前，请确保您是目标环境中的管理员。</span><span class="sxs-lookup"><span data-stu-id="85787-160">Before you copy an instance, be sure that you're an Administrator in the target environment.</span></span> <span data-ttu-id="85787-161">如果不是，则复制完成后您将无法登录到目标沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="85787-161">If you aren't, you won't be able to sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="85787-162">目标沙盒环境中的所有非管理员用户均会被禁用，以防止在沙盒环境中进行不必要的登录。</span><span class="sxs-lookup"><span data-stu-id="85787-162">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="85787-163">管理员可以根据需要重新启用用户。</span><span class="sxs-lookup"><span data-stu-id="85787-163">Administrators can reenable users if needed.</span></span>
