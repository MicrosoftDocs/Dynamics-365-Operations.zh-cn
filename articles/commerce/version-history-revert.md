---
title: 查看版本历史记录以还原页面和片段
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 站点生成器中查看页面或片段的版本历史记录，以及如何还原到旧版本。
author: phinneyridge
ms.date: 06/21/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: fa2ecdd9d9bc7e60b279d850573b5caa6df2c659
ms.sourcegitcommit: 9cfccb5c260ce56a3457f9ea12e80f54ea55a3b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183669"
---
# <a name="view-version-history-to-revert-pages-and-fragments"></a>查看版本历史记录以还原页面和片段

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

本文介绍如何在 Microsoft Dynamics 365 Commerce 站点生成器中查看页面或片段的版本历史记录，以及如何还原到旧版本。

Commerce 站点生成器可让您查看页面或片段的版本历史记录，并在需要时还原到文档的特定先前版本。 打开文档时，您可以在命令栏上选择 **显示历史记录**，以打开 **版本历史记录** 对话框（其中 **版本** 选项卡列出了所有版本的历史记录），并保存页面或片段的活动。 然后，您可以在列表中选择文档的先前版本，预览该文档并将其还原为当前版本。 对话框的 **活动** 选项卡列出了文档的完整活动历史记录，包括所有保存、发布和取消发布事件。

> [!NOTE]
> 每次站点作者进行更改，然后为文档选择 **完成编辑** 时，都会创建文档的新版本。 

若要查看页面或片段的版本历史记录并还原到以前的版本，请按照以下步骤操作。

1. 在站点生成器中，打开您要查看其版本历史记录的页面或片段。
1. 在命令栏中，选择 **显示历史记录**。

    ![显示历史记录按钮。](./media/version-history-1.png)

1. 在 **版本历史记录** 对话框中，在 **版本** 选项卡上，选择文档的先前版本。 右侧的属性窗格显示所选版本的缩略图预览，以及有关谁及何时修改了版本的信息。

    ![版本历史记录列表视图。](./media/version-history-2.png)

1. 若要查看所选文档版本的完全呈现预览，请选择 **预览**。 要关闭预览并返回 **版本历史记录** 对话框，请选择 **退出预览**。
1. 若要还原文档的先前版本，请在 **版本** 选项卡上的列表中选择它，然后选择 **还原**。 此时会显示 **还原版本 \<version number\>** 消息框，并提示您确认还原操作。 

    ![还原按钮和确认消息框。](./media/version-history-3.png)

1. 若要继续执行还原操作，请选择 **还原**。 站点生成器会刷新，并显示页面或片段的还原版本。
1. 要发布还原的页面，请选择 **完成编辑**，然后选择 **发布**。
