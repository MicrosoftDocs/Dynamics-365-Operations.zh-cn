---
title: 限制对个人信息的编辑
description: 限制员工在 Dynamics 365 Human Resources 中编辑联系人详细信息。
author: andreabichsel
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 727e0d4dbc5b330045bc9f91abab4d43b09e4382
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794797"
---
# <a name="restrict-editing-of-personal-information"></a>限制对个人信息的编辑

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

本主题介绍如何限制员工在 Dynamics 365 Human Resources 中编辑联系人详细信息。 您可能希望阻止员工编辑某些联系人详细信息，如他们的营业地点或电子邮件地址。

> [!NOTE]
> 要使用此功能，必须首先在“功能管理”中启用 **(预览)限制员工出于选择目的添加或编辑地址和联系信息**。 有关启用预览功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。<br><br>![启用预览功能](./media/hr-employee-self-service-restrict-enable.png)

## <a name="choose-the-information-an-employee-can-add-or-edit"></a>选择员工可以添加或编辑的信息

1. 在 Human Resources 中，选择 **人事管理**，选择 **链接**，然后选择 **人力资源参数**。

   ![转到“人力资源参数”](./media/hr-employee-self-service-human-resources-parameters.png)

2. 在 **人力资源参数** 页上，选择 **员工自助服务** 选项卡。

   ![选择“员工自助服务”](./media/hr-employee-self-service-tab.png)

3. 在 **员工自助服务** 选项卡上，取消选中 **地址和联系信息** 部分您不希望员工添加或编辑的所有信息。 在此示例中，我们取消选中了 **业务** 联系人信息。

   ![限制编辑业务联系人信息](./media/hr-employee-self-service-restrict-business.png)

4. 选择 **保存**。

   ![保存更改](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a>员工体验

限制员工添加或编辑联系人详细信息后，他们可以查看信息，但不能更改。

在此示例中，在限制员工编辑 **业务** 联系人详细信息时，他们仍然可以在员工自助服务中看到该信息：

![查看业务联系人详细信息](./media/hr-employee-self-service-restrict-view.png)

但是，当他们选择业务联系人详细信息时，**编辑地址** 窗格显示为只读，他们无法更改任何字段。

![业务联系人详细信息显示为只读](./media/hr-employee-self-service-restrict-read-only.png)

而且，如果他们选择 **添加** 来添加新地址，也无法从 **用途** 下拉框中选择 **业务**。

![员工无法添加业务地址](./media/hr-employee-self-service-restrict-add.png)

当员工在 **个人信息** 页选择 **联系人详细信息** 和添加新地址时，他们将获得相同的体验。 **用途** 下拉框仅显示他们可以添加的信息类型。 

![员工无法在“用途”下拉框中选择“业务”](./media/hr-employee-self-service-restrict-purpose.png)

**联系人详细信息** 现在在网格中显示 **用途**。

![在联系人详细信息网格中显示用途](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a>请参阅

[员工和经理自助服务概览](hr-employee-manager-self-service-overview.md)<br>
[配置 Human Resources 参数](hr-setup-parameters.md)<br>
[编辑个人信息](hr-employee-manager-self-service-edit-personal-information.md)