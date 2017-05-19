---
title: "为 Retail Modern POS 设置和管理图像"
description: "本文说明设置和管理显示在 Retail Modern POS (MPOS) 中的各个实体的图像所涉及的步骤。"
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 52851
ms.assetid: 5c21385e-64e0-4091-98fa-6a662eb33010
ms.search.region: global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: e144b05ec516d297c3cf81081936d306b9cb9026
ms.contentlocale: zh-cn
ms.lasthandoff: 04/26/2017


---

# <a name="set-up-and-manage-images-for-retail-modern-pos"></a>为 Retail Modern POS 设置和管理图像

[!include[banner](includes/banner.md)]


本文说明设置和管理显示在 Retail Modern POS (MPOS) 中的各个实体的图像所涉及的步骤。

<a name="setting-up-the-media-base-url-and-defining-media-templates-to-configure-the-format-for-image-urls"></a>设置媒体基 URL 和定义媒体模板，以配置图像 URL 的格式
-------------------------------------------------------------------------------------------------

Retail Modern POS (MPOS) 中显示的图像必须在外部承载（Microsoft Dynamics 365 for Operations - Retail 之外）。 通常，可在内容管理系统、内容交付网络 (CDN) 或媒体服务器承载。 然后，MPOS 通过访问目标 URL 来获取并显示相应实体（例如产品和类别）的图像。 若要获取这些外部承载的图像，MPOS 需要这些图像的正确 URL 格式。 您可以通过在通道配置文件中设置**“媒体基 URL”**的值并使用每个实体的**“定义媒体模板”**功能来为图像配置所需的 URL 格式。 您也可以通过使用**“在 Excel 中编辑”**功能来覆盖实体的子集的标准 URL 格式。 **重要注释：**在 Dynamics 365 for Operations - Retail 的当前版本中，您不能再通过使用实体的**默认**属性组中 MPOS 的**图像**属性 XML 来设置 URL 格式。 如果您熟悉 Microsoft Dynamics AX 2012 R3 且正在使用 Dynamics 365 for Operations - Retail 的当前版本，请确保始终使用新的**定义媒体模板**功能设置图像。 请勿使用或修改任何实体（包括产品）的**“默认”**属性组中的**“图像”**属性。 您在图像的**“默认”**属性组中直接作出的更改不会得到反映。 此选项将在未来版本中被禁用。 在以下过程中，将作为示例设置目录实体的图像。 这些过程将帮助确保为使用通用路径的所有目录图像隐式设置正确的图像目标路径。 例如，如果您在外部设置了媒体服务器或 CDN，且希望图像在给定商店的 MPOS 中显示，**“定义媒体模板”**功能可帮助您设置 MPOS 可在其中查找和检索图像的路径。 **注意：**对于此演示数据示例，媒体服务器是在零售服务器上部署的。 但是，您可以在 Dynamics 365 for Operations - Retail 意外的任何地方部署。

### <a name="set-up-the-media-base-url-for-a-channel"></a>为通道设置媒体基 URL

1.  打开 Dynamics 365 for Operations HQ 门户。
2.  单击**零售和商业** &gt; **渠道设置** &gt; **渠道配置文件**。 [![channel-profile1](./media/channel-profile1.png)](./media/channel-profile1.png)
3.  在您的商店用于 MPOS 的通道配置文件中，将**“媒体基 URL”**字段更新为您的媒体服务器或 CDN 的基 URL。 该基 URL 是不同实体的所有图像文件夹共享的 URL 的第一部分。[![channel-profile2](./media/channel-profile2.png)](./media/channel-profile2.png)

### <a name="define-the-media-template-for-an-entity"></a>为实体定义媒体模板

