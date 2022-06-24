---
title: 使用代码签名证书对 MPOS .appx 文件签名
description: 本文介绍如何使用代码签名证书对 MPOS 进行签名。
author: mugunthanm
ms.date: 05/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: 28021
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-09-2019
ms.openlocfilehash: 7e998514081cad1c7302aacb1cd74373f896f2d0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865961"
---
# <a name="sign-the-mpos-appx-file-with-a-code-signing-certificate"></a>使用代码签名证书对 MPOS .appx 文件签名

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

要安装 Modern POS (MPOS)，您必须使用来自受信任提供商的代码签名证书对 MPOS 应用进行签名，并在当前用户的受信任根文件夹下安装了 MPOS 的所有计算机上安装相同的证书。

要使用证书对 MPOS 应用进行签名，请使用 **Retail SDK\\Build tool\\Customization.settings** 文件中的以下选项之一：

- 添加 Azure DevOps 生成步骤的“保护文件任务”部分并上传证书以保护文件任务。 使用保护文件任务输出路径变量作为 Customization.settings 文件中的参数。

    > [!NOTE]
    > 保护文件任务不支持受密码保护的证书。 必须先删除密码，然后才能上传此任务。 由于证书已上传到 Azure 中的保护文件系统任务，因此您只能在此步骤删除密码。 但是，您应该与安全专家讨论是否删除密码，以确定这是否适合您的项目。 对于其他方案，请勿删除证书密码。
- 使用文件系统中的证书。 要执行此操作，请下载或生成证书并将其放入正在运行内部版本的文件系统中。 Microsoft 托管的代理或内部版本用户应有权访问此路径和文件。
- 使用指纹在商店中查找证书并使用该证书登录。

## <a name="use-a-secure-file-task-for-universal-windows-platform-app-signing"></a>使用保护文件任务进行通用 Windows 平台应用签名

