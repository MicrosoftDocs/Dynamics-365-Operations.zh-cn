---
title: 创建在线渠道和定义渠道属性
description: 此程序会逐步演示如何创建新的在线渠道，然后将其添加到组织层次结构。
author: jashanno
manager: AnnBe
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8e92e28c721692ed92fa931ed899c48678622349
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964783"
---
# <a name="create-online-channel-and-define-channel-attributes"></a>创建在线渠道和定义渠道属性

[!include [banner](../includes/banner.md)]

此程序会逐步演示如何创建新的在线渠道，然后将其添加到组织层次结构。 在创建新的在线渠道之前，您必须创建组织层次结构。 此程序使用 USRT 演示数据公司。


## <a name="create-a-new-online-channel"></a>创建新的在线渠道
1. 转至“Retail 和 Commerce”>“渠道”>“在线商店”。
2. 单击“新建”。
3. 在“名称”字段中，键入一个值。
4. 在“仓库”字段中，输入或选择一个值。
5. 在“商店时区”字段中，选择一个选项。
6. 在“默认客户”字段中，输入或选择一个值。
7. 在“客户通讯簿”字段中，输入或选择一个值。
8. 在“付款条款”字段中，输入或选择一个值。
9. 在“付款方式”字段中，输入或选择一个值。
10. 在“电子邮件通知配置文件”字段中，输入或选择一个值。
11. 扩展财务维度区段。
12. 在“业务单位”字段中，输入或选择一个值。
    * 同样设置所有其他默认维度的值。  
13. 单击“保存”。

## <a name="add-the-online-channel-to-organization-hierarchy"></a>将在线渠道添加到组织层次结构
1. 关闭该页面。
2. 转到“组织管理”>“组织”>“组织层次结构”。
3. 在列表中，找到并选择所需记录。
4. 单击“查看”。
5. 单击“编辑”。
    * 您可以选择您想要在其项下插入新渠道的任何层次结构节点。  
6. 单击“插入”。
7. 单击“商业渠道”。
8. 单击“确定”。
9. 单击“发布”以打开下拉对话框。
10. 在“有效日期”字段中输入日期和时间。
11. 单击“发布”。

## <a name="configure-orders-for-near-real-time-notification"></a>为订单配置近实时通知
1. 转到“Retail 和 Commerce”>“总部设置”>“参数”>“商业参数”。
2. 将“使用实时服务创建电子商务订单”设置为“是”。
3. 运行 1070 配送计划将更改同步到渠道数据库。 


