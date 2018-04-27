---
title: "使用 Excel 加载项"
description: "此主题介绍如何通过使用适用于 Excel 的 Microsoft Dynamics Office 加载项，在 Microsoft Excel 中打开实体数据，然后查看、更新和编辑这些数据。"
author: ChrisGarty
manager: AnnBe
ms.date: 04/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e0e3e86820e0857b320d832c3bf3c94757667919
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="use-the-excel-add-in"></a>使用 Excel 加载项

[!INCLUDE [banner](../includes/banner.md)]

此主题介绍如何通过使用适用于 Excel 的 Microsoft Dynamics Office 加载项，在 Microsoft Excel 中打开实体数据，然后查看、更新和编辑这些数据。 若要打开实体数据，可从 Excel 或 Microsoft Dynamics 365 for Finance and Operations 开始。

通过在 Excel 中打开实体数据，可以使用 Excel 加载项快速、轻松地查看和编辑这些数据。 此加载项需要 Microsoft Excel 2016。

> [!NOTE]
> 如果将您的 Microsoft Azure Active Directory (Azure AD) 租户配置为使用 Active Directory Federation Services (AD FS)，则必须确保已应用了 2016 年 5 月的 Office 更新，以便 Excel 加载项可以让您正确登录。

若要了解有关如何使用 Excel 加载项的详细信息，请观看短片[在 Dynamics 365 for Finance and Operations 中为标头和行模式创建 Excel 模板](https://youtu.be/RTicLb-6dbI)。

> [!Video https://www.youtube.com/embed/RTicLb-6dbI]


## <a name="open-entity-data-in-excel-when-you-start-from-finance-and-operations"></a>从 Finance and Operations 开始时在 Excel 中打开实体数据
1. 在 Finance and Operations 中的一个页面内，选择**在 Microsoft Office 中打开**。

    如果该页面的根数据源（表）与任何实体的根数据源相同，将为该页面生成默认**在 Excel 中打开**选项。 可以在常用页面（如**所有供应商**和**所有客户**）中找到**在 Excel 中打开**选项。
 
2. 选择**在 Excel 中打开**选项，然后打开生成的工作簿。 此工作簿中包含实体的绑定信息、指向您的环境的指针，以及指向 Excel 加载项的指针。
3. 在 Excel 中，选择**启用编辑**以启用并运行此 Excel 加载项。 将在 Excel 窗口右侧的窗格中运行此 Excel 加载项。
4. 如果首次运行此 Excel 加载项，则选择**信任此加载项**。
5. 如果系统提示您登录，选择**登录**，然后使用用于登录 Finance and Operations 的相同凭据登录。 此 Excel 加载项将使用 Internet Explorer 中之前的登录上下文，并自动让您登录（如果可以）。 因此，请验证此 Excel 加载项右上角中的用户名。

此 Excel 加载项自动读取您所选实体的数据。 请注意，Excel 加载项读入数据之前，工作簿中无任何数据。

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>从 Excel 开始时在 Excel 中打开实体数据
1. 在 Excel 中的**插入**选项卡上的**加载项**组中，选择**应用商店**打开 Office 应用商店。
2. 在 Office 应用商店中，搜索关键字 **Dynamics**，然后选择 **Microsoft Dynamics Office 加载项**（即此 Excel 加载项）旁边的**添加**。
3. 如果首次运行此 Excel 加载项，请选择**信任此加载项**以启用并运行此 Excel 加载项。 将在 Excel 窗口右侧的窗格中运行此 Excel 加载项。
4. 选择**添加服务器信息**打开**选项**页面。
5. 在浏览器中，复制目标 Finance and Operations 实例的 URL，将其粘贴到**服务器 URL** 字段中，然后删除主机名后的所有内容。 产生的 URL 应只有一个主机名。

    例如，如果 URL 为 `https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage`，则删除除 `https://xxx.dynamics.com` 以外的所有内容。

6. 选择**确定**，然后选择**是**确认更改。 此 Excel 加载项将重新启动并加载元数据。

    **设计**按钮现在可用。 如果此 Excel 加载项有**加载小程序**按钮，您可能无法作为正确用户登录。 有关详细信息，请参阅本主题[故障排除](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in#troubleshooting)部分中的“显示‘加载小程序’按钮”。

7. 选择**设计**。 此 Excel 加载项将检索实体元数据。
8. 选择**添加表**。 将显示实体列表。 将以“名称 - 标签”格式列出实体。
9. 选择列表中的实体（如**客户 - 客户**），然后选择**下一步**。
10. 若要将**可用字段**列表中的字段添加到**所选字段**列表，选择该字段，然后选择**添加**。 或者，双击**可用字段**列表中的字段。
11. 将字段添加到**所选字段**列表之后，请确保光标在工作表中的正确位置（如单元格 A1），然后选择**完成**。 然后选择**完成**退出设计器。
12. 选择**刷新**以提取一组数据。

## <a name="view-and-update-entity-data-in-excel"></a>在 Excel 中查看和更新实体数据
此 Excel 加载项将实体数据读入工作簿之后，随时可通过选择 Excel 加载项中的**刷新**更新这些数据。

## <a name="edit-entity-data-in-excel"></a>在 Excel 中编辑实体数据
可根据需要更改实体数据，然后通过选择 Excel 加载项中的**发布**将其发布回来。 若要编辑记录，请在工作表中选择单元格，然后更改单元格值。 若要创建新记录，请执行以下步骤之一：

- 单击数据源表中的任意位置，然后选择此 Excel 加载项中的**新建**。
- 在数据源表最后一行中单击任何位置，然后按 Tab 键，直到光标移出该行的最后一列，并创建一个新行。
- 在数据源表正下方的行中单击任何位置，然后开始在单元格中输入数据。 将光标移出该单元格时，表将扩展以容纳新行。
- 要进行标题记录的字段绑定，选择其中一个字段，然后在 Excel 加载项中选择**新建**。

请注意，只有当所有重要的必填字段在工作表中绑定时，或当使用筛选条件填写默认值时，才能够创建新记录。

若要删除记录，请执行以下步骤之一：

- 右键单击应删除的工作表行旁边的行号，然后选择**删除**。
- 右键单击应删除的工作表行旁边内的任何位置，然后选择**删除** &gt; **表行**。

如果数据源添加为相关数据源，标题在行前面发布。 如果其他数据源之间存在相关性，您可能必须更改默认发布顺序。 若要更改发布顺序，在 Excel 加载项中，选择**选项**按钮（齿轮符号），然后，在**数据连接器**快速选项卡上，选择**配置发布顺序**。

## <a name="add-or-remove-columns"></a>添加或删除列
可以使用设计器调整自动添加到工作表的列。

> [!NOTE]
> 如果**设计**按钮未出现在 Excel 加载项中的**筛选**按钮下，您必须启用数据源设计器。 选择**选项**按钮（齿轮符号），然后选择**启用设计**复选框。

1. 在 Excel 加载项中，选择**设计**。 将列出所有数据源。
2. 选择数据源旁边的**编辑**按钮（铅笔符号）。
3. 在**所选字段**列表中，根据需要调整字段列表：

    - 若要将**可用字段**列表中的字段添加到**所选字段**列表，选择该字段，然后选择**添加**。 或者，双击**可用字段**列表中的字段。
    - 若要删除**所选字段**列表中的字段，选择该字段，然后选择**删除**。 或者双击该字段。
    - 若要更改字段的顺序，请在**所选字段**列表中选择字段，然后选择**向上**或**向下**。

4. 若要应用对数据源的更改，选择**更新**。 然后选择**完成**退出设计器。
5. 如果添加了字段（列），选择**刷新**提取更新后的数据集。

## <a name="copy-environment-data"></a>复制环境数据

读入一个环境的工作簿中的数据可以复制到另一个环境。 但是，您无法仅更改连接 URL，因为工作簿中的数据缓存会继续将该数据视为现有数据。 您必须使用“复制环境数据”功能将数据作为新数据发布到新的环境。

1. 选择**选项**按钮（齿轮符号），然后，在**数据连接器**快速选项卡上，选择**复制环境数据**。 
2. 输入新环境的服务器 URL。 
3. 选择**确定**，然后选择**是**确认操作。 Excel 加载项将重新启动并连接到新的环境。 工作簿中的所有现有数据将被视为新数据。

    在 Excel 加载项重新启动后，消息框显示工作簿处于环境复制模式。

4. 若要作为新数据将数据复制到新环境，请选择**发布**。 若要取消环境复制操作并在新环境中查看现有数据，选择**刷新**。

## <a name="troubleshooting"></a>疑难解答
可通过某些简单步骤解决一些问题。

- **将显示“加载小程序”按钮** – 如果登录后此 Excel 加载项有**加载小程序**按钮，您可能无法作为正确用户登录。 若要解决此问题，请验证此 Excel 加载项右上角中是否显示正确的用户名。 如果显示错误的用户名，请选择该用户名，注销，然后再次登录。
- **您收到“已禁止”消息** – 如果此 Excel 加载项加载元数据时收到“已禁止”消息，则登录了该 Excel 加载项的帐户无权使用目标服务、实例或数据库。 若要解决此问题，请验证此 Excel 加载项右上角中是否显示正确的用户名。 如果显示错误的用户名，请选择该用户名，注销，然后再次登录。
- **Excel 上方显示空白网页** – 如果登录过程中打开空白网页，则帐户需要 AD FS，但是正在运行此 Excel 加载项的 Excel 版本不够高，无法加载登录对话框。 若要解决此问题，请更新正在使用的 Excel 版本。 若要当您在处于推迟渠道中的企业内时更新 Excel 版本，请使用 [Office 部署工具](https://technet.microsoft.com/library/jj219422.aspx)[从推迟渠道转到当前渠道](https://technet.microsoft.com/library/mt455210.aspx)。

