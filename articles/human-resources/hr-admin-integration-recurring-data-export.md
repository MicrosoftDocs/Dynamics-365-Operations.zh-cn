---
title: 创建重复性数据导出应用
description: 本文介绍如何创建按重复执行的计划从 Microsoft Dynamics 365 Human Resources 导出数据的 Microsoft Azure 逻辑应用。
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
ms.openlocfilehash: edd4b999624a845fc145ed9ff348ae9cba782719
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008180"
---
# <a name="create-a-recurring-data-export-app"></a><span data-ttu-id="370f3-103">创建重复性数据导出应用</span><span class="sxs-lookup"><span data-stu-id="370f3-103">Create a recurring data export app</span></span>

<span data-ttu-id="370f3-104">本文介绍如何创建按重复执行的计划从 Microsoft Dynamics 365 Human Resources 导出数据的 Microsoft Azure 逻辑应用。</span><span class="sxs-lookup"><span data-stu-id="370f3-104">This article shows how to create a Microsoft Azure logic app that exports data from Microsoft Dynamics 365 Human Resources on a recurring schedule.</span></span> <span data-ttu-id="370f3-105">本教程利用 Human Resources 的 DMF 包 REST 应用程序编程接口 (API) 来导出数据。</span><span class="sxs-lookup"><span data-stu-id="370f3-105">The tutorial takes advantage of Human Resources' DMF package REST application programming interface (API) to export the data.</span></span> <span data-ttu-id="370f3-106">导出数据后，逻辑应用将导出的数据包保存到 Microsoft OneDrive for Business 文件夹。</span><span class="sxs-lookup"><span data-stu-id="370f3-106">After the data has been exported, the logic app saves the exported data package to a Microsoft OneDrive for Business folder.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="370f3-107">业务方案</span><span class="sxs-lookup"><span data-stu-id="370f3-107">Business scenario</span></span>

<span data-ttu-id="370f3-108">在 Microsoft Dynamics 365 集成的一种典型业务方案中，必须按重复执行的计划将数据导出到下游系统。</span><span class="sxs-lookup"><span data-stu-id="370f3-108">In one typical business scenario for Microsoft Dynamics 365 integrations, data must be exported to a downstream system on a recurring schedule.</span></span> <span data-ttu-id="370f3-109">本教程说明如何从 Microsoft Dynamics 365 Human Resources 导出所有工作人员记录，并将工作人员列表保存在 OneDrive for Business 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="370f3-109">This tutorial shows how to export all worker records from Microsoft Dynamics 365 Human Resources and save the list of workers in a OneDrive for Business folder.</span></span>

> [!TIP]
> <span data-ttu-id="370f3-110">本教程中导出的特定数据以及导出数据的目标位置仅是示例。</span><span class="sxs-lookup"><span data-stu-id="370f3-110">The specific data that is exported in this tutorial and the destination of the exported data are only examples.</span></span> <span data-ttu-id="370f3-111">您可以轻松地更改它们以满足您的业务需求。</span><span class="sxs-lookup"><span data-stu-id="370f3-111">You can easily change them to meet your business needs.</span></span>

## <a name="technologies-used"></a><span data-ttu-id="370f3-112">使用的技术</span><span class="sxs-lookup"><span data-stu-id="370f3-112">Technologies used</span></span>

<span data-ttu-id="370f3-113">本教程使用以下技术：</span><span class="sxs-lookup"><span data-stu-id="370f3-113">This tutorial uses the following technologies:</span></span>

