---
title: 编辑 Dynamics 365 Talent - Onboard 中的入职指南和模板
description: 本主题说明如何将活动和其他信息添加到 Microsoft Dynamics 365 Talent - Onboard 中的入职指南和模板。
author: andreabichsel
manager: ''
ms.date: 06/19/2019
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
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 24369a878e95076783d670894236d56dca18e765
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812871"
---
# <a name="edit-onboarding-guides-and-templates-in-dynamics-365-talent---onboard"></a>编辑 Dynamics 365 Talent - Onboard 中的入职指南和模板

[!include [banner](includes/banner.md)]

在 Microsoft Dynamics 365 Talent: Onboard 中创建入职指南或模板后，您必须添加介绍、活动、联系人和资源。 Onboard 允许您在入职指南中包含丰富的内容，包括：

- YouTube 视频
- Microsoft Sway 演示文稿
- Microsoft PowerApps 应用
- Microsoft Stream 视频
- Microsoft Forms 表单
- 包含 Web 内容的 iframe

## <a name="edit-introductions-or-activities-imported-from-a-template"></a>编辑从模板导入的介绍或活动

如果您从模板创建入职指南，或者将活动从一个模板导入另一个模板，您会注意到导入活动上有一个**锁定**按钮。 这些称为*托管活动*。