> [!NOTE]
> 您还可以使用 Azure 密钥保管库存储证书，并使用 Azure 签名工具对 Modern POS .appx 文件和自助安装程序进行签名。 有关示例管道脚本和其他信息，请参阅[在 Azure DevOps 中设置生成管道以生成零售自助服务包](build-pipeline.md#set-up-a-build-pipeline-in-azure-devops-to-generate-retail-self-service-packages)。

使用保护文件任务是通用 Windows 平台 (UWP) 应用签名的推荐方法。 有关包签名的详细信息，请参阅[配置包签名](/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing)。 此过程如下图所示。

![MPOS 应用签名流。](media/POSSigningFlow.png)

> [!NOTE]
> 目前 OOB 打包仅支持对 .appx 文件进行签名，MPOIS、RSSU 和 HWS 等其他自助服务安装程序不通过此过程进行签名。 您需要使用 SignTool 或其他签名工具手动签名。 在安装了 Modern POS 的计算机中必须安装用于对 .appx 文件进行签名的证书。

## <a name="steps-to-configure-the-certificate-for-signing-in-azure-pipelines"></a>用于配置用来登录 Azure Pipelines 的证书的步骤

### <a name="certificate-in-the-file-systemsecure-location"></a>文件系统/安全位置中的证书

下载 [DownloadFile 任务](/visualstudio/msbuild/downloadfile-task)，并将其添加为生成流程中的第一步。 使用保护文件任务的好处是，无论生成管道是成功、失败还是被取消，生成过程中文件都会被加密并放在磁盘中。 在完成生成流程后，将从下载位置删除该文件。

1. 下载保护文件任务并将其添加为 Azure 生成管道中的第一步。 您可以从 [DownloadFile](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile) 下载保护文件任务。
1. 将证书上传到保护文件任务，并将“输出变量”下面设置引用名称，如下图所示。
    > [!div class="mx-imgBorder"]
    > ![保护文件任务。](media/SecureFile.png)
1. 通过在 **变量** 选项卡下选择 **新变量**，在 Azure Pipelines 中创建新变量。
1. 为值字段中的变量提供名称，例如 **MySigningCert**。
1. 保存此变量。
1. 从 **RetailSDK\\BuildTools** 中打开 **Customization.settings** 文件，并使用在管道中创建的变量名称更新 **ModernPOSPackageCertificateKeyFile**（步骤 3）。 例如:

    ```Xml
    <ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(MySigningCert)</ModernPOSPackageCertificateKeyFile>
    ```
    如果证书不受密码保护，则需要执行此步骤。 如果证书受密码保护，请继续执行以下步骤。
    
1. 如果在使用证书对 MPOS .appx 文件签名时要为其添加时间戳，请打开 **Retail SDK\\Build tool\\Customization.settings** 文件，并使用时间戳提供程序（例如 `http://timestamp.digicert.com`）更新 **ModernPOSPackageCertificateTimestamp** 变量。
1. 在管道的 **变量** 选项卡上，添加新的安全文本变量。 将名称设置为 **MySigningCert.secret** 并设置证书的密码值。 选择锁图标以保护变量。
1. 将 **Powershell 脚本** 任务添加到管道（在下载安全文件之后且在生成步骤之前）。 提供 **显示** 名称并将类型设置为 **内联**。 将以下内容复制并粘贴到脚本部分。

    ```powershell
    Write-Host "Start adding the PFX file to the certificate store."
    $pfxpath = '$(MySigningCert.secureFilePath)'
    $secureString = ConvertTo-SecureString "$(MySigningCert.secret)" -AsPlainText -Force
    Import-PfxCertificate -FilePath $pfxpath -CertStoreLocation Cert:\CurrentUser\My -Password $secureString
    ```

1. 从 **RetailSDK\\BuildTools** 中打开 **Customization.settings** 文件，并使用证书指纹值更新 **ModernPOSPackageCertificateThumbprint**。

    ```Xml
       <ModernPOSPackageCertificateThumbprint Condition="'$(ModernPOSPackageCertificateThumbprint)' == ''"></ModernPOSPackageCertificateThumbprint>
    ```
 
有关如何获取证书指纹的详细信息，请参阅[检索证书的指纹](/dotnet/framework/wcf/feature-details/how-to-retrieve-the-thumbprint-of-a-certificate#to-retrieve-a-certificates-thumbprint)。 

## <a name="download-or-generate-a-certificate-to-sign-the-mpos-app-manually-using-msbuild-in-sdk"></a>下载或生成证书以使用 SDK 中的 msbuild 手动对 MPOS 应用进行签名

如果下载或生成的证书用于对 MPOS 应用进行签名，则更新 **BuildTools\\Customization.settings** 文件中的 **ModernPOSPackageCertificateKeyFile** 节点，以指向 pfx 文件位置 (**$(SdkReferencesPath)\\appxsignkey.pfx**)。 例如:

```xml
<ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(SdkReferencesPath)\appxsignkey.pfx</ModernPOSPackageCertificateKeyFile>
```

在本例中，证书文件名称为 **appxsignkey.pfx**，位于 **Retail SDK\\Reference** 文件夹中。

## <a name="use-thumbprint-to-sign-the-mpos-app"></a>使用指纹对 MPOS 应用进行签名

如果您使用指纹对 MPOS 应用进行签名，则在本地安装证书。 更新 **BuildTools\\Customization.settings** 文件内 **ModernPOSPackageCertificateThumbprint** 节点中的指纹值。

如果内部版本用户是本地用户，则此选项将起作用。 但是，如果您要使用 Azure DevOps 代理生成内部版本，则代理可能无权访问证书存储，因此无法使用证书进行签名，或者将不在版本计算机上安装证书。 在这种情况下，解决方法是将内部版本用户更改为本地用户并在框中安装证书。 但是，如果您没有该框的管理员访问权限，则此选项将不起作用。

> [!NOTE]
> 如果使用 .pfx 文件或“保护文件任务”选项对应用进行签名，则将 **Customization.settings** 中的 **ModernPOSPackageCertificateThumbprint** 节点留空。 如果使用了指纹选项，则将 **ModernPOSPackageCertificateKeyFile** 留空。 如果更新了这两个值，则生成将失败。

### <a name="certification-renewal"></a>证书续订

### <a name="renew-a-certificate-from-trusted-ca"></a>向受信任的 CA 续订证书

请联系您的证书颁发机构 (CA) 以了解证书续订过程。 对于受信任的证书，MPOS 端不需要任何操作。

### <a name="renew-a-self-signed-certificate"></a>续订自签名证书

不要将零售 SDK 中提供的示例证书用于生产。 它只能用于开发目的。 示例 Contoso 证书无法续订，Retail SDK 版本 10.0.16 或更早版本中包含的示例证书将于 2020 年 12 月 31 日到期。 如果此证书或自签名证书已用于对定制的 Modern POS 进行签名，则 Modern POS 很可能在此日期之后无法正常运行。
 
### <a name="impact"></a>影响
 
如果上述情况适合您，那么您将遇到的问题是安装程序在 2020 年 12 月 31 日之后将无法运行。 根据使用的公司 IT 策略，Modern POS 可能无法运行。 通过将日期临时更改为将来日期来对其进行测试，以确定对您的组织的影响，这一点至关重要。
 
### <a name="steps-to-determine-the-issue"></a>用于确定问题的步骤
 
1.  使用 Windows 设置将计算机时钟更改为 2021 年的日期和时间。
2.  验证是否可以打开 Modern POS，是否可以登录，并且交易是否可以完成。
3.  验证 Modern POS 自助服务安装程序是否能够运行，如果能，则该安装将成功完成。
4.  将 Windows 时钟设置恢复为正确的日期和时间。
 
如果您可以顺利完成所有这些步骤，那么您将能够在 2020 年 12 月 31 日之后使用当前证书进行操作。  
 
### <a name="steps-going-forward"></a>后续步骤 

强烈建议您续订以前使用的证书。 强烈建议您获得新证书。 为此，您必须执行以下操作之一：
 
- **首选** - 从受信任的证书颁发机构获取代码签名证书。

- **非首选** - 生成要使用的自签名代码签名证书。 这通常仅用于域内的开发目的，不建议用于生产。 

- **可用作临时解决方案** - 使用续订的 Contoso 代码签名证书。 这通常用于测试目的，因此不建议将其部署在生产中。
 
接下来，生成一个新的自定义 Modern POS 包，该包使用从上述操作之一获得的此证书进行签名。 根据证书，必须执行以下步骤之一：
 
- 如果使用新的受信任证书（或新的自签名证书），您将需要在每台设备上安装新证书。 之后，您需要使用新创建的 Modern POS 包（安装程序），卸载现有应用程序，然后重新安装新的 Modern POS 包。 您将需要在每台设备上执行 Modern POS 的设备激活。

- 如果使用续订的 Contoso 证书，您将需要在每台设备上安装新证书并安装 Modern POS 包（安装程序）。 您不需要卸载，但必须在设备上重新安装。 请注意，不需要激活 Modern POS 的设备。 此选项是临时解决方案。 仅使用此选项以避免重新激活并在获取新的受信任证书之前解决问题。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
