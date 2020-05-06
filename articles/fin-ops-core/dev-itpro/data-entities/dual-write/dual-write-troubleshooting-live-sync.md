---
title: 解决实时同步问题
description: 本主题提供故障排除信息，可以帮助您解决实时同步问题。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: d45b19c1e88e6a27bde4335d4a356f2173bdfcd3
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275409"
---
# <a name="troubleshoot-live-synchronization-issues"></a><span data-ttu-id="7d99f-103">解决实时同步问题</span><span class="sxs-lookup"><span data-stu-id="7d99f-103">Troubleshoot live synchronization issues</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="7d99f-104">本主题提供 Finance and Operations 应用与 Common Data Service 之间的双写入集成的故障排除信息。</span><span class="sxs-lookup"><span data-stu-id="7d99f-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="7d99f-105">具体来说，提供可以帮助您解决实时同步问题的信息。</span><span class="sxs-lookup"><span data-stu-id="7d99f-105">Specifically, it provides information that can help you fix issues with live synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7d99f-106">本主题解决的某些问题可能需要系统管理员角色或 Microsoft Azure Active Directory (Azure AD) 租户管理员凭据。</span><span class="sxs-lookup"><span data-stu-id="7d99f-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="7d99f-107">介绍每个问题的每一节说明了是否需要特定角色或凭据。</span><span class="sxs-lookup"><span data-stu-id="7d99f-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-record-in-a-finance-and-operations-app"></a><span data-ttu-id="7d99f-108">在 Finance and Operations 应用中创建记录时，实时同步会引发“403 已禁止”错误</span><span class="sxs-lookup"><span data-stu-id="7d99f-108">Live synchronization throws a 403 Forbidden error when you create a record in a Finance and Operations app</span></span>

<span data-ttu-id="7d99f-109">当您在 Finance and Operations 应用中创建记录时，您可能会收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="7d99f-109">You might receive the following error message when you create a record in a Finance and Operations app:</span></span>

<span data-ttu-id="7d99f-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"此用户不是组织的成员。\\"}}\]，远程服务器返回错误：(403) 已禁止。"}}".*</span><span class="sxs-lookup"><span data-stu-id="7d99f-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"The user is not a member of the organization.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span></span>

<span data-ttu-id="7d99f-111">要解决此问题，请按照[系统要求和先决条件](requirements-and-prerequisites.md)中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="7d99f-111">To fix the issue, follow the steps in [System requirements and prerequisites](requirements-and-prerequisites.md).</span></span> <span data-ttu-id="7d99f-112">要完成这些步骤，在 Common Data Service 中创建的双写入应用程序用户必须具有系统管理员角色。</span><span class="sxs-lookup"><span data-stu-id="7d99f-112">To complete those steps, the dual-write application users who are created in Common Data Service must have the system admin role.</span></span> <span data-ttu-id="7d99f-113">默认的负责团队也必须具有系统管理员角色。</span><span class="sxs-lookup"><span data-stu-id="7d99f-113">The default owning team must also have the system admin role.</span></span>

## <a name="live-synchronization-for-any-entity-consistently-throws-a-similar-error-when-you-create-a-record-in-a-finance-and-operations-app"></a><span data-ttu-id="7d99f-114">在 Finance and Operations 应用中创建记录时，任何实体的实时同步都会引发类似的错误</span><span class="sxs-lookup"><span data-stu-id="7d99f-114">Live synchronization for any entity consistently throws a similar error when you create a record in a Finance and Operations app</span></span>

<span data-ttu-id="7d99f-115">**解决此问题所需的角色：** 系统管理员</span><span class="sxs-lookup"><span data-stu-id="7d99f-115">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="7d99f-116">每次尝试在 Finance and Operations 应用中保存实体数据时，您可能会收到以下这样的错误消息：</span><span class="sxs-lookup"><span data-stu-id="7d99f-116">You might receive an error message like the following every time that you try to save entity data in a Finance and Operations app:</span></span>

<span data-ttu-id="7d99f-117">*无法将更改保存到数据库。工作单元无法提交事务。无法将数据写入实体 uoms。写入 UnitOfMeasureEntity 失败，并显示错误消息“无法与实体 uoms 同步”。*</span><span class="sxs-lookup"><span data-stu-id="7d99f-117">*Cannot save the changes to the database. Unit of Work can not commit transaction. Unable to write data to entity uoms. Writes to UnitOfMeasureEntity failed with error message Unable to sync with entity uoms.*</span></span>

<span data-ttu-id="7d99f-118">要解决此问题，您必须确保 Finance and Operations 应用和 Common Data Service 中都存在必备的引用数据。</span><span class="sxs-lookup"><span data-stu-id="7d99f-118">To fix the issue, you must make sure that the prerequisite reference data exists in both the Finance and Operations app and Common Data Service.</span></span> <span data-ttu-id="7d99f-119">例如，如果您在 Finance and Operations 应用中的客户属于特定客户组，请确保该客户组存在于 Common Data Service 中。</span><span class="sxs-lookup"><span data-stu-id="7d99f-119">For example, if the customer that you're in the Finance and Operations app belongs to a specific customer group, make sure that the customer group exists in Common Data Service.</span></span>

