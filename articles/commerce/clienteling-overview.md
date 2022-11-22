---
title: 客户服务解决方案概览
description: 本文提供商店应用程序中可用的新客户服务解决方案功能的概览。
author: bebeale
ms.date: 11/16/2022
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom:
- "260624"
- intro-internal
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2018-10-01
ms.openlocfilehash: fc7daeb27c25efa21fd34b0456af8892074056d5
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785037"
---
# <a name="clienteling-overview"></a>客户服务解决方案概览

[!include [banner](includes/banner.md)]


许多零售商，尤其是高端专业零售商，都希望其销售助理与重要客户建立长期关系。 助理需要了解这些客户的好恶、购买历史、产品偏好以及重要日期，例如周年纪念日和生日。 助理需要一个可以捕获这些信息并在需要时轻松找到它们的地方。 如果可以在单个视图中获得这些信息，助理则可以轻松地定位满足特定条件的客户。 例如，他们可以找到所有喜欢购买手提包的客户，或者近期有重要事件（例如生日或周年纪念日）的客户。

以下视频演示了 Dynamics 365 Commerce 中客户服务的示例场景。


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE5bMSP]

## <a name="client-book"></a>客户端帐簿

在 Microsoft Dynamics 365 Commerce 中，零售商可以使用客户手册功能来帮助售货员与重要客户建立长期关系。

客户手册包括显示每个客户联系方式的客户卡，以及另外三个零售商在 Headquarters 中定义和配置的属性。 零售商可以决定销售助理应了解的关于客户的三个最重要事项。 例如，珠宝零售商可能希望包括重要的日期，例如周年纪念日或生日，因为这些日期是人们可能会购买更多珠宝的场合。 同样，时装零售商可能希望包括顾客的首选购物兴趣和品牌。

客户手册还允许销售助理筛选列表，以便它仅显示满足特定条件的客户。 例如，新的鞋子系列已经到达商店，助理想通知想要购买鞋子的客户。 在这种情况下，助理可以筛选客户手册以找到相关客户，然后采取进一步的措施。

如果由于某个原因不再将某个客户视为重要客户，因此不应对其进行密切管理，销售助理可以将其从客户手册中删除。

一些零售商不想在销售助理级别管理客户。 而是希望在商店级别管理重要客户的列表。 这些零售商可以从商店客户手册中查看客户。 通过使用此选项，零售商可以从通讯簿与当前商店的通讯簿匹配的所有销售助理的客户手册中查看客户。 这样，如果助理在法人的多个商店工作，客户手册将显示所有这些商店的客户。 此功能支持其他功能。 例如，可以将客户从一个助理重新分配给另一个助理。 当助理转岗或离开公司时，此功能很有用。

每个销售助理可以在每个法人有一个客户手册，助理可以在其客户手册中添加一个或多个客户。 在 Commerce 中，每个客户当前只能被添加到一个客户手册中。 但是，Microsoft 计划增加功能，使一个客户可以被添加到多个客户手册中。

> [!NOTE]
> 与客户搜索不同，客户手册不会根据商店的通讯簿筛选客户记录。

## <a name="activities-and-notes"></a>活动和注释

在线渠道为零售商提供了了解客户偏好的方式，而无需客户明确提供这些信息。 与之相比，当客户与商店中的销售助理互动时，他们会明确共享有关其偏好的信息。 遗憾的是，销售结束后，这些信息可能会丢失。 但是，如果记录了这些信息，则可以帮助零售商更好地了解客户，从而帮助他们提供更好的建议和更好的整体购物体验。

为了捕获客户共享的关键信息，销售助理不仅可以使用客户手册属性，还可以使用活动和注释功能。 零售商可以配置活动类型，例如有关进店、电子邮件地址，电话号码和约会的信息。 可以在销售点 (POS) 以时间线格式查看助理创建的活动。 也可以在“总部”的 **所有客户 \> 常规** 页面上的 **活动** 选项卡上查看它们。

销售助理还可以使用注释来捕获可以在每次交互之前参考的一般客户信息。 这些注释保存在“总部”中，可以在客户资料或呼叫中心的客户详细信息页面查看。

> [!NOTE]
> 当前，为法人工作的任何销售助理都可以查看所有注释和活动，并且可以查看客户详细信息页面。 注释和活动不仅限于将客户添加到客户手册中的助理。

## <a name="integration-with-dynamics-365-customer-insights"></a>与 Dynamics 365 Customer Insights 的集成

