---
title: "Dynamics 365 for Talent Core HR（2018 年 10 月 31 日）中的新增功能或更改的功能"
description: "此主题介绍了 Microsoft Dynamics 365 for Talent Core HR 中的新功能和更改的功能。"
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c5acd09e25ecd5fefa637342f83d0ee0f1891402
ms.contentlocale: zh-cn
ms.lasthandoff: 11/01/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-31-2018"></a>Dynamics 365 for Talent Core HR（2018 年 10 月 31 日）中的新增功能或更改的功能

[!include [banner](includes/banner.md)]

**内部版本 8.1.2031**

此主题介绍了 Core HR 中的新增功能和更改的功能。

## <a name="create-links-from-talent-to-finance-and-operations"></a>创建从 Talent 到 Finance and Operations 的链接
此新导航功能允许您从 Talent 链接到 Finance and Operations，为您提供访问 Finance and Operations 页面的直接导航。 在链接配置后，您可以指定链接应在 Talent 中显现的名称和组，以及要在 Finance and Operations 内打开的目标页。

#### <a name="coming-soon"></a>即将到期
未来将添加字段上下文，以允许直接导航到 Finance and Operations 中的相应记录。 例如，您可以使用**链接到字段**提供上下文以直接导航到 Finance and Operations 中的特定员工或职位。

### <a name="configure-target-systems"></a>配置目标系统

在 Talent 中，系统管理员可以定义将通过系统管理工作区显现的链接。 配置的一部分是您希望作为链接“目标”导航到的 Finance and Operations 环境。 您可以通过向目标系统提供名称并提供 Finance and Operations 环境的 URL 来完成此任务。 这是您会提供的 Finance and Operations URL 的示例：https://devax00124aos.cloud.test.dynamics.com/。 在配置您的目标系统后，您可以定义您的链接。

### <a name="configure-links"></a>配置链接

创建的每个链接将定义了以下信息。

- 链接 - 链接的名称，仅用于标识。

- 启用此链接 - 如果要向 Talent 用户显示链接，请设置为**是**。

- 显示名称 - 定义将显示为 Finance and Operations 的链接的名称。 此数据当前没有翻译。

- 窗体上的表面链接 - 选择您希望显示链接的页面。

- 组 - 组不是必要的，不过，如果您希望使用组来管理链接，请使用**组**字段选择现有组或创建新组。

- 目标系统 - 选择使用**配置目标系统**选项创建的目标系统。 这将是在使用链接导航时使用的 Finance and Operations 环境。

- 使用用户的当前公司 - 如果您希望在导航到 Finance and Operations 时使用用户的当前公司上下文，请选择**是**。 如果选择**否**，您可以选择应使用的公司。

- 目标菜单项 - 输入导航时链接应使用的 Finance and Operation 的菜单项。 提供您可以直接导航的菜单项。 若要查找所需的菜单项，打开 Finance and Operations 并打开作为导航目标的页面。 从 URL 复制菜单项。 例如，如果您希望链接将您带到 Finance and Operations 中的员工列表，请输入在 URL 中的 "&mi" 后出现的值。 https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees。 在本示例中导航到员工列表页面的菜单项是：HcmWorkerListPage_Employees。

- 链接到数据源 - 选择链接所引用数据的源。 提供最常见的源，如**工作人员**和**职位**。

- 链接到字段 -（即将推出）选择此字段将允许从 Talent 中的单一记录直接导航到 Finance and Operations 中的单一记录。

### <a name="access-to-links"></a>访问链接

系统管理员将在定义的页面上看到新创建的链接，即使**启用此链接**选项设置为**否**。 这可以用于在向其他员工显示链接前对链接进行测试。 在**启用此链接**选项设置为**是**后，所有其他角色将只能看到配置的链接。 有权访问链接显示页面的员工将有权访问这些链接。

用户还可以定义 Finance and Operations 内的安全权限以在 Finance and Operations 中访问页面。 如果未定义，在使用链接时将显示安全对话框。


## <a name="other-changesfixes"></a>其他更改/修复

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a>具有未来开始日期的职位不能分配给新员工

为允许员工被分配未来日期的职位进行了更改。 可以选择开始日期在将来的职位，员工分配将在工作流保存或完成后进行（如果启用了工作流）。

### <a name="new-employee-cannot-be-assigned-existing-position"></a>新员工不能被分配现有职位

进行了相应更改，新员工现在可以被分配到现有职位。

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a>当雇用开始日期在过去时，受聘日期/办公地点在保存记录时消息。

进行了相应更改，更正了在为以往员工保存更改时**受聘日期**和**办公地点**的可见性。

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a>无法在工作人员页面为将来日期的雇用输入数据

将来日期的雇用的雇用数据已在主工作人员页面禁用。 雇用数据可以通过**日期管理器**页面输入。 未来发布中将进行更多更改来支持直接在工作流程中输入雇用数据。

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a>将 ValidFrom 和 ValidTo 添加到 HcmPersonalContactPersonEntity 中

数据管理框架 (DMF) 实体 HcmPersonalContactPersonEntity 已更新，以包括支持某些福利集成场景的“生效”和“失效”日期。 

## <a name="known-issue"></a>已知问题
- **问题**：在将新附件添加到工作人员时，**新建**和**编辑**按钮变灰。 
- **解决方法：** 打开附件页面之前，确保已关闭**工作人员**页面中的速见表。 如果加载**工作人员**页面时速见表已关闭，将启用附件按钮。 （下一个平台更新中将解决这个问题。）

