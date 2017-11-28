---
title: "定义和维护零售渠道"
description: "本主题提供设置实体商店（在 Microsoft Dynamics 365 for Retail 中称为零售商店）的流程的概览。 它包含有关在设置零售商店前后必须完成的任务的信息。"
author: mugunthanm
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 52b3e2e78a03ac67507ee65a03e0884e5ed44678
ms.openlocfilehash: b6dd6d929d771e0b1fc2604b90a2a1522447e168
ms.contentlocale: zh-cn
ms.lasthandoff: 11/14/2017

---

# <a name="define-and-maintain-retail-channels"></a>定义和维护零售渠道

[!include[banner](includes/banner.md)]


本主题提供设置实体商店（在 Microsoft Dynamics 365 for Retail 中称为零售商店）的流程的概览。 它包含有关在设置零售商店前后必须完成的任务的信息。

Dynamics 365 for Retail 支持多个零售渠道，例如在线商店、呼叫中心和实体商店。 实体商店也叫做零售商店。 每个零售商店可以有自己的付款方式、价格组、销售终端 (POS) 收银机、收入帐户和支出帐户以及职员。 您必须先为零售商店设置所有这些元素，然后再创建零售商店。 在创建零售商店后，分配您希望其提供的产品。 您还可以将员工、收银机和客户分配到商店。 最后，您将新商店添加到组织层次结构。

## <a name="setting-up-retail-stores"></a>设置零售商店
您必须先完成一些先决任务，然后才能在 Dynamics 365 for Retail 中设置零售商店。 然后，您可以创建零售商店并添加详细信息。

### <a name="prerequisites"></a>必备项

您必须先完成以下任务，然后才能设置零售商店：

1.  配置您的组织结构和设置零售分类、补货和报告的组织层次结构。
2.  设置代表零售商店的仓库。
3.  设置零售商店、商店报表和报表凭证的编号规则。
4.  配置零售的参数。
5.  设置商店接受的付款方式。
6.  要处理零售 POS 收银机上的信用卡交易记录，您还可以设置付款服务。
7.  设置销售税组。
8.  设置零售产品。 作为此任务的一部分，您还可设置零售产品层次结构、产品变型和产品分类。
9.  设置产品价格组。
10. 设置零售产品定价。 作为此任务的一部分，您还可设置价格调整、折扣和折扣期间。
11. 设置职员。 **注意：**您还必须向工作人员分配适当的权限，以便他们可使用适用于 Retail POS 系统的 Dynamics 365 for Retail 登录并执行任务。
12. 配置要分配给商店的 Retail POS 配置文件。 此任务包括许多其他任务，例如，设置收银机、设置脱机配置文件和设置收据格式和配置文件。

查看包含在先决任务中的所有任务，并仅完成适用于您的任务。

### <a name="set-up-a-retail-store"></a>设置零售商店

在您完成先决任务后，完成以下任务以设置零售商店的详细信息：

1.  创建零售商店。
2.  将销售税组分配给商店。
3.  分配商店接受的付款方式。
4.  对您零售商店中提供的产品，添加有关产品描述的详细信息。 例如，您可以添加富文本和图像。 这些产品详细信息将在各种情况下显示，例如 POS 收银机或已打印的标签上。
5.  将商店添加到已分配到**“零售分类”**、**“零售补货”**或**“零售报告”**的默认组织层次结构。

### <a name="after-you-set-up-a-retail-store"></a>在您设置了零售商店后

在输入零售商店的详细信息后，请完成以下任务以将新的零售商店数据发送到 Retail POS：

1.  配置商店的 POS 收银机。
2.  将产品分类分配到商店。
3.  处理分类以生成包含在分类中的产品列表并使该产品可用在零售商店找到。
4.  将数据（例如编号规则、硬件配置文件和 POS 屏幕布局）发送到 Retail POS 收银机。
5.  发布零售商店以将商店数据发送到 Retail POS。
6.  运行作业以将商店数据发送到 Retail POS。

## <a name="organization-hierarchies"></a>组织层次结构
Retail 使用组织层次机构来构造零售渠道。 组织层次结构表示构成贵企业组织之间的关系。 在您设置商店时，您可以添加到组织层次结构。 存储然后共享用于分类、补货和报告的数据。




