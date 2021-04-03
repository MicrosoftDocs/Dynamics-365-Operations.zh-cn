---
title: 销售点 (POS) 应用程序和用户语言设置
description: 此主题介绍如何在 Modern POS (MPOS) 和 Cloud POS 中更改语言设置。
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
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 09824d3b2eb8e3c1602882f19131d9fe312baaac
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263148"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a><span data-ttu-id="b4721-103">销售点 (POS) 应用程序和用户语言设置</span><span class="sxs-lookup"><span data-stu-id="b4721-103">Point of sale (POS) application and user language settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b4721-104">此主题介绍如何在 Modern POS (MPOS) 和 Cloud POS 中更改语言设置。</span><span class="sxs-lookup"><span data-stu-id="b4721-104">This topic describes how to change language settings in Modern POS (MPOS) and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="b4721-105">概览</span><span class="sxs-lookup"><span data-stu-id="b4721-105">Overview</span></span>
<span data-ttu-id="b4721-106">Modern POS (MPOS) 和 Cloud POS 支持商店和用户设置之间的语言设置和交易记录可以改变的环境。</span><span class="sxs-lookup"><span data-stu-id="b4721-106">Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="b4721-107">例如，商店所在位置可能是客户最常用英语的区域，而某些工作人员更愿意使用法语翻译的应用程序。</span><span class="sxs-lookup"><span data-stu-id="b4721-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="b4721-108">数据语言</span><span class="sxs-lookup"><span data-stu-id="b4721-108">Data language</span></span>

<span data-ttu-id="b4721-109">不论用户如何设置，MPOS 和 Cloud POS 都始终使用商店的语言设置确定用于数据的翻译。</span><span class="sxs-lookup"><span data-stu-id="b4721-109">Regardless of the user's settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="b4721-110">这将确保所有用户和客户将获得一致的体验。</span><span class="sxs-lookup"><span data-stu-id="b4721-110">This will ensure that all users and customers will have a consistent experience.</span></span> <span data-ttu-id="b4721-111">数据的示例包括：</span><span class="sxs-lookup"><span data-stu-id="b4721-111">Examples of data include:</span></span>

- <span data-ttu-id="b4721-112">产品</span><span class="sxs-lookup"><span data-stu-id="b4721-112">Products</span></span>
- <span data-ttu-id="b4721-113">属性和值</span><span class="sxs-lookup"><span data-stu-id="b4721-113">Attributes and values</span></span>
- <span data-ttu-id="b4721-114">类别名称</span><span class="sxs-lookup"><span data-stu-id="b4721-114">Category names</span></span>
- <span data-ttu-id="b4721-115">打印的或已发送电子邮件的交易记录收据</span><span class="sxs-lookup"><span data-stu-id="b4721-115">Printed or emailed transaction receipts</span></span>
- <span data-ttu-id="b4721-116">付款方式名称</span><span class="sxs-lookup"><span data-stu-id="b4721-116">Payment method names</span></span>
- <span data-ttu-id="b4721-117">行显示消息</span><span class="sxs-lookup"><span data-stu-id="b4721-117">Line display messages</span></span>

<span data-ttu-id="b4721-118">商店的语言也将用于主 POS 登录屏幕，因为不能在用户登录前了解其偏好语言。</span><span class="sxs-lookup"><span data-stu-id="b4721-118">The store's language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="b4721-119">如果交易记录不支持商店的语言，POS 将恢复为公司的语言。</span><span class="sxs-lookup"><span data-stu-id="b4721-119">If a translation is not available for the store's language, the POS will revert to the company's language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="b4721-120">配置商店的语言设置</span><span class="sxs-lookup"><span data-stu-id="b4721-120">Configuring the store's language setting</span></span>

<span data-ttu-id="b4721-121">商店的语言设置从 **常规 &gt; 区域设置 &gt; 语言** 下的 **商店** 页上的 **所有商店** 设置。</span><span class="sxs-lookup"><span data-stu-id="b4721-121">The store's language setting is set from **All stores** on the **Store** page under **General &gt; Regional Settings &gt; Language**.</span></span> <span data-ttu-id="b4721-122">请使用下拉列表为每个商店选择语言。</span><span class="sxs-lookup"><span data-stu-id="b4721-122">Use the drop-down list to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="b4721-123">使用界面语言</span><span class="sxs-lookup"><span data-stu-id="b4721-123">User interface language</span></span>

