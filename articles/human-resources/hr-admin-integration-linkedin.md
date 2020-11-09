---
title: 与 LinkedIn Talent Hub 集成
description: 本主题介绍了如何设置 Microsoft Dynamics 365 Human Resources 与 LinkedIn Talent Hub 之间的集成。
author: jaredha
manager: tfehr
ms.date: 10/20/2020
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
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e82b79858060f31a6310cc5abdb2faf87db2d6c2
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/20/2020
ms.locfileid: "4056089"
---
# <a name="integrate-with-linkedin-talent-hub"></a>与 LinkedIn Talent Hub 集成

[!include [banner](includes/preview-feature.md)]

[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) 是申请人跟踪系统 (ATS) 平台。 通过此一体式平台，您可以找到、管理和雇用员工。 通过将 Microsoft Dynamics 365 Human Resources 与 LinkedIn Talent Hub 集成，您可以轻松地在 Human Resources 中为已被聘请担任某职位的申请人创建员工记录。

## <a name="setup"></a>设置

系统管理员必须完成设置任务才能与 LinkedIn Talent Hub 集成。 首先，在 Power Apps 环境中，您必须设置用户和安全角色，以授予 LinkedIn Talent Hub 适当的权限来将数据写入 Human Resources 中。

### <a name="link-your-environment-to-linkedin-talent-hub"></a>将您的环境链接到 LinkedIn Talent Hub

1. 打开 [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub)。

2. 在用户下拉菜单上，选择 **产品设置** 。

3. 在左侧导航窗格的 **高级** 部分中，选择 **集成** 。

4. 针对 Microsoft Dynamics 365 Human Resources 集成选择 **授权** 。

5. 在 **Dynamics 365 Human Resources** 页面上，选择 LinkedIn Talent Hub 要链接到的环境，然后选择 **链接** 。

    ![LinkedIn Talent Hub 入职](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > 您只能链接到用户帐户对 Human Resources 环境以及关联的 Power Apps 环境具有管理员访问权限的环境。 如果 Human Resources 链接页面上未列出任何环境，请确保已在租户上获得了 Human Resources 环境的许可，并且您以该身份登录到链接页面的用户对 Human Resources 环境和 Power Apps 环境具有管理员权限。

### <a name="create-a-power-apps-security-role"></a>创建 Power Apps 安全角色

1. 打开 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com)。

2. 在 **环境** 列表中，选择与您要将 LinkedIn Talent Hub 实例链接到的 Human Resources 环境相关联的环境。

3. 选择 **设置** 。

4. 展开 **用户 + 权限** 节点，然后选择 **安全角色** 。

5. 在 **安全角色** 页面的工具栏上，选择 **新建角色** 。

6. 在 **详细信息** 选项卡上，输入角色名称，例如 **LinkedIn Talent Hub HRIS 集成** 。

7. 在 **自定义** 选项卡上，为以下实体选择组织级别的 **读取** 权限：

    - 实体
    - 字段
    - 关系

8. 保存并关闭安全角色。

### <a name="create-a-power-apps-application-user"></a>创建 Power Apps 申请用户

必须为 LinkedIn Talent Hub 适配器创建申请用户，以授予该适配器的权限来将应聘者记录写入 Power Apps 环境中。

1. 打开 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com)。

2. 在 **环境** 列表中，选择与您要将 LinkedIn Talent Hub 实例链接到的 Human Resources 环境相关联的环境。

3. 选择 **设置** 。

4. 展开 **用户 + 权限** 节点，然后选择 **用户** 。

5. 选择 **管理 Dynamics 365 中的用户** 。

6. 使用列表上方的下拉菜单将视图从默认的 **已启用用户** 视图更改为 **申请用户** 。

    ![申请用户视图](./media/hr-admin-integration-power-apps-application-users.jpg)

7. 在工具栏上，选择 **新建** 。

8. 在 **新建用户** 页面上，执行以下步骤：

    1. 将 **用户类型** 字段的值更改为 **申请用户** 。
    2. 将 **用户名** 字段设置为 **Dynamics365 HR LinkedIn HRIS 集成** 。
    3. 将 **申请 ID** 字段设置为 **3a225c96-d62a-44ce-b3ec-bd4e8e9befef** 。
    4. 在 **名字** 、 **姓氏** 和 **主要电子邮件** 字段中输入任何值。
    5. 在工具栏上，选择 **保存 \& 关闭** 。

