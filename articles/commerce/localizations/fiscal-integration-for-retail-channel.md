---
title: Commerce 渠道的会计集成概览
description: 此主题提供 Dynamics 365 Commerce 中可用的会计整合功能的概览。
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 46e0afd5a8cb692da56a7d5f261ca30d9b3aaa80
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388305"
---
# <a name="fiscal-integration-overview-for-commerce-channels"></a>Commerce 渠道的会计集成概览

[!include [banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

此主题是 Dynamics 365 Commerce 中可用的会计整合功能的概览。 

会计整合包括与不同会计设备和服务的集成，这些设备和服务支持依据旨在防止零售行业的税收欺诈的地方政法进行销售的会计登记。 以下是可以使用会计整合应对的一些典型场景：

- 在连接到销售点 (POS) 的会计设备（如税控打印机）上登记销售，以及为客户打印财务收据。
- 安全地向税务主管机构管理的外部 Web 服务提交与在 Retail POS 完成的销售和退货相关的信息。
- 通过数字签名帮助确保销售交易数据的不变性。

会计整合功能是一个框架，为进一步开发和自定义 Retail POS 与会计设备和服务之间的整合提供通用解决方案。 此功能还包括支持特定国家或地区的基本方案，以及使用特定会计设备或服务的会计整合示例。 会计整合示例由若干 Commerce 组件的扩展组成，包含在软件开发套件 (SDK) 中。 有关会计整合示例的详细信息，请参阅 [Commerce SDK 中的会计整合示例](#fiscal-integration-samples-in-the-commerce-sdk)。 有关如何安装和使用 Commerce SDK 的信息，请参阅 [Retail 软件开发套件 (SDK) 体系结构](../dev-itpro/retail-sdk/retail-sdk-overview.md)。

为了支持会计整合示例不支持的其他方案，将 Retail POS 与其他会计设备或服务整合，或者满足其他国家或地区的要求，您必须扩展用现有的会计整合示例或将现有示例用作范例创建新示例。

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services"></a>会计设备和服务的会计登记流程和会计整合示例

Retail POS 中的会计登记流程可以包含一个或多个步骤。 每个步骤涉及一个会计设备或服务的特定交易或事件的会计登记。 以下解决方案组件参与会计设备或服务中的会计登记：

- **会计单据提供程序** – 此组件序列化同时用于与会计设备或服务交互的格式的交易/事件数据，分析来自会计设备或服务的回应，并在通道数据库中存储响应。 此扩展还定义必须登记的特定交易和事件。
- **会计连接器** – 此组件初始化与会计设备或服务的通信，基于从会计单据提取的交易/事件数据向会计设备或服务发送请求或直接命令，并接收来自会计设备或服务的响应

会计整合示例可能包含会计单据提供程序和会计连接器的 Commerce runtime (CRT)、硬件工作站和 POS 扩展。 它还包含以下组件配置：

- **会计单据提供程序配置** – 此配置定义会计单据的输出方法和格式。 它还包含税收和付款方式的数据映射，以使 Retail POS 中的数据与会计设备或服务固件中预定义的值兼容。
- **会计连接器配置** – 此配置定义与特定会计设备或服务的实际通信。

特定 POS 登记的会计登记流程由 POS 功能配置文件中的相应设置定义。 有关如何配置会计登记流程、上载会计单据提供程序和会计连接器配置以及更改配置参数的更多详细信息，请参阅[设置会计登记流程](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process)。

> [!NOTE]
> 如果您需要用于非会计操作（如产品目录搜索、客户查找或交易记录草稿创建）的设备，您可以选择这些设备作为具有会计流程限制的收银机。 有关详细信息，请参阅[设置具有会计登记限制的收银机](setting-up-fiscal-integration-for-retail-channel.md#set-up-registers-with-fiscal-registration-restrictions)。

以下典型的会计登记流程从 POS 中的一个事件开始（例如，完成销售交易），实施一系列涉及其他 Commerce 组件（如 CRT 和硬件工作站）的预定义步骤。

1. POS 从会计整合框架 (FIF) 请求会计单据。
1. FIF 确定当前事件是否需要会计登记。
1. 基于会计登记流程的设置，FIF 确定用于会计登记的会计连接器和对应的会计单据提供程序。
1. FIF 运行生成表示交易或事件的会计单据（例如，XML 文档）的会计单据提供程序。
1. FIF 将生成的会计单据返回到 POS。
1. POS 请求 FIF 将会计单据提交到会计设备或服务。
1. FIF 运行处理会计单据并将其提交到会计设备或服务的会计连接器。
1. FIF 将会计响应（即会计设备或服务的响应）返回到 POS。
1. POS 分析会计响应以确定会计登记是否成功。 根据需要，POS 请求 FIF 处理发生的任何错误。 
1. POS 请求 FIF 处理并保存会计响应。
1. 会计单据提供程序处理会计响应。 作为此处理的一部分，会计单据提供程序分析响应并从中提取扩展数据。
1. FIF 将响应和扩展数据保存到渠道数据库。
1. 根据需要，POS 通过连接到硬件工作站的常规收据打印机打印收据。 收据可以包含来自会计响应的必需数据。
 
以下示例显示典型会计设备或服务的会计登记执行流。
 
### <a name="fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station"></a>会计登记通过连接到硬件工作站的设备进行

此配置在实体会计设备（如会计打印机）连接到硬件工作站时使用。 通过在硬件工作站上安装的软件完成与会计设备或服务的通信时也适用。 在这种情况下，会计单据提供程序位于 CRT，会计连接器位于硬件工作站。

![会计登记通过连接到硬件工作站的设备进行。](media/FIF-CRT-HWS.png)

### <a name="fiscal-registration-is-done-via-an-external-service"></a>会计登记通过外部服务完成

此配置在通过外部服务（如由税务机构运营的 Web 服务）完成会计登记时使用。 在这种情况下，会计单据提供程序和会计连接器均位于 CRT。

![会计登记通过外部服务完成。](media/FIF-CRT-CRT.png)
 
### <a name="fiscal-registration-is-done-internally-in-the-crt"></a>会计登记在 CRT 中内部完成

此配置在会计登记不需要外部会计设备或服务时使用。 例如，在通过对销售交易记录进行数字签名完成会计登记时使用。 在这种情况下，会计单据提供程序和会计连接器均位于 CRT。

![会计登记在 CRT 中内部完成。](media/FIF-CRT-CRT-SGN.png)

### <a name="fiscal-registration-is-done-via-a-device-or-service-in-the-local-network"></a>会计登记通过本地网络中的设备或服务完成

当商店的本地网络中存在实体会计设备或会计服务并且其提供 HTTPS 应用程序编程接口 (API) 时，将使用此配置。 在这种情况下，会计单据提供程序位于 CRT，会计连接器位于 POS。

![会计登记通过本地网络中的设备或服务完成。](media/FIF-CRT-POS.png)

## <a name="error-handling"></a>错误处理

会计整合框架在会计登记期间提供以下处理失败情况的选项：

- **重试** – 操作员可以在失败能够快速解决时使用此选项，会计登记可以重新运行。 例如，此选项可以在会计设备未连接、税控打印机缺纸或税控打印机卡纸时使用。
- **取消** – 此选项允许操作员在登记失败时延期当前交易或事件的会计登记。 登记延期后，操作员可以继续在 POS 上工作，并可以完成不需要会计登记的任何操作。 在需要会计登记的任何事件在 POS 中发生时（例如，打开新交易记录），错误处理对话框将自动显示以通知操作员上一项交易未正确登记并提供错误处理选项。
- **跳过** – 操作可以在会计登记可在特定条件下忽略并且可以继续在 POS 上执行常规操作时使用此选项。 例如，当会计登记失败的销售交易可以在特殊的纸质日记帐中登记时，可以使用此选项。
- **标记为已登记** – 当交易在会计设备中实际已登记（例如，财务收据已打印），但在会计响应保存到通道数据库时失败的情况下，操作员可以使用此选项。
- **推迟** – 当交易记录因登记服务不可用而未登记时，操作员可以使用此选项。 

> [!NOTE]
> 在使用前，**跳过**、**标记为已登记** 和 **推迟** 选项必须在会计登记流程中启用。 此外，必须向操作员授予相应权限。

**跳过**、**标记为已登记** 和 **推迟** 选项支持信息代码获取有关失败的一些具体信息，如失败原因或跳过会计登记或将交易标记为已登记的理由。 有关如何设置错误处理参数的更多详细信息，请参阅[设置错误处理设置](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings)。

### <a name="optional-fiscal-registration"></a>可选会计登记

会计登记对某些操作而言为强制，但对其他操作则为可选。 例如，常规销售和退货的会计登记可能为强制，但是与客户存款有关的操作的会计登记可能为可选。 在此情况下，未能完成销售的会计登记可能会妨碍更多销售，但是未能完成客户存款的会计登记应该不会妨碍更多销售。 若要区分强制操作和可选操作，建议通过不同单据提供程序处理，并且在这些提供程序的会计登记流程中设置单独的步骤。 应该为与可选会计登记有关的所有步骤启用 **出错时继续** 参数。 有关如何设置错误处理参数的更多详细信息，请参阅[设置错误处理设置](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings)。

### <a name="manually-rerun-fiscal-registration"></a>手动重新运行会计登记

如果失败后已推迟了交易记录或事件的会计登记（例如，如果操作员在错误处理对话框中选择了 **取消**），可以通过调用相应操作手动重新运行会计登记。 有关更多详细信息，请参阅[启用已推迟会计登记的手动执行](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration)。

### <a name="postpone-option"></a>推迟选项

如果当前步骤失败，**推迟** 选项可让您继续执行财务登记流程。 当存在会计登记备份选项时，可以使用此选项。

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
- 会计登记的状态：**已完成** 表示成功的登记，如果操作员为失败的登记选择了 **跳过** 选项则为 **已跳过**，如果操作员选择了 **标记为已登记** 选项，则为 **标记为已登记**，或者如果操作员选择了 **推迟** 选项，则为 **已推迟**。
- 与所选会计交易记录相关的信息代码交易记录。 要查看信息代码交易记录，在 **会计交易记录** 快速选项卡上，选择状态为 **已跳过**、**标记为已登记** 或 **已推迟** 的会计交易记录，然后选择 **信息代码交易记录**。

通过选择 **扩展数据**，您还可以查看会计交易的某些属性。 可查看的属性列表特定于生成会计交易的会计登记功能。 例如，您可以查看法国数字签名功能的数字签名、序列号、证书指纹、哈希算法标识和其他会计交易记录属性。

## <a name="fiscal-texts-for-discounts"></a>折扣的会计文本

某些国家或地区对在应用不同类型的折扣时必须在财务收据上打印的其他文本有特殊要求。 会计整合功能允许您在财务收据上打印的折扣行后面设置特殊的折扣文本。 对于手动折扣，您可以为在 POS 功能配置文件中指定为 **产品折扣** 信息代码的信息代码配置会计文本。 有关如何为折扣设置会计文本的更多详细信息，请参阅[设置折扣的会计文本](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts)。

## <a name="printing-fiscal-x-and-fiscal-z-reports"></a>打印会计 X 和会计 Z 报表

会计整合功能支持生成特定于整合的会计设备或服务的日结报表：

- 运行相应操作的新按钮应添加到 POS 屏幕布局。 更多详细信息，请参阅[从 POS 设置会计 X/Z 报表](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos)。
- 在会计整合示例中，这些操作应匹配到会计设备的相应操作。

## <a name="fiscal-integration-samples-in-the-commerce-sdk"></a>Commerce SDK 中的会计整合示例

以下会计整合示例当前在 Commerce SDK 中可用：

- [意大利税控打印机集成示例](./emea-ita-fpi-sample.md)
- [波兰税控打印机集成示例](./emea-pol-fpi-sample.md)
- [奥地利的会计登记服务集成示例](./emea-aut-fi-sample.md)
- [捷克共和国的会计登记服务集成示例](./emea-cze-fi-sample.md)
- [瑞典的控制单元集成示例](./emea-swe-fi-sample.md)
- [德国的会计登记服务集成示例](./emea-deu-fi-sample.md)
- [俄罗斯税控打印机集成示例](./rus-fpi-sample.md)

以下会计整合功能也通过使用会计集成框架来实现，但该功能可即装即用，并且未包含在 Commerce SDK 中：

- [巴西的会计登记](./latam-bra-commerce-localization.md#fiscal-registration-for-brazil)
- [法国数字签名](./emea-fra-cash-registers.md)

以下会计整合功能也在 Commerce SDK 中可用，但当前不利用会计整合框架。 在以后的更新中已计划了将此功能迁移到会计整合框架。

- [挪威数字签名](./emea-nor-cash-registers.md)

Commerce SDK 中提供的以下旧版会计整合功能不使用会计整合框架，将在以后的更新中弃用：

- [瑞典的控制单元集成示例（旧）](./retail-sdk-control-unit-sample.md)
- [法国数字签名（旧版）](./emea-fra-deployment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
