---
title: Invoice capture 解决方案概述
description: 本文提供有关 Invoice capture 解决方案的信息。
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76441220b93744527f412110db536601a2fa1dd9
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691140"
---
# <a name="invoice-capture-solution"></a>Invoice capture 解决方案

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

本文提供有关从数字发票图像自动创建供应商发票的 Invoice capture 解决方案的信息。

应付帐款 (AP) 部门管理和处理收到的货物和服务的发票。 AP 会计师出于以下原因验证供应商发票上的数据：

- 在期末结算期间需要调整或更正时避免额外的工作量
- 及时支付供应商发票，防止因错误或欺诈而造成财务损失

光学字符识别 (OCR) 在过去几年已被不同行业广泛使用。 现在将印刷文本数字化非常常见，这样可以对其进行电子编辑、搜索、更紧密地存储并可在线显示。 数字文本可用于认知计算、机器翻译、文本转语音、关键数据和文本挖掘等机器过程。

人工智能 (AI) 技术的发展使现代 OCR 解决方案能够读取来自不同供应商的不同发票格式，而无需太多人工干预。 越来越多的公司意识到他们可以通过自动化处理发票而不是手动处理来节省工作量，并提高准确性。

## <a name="system-landscape"></a>系统布局

下图显示了 Invoice capture 解决方案中的主要组件和步骤。

[![Invoice capture 解决方案中的组件和步骤。](./media/Invoice-capture2.png)](./media/Invoice-capture2.png)

## <a name="required-roles"></a>所需角色

下表显示了设置和使用 Invoice capture 解决方案所需的角色。

| 角色          | 变动 | 系统 | 角色名称 |
|---------------|---------|---------|-----------|
| 管理员 | <ul><li>在 Microsoft Power Platform 中设置环境。</li><li>在 Microsoft Power Platform 中部署解决方案。</li><li>设置 Dynamics 365 和 AI Builder 之间的连接。</li><li>设置 Azure Data Lake Storage 位置。</li></ul> | <ul><li>Dynamics 365</li><li>Microsoft Power Platform</li><li>Azure Data Lake Storage</li></ul> | <ul><li>Dynamics 365 管理员</li><li>Power Platform 管理员</li><li>存储 Blob 数据负责人</li></ul> |
| AI 开发者      | <ul><li>维护流。</li><li>创建自定义 AI 模型。</li></ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>平民开发者</li></ul> |
| AP 职员      | <ul><li>在供应商发票暂存区域查看和执行操作。</li><ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Power Platform 中的新 AP 职员角色</li></ul> |
| AP 职员      | <ul><li>作为 AP 职员执行日常操作。</li><li>导航到供应商发票暂存区域。</li></ul> | <ul><li>Dynamics 365</li></ul> | <ul><li>应付帐款员</li></ul> |
  
有关安装 Invoice capture 的更多信息，请参阅[安装 Invoice capture](../accounts-payable/install-invoice-capture.md)。  
