---
title: 客户证书和机密
description: 本主题说明如何在电子开票中设置客户证书和机密。
author: dkalyuzh
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1325cad95e9a6dc470691f5f168439fccaaa78e1
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371521"
---
# <a name="customer-certificates-and-secrets"></a>客户证书和机密

[!include [banner](../includes/banner.md)]

如果您在 Regulatory Configuration Service (RCS) 中已有 Microsoft Azure Key Vault 引用，您可以创建对 Key Vault 证书和机密的引用。 如果您还没有 Key Vault 引用，请参阅[服务环境](e-invoicing-service-environments.md)了解有关如何创建此引用的信息。

## <a name="create-certificates-and-secrets"></a>创建证书和机密

要创建和设置证书和机密，请按照以下步骤操作。

1. 登录您的 RCS 帐户。
2. 在 **全球化功能** 工作区的 **环境** 部分中，选择 **电子开票** 磁贴。
3. 在 **环境设置** 页上的操作窗格上，选择 **服务环境**。
4. 在 **服务环境** 页面上的操作窗格上，选择 **Key Vault 参数**。
5. 在 **Key Vault 参数** 页面上，选择一个 Key Vault 引用，然后在 **证书** 部分，选择 **添加**。
6. 在 **名称** 字段中，输入 Key Vault 证书或机密的名称。 有关详细信息，请参阅[在 Azure 门户中创建 Azure 存储帐户](e-invoicing-create-azure-storage-account-azure-portal.md)。
7. 在 **描述** 字段中，输入描述。
8. 如果您要引用存储在密钥保管库中的证书，在 **类型** 字段中选择 **证书**。 如果您要引用存储在密钥保管库中的机密，选择 **机密**。
9. 选择 **保存**。

> [!NOTE]
> 在某些情况下，您必须使用具有 .cer 文件扩展名的公共证书。 但是，Key Vault 不支持将此类型的证书作为 Key Vault 证书导入和存储。 在这些情况下，您应该将 .cer 文件保存为 Base-64 编码的 X.509 (.CER) 字符串。 然后，在 Key Vault 机密中，存储出现在文件中 **BEGIN CERTIFICATE** 行和 **END CERTIFICATE** 行之间的字符串。 在服务环境中，您仍应创建对 Key Vault 记录的引用并将 **类型** 字段设置为 **证书**。

## <a name="create-a-chain-of-certificates"></a>创建证书链

如果您的国家/地区特定发票需要证书链来应用数字签名或建立与外部 Web 服务的安全（安全套接字层 \[SSL\]）连接，请创建证书链，证书采用以下顺序：

1. 根证书
2. 中间证书
3. 最终用户证书

根证书主管机构 (CA) 是可信的证书来源。 中间 CA 证书是将最终用户证书链接到根 CA 证书的桥梁。

要创建和设置证书链，请按照以下步骤操作。

1. 在 **Key Vault 参数** 页面上的操作窗格上，选择 **证书链**。
2. 选择 **新建** 创建证书链。
3. 在 **名称** 字段中，输入证书链的名称。
4. 在 **描述** 字段中，输入描述。
5. 在 **证书** 部分，选择 **添加** 将证书添加到链中。
6. 使用 **向上** 或 **向下** 按钮更改证书在链中的位置。 将 CA 根证书放在列表顶部，将最终用户证书放在底部。
7. 选择 **保存**。

您可以根据需要在 RCS 中创建任意数量的 Key Vault 引用。 请记住，存储共享访问签名 (SAS) 令牌的机密用于将给定的服务环境链接到 Key Vault 引用。 您可以引用存储在密钥保管库中的 Key Vault 证书和机密，该密钥保管库还包含您在设置服务环境时使用的存储 SAS 令牌的机密。
