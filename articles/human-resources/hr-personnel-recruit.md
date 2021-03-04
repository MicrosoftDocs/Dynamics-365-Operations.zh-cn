---
title: 招聘工作应聘者
description: 本主题显示如何在 Dynamics 365 Human Resources 中招聘应聘者。
author: andreabichsel
manager: tfehr
ms.date: 12/03/2020
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
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9a35abcb8a2f6aa8031c8d84a44c2a8ad93883ac
ms.sourcegitcommit: 0354ca7e566fbd2eb0aabdd40000d4ac5c44ea78
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/04/2020
ms.locfileid: "4669155"
---
# <a name="recruit-job-candidates"></a>招聘工作应聘者

[!include [banner](includes/preview-feature.md)]

Dynamics 365 Human Resources 帮助您管理招聘请求。 它还帮助您无缝地将工作应聘者转换为员工。 如果您的组织使用单独的招聘应用程序，您的招聘流程可能包括以下步骤：

- 在 Human Resources 中输入您的招聘请求。
- 从招聘应用程序接收 Human Resources 中的应聘者引荐。
- 在 Human Resources 中完成应聘者审批流程。

如果您不使用单独的招聘应用程序，还可以在 Human Resources 中手动管理应聘者。

>[!NOTE]
>如果您是管理员或开发人员，并且想要将 Human Resources 与第三方招聘应用程序集成，请参阅[配置 Common Data Service 集成](hr-admin-integration-common-data-service.md)和[配置 Common Data Service 虚拟实体](hr-admin-integration-common-data-service-virtual-entities.md)
>
> 您还可以在 [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics) 上找到招聘集成应用。
>
> 若要试用与 LinkedIn Talent Hub 集成的预览功能，请参阅[与 LinkedIn Talent Hub 集成](hr-admin-integration-linkedin.md)。

## <a name="enable-recruiting-requests"></a>启用招聘请求

如果要在 Human Resources 中提交招聘请求，您必须先在 **Human Resources 参数** 中启用该功能。

1. 在 **人事管理** 工作区中，选择 **链接**。

2. 在 **设置** 下，选择 **人力资源参数**。

3. 在 **常规** 选项卡上，在 **招聘** 下，将 **启用招聘请求** 设置为 **是**。

   ![启用招聘请求](./media/hr-recruit-0-enable-requests.png)

## <a name="add-a-recruiting-request-location"></a>添加招聘请求位置

如果您的组织有多个位置，可以添加它们，以便请求者可以选择新招聘的工作位置。 位置将包含在工作发布中。

1. 在搜索栏中，输入 **招聘请求位置**。

2. 选择 **新建**。

3. 在 **招聘请求位置** 字段中，输入位置名称。

   ![添加招聘请求位置](./media/hr-recruit-0a-add-location.png)

4. 在 **描述** 中，输入位置的描述。

5. 在 **位置** 下面，选择 **添加**。 如果显示 **新地址** 弹出窗口，输入位置的地址。

   ![请输入地址](./media/hr-recruit-0b-address.png)

6. 在 **联系人信息** 下，输入该位置的联系人的信息。

7. 选择 **保存**。

## <a name="add-a-recruiting-request"></a>添加招聘请求

经理可以在 Human Resources 中提交招聘请求。 如果您使用单独的招聘应用程序，完成这些步骤将发送一个招聘请求，并在该应用程序中开始招聘流程。 否则，完成此过程以开始您自己的内部招聘流程的工作流。

1. 选择 **员工自助服务**。

2. 选择 **我的团队** 选项卡。

3. 选择 **招聘请求**。

   ![开始招聘请求](./media/hr-recruit-1-request-to-recruit.png)

4. 填写 **描述**、**工作** 和 **预计开始日期** 字段。

   ![完成招聘请求](./media/hr-recruit-2-request-to-recruit.png)

5. 选择 **继续**。 将显示您的职位的招聘请求。

6. 在 **常规** 下，从 **招聘人员** 下拉菜单中选择招聘人员，然后从 **招聘请求位置** 中选择位置。

7. 在 **工作** 下，根据需要更改任何信息，然后选择 **通过工作创建详细信息**。

   ![通过作业创建详细信息](./media/hr-recruit-3-create-details-from-job.png)

   将使用您输入的工作的默认信息填充招聘请求的其余部分。

8. 在 **外部描述** 下，输入一个外部工作描述。

9. 在 **职位** 下，选择 **添加**，然后为此招聘请求选择一个职位。

   ![添加职位](./media/hr-recruit-4-select-position.png)