<span data-ttu-id="7d99f-120">如果两处都存在数据，并且您已确认问题与数据无关，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="7d99f-120">If data exists on both sides, and you've confirmed that the issue isn't data-related, follow these steps.</span></span>

1. <span data-ttu-id="7d99f-121">停止相关实体。</span><span class="sxs-lookup"><span data-stu-id="7d99f-121">Stop the related entity.</span></span>
2. <span data-ttu-id="7d99f-122">登录到 Finance and Operations 应用，并确保失败实体的记录存在于 DualWriteProjectConfiguration 和 DualWriteProjectFieldConfiguration 表中。</span><span class="sxs-lookup"><span data-stu-id="7d99f-122">Sign in to the Finance and Operations app, and make sure that records for the failing entity exist in the DualWriteProjectConfiguration and DualWriteProjectFieldConfiguration tables.</span></span> <span data-ttu-id="7d99f-123">例如，以下是**客户**实体失败时查询将呈现的类似状态。</span><span class="sxs-lookup"><span data-stu-id="7d99f-123">For example, here is what the query looks like if the **Customers** entity is failing.</span></span>

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. <span data-ttu-id="7d99f-124">即使停止实体映射后，如果仍有失败实体的记录，请删除与失败实体相关的记录。</span><span class="sxs-lookup"><span data-stu-id="7d99f-124">If there are records for the failing entity even after you stop the entity mapping, delete the records that are related to the failing entity.</span></span> <span data-ttu-id="7d99f-125">记下 DualWriteProjectConfiguration 表中的 **projectname** 列，并通过使用项目名称删除记录来获取 DualWriteProjectFieldConfiguration 表中的记录。</span><span class="sxs-lookup"><span data-stu-id="7d99f-125">Make a note of the **projectname** column in the DualWriteProjectConfiguration table, and fetch the record in the DualWriteProjectFieldConfiguration table by using the project name to delete the record.</span></span>
4. <span data-ttu-id="7d99f-126">开始实体映射。</span><span class="sxs-lookup"><span data-stu-id="7d99f-126">Start the entity mapping.</span></span> <span data-ttu-id="7d99f-127">验证数据是否同步，没有任何问题。</span><span class="sxs-lookup"><span data-stu-id="7d99f-127">Validate whether the data is synced without any issues.</span></span>

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a><span data-ttu-id="7d99f-128">在 Finance and Operations 应用中创建数据时处理读或写权限错误</span><span class="sxs-lookup"><span data-stu-id="7d99f-128">Handle read or write privilege errors when you create data in a Finance and Operations app</span></span>

<span data-ttu-id="7d99f-129">在 Finance and Operations 应用中创建数据时，您可能会收到类似于以下示例的“错误请求”错误消息。</span><span class="sxs-lookup"><span data-stu-id="7d99f-129">You might receive a "Bad Request" error message that resembles the following example when you create data in a Finance and Operations app.</span></span>

![“错误请求”错误消息的示例](media/error_record_id_source.png)

<span data-ttu-id="7d99f-131">若要解决此问题，您必须为映射的 Dynamics 365 Sales 或 Dynamics 365 Customer Service 业务单位的团队分配正确的安全角色，以启用缺少的权限。</span><span class="sxs-lookup"><span data-stu-id="7d99f-131">To fix the issue, you must assign the correct security role to the team of the mapped Dynamics 365 Sales or Dynamics 365 Customer Service business unit to enable the missing privilege.</span></span>

1. <span data-ttu-id="7d99f-132">在 Finance and Operations 应用中，找到在数据集成连接集中映射的业务单位。</span><span class="sxs-lookup"><span data-stu-id="7d99f-132">In the Finance and Operations app, find the business unit that is mapped in the Data Integration connection set.</span></span>

    ![组织映射](media/mapped_business_unit.png)

2. <span data-ttu-id="7d99f-134">登录到 Dynamics 365 中的模型驱动应用内的环境，导航至**设置 \> 安全**，找到映射业务单位的团队。</span><span class="sxs-lookup"><span data-stu-id="7d99f-134">Sign in to the environment in the model-driven app in Dynamics 365, navigate to **Setting \> Security**, and find the team of the mapped business unit.</span></span>

    ![映射业务单位的团队](media/setting_security_page.png)

3. <span data-ttu-id="7d99f-136">打开要编辑的团队页面，然后选择**管理角色**打开**管理团队角色**对话框。</span><span class="sxs-lookup"><span data-stu-id="7d99f-136">Open the page for the team for editing, and then select **Manage roles** to open the **Manage Team Roles** dialog box.</span></span>

    ![管理角色按钮](media/manage_team_roles.png)

