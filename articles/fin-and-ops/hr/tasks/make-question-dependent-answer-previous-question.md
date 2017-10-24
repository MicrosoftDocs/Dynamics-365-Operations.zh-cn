--- 
title: "根据前一个问题的回答设定问题依赖项"
description: "有条件问题允许您根据前一问题的回答，指定向回答者显示哪些后续问题。"
author: twheeloc
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 05f7af94813934c1d77d6a509587280395f0e8bd
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>根据前一个问题的回答设定问题依赖项

[!include[task guide banner](../../includes/task-guide-banner.md)]

有条件问题允许您根据前一问题的回答，指定向回答者显示哪些后续问题。 例如，如果您提问“您喜欢喝咖啡还是茶”，可以根据回答者选择的是咖啡还是茶来确定逻辑后续问题。 创建此程序的演示数据公司是 USMF。


## <a name="find-the-existing-questionnaire"></a>找到现有的调查表
1. 转到“调查表”>“设计”>“调查表”。
2. 在列表中，选择 WorkFH 调查表。

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a>添加所有问题和子问题到调查表中
1. 单击问题。
2. 单击“新建”。
3. 在“问题”字段中，选择问题编号 00016。
4. 在列表中，找到并选择所需记录。
5. 在列表中，单击所选行中的链接。
6. 单击“保存”。
7. 关闭该页面。

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a>设置有条件问题的调查表顺序，并使问题依赖于相应问题
1. 单击“编辑”。
2. 展开“设置”部分。
3. 在“问题顺序”字段中，选择“有条件”。
4. 单击“有条件问题”。
5. 在树结构中，选择“问题\说明为什么以这种方式回答前一问题”。
6. 在“主要问题”字段中，选择问题编号 00009
7. 在列表中，单击所选行中的链接。
8. 在“回答”字段中，输入您所希望的依赖项的回答选项的序列 ID。 例如，在第一个回答选项中输入 1。
9. 单击“保存”。
10. 在树结构中，选择“问题\我获得公平的工作报酬”。
    * 请注意，问题树已更新以显示差异。  


