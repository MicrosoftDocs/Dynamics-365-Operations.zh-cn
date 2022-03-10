---
title: 创建定期数据导出应用
description: 本主题介绍如何创建按重复执行的计划从 Microsoft Dynamics 365 Human Resources 导出数据的 Microsoft Azure 逻辑应用。
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 368eee6bb182f363f47467a5c5ad8208a57db7ec
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069774"
---
# <a name="create-a-recurring-data-export-app"></a>创建定期数据导出应用


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍如何创建按重复执行的计划从 Microsoft Dynamics 365 Human Resources 导出数据的 Microsoft Azure 逻辑应用。 本教程利用 Human Resources 的 DMF 包 REST 应用程序编程接口 (API) 来导出数据。 导出数据后，逻辑应用将导出的数据包保存到 Microsoft OneDrive for Business 文件夹。

## <a name="business-scenario"></a>业务方案

在 Microsoft Dynamics 365 集成的一种典型业务方案中，必须按重复执行的计划将数据导出到下游系统。 本教程说明如何从 Microsoft Dynamics 365 Human Resources 导出所有工作人员记录，并将工作人员列表保存在 OneDrive for Business 文件夹中。

> [!TIP]
> 本教程中导出的特定数据以及导出数据的目标位置仅是示例。 您可以轻松地更改它们以满足您的业务需求。

## <a name="technologies-used"></a>使用的技术

本教程使用以下技术：

