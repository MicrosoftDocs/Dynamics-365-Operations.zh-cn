---
title: "使用 Excel 外接程序"
description: "使用 Excel 的 Office，Microsoft Dynamics 外接程序此主题说明如何到 Microsoft Excel 中对数据实体，然后更新，显示，以及编辑数据。 若要打开数据实体，则可以从 Excel 或 Microsoft Dynamics 365 开始的工序。"
author: ChrisGarty
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: af7e7288f741b3c519227e2778c4c4311c3a2012
ms.openlocfilehash: 8af663b47117759ed3b2e2ed8eee85ae4df100d1
ms.lasthandoff: 03/31/2017


---

# <a name="use-the-excel-add-in"></a>使用 Excel 外接程序

使用 Excel 的 Office，Microsoft Dynamics 外接程序此主题说明如何到 Microsoft Excel 中对数据实体，然后更新，显示，以及编辑数据。 若要打开数据实体，则可以从 Excel 或 Microsoft Dynamics 365 开始的工序。

使用 Excel 的 Office，Microsoft Dynamics 外接程序"按在 Microsoft Excel 中对数据实体，可以轻松快捷地查看和编辑的数据。 此外接程序需要 Microsoft Excel 2016 年。 **注释：**，如果您的 Microsoft Azure Active Directory (Azure 的 AD) 有关配置使用 Active Directory 选择身份验证服务 (AD FS)，则您必须确保，5 月 2016 更新应用，因此，Excel 外接程序可以正确。您。

## <a name="open-entity-data-in-excel-when-you-start-from-dynamics-365-for-operations"></a>在 Excel 数据实体的开票，在从 Dynamics 365 开始的工序
1.  在一页。Microsoft Dynamics 365 中的工序，请单击**在 Microsoft Office **打开。 如果根数据源 ("表") 页的与所有实体的根目录数据源，默认的相同的**在 Excel 中打开。**页面选项生成。 **在 Excel **未结的选项可以在中频繁使用的页面找到，例如**所有供应商** ** **和所有客户。
2.  **单击打开在 Excel **选项，并且打开生成的工作簿。 此工作簿具有实体、指针到您的环境和指针约束的信息。外接程序 Excel。
3.  **在 Excel，启用"启用编辑**对运行的 Excel 外接程序单击"。 Excel 外接程序窗格中运行以在 Excel 窗口的权限。
4.  如果您是运行一次外接程序 Excel，请单击**此委托外接程序**。
5.  如果提示您登录，请单击**登录**登录，然后使用您使用登录到工序的 Dynamics 365 的相同凭据。 则可以外接程序，Excel 将使用来自 Internet Explorer 中前登录上下文和自动签入您。 因此，请验证用户名。在 Excel 外接程序的右上角中。

Excel 外接程序读取数据自动为您所选实体。 这不会注意在工作簿中数据，在 Excel 外接程序写入它。

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>在 Excel 数据实体的开票，在从 Excel 开始
1.  在 Excel，在插入** **请在**组中的选项卡上，Addins **，**开设 Office 商店的商店。单击**
2.  在 Office 商店，在"搜索关键字“Dynamics”，然后单击"添加** **的旁边** Microsoft Dynamics 外接程序** Office Excel (外接程序)。
3.  如果您是运行一次，请外接程序 Excel **此委托外接程序**启用对运行的 Excel 外接程序单击"。 Excel 外接程序窗格中运行以在 Excel 窗口的权限。
4.  **请添加服务器信息**打开**选项**窗格中单击。
5.  复制 URL 从您的工序的目标 Dynamics 365 实例的浏览器，将数据粘贴到**在服务器 URL **主机名后"，然后删除所有内容 (例如，删除**/? ** cmp=usmf&mi=CustTableListPage)。 发生的 URL 应与主机名 (例如，https://xxx.dynamics.com**) **。
6.  **好**单击，然后单击** **为确认更改。 添加 Excel 重新启动负荷和元数据。 ** Design **现在按钮才可用。 如果 Excel 外接程序具有**。负荷小程序**，请按您可能没有正确身份登录到的用户。 有关详细信息，请参阅“小程序负荷按钮{{在此：in}}主题的“排除”部分显示”。
7.  ** Design **单击。 Excel 外接程序检索实体元数据。
8.  **单击表**添加。 实体列表中会出现相应 实体“名称列表-标记”格式。
9.  在列表中选择某一实体，例如-客户** **客户，然后单击"下一步** **。
10. **从可用字段**列表要添加字段。**所选字段**列表中，请单击该字段，然后单击** **添加。 或者，请双击字段。
11. 在您添加了所需字段。** **选择的字段列表后，确保游标工作表中的正确位置 (例如，A1 单元格)，然后单击** **执行。 然后单击**执行**退出设计器。
12. **一组可提取**单击"刷新数据。

