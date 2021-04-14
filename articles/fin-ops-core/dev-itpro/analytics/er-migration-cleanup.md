---
title: ER 迁移清理
description: 本主题说明如何使用 ER 迁移清理功能解决 ER 模板问题。
author: NickSelin
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, ERParameters, ERMigrationCleanup
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 97dbb625fc312548fb266b2ef6643a2b8e2b0f81
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750878"
---
# <a name="er-migration-cleanup"></a><span data-ttu-id="18bf8-103">ER 迁移清理</span><span class="sxs-lookup"><span data-stu-id="18bf8-103">ER migration cleanup</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="18bf8-104">在管理 Finance 实例时，您可能会决定将当前实例迁移到另一个位置。</span><span class="sxs-lookup"><span data-stu-id="18bf8-104">When you manage your Finance instances, you might decide to migrate your current instance to another location.</span></span> <span data-ttu-id="18bf8-105">例如，您可以将生产实例迁移到新的沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="18bf8-105">For example, you might migrate your production instance to a new sandbox environment.</span></span> <span data-ttu-id="18bf8-106">如果您将电子申报 (ER) 框架配置为将模板存储在 Microsoft Azure Blob 存储中，则新沙盒环境中的 **DocuValue** 表将在生产环境中引用 Blob 存储的实例。</span><span class="sxs-lookup"><span data-stu-id="18bf8-106">If you configured the Electronic reporting (ER) framework to store templates in Microsoft Azure Blob storage, the **DocuValue** table in the new sandbox environment refers to the instance of Blob storage in the production environment.</span></span> <span data-ttu-id="18bf8-107">但是，无法从沙盒环境访问此实例，因为迁移过程不支持迁移 Blob 存储中的项目。</span><span class="sxs-lookup"><span data-stu-id="18bf8-107">However, this instance can't be accessed from the sandbox environment because the migration process doesn't support the migration of artifacts in Blob storage.</span></span> <span data-ttu-id="18bf8-108">相反，预计在新沙盒环境中，您会引用尚未获得 ER 模板的沙盒环境中的 Blob 存储实例。</span><span class="sxs-lookup"><span data-stu-id="18bf8-108">Rather, it's expected that in the new sandbox environment, you refer to the instance of Blob storage in the sandbox environment that does not yet obtain the ER templates.</span></span>

<span data-ttu-id="18bf8-109">如果尝试运行使用模板生成业务文档的 ER 格式，则会发生异常，并且会通知您缺少的模板。</span><span class="sxs-lookup"><span data-stu-id="18bf8-109">If you try to run an ER format that uses a template to generate business documents, an exception occurs, and you're notified about the missing template.</span></span> <span data-ttu-id="18bf8-110">系统还会指导您使用 ER 迁移清理选项删除包含模板的 ER 格式配置，然后重新导入该配置。</span><span class="sxs-lookup"><span data-stu-id="18bf8-110">You're also guided to use the ER migration cleanup option to delete and then re-import the ER format configuration that contains the template.</span></span>

<span data-ttu-id="18bf8-111">[![运行 ER 格式](./media/er-migration-cleanup-run.png)](./media/er-migration-cleanup-run.png)</span><span class="sxs-lookup"><span data-stu-id="18bf8-111">[![Running an ER format](./media/er-migration-cleanup-run.png)](./media/er-migration-cleanup-run.png)</span></span>

<span data-ttu-id="18bf8-112">如果您导航到 **配置** 页面（**组织管理** \> **电子申报** \> **配置**）并位于配置树中，那么您将收到类似的错误，请尝试删除使用模板的 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="18bf8-112">You will receive a similar error if you navigate to the **Configurations** page (**Organization administration** \> **Electronic reporting** \> **Configurations**) and in the configurations tree, try to delete an ER format configuration that uses a template.</span></span>

<span data-ttu-id="18bf8-113">[![删除 ER 格式](./media/er-migration-cleanup-delete.png)](./media/er-migration-cleanup-delete.png)</span><span class="sxs-lookup"><span data-stu-id="18bf8-113">[![Deletion an ER format](./media/er-migration-cleanup-delete.png)](./media/er-migration-cleanup-delete.png)</span></span>

<span data-ttu-id="18bf8-114">完成以下步骤来解决您无法访问 ER 模板的问题。</span><span class="sxs-lookup"><span data-stu-id="18bf8-114">Complete the following steps to resolve issues with ER templates that you are unable to access.</span></span>

1.  <span data-ttu-id="18bf8-115">转到 **组织管理** \> **定期** \> **迁移清理** 页面。</span><span class="sxs-lookup"><span data-stu-id="18bf8-115">Go to **Organization administration** \> **Periodic** \> **Migration cleanup** page.</span></span>
2.  <span data-ttu-id="18bf8-116">选择无法执行或删除的 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="18bf8-116">Select an ER format configuration that can’t be executed or deleted.</span></span>
3.  <span data-ttu-id="18bf8-117">选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="18bf8-117">Select **Delete**.</span></span>
4.  <span data-ttu-id="18bf8-118">确认删除所选的 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="18bf8-118">Confirm the deletion of the selected ER format configuration.</span></span>
5.  <span data-ttu-id="18bf8-119">将已删除的 ER 格式配置[导入](download-electronic-reporting-configuration-lcs.md)到当前的 Finance 实例中。</span><span class="sxs-lookup"><span data-stu-id="18bf8-119">[Import](download-electronic-reporting-configuration-lcs.md) the deleted ER format configuration to the current Finance instance.</span></span>