1.  单击**零售和商业** &gt; **目录管理** &gt; **目录图像**。
2.  在**“目录图像”**页面上的“操作”窗格中，单击**“定义媒体模板”**。 在**“定义媒体模板”**对话框的**“实体”**字段中，默认情况下应选择**“目录”**。
3.  在**“媒体路径”**快速选项卡上，输入图像位置的剩余路径。 媒体路径支持**“LanguageID”**作为变量。 例如，对于演示数据，您可以在您的媒体服务器的媒体基 URL (https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer) 下为所有目录图像创建一个**“目录”**文件夹。 然后可以为每种语言创建一个文件夹（例如 en-US 或 fr-FR），然后将相应图像复制到每个文件夹下。 如果您没有各种语言的不同图像，您可以忽略您的文件夹结构中的**“LanguageID”**变量，并直接指向包含目录图像的“目录”文件夹。 **注意：**Dynamics AX 当前版本支持目录、产品和类别实体的**“{LanguageId}”**令牌。 （根据自 Microsoft Dynamics AX 6.x. 以来已生效的现有标准，客户和工作人员实体**“{LanguageID}”**令牌）
4.  对于图像，文件名格式是硬编码为目录名称的，不能更改。 因此，请重命名您的图像，使其具有适当的目录名称，以帮助确保 MPOS 正确处理它们。
5.  在**“文件扩展名”**字段中，根据您拥有的图像的类型选择预期的文件扩展名。 例如，对于演示数据，目录图像扩展名将设置为 .jpg。 （图像文件也已重命名，使其具有类别名称。）
6.  单击**确定**。
7.  为了验证图像的媒体模板是否已正确保存，请在**“目录图像”**页面上再次单击**“定义媒体模板”**。 若要在不关闭**“定义媒体模板”**对话框的情况下验证模板，您可以使用**生成适用于 Excel 的图像 URL** 快速选项卡。 检查图像 URL 的外观，并验证 URL 是否符合之前提到的模板标准。 现在，**“定义媒体模板”**对话框针对使用此通用 URL 路径的所有目录图像隐式设置了图像路径。 此 URL 路径适用于所有目录图像，除非它们被覆盖。 图像路径的第一部分取自您在通道配置文件中定义的媒体基 URL。 路径的其余部分取自您在媒体模板中定义的路径。 这两部分串联起来形成图像位置的完成 URL。 例如，演示数据中一个目录名为“Fabrikam Base Catalog”。 因此，图像名称必须为 Fabrikam Base Catalog.jpg，以便其使用目录名称和模板中的配置的 .jpg 文件扩展名。 在本例中，串连后的 URL 为 https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer/Catalogs/en-US/Fabrikam Base Catalog.jpg。
8.  运行同步作业可将新模板推送到通道数据库，以便 MPOS 使用该模板访问图像。
9.  若要在通道侧更新目录图像的媒体模板，请确保从**零售 IT** &gt; **配送计划**运行**目录作业 1150**。[![catalog1](./media/catalog1.png)](./media/catalog1.png)

## <a name="previewing-an-image-from-the-entity-level"></a>从实体级别预览图像
1.  从 HQ 中的实体项目的页面上，您可以预览使用派生自媒体模板的图像 URL 的图像。 对于本示例，请转到相应目录，然后在“操作”窗格中单击**媒体** &gt; **图像**。 使用下拉列表选择可能具有不同通道配置文件的不同商店。
2.  若要编辑或删除隐式媒体模板，您必须返回到**“目录图像”**页面的**“定义媒体模板”**对话框。
3.  您可以使用**“添加”**和**“删除”**手动更改基于隐式模板并用于特定图像的路径。 有关更多信息，请参阅本文后面的“覆盖实体项目的媒体模板”一节。
4.  完成预览图像和进行所需的更改后，请启动相应商店的 MPOS 实例，查看是否显示目录图像。[![catalog4](./media/catalog4.png)](./media/catalog4.png)

**注意：**您可以对受支持的所有五个实体使用相同的过程：工作人员、客户、目录、类别和产品。 “目录产品”（在目录级别设置的产品）和“通道目录”（在通道级别设置的产品）使用针对产品实体设置的媒体模板。 对于产品媒体模板，您可以选择每个产品要显示的产品图像数。 您也可以为给定产品设置默认图像。 这样，您可以防止 MPOS 中出现空白图像并帮助控制将哪个图像用作产品物料的默认图像。 在以下示例中，每个产品有五个图像，第一个图像设置为默认图像。 变型产品采用与基础产品相同的方式处理。 图像文件的文件名应基于产品编号。 在生成文件名时，也会跳过一些字符。 因此，最好通过使用**生成适用于 Excel 的图像 URL** 部分来验证文件名称。 [![prods](./media/prods.png)](./media/prods.png)  

## <a name="synchronization-jobs-to-send-a-media-template-to-the-channel-side"></a>将媒体模板发送到通道侧的同步作业
对于所有五个受支持的实体（工作人员、客户、目录、类别和产品），无论您何时更新**定义媒体模板**对话框来设置图像，请确保从**零售 IT** &gt; **配送计划**运行目录作业 (1150)。 此作业支持将更新后的媒体模板同步到通道和供 MPOS 使用。 在进行以下任意更改后运行目录作业 (1150)：

-   从**目录图像** &gt; **定义媒体模板**更新目录图像媒体模板。
-   从**员工图像** &gt; **定义媒体模板**更新员工图像媒体模板。
-   从**客户图像** &gt; **定义媒体模板**更新客户图像媒体模板。
-   从**产品图像** &gt; **定义媒体模板**更新产品图像媒体模板。
-   从**类别图像** &gt; **定义媒体模板**更新类别图像媒体模板。 您还必须发布通道。

