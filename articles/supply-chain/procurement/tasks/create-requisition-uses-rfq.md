---
title: 创建使用询价的申请
description: 此主题介绍如何将价格和供应商信息添加到询价流程的采购申请。
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6083afe0e2bfafd337d572863a198330e8cb6cc8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812125"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a>创建使用询价的申请

[!include [banner](../../includes/banner.md)]

此主题介绍如何将价格和供应商信息添加到询价流程的采购申请。 可以在 USMF 演示数据公司中使用此指南中显示的示例，并且必须以 Admin 身份登录才能完成所有任务。 此指南中的任务通常由采购专业人员完成。


## <a name="create-a-requisition"></a>创建申请
1. 在导航窗格中，转到 **模块 > 采购 > 采购申请 > 由我准备的采购申请**。
2. 选择 **新建**。
3. 在 **名称** 字段中，键入一个值。
4. 在 **请求日期** 字段中，输入一个日期。
5. 在 **会计结算日期** 字段中，输入一个日期。
6. 选择 **确定**。
7. 在 **原因** 字段中，输入或选择一个值。
8. 选择 **添加行**。
9. 在 **采购类别** 字段中，选择树中的类别，然后选择 **确定**。
10. 在 **产品名称** 字段中，键入一个值。
11. 在 **数量** 字段中，输入一个数字。
12. 在 **单位** 字段中，输入或选择一个值。
13. 选择 **保存**。
14. 选择 **工作流** 以打开下拉对话框。
15. 选择 **提交**。
16. 关闭该页面。
17. 选择 **提交**。

## <a name="reassign-a-workflow-task"></a>为工作流重新分配任务
下一项任务是创建询价以获取供应商对产品的出价。 在 USMF 演示数据中，为申请工作流设置了规则，以便在未选择供应商或某行的单价为 0 时，为特定工作人员分配任务以创建询价。 要继续完成此指南，需要将该任务重新分配给其他用户（您自己）。 仅当您以 Admin 身份登录时，才能执行此操作。  

1. 选择 **工作流** 以打开下拉对话框。
2. 选择 **查看历史记录**。
3. 刷新该页面。
4. 展开 **跟踪详细信息** 部分。
5. 在树中，请选择以“行工作流启用于”开始的行。
6. 选择 **查看工作流详细信息**。
7. 展开 **工作项** 部分。
8. 选择 **重新分配**。
9. 在 **用户** 字段中，选择 **Admin**。
10. 选择 **重新分配**。
11. 关闭这两个页面。

## <a name="create-an-rfq"></a>创建询价

1. 刷新该页面。
2. 选择 **询价**。
3. 在 **购买法人** 字段中，选择 **USMF**。 必须选择位于申请行中的同一个法人。  
4. 在列表中，标记所选的行。 如果采购申请中有多行，请选择要添加到询价的所有行。  
5. 选择 **确定**。
6. 刷新该页面。
7. 确保此速见表已打开，然后展开 **相关单据** 部分。
8. 选择 **询价** 字段中的链接打开刚才创建的询价。
9. 选择 **标题**。
10. 选择 **添加**。
11. 在 **供应商帐户** 字段中，输入或选择一个值。
12. 选择 **添加**。
13. 在 **供应商帐户** 字段中，输入或选择一个值。
14. 选择 **发送**。
15. 选择 **确定**。
16. 选择 **输入回复**。
17. 在操作窗格上，选择 **回复**。
18. 选择 **将数据复制到回复**。 这将把数量和日期之类数据从询价复制到回复。  
19. 在 **单价** 字段中，输入一个数字。 这是您从供应商处收到的价格。 您可能还希望输入供应商提供的其他信息。  
20. 选择 **接受**。
21. 选择 **确定**。

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>验证是否已将供应商和价格转移到申请
1. 关闭该页面。
2. 选择 **行**。
3. 选择 **相关信息**。
4. 选择 **采购申请**。
5. 选择已转移到询价的行。 验证是否已将价格和供应商复制到申请。  
6. 选择 **工作流** 以打开下拉对话框。
7. 选择“完成”。
8. 选择此页面。
9. 选择“完成”。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]