- <span data-ttu-id="370f3-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – 将导出的工作人员的主数据源。</span><span class="sxs-lookup"><span data-stu-id="370f3-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – The master data source for workers that will be exported.</span></span>
- <span data-ttu-id="370f3-115">**[Azure 逻辑应用](https://azure.microsoft.com/services/logic-apps/)** – 提供重复导出的业务流程和计划的技术。</span><span class="sxs-lookup"><span data-stu-id="370f3-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – The technology that provides orchestration and scheduling of the recurring export.</span></span>

    - <span data-ttu-id="370f3-116">**[连接器](https://docs.microsoft.com/azure/connectors/apis-list)** – 用于将逻辑应用连接到所需终结点的技术。</span><span class="sxs-lookup"><span data-stu-id="370f3-116">**[Connectors](https://docs.microsoft.com/azure/connectors/apis-list)** – The technology that is used to connect the logic app to the required endpoints.</span></span>

        - <span data-ttu-id="370f3-117">[HTTP 与 Azure AD](https://docs.microsoft.com/connectors/webcontents/) 连接器</span><span class="sxs-lookup"><span data-stu-id="370f3-117">[HTTP with Azure AD](https://docs.microsoft.com/connectors/webcontents/) connector</span></span>
        - <span data-ttu-id="370f3-118">[OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) 连接器</span><span class="sxs-lookup"><span data-stu-id="370f3-118">[OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) connector</span></span>

- <span data-ttu-id="370f3-119">**[DMF 包 REST API](../dev-itpro/data-entities/data-management-api.md)** – 用于触发导出并监视其进度的技术。</span><span class="sxs-lookup"><span data-stu-id="370f3-119">**[DMF package REST API](../dev-itpro/data-entities/data-management-api.md)** – The technology that is used to trigger the export and monitor its progress.</span></span>
- <span data-ttu-id="370f3-120">**[OneDrive for Business](https://onedrive.live.com/about/business/)** – 导出的工作人员的目标位置。</span><span class="sxs-lookup"><span data-stu-id="370f3-120">**[OneDrive for Business](https://onedrive.live.com/about/business/)** – The destination for the exported workers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="370f3-121">先决条件</span><span class="sxs-lookup"><span data-stu-id="370f3-121">Prerequisites</span></span>

<span data-ttu-id="370f3-122">在开始本教程中的练习之前，您必须具有以下各项：</span><span class="sxs-lookup"><span data-stu-id="370f3-122">Before you begin the exercise in this tutorial, you must have the following items:</span></span>

- <span data-ttu-id="370f3-123">在环境中具有管理员级权限的 Human Resources 环境</span><span class="sxs-lookup"><span data-stu-id="370f3-123">A Human Resources environment that has admin-level permissions in the environment</span></span>
- <span data-ttu-id="370f3-124">用于托管逻辑应用的 [Azure 订阅](https://azure.microsoft.com/free/)</span><span class="sxs-lookup"><span data-stu-id="370f3-124">An [Azure subscription](https://azure.microsoft.com/free/) to host the logic app</span></span>

## <a name="the-exercise"></a><span data-ttu-id="370f3-125">练习</span><span class="sxs-lookup"><span data-stu-id="370f3-125">The exercise</span></span>

<span data-ttu-id="370f3-126">在本练习结束时，您将拥有一个逻辑应用，该应用已连接到您的 Human Resources 环境和 OneDrive for Business 帐户。</span><span class="sxs-lookup"><span data-stu-id="370f3-126">At the end of this exercise, you will have a logic app that is connected to your Human Resources environment and your OneDrive for Business account.</span></span> <span data-ttu-id="370f3-127">逻辑应用将从 Human Resources 导出数据包、等待导出完成、下载导出的数据包，然后将数据包保存在您指定的 OneDrive for Business 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="370f3-127">The logic app will export a data package from Human Resources, wait for the export to be completed, download the exported data package, and save the data package in the OneDrive for Business folder that you specified.</span></span>

<span data-ttu-id="370f3-128">完成的逻辑应用将类似于下图。</span><span class="sxs-lookup"><span data-stu-id="370f3-128">The completed logic app will resemble the following illustration.</span></span>

![逻辑应用概览](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a><span data-ttu-id="370f3-130">步骤 1：在 Human Resources 中创建数据导出项目</span><span class="sxs-lookup"><span data-stu-id="370f3-130">Step 1: Create a data export project in Human Resources</span></span>

<span data-ttu-id="370f3-131">在 Human Resources 中，创建一个导出工作人员的数据导出项目。</span><span class="sxs-lookup"><span data-stu-id="370f3-131">In Human Resources, create a data export project that exports workers.</span></span> <span data-ttu-id="370f3-132">将项目命名为**导出工作人员**，并确保将**生成数据包**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="370f3-132">Name the project **Export Workers**, and make sure that the **Generate data package** option is set to **Yes**.</span></span> <span data-ttu-id="370f3-133">将单个实体（**工作人员**）添加到项目，然后选择导出要使用的格式。</span><span class="sxs-lookup"><span data-stu-id="370f3-133">Add a single entity (**Worker**) to the project, and select the format to export in.</span></span> <span data-ttu-id="370f3-134">（本教程使用 Microsoft Excel 格式。）</span><span class="sxs-lookup"><span data-stu-id="370f3-134">(Microsoft Excel format is used in this tutorial.)</span></span>

![“导出工作人员”数据项目](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> <span data-ttu-id="370f3-136">记住数据导出项目的名称。</span><span class="sxs-lookup"><span data-stu-id="370f3-136">Remember the name of the data export project.</span></span> <span data-ttu-id="370f3-137">在下一步中创建逻辑应用时，将需要用到它。</span><span class="sxs-lookup"><span data-stu-id="370f3-137">You will need it when you create the logic app in the next step.</span></span>

### <a name="step-2-create-the-logic-app"></a><span data-ttu-id="370f3-138">步骤 2：创建逻辑应用</span><span class="sxs-lookup"><span data-stu-id="370f3-138">Step 2: Create the logic app</span></span>

<span data-ttu-id="370f3-139">大部分练习涉及创建逻辑应用。</span><span class="sxs-lookup"><span data-stu-id="370f3-139">The bulk of the exercise involves creating the logic app.</span></span>

1. <span data-ttu-id="370f3-140">在 Azure 门户中，创建一个逻辑应用。</span><span class="sxs-lookup"><span data-stu-id="370f3-140">In the Azure portal, create a logic app.</span></span>

    ![逻辑应用创建页面](media/integration-logic-app-creation-1.png)

2. <span data-ttu-id="370f3-142">在逻辑应用设计器中，从空白逻辑应用开始。</span><span class="sxs-lookup"><span data-stu-id="370f3-142">In the Logic Apps Designer, start with a blank logic app.</span></span>
3. <span data-ttu-id="370f3-143">添加[重复执行计划触发器](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence)，每 24 小时（或根据您选择的计划）运行一次逻辑应用。</span><span class="sxs-lookup"><span data-stu-id="370f3-143">Add a [Recurrence Schedule trigger](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) to run the logic app every 24 hours (or according to a schedule of your choice).</span></span>

    ![“重复执行”对话框](media/integration-logic-app-recurrence-step.png)

4. <span data-ttu-id="370f3-145">调用 [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API 计划数据包的导出。</span><span class="sxs-lookup"><span data-stu-id="370f3-145">Call the [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API to schedule the export of your data package.</span></span>

    1. <span data-ttu-id="370f3-146">从带有 Azure AD 连接器的 HTTP 使用**调用 HTTP 请求**操作。</span><span class="sxs-lookup"><span data-stu-id="370f3-146">Use the **Invoke an HTTP request** action from the HTTP with Azure AD connector.</span></span>

        - <span data-ttu-id="370f3-147">**基本资源 URL：** Human Resources 环境的 URL（不包括路径/命名空间信息）。</span><span class="sxs-lookup"><span data-stu-id="370f3-147">**Base Resource URL:** The URL of your Human Resources environment (Don't include path/namespace information.)</span></span>
        - <span data-ttu-id="370f3-148">**Azure AD 资源 URI：**`http://hr.talent.dynamics.com`</span><span class="sxs-lookup"><span data-stu-id="370f3-148">**Azure AD Resource URI:** `http://hr.talent.dynamics.com`</span></span>

        > [!NOTE]
        > <span data-ttu-id="370f3-149">Human Resources 服务尚未提供用于公开构成 DMF 包 REST API（如 **ExportToPackage**）的所有 API 的连接器。</span><span class="sxs-lookup"><span data-stu-id="370f3-149">The Human Resources service doesn't yet provide a connector that exposes all the APIs that make up the DMF package REST API, such as **ExportToPackage**.</span></span> <span data-ttu-id="370f3-150">您必须通过带有 Azure AD 连接器的 HTTP 使用原始 HTTPS 请求来调用 API。</span><span class="sxs-lookup"><span data-stu-id="370f3-150">Instead, you must call the APIs by using raw HTTPS requests through the HTTP with Azure AD connector.</span></span> <span data-ttu-id="370f3-151">此连接器使用 Azure Active Directory (Azure AD) 对 Human Resources 进行身份验证和授权。</span><span class="sxs-lookup"><span data-stu-id="370f3-151">This connector uses Azure Active Directory (Azure AD) for authentication and authorization to Human Resources.</span></span>

        ![带有 Azure AD 连接器的 HTTP](media/integration-logic-app-http-aad-connector-step.png)

    2. <span data-ttu-id="370f3-153">通过带有 Azure AD 连接器的 HTTP 登录到您的 Human Resources 环境。</span><span class="sxs-lookup"><span data-stu-id="370f3-153">Sign in to your Human Resources environment through the HTTP with Azure AD connector.</span></span>
    3. <span data-ttu-id="370f3-154">设置 HTTP **POST** 请求以调用 **ExportToPackage** DMF REST API。</span><span class="sxs-lookup"><span data-stu-id="370f3-154">Set up an HTTP **POST** request to call the **ExportToPackage** DMF REST API.</span></span>

        - <span data-ttu-id="370f3-155">**方法：** POST</span><span class="sxs-lookup"><span data-stu-id="370f3-155">**Method:** POST</span></span>
        - <span data-ttu-id="370f3-156">**请求的 URL：** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span><span class="sxs-lookup"><span data-stu-id="370f3-156">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span></span>
        - <span data-ttu-id="370f3-157">**请求的正文：**</span><span class="sxs-lookup"><span data-stu-id="370f3-157">**Body of the request:**</span></span>

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![调用 HTTP 请求操作](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > <span data-ttu-id="370f3-159">您可能需要重命名每个步骤，以使其比默认名称**调用 HTTP 请求**更有意义。</span><span class="sxs-lookup"><span data-stu-id="370f3-159">You might want to rename each step so that it's more meaningful than the default name, **Invoke an HTTP request**.</span></span> <span data-ttu-id="370f3-160">例如，您可以重命名此步骤 **ExportToPackage**。</span><span class="sxs-lookup"><span data-stu-id="370f3-160">For example, you can rename this step **ExportToPackage**.</span></span>

5. <span data-ttu-id="370f3-161">[初始化变量](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable)以存储 **ExportToPackage** 请求的执行状态。</span><span class="sxs-lookup"><span data-stu-id="370f3-161">[Initialize a variable](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) to store the execution status of the **ExportToPackage** request.</span></span>

    ![初始化变量操作](media/integration-logic-app-initialize-variable-step.png)

6. <span data-ttu-id="370f3-163">等待直到数据导出的执行状态为**已成功**。</span><span class="sxs-lookup"><span data-stu-id="370f3-163">Wait until the execution status of the data export is **Succeeded**.</span></span>

    1. <span data-ttu-id="370f3-164">添加一个一直重复到 **ExecutionStatus** 变量的值为**已成功**的 [Until 循环](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop)。</span><span class="sxs-lookup"><span data-stu-id="370f3-164">Add an [Until loop](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop) that repeats until the value of the **ExecutionStatus** variable is **Succeeded**.</span></span>
    2. <span data-ttu-id="370f3-165">添加等待五秒钟，然后才轮询导出的当前执行状态的**延迟**操作。</span><span class="sxs-lookup"><span data-stu-id="370f3-165">Add a **Delay** action that waits five seconds before it polls for the current execution status of the export.</span></span>

        ![Until 循环容器](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > <span data-ttu-id="370f3-167">将限制计数设置为 **15**，以最多等待 75 秒（15 次迭代 × 5 秒）完成导出。</span><span class="sxs-lookup"><span data-stu-id="370f3-167">Set the limit count to **15** to wait a maximum of 75 seconds (15 iterations × 5 seconds) for the export to be completed.</span></span> <span data-ttu-id="370f3-168">如果导出需要更多时间，请适当调整限制计数。</span><span class="sxs-lookup"><span data-stu-id="370f3-168">If your export takes more time, adjust the limit count as appropriate.</span></span>        

    3. <span data-ttu-id="370f3-169">添加**调用 HTTP 请求**操作以调用 [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API，并将 **ExecutionStatus** 变量设置为 **GetExecutionSummaryStatus** 响应的结果。</span><span class="sxs-lookup"><span data-stu-id="370f3-169">Add an **Invoke HTTP request** action to call the [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API, and set the **ExecutionStatus** variable to the result of the **GetExecutionSummaryStatus** response.</span></span>

        > <span data-ttu-id="370f3-170">此示例不进行错误检查。</span><span class="sxs-lookup"><span data-stu-id="370f3-170">This sample doesn't do error checking.</span></span> <span data-ttu-id="370f3-171">**GetExecutionSummaryStatus** API 可以返回不成功的终端状态（即，**已成功**以外的状态）。</span><span class="sxs-lookup"><span data-stu-id="370f3-171">The **GetExecutionSummaryStatus** API can return non-successful terminal states (that is, states other than **Succeeded**).</span></span> <span data-ttu-id="370f3-172">有关详细信息，请参阅 [API 文档](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus)。</span><span class="sxs-lookup"><span data-stu-id="370f3-172">For more information, see the [API documentation](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span></span>

        - <span data-ttu-id="370f3-173">**方法：** POST</span><span class="sxs-lookup"><span data-stu-id="370f3-173">**Method:** POST</span></span>
        - <span data-ttu-id="370f3-174">**请求的 URL：** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span><span class="sxs-lookup"><span data-stu-id="370f3-174">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span></span>
        - <span data-ttu-id="370f3-175">**请求的正文：** body('Invoke\_an\_HTTP\_request')?['value']</span><span class="sxs-lookup"><span data-stu-id="370f3-175">**Body of the request:** body('Invoke\_an\_HTTP\_request')?['value']</span></span>

            > [!NOTE]
            > <span data-ttu-id="370f3-176">您可能必须在代码视图或设计器的函数编辑器中输入**请求的正文**值。</span><span class="sxs-lookup"><span data-stu-id="370f3-176">You might have to enter the **Body of the request** value either in code view or in the function editor in the designer.</span></span>

        ![调用 HTTP 请求 2 操作](media/integration-logic-app-get-execution-status-step.png)

        ![设置变量操作](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > <span data-ttu-id="370f3-179">**设置变量**操作的值 (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) 与**调用 HTTP 请求 2** 正文值的值不同，即使设计器将以相同方式显示这些值。</span><span class="sxs-lookup"><span data-stu-id="370f3-179">The value for the **Set variable** action (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) will differ from the value for the **Invoke an HTTP request 2** body value, even though the designer will show the values in the same way.</span></span>

7. <span data-ttu-id="370f3-180">获取导出包的下载 URL。</span><span class="sxs-lookup"><span data-stu-id="370f3-180">Get the download URL of the exported package.</span></span>

    - <span data-ttu-id="370f3-181">添加**调用 HTTP 请求**操作以调用 [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API。</span><span class="sxs-lookup"><span data-stu-id="370f3-181">Add an **Invoke HTTP request** action to call the [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API.</span></span>

        - <span data-ttu-id="370f3-182">**方法：** POST</span><span class="sxs-lookup"><span data-stu-id="370f3-182">**Method:** POST</span></span>
        - <span data-ttu-id="370f3-183">**请求的 URL：** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span><span class="sxs-lookup"><span data-stu-id="370f3-183">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span></span>
        - <span data-ttu-id="370f3-184">**请求的正文：** {"executionId": body('GetExportedPackageURL')?['value']}</span><span class="sxs-lookup"><span data-stu-id="370f3-184">**Body of the request:** {"executionId": body('GetExportedPackageURL')?['value']}</span></span>

        ![GetExportedPackageURL 操作](media/integration-logic-app-get-exported-package-step.png)

8. <span data-ttu-id="370f3-186">下载导出的包。</span><span class="sxs-lookup"><span data-stu-id="370f3-186">Download the exported package.</span></span>

    - <span data-ttu-id="370f3-187">添加 HTTP **GET** 请求（内置的 [HTTP 连接器操作](https://docs.microsoft.com/azure/connectors/connectors-native-http)）以从上一步中返回的 URL 下载包。</span><span class="sxs-lookup"><span data-stu-id="370f3-187">Add an HTTP **GET** request (a built-in [HTTP connector action](https://docs.microsoft.com/azure/connectors/connectors-native-http)) to download the package from the URL that was returned in the previous step.</span></span>

        - <span data-ttu-id="370f3-188">**方法：** GET</span><span class="sxs-lookup"><span data-stu-id="370f3-188">**Method:** GET</span></span>
        - <span data-ttu-id="370f3-189">**URI：** body('Invoke\_an\_HTTP\_request\_3').value</span><span class="sxs-lookup"><span data-stu-id="370f3-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span></span>

            > [!NOTE]
            > <span data-ttu-id="370f3-190">您可能必须在代码视图或设计器的函数编辑器中输入 **URI** 值。</span><span class="sxs-lookup"><span data-stu-id="370f3-190">You might have to enter the **URI** value either in code view or in the function editor in the designer.</span></span>

        ![HTTP GET 操作](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > <span data-ttu-id="370f3-192">此请求不需要任何其他身份验证，因为 **GetExportedPackageUrl** API 返回的 URL 包含一个共享访问签名令牌，该令牌授予下载文件的访问权限。</span><span class="sxs-lookup"><span data-stu-id="370f3-192">This request doesn't require any additional authentication, because the URL that the **GetExportedPackageUrl** API returns includes a shared access signatures token that grants access to download the file.</span></span>

9. <span data-ttu-id="370f3-193">使用 [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) 连接器保存下载的包。</span><span class="sxs-lookup"><span data-stu-id="370f3-193">Save the downloaded package by using the [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) connector.</span></span>

    - <span data-ttu-id="370f3-194">添加 OneDrive for Business [创建文件](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file)操作。</span><span class="sxs-lookup"><span data-stu-id="370f3-194">Add a OneDrive for Business [Create File](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file) action.</span></span>
    - <span data-ttu-id="370f3-195">根据需要连接到您的 OneDrive for Business 帐户。</span><span class="sxs-lookup"><span data-stu-id="370f3-195">Connect to your OneDrive for Business account, as required.</span></span>

        - <span data-ttu-id="370f3-196">**文件夹路径：** 您选择的文件夹</span><span class="sxs-lookup"><span data-stu-id="370f3-196">**Folder Path:** A folder of your choice</span></span>
        - <span data-ttu-id="370f3-197">**文件名：** worker\_package.zip</span><span class="sxs-lookup"><span data-stu-id="370f3-197">**File Name:** worker\_package.zip</span></span>
        - <span data-ttu-id="370f3-198">**文件内容：** 上一步中的正文（动态内容）</span><span class="sxs-lookup"><span data-stu-id="370f3-198">**File Content:** The body from the previous step (dynamic content)</span></span>

        ![创建文件操作](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a><span data-ttu-id="370f3-200">步骤 3：测试逻辑应用</span><span class="sxs-lookup"><span data-stu-id="370f3-200">Step 3: Test the logic app</span></span>

<span data-ttu-id="370f3-201">要测试您的逻辑应用，在设计器中选择**运行**按钮。</span><span class="sxs-lookup"><span data-stu-id="370f3-201">To test your logic app, select the **Run** button in the designer.</span></span> <span data-ttu-id="370f3-202">您将看到逻辑应用的步骤开始运行。</span><span class="sxs-lookup"><span data-stu-id="370f3-202">You will see that the steps of the logic app start to run.</span></span> <span data-ttu-id="370f3-203">30 到 40 秒后，逻辑应用应会完成运行，您的 OneDrive for Business 文件夹应包括一个包含导出的工作人员的新包文件。</span><span class="sxs-lookup"><span data-stu-id="370f3-203">After 30 to 40 seconds, the logic app should finish running, and your OneDrive for Business folder should include a new package file that contains the exported workers.</span></span>

<span data-ttu-id="370f3-204">如果报告有任何步骤失败，在设计器中选择失败的步骤，然后检查步骤的**输入**和**输出**字段。</span><span class="sxs-lookup"><span data-stu-id="370f3-204">If a failure is reported for any step, select the failed step in the designer, and examine the **Inputs** and **Outputs** fields for it.</span></span> <span data-ttu-id="370f3-205">根据需要调试并调整步骤以更正错误。</span><span class="sxs-lookup"><span data-stu-id="370f3-205">Debug and adjust the step as required to correct the errors.</span></span>

<span data-ttu-id="370f3-206">下图显示了逻辑应用的所有步骤成功运行时逻辑应用设计器呈现的状态。</span><span class="sxs-lookup"><span data-stu-id="370f3-206">The following illustration shows what the Logic Apps Designer looks like when all the steps of the logic app run successfully.</span></span>

![成功的逻辑应用运行](media/integration-logic-app-successful-run.png)

## <a name="summary"></a><span data-ttu-id="370f3-208">摘要</span><span class="sxs-lookup"><span data-stu-id="370f3-208">Summary</span></span>

<span data-ttu-id="370f3-209">在本教程中，您学习了如何使用逻辑应用从 Human Resources 导出数据并将导出的数据保存到 OneDrive for Business 文件夹。</span><span class="sxs-lookup"><span data-stu-id="370f3-209">In this tutorial, you learned how to use a logic app to export data from Human Resources and save the exported data to a OneDrive for Business folder.</span></span> <span data-ttu-id="370f3-210">您可以根据需要修改本教程的步骤以适合您的业务需求。</span><span class="sxs-lookup"><span data-stu-id="370f3-210">You can modify the steps of this tutorial as required to suit your business needs.</span></span>