<span data-ttu-id="b4721-124">POS 用户的语言设置确定在应用程序用户界面使用的翻译。</span><span class="sxs-lookup"><span data-stu-id="b4721-124">The POS user's language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="b4721-125">这包括不视为数据的所有标签、菜单和列表。</span><span class="sxs-lookup"><span data-stu-id="b4721-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="b4721-126">POS 按钮网格中显示的文本除外。</span><span class="sxs-lookup"><span data-stu-id="b4721-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="b4721-127">这些按钮网格不支持翻译，所以始终按照按钮的定义显示文本。</span><span class="sxs-lookup"><span data-stu-id="b4721-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="b4721-128">要支持经过翻译的按钮，必须复制并保留单独的按钮网格，然后根据需要将其分配给用户。</span><span class="sxs-lookup"><span data-stu-id="b4721-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="b4721-129">配置用户的语言设置</span><span class="sxs-lookup"><span data-stu-id="b4721-129">Configuring the user's language setting</span></span>

<span data-ttu-id="b4721-130">POS 用户的语言设置从 **Retail 和 Commerce &gt; 语言** 下的 **工作人员** 页上的 **所有工作人员** 设置。</span><span class="sxs-lookup"><span data-stu-id="b4721-130">The POS user's language setting is set from **All workers** on the **Worker** page under **Retail and Commerce &gt; Language**.</span></span> <span data-ttu-id="b4721-131">不在主“配置文件”选项卡上设置。POS 不使用此设置。</span><span class="sxs-lookup"><span data-stu-id="b4721-131">It is not set on the main Profile tab. This setting is not used by POS.</span></span> <span data-ttu-id="b4721-132">如果未设置用户的语言或设置为不可使用翻译的语言，POS 将恢复为商店的语言。</span><span class="sxs-lookup"><span data-stu-id="b4721-132">If the user's language is not set or it is set to a language where translations are not available, the POS will revert to the store's language.</span></span>

|             | <span data-ttu-id="b4721-133">UI 语言  </span><span class="sxs-lookup"><span data-stu-id="b4721-133">UI language</span></span>                | <span data-ttu-id="b4721-134">数据语言（产品、收据格式、行显示等）</span><span class="sxs-lookup"><span data-stu-id="b4721-134">Data language (products, receipt formats, line display, etc.)</span></span> |
|-------------|----------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b4721-135">**公司**</span><span class="sxs-lookup"><span data-stu-id="b4721-135">**Company**</span></span> | <span data-ttu-id="b4721-136">默认值</span><span class="sxs-lookup"><span data-stu-id="b4721-136">Default</span></span>                    | <span data-ttu-id="b4721-137">默认值</span><span class="sxs-lookup"><span data-stu-id="b4721-137">Default</span></span>                                                       |
| <span data-ttu-id="b4721-138">**商店**</span><span class="sxs-lookup"><span data-stu-id="b4721-138">**Store**</span></span>   | <span data-ttu-id="b4721-139">覆盖公司</span><span class="sxs-lookup"><span data-stu-id="b4721-139">Overrides company</span></span>          | <span data-ttu-id="b4721-140">覆盖公司</span><span class="sxs-lookup"><span data-stu-id="b4721-140">Overrides company</span></span>                                             |
| <span data-ttu-id="b4721-141">**用户**</span><span class="sxs-lookup"><span data-stu-id="b4721-141">**User**</span></span>    | <span data-ttu-id="b4721-142">覆盖商店或公司</span><span class="sxs-lookup"><span data-stu-id="b4721-142">Overrides store or company</span></span> | <span data-ttu-id="b4721-143">从不</span><span class="sxs-lookup"><span data-stu-id="b4721-143">Never</span></span>                                                         |


[!INCLUDE[footer-include](../includes/footer-banner.md)]