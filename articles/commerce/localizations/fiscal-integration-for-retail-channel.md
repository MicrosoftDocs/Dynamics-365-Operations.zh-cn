---
title: 商业渠道的会计整合概览
description: 此主题提供 Dynamics 365 Commerce 中可用的会计整合功能的概览。
author: josaw
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2019-1-16
ms.dyn365.ops.version: 10
ms.openlocfilehash: 155056eb3a2acd0d66e0ace8d5558929678cb8e3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798773"
---
# <a name="overview-of-fiscal-integration-for-commerce-channels"></a>商业渠道的会计整合概览

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>简介

此主题是 Dynamics 365 Commerce 中可用的会计整合功能的概览。 会计整合包括与不同会计设备和服务的集成，这些设备和服务支持依据旨在防止零售行业的税收欺诈的地方政法进行销售的会计登记。 以下是可以使用会计整合应对的一些典型场景：

- 在连接到销售点 (POS) 的会计设备（如税控打印机）上登记销售，以及为客户打印财务收据。
- 安全地向税务主管机构管理的外部 Web 服务提交与在 Retail POS 完成的销售和退货相关的信息。
- 通过数字签名帮助确保销售交易数据的不变性。

会计整合功能是一个框架，为进一步开发和自定义 Retail POS 与会计设备和服务之间的整合提供通用解决方案。 此功能还包括支持特定国家或地区的基本方案，以及使用特定会计设备或服务的会计整合示例。 会计整合示例由若干 Commerce 组件的扩展组成，包含在软件开发套件 (SDK) 中。 有关会计整合示例的详细信息，请参阅 [Retail SDK 中的会计整合示例](#fiscal-integration-samples-in-the-retail-sdk)。 有关如何安装和使用 Retail SDK 的信息，请参阅 [Retail 软件开发套件 (SDK) 体系结构](../dev-itpro/retail-sdk/retail-sdk-overview.md)。

为了支持会计整合示例不支持的其他方案，将 Retail POS 与其他会计设备或服务整合，或者满足其他国家或地区的要求，您必须扩展用现有的会计整合示例或将现有示例用作范例创建新示例。

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices"></a>会计设备的会计登记流程和会计整合示例

Retail POS 中的会计登记流程可以包含一个或多个步骤。 每个步骤涉及一个会计设备或服务的特定交易或事件的会计登记。 以下解决方案组件参与连接到硬件工作站的会计设备上的会计登记：

- **Commerce Runtime (CRT) 扩展** – 此组件序列化同时用于与会计设备交互的格式的交易/事件数据，分析来自会计设备的回应，并在通道数据库中存储响应。 此扩展还定义必须登记的特定交易和事件。 此组件通常称为 *会计单据提供程序*。
- **硬件工作站扩展** – 此组件初始化与会计设备的通信，基于从会计单据提取的交易/事件数据向会计设备发送请求和直接命令，并接收来自会计设备的响应。 此组件通常称为 *会计连接器*。

会计设备的会计整合示例分别包含会计单据提供程序和会计连接器的 CRT 和硬件工作站扩展。 它还包含以下组件配置：

- **会计单据提供程序配置** – 此配置定义会计单据的输出方法和格式。 它还包含税收和付款方式的数据映射，以使 Retail POS 中的数据与会计设备固件中预定义的值兼容。
- **会计连接器配置** – 此配置定义与特定会计设备的实际通信。

特定 POS 登记的会计登记流程由 POS 功能配置文件中的相应设置定义。 有关如何配置会计登记流程、上载会计单据提供程序和会计连接器配置以及更改其参数的更多详细信息，请参阅[设置会计登记流程](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process)。

以下示例显示会计设备的典型会计登记执行流。 此流从 POS 中的事件开始（例如，销售交易的最终完成），实现以下步骤序列：

1. POS 从 CRT 请求会计单据。
2. CRT 确定当前事件是否需要会计登记。
3. 基于会计登记流程设置，CRT 标识用于会计登记的会计连接器和对应的会计单据提供程序。
4. CRT 运行生成表示交易或事件的会计单据（例如，XML 文档）的会计单据提供程序。
5. POS 将 CRT 准备的会计单据发送到硬件工作站。
6. 硬件工作站运行处理会计单据并将其传送到会计设备或服务的会计连接器。
7. POS 分析来自会计设备或服务的响应以确定会计登记是否成功。
8. CRT 将响应保存到通道数据库。

![解决方案架构](media/emea-fiscal-integration-solution.png "解决方案架构")

## <a name="error-handling"></a>错误处理

会计整合框架在会计登记期间提供以下处理失败情况的选项：

- **重试** – 操作员可以在失败能够快速解决时使用此选项，会计登记可以重新运行。 例如，此选项可以在会计设备未连接、税控打印机缺纸或税控打印机卡纸时使用。
- **取消** – 此选项允许操作员在登记失败时延期当前交易或事件的会计登记。 登记延期后，操作员可以继续在 POS 上工作，并可以完成不需要会计登记的任何操作。 在需要会计登记的任何事件在 POS 中发生时（例如，打开新交易记录），错误处理对话框将自动显示以通知操作员上一项交易未正确登记并提供错误处理选项。
- **跳过** – 操作可以在会计登记可在特定条件下忽略并且可以继续在 POS 上执行常规操作时使用此选项。 例如，当会计登记失败的销售交易可以在特殊的纸质日记帐中登记时，可以使用此选项。
- **标记为已登记** – 当交易在会计设备中实际已登记（例如，财务收据已打印），但在会计响应保存到通道数据库时失败的情况下，操作员可以使用此选项。

> [!NOTE]
> 在使用前，**跳过** 和 **标记为已登记** 选项必须在会计登记流程中启用。 此外，必须向操作员授予相应权限。

**跳过** 和 **标记为已登记** 选项支持信息代码获取有关失败的一些具体信息，如失败原因或跳过会计登记或将交易标记为已登记的理由。 有关如何设置错误处理参数的更多详细信息，请参阅[设置错误处理设置](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings)。

### <a name="optional-fiscal-registration"></a>可选会计登记

会计登记对某些操作而言为强制，但对其他操作则为可选。 例如，常规销售和退货的会计登记可能为强制，但是与客户存款有关的操作的会计登记可能为可选。 在此情况下，未能完成销售的会计登记可能会妨碍更多销售，但是未能完成客户存款的会计登记应该不会妨碍更多销售。 若要区分强制操作和可选操作，建议通过不同单据提供程序处理，并且在这些提供程序的会计登记流程中设置单独的步骤。 应该为与可选会计登记有关的所有步骤启用 **出错时继续** 参数。 有关如何设置错误处理参数的更多详细信息，请参阅[设置错误处理设置](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings)。

### <a name="manually-running-fiscal-registration"></a>手动运行会计登记

如果失败后已推迟了交易记录或事件的会计登记（例如，如果操作员在错误处理对话框中选择了 **取消**），可以通过调用相应操作手动重新运行会计登记。 有关更多详细信息，请参阅[启用已推迟会计登记的手动执行](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration)。

### <a name="fiscal-registration-health-check"></a>会计登记运行状况检查

会计登记的运行状况检查过程用于在特定事件发生时验证会计设备或服务的可用性。 如果当前不能完成会计登记，将提前通知操作员。

发生以下事件时，POS 将运行运行状况检查：

- 开立了新交易记录。
- 撤回了封存的交易记录。
- 完成了销售或退货交易记录。

如果运行状况检查失败，POS 将显示运行状况检查对话框。 此对话框中提供以下按钮：

- **确定** – 操作员可使用此按钮忽略运行状况检查错误并继续处理操作。 仅当为其启用了 **允许跳过运行状况检查错误** 权限，操作员才能选择此按钮。
- **取消** – 如果操作员选择此按钮，POS 将取消最后一个操作（例如，不向新交易记录添加某项）。

> [!NOTE]
> 仅当当前操作需要会计登记，并且为会计登记流程的当前步骤禁用了 **出错时继续** 参数，才会运行运行状况检查。 有关更多详细信息，请参阅[设置错误处理设置](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings)。

## <a name="storing-fiscal-response-in-fiscal-transaction"></a>在会计交易记录中存储会计响应

当交易或事件的会计登记成功时，会计交易记录将在通道数据库中创建并链接到原始交易或事件。 同样，如果为失败的会计登记选择了 **跳过** 或 **标记为已登记** 选项，此信息将存储在会计交易记录中。 会计交易记录保留会计设备或服务的会计响应。 如果会计登记流程包括多个步骤，将为登记成功或失败的流程的每个步骤创建一个会计交易记录。

会计交易记录通过 *P 作业* 与交易记录一起转移到总部。 在 **商店交易记录** 页的 **会计交易记录** 快速选项卡上，您可以查看链接到零售交易记录的会计交易记录。

会计交易记录存储以下详细信息：

- 会计登记流程详细信息（流程、连接器组、连接器等）。 另外还存储 **登记编号** 字段中会计设备的序列号（如果此信息包含在会计响应中）。
- 会计登记的状态：**已完成** 表示成功的登记，如果操作员为失败的登记选择了 **跳过** 选项则为 **已跳过**，或者如果操作员选择了 **标记为已登记** 选项，则为 **标记为已登记**。
- 与所选会计交易记录相关的信息代码交易记录。 要查看信息代码交易记录，在 **会计交易记录** 快速选项卡上，选择状态为 **已跳过** 或 **标记为已登记** 的会计交易记录，然后选择 **信息代码交易记录**。

## <a name="fiscal-texts-for-discounts"></a>折扣的会计文本

某些国家或地区对在应用不同类型的折扣时必须在财务收据上打印的其他文本有特殊要求。 会计整合功能允许您在财务收据上打印的折扣行后面设置特殊的折扣文本。 对于手动折扣，您可以为在 POS 功能配置文件中指定为 **产品折扣** 信息代码的信息代码配置会计文本。 有关如何为折扣设置会计文本的更多详细信息，请参阅[设置折扣的会计文本](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts)。

## <a name="printing-fiscal-x-and-fiscal-z-reports"></a>打印会计 X 和会计 Z 报表

会计整合功能支持生成特定于整合的会计设备或服务的日结报表：

- 运行相应操作的新按钮应添加到 POS 屏幕布局。 更多详细信息，请参阅[从 POS 设置会计 X/Z 报表](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos)。
- 在会计整合示例中，这些操作应匹配到会计设备的相应操作。

## <a name="fiscal-integration-samples-in-the-retail-sdk"></a>Retail SDK 中的会计整合示例

以下会计整合示例当前在 Retail SDK 中可用：

- [意大利税控打印机集成示例](emea-ita-fpi-sample.md)
- [波兰税控打印机集成示例](emea-pol-fpi-sample.md)
- [奥地利的会计登记服务集成示例](emea-aut-fi-sample.md)
- [捷克共和国的会计登记服务集成示例](emea-cze-fi-sample.md)
- [瑞典的控制单元集成示例](./emea-swe-fi-sample.md)
- [德国的会计登记服务集成示例](./emea-deu-fi-sample.md)

以下会计整合功能也在 Retail SDK 中可用，但当前不利用会计整合框架。 在以后的更新中已计划了将此功能迁移到会计整合框架。


- [法国数字签名](emea-fra-cash-registers.md)
- [挪威数字签名](emea-nor-cash-registers.md)

Retail SDK 中提供的以下旧版会计整合功能不使用会计整合框架，将在以后的更新中弃用：

- [瑞典的控制单元集成示例（旧）](./retail-sdk-control-unit-sample.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]