## <a name="applicability"></a><span data-ttu-id="18bf8-120">适用性</span><span class="sxs-lookup"><span data-stu-id="18bf8-120">Applicability</span></span>

> <span data-ttu-id="18bf8-121">[重要提示] **迁移清理** 选项仅适用于包含不可访问的 ER 模板的 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="18bf8-121">[Important] The **Migration cleanup** option is targeted only for ER format configurations that contain non-accessible ER templates.</span></span> <span data-ttu-id="18bf8-122">当您使用 **迁移清理** 选项删除 ER 格式配置时，ER 会删除与唯一应用程序数据库中的配置项目相关的模板。</span><span class="sxs-lookup"><span data-stu-id="18bf8-122">When you delete an ER format configuration by using the **Migration cleanup** option, ER deletes the templates that are related to the configuration artifacts in the only application database.</span></span> <span data-ttu-id="18bf8-123">未验证 Blob 存储中是否存在合适的物理文件。</span><span class="sxs-lookup"><span data-stu-id="18bf8-123">The existence of the appropriate physical files in Blob storage are not validated.</span></span> <span data-ttu-id="18bf8-124">相反，假定不存在这些文件。</span><span class="sxs-lookup"><span data-stu-id="18bf8-124">Instead, it is assumed that there are none.</span></span> <span data-ttu-id="18bf8-125">因此，请勿使用 **迁移清理** 选项代替 **配置** 页面上的 ER 配置删除选项。</span><span class="sxs-lookup"><span data-stu-id="18bf8-125">Therefore, do not use the **Migration cleanup** option as an alternative to the ER configuration deletion option on the **Configurations** page.</span></span> <span data-ttu-id="18bf8-126">仅当 **配置** 页面上的 ER 配置删除选项失效时，才使用 **迁移清理** 选项。</span><span class="sxs-lookup"><span data-stu-id="18bf8-126">Use the **Migration cleanup** option only when the ER configuration deletion option on the **Configurations** page failed.</span></span>
>
> <span data-ttu-id="18bf8-127">在 Blob 存储中有可用的引用模板时，如果使用 **迁移清理** 选项删除 ER 格式配置，则将仅删除应用程序数据库中的相关配置项目。</span><span class="sxs-lookup"><span data-stu-id="18bf8-127">If you use the **Migration cleanup** option to delete an ER format configuration when the referred template is available in the Blob storage, you only delete related configuration artifacts in the application database.</span></span> <span data-ttu-id="18bf8-128">Blob 存储中的模板物理文件仍然保留。</span><span class="sxs-lookup"><span data-stu-id="18bf8-128">The physical file of the template in the Blob storage remains.</span></span> <span data-ttu-id="18bf8-129">不再允许在 Blob 存储中覆盖文件。</span><span class="sxs-lookup"><span data-stu-id="18bf8-129">File overwriting in Blob storage is no longer allowed.</span></span> <span data-ttu-id="18bf8-130">有关详细信息，请参阅 [KB4557217](https://fix.lcs.dynamics.com/Issue/Details?kb=4557217)。</span><span class="sxs-lookup"><span data-stu-id="18bf8-130">For more information, see [KB4557217](https://fix.lcs.dynamics.com/Issue/Details?kb=4557217).</span></span> <span data-ttu-id="18bf8-131">此外，您将无法再重新导入在该环境中使用迁移清理删除的配置。</span><span class="sxs-lookup"><span data-stu-id="18bf8-131">Additionally, you will no longer be able to re-import the configurations deleted by using the Migration cleanup in this environment.</span></span> <span data-ttu-id="18bf8-132">要解决此问题，您需要在 Blob 存储中找到相应的文件并手动将其删除。</span><span class="sxs-lookup"><span data-stu-id="18bf8-132">To resolve this issue, you need to find the corresponding file in Blob storage and manually delete it.</span></span>

<span data-ttu-id="18bf8-133">[![导入 ER 格式](./media/er-migration-cleanup-import.png)](./media/er-migration-cleanup-import.png)</span><span class="sxs-lookup"><span data-stu-id="18bf8-133">[![Importing an ER format](./media/er-migration-cleanup-import.png)](./media/er-migration-cleanup-import.png)</span></span>

<span data-ttu-id="18bf8-134">如果将应用程序实例迁移到已多次用作迁移目标的另一个位置，并且 Blob 存储已经包含其 ER 模板文件，则可能会发生类似的问题。</span><span class="sxs-lookup"><span data-stu-id="18bf8-134">A similar issue may occur if you migrate your application instance to another location that has been used as a migration target more than once and for which the Blob storage already contains ER template files.</span></span>

<span data-ttu-id="18bf8-135">因为您可以具有几种 ER 格式配置，所以此过程可能很耗时。</span><span class="sxs-lookup"><span data-stu-id="18bf8-135">Because you can have several ER format configurations, this process can be time consuming.</span></span> <span data-ttu-id="18bf8-136">因此，最好使用 [ER 模板的备份存储](er-backup-storage-templates.md)功能自动恢复具有被破坏的引用的模板。</span><span class="sxs-lookup"><span data-stu-id="18bf8-136">Therefore, using the [Backup storage of ER templates](er-backup-storage-templates.md) feature to automatically recover templates with broken references is preferred.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]