## <a name="overwriting-the-media-template-for-entity-items"></a>覆盖实体项目的媒体模板
正如您在上一节中所学的，给定实体的媒体模板仅支持一个通用路径。 该路径基于配置的媒体基 URL 和定义的媒体路径。 不过，在很多情况下，零售商希望能将来自不同源的图像用于一个实体中项目的子集。 例如，某个商店将自托管的媒体服务器用于一组目录图像，而将 CDN URL 用于另一组目录图像。 若要针对实体级别的实体图像覆盖基于媒体模板的图像 URL，您可以从**“预览”**页面使用“在 Excel 中编辑”和“手动编辑”功能。

### <a name="overwrite-by-using-edit-in-excel"></a>使用“在 Excel 中编辑”覆盖

1.  单击**零售和商业** &gt; **目录管理** &gt; **目录图像**。
2.  在**“目录图像”**页面上，单击**“定义媒体模板”**。 在**“定义媒体模板”**对话框的**“实体”**字段中，应选择**“目录”**。
3.  在**“媒体路径”**快速选项卡上，注意图像位置。
4.  在**“生成适用于 Excel 的图像 URL”**快速选项卡上，单击**“生成”**。 **重要信息：**无论何时更改媒体模板，您都必须单击**“生成”**才能使用“在 Excel 中编辑”功能。 [![excel1](./media/excel1.jpg)](./media/excel1.jpg) 现在您可以看到基于上一次保存的媒体模板生成的图像 URL 的预览。 [![excel2](./media/excel2.png)](./media/excel2.png) **注意**：为 Excel 生成的 URL 使用已定义的媒体模板的路径和惯例。 这些惯例包括适用于文件名的惯例。 预期是您在 Dynamics AX 以外设置了物理图像，且这些图像可以从派生自您之前定义的媒体模板的 URL 中检索。 您可以使用“在 Excel 中编辑”功能来覆盖这些派生的 URL。
5.  单击**“在 Excel 中编辑”**。
6.  打开 Microsoft Excel 工作表后，在系统提示时单击**“启用编辑”**。
7.  当系统提示时，单击右侧窗格中的**“信任此加载项”**，并等待加载项完成安装。 [![信任此加载项](./media/excel4.jpg)](./media/excel4.jpg)
8.  如果系统提示您登录，请输入您用来登录 HQ 的凭证。 [![登录提示](./media/excel5.png)](./media/excel5.png)
9.  登录后，您应该可以看到各种目录条目的图像 URL 的列表。
10. 您可以针对各种实体项目编辑、添加和删除图像 URL。
11. 对于除产品外的所有实体，您可以覆盖图形 URL。 修改现有图像 URL，使其使用图像的新目标 URL，然后将文件名更新为图像文件的新文件名。 文件名必须唯一，才能帮助保证记录唯一。 [![在 Excel 中覆盖图像 URL](./media/excel6.jpg)](./media/excel6.jpg) **注意：**当您使用“在 Excel 中编辑”功能或实体项目页覆盖产品实体的图像 URL 时，MPOS 将始终将所有媒体模板图像 URL 与被覆盖的图像 URL 一起显示。
12. 完成更改后，单击**“在 Excel 中发布”**以创建新的显式关联实体。
13. 返回到 HQ，并单击**“确定”**。
14. 运行与实体相应的同步作业，并在实体页面上或 MPOS 中查看预览。

#### <a name="creating-new-records"></a>创建新记录

您可以在 Excel 中创建新记录。 不过，请确保提供正确的信息。 例如，若要为某个目录创建一个新条目，要确保目录 ID 和目录名称正确，还要提供唯一文件名。 唯一文件名很重要，因为发布过程中会验证 Excel 中记录的唯一性。 首先复制您要为其创建新记录的目录的详细信息，然后复制记录。 只需更新文件名和 URL，因为其余信息都将是相同的。 若要为产品实体项目创建新记录，您可以使用相同的基本过程。 从 Excel 工作表，复制您要为其创建新记录的产品的现有记录，然后替换图像 URL 和文件名。 确保文件名是唯一的。

#### <a name="deleting-an-existing-record"></a>删除现有记录

仅可删除被覆盖的图像 URL 记录。 删除某个图像并完成同步后，该图像便不会再出现在**“预览”**页面上或 MPOS 中。 不能删除从媒体模板派生的图像 URL 记录，因为这些记录每次都将始终从媒体模板中派生出来。

### <a name="overwrite-from-the-entity-level-preview-page"></a>从实体级别“预览”页面覆盖

