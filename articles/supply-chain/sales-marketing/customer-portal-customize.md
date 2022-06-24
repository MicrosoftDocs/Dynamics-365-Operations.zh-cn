---
title: 自定义和使用客户门户
description: 本文说明将客户门户添加到系统后如何对其进行自定义。
author: Henrikan
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 85ec4beda2efe62ff5076a5ed694efbc47c6d87f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878865"
---
# <a name="customize-and-use-the-customer-portal"></a>自定义和使用客户门户

[!include [banner](../includes/banner.md)]


本文介绍客户门户中现成可用的不同页面。 说明了页面的功能以及如何自定义页面。

客户门户提供了一些现成的网页和操作。 以下站点地图提供了这些网页和操作以及可以执行这些操作的角色的概览。

![客户门户站点地图。](media/customer-portal-site-map.png "客户门户站点地图")

## <a name="typical-customizations"></a>典型自定义

以下文章将帮助您学习有关 Power Apps 门户以及如何定制这些门户的基础知识：

- [使用模板](/powerapps/maker/portals/work-with-templates) – 此文章概括介绍 Power Apps 门户的工作原理以及如何对门户进行简单的自定义。
- [管理门户内容](/dynamics365/portals/manage-portal-content) – 此文章说明如何管理和自定义您在门户中显示的内容。
- [编辑 CSS](/powerapps/maker/portals/edit-css) – 此文章帮助您对门户的用户界面 (UI) 进行更复杂的自定义。
- [为您的门户创建主题](/dynamics365/portals/create-theme) – 此文章帮助您为门户创建 UI 主题。
- [轻松创建和公开门户内容](/dynamics365/portals/create-expose-portal-content) – 此文章帮助您管理用于门户的基础数据和表。
- [配置要在门户上使用的联系人](/powerapps/maker/portals/configure/configure-contacts) – 此文章说明如何创建和自定义用户角色，以及 Power Apps 门户中的安全性和身份验证如何运行。
- [在门户上配置表窗体和 Web 窗体的注释](/powerapps/maker/portals/configure-notes) – 此文章说明如何向门户添加文档和其他存储。
- [门户网站的错误处理](/powerapps/maker/portals/admin/view-portal-error-log) – 此文章说明如何查看门户错误日志并将其存储在您的 Microsoft Azure Blob 存储帐户中。

## <a name="customize-the-order-creation-process"></a>自定义订单创建流程

当用户使用客户门户提交订单时，订单将自动同步到相应的 Dynamics 365 Supply Chain Management 环境。 由于用户是外部客户，因此有意向他们隐藏了一些必需的信息。 表单提交后，这些信息会自动填写。

本节说明应该如何设置联系人以避免错误。 其中说明了自动设置的字段以及如何在必要时修改这些字段的值。

### <a name="the-out-of-box-order-creation-process"></a>现成的订单创建流程

以下是从客户门户提交订单的标准步骤。

1. 在主页上，选择 **创建订单** 磁贴打开 **创建订单** 向导。
1. 在 **订单信息** 页面上，设置以下字段：

    - **请求收货日期** – 指定交货日期。
    - **交货地址** – 输入应该交付订单的地址。
    - **公司** – 选择客户公司的名称。 此字段将为非管理员用户自动设置。
    - **申请编号** – 输入订单的申请编号。 此字段不是必填项。
    - **运达国家/地区** – 输入物料将送达的国家或地区。 此字段将为非管理员用户自动设置。

    ![订单信息页面。](media/customer-portal-order-information.png "订单信息页面")

1. 选择 **下一步**。
1. 在 **物料** 页上，选择 **添加物料**。

    ![物料页面。](media/customer-portal-items.png "“物料”页面")

1. 在 **物料信息** 对话框中，设置以下字段：

    - **产品名称** – 查找并选择要添加到订单中的产品。
    - **数量** – 输入所选产品的数量。
    - **单位** – 指定度量单位（例如，**个**、**公斤** 或 **箱**）。
    - **估计净额** – 此值计算为“物料的估计价格 × 所选单位的数量”。

    ![物料信息对话框。](media/customer-portal-item-information.png "“物料信息”对话框")

1. 选择 **提交** 将物料添加到订单。
1. 重复步骤 4 到 6，直到您添加了要订购的所有物料。
1. 添加完物料后，在 **物料** 页上选择 **下一步**。
1. **订单信息** 页提供订单摘要。 查看订单内容和交货详细信息。 如果每一项看起来都正确，选择 **提交** 提交订单。

    ![已完成订单信息页面。](media/customer-portal-order-submit.png "已完成订单信息页面")

