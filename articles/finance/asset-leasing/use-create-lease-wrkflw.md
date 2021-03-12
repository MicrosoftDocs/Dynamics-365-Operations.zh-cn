---
title: 使用租赁审批工作流
description: 本主题说明如何使用工作流审批资产租赁，以及如何跟踪工作流的状态和历史记录。
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
ms.openlocfilehash: 1805e1f87ee70a1f35d9105b8f7ad6c95861efcc
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4440968"
---
# <a name="use-lease-approval-workflows"></a>使用租赁审批工作流

[!include [banner](../includes/banner.md)]

本主题说明如何使用工作流审批资产租赁，以及如何跟踪工作流的状态和历史记录。 工作流通过提供一组标准的审批步骤并分配审批流程的每个步骤的特定用户，帮助租赁审批的管理保持一致。 审批者可以批准租赁，拒绝租赁，申请更改租赁或将租赁分配给其他用户进行审批。 通过让您跟踪其状态和历史记录，工作流还可以提高审批过程的可见性。 此外，您还可以查看集中工作清单，该清单列出了分配给特定审核者的任务和审批。

在使用此过程之前，请确保至少已创建“租赁审批”工作流。 如果不存在工作流，请创建一个。 有关如何设置工作流的详细信息，请参阅[设置审批工作流](set-up-lease-wrkflw.md)。

1. 提交日记帐以供审核。 在租赁的 **帐簿详细资料** 页面，选择 **工作流**，然后选择 **提交**。
2. 在出现的对话框中，您可以添加注释。 指定的审批者将看到此注释以及租赁。 输入完注释后，选择 **提交**。 租赁已提交到工作流系统，审批者将接收以供审批。
3. 要查看指派给其审批的租赁，请转到 **模型 \> 通用 \> 工作项 \> 分配给我的工作项**。
4. 在 **分配给我的工作项** 页面上，选择要查看的租赁的 **租赁 ID**。 出现的页面取决于您可以访问的租赁帐簿和租赁详细信息。
5. 查看完租赁后，选择 **工作流**，并决定应采取的措施。 选项包括 **批准**、**拒绝**、**请求更改**、**委派** 和 **取消**。 您也可以选择 **查看历史记录** 查看所选租赁的审批历史记录。
6. 选择操作后，输入注释以描述该操作。 输入完注释后，选择列表中的 **已批准** 操作。
7. 要查看审批操作，请从 **租赁摘要** 页面返回到 **租赁详细信息** 页，然后选择 **工作流 \> 查看历史记录**。

    您可以在 **工作流历史记录** 页上查看工作流活动。 此页面显示已对特定租赁采取的工作流步骤。 您也可以使用 **工作项** 字段查看已分配工作项的状态。

8. 要停止工作流，请在 **工作流历史记录** 页面上，选择 **撤回**。 在显示的对话框中，选择一个注释，然后选择 **确定**。
9. 要停用工作流或激活先前创建的工作流，请转到 **资产租赁 \> 设置 \> 租赁工作流**。 然后，在 **租赁工作流** 页面上，选择 **工作流 \> 版本**。 要使当前工作流处于非活动状态，请在“租赁版本”对话框中选择活动的租赁，然后选择 **停用**。 要激活现有工作流，请选择工作流，然后选择 **激活**。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]