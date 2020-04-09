---
title: 解决与 Finance and Operations 应用升级相关的问题
description: 本主题提供故障排除信息，可以帮助您解决与 Finance and Operations 应用升级有关的问题。
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
ms.openlocfilehash: 59384d8e8d043eb14231a471c7218ced2dddf739
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172869"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="80354-103">解决与 Finance and Operations 应用升级相关的问题</span><span class="sxs-lookup"><span data-stu-id="80354-103">Troubleshoot issues related to upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="80354-104">本主题提供 Finance and Operations 应用与 Common Data Service 之间的双写入集成的故障排除信息。</span><span class="sxs-lookup"><span data-stu-id="80354-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="80354-105">具体来说，提供可以帮助您解决与 Finance and Operations 应用升级有关的问题的信息。</span><span class="sxs-lookup"><span data-stu-id="80354-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="80354-106">本主题解决的某些问题可能需要系统管理员角色或 Microsoft Azure Active Directory (Azure AD) 租户管理员凭据。</span><span class="sxs-lookup"><span data-stu-id="80354-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="80354-107">介绍每个问题的每一节说明了是否需要特定角色或凭据。</span><span class="sxs-lookup"><span data-stu-id="80354-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="80354-108">数据库同步错误</span><span class="sxs-lookup"><span data-stu-id="80354-108">Database synchronization errors</span></span>

<span data-ttu-id="80354-109">**解决此问题所需的角色：** 系统管理员</span><span class="sxs-lookup"><span data-stu-id="80354-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="80354-110">当您尝试使用 **DualWriteProjectConfiguration** 实体将 Finance and Operations 应用更新为平台更新 30 时，您可能会收到类似于以下示例的错误消息。</span><span class="sxs-lookup"><span data-stu-id="80354-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** entity to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="80354-111">若要解决此问题，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="80354-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="80354-112">登录到 Finance and Operations 应用的虚拟机 (VM)。</span><span class="sxs-lookup"><span data-stu-id="80354-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="80354-113">以管理员身份打开 Visual Studio，然后打开应用程序对象树 (AOT)。</span><span class="sxs-lookup"><span data-stu-id="80354-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="80354-114">搜索 **DualWriteProjectConfiguration**。</span><span class="sxs-lookup"><span data-stu-id="80354-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="80354-115">在 AOT 中，右键单击 **DualWriteProjectConfiguration**，然后选择**添加到新项目**。</span><span class="sxs-lookup"><span data-stu-id="80354-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="80354-116">选择**确定**创建使用默认选项的新项目。</span><span class="sxs-lookup"><span data-stu-id="80354-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="80354-117">在解决方案资源管理器中，右键单击**项目属性**，将**在构建时同步数据库**设置为 **True**。</span><span class="sxs-lookup"><span data-stu-id="80354-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="80354-118">构建项目，并确认构建成功。</span><span class="sxs-lookup"><span data-stu-id="80354-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="80354-119">在 **Dynamics 365** 菜单上，选择**同步数据库**。</span><span class="sxs-lookup"><span data-stu-id="80354-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="80354-120">选择**同步**进行完全数据库同步。</span><span class="sxs-lookup"><span data-stu-id="80354-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="80354-121">完全数据库同步成功后，请在 Microsoft Dynamics Lifecycle Services (LCS) 中重新运行数据库同步步骤，并在适用时使用手动升级脚本，以便可以继续进行更新。</span><span class="sxs-lookup"><span data-stu-id="80354-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-entity-fields-issue-on-maps"></a><span data-ttu-id="80354-122">映射中的缺少实体字段问题</span><span class="sxs-lookup"><span data-stu-id="80354-122">Missing entity fields issue on maps</span></span>

<span data-ttu-id="80354-123">**解决此问题所需的角色：** 系统管理员</span><span class="sxs-lookup"><span data-stu-id="80354-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="80354-124">在**双写入**页面上，您可能会收到类似于以下示例的错误消息：</span><span class="sxs-lookup"><span data-stu-id="80354-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="80354-125">*架构中缺少源字段\<字段名称\>。*</span><span class="sxs-lookup"><span data-stu-id="80354-125">*Missing source field \<field name\> in the schema.*</span></span>

