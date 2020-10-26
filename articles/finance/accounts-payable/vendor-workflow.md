---
title: 供应商工作流
description: 修改供应商信息和使用工作流进行审核。
author: mikefalkner
manager: annbe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 55ae179298a980073a03a804711707a1f02c68bd
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977975"
---
# <a name="vendor-workflow"></a>供应商工作流

[!include [banner](../includes/banner.md)]

如果使用供应商工作流，将先把对特定字段进行的更改发送到工作流进行审核，之后才能将其添加到供应商。

## <a name="set-up-the-vendor-workflow"></a>设置供应商工作流

此工作流功能必须经过启用才能使用。

1. 转到**应付帐款 \>设置 \> 应付帐款参数**。
2. 在**常规**选项卡的**供应商审核**快速选项卡上，将**启用供应商审核**选项设置为**是**。
3. 在**数据实体行为**字段中，选择应在导入字段时使用的行为：

    - **允许在不审核的情况下进行更改** – 此数据实体可以在不通过工作流进行处理的情况下更新供应商记录。
    - **拒绝更改** – 不能对供应商记录进行更改。 为工作流启用的字段的导入将失败。
    - **创建更改方案** – 将更改除为工作流启用的字段以外的所有字段。 将把这些字段的新值作为建议的更改添加到供应商，并自动启动工作流。

4. 在供应商字段列表中，选中进行更改前必须先批准的每个字段的**启用**复选框。
5. 转到**应付帐款 \>设置 \> 应付帐款工作流**。
6. 选择**新建**。
7. 选择**建议的供应商更改工作流**。 
8. 设置工作流，使其与您的审核流程匹配。 **建议的供应商更改的工作流审核**工作流审核元素将应用对供应商的更改。

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a>更改供应商信息并将更改提交给工作流

更改为工作流启用的字段时，将显示**建议的更改**页。 此页面显示字段的原始值和您输入的新值。 将把您更改的字段恢复为原始值。 还会通过状态消息告知您尚未提交您的更改。 

只要更改了为工作流启用的字段，都将把该字段添加到**建议的更改**页上的列表中。 若要放弃字段的建议值，请使用列表中该字段旁边的**放弃**按钮。 若要放弃所有更改，请使用页面底部的**放弃所有更改**按钮。 选择**确定**关闭页面。

至少执行一项建议的更改之后，操作窗格中将显示两个额外的选项卡：**建议的更改**和**工作流**。

1. 选择 **建议的更改**打开**建议的更改** 页并查看您的更改。
2. 选择**工作流 \> 提交**以提交对工作流的更改。

    页面上的状态将更改为**更改待审核**。

工作流执行标准工作流程。 将把审核者定向到**供应商**页面，可在此处查看**建议的更改**页中的更改，然后选择**工作流 \> 审核**以审核工作流。 在完成所有审核后，字段将更新为您建议的值。
