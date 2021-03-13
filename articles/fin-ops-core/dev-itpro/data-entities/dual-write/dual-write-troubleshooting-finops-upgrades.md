---
title: 解决 Finance and Operations 应用升级存在的问题
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: a11ce426d7f30b6b124bd2022514a0201c2b332c
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "5131213"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="1b362-103">解决 Finance and Operations 应用升级存在的问题</span><span class="sxs-lookup"><span data-stu-id="1b362-103">Troubleshoot issues from upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="1b362-104">本主题提供 Finance and Operations 应用与 Dataverse 之间的双写入集成的故障排除信息。</span><span class="sxs-lookup"><span data-stu-id="1b362-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="1b362-105">具体来说，提供可以帮助您解决与 Finance and Operations 应用升级有关的问题的信息。</span><span class="sxs-lookup"><span data-stu-id="1b362-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1b362-106">本主题解决的某些问题可能需要系统管理员角色或 Microsoft Azure Active Directory (Azure AD) 租户管理员凭据。</span><span class="sxs-lookup"><span data-stu-id="1b362-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="1b362-107">介绍每个问题的每一节说明了是否需要特定角色或凭据。</span><span class="sxs-lookup"><span data-stu-id="1b362-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="1b362-108">数据库同步错误</span><span class="sxs-lookup"><span data-stu-id="1b362-108">Database synchronization errors</span></span>

<span data-ttu-id="1b362-109">**解决此问题所需的角色：** 系统管理员</span><span class="sxs-lookup"><span data-stu-id="1b362-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="1b362-110">当您尝试使用 **DualWriteProjectConfiguration** 表将 Finance and Operations 应用更新为平台更新 30 时，您可能会收到类似于以下示例的错误消息。</span><span class="sxs-lookup"><span data-stu-id="1b362-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** table to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="1b362-111">若要解决此问题，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="1b362-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="1b362-112">登录到 Finance and Operations 应用的虚拟机 (VM)。</span><span class="sxs-lookup"><span data-stu-id="1b362-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="1b362-113">以管理员身份打开 Visual Studio，然后打开应用程序对象树 (AOT)。</span><span class="sxs-lookup"><span data-stu-id="1b362-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="1b362-114">搜索 **DualWriteProjectConfiguration**。</span><span class="sxs-lookup"><span data-stu-id="1b362-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="1b362-115">在 AOT 中，右键单击 **DualWriteProjectConfiguration**，然后选择 **添加到新项目**。</span><span class="sxs-lookup"><span data-stu-id="1b362-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="1b362-116">选择 **确定** 创建使用默认选项的新项目。</span><span class="sxs-lookup"><span data-stu-id="1b362-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="1b362-117">在解决方案资源管理器中，右键单击 **项目属性**，将 **在构建时同步数据库** 设置为 **True**。</span><span class="sxs-lookup"><span data-stu-id="1b362-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="1b362-118">构建项目，并确认构建成功。</span><span class="sxs-lookup"><span data-stu-id="1b362-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="1b362-119">在 **Dynamics 365** 菜单上，选择 **同步数据库**。</span><span class="sxs-lookup"><span data-stu-id="1b362-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="1b362-120">选择 **同步** 进行完全数据库同步。</span><span class="sxs-lookup"><span data-stu-id="1b362-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="1b362-121">完全数据库同步成功后，请在 Microsoft Dynamics Lifecycle Services (LCS) 中重新运行数据库同步步骤，并在适用时使用手动升级脚本，以便可以继续进行更新。</span><span class="sxs-lookup"><span data-stu-id="1b362-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-table-columns-issue-on-maps"></a><span data-ttu-id="1b362-122">映射中缺少表列问题</span><span class="sxs-lookup"><span data-stu-id="1b362-122">Missing table columns issue on maps</span></span>

<span data-ttu-id="1b362-123">**解决此问题所需的角色：** 系统管理员</span><span class="sxs-lookup"><span data-stu-id="1b362-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="1b362-124">在 **双写入** 页面上，您可能会收到类似于以下示例的错误消息：</span><span class="sxs-lookup"><span data-stu-id="1b362-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="1b362-125">*架构中缺少源字段 \<field name\>。*</span><span class="sxs-lookup"><span data-stu-id="1b362-125">*Missing source field \<field name\> in the schema.*</span></span>

