---
title: 客户工作流
description: 本主题提供有关客户工作流的信息。 您更改客户的特定字段，然后在将字段添加到客户前使用工作流发送这些更改进行审核。
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: af66887dda551d3820b744fbb96d7d13c897e71b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236882"
---
# <a name="customer-workflow"></a>客户工作流

[!include [banner](../includes/banner.md)]

客户工作流已添加至版本 8.0.4。 您可以更改客户的特定字段，然后在将字段添加到客户前使用工作流发送这些更改进行审核。

## <a name="set-up-the-customer-workflow"></a>设置客户工作流

在使用客户工作流功能之前，您必须先启用。

1. 转至 **应收帐款 \> 设置 \> 应收帐款参数**。
2. 在 **常规** 选项卡上，在 **客户审核** 快速选项卡上，将 **启用客户审核** 选项设置为 **是** 来启用此功能。
3. 在 **数据实体行为** 字段中，选择导入数据时数据实体应使用的行为：

    - **允许在不审核的情况下进行更改** - 实体可以通过工作流在不处理客户记录的情况下更新记录。
    - **拒绝更改** - 不能对客户记录进行更改。 导入为工作流启用的字段将失败。
    - **创建更改方案** - 除为工作流启用的字段外，所有字段都会被更改。 这些字段的新值将作为建议的更改添加到客户，工作流将自动开始。

4. 在客户字段列表中，选择在进行更改前必须审核的每个字段的 **启用** 复选框。
5. 转至 **应收帐款 \> 设置 \> 应收帐款工作流**。
6. 选择 **新建**。
7. 选择 **建议的客户更改工作流**。 
8. 设置工作流，使其与您的审核流程匹配。 **建议的客户更改的工作流审核** 工作流审核元素将更改应用于客户。

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a>更改客户信息并向工作流提交更改

在更改为工作流启用的字段时，**建议的更改** 页面会显示。 此页面显示字段的原始值和您输入的新值。 您更改的字段还原为原始值。 页面上的状态消息通知您更改尚未提交。

每次更改为工作流启用的字段时，该字段将添加到建议的更改列表中。 若要放弃字段的建议值，使用列表中字段旁边的 **放弃** 按钮。 若要放弃所有更改，使用页面底部的 **放弃所有更改** 按钮。 选择 **确定** 关闭页面。

在您至少有一项建议的更改后，操作窗格上将另外出现两个菜单：**建议的更改** 和 **工作流**。

1. 选择 **建议的更改** 打开 **建议的更改** 页面并查看您的更改。
2. 选择 **工作流 \> 提交** 将更改提交到工作流。

    页面上的状态将更改为 **更改待审核**。

工作流执行应用程序中的标准工作流程。 审核人被定向到 **客户** 页面，并且可在此处的 **建议的更改** 页面上查看更改，然后选择 **工作流 \> 审核** 以审核工作流。 在完成所有审核后，字段将更新为您建议的值。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]