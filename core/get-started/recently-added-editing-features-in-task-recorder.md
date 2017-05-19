---
title: "任务录制器中最近增加的编辑功能"
description: "如果您使用任务录制器创建任务指南，您可以使用此主题中介绍的内容提高此功能的使用效率。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core
ms.custom: 266464
ms.assetid: b4640e67-4b92-4855-8041-1bfc71aadc47
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 3be54879494948f75b192fcc22239b9064173220
ms.contentlocale: zh-cn
ms.lasthandoff: 04/25/2017


---

# <a name="recently-added-editing-features-in-task-recorder"></a>任务录制器中最近增加的编辑功能

[!include[banner](../includes/banner.md)]


如果您使用任务录制器创建任务指南，您可以使用此主题中介绍的内容提高此功能的使用效率。

这些功能位于**设置 &gt; 任务录制器 &gt; 编辑录制**菜单中。

-   插入步骤但不重新录制整个文件。
-   在子任务下移动步骤但不重新录制整个文件。
-   折叠录制名称和描述字段。

## <a name="insert-steps-without-rerecording-the-entire-file"></a>插入步骤但不重新录制整个文件
现在可以在任务指南中的任何位置添加步骤，但不播放或重新录制整个文件。

1.  选择要在其后插入新步骤的步骤。 确定该步骤已突出显示。

必须打开正确的页面，任务录制器才能插入步骤。 正确页面是执行新步骤的页面。 任务录制器有一种新机制，可确定哪个页面是活动页面，并在未打开正确页面时禁用此功能。 

[![tg1](./media/tg1.png)](./media/tg1.png) 


在正确页面中后，**插入步骤**将变为可用。

[![tg2](./media/tg2-231x300.png)](./media/tg2.png)

2. 单击**插入步骤**。

单击**插入步骤**时，任务录制器将切换为录制模式。 将录制 UI 中执行的任何操作并按原状添加为步骤。

3. 单击**停止**。

可以重复此过程，根据需要添加任意数量的步骤或移动任意数量的子任务（有关子任务，请参见下文）。

4. 编辑完任务指南之后，单击**完成编辑**，然后选择一个选项保存或发布任务指南。

## <a name="move-steps-under-a-subtask-without-rerecording-the-entire-file"></a>在子任务下移动步骤但不重新录制整个文件
可以在子任务下移动步骤但不播放或重新录制整个文件。 如果希望为现有步骤块分组，也可以移动子任务步骤或结束子任务步骤。

1.  选择要移动的步骤或子任务步骤。 确定该步骤已突出显示。
2.  单击省略号，然后单击**将步骤移到以下项目后面**。

[![tg3](./media/tg3.png)](./media/tg3.png)

3. 选择要将步骤或子任务步骤移动到其后的步骤或子任务步骤。 任务录制器将移动步骤。

4. 若要移动结束子任务步骤，将其选中，单击省略号，单击**将步骤移到以下项目后面**，然后选择要将结束子任务步骤移到其后的步骤。

如果要让任务指南中的第一个步骤在子任务内，请创建一个子任务步骤充当第二个步骤，然后将第一个步骤移动到这个步骤中。 可以根据需要添加或移动任意数量的步骤或子任务。

5. 编辑完任务指南之后，单击**完成编辑**，然后选择一个选项保存或发布任务指南。

## <a name="collapse-recording-name-and-description"></a>折叠录制名称和描述
可以展开和折叠**录制名称**合**录制描述**字段。 当这些字段折叠后，任务录制器编辑窗格中将显示更多步骤。 

[![tg4](./media/tg4-300x252.png)](./media/tg4.png)  

<a name="see-also"></a>请参阅
--------

[使用任务录制创建文档或培训](/dynamics365/operations/dev-itpro/user-interface/task-recorder)

[任务录制器快速参考](/dynamics365/operations/dev-itpro/user-interface/task-recorder-quick-reference)