![缺少源字段错误消息的示例](media/error_missing_field.png)

<span data-ttu-id="80354-127">要解决此问题，请首先执行以下步骤，以确保字段在实体中。</span><span class="sxs-lookup"><span data-stu-id="80354-127">To fix the issue, first follow these steps to make sure that the fields are in the entity.</span></span>

1. <span data-ttu-id="80354-128">登录到 Finance and Operations 应用的 VM。</span><span class="sxs-lookup"><span data-stu-id="80354-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="80354-129">转到**工作区 \> 数据管理**，选择**框架参数**磁贴，然后在**实体设置**选项卡上，选择**刷新实体列表**刷新实体。</span><span class="sxs-lookup"><span data-stu-id="80354-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Entity settings** tab, select **Refresh entity list** to refresh the entities.</span></span>
3. <span data-ttu-id="80354-130">转到**工作区 \> 数据管理**，选择**数据实体**选项卡，确保实体已列出。</span><span class="sxs-lookup"><span data-stu-id="80354-130">Go to **Workspaces \> Data management**, select the **Data entities** tab, and make sure that the entity is listed.</span></span> <span data-ttu-id="80354-131">如果实体未列出，登录到 Finance and Operations 应用的 VM，确保实体可用。</span><span class="sxs-lookup"><span data-stu-id="80354-131">If the entity isn't listed, sign in to the VM for the Finance and Operations app, and make sure the entity is available.</span></span>
4. <span data-ttu-id="80354-132">从 Finance and Operations 应用中的**双写入**页面打开**实体映射**页面。</span><span class="sxs-lookup"><span data-stu-id="80354-132">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="80354-133">选择**刷新实体列表**自动填充实体映射中的字段。</span><span class="sxs-lookup"><span data-stu-id="80354-133">Select **Refresh entity list** to automatically fill the fields in the entity mappings.</span></span>

<span data-ttu-id="80354-134">如果问题仍然没有解决，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="80354-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="80354-135">这些步骤将指导您完成删除实体然后再次添加实体的过程。</span><span class="sxs-lookup"><span data-stu-id="80354-135">These steps guide you through the process of deleting an entity and then adding it again.</span></span> <span data-ttu-id="80354-136">为避免出现问题，请确保严格按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="80354-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="80354-137">在 Finance and Operations 应用中，转到**工作区 \> 数据管理**，然后选择**数据实体**磁贴。</span><span class="sxs-lookup"><span data-stu-id="80354-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data entities** tile.</span></span>
2. <span data-ttu-id="80354-138">查找缺少该字段的实体。</span><span class="sxs-lookup"><span data-stu-id="80354-138">Find the entity that is missing the field.</span></span> <span data-ttu-id="80354-139">记下目标实体、暂存表、实体名称和其他列值。</span><span class="sxs-lookup"><span data-stu-id="80354-139">Make a note of the target entity, staging table, entity name, and other column values.</span></span>
3. <span data-ttu-id="80354-140">如果您的任何处理组都依赖此实体，请在删除实体之前对处理组采取适当的措施。</span><span class="sxs-lookup"><span data-stu-id="80354-140">If any of your processing groups depend on this entity, take appropriate action for the processing groups before you delete the entity.</span></span>
4. <span data-ttu-id="80354-141">删除缺少该字段的实体。</span><span class="sxs-lookup"><span data-stu-id="80354-141">Delete the entity that is missing the field.</span></span>
5. <span data-ttu-id="80354-142">选择**新建**，然后重新添加实体。</span><span class="sxs-lookup"><span data-stu-id="80354-142">Select **New**, and add the entity back.</span></span> <span data-ttu-id="80354-143">指定在步骤 2 中记下的值。</span><span class="sxs-lookup"><span data-stu-id="80354-143">Specify the values that you made a note of in step 2.</span></span>
6. <span data-ttu-id="80354-144">从 Finance and Operations 应用中的**双写入**页面打开**实体映射**页面。</span><span class="sxs-lookup"><span data-stu-id="80354-144">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
7. <span data-ttu-id="80354-145">选择**刷新实体列表**自动填充实体映射中的字段。</span><span class="sxs-lookup"><span data-stu-id="80354-145">Select **Refresh entity list** to automatically fill the fields in the entity mappings.</span></span>
