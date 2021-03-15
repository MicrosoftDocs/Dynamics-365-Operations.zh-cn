---
title: Modern POS (MPOS) 和 Cloud POS 中的演示数据屏幕布局
description: 本主题提供了有关 Dynamics 365 Commerce 中销售点 (POS) 体验的演示数据集包含的屏幕布局信息。
author: josaw1
manager: AnnBe
ms.date: 10/05/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: e55db57089c8ea5bd3def25d79d9c65a3165526c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982706"
---
# <a name="demo-data-screen-layouts-in-modern-pos-mpos-and-cloud-pos"></a>Modern POS (MPOS) 和 Cloud POS 中的演示数据屏幕布局

[!include [banner](includes/banner.md)]

本主题提供了有关 Dynamics 365 Commerce 中销售点 (POS) 体验的演示数据集包含的屏幕布局信息。

## <a name="overview"></a>概览

包括在 Commerce 演示数据中的示例屏幕布局提供为各个零售段、商店工作人员角色和设备优化的内容。 一个布局可以包含多个布局大小和按钮网格组合，以在商店工作人员在设备和工作站之间移动时帮助确保覆盖范围。 此主题突出介绍了这些布局之间的区别、它们提供的操作和整体体验。

![跨设备演示数据布局](../commerce/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a>屏幕布局 ID 的分类

若要查找屏幕布局，请转到 **Retail 和 Commerce** \> **渠道设置** \> **POS 设置** \> **POS** \> **屏幕布局**。

![屏幕布局页面](../commerce/media/demo-screen-layouts-fig-2-1.png)

屏幕布局 ID 最多可以有 10 个字符。 ID 是一个包括三个信息的字符串，按以下顺序：

1. 公司
2. 布局版本
3. 人员

### <a name="company"></a>公司

| 字母 | 公司         |
|--------|-----------------|
| A      | Adventure Works |
| F      | Fabrikam        |
| C      | Contoso         |

### <a name="layout-version"></a>布局版本

| 版本号 | 说明                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| 3              | 支持各种设备和纵横比的多个屏幕尺寸的基本版本 |
| 3.1            | 具有其他 **建议的产品** 面板支持的基础版本        |
| 4              | 扩展 Fabrikam 更新布局的扩展版本                                  |

### <a name="persona"></a>人员

| 缩写 | 人员       | 内容 |
|--------------|---------------|----------|
| CSH          | 出纳       | 出纳布局包括所有与交易相关的操作，如客户订单、退货、折扣、失效和礼品卡。 这些布局还包括库存管理的日常任务，如价格检查、库存查找和存货盘点。 基本的班次管理还为初始金额、暂停班次和打卡时间提供。 |
| MGR          | 商店经理 | 商店经理布局包括在出纳布局中找到的所有交易相关操作，而且包括税覆盖。 这些布局还包括库存管理的日常任务，如价格检查、库存查找和存货盘点。 班次管理为开始、暂停和结束班次提供。 此外，这些布局还包括输入、删除、钱币清点以及金库投箱和银行投箱的开票人操作。 最后，这些布局包括对绩效报表的访问，以及启用要打印的 X 和 Z 报表。 |
| STK          | 保管员   | 保管员布局针对库存管理进行了优化。 它们包括对价格检查、库存查找、领料和收货、库存盘点和配套件拆卸的日常任务的访问。 这些布局还为时钟和暂停班次提供基本班次操作。 尽管这些布局主要用于后勤办公室任务，保管员与出纳的交易记录屏幕具有相同的操作。 |

### <a name="example-layout"></a>示例布局

这是 Fabrikam 公司、布局版本 4 和人员为商店经理的屏幕布局 ID 的示例：

F4MGR

下图显示 Fabrikam 商店经理的欢迎屏幕的示例。

![Fabrikam 商店经理的欢迎屏幕](../commerce/media/demo-screen-layouts-fig-2-2.png)

## <a name="layout-sizes"></a>布局大小

### <a name="full-vs-compact-layouts"></a>完整型布局与紧凑型布局

屏幕布局同时具有完整设备和紧凑设备的配置。 因此，用户可以被分配一个屏幕布局，而该屏幕布局支持商店内的多种尺寸和外形。

- **现代 POS - 完整型** – 通常，完整型布局最适合较大显示器，如台式机显示器或平板电脑。 用户可以选择布局包含的元素 UI，指定这些元素的尺寸和位置，并配置它们的详细属性。 完整型布局同时支持垂直配置和水平配置。
- **现代 POS - 紧凑型** - 通常，紧凑型布局最适合手机或小平板电脑。 对于紧凑型设备，设计功能受到限制。 用户可以为收据窗格和总计窗格配置列和字段。

### <a name="screen-resolutions-that-are-provided"></a>提供的屏幕分辨率

下表显示为典型的屏幕分辨率提供的布局大小。

| 布局类型 | 分辨率 | 纵横比 | 目标显示          |
|-------------|------------|--------------|-------------------------|
| 压缩\*   | 480 × 853  | 16:9         | 电话                  |
| 完全        | 1024 × 768 | 4:3          | 平板电脑                 |
| 完全\*      | 1280 × 720 | 16:9         | 平板电脑                 |
| 完全        | 1366 × 768 | 16:9         | 平板电脑，较大屏幕 |
| 全尺寸        | 1440 × 960 | 3:2          | 平板电脑，较大屏幕 |
| 全尺寸\*      | 1536 × 864 | 16:9         | 平板电脑，较大屏幕 |

\*这些额外的布局大小仅在 Adventure Works 和 Fabrikam 布局中提供。

> [!TIP]
> POS 基于与可用于当前应用窗口的屏幕分辨率最接近的大小自动选择布局大小。 若要查找当前使用的屏幕布局 ID 和布局分辨率，在 Modern POS (MPOS) 或 Retail Cloud POS (CPOS) 中，打开 **设置** 页，然后在 **会话信息** 部分查找。 您还可以看到当前应用程序或浏览器框架的实际窗口分辨率。 在具有此信息后，可以查找布局内容的源，方法是转到 **渠道设置** \> **POS 设置** \> **POS** \> **屏幕布局**。

![Commerce 和 POS 中的屏幕布局和布局分辨率/大小](../commerce/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a>公司和品牌

每个虚构的公司面向不同的零售段，包含为公司的市场调整的产品目录。 每家公司都具有伴随其产品的独一无二的视觉品牌。 品牌元素包括个性色、深色主题或浅色主题，以及提供逼真体验的附带照片。

### <a name="company-segment-and-visual-characteristics"></a>公司细分市场和视觉特征

| 公司         | 库位 | 分段        | 个性 | 主题 |
|-----------------|----------|----------------|--------|-------|
| Adventure Works | 西雅图  | 体育用品 | 蓝色   | 深色  |
| Fabrikam        | 旧金山  | 风格        | 绿色  | 浅色 |
| Contoso         | 波士顿   | 电子    | 红色    | 深色  |

> [!NOTE]
> Adventure Works 和 Fabrikam 为两个旗舰品牌。 Contoso 可用，但并不提供所有布局。

下图显示了三个虚构公司的欢迎页面和交易页面示例。

### <a name="adventure-works"></a>Adventure Works

![演示数据：Adventure Works 的欢迎页面](../commerce/media/demo-screen-layouts-fig-4-1a.png)

![演示数据：Adventure Works 的交易页面](../commerce/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a>Fabrikam

![演示数据：Fabrikam 的欢迎页面](../commerce/media/demo-screen-layouts-fig-4-2a.png)

![演示数据：Fabrikam 的交易页面](../commerce/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a>Contoso

![演示数据：Contoso 的布局](../commerce/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a>用户登录矩阵

已为各个屏幕布局提供了用户。 通过使用下表，您应该能够访问任何屏幕。 使用相应的操作员 ID 登录。

| 公司         | 屏幕布局 ID | 人员       | 操作员 ID           |
|-----------------|------------------|---------------|------------------------|
| Adventure Works | A3MGR            | 商店经理 | 000154、000137、000073 |
| Adventure Works | A3CSH            | 出纳       | 000150、000175、000165 |
| Adventure Works | A3STK            | 保管员   | 000155、000181、000152 |
| Fabrikam        | F4MGR            | 商店经理 | 000160、000713         |
| Fabrikam        | F3CSH            | 出纳       | 000161、000113、000114 |
| Fabrikam        | F3STK            | 保管员   | 000164、000112、000123 |
| Contoso         | C3MGR            | 商店经理 | 000100、000111         |
| Contoso         | C3CSH            | 出纳       | 000110、000120         |
| Contoso         | 不适用   | 保管员   | 不适用         |

> [!TIP]
> 为了达到最佳效果，请在相应的商店位置激活收银机，然后将公司设置为您计划在登录时使用的人员的公司。 这样，您可以帮助确保视觉形象和品牌图像与整个体验一致。 例如，如果您有兴趣查看出纳的 Fabrikam 布局，则应该在休斯敦商店激活收银机。

<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail and Commerce \> Channel setup \> POS setup \> POS \> Images**. -->

<!-- ![Images in Dynamics 365 Commerce](../commerce/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../commerce/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->


[!INCLUDE[footer-include](../includes/footer-banner.md)]