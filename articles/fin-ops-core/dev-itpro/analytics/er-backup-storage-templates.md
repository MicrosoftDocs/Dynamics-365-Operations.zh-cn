---
title: ER 模板的备份存储
description: 此主题介绍如何使用电子申报 (ER) 备份存储来恢复模板。
author: NickSelin
manager: AnnBe
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-13
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d1bf2f13833b4441812b1c5326f897415c752091
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565617"
---
# <a name="backup-storage-of-er-templates"></a><span data-ttu-id="fdff4-103">ER 模板的备份存储</span><span class="sxs-lookup"><span data-stu-id="fdff4-103">Backup storage of ER templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fdff4-104">业务用户可使用[电子申报 (ER) 概览](general-electronic-reporting.md)根据各个国家和地区的法律要求配置传出文档的格式。</span><span class="sxs-lookup"><span data-stu-id="fdff4-104">The [Electronic reporting (ER) overview](general-electronic-reporting.md) lets business users configure formats for outbound documents according to the legal requirements of various countries and regions.</span></span> <span data-ttu-id="fdff4-105">配置的 ER 格式可使用预定义的模板生成各种格式（如 Microsoft Excel 工作簿、Microsoft Word 文档或 PDF 文档）的传出文档。</span><span class="sxs-lookup"><span data-stu-id="fdff4-105">Configured ER formats can use predefined templates to generate outbound documents in various formats, such as Microsoft Excel workbooks, Microsoft Word documents, or PDF documents.</span></span> <span data-ttu-id="fdff4-106">已经使用为生成的文档配置的数据流所需数据填充了模板。</span><span class="sxs-lookup"><span data-stu-id="fdff4-106">The templates are filled with data that the configured dataflow for generated documents requires.</span></span>

<span data-ttu-id="fdff4-107">可以在 ER 解决方案中发布配置的每种格式。</span><span class="sxs-lookup"><span data-stu-id="fdff4-107">Each configured format can be published as part of an ER solution.</span></span> <span data-ttu-id="fdff4-108">可以从一个 Finance and Operations 实例导出每个 ER 解决方案，然后将其导入到另一个实例中。</span><span class="sxs-lookup"><span data-stu-id="fdff4-108">Each ER solution can be exported from one instance of Finance and Operations and imported into another instance.</span></span>

<span data-ttu-id="fdff4-109">ER 框架使用[配置文档管理](../../fin-ops/organization-administration/configure-document-management.md)保留当前 Finance and Operations 实例所需的模板。</span><span class="sxs-lookup"><span data-stu-id="fdff4-109">The ER framework uses the [Configure document management](../../fin-ops/organization-administration/configure-document-management.md) to keep the required templates for the current Finance and Operations instance.</span></span> <span data-ttu-id="fdff4-110">可以根据 ER 框架的设置，将 Microsoft Azure Blob 存储或 Microsoft SharePoint 文件夹选作模板的物理主存储位置。</span><span class="sxs-lookup"><span data-stu-id="fdff4-110">Depending on the settings of the ER framework, Microsoft Azure Blob storage or a Microsoft SharePoint folder can be selected as the physical primary storage location for templates.</span></span> <span data-ttu-id="fdff4-111">（有关详细信息，请参阅[配置电子申报 (ER) 框架](electronic-reporting-er-configure-parameters.md)。）DocuValue 表中是每个模板的单个记录。</span><span class="sxs-lookup"><span data-stu-id="fdff4-111">(For more information, see [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md).) The DocuValue table holds an individual record for each template.</span></span> <span data-ttu-id="fdff4-112">在每个记录中，**AccessInformation** 字段中存储模板文件在配置的存储位置内的路径。</span><span class="sxs-lookup"><span data-stu-id="fdff4-112">In each record, the **AccessInformation** field stores the path of a template file that is located in the configured storage location.</span></span>

