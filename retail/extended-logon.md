---
title: "云和 POS 的安装端登录扩展的功能"
description: "此 wiki 介绍设置 Cloud POS 和 Retail Modern POS (MPOS) 扩展登录的选项。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 0dc80784a5c9a7de6009826284cb68f1aee83f70
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-extended-logon-functionality-for-cloud-pos-and-mpos"></a>云和 POS 的安装端登录扩展的功能

此 wiki 介绍设置 Cloud POS 和 Retail Modern POS (MPOS) 扩展登录的选项。

<a name="setting-up-extended-logon"></a>设置扩展登录
=========================

您可以查找条码掩码的设置在**零售和商务** &gt; **的设置渠道** &gt; **的设置 POS ** &gt; ** POS 模板** &gt; ** **功能配置文件。 **功能**快速选项卡包括与扩展登录有关的以下选项。

### <a name="staff-bar-code-logon"></a>职员条码登录

在**职员条码登录**选项启用时，将扩展登录分配到销售点 (POS) 凭据的工作人员可以使用条码登录。

### <a name="staff-bar-code-logon-requires-password"></a>职员条码登录需要密码

在**职员条码登录需要密码**选项启用时，职员条码登录只选择分配给存在的扩展登录的工作人员。 在此选项启用时，工作人员仍必须输入密码。

### <a name="staff-card-logon"></a>职员卡登录

在**职员卡登录**选项启用时，将扩展登录分配到 POS 凭据的工作人员可以使用磁条登录。

### <a name="staff-card-logon-requires-password"></a>职员卡登录需要密码

在**职员卡登录需要密码**选项启用时，职员卡码登录只选择分配给存在的扩展登录的工作人员。 在此选项启用时，工作人员仍必须输入密码。

<a name="assigning-an-extended-logon"></a>分配扩展登录
===========================

默认情况下，只有经理可以将扩展登录分配给工作人员。 若要分配扩展的登录到，请对**扩展的登录**在 POS。 多个工作的人员通过搜索为它们输入在搜索字段来的操作员 ID。 选择工作人员，然后单击**分配**。 在下一个页面，刷卡或扫描扩展登录以分配给工作人员。 如果成功读取刷卡或扫描，**确定**按钮将可用。 单击**确定**为该工作人员保存扩展登录。

<a name="deleting-an-extended-logon"></a>删除扩展登录
==========================

若要删除分配给工作人员的扩展登录，使用**扩展登录**操作搜索工作人员。 选择工作人员，然后单击**取消分配**。 与该工作人员关联的所有扩展登录凭据将被删除。

<a name="extending-extended-logon"></a>扩展扩展登录
========================

登录服务可扩展以支持其他扩展登录设备，例如掌上扫描仪。 有关详细信息，请参阅 POS 可扩展性文档。

<a name="using-extended-logon"></a>使用扩展登录
====================

在配置扩展登录时，并且工作人员已被分配了条码或磁条，在 POS 登录页显示时，工作人员必须刷或扫描他或她的卡。 如果还需要密码才能继续登录，系统将提示工作人员输入他或她的密码。