10. 在 **技能** 下，选择 **添加**，然后选择一项技能。

11. 在 **教育要求** 下，选择 **添加**，然后从 **教育** 和 **教育程度** 下拉菜单中选择值。

   ![添加教育要求](./media/hr-recruit-5-select-educational-requirements.png)

12. 在 **注释** 下，根据需要添加注释。

13. 在 **薪酬** 下，从 **级别** 下拉菜单中选择一个级别，然后根据需要调整 **低阈值**、**控制点** 和 **高阈值**。

14. 在完成招聘请求并且您准备好开始招聘流程时，在菜单栏中选择 **激活**。

   ![激活招聘请求](./media/hr-recruit-6-activate-recruit-request.png)

15. 选择 **保存**。

## <a name="view-and-edit-your-recruiting-requests"></a>查看和编辑您的招聘请求

如果您是经理，并且想要查看自己的请求：

1. 选择 **员工自助服务**。

2. 选择 **我的团队** 选项卡。

3. 在 **我的团队信息** 下，选择 **招聘请求** 选项卡。

   ![选择“招聘请求”选项卡](./media/hr-recruit-7-recruiting-requests.png)

4. 若要查看或编辑招聘请求，请在网格中选择它。

如果您是 HR 专业人员，并且想要查看所有招聘请求：

1. 选择 **人事管理**。

2. 选择 **招聘请求**。

   ![在人事管理中查看招聘请求](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. 若要查看或编辑招聘请求，请在网格中选择它。

## <a name="add-or-edit-a-candidate-profile"></a>添加或编辑应聘者个人资料

如果您的组织已与另一个应用程序集成以管理招聘请求，招聘请求将转发到该应用程序。 然后，招聘应用程序将应聘者信息发送回 Human Resources。 否则，您可以遵循自己的内部招聘流程并手动输入应聘者信息。

1. 选择 **人事管理**。

2. 选择 **链接**。

3. 在 **招聘** 下，选择 **应聘者**。

   ![查看应聘者](./media/hr-recruit-9-candidates.png)

4. 若要添加应聘者，选择 **新建**。 若要编辑现有应聘者，请从列表中选择应聘者，然后选择 **编辑**。 将显示应聘者个人资料。

5. 在 **应聘者汇总** 下，根据需要输入或编辑应聘者信息。

6. 在 **招聘请求** 下，选择将应聘者链接到的招聘请求。 然后，根据需要填写 **预计开始日期**、**雇用经理**、**职位** 和 **描述** 字段。

   ![链接到招聘请求](./media/hr-recruit-10-link-to-recruiting-request.png)

7. 填写要包含在应聘者记录中的以下区域中的所有信息：
   - **注释**
   - **工作经验**
   - **联系人信息**
   - **教育程度**
   - **技能**
   - **证书**
   - **筛选**

8. 选择 **保存**。

## <a name="hire-a-candidate"></a>雇用应聘者

当您准备雇用应聘者时，请遵循此过程将应聘者转换为员工。

1. 在应聘者窗体上，选择 **雇用**。

   ![雇用应聘者](./media/hr-recruit-11-hire.png)

2. 在 **雇用新工作人员** 窗体上，在 **详细信息** 下，填写所有字段。

   ![输入新雇用详细信息](./media/hr-recruit-12-hire-new-worker.png)

3. 在 **职位详细信息** 下，根据需要验证和更改信息。

4. 在 **入职核对清单** 下，为此员工选择相关的入职核对清单。

5. 选择 **继续** 以创建员工记录。

   >[!NOTE]
   >根据您组织的工作流，应聘者记录在成为员工记录之前，可能要完成其他审批步骤。

## <a name="decide-not-to-hire-a-candidate"></a>决定不雇用应聘者

如果您决定不雇用应聘者，请遵循此过程将其从审核流程中删除。 

1. 在应聘者窗体上，选择 **不雇用**。

   ![不雇用应聘者](./media/hr-recruit-13-do-not-hire.png)

2. 选择一个 **原因代码** 并包括任何注释。

3. 选择 **确定**。

## <a name="dismiss-a-candidate"></a>解雇应聘者

如果需要，您可以在雇用应聘者后将其解雇。 例如，应聘者可能拒绝您的聘约或在第一天不露面。

- 在应聘者窗体上，选择 **解雇应聘者**。

  ![消除应聘者](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a>请参阅

[配置 Common Data Service 虚拟实体](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[组织您的劳动力](hr-personnel-departments-jobs-positions.md)<br>
[设置工作组件](hr-personnel-jobs.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]