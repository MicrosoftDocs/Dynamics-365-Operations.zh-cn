---
title: 设置租赁审批工作流
description: 该主题说明如何设置在创建新租赁时将运行的审批工作流。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 58c0fd781710b7ab8efeaa7a6874f412279a5924
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4440942"
---
# <a name="set-up-lease-approval-workflows"></a>设置租赁审批工作流

[!include [banner](../includes/banner.md)]

该主题说明如何设置在创建新租赁时将运行的审批工作流。 有关如何使用此工作流的详细信息，请参阅[使用审批工作流](use-create-lease-wrkflw.md)。 

1. 转到 **资产租赁 \> 设置 \> 租赁工作流**。
2. 在 **租赁工作流** 页面上，选择 **新建**。
3. 在出现的对话框中 **工作流类型** 下，选择 **租赁工作流** 链接。

    将打开该应用程序。 运行后，登录到要重定向到工作流应用程序的 Azure Active Directory (Azure AD)。

4. 将 **租赁工作流审批** 元素添加到工作流中。
5. 将一个节点从 **开始** 连接到 **租赁工作流审批**。 然后将 **租赁工作流审批** 连接到 **结束**。
6. 双击 **租赁工作流审批**。
7. 选择 **属性**，然后在 **基本设置** 下输入工作流的名称。

    在此页面上，您还可以为工作流设置更多参数。 如果您已开启 **自动操作**，系统将自动执行特定操作。 如果在 **通知** 选项卡上指定了通知，则可以发送通知。在 **高级设置** 选项卡中，您可以指定最终审批者，设置时间限制，以及指定必须完成的特定操作。

8. 完成工作流参数的设置后，请选择 **关闭**。
9. 选择 **步骤 1**，然后选择 **属性**。
10. 在 **基本设置** 下，输入步骤的名称，为审批创建主题行，然后指定审批说明。
11. 在 **分配** 页面上，选择分配类型。
12. 要为审批分配特定用户，请选择 **用户**，选择审批租赁的用户，然后选择 **关闭**。
13. 选择 **保存并关闭** 以创建工作流。 然后，在系统提示时，选择 **确定**。
14. 在 **创建工作流** 页面上，选择 **关闭**。
14. 选择新工作流，然后选择 **版本号**。 然后选择 **激活** 以确保工作流处于活动状态。
15. 选择 **关闭**。 将显示新的活动版本。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]