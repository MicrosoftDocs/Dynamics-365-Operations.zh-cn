---
title: 简化的员工条目和导航
description: Dynamics 365 Talent 中的工作人员的数据输入已得到增强，允许所有员工（过去、现在或将来）快速输入。 已更新简化/整合的导航模型，可以快速查找相关信息并查看和进行任何必要的更新。
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent October 2019 update
ms.openlocfilehash: 40bbb8429355fa18fe12c7cf56f8d58f19766cad
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009414"
---
# <a name="streamlined-employee-entry-and-navigation"></a>简化的员工条目和导航

[!include [banner](includes/banner.md)]

Dynamics 365 Talent 允许高效输入员工和雇用数据。 您可以快速更新过去、现在和将来员工和合同工的工作历史信息。

您还可以启用简化的导航体验，来快速查找相关信息并进行必要的更改。 此功能现在可在沙盒环境中使用。 要打开此功能，请导航至**系统管理 > 链接 > 设置 > 系统参数 > 预览功能**。 选择**增强的工作人员窗体和导航**。 这将为所有用户启用这些更改。 您可以随时关闭此选项。

## <a name="view-options"></a>视图选项

您可以使用工作人员窗体上的**查看选项**从单个列表中选择员工和合同工的任意组合。 通过这些选项，您可以跨法人查看工作人员或查看您当前登录的法人的工作人员。 您还可以查看有效、待定和离职的工作人员，您可以根据工作人员的类型（员工或合同工）限定结果。 如果启用了高级安全性，您将只能看到您有权访问的法人的员工和合同工。

列表视图中的列会根据您的选择而更改。 例如，在查看离职员工时，终止雇用日期和原因代码将显示为列表中的其他列。 

[![视图选项](./media/Worker-view-option.png)](./media/worker-view-option.png)

## <a name="navigation-and-banner"></a>导航和横幅

横幅显示每个工人的关键信息。 有效工作人员的横幅显示以下字段：

- **称谓**
- **部门**
- **职位类型**
- **工作人员类型**
- **经理**
- **法人**

离职工作人员的横幅显示以下字段：

- **离职日期**
- **原因**

待定员工的横幅显示以下字段：

- **称谓**
- **部门**
- **职位类型**
- **经理**
- **开始日期**
- **法人**

工作人员页面的操作窗格已重新安排，以包含更少的选项。 信息现在按以下类别管理： 

- 工作
- 人员
- 离开
- 薪酬
- 福利
- 合规性

此外，主工作人员页面上的新**链接**选项卡为用户提供了访问工作人员所有相关信息的中心位置。

由于这些更改，信息可能会出现在您习惯的不同位置。 例如，先前显示在工作人员窗体上的工资单信息现在显示在**薪酬 > 工资单**下的操作窗格中，而**个人信息**选项卡现在具有**更多信息**按钮，可以隐藏不经常访问的字段。

[![横幅](./media/Banner.png)](./media/Banner.png)

## <a name="work-history"></a>工作历史记录

**工作历史记录**选项卡显示所有法人的工作历史记录，可供离职、有效和待定的员工和合同工使用。 您现在可以立即查看您有权访问的法人的所有工作历史记录。 此外，您还可以编辑每个工作历史记录条目的信息，而无需更改数据上下文。 您可以直接在页面上更新所有信息。 

[![工作历史记录](./media/Worker-work-history.png)](./media/Worker-work-history.png)

## <a name="position-history"></a>职位历史记录

主工作人员页面上的**职位**选项卡提供了组织内所有职位的完整视图，包括过去、现在和所有将来的分配。 您仍然可以在操作窗格中直接导航到工作人员的职位历史记录。

[![职位](./media/Worker-position-history.png)](./media/Worker-position-history.png)