### <a name="assign-a-security-role-to-the-new-user"></a>为新用户分配安全角色

保存并关闭上一部分中的新申请用户后，您将返回到 **用户列表** 页面。

1. 在 **用户列表** 页面上，将视图更改为 **申请用户** 。

2. 选择在上一部分中创建的申请用户。

3. 在工具栏上，选择 **管理角色** 。

4. 选择您之前为集成创建的安全角色。

5. 选择 **确定** 。

### <a name="add-an-azure-active-directory-app-in-human-resources"></a>在 Human Resources 中添加 Azure Active Directory 应用

1. 在 Dynamics 365 Human Resources 中，打开 **Azure Active Directory 应用程序** 页面。
2. 将新记录添加到列表，然后设置以下字段：

    - **客户端 ID** ：输入 **3a225c96-d62a-44ce-b3ec-bd4e8e9befef** 。
    - **名称** ：输入您之前创建的 Power Apps 安全角色的名称，例如 **LinkedIn Talent Hub HRIS 集成** 。
    - **用户 ID** ：选择具有在“人员管理”中写入数据的权限的用户。

### <a name="create-the-entity-in-common-data-service"></a>在 Common Data Service 中创建实体

> [!IMPORTANT]
> 与 LinkedIn Talent Hub 的集成取决于适用于 Human Resources 的 Common Data Service 中的虚拟实体。 作为设置中此步骤的先决条件，必须配置虚拟实体。 有关如何配置虚拟实体的信息，请参阅[配置 Common Data Service 虚拟实体](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities)。

1. 在 Human Resources 中，打开 **Common Data Service (CDS) 集成** 页面。

2. 选择 **虚拟实体** 选项卡。

3. 按实体标签筛选实体列表以查找 **LinkedIn 导出的应聘者** 。

4. 选择实体，然后选择 **生成/刷新** 。

## <a name="exporting-candidate-records"></a>导出应聘者记录

完成设置后，招聘人员和 Human resources (HR) 专业人员可以使用 LinkedIn Talent Hub 中的 **导出到 HRIS** 功能，将雇用的应聘者记录从 LinkedIn Talent Hub 导出到 Human Resources。

### <a name="export-records-from-linkedin-talent-hub"></a>从 LinkedIn Talent Hub 导出记录

在应聘者完成招聘流程并被录用后，您可以将应聘者记录从 LinkedIn Talent Hub 导出到 Human Resources。

1. 在 LinkedIn Talent Hub 中，打开您为其雇用了新员工的项目。

2. 选择应聘者记录。

3. 选择 **更改阶段** ，然后选择 **雇用** 。

4. 在应聘者的省略号菜单 ( **...** ) 上，选择 **导出到 HRIS** 。

5. 在 **导出到 HRIS** 窗格中，输入必须导出的信息：

    - 在 **HRIS 提供商** 字段中，选择 **Microsoft Dynamics 365 Human Resources** 。
    - 在 **开始日期** 字段中，为新员工选择一个值。
    - 在 **职务** 字段中，输入新员工的工作的职务。
    - 在 **位置** 字段中，输入员工的所在地。
    - 输入或验证员工的电子邮件地址。

![LinkedIn Talent Hub 中的“导出到 HRIS”窗格](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a>在 Human Resources 中完成入职

从 LinkedIn Talent Hub 导出到 Human Resources 的应聘者记录将显示在 **人员管理** 页面的 **可雇用的应聘者** 部分中。

1. 在 Human Resources 中，打开 **人员管理** 页面。

2. 在 **可雇用的应聘者** 部分中，对于选定的应聘者选择 **雇用** 。

3. 在 **雇用新工作人员** 对话框中，查看记录，然后添加所有必需的信息。 您还可以选择已雇用的应聘者的职位编号。

输入所需的信息后，您可以继续执行创建员工记录和员工入职的标准流程。

以下详细信息将导入并包括在新员工记录上：

- 名
- 姓
- 雇用开始日期
- 电子邮件地址
- 电话号码

## <a name="see-also"></a>请参阅

[配置 Common Data Service 虚拟实体](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[什么是 Common Data Service？](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)