<span data-ttu-id="fdff4-113">在管理 Finance and Operations 实例时，您可能会决定将当前实例迁移到另一个位置。</span><span class="sxs-lookup"><span data-stu-id="fdff4-113">When you manage your Finance and Operations instances, you might decide to migrate the current instance to another location.</span></span> <span data-ttu-id="fdff4-114">例如，您可以将生产实例迁移到新的沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="fdff4-114">For example, you might migrate your production instance to a new sandbox environment.</span></span> <span data-ttu-id="fdff4-115">如果将 ER 框架配置为把模板存储到 Blob 存储中，则新沙盒环境中的 DocuValue 表引用生产环境中的 Blob 存储实例。</span><span class="sxs-lookup"><span data-stu-id="fdff4-115">If you configured the ER framework to store templates in Blob storage, the DocuValue table in the new sandbox environment refers to the instance of Blob storage in the production environment.</span></span> <span data-ttu-id="fdff4-116">但是，不能从沙盒环境访问此实例，因为迁移过程不支持迁移 Blob 存储中的项目。</span><span class="sxs-lookup"><span data-stu-id="fdff4-116">However, this instance can't be accessed from the sandbox environment, because the migration process doesn't support the migration of artifacts in Blob storage.</span></span> <span data-ttu-id="fdff4-117">因此，如果尝试运行使用模板的 ER 格式来生成业务文档，将发生异常，并通知您缺少模板。</span><span class="sxs-lookup"><span data-stu-id="fdff4-117">Therefore, if you try to run an ER format that uses a template to generate business documents, an exception occurs, and you're notified about the missing template.</span></span> <span data-ttu-id="fdff4-118">还将引导您使用 ER 清理工具删除再重新导入其中包含此模板的 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="fdff4-118">You're also guided to use the ER cleanup tool to delete and then re-import the ER format configuration that contains the template.</span></span> <span data-ttu-id="fdff4-119">因为您可能有多个 ER 格式配置，所以此过程可能需要很长时间。</span><span class="sxs-lookup"><span data-stu-id="fdff4-119">Because you might have several ER format configurations, this process can be time consuming.</span></span>

<span data-ttu-id="fdff4-120">ER 模板的备份存储功能可帮助您创建模板，这样始终可以使用这些模板来生成业务文档。</span><span class="sxs-lookup"><span data-stu-id="fdff4-120">The Backup storage of ER templates feature can help you make your templates so that they are always available to generate business documents.</span></span>

> [!NOTE]
> <span data-ttu-id="fdff4-121">仅当已选择 Blob 存储作为 ER 模板的物理存储位置，才能使用此功能。</span><span class="sxs-lookup"><span data-stu-id="fdff4-121">This feature can be used only when Blob storage has been selected as the physical storage location for ER templates.</span></span>

## <a name="automated-recovery-and-notification"></a><span data-ttu-id="fdff4-122">自动恢复和通知</span><span class="sxs-lookup"><span data-stu-id="fdff4-122">Automated recovery and notification</span></span>

<span data-ttu-id="fdff4-123">对于此功能，如果发生以下事件，将把当前环境中新 ER 格式配置的每个模板自动保存到模板的备份存储位置（ERDocuDatabaseStorage 数据库表）：</span><span class="sxs-lookup"><span data-stu-id="fdff4-123">For this feature, every template of a new ER format configuration in the current environment is automatically saved to the backup storage location for templates (the ERDocuDatabaseStorage database table) when the following events occur:</span></span>

- <span data-ttu-id="fdff4-124">导入其中包含模板的新 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="fdff4-124">You import a new ER format configuration that contains a template.</span></span>
- <span data-ttu-id="fdff4-125">完成其中包含模板的 ER 格式配置的草稿版本。</span><span class="sxs-lookup"><span data-stu-id="fdff4-125">You complete the draft version of an ER format configuration that contains a template.</span></span>

<span data-ttu-id="fdff4-126">模板的备份副本会作为应用程序数据库的一部分迁移到 Finance and Operations 的新实例。</span><span class="sxs-lookup"><span data-stu-id="fdff4-126">Backup copies of templates are migrated to a new instance of Finance and Operations as part of the application database.</span></span>

<span data-ttu-id="fdff4-127">如果需要 ER 格式的模板才能生成传出文档（例如，为了处理其中包含付款通知和控制报告的供应商付款），但是未在主存储位置中找到所需模板，则会发生以下事件：</span><span class="sxs-lookup"><span data-stu-id="fdff4-127">If a template of an ER format is required for generation of outbound documents, to process vendor payments including generation of payment advice and control reports, for example, but the required template isn't found in the primary storage location, the following events occur:</span></span>

