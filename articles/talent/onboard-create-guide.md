---
title: 使用 Dynamics 365 Talent - Onboard 创建和发送入职指南
description: 本主题说明如何使用 Microsoft Dynamics 365 Talent - Onboard 应用为新雇员创建入职指南。 此任务是人力资本管理 (HCM) 雇佣退休战略的重要的第一步。
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 3c465c667cbb8a66f301637ca620429b0ddc11c6
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550335"
---
# <a name="create-and-send-an-onboarding-guide-by-using-dynamics-365-talent---onboard"></a>使用 Dynamics 365 Talent - Onboard 创建和发送入职指南

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talent: Onboard 允许您从自己创建的模板、库中可用的模板或从头开始创建入职指南。

在您创建入职指南后，您可以将其发送给新雇员。 或者，您可以将其发送给您从 Onboard 应用下载的 Microsoft Excel 文件中指定的多个新雇员。

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-a-single-new-hire"></a>从模板创建入职指南并将其发送给单个新雇员

1. 在左侧菜单中，选择**模板**。
2. 在**我的模板**下，选择您要设置为新雇员入职指南的模板。
3. 根据需要编辑模板。 编辑时一定要保存您的工作。
4. 编辑完模板后，选择**创建指南**。

    [![从模板创建入职指南](./media/onboard-create-guide.png)](./media/onboard-create-guide.png)

5. 在**创建指南**窗口，在**您的入职对象**下，输入新雇员的姓名或电子邮件地址。 如果新雇员尚未在系统中，选择**立即添加**，然后输入员工的信息。

    ![[输入入职指南的信息](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

6. 在**何时入职**下，选择一个开始日期。
7. 如果应在特定日期自动将入职指南发送给新雇员，请确保**安排自动发送日期**选项已打开，然后选择自动发送日期。 要立即发送指南，请关闭**安排自动发送日期**选项。
8. 选择**完成**。
9. 完成编辑入职指南后，在右上角选择**发送**。 然后按照以下步骤之一操作：

    - 要向新雇员发送指向入职指南的链接，请选择**复制链接**，然后选择**复制**。
    - 要在发送之前自定义入职指南的电子邮件，请选择**发送前自定义电子邮件**，选择**下一步**，根据需要自定义电子邮件，然后选择**发送**。
    - 要在不自定义的情况下发送电子邮件，请选择**下一步**，然后选择**发送**。

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-multiple-new-hires"></a>从模板创建入职指南并将其发送给多个新雇员

Onboard 允许您同时向多个新雇员发送入职指南。

1. 在左侧菜单中，选择**模板**。
2. 在**我的模板**下，选择您要设置为新雇员入职指南的模板。
3. 根据需要编辑模板。 编辑时一定要保存您的工作。
4. 编辑完模板后，选择**创建指南**。
5. 在**创建指南**窗口中，选择**需要一次入职多人**。

    [![为多个新雇员创建入职指南](./media/onboard-send-guide-multiple-people.png)](./media/onboard-send-guide-multiple-people.png)

6. 选择**新雇员模板**。
7. 下载 .xlsx 文件后，选择**打开**，在 Excel 工作簿中输入员工信息，然后保存工作簿。

    [![下载 Excel 模板以将入职指南发送给多个新雇员](./media/onboard-send-guide-download-spreadsheet.png)](./media/onboard-send-guide-download-spreadsheet.png)

    > [!NOTE]
    > 您必须在 Excel 中选择**启用编辑**，然后才能够编辑工作簿。
    > 
    > [![启用编辑](./media/onboard-send-guide-enable-editing.png)](./media/onboard-send-guide-enable-editing.png)

8. 将 Excel 工作簿拖动到**创建多个指南**窗口中的指定区域，或单击该区域的任意位置来浏览计算机上的文件。

    [![拖动已编辑的工作簿](./media/onboard-send-guide-drag-spreadsheet.png)](./media/onboard-send-guide-drag-spreadsheet.png)

9. 完成编辑入职指南后，在右上角选择**发送**。 然后按照以下步骤之一操作：

    - 要向新雇员发送指向入职指南的链接，请选择**复制链接**，然后选择**复制**。
    - 要在发送之前自定义入职指南的电子邮件，请选择**发送前自定义电子邮件**，选择**下一步**，根据需要自定义电子邮件，然后选择**发送**。
    - 要在不自定义的情况下发送电子邮件，请选择**下一步**，然后选择**发送**。

## <a name="create-a-guide-without-using-a-template"></a>不使用模板创建指南

您不必总是从模板创建指南。 如果您愿意，可以从头开始创建指南。

1. 在左侧菜单中，选择**指南**，然后选择**添加**按钮（加号 \[**+**\]）。
2. 在**创建指南**窗口，在**您的入职对象**下，输入新雇员的姓名或电子邮件地址。 如果新雇员尚未在系统中，选择**立即添加**，然后输入员工的信息。

    ![[输入入职指南的信息](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

3. 在**何时入职**下，选择一个开始日期。
4. 如果应在特定日期自动将入职指南发送给新雇员，请确保**安排自动发送日期**选项已打开，然后选择自动发送日期。 要立即发送指南，请关闭**安排自动发送日期**选项。
5. 选择**完成**。

## <a name="save-a-guide-as-a-template"></a>将指南另存为模板

您可以将入职指南另存为模板。 这样，您可以在以后必须创建更多入职指南时节省时间。

1. 在左侧菜单中，选择**指南**。
2. 选择要从其创建模板的指南**更多**按钮（省略号 \[**...**\]），然后选择**另存为模板**。

    ![[将入职指南另存为模板](./media/onboard-save-guide-as-template.png)](./media/onboard-save-guide-as-template.png)

3. 在**另存为新模板**窗口，输入新模板的名称，然后选择**保存**。

## <a name="next-steps"></a>后续步骤

- [编辑入职指南和模板](./onboard-edit-guides-templates.md)
- [与其他参与者共享内容](./onboard-share-template.md)
- [查看任务和入职员工的状态](./onboard-view-status.md)
- [在 Onboard 中创建招聘团队](./onboard-create-team.md)

### <a name="see-also"></a>请参阅

- [试用或购买 Onboard 应用](https://dynamics.microsoft.com/talent/onboard/)
- [新增功能](./whats-new.md)
- [版本说明](https://docs.microsoft.com/business-applications-release-notes/index)
- [获取支持](./talent-support.md)