### <a name="standard-data-setup"></a>标准数据设置

为了帮助确保流畅的用户体验，客户门户会自动填充几个必填字段的值。 这些值基于提交订单的客户的联系记录中的信息。

对于属于将使用客户门户提交订单的客户的每个[联系人行](/powerapps/maker/portals/configure/configure-contacts)，必须为以下必填字段指定值。 否则会发生错误。

- **公司** – 订单所属的法人
- **潜在客户** – 与订单关联的客户帐户
- **价目表** – 客户的自定义价目表
- **货币** – 价格使用的货币
- **运达国家/地区** – 物料将送达的国家或地区

将自动为销售订单表设置以下字段：

- **语言** – 订单的语言（默认情况下，此值取自联系人记录。）
- **运达国家/地区** – 物料将被运送到的国家或地区（默认情况下，此值取自联系人记录。）
- **联系人** – 可以与其联系来获取有关订单的信息的用户（默认情况下，此值取自联系人记录。）
- **公司** – 订单所属的法人（默认情况下，此值取自联系人记录。）
- **潜在客户** – 与订单关联的客户帐户（默认情况下，此值取自联系人记录。）
- **发票客户** – 订单的计费帐户（默认值为联系人记录中的潜在客户。）
- **销售订单名称** – 销售订单的名称（默认值为 **销售订单**。）
- **货币** – 价格使用的货币（默认情况下，此值取自联系人记录。）
- **价目表** – 客户的自定义价目表（默认情况下，此值取自联系人记录。）
- **交货地址描述** – 销售订单的交货地址（默认值为 **交货地址描述**。）

### <a name="modify-the-order-creation-process"></a>修改订单创建流程

如果不更改基本订单创建流程，可以自由修改客户门户的外观和 UI。 如果要更改订单创建流程，必须牢记几点。

不要从 Microsoft Dataverse 中的销售订单表中删除以下列，因为它们是以双写入方式创建销售订单所必需的：

- **公司** – 订单所属的法人
- **名称** – 销售订单的名称
- **货币** – 价格使用的货币
- **价目表** – 客户的自定义价目表
- **运达国家/地区** – 物料将送达的国家或地区
- **潜在客户** – 与订单关联的客户帐户
- **语言** – 订单的语言（通常，此语言是潜在客户的语言。）
- **交货地址描述** – 销售订单的交货地址

对于物料，必须有以下列：

- **产品** – 要订购的产品
- **数量** – 所选产品的数量
- **单位** – 度量单位（例如，**个**、**公斤** 或 **箱**）
- **运达国家/地区** – 交货国家或地区
- **交货地址描述** – 订单的交货地址

您必须确保客户门户以某种方式提交所有这些列的值。

如果要向页面添加列或删除列，请参阅[创建或编辑快速创建窗体以简化数据输入体验](/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms)。

如果要更改保存页面时列的预设方式和值的设置方式，请参阅 Power Apps 门户文档中的以下信息：

- [预填充字段](/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [保存时设置值](/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a>自定义主页

客户门户中的所有控件都是内置的 Power Apps 门户控件。 您可以按照 Power Apps 门户文档中[设计页面](/powerapps/maker/portals/compose-page)中的以下步骤自定义这些控件。

客户门户模板中包含的唯一自定义控件用于在主页上创建磁贴。

![主页上的磁贴。](media/customer-portal-home-page-tiles.png "主页上的磁贴")

要修改磁贴，请按照下列步骤操作。

1. 打开[“门户管理”应用](/powerapps/maker/portals/configure/configure-portal)。
1. 在左侧的导航窗格中，选择 **页面模板**。

    ![门户管理导航窗格。](media/customer-portal-nav.png "“门户管理”导航窗格")

1. 选择名为 **主页** 的页面模板。
1. 在 **Web 模板** 字段中，选择 **主页** 链接打开该页面的源代码。

    ![Web 模板字段。](media/customer-portal-web-template.png "“Web 模板”字段")

1. 现在，您应该可以看到主页的所有源代码，并可以根据需要对其进行修改。

## <a name="resources"></a>资源

要了解有关如何设置和自定义客户门户的详细信息，请参阅以下资源：

- [Power Apps 门户文档](/powerapps/maker/portals/overview)
- [双写入文档](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [关于门户生命周期](/powerapps/maker/portals/admin/portal-lifecycle)
- [升级门户](/powerapps/maker/portals/admin/upgrade-portal)
- [迁移门户配置](/powerapps/maker/portals/admin/migrate-portal-configuration)
- [解决方案生命周期管理：Dynamics 365 for Customer Engagement 应用](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]