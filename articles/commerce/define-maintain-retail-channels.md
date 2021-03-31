---
title: 定义和维护零售渠道
description: 本主题提供设置实体商店（在 Dynamics 365 Commerce 中称为商店）的流程的概览。 它包含有关在设置商店前后必须完成的任务的信息。
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a2ac4a4a42447e4ee57d24548a79f43b88b03927
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213690"
---
# <a name="define-and-maintain-retail-channels"></a>定义和维护零售渠道

[!include [banner](includes/banner.md)]

本主题提供设置实体商店（在 Dynamics 365 Commerce 中称为商店）的流程的概览。 它包含有关在设置商店前后必须完成的任务的信息。

Commerce 支持多个渠道，例如在线商店、呼叫中心和实体商店。 实体商店也叫做商店。 每个商店可以有自己的付款方式、价格组、销售终端收银机 (POS)、登记、收入帐户和支出帐户以及职员。 您必须先为商店设置所有这些元素，然后再创建商店。 在创建商店后，分配您希望其提供的产品。 您还可以将员工、收银机和客户分配到商店。 最后，您将新商店添加到组织层次结构。

## <a name="setting-up-stores"></a>设置存储

在您可以在 Commerce 中设置商店之前，必须完成某些先决任务。 然后，您可以创建商店并添加详细信息。

### <a name="prerequisites"></a>先决条件

您必须先完成以下任务，然后才能设置商店：

1. 配置您的组织结构和设置零售分类、补货和报告的组织层次结构。
2. 设置代表商店的仓库。
3. 设置商店、商店报表和报表凭证的编号规则。
4. 配置 Commerce 参数。
5. 设置商店接受的付款方式。
6. 要处理 POS 收银机上的信用卡交易记录，您还可以设置付款服务。
7. 设置销售税组。
8. 设置产品： 作为此任务的一部分，您还可设置产品层次结构、产品变型和产品分类。
9. 设置产品价格组。
10. 设置产品定价。 作为此任务的一部分，您还可设置价格调整、折扣和折扣期间。
11. 设置职员。

    > [!NOTE]
    > 您还必须向工作人员分配适当的权限，以便他们可使用 POS 系统登录并执行任务。

12. 配置要分配给商店的 POS 配置文件。 此任务包括许多其他任务，例如，设置收银机、设置脱机配置文件和设置收据格式和配置文件。

查看包含在先决任务中的所有任务，并仅完成适用于您的任务。

### <a name="set-up-a-store"></a>设置商店

在您完成先决任务后，完成以下任务以设置商店的详细信息：

1. 创建商店。
2. 将销售税组分配给商店。
3. 分配商店接受的付款方式。
4. 对您商店中提供的产品，添加有关产品描述的详细信息。 例如，您可以添加富文本和图像。 这些产品详细信息将在各种情况下显示，例如 POS 收银机或已打印的标签上。
5. 将商店添加到已分配到 **零售分类**、**零售补货** 或 **零售报告** 的默认组织层次结构。

### <a name="after-you-set-up-a-store"></a>在您设置了商店后

在输入商店的详细信息后，请完成以下任务以发送新的商店数据到 POS：

1. 配置商店的 POS 收银机。
2. 将产品分类分配到商店。
3. 处理分类以生成包含在分类中的产品列表并使该产品可用在商店找到。
4. 将数据（例如编号规则、硬件配置文件和 POS 屏幕布局）发送到 POS 收银机。
5. 发布商店，从而将商店数据发送到 POS。
6. 运行作业以将商店数据发送到 POS。

## <a name="organization-hierarchies"></a>组织层次结构

Commerce 使用组织层次机构来构造渠道。 组织层次结构表示构成贵企业组织之间的关系。 在您设置商店时，您可以添加到组织层次结构。 存储然后共享用于分类、补货和报告的数据。

> [!NOTE]
> 要使用 Commerce 销售功能，**多次收货** 的配置键必须启用。 可以在 **系统管理** \> **设置** \> **许可证配置** 下的 **贸易配置** 键中找到此配置键。 由于会根据在销售订单行级别配置的交货地址执行各种验证，因此这是必需的。



[!INCLUDE[footer-include](../includes/footer-banner.md)]