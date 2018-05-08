---
title: "扩展 Microsoft Dynamics 365 for Talent 的功能"
description: "如果您创建了任何 Microsoft PowerApps，您可以从 Microsoft Dynamics 365 for Talent 内的链接启动那些应用程序。"
author: rschloma
manager: AnnBe
ms.date: 03/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 51eb4288f5b6c732755007c1dcd8c4db090ccc0a
ms.contentlocale: zh-cn
ms.lasthandoff: 03/07/2018

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a>扩展 Microsoft Dynamics 365 for Talent 的功能

[!include [banner](includes/banner.md)]

如果您创建了任何 Microsoft PowerApps，您可以从 Microsoft Dynamics 365 for Talent 内的链接启动那些应用程序。 若要设置对您的应用程序的访问，您需要在可以从**系统管理**工作区打开的配置页面上设置 Talent 中的一些信息。

## <a name="configuring-embedded-powerapps-within-talent"></a>配置 Talent 内嵌入的 PowerApps
使用**设置嵌入的 Microsoft PowerApps** 页面来将 Talent 页面配置为启动 PowerApps 应用程序。 若要打开**设置嵌入的 Microsoft PowerApps** 页面，请打开**系统管理**工作区，然后打开**链接**选项卡。从**设置**组选择 **Microsoft PowerApps**。 

以下信息在此页上输入或设置： 

 -  每个 PowerApps 应用程序的描述性名称或标识符。
 -  您添加到 Talent 页面的每个应用程序的唯一标识符 (GUID)。 应用 ID 在 PowerApps 网站 [powerapps.com](http://powerapps.com/) 上可用。 
 -  用户可以打开应用程序或报表的页面。 并非所有 Talent 页面都支持嵌入的 PowerApps 和 Power BI 报表。 

 > [!NOTE]
 >  输入页面的内部名称，而不是在页面顶部出现的显示名称。 若要找到内部名称，打开您需要其内部名称的页面，右键单击页面的任何位置。 在菜单打开时，悬停在**窗体信息**项上。 内部窗体名称显示在菜单中**窗体信息**项的旁边。
 
-   指定应用程序可以从中检索上下文数据的窗体控件。 例如，应用程序可以使用工作人员的相关数据。 如果您在**上下文**字段中输入**工作人员**页面，在您启动应用程序时**工作人员**页面将打开。 在**上下文字段**中的输入是可选的。 
-   设置 PowerApps 应用程序将在其中运行的对话框的大小。 对话框被指定为“小”或“大”以优化应用程序分别在手机或更大设备上运行时的用户界面。 


您还可以指定可使用应用程序的法人，或者您可以让其对所有法人可用。 默认情况下，您的 PowerApps 应用程序可供所有法人使用。

## <a name="opening-an-application"></a>打开应用程序
在配置了嵌入的 PowerApps 应用程序后，指向您指定的应用程序的链接将被添加到 Talent 内的页面。 单击一个链接打开一个应用程序。 



