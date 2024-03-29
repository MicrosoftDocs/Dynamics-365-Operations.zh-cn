---
title: 编辑个人信息
description: 本文介绍如何在员工和经理自助服务中编辑个人信息。
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d7e78873d0995334ac80ac22e8058b7fe0bc31ac
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686100"
---
# <a name="edit-personal-information"></a>编辑个人信息


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

您可以在 **员工自助服务** 工作区的 Dynamics 365 Human Resources 中编辑您的个人信息。

您可以编辑的个人信息包括：

- 地址
- 联系人详细信息
- 个人联系人
- 标识号
- 付款方式
- Human Resources 中使用的图像

>[!NOTE]
>您可能无法编辑某些类型的个人信息，如业务联系人详细信息。 有关详细信息，请参阅[限制对个人信息的编辑](hr-employee-self-service-restrict-editing.md)。

在 **全局通讯簿参数** 页面中设置的参数决定哪些角色可以查看您的个人信息。

1. 在 Human Resources 中，选择 **员工自助服务**。

2. 选择 **编辑个人详细信息**。

3. 要更改您的地址，请选择 **地址** 选项卡。您所做的更改将显示在 **人事管理** 工作区中，以提醒人力资源。

    - 要添加新地址，请选择 **添加**。
    - 要编辑现有地址，请选择该地址，然后选择 **编辑**。
    - 要查看地图，请选择 **地图**。
    - 要添加或删除联系人，请选择 **更多选择**，然后选择 **高级**。 在 **联系信息** 下，选择 **添加** 或 **删除**，然后根据需要编辑字段。
    - 要设置时区和位置，请选择 **更多选择**，然后选择 **高级**。 在 **常规** 下，根据需要编辑字段。

4. 要更改您的联系人详细信息，请选择 **联系人详细信息** 选项卡。您可以提供不同类型的联系信息，包括电话、电子邮件和社交媒体链接。 您可以将联系人详细信息设置为主要，但只能将每种类型的一种联系人详细信息设置为主要。

    - 若要添加新的联系信息，请选择 **添加**。 根据需要编辑字段。
    - 要编辑现有联系信息，请选择该项目，然后选择 **编辑**。 根据需要编辑字段。
    - 要将联系人详细信息设置为非公开，请选择该项目，选择 **高级**，然后将 **非公开** 切换设置为 **是**。 选择 **确定**。
      >[!NOTE]
      >如果您的管理员在您的环境中启用了 **(预览)限制员工出于选择目的添加或编辑地址和联系信息** 功能，**高级** 按钮将不可用。 有关详细信息，请参阅[限制对个人信息的编辑](hr-employee-self-service-restrict-editing.md)。
  
5. 要更改您的个人联系人，请选择 **个人联系人** 选项卡。您可以指定紧急联系人、受益人和依赖方。 联系人可以是个人或组织。 **福利管理** 功能使用个人联系信息。 有关详细信息，请参阅[配置个人联系人资格选项](hr-benefits-setup-contact-eligibility-options.md)。

6. 要更改您的身份证明编号，如社会保险号，请选择 **身份证明编号** 选项卡。如果您的组织设置了审核工作流，更改可能要经过审核流程。

    - 要添加身份证明编号，请选择 **新建**。 根据需要填写字段，然后选择 **保存**。
    - 要编辑编号，请选择 **编辑**。 根据需要编辑字段，然后选择 **保存**。

7. 要更改付款方式，请选择 **我的付款信息** 选项卡。此选项卡仅在 **人力资源参数** 页面中启用了付款方式时可用。 人力资源可以启用 **银行汇票**、**现金**、**支票**、**电子付款** 或 **其他**。 人力资源还可以禁用电子付款验证（用于美国工资单）以及银行账户和银行代号验证。

8. 要更改显示在 Human Resources 中的个人资料的图像，请选择 **图像** 选项卡。根据组织的设置，可能会传送图像以进行审核。

    - 要上载图像，请选择 **上载新图像**。
    - 要删除图像，请选择该图像，然后选择 **删除**。



[!INCLUDE[footer-include](../includes/footer-banner.md)]