- **[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – 将导出的工作人员的主数据源。
- **[Azure 逻辑应用](https://azure.microsoft.com/services/logic-apps/)** – 提供重复导出的业务流程和计划的技术。

    - **[连接器](/azure/connectors/apis-list)** – 用于将逻辑应用连接到所需终结点的技术。

        - [HTTP 与 Azure AD](/connectors/webcontents/) 连接器
        - [OneDrive for Business](/azure/connectors/connectors-create-api-onedriveforbusiness) 连接器

- **[DMF 包 REST API](../fin-ops-core/dev-itpro/data-entities/data-management-api.md)** – 用于触发导出并监视其进度的技术。
- **[OneDrive for Business](https://onedrive.live.com/about/business/)** – 导出的工作人员的目标位置。

## <a name="prerequisites"></a>先决条件

在开始本教程中的练习之前，您必须具有以下各项：

- 在环境中具有管理员级权限的 Human Resources 环境
- 用于托管逻辑应用的 [Azure 订阅](https://azure.microsoft.com/free/)

## <a name="the-exercise"></a>练习

在本练习结束时，您将拥有一个逻辑应用，该应用已连接到您的 Human Resources 环境和 OneDrive for Business 帐户。 逻辑应用将从 Human Resources 导出数据包、等待导出完成、下载导出的数据包，然后将数据包保存在您指定的 OneDrive for Business 文件夹中。

完成的逻辑应用将类似于下图。

![逻辑应用概览。](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a>步骤 1：在 Human Resources 中创建数据导出项目

在 Human Resources 中，创建一个导出工作人员的数据导出项目。 将项目命名为 **导出工作人员**，并确保将 **生成数据包** 选项设置为 **是**。 将单个实体（**工作人员**）添加到项目，然后选择导出要使用的格式。 （本教程使用 Microsoft Excel 格式。）

![导出工作人员数据项目。](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> 记住数据导出项目的名称。 在下一步中创建逻辑应用时，将需要用到它。

### <a name="step-2-create-the-logic-app"></a>步骤 2：创建逻辑应用

大部分练习涉及创建逻辑应用。

1. 在 Azure 门户中，创建一个逻辑应用。

    ![逻辑应用创建页面。](media/integration-logic-app-creation-1.png)

2. 在逻辑应用设计器中，从空白逻辑应用开始。
3. 添加[重复执行计划触发器](/azure/connectors/connectors-native-recurrence)，每 24 小时（或根据您选择的计划）运行一次逻辑应用。

    ![重复执行对话框。](media/integration-logic-app-recurrence-step.png)

4. 调用 [ExportToPackage](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API 计划数据包的导出。

    1. 从带有 Azure AD 连接器的 HTTP 使用 **调用 HTTP 请求** 操作。

        - **基本资源 URL：** Human Resources 环境的 URL（不包括路径/命名空间信息）。
        - **Azure AD 资源 URI：**`http://hr.talent.dynamics.com`

        > [!NOTE]
        > Human Resources 服务尚未提供用于公开构成 DMF 包 REST API（如 **ExportToPackage**）的所有 API 的连接器。 您必须通过带有 Azure AD 连接器的 HTTP 使用原始 HTTPS 请求来调用 API。 此连接器使用 Azure Active Directory (Azure AD) 对 Human Resources 进行身份验证和授权。

        ![带有 Azure AD 连接器的 HTTP。](media/integration-logic-app-http-aad-connector-step.png)

    2. 通过带有 Azure AD 连接器的 HTTP 登录到您的 Human Resources 环境。
    3. 设置 HTTP **POST** 请求以调用 **ExportToPackage** DMF REST API。

        - **方法：** POST
        - **请求的 URL：** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage
        - **请求的正文：**

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![调用 HTTP 请求操作。](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > 您可能需要重命名每个步骤，以使其比默认名称 **调用 HTTP 请求** 更有意义。 例如，您可以重命名此步骤 **ExportToPackage**。

5. [初始化变量](/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable)以存储 **ExportToPackage** 请求的执行状态。

    ![初始化变量操作。](media/integration-logic-app-initialize-variable-step.png)

6. 等待直到数据导出的执行状态为 **已成功**。

    1. 添加一个一直重复到 **ExecutionStatus** 变量的值为 **已成功** 的 [Until 循环](/azure/logic-apps/logic-apps-control-flow-loops#until-loop)。
    2. 添加等待五秒钟，然后才轮询导出的当前执行状态的 **延迟** 操作。

        ![Until 循环容器。](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > 将限制计数设置为 **15**，以最多等待 75 秒（15 次迭代 × 5 秒）完成导出。 如果导出需要更多时间，请适当调整限制计数。        

    3. 添加 **调用 HTTP 请求** 操作以调用 [GetExecutionSummaryStatus](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API，并将 **ExecutionStatus** 变量设置为 **GetExecutionSummaryStatus** 响应的结果。

        > 此示例不进行错误检查。 **GetExecutionSummaryStatus** API 可以返回不成功的终端状态（即，**已成功** 以外的状态）。 有关详细信息，请参阅 [API 文档](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus)。

        - **方法：** POST
        - **请求的 URL：** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus
        - **请求的正文：** body('Invoke\_an\_HTTP\_request')?['value']

            > [!NOTE]
            > 您可能必须在代码视图或设计器的函数编辑器中输入 **请求的正文** 值。

        ![调用 HTTP 请求 2 操作。](media/integration-logic-app-get-execution-status-step.png)

        ![设置变量操作。](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > **设置变量** 操作的值 (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) 与 **调用 HTTP 请求 2** 正文值的值不同，即使设计器将以相同方式显示这些值。

7. 获取导出包的下载 URL。

    - 添加 **调用 HTTP 请求** 操作以调用 [GetExportedPackageUrl](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API。

        - **方法：** POST
        - **请求的 URL：** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl
        - **请求的正文：**{"executionId": body('GetExportedPackageURL')?['value']}

        ![GetExportedPackageURL 操作。](media/integration-logic-app-get-exported-package-step.png)

8. 下载导出的包。

    - 添加 HTTP **GET** 请求（内置的 [HTTP 连接器操作](/azure/connectors/connectors-native-http)）以从上一步中返回的 URL 下载包。

        - **方法：** GET
        - **URI：** body('Invoke\_an\_HTTP\_request\_3').value

            > [!NOTE]
            > 您可能必须在代码视图或设计器的函数编辑器中输入 **URI** 值。

        ![HTTP GET 操作。](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > 此请求不需要任何其他身份验证，因为 **GetExportedPackageUrl** API 返回的 URL 包含一个共享访问签名令牌，该令牌授予下载文件的访问权限。

9. 使用 [OneDrive for Business](/azure/connectors/connectors-create-api-onedriveforbusiness) 连接器保存下载的包。

    - 添加 OneDrive for Business [创建文件](/connectors/onedriveforbusinessconnector/#create-file)操作。
    - 根据需要连接到您的 OneDrive for Business 帐户。

        - **文件夹路径：** 您选择的文件夹
        - **文件名：** worker\_package.zip
        - **文件内容：** 上一步中的正文（动态内容）

        ![创建文件操作。](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a>步骤 3：测试逻辑应用

要测试您的逻辑应用，在设计器中选择 **运行** 按钮。 您将看到逻辑应用的步骤开始运行。 30 到 40 秒后，逻辑应用应会完成运行，您的 OneDrive for Business 文件夹应包括一个包含导出的工作人员的新包文件。

如果报告有任何步骤失败，在设计器中选择失败的步骤，然后检查步骤的 **输入** 和 **输出** 字段。 根据需要调试并调整步骤以更正错误。

下图显示了逻辑应用的所有步骤成功运行时逻辑应用设计器呈现的状态。

![成功的逻辑应用运行。](media/integration-logic-app-successful-run.png)

## <a name="summary"></a>摘要

在本教程中，您学习了如何使用逻辑应用从 Human Resources 导出数据并将导出的数据保存到 OneDrive for Business 文件夹。 您可以根据需要修改本教程的步骤以适合您的业务需求。




[!INCLUDE[footer-include](../includes/footer-banner.md)]
