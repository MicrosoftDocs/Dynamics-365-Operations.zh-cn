---
title: "定义和维护零售渠道"
description: "文章此窗体可以设置砖和商店流程的概览，泥提供在 Microsoft Dynamics 365 中引用零售店操作。 它包含有关在设置零售商店前后必须完成的任务的信息。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: b775ba34ef7d88dd0b47904e4a3e9be79664f14b
ms.lasthandoff: 03/31/2017


---

# <a name="define-and-maintain-retail-channels"></a>定义和维护零售渠道

文章此窗体可以设置砖和商店流程的概览，泥提供在 Microsoft Dynamics 365 中引用零售店操作。 它包含有关在设置零售商店前后必须完成的任务的信息。

零售和商务 Dynamics 中 365 操作的支持多个零售通道，例如商店、网络呼叫中心和砖和泥商店。 在“零售和商业”中，实体商店也称作“零售商店”。 每个零售商店可以有自己的付款方式、价格组、销售终端 (POS) 收银机、收入帐户和支出帐户以及职员。 您必须先为零售商店设置所有这些元素，然后再创建零售商店。 在创建零售商店后，分配您希望其提供的产品。 您还可以将员工、收银机和客户分配到商店。 最后，您将新商店添加到组织层次结构。

## <a name="setting-up-retail-stores"></a>设置零售商店
在您可以设置在 Dynamics 365 的一个的零售店工序之前，必须完成某些任务的先决条件。 然后，您可以创建零售商店并添加详细信息。

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
11. 设置职员。 **注释：**还必须分配适当的权限。工作人员，因此，它们可以登录和执行任务使用工序 365 的 Dynamics Retail POS 的系统。
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
Retail 在 Microsoft Dynamics AX 中使用组织层次结构以构造零售渠道。 组织层次结构表示构成贵企业组织之间的关系。 在您设置商店时，您可以添加到组织层次结构。 存储然后共享用于分类、补货和报告的数据。