对于除产品外的所有实体，您可以覆盖从**“预览”**页面在实体项目级别上覆盖给定实体项目的图像 URL。 对于产品实体，您可以使用“目录产品”实体页面。 此示例显示如何覆盖目录图像。

1.  单击**目录** &gt; **媒体** &gt; **图像**，然后选择要更新的目录图像。
2.  单击**“添加”**，然后输入该图像 URL，以覆盖媒体模板 URL。
3.  如果您希望此图像在目录的 MPOS 中显示，可以将其设置为默认图像。
4.  单击“**OK**”。 此时此目录图像的图像 URL 已更新，且会显示预览。 [![preview3](./media/preview3.png)](./media/preview3.png)
5.  您也可以在**“目录图像”**库页面上查看所有被覆盖的图像 URL 的图像预览。

**[![preview-4](./media/preview-4.png)](./media/preview-4.png)注意：**目前，库不会显示媒体模板图像 URL 的图像预览。 对于目录、工作人员、客户和类别实体，如果用户通过此页面明确提供 URL，我们建议您指明哪个图像是默认图像，因为零售服务器客户端仅对每个目录、客户、工作人员和类别显示一个图像。 如果用户未指定默认图像，系统将确定默认图像并将其发送到零售服务调用方（MPOS 或 Ecommerce）。

### <a name="overwrite-the-image-url-for-catalog-product-images-from-the-preview-page"></a>从“预览”页面覆盖目录产品图像的图像 URL

若要覆盖目录产品图像的图像 URL，您必须使用**“预览”**页面。 不能使用“在 Excel 中编辑”功能。

1.  若要在目录级别上覆盖产品图像，请选择一个目录，然后选择要为其覆盖图像的产品。
2.  单击**“属性”**。
3.  在下一页上，选择**“图像”**，然后单击**“编辑”**。 “**预览**”页面以滑块对话框形式打开。
4.  单击**“添加”**，然后用新的 URL 覆盖图像 URL。
5.  单击“**OK**”。 现在您可以看到新图像的预览，并且可以将其设置为默认图像。

**[![cat3](./media/cat3.png)](./media/cat3.png)注意：**关联类别图像后，您必须发布通道并运行通道作业才能帮助确保将更改发布到通道数据库。

## <a name="setting-up-images-to-appear-in-offline-mode-for-mpos"></a>将图像设置为在 MPOS 的脱机模式下显示
MPOS 可以在联机模式下运行（当 MPOS 连接到零售服务器时），也可以在脱机模式下运行（当没有零售服务器或网络连接，且交易记录存储在本地脱机数据库中时）。 当 MPOS 在脱机模式下运行时，它不能从外部图像服务器获取要在零售服务器中显示的图像，因为零售服务器连接已丢失。 不过，您仍可以设置图像，使其在 MPOS 以脱机模式运行时显示。

### <a name="set-up-product-images-to-appear-in-offline-mode-for-mpos"></a>将产品图像设置为在 MPOS 的脱机模式下显示

通过将所需的物理图像上载到基本产品图像中，可以设置必须在脱机模式下使用的产品图像。

1.  单击**产品信息管理** &gt; **产品** &gt; **产品**。
2.  选择要为其设置脱机图像的产品。
3.  单击**“编辑”**，然后单击右角的箭头以显示右窗格。
4.  在**“产品图像”**快速选项卡上，单击**“更改图像”**，然后上载要在脱机模式下用于所选产品的物理图像。
5.  保存并关闭页面。
6.  当 MPOS 处于联机模式时，在 HQ 中运行目录作业，以确保至少一次将数据发送到脱机数据库。
7.  将 MPOS 置于脱机模式。 您应该可以在 HQ 中看到您为特定产品上载的图像。 [![offline1](./media/offline1.png)](./media/offline1.png)

 

### <a name="set-up-catalog-category-employee-and-customer-images-to-appear-in-offline-mode-for-mpos"></a>将目录、类别、员工和客户图像设置为在 MPOS 的脱机模式下显示

通过将所需图像的目标链接添加到库并将该图像设置为所选实体的默认图像，可以设置必须在脱机模式下使用的目录、类别、员工和客户图像。

1.  转到目录，然后在“操作”窗格上单击**媒体** &gt; **图像**。
2.  按照**“从实体级别“预览”页面覆盖”**一节中的步骤添加外部图像 URL。
3.  通过选中网格中列出的图像的复选框，将此图像设置为该目录的默认图像。
4.  运行目录作业。 现在，此图像将在 MPOS 中用作该目录的脱机图像。
5.  对于其他实体（例如类别、员工和客户），请按照类似流程操作。

[![offline2](./media/offline2.png)](./media/offline2.png)    




