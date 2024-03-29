---
title: 根据前一个问题的回答设定问题依赖项
description: 有条件问题允许您根据前一问题的回答，指定向回答者显示哪些后续问题。
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2f7d55b577478f3156a8299fc2f827ab3bb60f1
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686071"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>根据前一个问题的回答设定问题依赖项


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



有条件问题允许您根据前一问题的回答，指定向回答者显示哪些后续问题。 例如，如果您提问“您喜欢喝咖啡还是茶”，可以根据回答者选择的是咖啡还是茶来确定逻辑后续问题。 创建此程序的演示数据公司是 USMF。


## <a name="find-the-existing-questionnaire"></a>找到现有的调查表
1. 转到 **调查表** > **设计** > **调查表**。
2. 在列表中，选择 WorkFH 调查表。

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a>添加所有问题和子问题到调查表中
1. 单击 **问题**。
2. 单击 **新建**。
3. 在 **问题** 字段中，选择问题编号 00016。
4. 在列表中，找到并选择所需记录。
5. 在列表中，单击所选行中的链接。
6. 单击 **保存**。
7. 关闭该页面。

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a>设置有条件问题的调查表顺序，并使问题依赖于相应问题
1. 单击 **编辑**。
2. 展开 **设置** 部分。
3. 在 **问题顺序** 字段中，选择“有条件”。
4. 单击 **有条件** 问题。
5. 在树结构中，选择“问题\说明为什么以这种方式回答前一问题”。
6. 在 **主要问题** 字段中，选择问题编号 00009。
7. 在列表中，单击所选行中的链接。
8. 在 **回答** 字段中，输入您所希望的依赖项的回答选项的序列 ID。 例如，在第一个回答选项中输入 1。
9. 单击 **保存**。
10. 在树结构中，选择“问题\我获得公平的工作报酬”。
    * 请注意，问题树已更新以显示差异。  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