- <span data-ttu-id="fdff4-128">如果备份存储位置中有此模板，则会从备份存储位置自动提取该模板，还原到主存储位置，用于当前执行。</span><span class="sxs-lookup"><span data-stu-id="fdff4-128">If the template is available in the backup storage location, it is automatically taken from the backup storage location, restored to the primary storage location, and used for the current execution.</span></span>
- <span data-ttu-id="fdff4-129">将通过操作中心向为其分配了 **电子申报开发人员** 或 **系统管理员** 角色的每位用户通知发生了缺少模板问题。</span><span class="sxs-lookup"><span data-stu-id="fdff4-129">Every user who is assigned to the **Electronic reporting developer** or **System administrator** role is notified about the missing template issue through the Action center.</span></span> <span data-ttu-id="fdff4-130">显示的消息取决于 **自动运行受损附件批量还原** 参数的值：</span><span class="sxs-lookup"><span data-stu-id="fdff4-130">The message that appears depends on the value of the **Automatically run the procedure of restoring the broken templates in batch** parameter:</span></span>

    - <span data-ttu-id="fdff4-131">如果此参数设置为 **关**，则此消息将建议您开始执行批处理流程以自动修复其他 ER 格式配置模板的相似问题。</span><span class="sxs-lookup"><span data-stu-id="fdff4-131">If this parameter is set to **Off**, the message recommends that you start the batch process to automatically fix similar issues for other ER format configuration templates.</span></span> <span data-ttu-id="fdff4-132">此消息中有一个链接，可用于启动批处理流程。</span><span class="sxs-lookup"><span data-stu-id="fdff4-132">The message includes a link that you can use to start the batch process.</span></span>
    - <span data-ttu-id="fdff4-133">如果此参数设置为 **开**，此消息将通知您，说明已发现了缺少模板问题，并且已自动安排了新的批处理流程 **通过内部数据库备份还原受损模板**。</span><span class="sxs-lookup"><span data-stu-id="fdff4-133">If this parameter is set to **On**, the message notifies you that a missing templates issue has been discovered, and that a new batch process, **Restore broken templates from internal database backup**, has been automatically scheduled.</span></span> <span data-ttu-id="fdff4-134">此批处理流程将自动修复其他模板的相似问题。</span><span class="sxs-lookup"><span data-stu-id="fdff4-134">This batch process will automatically fix similar issues for other templates.</span></span>

<span data-ttu-id="fdff4-135">若要设置 **自动运行受损附件批量还原** 参数，请完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="fdff4-135">To set up the **Automatically run the procedure of restoring the broken templates in batch** parameter, complete the following steps:</span></span>

1. <span data-ttu-id="fdff4-136">在 Finance and Operations 中，打开 **组织管理 \> 电子申报 \> 配置页面**。</span><span class="sxs-lookup"><span data-stu-id="fdff4-136">In Finance and Operations, open the **Organization administration \> Electronic reporting \> Configurations page**.</span></span>
2. <span data-ttu-id="fdff4-137">在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。</span><span class="sxs-lookup"><span data-stu-id="fdff4-137">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="fdff4-138">在 **用户参数** 对话框中，设置 **自动运行受损附件批量还原** 参数所需值。</span><span class="sxs-lookup"><span data-stu-id="fdff4-138">In the **User parameters** dialog box, set the required value for the **Automatically run the procedure of restoring the broken templates in batch** parameter.</span></span>

> [!NOTE]
> <span data-ttu-id="fdff4-139">此参数定义为应用程序用户，并特定于记录的公司。</span><span class="sxs-lookup"><span data-stu-id="fdff4-139">This parameter is defined as application user and logged company specific.</span></span>

![ER 配置页](./media/GER-BackupTemplates-1.png)

<span data-ttu-id="fdff4-141">下图显示当 **自动运行受损附件批量还原** 参数设置为 **开** 时显示的消息的示例。</span><span class="sxs-lookup"><span data-stu-id="fdff4-141">The following illustration shows an example of the message that appears when the **Automatically run the procedure of restoring the broken templates in batch** parameter is set to **On**.</span></span>

![供应商付款日记帐页](./media/GER-BackupTemplates-2.png)

<span data-ttu-id="fdff4-143">下图显示 **批处理作业** 页上的 **通过内部数据库备份还原受损模板** 批处理流程。</span><span class="sxs-lookup"><span data-stu-id="fdff4-143">The following illustration shows the **Restore broken templates from internal database backup** batch process on the **Batch job** page.</span></span>

![批处理作业页](./media/GER-BackupTemplates-3.png)

<span data-ttu-id="fdff4-145">已完成的 **通过内部数据库备份还原受损模板** 批处理流程的执行日志中包含有关已从备份存储位置还原到主存储位置的模板的信息。</span><span class="sxs-lookup"><span data-stu-id="fdff4-145">The execution log of the completed **Restore broken templates from internal database backup** batch process includes information about the templates that have been restored from the backup storage location to the primary storage location.</span></span>

![批处理作业历史记录页](./media/GER-BackupTemplates-4.png)

