---
title: Dynamics 365 Talent - Core HR（2018 年 10 月 31 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent - Core HR 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4851c62a19bb562c7f5f578aecbae99cfcdb982f
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897365"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-31-2018"></a><span data-ttu-id="c5a5b-103">Dynamics 365 Talent - Core HR（2018 年 10 月 31 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="c5a5b-103">What's new or changed in Dynamics 365 Talent - Core HR (October 31, 2018)</span></span>

<span data-ttu-id="c5a5b-104">**内部版本 8.1.2031**</span><span class="sxs-lookup"><span data-stu-id="c5a5b-104">**Build 8.1.2031**</span></span>

<span data-ttu-id="c5a5b-105">此主题介绍了 Core HR 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="create-links-from-talent-to-finance"></a><span data-ttu-id="c5a5b-106">创建从 Talent 到 Finance 的链接</span><span class="sxs-lookup"><span data-stu-id="c5a5b-106">Create links from Talent to Finance</span></span>
<span data-ttu-id="c5a5b-107">此新导航功能允许您从 Talent 链接到 Finance ，为您提供访问 Finance 页面的直接导航。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-107">This new navigation functionality allows you to link from Talent to Finance, giving you direct navigation into Finance pages.</span></span> <span data-ttu-id="c5a5b-108">在链接配置后，您可以指定链接应在 Talent 中显现的名称和组，以及要在 Finance 内打开的目标页。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-108">When links are configured, you can specify the name and group of the link, where the link should surface in Talent, and the target page to be opened within Finance.</span></span>

#### <a name="coming-soon"></a><span data-ttu-id="c5a5b-109">即将到期</span><span class="sxs-lookup"><span data-stu-id="c5a5b-109">Coming soon</span></span>
<span data-ttu-id="c5a5b-110">未来将添加字段上下文，以允许直接导航到 Finance 中的相应记录。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-110">Field context will be added in the future to allow for direct navigation to corresponding records in Finance.</span></span> <span data-ttu-id="c5a5b-111">例如，您可以使用**链接到字段**提供上下文以直接导航到 Finance 中的特定员工或职位。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-111">For example, you can use **Link to field** to provide the context to navigate directly to a specific employee or position in Finance.</span></span>

### <a name="configure-target-systems"></a><span data-ttu-id="c5a5b-112">配置目标系统</span><span class="sxs-lookup"><span data-stu-id="c5a5b-112">Configure target systems</span></span>

<span data-ttu-id="c5a5b-113">在 Talent 中，系统管理员可以定义将通过系统管理工作区显现的链接。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-113">In Talent, system administrators can define links that will be surfaced through the System Administration workspace.</span></span> <span data-ttu-id="c5a5b-114">配置的一部分是您希望作为链接“目标”导航到的 Finance 环境。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-114">Part of the configuration is the Finance environments that you would like to navigate to as the "target" of the link.</span></span> <span data-ttu-id="c5a5b-115">您可以通过向目标系统提供名称并提供 Finance 环境的 URL 来完成此任务。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-115">You do this by giving the target system a name and providing the URL of the Finance environment.</span></span> <span data-ttu-id="c5a5b-116">这是您会提供的 Finance URL 的示例：https://devax00124aos.cloud.test.dynamics.com/。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-116">Here is an example of a Finance URL that you would provide: https://devax00124aos.cloud.test.dynamics.com/.</span></span> <span data-ttu-id="c5a5b-117">在配置您的目标系统后，您可以定义您的链接。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-117">After you have configured your target systems,  you can define your links.</span></span>

### <a name="configure-links"></a><span data-ttu-id="c5a5b-118">配置链接</span><span class="sxs-lookup"><span data-stu-id="c5a5b-118">Configure links</span></span>

<span data-ttu-id="c5a5b-119">创建的每个链接将定义了以下信息。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-119">Each link that is created will have the following information defined.</span></span>

- <span data-ttu-id="c5a5b-120">链接 - 链接的名称，仅用于标识。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-120">Link - Name of the link, used for identification only.</span></span>

- <span data-ttu-id="c5a5b-121">启用此链接 - 如果要向 Talent 用户显示链接，请设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-121">Enable this Link - Set to **Yes** if you want to display the link to users of Talent.</span></span>

- <span data-ttu-id="c5a5b-122">显示名称 - 定义将显示为 Finance 的链接的名称。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-122">Display name - Define the name that will appear as a link to Finance.</span></span> <span data-ttu-id="c5a5b-123">此数据当前没有翻译。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-123">This data is currently is not translated.</span></span>