![缺少源列错误消息的示例](media/error_missing_field.png)

<span data-ttu-id="1b362-127">要解决此问题，请首先执行以下步骤，以确保列在表中。</span><span class="sxs-lookup"><span data-stu-id="1b362-127">To fix the issue, first follow these steps to make sure that the columns are in the table.</span></span>

1. <span data-ttu-id="1b362-128">登录到 Finance and Operations 应用的 VM。</span><span class="sxs-lookup"><span data-stu-id="1b362-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="1b362-129">转到 **工作区 \> 数据管理**，选择 **框架参数** 磁贴，然后在 **表设置** 选项卡上，选择 **刷新表列表** 刷新表。</span><span class="sxs-lookup"><span data-stu-id="1b362-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Table settings** tab, select **Refresh table list** to refresh the tables.</span></span>
3. <span data-ttu-id="1b362-130">转到 **工作区 \> 数据管理**，选择 **数据表** 选项卡，确保表已列出。</span><span class="sxs-lookup"><span data-stu-id="1b362-130">Go to **Workspaces \> Data management**, select the **Data tables** tab, and make sure that the table is listed.</span></span> <span data-ttu-id="1b362-131">如果表未列出，登录到 Finance and Operations 应用的 VM，确保表可用。</span><span class="sxs-lookup"><span data-stu-id="1b362-131">If the table isn't listed, sign in to the VM for the Finance and Operations app, and make sure the table is available.</span></span>
4. <span data-ttu-id="1b362-132">从 Finance and Operations 应用中的 **双写入** 页面打开 **表映射** 页面。</span><span class="sxs-lookup"><span data-stu-id="1b362-132">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="1b362-133">选择 **刷新表列表** 自动填充表映射中的列。</span><span class="sxs-lookup"><span data-stu-id="1b362-133">Select **Refresh table list** to automatically fill the columns in the table mappings.</span></span>

<span data-ttu-id="1b362-134">如果问题仍然没有解决，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="1b362-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1b362-135">这些步骤将指导您完成删除表然后再次添加表的过程。</span><span class="sxs-lookup"><span data-stu-id="1b362-135">These steps guide you through the process of deleting a table and then adding it again.</span></span> <span data-ttu-id="1b362-136">为避免出现问题，请确保严格按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="1b362-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="1b362-137">在 Finance and Operations 应用中，转到 **工作区 \> 数据管理**，然后选择 **数据表** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="1b362-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data tables** tile.</span></span>
2. <span data-ttu-id="1b362-138">查找缺少该属性的表。</span><span class="sxs-lookup"><span data-stu-id="1b362-138">Find the table that is missing the attribute.</span></span> <span data-ttu-id="1b362-139">单击工具栏中的 **修改目标映射**。</span><span class="sxs-lookup"><span data-stu-id="1b362-139">Click **Modify target mapping** in the toolbar.</span></span>
3. <span data-ttu-id="1b362-140">在 **将暂存映射到目标** 窗格中，单击 **生成映射**。</span><span class="sxs-lookup"><span data-stu-id="1b362-140">On the **Map staging to target** pane, click **Generate mapping**.</span></span>
4. <span data-ttu-id="1b362-141">从 Finance and Operations 应用中的 **双写入** 页面打开 **表映射** 页面。</span><span class="sxs-lookup"><span data-stu-id="1b362-141">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="1b362-142">如果该属性未在映射中自动填充，请单击 **添加属性** 按钮，然后单击 **保存** 手动添加该属性。</span><span class="sxs-lookup"><span data-stu-id="1b362-142">If the attribute is not auto-populated on the map, add it manually by clicking **Add attribute** button and then clicking **Save**.</span></span> 
6. <span data-ttu-id="1b362-143">选择映射并单击 **运行**。</span><span class="sxs-lookup"><span data-stu-id="1b362-143">Select the map and click **Run**.</span></span>
