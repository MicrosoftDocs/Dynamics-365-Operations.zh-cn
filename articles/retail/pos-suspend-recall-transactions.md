---
title: 暂停和恢复销售点 (POS) 的交易
description: 本主题说明用户如何使用 Microsoft Dynamics 365 for Retail 暂停正在进行的交易，然后在以后或在其他收银机上恢复交易。
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ffb04609318c7de4b9ef729a8e03a7f9395806b8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569536"
---
# <a name="suspend-and-resume-transactions-in-the-point-of-sale-pos"></a>暂停和恢复销售点 (POS) 的交易

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

销售点 (POS) 用户可以暂停正在进行的交易，然后在以后或在其他收银机上恢复交易。 暂停交易通常是为了快速释放收银机以处理其他任务，而不会丢失当前交易的任何进度。 例如，售货员开始在移动设备上处理客户交易，但必须先在具有银箱的收银机上完成此交易。 在这种情况下，售货员可以暂停移动设备上的交易，然后在收银机上撤回和恢复交易。

## <a name="configure-suspend-and-resume-functionality"></a>配置暂停和恢复功能

### <a name="pos-operations"></a>POS 操作

两个 [POS 操作](pos-operations.md)允许 POS 支持暂停和恢复方案。 您可以在交易记录页面或欢迎页面将这些操作分配到[按钮网格](pos-screen-layouts.md)。

- 503：暂停交易
- 504：撤回交易

### <a name="receipt-template"></a>收据模板

POS 可以配置为在暂停交易时生成打印单。 该单以后可以用于快速识别和撤销交易。

若要支持 POS 打印清单，您必须将**暂停交易**收据格式添加到商店的收据模板。 您可以设计收据格式，使其包括或排除有关交易的具体详细信息。 例如，格式可以包括支持扫描的条码。

### <a name="receipt-numbering"></a>收据编号

对于生成打印收据的其他 POS 交易类型，您可以在商店的功能配置文件的**收据编号**部分为暂停交易定义编号规则。

### <a name="void-when-closing-shift"></a>在结束班次时失效

您可以使用**在结束班次时失效**选项要求用户在结束其班次前完成或取消任何暂停交易。 在执行**结束班次**操作期间，POS 将提示用户查看或取消所有未清的暂停交易。

## <a name="suspend-and-resume-a-transaction"></a>暂停和恢复交易

### <a name="suspend-a-transaction"></a>暂停交易

具有足够权限并且具有包含**暂停交易**操作的屏幕布局的用户，可以暂停交易，以便交易可以在以后或在其他收银机上撤销。

只有当交易**不**包含以下行类型时交易才可以被暂停：

- 有效付款行
- 礼品卡行（签发礼品卡或添加到礼品卡余额）

暂停交易不会影响商店的销售信息或库存现有量信息。

### <a name="resume-a-suspended-transaction"></a>恢复暂停交易

暂停交易可以在同一商店内由具有足够权限，并且还具有包含**撤销交易**操作的布局的任何用户撤销和恢复。

若要快速轻松地撤销暂停交易，在您查看**撤销交易**操作的交易列表时扫描打印单上的条码。

### <a name="considerations-for-offline-mode"></a>脱机模式的注意事项

- 在 POS 处于联机模式时暂停的任何交易都不能在脱机模式下恢复，因为数据不同步到脱机数据库。
- 如果您在 POS 处于脱机模式时暂停交易，您可以在脱机模式下撤销它，前提是从您暂停交易起，POS 未在任何时间切换回联机模式。 在 POS 切换回脱机模式后，暂停交易的相关数据将移到脱机数据库，并被从联机数据库中删除。 因此，交易只能在脱机模式下恢复。 如果您将 POS 切换回脱机模式，您将无法恢复暂停交易，因为它们已被从脱机数据库中删除。

### <a name="void-a-suspended-transaction"></a>取消暂停交易

您可以通过撤销交易然后执行**取消交易**操作来取消暂停交易，或者通过选择**撤销交易**列表中的交易并选择应用栏上的**取消**来取消。 或者，可以将商店配置为提示用户在结束班次时取消暂停交易。