- <span data-ttu-id="c5a5b-124">窗体上的表面链接 - 选择您希望显示链接的页面。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-124">Surface link on form - Choose which page you would like to display the link on.</span></span>

- <span data-ttu-id="c5a5b-125">组 - 组不是必要的，不过，如果您希望使用组来管理链接，请使用**组**字段选择现有组或创建新组。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-125">Group - Groups are not required, but if you want to organize your links using groups, select an existing group or create a new one using the **Group** field.</span></span>

- <span data-ttu-id="c5a5b-126">目标系统 - 选择使用**配置目标系统**选项创建的目标系统。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-126">Target system - Select the target system that was created using the **Configure target system** option.</span></span> <span data-ttu-id="c5a5b-127">这将是在使用链接导航时使用的 Finance 环境。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-127">This will be the Finance environment that will be used when navigating by using the link.</span></span>

- <span data-ttu-id="c5a5b-128">使用用户的当前公司 - 如果您希望在导航到 Finance 时使用用户的当前公司上下文，请选择**是**。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-128">Use user's current Company - Select **Yes** if you would like to use the User's current company context when navigating to Finance.</span></span> <span data-ttu-id="c5a5b-129">如果选择**否**，您可以选择应使用的公司。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-129">If **No** is selected, then you can select the company that should be used.</span></span>

- <span data-ttu-id="c5a5b-130">目标菜单项 - 输入导航时链接应使用的 Finance 的菜单项。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-130">Target menu item - Enter the menu item from Finance that the link should use when navigating.</span></span> <span data-ttu-id="c5a5b-131">提供您可以直接导航的菜单项。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-131">Menu items that you can directly navigate to are available.</span></span> <span data-ttu-id="c5a5b-132">若要查找所需的菜单项，打开 Finance 并打开作为导航目标的页面。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-132">To find the menu item required, open Finance and open the page that is the target of the navigation.</span></span> <span data-ttu-id="c5a5b-133">从 URL 复制菜单项。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-133">Copy the menu item from the URL.</span></span> <span data-ttu-id="c5a5b-134">例如，如果您希望链接将您带到 Finance and Operations 中的员工列表，请输入在 URL 中的 "&mi" 后出现的值。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-134">For example, if you want the link to take you to the employee list in Finance and Operations, enter the value that appears after the "&mi" in the URL.</span></span> <span data-ttu-id="c5a5b-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span></span> <span data-ttu-id="c5a5b-136">在本示例中导航到员工列表页面的菜单项是：HcmWorkerListPage_Employees。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-136">The menu item to navigate to the employee list page in this example is: HcmWorkerListPage_Employees.</span></span>

- <span data-ttu-id="c5a5b-137">链接到数据源 - 选择链接所引用数据的源。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-137">Link to data source - Select the source of data that the link is referencing.</span></span> <span data-ttu-id="c5a5b-138">提供最常见的源，如**工作人员**和**职位**。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-138">The most common sources like **Worker** and **Position** are available.</span></span>

- <span data-ttu-id="c5a5b-139">链接到字段 -（即将推出）选择此字段将允许从 Talent 中的单一记录直接导航到 Finance 中的单一记录。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-139">Link to field - (Coming soon) This field selection will allow for direct navigation from a single record in Talent to a single record in Finance.</span></span>

### <a name="access-to-links"></a><span data-ttu-id="c5a5b-140">访问链接</span><span class="sxs-lookup"><span data-stu-id="c5a5b-140">Access to links</span></span>

<span data-ttu-id="c5a5b-141">系统管理员将在定义的页面上看到新创建的链接，即使**启用此链接**选项设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-141">System administrators will see the newly created links on the defined pages even if the **Enable this link** option is set to **No**.</span></span> <span data-ttu-id="c5a5b-142">这可以用于在向其他员工显示链接前对链接进行测试。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-142">This can be used for testing links prior to surfacing them to other employees.</span></span> <span data-ttu-id="c5a5b-143">在**启用此链接**选项设置为**是**后，所有其他角色将只能看到配置的链接。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-143">All other roles will only see the configured links after the **Enable this link** option is set to **Yes**.</span></span> <span data-ttu-id="c5a5b-144">有权访问链接显示页面的员工将有权访问这些链接。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-144">Employees who have access to the pages in which the links are surfaced will have access to the links.</span></span>

