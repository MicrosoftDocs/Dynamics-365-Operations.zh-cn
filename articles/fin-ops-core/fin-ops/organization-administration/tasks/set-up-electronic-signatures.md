---
title: 设置电子签名
description: 使用该过程设置电子签名。
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysConfiguration, SIGParameters, SIGReasonCode, SIGProcSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be8d2c95b95be621c81d41fd98e5857caa8bbbcb
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981762"
---
# <a name="set-up-electronic-signatures"></a>设置电子签名

[!include [banner](../../includes/banner.md)]

使用该过程设置电子签名。 电子签名确认要启动或审核计算流程的人员的身份。 用于创建该过程的演示数据公司是 DAT。


## <a name="enable-the-electronic-signature-configuration-key"></a>启用“电子签名配置密钥”
1. 转到“系统管理”>“设置”>“允许”>“许可证配置”。
2. 在树形图中，展开“管理”。
    * 核实“电子签名”复选框是否已选中。  
    * 如果“电子签名”复选框未选中，您必须启用维护模式。 通过运行来自“生命周期服务”的维护作业，或通过在本地使用 Deployment.Setup 工具，可以在此环境下启用维护模式。  
3. 关闭该页面。

## <a name="set-up-electronic-signature-parameters"></a>设置电子签名参数
1. 转到“组织管理”>“设置”>“电子签名”>“电子签名参数”。
2. 单击“编辑”。
3. 在“通知”字段中，键入一个值。
    * 输入在请求签名时签名人将要收到的通知。 您可以输入任意文本。 一般此文本将告诉用户对文档进行电子签名意味着什么。  
    * 如果您想使用其他语言输入“通知”文本，请单击“翻译”按钮。  
4. 单击“保存”。
5. 关闭该页面。

## <a name="set-up-reason-codes-for-electronic-signatures"></a>设置电子签名的原因代码
1. 转到“组织管理”>“设置”>“电子签名”>“电子签名原因代码”。
2. 单击“新建”。
    * 在使用电子签名前必须设置原因代码。 对文档签名时需要有效的原因代码。     签名人选择指示电子签名用途的原因代码。 例如，原因代码可以用于指示合法性。  
3. 在“原因代码”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
    * 如果需要，输入其他原因代码。  
5. 单击“保存”。
6. 关闭该页面。

## <a name="require-electronic-signatures-for-existing-processes"></a>现有流程所需的电子签名
1. 转到“组织管理”>“设置”>“电子签名”>“电子签名要求”。
2. 在列表中，找到并选择所需记录。
    * 选择一个需要电子签名的流程。  
3. 选择或取消选择“所需的签名”复选框。
    * 对于需要电子签名的每一个流程，重复执行这些步骤。  
4. 单击“保存”。

## <a name="create-a-custom-requirement-for-electronic-signatures"></a>创建电子签名的自定义要求
1. 单击“新建”。
2. 选择或取消选择“所需的签名”复选框。
3. 在“名称”字段中，输入需要电子签名流程中适用的名称。
4. 在“表格名称”字段中，单击下拉按钮以打开查找。
5. 在列表中，查找并选择必须签名的数据将存储在其中的表格。
6. 在列表中，单击所选行中的链接。
7. 在“字段名称”字段中，单击下拉按钮以打开查找。
8. 在列表中，查找并选择您想要监控的表格中的字段。
9. 在列表中，单击所选行中的链接。
    * 指定何时需要签名。     如果当字段中的数据发生更改时需要签名，请选择“始终”。     如果仅在某些情况下需要签名，请选择“仅”。 如果您选择“仅”，您还必须选择以下选项之一：在插入记录时，在更新记录或删除记录时。  
10. 单击“保存”。
11. 关闭该页面。

