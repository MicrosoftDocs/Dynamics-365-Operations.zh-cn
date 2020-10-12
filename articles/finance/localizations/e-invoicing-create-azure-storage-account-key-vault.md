---
title: 创建 Azure 存储帐户和密钥保管库
description: 本主题说明如何创建 Azure 存储帐户和密钥保管库。
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: b8e39539f767cc2944a9a7fdda09121921c64763
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2020
ms.locfileid: "3835914"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a>创建 Azure 存储帐户和密钥保管库

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


电子开票附加产品服务负责将所有业务数据存储在您的公司拥有的 Microsoft Azure 资源中。 为确保服务正常运行，并且仅电子开票附加产品能够访问此附加产品所需的和生成的所有业务数据，您必须创建两个主要的 Azure 资源：

- 用于存储电子发票的 Azure 存储帐户（Blob 存储）
- 用于存储证书和存储帐户的统一资源标识符 (URI) 的 Azure 密钥保管库

> [!NOTE]
> 必须专门分配专用的密钥保管库资源和客户 Blob 存储，以与电子开票附加产品一起使用。

## <a name="prerequisites"></a>先决条件

您必须确保先完成以下任务，然后才能完成本主题中的步骤：

- 在 Azure 中创建密钥保管库资源。 有关详细信息，请参阅[关于 Azure 密钥保管库](https://docs.microsoft.com/azure/key-vault/general/overview)。
- 创建 Azure 存储帐户（Blob 存储）。 有关详细信息，请参阅[维护 Azure 存储帐户](https://docs.microsoft.com/azure/storage/blobs/)。

## <a name="overview"></a>概览

在本主题中，您将完成两个主要步骤：

- 设置 Azure 存储帐户以获取存储帐户 URI。
- 设置密钥保管库以存储存储帐户 URI。

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a>设置 Azure 存储帐户以获取存储帐户 URI

1. 打开您计划与电子开票附加产品一起使用的存储帐户。
2. 转到 **Blob 服务** \> **容器**，创建一个新容器。
3. 为容器输入名称，然后将**公共访问级别**字段设置为**专用(无匿名访问)**。
4. 打开容器，转到**设置 \> 访问策略**。
5. 选择**添加策略**添加存储的访问策略。
6. 根据需要设置**标识符**和**权限**字段。 在**权限**字段中，您应该选择所有权限。

    ![授予 Blob 存储权限](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. 输入开始日期和到期日期。 到期日期应该在将来。
8. 选择**确定**保存策略，然后保存对容器进行的更改。
9. 返回到存储帐户，打开**存储资源管理器(预览)**。
10. 用鼠标右键单击容器，然后选择**获取共享访问签名**。
11. 在**共享访问签名**对话框中，将值复制并存储到 **URI** 字段中。 此值将在下一个过程中使用，将称为*共享访问签名 URI*。

    ![选择并复制 URI 值](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a>设置密钥保管库以存储存储帐户 URI

1. 打开您打算与电子开票附加产品一起使用的密钥保管库。
2. 转到**设置** \> **密码**，然后选择**生成/导入**创造新密码。
3. 在**创建密码**页上，在**上载选项**字段中，选择**手动**。
4. 输入密码的名称。 此名称将在 Regulatory Configuration Service (RCS) 中的服务设置期间使用，将称为*密钥保管库密码名称*。
5. 在**值**字段中，选择**共享访问签名 URI**，然后选择**创建**。
6. 设置访问策略，以授予电子开票附加产品访问您创建的密码的正确安全访问级别。 转到**设置 \> 访问策略**，选择**添加访问策略**。
7. 为**获取**和**列出**操作设置密码权限。

    ![授予服务访问权限](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. 为**获取**和**列出**操作设置证书权限。

    ![授予证书权限](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. 在**主体**对话框中，通过添加**电子开票附加产品**选择主体。
10. 选择**添加**，然后选择**保存密钥保管库更改**。
11. 在**概览**页上，复制密钥保管库的 **DNS 名称**值。 此值将在 RCS 中的服务设置期间使用，将称为*密钥保管库 URI*。
