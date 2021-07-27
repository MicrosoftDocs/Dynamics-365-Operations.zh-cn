---
title: 压缩在电子报告中生成的大型文档
description: 本主题说明如何压缩使用电子报告 (ER) 格式生成的大型文档。
author: NickSelin
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERFormatDestinationTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 5b58a9345b83219296a3570e7bf653ef8624b7a1
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6357634"
---
# <a name="compress-large-documents-that-are-generated-in-electronic-reporting"></a>压缩在电子报告中生成的大型文档 

[!include [banner](../includes/banner.md)]

您可以使用[电子报告 (ER) 框架](general-electronic-reporting.md)配置一个获取交易记录数据以生成传出文档的解决方案。 这生成的文档可能很大。 生成此类文档时，将使用[应用程序对象服务器 (AOS)](../dev-tools/access-instances.md#location-of-packages-source-code-and-other-aos-configurations) 内存保留它。 在某些时候，之后必须从 Microsoft Dynamics 365 Finance 应用程序下载该文档。 当前，在 ER 中生成的单个文档的最大大小限制为 2 GB。 此外，Finance 目前[限制](https://fix.lcs.dynamics.com/Issue/Details?kb=4569432&bugId=453907&dbType=3)下载文件的大小为 1 GB。 因此，您必须配置一个 ER 解决方案，以减少超过这些限制的可能性，使用此解决方案时，您将收到 **流太长** 或 **数学运算中溢出或下溢** 异常。

配置解决方案时，可以通过添加 **文件夹** 类型的根元素来压缩由其嵌套元素生成的内容，以在 Operations 设计器中调整 ER 格式。 压缩是“及时”进行的，因此可以减少高峰内存使用量和将要下载的文件大小。

> [!NOTE]
> 文件压缩会占用额外的 CPU 用量百分比。

有关此方法的详细信息，请完成本主题中的示例。

## <a name="example-compress-an-outbound-document"></a>示例：压缩传出文档

此示例显示了分配了 **系统管理员** 或 **电子报告功能顾问** 角色的用户如何配置 ER 格式来压缩生成的文档。

### <a name="prerequisites"></a>先决条件

在完成本主题中的过程之前，必须完成以下步骤。

1. [激活配置提供程序](er-defer-xml-element.md#activate-a-configuration-provider)。
2. [导入示例 ER 配置](er-defer-xml-element.md#import-the-sample-er-configurations)。
3. [查看导入的格式](er-defer-xml-element.md#review-the-imported-format)。

> [!NOTE]
> 当前，格式结构从 **文件** 类型的 **报表** 元素开始，包含 XML 元素。 因此，将以 XML 格式生成传出文档，不会使用压缩。

### <a name="generate-an-er-format-to-get-an-uncompressed-document"></a>生成 ER 格式以获取未压缩的文档

1. [运行导入的格式](er-defer-xml-element.md#run-the-imported-format)。
2. 请注意，以 XML 格式生成的文档的大小为 3 KB。

    ![未压缩的传出文档预览。](./media/er-compress-outbound-files1.png)

### <a name="modify-the-format-to-compress-the-generated-output"></a>修改格式以压缩生成的输出

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页上的配置树中，展开 **用于了解推迟的元素的模型**。
3. 选择 **用于了解推迟 XML 元素的格式** 配置。
4. 选择 **设计器** 修改格式结构。
5. 在 **格式设计器** 页的 **格式** 选项卡上，选择 **添加根** 添加根格式元素。
6. 在 **添加** 对话框中，选择 **常见\\文件夹**。
7. 选择 **确定** 确认添加新的根元素。
8. 选择 **保存**。

> [!NOTE]
> 格式结构从 **文件夹** 类型的元素开始。 此元素将作为压缩 (zip) 文件生成输出。 将由 **报表** 元素生成的文档放入传出 zip 文件时，其内容将被压缩以减小传出文件的大小。

### <a name="generate-an-er-format-to-get-a-compressed-document"></a>生成 ER 格式以获取压缩文档

1. 在 **格式设计器** 页上，选择 **运行**。
2. 下载 Web 浏览器提供的 zip 文件，然后将其打开以进行检查。
3. 请注意，以 ZIP 格式生成的文档的大小为 1 KB。

    > [!NOTE] 
    > 此 zip 文件保留的 XML 文件的压缩率为 87%。 压缩率取决于要压缩的数据。

    ![压缩的传出文档预览。](./media/er-compress-outbound-files2.png)

> [!NOTE]
> 如果为生成输出的格式元素（此示例中的 **报表** 元素）配置了 ER [目标](electronic-reporting-destinations.md)，将跳过输出压缩。

## <a name="additional-resources"></a>其他资源

[电子报告 (ER) 概览](general-electronic-reporting.md)

[电子报告 (ER) 目标](electronic-reporting-destinations.md)

[推迟执行电子报告格式的 XML 元素](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]