## <a name="view-and-update-entity-data-in-excel"></a>查看和实体在 Excel 数据更新
在 Excel 外接程序读取数据实体到工作簿后，可以通过单击"更新数据刷新**在任何时间**在 Excel 外接程序。

## <a name="edit-entity-data-in-excel"></a>编辑在 Excel 数据实体的
您可更改数据实体，然后通过单击您需要将其发布**请发布**在 Excel 外接程序。 若要编辑记录，请选择工作表中的单元格，然后更改单元格值。 若要创建新记录，请按以下步骤之一：

-   单击想要在工作表，然后单击新** **在 Excel 外接程序。
-   单击在工作表的最后一行，然后按搬出游标标记键，直到该行结束列，并且新的行进行创建。
-   单击"行立即在工作表下，并会使启动输入在单元格的数据。 当您移动该焦点不足单元格中时，该工作表展开到涵盖新行。

若要删除记录，请按以下步骤之一：

-   单击该工作表行旁边行号删除右键单击，然后单击** **删除。
-   右键单击在工作表删除行，然后单击"删除** &gt; ** **表**行。

## <a name="add-or-remove-columns"></a>添加或删除列
您可以使用设计器调整自动添加到工作表的列。

1.  **通过单击选项** (按齿轮符号) 然后选择**启用"设计**此复选框可以启动 Excel 外接程序的数据源设计器。
2.  **单击 Design **在 Excel 外接程序。 所有数据源中。
3.  "数据源旁，请单击"编辑** ** "按钮 (铅笔符号)。
4.  在调整的列表**所选字段**列表，您需要：
    -   **从可用字段**列表要添加字段。**所选字段**列表中，请单击该字段，然后单击** **添加。 或者，请双击字段。
    -   从字段**若要删除所选字段**列表中，请单击该字段，然后单击** **中删除。 或者，请双击字段。
    -   若要更改字段顺序，单击所选字段的字段** **列出，然后单击** ** **或向下**。

5.  通过单击应用对数据的来源更改** **更新。 然后单击**执行**退出设计器。 如果您添加了一字段 (列)，单击**刷新**组使用更新数据。

## <a name="httpspowerappsmicrosoftcomenustutorialsdataplatforminteractiveexceltroubleshootingtroubleshooting"></a>[](https://powerapps.microsoft.com/enus/tutorials/dataplatforminteractiveexcel/#troubleshooting)Troubleshooting
具有可以通过最便捷的某些步骤以解析的一些问题。

-   **负荷小程序"按钮进行查看。** 如果 Excel 外接程序具有**。负荷小程序**登录，则在以后可能按未登录为正确的用户。 为了解决此问题，请确认正确的用户名。显示在 Excel 外接程序的右上角中。 如果了不正确显示用户名，它，请单击"注销"，然后签名。
-   **您收到“取消”的消息。** 如果您接收“禁止的”消息，在 Excel 外接程序加载元数据时，登录到 Excel 外接程序的帐户无权在使用所针对的服务、实例或数据库。 为了解决此问题，请确认正确的用户名。显示在 Excel 外接程序的右上角中。 如果了不正确显示用户名，它，请单击"注销"，然后签名。
-   **一个空白部件显示在 Excel。** 如果一个空白 Web 在登录过程中打开，帐户 AD FS，要求，但运行外接程序 Excel 的版本不是最近的足够加载登录对话框。 为了解决此问题，请更新您使用 Excel 的版本。 若要更新 Excel 的版本，当您是在延迟的通道的企业中，请将 [Office 部署工具 https://technet.microsoft.com/library/jj219422.aspx) 从 [] (延迟的通道的移到当前通道] (https://technet.microsoft.com/library/mt455210.aspx)。



