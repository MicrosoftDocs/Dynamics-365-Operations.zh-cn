---
title: 服务协议和项目的集成
description: 在您处理服务协议和服务协议行时，使用在“项目管理与核算”中的区域中设置的数据。
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 77b61c0b9d48557e25ec5aec43dd6546605d35b6fa2ac810d55b3333a8f00289
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720149"
---
# <a name="integration-for-service-agreements-and-projects"></a>服务协议和项目的集成 

[!include [banner](../includes/banner.md)]


在您处理服务协议和服务协议行时，使用在 **项目管理与核算** 中的以下区域中设置的数据。

## <a name="project-prices"></a>项目价格

服务协议交易记录的成本和销售价从应用于附加到该服务协议的项目的成本价设置派生。 可以按项目、员工和类别设置成本价和销售价。 

## <a name="project-validation"></a>项目验证

可通过 **项目管理与核算** 中的验证设置，限制可用于服务协议行上选定内容的项目、员工和类别。 使用验证设置，您可以将员工、项目和类别结合起来用于控制访问。 

## <a name="project-line-properties"></a>项目行属性

为服务协议行自动输入记录属性。

行属性在 **项目管理与核算** 中的 **行属性** 窗体中创建。 记录属性在“”的“”窗体中创建，在某一服务协议上输入的记录属性将附加到为该服务协议选择的项目，并且该记录属性以后将由服务协议行继承。 

## <a name="default-offset-accounts"></a>默认对方科目

如果您输入某一支出交易记录，则自动为该交易记录选择默认的支出对方科目。 针对附加到当前服务协议的项目设置默认的支出帐户。

## <a name="project-categories"></a>项目类别

可用于服务协议行的类别在 **项目管理与核算** 中的 **项目类别** 窗体中设置。 

> [!NOTE]
> <P>在<STRONG>项目类别</STRONG>窗体<STRONG>项目</STRONG>选项卡中选中了<STRONG>在日记帐中有效</STRONG>复选框的类别可供选择。 但是，如果选中了<STRONG>项目管理与核算参数</STRONG>窗体<STRONG>日记帐</STRONG>选项卡中的<STRONG>无效类别</STRONG>复选框，则所有类别均可供选择。</P>

## <a name="project-parameters"></a>项目参数

如果选中了 **项目管理与核算参数** 窗体 **日记帐** 选项卡中的 **已离职工作人员** 字段，则可在 **服务协议** 和 **服务订单** 窗体中选择已离职员工和有效员工。

此外，您可以在 **服务订单** 中的 **项目** 选项卡上启用 **开始时间** 和 **结束时间** 字段，以便针对服务订单行输入开始时间和结束时间。

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a>启用服务订单的开始和结束时间功能

1.  单击 **项目管理与核算** \> **设置** \> **项目管理与核算参数**。

2.  单击 **日记帐** 选项卡，然后选中 **显示开始/结束时间** 复选框。

3.  单击 **项目管理与核算** \> **设置** \> **日记帐** \> **日记帐名称**。

4.  选择附加到该服务订单的日志名称。

5.  单击 **常规** 选项卡，然后选中 **显示开始/结束时间** 复选框。


> [!NOTE]
> <P>在<STRONG>服务管理参数</STRONG>窗体<STRONG>日记帐</STRONG>选项卡上的<STRONG>工时</STRONG>字段中，为该服务订单选择日志名称。</P>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]