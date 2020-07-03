---
title: 确认、更新和发送项目报价单
description: 本主题提供有关向客户发送报价单以进行确认、基于反馈进行修改然后重新发送报价单的信息。
author: kfend
manager: AnnBe
ms.date: 05/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 7c2f7435ed63702dafb52b0eff57c0f174ff829e
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410196"
---
# <a name="confirm-update-and-send-a-project-quotation"></a>确认、更新和发送项目报价单

[!include [banner](../includes/banner.md)]

创建项目报价单并将其发送给客户之后，必须先从客户那里得到确认，然后才能将报价单状态更新为**已发送**。 客户要求的任何修改都可以在报价单中更新。 在您将报价单状态更新为**已发送**后，将无法再进行修改。 以下过程描述了以下选项：发送报价单以进行确认，基于反馈进行更新，然后发送报价单。

## <a name="send-a-project-quotation-confirmation"></a>发送项目报价单确认  

您可以通过电子邮件或作为打印副本发送现有项目报价单进行确认。 

1. 转到**项目管理与核算** > **报价单** > **项目报价单**。 
2. 在**项目报价单**页面上，选择要发送进行确认的报价单。 
3. 在**跟进**选项卡上，在**生成**组中，选择**确认**。 
4. 在**确认报价单**页面上，设置所需的参数。 例如，要打印确认，请在**打印**选项下，打开**打印确认**，然后选择**确定**。
5. 在**发送报价单**页面上，选择**选项**，在**打印目标设置**页面上，选择是要将报价单发送到**屏幕**、**电子邮件**、**文件**、**打印存档**还是**打印机**，然后在**说明**区域中进行所需的调整以传递报价单。
6. 在**打印目标设置**页面中，选择**确定**。  

## <a name="update-a-project-quotation"></a>更新项目报价单

要修改现有项目报价单，报价单状态必须为**已创建**。 完成以下步骤以更新现有报价单。 

1. 转到**项目管理与核算** > **报价单** > **项目报价单**。
2. 在**项目报价单**页面上，选择要更新的报价单，然后在操作窗格上选择**编辑**。
3. 更新必要的字段信息，然后在“操作窗格”上选择**保存**。  

## <a name="send-a-project-quotation-to-a-customer"></a>将项目报价单发送给客户 

1. 转到**项目管理与核算** > **报价单** > **项目报价单**，然后选择要发送的项目报价单。
2. 在**项目报价单**页面上的**报价**选项卡，在**流程**组中，选择**发送报价单**。 报价单状态将更新为**已发送**。

> [!NOTE]
> 状态更改为**已发送**后，您将无法修改项目报价单。
