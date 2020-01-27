---
title: Dynamics 365 Talent（2019 年 2 月 27 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 02/27/2019
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
ms.search.validFrom: 2019-02-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d0fdc9f056ea494cf52e8483b901070dae0bcd29
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897664"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-27-2019"></a>Dynamics 365 Talent（2019 年 2 月 27 日）中的新增功能或更改

此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。

## <a name="changes-in-onboard"></a>Onboard 中的更改

本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改

本部分中的更改适用于内部版本号 8.1.2163

### <a name="add-a-custom-fields-menu-item-to-system-administration"></a>在“系统管理”中增加了一个“自定义字段”菜单项

**系统管理**工作区中增加了到**自定义字段**菜单的导航。

### <a name="hide-the-import-and-create-options-for-new-mobile-applications"></a>对新移动应用程序隐藏导入和创建选项

目前不能在 Talent 中创建新移动应用程序。 **移动应用**菜单中已删除了用于新建移动体验的选项。

### <a name="variable-compensation-award-dmf-entity"></a>可变薪酬奖励（DMF 实体）

此版本中现在可导出**可变薪酬奖励** 数据管理框架 (DMF) 实体。

### <a name="uk-addresses-appear-in-the-personnel-management-analytics-page-as-swiss-addresses"></a>英国地址在个人管理分析页中显示为瑞士地址。

此版本中，地址按城市显示。 此版本更正了员工地址显示不正确这一问题。

### <a name="the-workforce-power-bi-report-shows-an-error-when-a-workers-seniority-date-is-on-leap-day"></a>当工作人员受聘日期是闰日时劳动力 Power BI 报表显示错误

Microsoft Power BI 中已修复了帐户的 2 月 29 日闰日问题。

### <a name="employee-fixed-compensation-employee-variable-awards-employee-variable-plans-enrollments-allow-for-custom-fields"></a>允许将“员工固定薪酬”、“员工可变奖励”、“员工可变计划(登记)”字段设置为自定义字段。

现在可为员工固定薪酬、员工可变奖励和员工可变计划（登记）添加自定义字段。 除了默认显示的信息，现在还可以跟踪有关员工固定薪酬计划和可变薪酬计划的详细信息。 可以通过用户界面或提供的实体输入和更新自定义字段。

### <a name="other-miscellaneous-bug-fixes"></a>其他杂项缺陷修复

此版本中还包含其他小缺陷修复。

## <a name="coming-soon"></a>即将到期

### <a name="advanced-compensation-security-fixed-and-variable"></a>高级薪酬安全（固定和可变）

在许多组织中，薪酬和福利经理可能只能访问特定薪酬记录。 这些记录可能是有关管理层或地区员工的记录。 这一更改让人力资源 (HR) 可以管理和维护组织中不同员工群的薪酬计划。 可分配给固定计划和可变计划的安全角色决定这些计划和与其有关的员工数据（例如，工资信息和奖金记录）的访问权限。 只有具有指定访问权限的角色才能处理这些员工的薪酬。

### <a name="platform-update-24-for-finance-and-operations"></a>Finance and Operations 的平台更新 24

有关 Microsoft Dynamics 365 Finance and Operations 的平台更新 24（2019 年 3 月）的详细信息，请参阅 [Finance and Operations 平台更新 24（2019 年 3 月）中的预览功能](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24)。

### <a name="make-employee-fixed-compensation-available-for-future-position-assignments"></a>将来的职位分配中可使用员工固定薪酬。

加入组织的员工的开始日期通常在以后。 通过此项更改，可以为将来分配的职位所属员工定义固定薪酬。

## <a name="known-issues"></a>已知问题

### <a name="changes-to-the-core-hr-integration-template-talent-common-data-service-to-finance"></a>Core HR 集成模板（Talent Common Data Service 到 Finance）的更改
Core HR 的模板已更新为“高级查询模板”。 因此，默认情况下，通过使用此模板创建的项目可使用高级查询。 次日，只有高级查询编辑器中才会显示任何默认映射功能。 （默认映射功能在映射中显示为“FN”。）

有关映射错误的详细信息，请参阅 [Dynamics 365 Talent: Core HR（2018 年 12 月 14 日）中的新增功能或更改](https://docs.microsoft.com/dynamics365/unified-operations/talent/whats-new-talent-december-14)。

若要使用新模板，请新建一个项目，然后选择新的 Talent 集成模板。

若要更新现有模板，请执行以下步骤。

1. 更新以下映射：

    - **工作职位到职位：** 删除此映射。
    - **职位到职位父工作分配”：** 删除此映射。
    - **工作职位到基本职位：** 添加从 Common Data Service **工作职位**实体到 Finance and Operations **基本职位**实体的新映射。 将其移到了序列中的位置 7。

        [![“工作职位”到“基本职位”映射](./media/CDS-Mapping1.png)](./media/CDS-Mapping1.png)

    - **工作职位到职位详细信息：** 添加从 Common Data Service **工作职位**实体到 Finance and Operations **职位详细信息**实体的新映射。 将其移到了序列中的位置 8。

        [![“工作职位”到“职位详细信息”映射](./media/CDS-Mapping2.png)](./media/CDS-Mapping2.png)

    - **工作职位到职位持续时间：** 添加从 Common Data Service **工作职位**实体到 Finance and Operations **职位持续时间**实体的新映射。

        [![“工作职位”到“职位持续时间”映射](./media/CDS-Mapping3.png)](./media/CDS-Mapping3.png)

    - **工作职位到职位层次结构：** 添加从 Common Data Service **工作职位**实体到 Finance and Operations **职位层次结构**实体的新映射。 选择**高级查询**可将高级查询用于您的项目。

       [![“高级查询”按钮](./media/CDS-Advanced-Query.png)](./media/CDS-Advanced-Query.png)

2. 添加以下映射。
    
    [![地理信息](./media/CDS-Mapping4.png)](./media/CDS-Mapping4.png)

    1. cdm_jobpositionnumber cdm_jobspositionnumb... = POSITIONID cdm_parentjobpositionid.cdm-jobpositionnumb... = PARENTPOSITIONID cdm_validfrom cdm_validfrom = VALIDFROM cdm_validto cdm_validto = VALIDTO
       
    2. 选择**搜索**字段旁边的**高级查询和筛选**链接。  

    3. 找到 **cdm_parentjobpositionid.cdm_jobpositionnumber** 列，然后选择其右侧的向下箭头按钮。

    4. 在显示的对话框中，选择**删除空**。

    5. 选择**添加列 \> 添加条件列**为 HIERARCHYTYPENAME 添加默认值转换。

        [![“添加条件列”命令](./media/Add-column.png)](./media/Add-column.png)

    6. 在**添加条件列**对话框中，输入 **HIERARCHYTYPENAME** 充当新列的名称。
    7. 在条件的 **If** 部分中，选择任何字段，关系使用**等于**，然后输入任何值。 在条件的 ***Then** 和 **Otherwise** 部分中，指定应使用哪个默认值。 在此案例中，两部分均输入**行**。

        [![“添加条件列”对话框](./media/Add-conditional-column.png)](./media/Add-conditional-column.png)

    8. 选择**确定**关闭**高级查询和筛选**对话框。
    9. 在**映射任务**页上，源选择新列，以便为 HIERARCHYTYPENAME 再创建一个映射。

        [![地理信息](./media/CDS-Mapping5.png)](./media/CDS-Mapping5.png)