<span data-ttu-id="c5a5b-145">用户还可以定义 Finance 内的安全权限以在 Finance and Operations 中访问页面。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-145">Users can also have security rights within Finance defined to access the pages in Finance and Operations.</span></span> <span data-ttu-id="c5a5b-146">如果未定义，在使用链接时将显示安全对话框。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-146">If they don't, a security dialog box will be displayed when using the link.</span></span>


## <a name="other-changesfixes"></a><span data-ttu-id="c5a5b-147">其他更改/修复</span><span class="sxs-lookup"><span data-stu-id="c5a5b-147">Other changes/fixes</span></span>

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a><span data-ttu-id="c5a5b-148">具有未来开始日期的职位不能分配给新员工</span><span class="sxs-lookup"><span data-stu-id="c5a5b-148">Positions with a future start date cannot be assigned to a new employee</span></span>

<span data-ttu-id="c5a5b-149">为允许员工被分配未来日期的职位进行了更改。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-149">Changes have been made to allow employee assignments to future-dated positions.</span></span> <span data-ttu-id="c5a5b-150">可以选择开始日期在将来的职位，员工分配将在工作流保存或完成后进行（如果启用了工作流）。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-150">Positions that have start dates in the future can be selected and the employee assignment will be made upon save or completion of the workflow (if the workflow is enabled).</span></span>

### <a name="new-employee-cannot-be-assigned-existing-position"></a><span data-ttu-id="c5a5b-151">新员工不能被分配现有职位</span><span class="sxs-lookup"><span data-stu-id="c5a5b-151">New employee cannot be assigned existing position</span></span>

<span data-ttu-id="c5a5b-152">进行了相应更改，新员工现在可以被分配到现有职位。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-152">Changes have been made so new employee assignment can now be assigned to existing positions.</span></span>

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a><span data-ttu-id="c5a5b-153">当雇用开始日期在过去时，受聘日期/办公地点在保存记录时消息。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-153">Seniority date/Office location disappears when the employment start date is in the past and the record is saved</span></span>

<span data-ttu-id="c5a5b-154">进行了相应更改，更正了在为以往员工保存更改时**受聘日期**和**办公地点**的可见性。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-154">Changes have been made to correct the visibilty of the **Senority date** and **Office location** when saving changes for past employees.</span></span>

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a><span data-ttu-id="c5a5b-155">无法在工作人员页面为将来日期的雇用输入数据</span><span class="sxs-lookup"><span data-stu-id="c5a5b-155">Can't enter data for future-dated employments on the worker page</span></span>

<span data-ttu-id="c5a5b-156">将来日期的雇用的雇用数据已在主工作人员页面禁用。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-156">Employment data for future-dated employments has been disabled on the main worker page.</span></span> <span data-ttu-id="c5a5b-157">雇用数据可以通过**日期管理器**页面输入。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-157">Employment data can be entered through the **Date Manager** pages.</span></span> <span data-ttu-id="c5a5b-158">未来发布中将进行更多更改来支持直接在工作流程中输入雇用数据。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-158">Additional changes will be made in future releases to enable entering employment data directly during the workflow process.</span></span>

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a><span data-ttu-id="c5a5b-159">将 ValidFrom 和 ValidTo 添加到 HcmPersonalContactPersonEntity 中</span><span class="sxs-lookup"><span data-stu-id="c5a5b-159">Add ValidFrom and ValidTo to HcmPersonalContactPersonEntity</span></span>

<span data-ttu-id="c5a5b-160">数据管理框架 (DMF) 实体 HcmPersonalContactPersonEntity 已更新，以包括支持某些福利集成场景的“生效”和“失效”日期。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-160">The Data Management Framework (DMF) entity HcmPersonalContactPersonEntity has been updated to include "valid from" and "valid to" dates to enable certain benefit integration scenarios.</span></span> 

## <a name="known-issue"></a><span data-ttu-id="c5a5b-161">已知问题</span><span class="sxs-lookup"><span data-stu-id="c5a5b-161">Known issue</span></span>
- <span data-ttu-id="c5a5b-162">**问题**：在将新附件添加到工作人员时，**新建**和**编辑**按钮变灰。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-162">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="c5a5b-163">**解决方法：** 打开附件页面之前，确保已关闭**工作人员**页面中的速见表。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-163">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="c5a5b-164">如果加载**工作人员**页面时速见表已关闭，将启用附件按钮。</span><span class="sxs-lookup"><span data-stu-id="c5a5b-164">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="c5a5b-165">（下一个平台更新中将解决这个问题。）</span><span class="sxs-lookup"><span data-stu-id="c5a5b-165">(This issue will be fixed in the next platform update.)</span></span>
