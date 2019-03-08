---
title: 销售点 (POS) 应用程序和用户语言设置
description: 此主题介绍如何在 Retail Modern POS (MPOS) 和 Cloud POS 中更改语言设置。
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: faf8cdcee70b55842072298b51789f6cd7a577af
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "336742"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a>销售点 (POS) 应用程序和用户语言设置

[!include [banner](includes/banner.md)]

此主题介绍如何在 Retail Modern POS (MPOS) 和 Cloud POS 中更改语言设置。

## <a name="overview"></a>概览

Retail Modern POS (MPOS) 和 Cloud POS 支持商店和用户设置之间的语言设置和交易记录可以改变的环境。 例如，商店所在位置可能是客户最常用英语的区域，而某些工作人员更愿意使用法语翻译的应用程序。

## <a name="data-language"></a>数据语言

不论用户如何设置，MPOS 和 Cloud POS 都始终使用商店的语言设置确定用于数据的翻译。 这将确保所有用户和客户将获得一致的体验。 数据的示例包括：

- 产品
- 属性和值
- 类别名称
- 打印的或已发送电子邮件的交易记录收据
- 付款方式名称
- 行显示消息

商店的语言也将用于主 POS 登录屏幕，因为不能在用户登录前了解其偏好语言。 如果交易记录不支持商店的语言，POS 将恢复为公司的语言。

### <a name="configuring-the-stores-language-setting"></a>配置商店的语言设置

商店的语言设置从**常规 &gt; 区域设置 &gt; 语言**下的**零售商店**页上的**所有零售商店**设置。 请使用下拉列表为每个商店选择语言。

## <a name="user-interface-language"></a>使用界面语言

POS 用户的语言设置确定在应用程序用户界面使用的翻译。 这包括不视为数据的所有标签、菜单和列表。 POS 按钮网格中显示的文本除外。 这些按钮网格不支持翻译，所以始终按照按钮的定义显示文本。 要支持经过翻译的按钮，必须复制并保留单独的按钮网格，然后根据需要将其分配给用户。

### <a name="configuring-the-users-language-setting"></a>配置用户的语言设置

POS 用户的语言设置从**零售 &gt; 语言**下的**工作人员**页上的**所有工作人员**设置。 不在主“配置文件”选项卡上设置。POS 不使用此设置。 如果未设置用户的语言或设置为不可使用翻译的语言，POS 将恢复为商店的语言。

|             | UI 语言                  | 数据语言（产品、收据格式、行显示等） |
|-------------|----------------------------|---------------------------------------------------------------|
| **公司** | 默认值                    | 默认值                                                       |
| **商店**   | 覆盖公司          | 覆盖公司                                             |
| **用户**    | 覆盖商店或公司 | 从不                                                         |