4. <span data-ttu-id="7d99f-138">为相关实体分配具有读/写权限的角色，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="7d99f-138">Assign the role that has the read/write privilege for the relevant entities, and then select **OK**.</span></span>

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-common-data-service-environment"></a><span data-ttu-id="7d99f-139">在最近更改了 Common Data Service 环境的环境中解决同步问题</span><span class="sxs-lookup"><span data-stu-id="7d99f-139">Fix synchronization issues in an environment that has a recently changed Common Data Service environment</span></span>

<span data-ttu-id="7d99f-140">**解决此问题所需的角色：** 系统管理员</span><span class="sxs-lookup"><span data-stu-id="7d99f-140">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="7d99f-141">当您在 Finance and Operations 应用中创建数据时，您可能会收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="7d99f-141">You might receive the following error message when you create data in a Finance and Operations app:</span></span>

<span data-ttu-id="7d99f-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**无法为实体 CustCustomerV3Entity 生成有效负载**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"有效负载创建失败，显示错误“URI 无效：此 URI 是空的”。"}\],"isErrorCountUpdated":true}*</span><span class="sxs-lookup"><span data-stu-id="7d99f-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Unable to generate payload for entity CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Payload creation failed with error Invalid URI: The URI is empty."}\],"isErrorCountUpdated":true}*</span></span>

<span data-ttu-id="7d99f-143">这是在 Dynamics 365 中的模型驱动应用中出现的错误情况：</span><span class="sxs-lookup"><span data-stu-id="7d99f-143">Here is what the error looks like in the model-driven app in Dynamics 365:</span></span>

<span data-ttu-id="7d99f-144">*ISV 代码发生意外错误。(ErrorType = ClientError) 插件发生意外异常 (Execute)：Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception：无法处理实体帐户 -（连接尝试失败，因为连接方未在一段时间后正确响应，或由于连接的主机未能响应导致建立的连接失败*</span><span class="sxs-lookup"><span data-stu-id="7d99f-144">*An unexpected error occurred from ISV code. (ErrorType = ClientError) Unexpected exception from plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: failed to process entity account - (A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond*</span></span>

<span data-ttu-id="7d99f-145">当您尝试在 Finance and Operations 应用中创建数据但未正确重置 Common Data Service 环境时，将发生此错误。</span><span class="sxs-lookup"><span data-stu-id="7d99f-145">This error occurs when the Common Data Service environment is incorrectly reset at the same time that you try to create data in the Finance and Operations app.</span></span>

<span data-ttu-id="7d99f-146">若要解决此问题，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="7d99f-146">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="7d99f-147">登录到 Finance and Operations 虚拟机 (VM)，打开 SQL Server Management Studio (SSMS)，在 DUALWRITEPROJECTCONFIGURATIONENTITY 表中查找记录，其中 **internalentityname** 等于 **客户 V3**，**externalentityname** 等于**客户**。</span><span class="sxs-lookup"><span data-stu-id="7d99f-147">Sign in to the Finance and Operations virtual machine (VM), open SQL Server Management Studio (SSMS), and look for records in the DUALWRITEPROJECTCONFIGURATIONENTITY table where **internalentityname** equals **Customers V3** and **externalentityname** equals **accounts**.</span></span> <span data-ttu-id="7d99f-148">这是查询呈现的状态。</span><span class="sxs-lookup"><span data-stu-id="7d99f-148">Here is what the query looks like.</span></span>

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. <span data-ttu-id="7d99f-149">使用上一个查询的结果中的项目名称来运行以下查询。</span><span class="sxs-lookup"><span data-stu-id="7d99f-149">Use the project name from the results of the previous query to run the following query.</span></span>

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. <span data-ttu-id="7d99f-150">确保 **externalenvironmentURL** 列具有正确的 Common Data Service 或应用 URL。</span><span class="sxs-lookup"><span data-stu-id="7d99f-150">Make sure that the **externalenvironmentURL** column has the correct Common Data Service or app URL.</span></span> <span data-ttu-id="7d99f-151">删除任何指向错误的 Common Data Service URL 的重复记录。</span><span class="sxs-lookup"><span data-stu-id="7d99f-151">Delete any duplicate records that point to the wrong Common Data Service URL.</span></span> <span data-ttu-id="7d99f-152">删除 DUALWRITEPROJECTFIELDCONFIGURATION 和 DUALWRITEPROJECTCONFIGURATION 表中的相应记录。</span><span class="sxs-lookup"><span data-stu-id="7d99f-152">Delete the corresponding records in the DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION tables.</span></span>
4. <span data-ttu-id="7d99f-153">停止实体映射，然后重新开始映射</span><span class="sxs-lookup"><span data-stu-id="7d99f-153">Stop the entity mapping, and then restart it</span></span>