通过使用 Dynamics 365 Customer Insights 应用程序，零售商可以聚合来自客户用来与零售商品牌进行交互的各个系统的数据。 然后，可以使用此数据生成客户的单一视图并获得见解。 Customer Insights 与 Commerce 的集成使零售商可以选择一种或多种应在客户手册的客户卡上显示的度量。 例如，零售商可以使用 Customer Insights 中的数据来计算客户的“流失概率”，并定义“下一个最佳行为”。 如果将这些值定义为度量，它们可以显示在客户卡上，并可以向销售助理提供重要信息。 有关 Customer Insights 的详细信息，请参阅 [Dynamics 365 Customer Insights](/dynamics365/ai/customer-insights/overview) 文档。 有关度量的详细信息，请参阅[度量](/dynamics365/ai/customer-insights/pm-measures)。

## <a name="set-up-clienteling"></a>设置客户服务解决方案

要打开您环境中的客户服务解决方案功能，请按照下列步骤操作。

1. 在 **功能管理** 工作区，按 **零售和商业** 模块筛选功能。

    ![Commerce 模块的功能列表中的客户服务解决方案。](./media/Enable_clienteling.png "“零售和商业”模块的功能列表中的客户服务解决方案")

2. 通过选择 **立即启用**，开启 **客户服务解决方案** 功能。
3. 在 **商业参数** 页面上的 **编号规则** 选项卡上，选择 **客户手册标识符** 行。 然后，在 **编号规则代码** 字段中，选择一个编号规则。 系统将使用此编号规则为客户手册分配 ID。
4. 选择 **保存**。
5. 创建一个新的属性组，其中包含要为客户手册中管理的客户捕获的属性。 相关说明请参阅[属性和属性组](./attribute-attributegroups-lifecycle.md)。

    - 将所需的属性定义为 **可细化**。 然后，销售助理可以使用这些属性来筛选其客户手册。
    - 设置这些属性的显示顺序。 此显示顺序确定应在客户手册的客户卡上显示哪些属性。 显示顺序 1 被视为比显示顺序 2 更高。 因此，显示顺序为 1 的属性将显示在显示顺序为 2 的属性之前。

    > [!NOTE]
    > 您可以在同一页面上提供 Customer Insights。 但是，出于身份验证目的，必须创建一个 Azure 应用程序 ID 和密钥。 （有关要求的信息，请参阅本文后面的[打开 Customer Insights 与 Commerce 的集成](#turn-on-the-integration-of-customer-insights-with-commerce)一节。）如果 Customer Insights 已打开，并且您选择了应在客户卡上显示的一个或多个度量，则这些度量将首先显示。 接下来，将基于显示顺序显示客户手册属性组。 例如，如果您从 Customer Insights 选择两个度量，这两个度量和一个客户手册属性将显示在客户卡上。 （显示的客户手册属性将是显示顺序最高的属性。）

6. 在 **商业参数** 页面上，在 **客户服务解决方案** 选项卡上的 **客户手册属性组** 字段中，选择刚才创建的属性组。

    ![已选择客户手册属性组。](./media/Client%20book%20attributes.png "已选择客户手册属性组")

7. 要捕获 POS 上发生的活动，请在 **活动类型** 页面定义活动类型（**Retail 和 Commerce \> 客户 \> 活动类型**）。

    > [!NOTE]
    >  Commerce Scale Unit 在首次进行实时调用时会提取活动类型。 提取活动后，它们将被缓存几个小时。 如果更改活动类型，请等待直到缓存不再有效。 或者，对于非生产环境，重新启动 Commerce Scale Unit 服务。

8. 在适当的 POS 屏幕布局中添加两个按钮，以便销售助理可以查看自己的客户手册和商店客户手册。 （商店客户手册包括与商店共享通讯簿的所有助理的所有客户手册中的客户。）相应的操作被分别命名为 **查看客户手册中的客户** 和 **查看商店客户手册中的客户**。 与客户手册有关的三个其他操作可用。 这些操作确定哪些助理可以从客户手册中添加、删除和重新分配客户。 它们分别被命名为 **将客户添加到客户手册中**、**从客户手册中删除客户** 和 **将客户重新分配到客户手册**。
9. 运行以下配送计划作业：1040、1150、1110 和 1090。

完成此过程后，销售助理可以在 POS 上打开客户详细信息页面，然后将客户添加到他们的客户手册中，查看和捕获客户的活动和注释，并通过使用客户和客户手册属性筛选客户手册来定位客户。 下图显示了一个客户手册的示例。

![客户手册的示例。](./media/client_book.png "客户手册的示例")

## <a name="turn-on-the-integration-of-customer-insights-with-commerce"></a>打开 Customer Insights 与 Commerce 的集成

要打开 Customer Insights 与 Commerce 的集成，必须确保在预配 Commerce 的租户中有一个 Customer Insights 的活动实例。 您还必须有具有 Azure 订阅的 Azure Active Directory (Azure AD) 用户帐户。

请按照以下步骤设置集成。

1. 在 Azure 门户中，注册一个新应用程序并记下应用程序名称、应用程序 ID 和密码。 此信息将用于 Commerce 和 Customer Insights 之间的服务对服务身份验证。 请以安全方式记下密码，在密钥保管库中进行保存时需要用到。 对于以下示例，请分别将 CI_Access_name、CI_Access_AppID、CI_Access_Secret 用作应用程序名称、应用程序 ID 和密码。 有关详细信息，请参阅[快速入门：向 Microsoft 身份平台注册应用程序](/azure/active-directory/develop/quickstart-register-app)。

    > [!IMPORTANT]
    > 采取措施，以便您记住在密钥到期之前对其进行更改。 否则，集成将意外停止。

2. 转到您的 Customer Insights 实例并搜索上面创建的应用程序的名称（在本示例中为“CI_Access_name”）。
3. 创建一个 Azure 密钥保管库，并记下名称和 URL（在此示例中为“KeyVaultName”、“KeyVaultURL”）。 有关说明，请参阅[快速入门：使用 Azure 门户设置密钥以及从 Azure 密钥保管库检索密钥](/azure/key-vault/quick-create-portal)。
4. 将密码（在本示例中为“CI_Access_Secret”）保存在保管库中。 当此密码存储在保管库中时，密码将获得一个名称。 记下密码的名称（在此示例中为“SecretName”）。
5. 若要从 Azure 密钥保管库访问密码，您需要使用应用程序 ID 和密码（在本示例中为“KeyVault_Access_AppID”和“KeyVault_Access_Secret”）创建另一个应用程序。 以安全方式记下密码，它不会再显示。
6. 接下来，您需要授予应用程序使用 API 从 Commerce 访问密钥保管库的权限。 在 Azure 门户中转到应用程序页面。 在 **管理** 部分下，选择 **API 权限**。 添加权限以访问 **Azure 密钥保管库**。 为此权限，选择 **访问政策**。 模板选择 **密码管理**，然后选择 **获取**、**列出**、**解密** 和 **加密** 选项。 
5. 在 Commerce headquarters 中，转到 **系统管理 \> 设置 \> 密钥保管库参数**，然后输入密钥保管库所需的信息。 然后，在 **密钥保管库客户端** 字段中，输入您在步骤 4 中使用的应用程序 ID，以便 Commerce 可以访问密钥保管库中的密钥。
6. 要将您在步骤 1 中创建的应用程序添加到安全应用程序列表（有时称为安全列表）中，请转到 Customer Insights，并选择对应用程序的 **查看** 访问权限。 有关说明，请参阅[权限](/dynamics365/ai/customer-insights/pm-permissions)。
7. 在 Commerce HQ 中的 **系统管理 > 设置 > 密钥保管库参数** 页，如下所述更新字段： 

- **密钥保管库 URL**：“KeyVaultURL”（来自上面的步骤 3）。
- **密钥保管库客户端**：“KeyVault_Access_AppID”（来自上面的步骤 5）。
- **密钥保管库密钥**：“KeyVault_Access_Secret”（来自上面的步骤 5）。
- 在 **密码** 部分下：
    - **名称**：任何名称，例如，“CISecret”。
    - **描述**：任何值。
    - **机密**：**保管库**：`//<Name of key vault>/<name of secret>>`在此示例中，它将是 `vault://KeyVaultName/SecretName`。

更新字段后，选择 **验证** 确保密码可以被 Commerce 应用程序访问。

8. 在 Commerce 中，在 **Commerce 参数** 页上的 **客户服务解决方案** 选项卡上，在 **Dynamics 365 Customer Insights** 快速选项卡上，将 **应用程序 ID** 设置为“CI_Access_AppID”（来自上面的步骤 1）。 对于 **密码名称**，选择在上面的步骤 7 中输入的密码的名称（“CISecret”）。 将 **启用 Customer Insights** 选项设置为 **是**。 如果由于任何原因设置失败，将显示一条错误消息，此选项将设置为 **否**。 

您可以在 Customer Insights 中拥有多个环境，例如测试和生产环境。 在 **环境实例 ID** 字段中，输入适当的环境。 在 **备用客户 ID** 字段中，在 Customer Insights 中输入映射到客户帐号的属性。 （在 Commerce 中，客户帐号是客户 ID。）其余三个属性是将显示在客户手册中客户卡上的度量。 您最多可以选择三个度量在客户卡上显示。 不过，您无需选择任何度量。 如前所述，系统将首先显示这些值，然后显示客户手册属性组的值。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