<span data-ttu-id="fdff4-147">命若琴弦看，已开启 ER 格式配置中的模板的自动创建备份副本流程。</span><span class="sxs-lookup"><span data-stu-id="fdff4-147">By default, the process of automatically creating backup copies of templates that reside in ER format configurations is turned on.</span></span> <span data-ttu-id="fdff4-148">若要停止创建模板的备份副本，请将 **电子申报参数** 页 **附件** 选项卡上的 **停止制作模板的备份副本** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="fdff4-148">To stop making backup copies of templates, set the **Stop making backup copies of template** option to **Yes** on the **Attachments** tab of the **Electronic reporting parameters** page.</span></span> <span data-ttu-id="fdff4-149">可从 **电子申报** 工作区打开此页。</span><span class="sxs-lookup"><span data-stu-id="fdff4-149">You can open this page from the **Electronic reporting** workspace.</span></span>

<span data-ttu-id="fdff4-150">如果将 **停止制作模板的备份副本** 选项设置为 **是**，但是不希望保留以前创建的模板备份副本，请选择 **电子申报参数** 页上的 **清理备份存储**。</span><span class="sxs-lookup"><span data-stu-id="fdff4-150">If you set the **Stop making backup copies of templates** option to **Yes** and don't want to keep the backup copies that were previously made of templates, select **Clean up backup storage** on the **Electronic reporting parameters** page.</span></span>

<span data-ttu-id="fdff4-151">如果您已将环境升级到 Finance and Operations 版本 10.0.5（2019 年 10 月），并想迁移到包含可以运行的 ER 格式配置的新环境，请选择 **电子申报参数** 页面上的 **填写备份存储**，然后进行迁移。</span><span class="sxs-lookup"><span data-stu-id="fdff4-151">If you upgraded your environment to Finance and Operations version 10.0.5 (October 2019) and want to migrate to a new environment that includes ER format configurations that can be run, select **Fill in backup storage** on the **Electronic reporting parameters** page before the migration occurs.</span></span> <span data-ttu-id="fdff4-152">此按钮用于开始创建所有可用模板的备份副本，所以可将其存储到模板的 ER 备份存储位置中。</span><span class="sxs-lookup"><span data-stu-id="fdff4-152">This button starts the process of making backup copies of all available templates, so that they can be stored in the ER backup storage location for templates.</span></span>

![“电子申报参数”页面](./media/GER-BackupTemplates-5.png)

## <a name="manual-recovery"></a><span data-ttu-id="fdff4-154">手动回收</span><span class="sxs-lookup"><span data-stu-id="fdff4-154">Manual recovery</span></span>

<span data-ttu-id="fdff4-155">转到 **组织管理** \> **电子申报** \> **恢复损坏的模板**，以手动启动将 ER 模板从备份存储位置恢复到主存储位置的过程。</span><span class="sxs-lookup"><span data-stu-id="fdff4-155">Go to **Organization administration** \> **Electronic reporting** \> **Restore broken templates** to manually initiate the process of restoring ER templates from the backup storage location to the primary storage location.</span></span> <span data-ttu-id="fdff4-156">在开始此过程之前，在 **恢复损坏的模板** 页面上，您可以指定是将交互执行此过程，还是将为此计划批处理。</span><span class="sxs-lookup"><span data-stu-id="fdff4-156">Before you start this process, on the **Restore broken templates** page you can specify whether it will be performed interactively, or the batch process will be scheduled for this.</span></span>

## <a name="supported-deployments"></a><span data-ttu-id="fdff4-157">支持的部署</span><span class="sxs-lookup"><span data-stu-id="fdff4-157">Supported deployments</span></span>

<span data-ttu-id="fdff4-158">在 Finance and Operations 版本 10.0.5 中，ER 模板的备份存储功能仅在云部署中可用。</span><span class="sxs-lookup"><span data-stu-id="fdff4-158">In Finance and Operations version 10.0.5, the Backup storage of ER templates feature is available only in cloud deployments.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fdff4-159">其他资源</span><span class="sxs-lookup"><span data-stu-id="fdff4-159">Additional resources</span></span>

[<span data-ttu-id="fdff4-160">电子申报 (ER) 概览</span><span class="sxs-lookup"><span data-stu-id="fdff4-160">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="fdff4-161">配置电子报告 (ER) 框架</span><span class="sxs-lookup"><span data-stu-id="fdff4-161">Configure the Electronic reporting (ER) framework</span></span>](electronic-reporting-er-configure-parameters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]