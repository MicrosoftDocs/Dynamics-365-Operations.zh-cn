---
title: 查看工作流历史记录
description: 本主题介绍用于查看提交给工作流系统进行处理和审核的单据的状态的步骤。
author: jasongre
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0410e8cad5d18c3c8efd96d065967515a657f7edbd0256d148cdb6c6d0b7df41
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749404"
---
# <a name="view-workflow-history"></a>查看工作流历史记录

[!include [banner](../../includes/banner.md)]

本主题介绍用于查看提交给工作流系统进行处理和审核的单据的状态的步骤。 创建此程序的演示数据公司是 USMF。

1. 转到 **导航窗格 > 模块 > 常用 > 查询 > 工作流 > 工作流历史记录**。
    - 使用此窗体可以查看提交给工作流系统进行处理和审核的单据的状态。  
    - **实例 ID** 是正在处理或已经处理单据的工作流实例的标识代码。  
    - **状态** 是单据的工作流状态。  
    - **工作流 ID** 是正在处理或已经处理单据的工作流的标识代码。  
    - **单据** 是单据的标识代码。  
    - **单据类型** 是提交以处理的单据的类型。  
    - **工作流** 是正在处理或已经处理单据的工作流的名称。  
    - **版本** 是正在处理或已经处理单据的工作流的版本号。  
    - **创建日期和时间** 是是提交单据的日期和时间。  
    - **占用时间** 是自单据提交后经过的时间。  
    - 可通过 **恢复** 按钮恢复所选单据的工作流。  
    - 可通过 **撤消** 按钮撤消所选单据，以便不处理该单据。   
2. 在列表中，选择所需行中的链接。
    - 确保已展开 **工作项** 部分。 在此部分中，可以查看与所选单据关联的工作项。 例如，可能必须完成某项任务，或者可能必须审核单据。  
    - **重新分配** 按钮将打开一个对话框，从中可向其他用户重新分配工作项。  
    - 确保已展开 **跟踪详细信息** 部分。 在此部分中，可以查看所选单据的工作流历史记录。  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]