[![托管活动](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)

选择托管活动时，您可以在活动顶部看到源模板。

[![托管活动源](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)

如果您在模板中编辑活动，Onboard 会将更改推送到基于该模板的所有模板和未发送的指南。 如果您根据编辑的模板选择未发送的指南，然后选择指南中的**活动**选项卡，您将看到指南已更改的通知。 要消除通知，请选择**确定**。 

[![更改通知](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)

您会在更新的活动旁边看到一个黑点。

[![已更改活动](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)

除了在活动的右侧部分添加受托人、到期日期或其他信息外，您无法编辑原始模板之外的托管活动。

如果要编辑托管活动，或者如果您不希望活动从其来源模板接收更新，请选择该活动的**锁定**按钮。 **锁定**按钮将消失。 该活动将不再由原始模板管理，并且将不再从该模板接收更新。 您对活动所做的更新不会影响原始模板。

如果您从指南中删除活动并从该指南的模板中推送更改，则该活动将在指南中保持删除状态。

> [!NOTE]
> 联系人和资源不受模板管理。 此外，还不管理部分，因此，如果您在模板中添加或编辑部分，则不会将更改推送到使用该模板的任何指南或模板。
> 
> 如果向模板添加新活动，则会基于该模板将新活动推送到指南和模板，并在顶部显示新活动。

## <a name="import-activities-from-another-template"></a>从另一个模板导入活动

您可以将一个或多个模板中的活动导入指南或模板。

1. 选择要编辑的指南或模板。

2. 选择**活动**选项卡。

3. 在右侧部分中选择**导入**选项卡。

   [![导入活动](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)

4. 要在浏览器的新选项卡中预览任务，请选择任意模板上的**在新选项卡中打开**按钮。

   [![导入活动](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)

5. 将所需模板拖放到指南模板中要显示活动的位置。 继续编辑指南或模板。

导入的活动将包含**锁定**按钮，表示这些活动由您从中导入活动的模板管理。 当您对导入的模板进行更改时，这些活动将在您将其导入的模板中更新。 但是，更改不会自动推送到从向其导入的模板创建的任何指南。

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a>将更改从模板推送到其他模板或指南

如果编辑包含其他模板或指南使用的活动的模板，如果希望更改出现在其他模板或指南中，则必须推送更改。

如果您不确定模板的活动是否在其他模板或指南中使用，请选择**使用位置**选项卡查看这些活动的显示位置。

   [![查看指南和模板活动的使用位置](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)

推送更改：

1. 选择**保存**按钮保存更改。 如果不这样做，系统将提示您在下一步中保存更改。

2. 选择**推送这些更改**。

   
## <a name="add-or-edit-an-introduction"></a>添加或编辑介绍

1. 在**介绍**选项卡上，输入指南的标题和开场白消息。 要使用示例文本，请选择**使用此消息**。

    [![Onboard 模板中的“介绍”选项卡](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)

2. 使用格式按钮根据需要调出文本，或添加图像或链接。
3. 选择**保存**保存您的工作。

## <a name="add-or-edit-activities"></a>添加或编辑活动

1. 在**活动**选项卡上，将项目从右侧拖动到编辑区域。
2. 要将指南安排到各个部分，请将**新部分**项目拖动到编辑区域，然后输入部分的名称和可选描述。

    ![[将新部分添加到入职指南或模板](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. 要为新雇员添加要完成的活动，请将**新活动**项目拖到编辑区域，然后输入活动的名称和描述。

    ![[将新活动添加到入职指南或模板](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. 为您的入职指南添加丰富的内容：

    - 要添加 YouTube 视频，请将 **YouTube** 项目拖至编辑区域，输入活动的名称和描述，然后输入 YouTube 视频的 URL。
    - 要添加 Sway 演示文稿或新闻稿，请将 **Sway** 项目拖到编辑区域，输入活动的名称和描述，然后输入 Sway 演示文稿或新闻稿的嵌入 URL。
    - 要添加 Microsoft Power Apps 应用，请将 **Power Apps** 项目拖动到编辑区域，输入活动的名称和描述，然后选择 Power Apps 应用或输入 Power Apps 应用 ID。
    - 要添加 Microsoft Stream 视频，请将 **Microsoft Stream** 项目拖到编辑区域，输入活动的名称和描述，然后输入 Microsoft Stream 视频的 URL。
    - 要添加 Microsoft Forms 表单，请将 **Microsoft Forms** 项目拖到编辑区域，输入活动的名称和描述，输入 Microsoft Forms 表单的 URL，并指定屏幕区域的大小。
    - 要添加包含 Web 内容的 iframe，请将 **Web 内容(iframe)** 项目拖到编辑区域，输入活动的名称和描述，输入 Web 内容的 URL，并指定 屏幕区域的大小。

    ![[将丰富内容添加到入职指南或模板](./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. 可选：在每个活动右侧的区域中，将活动分配给特定的人员或角色、添加到期日期和联系人、分配类别颜色。 将活动分配给人员或角色时，会为每个人创建一个任务。 此任务显示在 Onboard 上的**任务**菜单中。

    [![在入职指南或模板中分配活动](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)

3. 选择**保存**保存您的工作。

要删除活动或部分，请选择活动或部分右上角的**删除**按钮（垃圾桶符号）。

要重新排列活动和部分，请将它们拖动到新位置。

## <a name="add-or-edit-contacts"></a>添加或编辑联系人

您可以添加可以从第一天起帮助您的新雇员取得成功的联系人。 这些联系人可以是招聘人员、团队成员、入职联系人、指导者、管理员和 IT 支持人员。

1. 在**联系人**选项卡上，选择**新联系人**。
2. 在**添加团队成员**对话框中，输入联系人的姓名或电子邮件地址，输入说明联系人如何帮助新雇员的简短说明，然后选择**添加**。 

    ![[将联系人添加到入职指南或模板](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    或者，您可以在**建议**下选择一个或多个联系人。

3. 选择**保存**保存您的工作。

要删除联系人，请选择联系人右侧的**删除**按钮（垃圾桶符号）。

要编辑联系人，请选择联系人右侧的**编辑**按钮（铅笔符号）。

## <a name="add-or-edit-resources"></a>添加或编辑资源

您可以将有用的文件、地图和链接添加到入职指南的**资源**部分。

1. 在**资源**选项卡上，选择**新资源**。
2. 按以下步骤之一：

    - 要添加文件，请选择**文件**选项卡，然后将文件拖到指定区域。 （或者，单击该区域中的任意位置以浏览计算机上的文件，或选择**浏览 OneDrive**。）输入文件的名称，然后选择**添加**。
    - 要添加链接，请选择**链接**选项卡，输入链接的名称和地址，然后选择**添加**。
    - 要添加地图，请选择**地图**选项卡，输入地图的名称和地址，然后选择**添加**。 Onboard 将包含您指定的地址的地图。

    ![[将资源添加到入职指南或模板](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. 选择**保存**保存您的工作。

要删除资源，请选择资源右侧的**删除**按钮（垃圾桶符号）。

要编辑联系人，请选择资源右侧的**编辑**按钮（铅笔符号）。

## <a name="next-steps"></a>后续步骤

- [与其他参与者共享内容](./onboard-share-template.md)
- [查看任务和入职员工的状态](./onboard-view-status.md)
- [在 Onboard 中创建招聘团队](./onboard-create-team.md)

### <a name="see-also"></a>请参阅

- [试用或购买 Onboard 应用](https://dynamics.microsoft.com/talent/onboard/)
- [Dynamics 365 Talent 新增功能或更改](./whats-new.md)
- [发布计划](https://docs.microsoft.com/business-applications-release-notes/index)
- [获取 Microsoft Dynamics 365 Talent 支持](./talent-support.md)
