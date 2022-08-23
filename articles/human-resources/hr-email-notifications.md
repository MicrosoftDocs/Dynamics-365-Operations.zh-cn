---
title: 福利电子邮件通知
description: 本文提供 Microsoft Dynamics 365 Human Resources 中的福利管理电子邮件通知功能的概述。
author: twheeloc
ms.date: 08/01/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d550cbb2f639535dbb43765c9fb0632a514fbe8c
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229887"
---
# <a name="benefits-email-notification"></a>福利电子邮件通知

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [banner](../includes/preview-banner.md)]

电子邮件通知功能允许在以下情况下将电子邮件通知和提醒发送给员工：

- 新雇用登记
- 开放登记
- 符合条件的生活事件

您可以使用 **福利管理** 工作区和 **工作人员福利** 页面创建和设置多个电子邮件模板并发送通知。 您还可以跟踪通知/提醒历史记录。

## <a name="set-up-human-resources-shared-parameters"></a>设置人力资源共享参数

在 **人力资源共享参数** 页面上，您可以为发送给员工或员工组的不同类型的通信创建福利电子邮件模板。

## <a name="create-a-new-email-id-template"></a>创建新电子邮件 ID 模板

若要创建新电子邮件 ID 模板，请执行以下步骤。

1. 转到 **系统电子邮件模板**。
2. 选择 **新建**。
3. 在 **电子邮件 ID** 字段中，输入名称。
4. 根据需要设置其他字段。
5. 选择 **编辑消息** 以上传模板。
6. 在 **人力资源共享参数** 页面上，选择 **系统模板** 下面的新模板，然后将其移到 **福利模板** 下面。

## <a name="send-email-to-employees"></a>将电子邮件发送到员工

要向尚未开始工作的新雇员发送电子邮件，请按照以下步骤操作。

1. 打开 **福利管理** 工作区。
2. 选择要将电子邮件发送到的员工组的磁贴。
3. 选择 **发送电子邮件**。
4. 选择要将电子邮件发送到的员工。
5. 选择 **发送电子邮件**。
6. 选择要使用的模板。
7. 选择 **确定** 以发送电子邮件。

    您可以从员工的 **工作人员福利** 页面或通过在 **福利管理** 工作区的 **链接** 部分中选择 **福利电子邮件历史记录** 来查看电子邮件和状态。 您还可以从 **工作人员福利计划** 页面发送电子邮件。

8. 若要查看福利电子邮件历史记录，请在 **福利管理** 工作区内的 **链接** 部分中选择 **福利电子邮件历史记录**。
9. 查看已发送福利电子邮件的完整电子邮件历史记录。 若要查看电子邮件的内容，请选择 **显示消息**。
10. 选择 **工作人员**。
11. 在 **工作人员福利计划** 页面上，您可以发送电子邮件并查看福利电子邮件历史记录。

**福利管理** 工作区包含不同的磁贴。 您可以通过选择相关模板来发送电子邮件。 如果已发送新的雇用登记电子邮件，请选择 **新雇用未开始** 磁贴，然后选择 **发送提醒** 链接。 您可以选择提醒模板，并将通知的标题设置为第一个、第二个或第三个提醒。
