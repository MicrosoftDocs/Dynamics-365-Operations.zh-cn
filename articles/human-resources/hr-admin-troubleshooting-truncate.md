---
title: 避免职位层次结构的文本截断并导出到 Visio
description: 本主题说明如何解决当客户在 Microsoft Dynamics 365 Human Resources 中查看职位层次结构时出现个人姓名和职位名称截断的问题。
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 20331b3a06301d10177fd0d5734f6e33994ef123
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693939"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a>避免职位层次结构的文本截断并导出到 Visio


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**发货**

当客户在 Microsoft Dynamics 365 Human Resources 中查看职位层次结构时，个人和职位名称截断。 因此，可能很难拍摄屏幕快照，或打印和分配层次结构。

![职位层次结构。](media/position-h.png)

**原因**

此为有意行为。

**解决方法**

遗憾的是，用户不能轻松更改文本的大小。 但是，您可以将职位层次结构从 Human Resources 中导出，然后导入到 Microsoft Visio。 以下文章是为 Microsoft Dynamics AX 2012 所写，但过程也适用于 Human Resources：[导出职位层次结构到 Microsoft Visio](/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio)。

执行以下步骤导出到 Visio。

1. 在 Human Resources 中，打开 **职位** 列表页。

    若要在组织结构图中包括更多信息，请向 **职位** 列表添加字段，以便在您以后在此过程中使用 **组织结构图向导** 时这些信息可用。

2. 在操作窗格上，选择 **在 Microsoft Office 中打开** 按钮，然后，在 **导出到 Excel** 下，选择 **职位**。 或者，按 Ctrl+T。

    ![将职位列表页面导出到 Excel。](media/org-admin.png)

3. 保存导出的 Excel 文件。

    ![“导出到 Excel”对话框。](media/export-excel.png)

4. 在 Visio 中，选择 **Visio - 新建**，然后选择 **业务** 模板类别。

    ![新建图表。](media/new.png)

5. 选择 **组织结构图向导**，然后选择 **创建**。

    ![组织结构图向导对话框。](media/orgchart-wizard.png)

6. 选择 **文件或数据库中已存储的信息**，然后选择 **下一步**。

    ![组织结构图向导 1。](media/orgchart-wizard7.png)

7. 选择 **文本、Org Plus (\*.txt) 或 Excel 文件**，然后选择 **下一步**。

    ![组织结构图向导 2。](media/orgchart-wizard3.png)

8. 浏览选择导出的包含职位层次结构的 Excel 文件，然后选择 **下一步**。

    ![组织结构图向导 3。](media/orgchart-wizard2.png)

9. 将 **名称** 字段设置为 **职位**，将 **报告至** 字段设置为 **直接上级职位**，然后选择 **下一步**。

    ![组织结构图向导 4。](media/orgchart-wizard1.png)

10. 选择应显示在每个节点的字段，然后选择 **下一步**。

    ![组织结构图向导 5。](media/orgchart-wizard5.png)

11. 将 **职位** 列添加到 **形状数据字段** 列表，然后选择 **下一步**。

    ![组织结构图向导 6。](media/orgchart-wizard6.png)

12. 图片当前未提供。 因此，在下一页，选择 **下一步**。
13. 选择 **我希望向导跨各个页面自动中断我的组织结构图**。

    ![组织结构图向导 7。](media/orgchart-wizard4.png)

14. 选择 **完成**。

    如果有职位未在结构中，将要求您在图表中包括它们。

在 Visio 中生成的图表在单独的工作表中显示每位经理。

根据您选择要包括在图表中的字段，每个节点会在 Visio 文件生成时显示相应的信息。

![层次结构图。](media/hierarchy.png)

**其他选项**

在 Human Resources 中，您可能还可以使用 **人员** 工作区来查看某些层次结构相关信息。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
