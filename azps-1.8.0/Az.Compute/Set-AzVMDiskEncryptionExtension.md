---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: da50845ff5012d466eed0c68103cdbd0baea4e7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868886"
---
# <span data-ttu-id="f2903-101">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="f2903-101">Set-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="f2903-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2903-102">SYNOPSIS</span></span>
<span data-ttu-id="f2903-103">Azure에서 실행 중인 IaaS 가상 컴퓨터에서 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

## <span data-ttu-id="f2903-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f2903-104">SYNTAX</span></span>

### <span data-ttu-id="f2903-105">SinglePassParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f2903-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2903-106">AADClientSecretParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2903-106">AADClientSecretParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2903-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2903-107">AADClientCertParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2903-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f2903-108">DESCRIPTION</span></span>
<span data-ttu-id="f2903-109">**AzVMDiskEncryptionExtension** cmdlet은 실행 중인 인프라를 Azure의 IaaS (서비스) 가상 컴퓨터에서 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-109">The **Set-AzVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>
<span data-ttu-id="f2903-110">이 cmdlet은 가상 컴퓨터에 디스크 암호화 확장을 설치 하 여 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-110">This cmdlet enables encryption by installing the disk encryption extension on the virtual machine.</span></span>
<span data-ttu-id="f2903-111">*Name* 매개 변수를 지정 하지 않으면 Windows 운영 체제를 실행 하는 가상 컴퓨터 또는 Linux 용 Azurediskencryption forlinux 가상 머신에 대 한 기본 이름 AzureDiskEncryption 확장자가 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-111">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>
<span data-ttu-id="f2903-112">이 cmdlet은 암호화를 사용 하도록 설정 하는 단계 중 하나에서 가상 컴퓨터를 다시 시작 해야 하는 경우 사용자에 게 확인이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-112">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>
<span data-ttu-id="f2903-113">이 cmdlet을 실행 하기 전에 가상 컴퓨터에 작업을 저장 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-113">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

## <span data-ttu-id="f2903-114">예제의</span><span class="sxs-lookup"><span data-stu-id="f2903-114">EXAMPLES</span></span>

### <span data-ttu-id="f2903-115">예제 1: 암호화 사용</span><span class="sxs-lookup"><span data-stu-id="f2903-115">Example 1: Enable encryption</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="f2903-116">이 예제에서는 광고 자격 증명을 지정 하지 않고 암호화를 설정 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-116">This example demonstrates enabling encryption without specifying AD credentials.</span></span>   

### <span data-ttu-id="f2903-117">예제 2: 파이프라인 입력으로 암호화 사용</span><span class="sxs-lookup"><span data-stu-id="f2903-117">Example 2: Enable encryption with pipelined input</span></span>
```
$params = New-Object PSObject -Property @{
    ResourceGroupName = "[resource-group-name]"
    VMName = "[vm-name]"
    DiskEncryptionKeyVaultId = "/subscriptions/[subscription-id-guid]/resourceGroups/[resource-group-name]/providers/Microsoft.KeyVault/vaults/[keyvault-name]"
    DiskEncryptionKeyVaultUrl = "https://[keyvault-name].vault.azure.net"
    KeyEncryptionKeyVaultId = "/subscriptions/[subscription-id-guid]/resourceGroups/[resource-group-name]/providers/Microsoft.KeyVault/vaults/[keyvault-name]"
    KeyEncryptionKeyUrl = "https://[keyvault-name].vault.azure.net/keys/[kekname]/[kek-unique-id]"
    VolumeType = "All"
}

$params | Set-AzVmDiskEncryptionExtension
```

<span data-ttu-id="f2903-118">이 예제에서는 파이프라인 입력을 사용 하 여 매개 변수를 보내는 방법과 광고 자격 증명을 지정 하지 않고 암호화를 사용 하도록</span><span class="sxs-lookup"><span data-stu-id="f2903-118">This example demonstrates sending parameters using pipelined input to enable encryption without specifying AD credentials.</span></span>  

### <span data-ttu-id="f2903-119">예제 3: Azure AD 클라이언트 ID 및 클라이언트 암호를 사용 하 여 암호화 사용</span><span class="sxs-lookup"><span data-stu-id="f2903-119">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="f2903-120">이 예제에서는 Azure AD 클라이언트 ID와 클라이언트 암호를 사용 하 여 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-120">This example enables encryption using Azure AD client ID, and client secret.</span></span>

### <span data-ttu-id="f2903-121">예제 4: Azure AD 클라이언트 ID 및 클라이언트 인증 지문을 사용 하 여 암호화 사용</span><span class="sxs-lookup"><span data-stu-id="f2903-121">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue 
$ServicePrincipal = New-AzADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

$AADClientID = $AzureAdApplication.ApplicationId
$aadClientCertThumbprint= $cert.Thumbprint

#Upload pfx to KeyVault 
$KeyVaultSecretName = "MyAADCert"
$FileContentBytes = get-content $CertPath -Encoding Byte
$FileContentEncoded = [System.Convert]::ToBase64String($fileContentBytes)
$JSONObject = @"
    { 
        "data" : "$filecontentencoded", 
        "dataType" : "pfx", 
        "password" : "$CertPassword" 
    } 
"@
$JSONObjectBytes = [System.Text.Encoding]::UTF8.GetBytes($jsonObject)
$JSONEncoded = [System.Convert]::ToBase64String($jsonObjectBytes)

$Secret = ConvertTo-SecureString -String $JSONEncoded -AsPlainText -Force
Set-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="f2903-122">이 예제에서는 Azure AD 클라이언트 ID 및 클라이언트 인증 지문을 사용 하 여 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-122">This example enables encryption using Azure AD client ID and client certification thumbprints.</span></span>

### <span data-ttu-id="f2903-123">예제 5: Azure AD 클라이언트 ID를 사용 하 여 암호화 설정, 클라이언트 비밀 및 키 암호화 키를 사용 하 여 디스크 암호화 키 래핑</span><span class="sxs-lookup"><span data-stu-id="f2903-123">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="f2903-124">이 예제에서는 키 암호화 키를 사용 하 여 Azure AD 클라이언트 ID, 클라이언트 암호 및 디스크 줄 바꿈 키를 사용 하 여 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-124">This example enables encryption using Azure AD client ID, client secret, and wrap disk encryption key by using the key encryption key.</span></span>

### <span data-ttu-id="f2903-125">예제 6: Azure AD 클라이언트 ID를 사용 하 여 암호화 설정, 클라이언트 인증서 지문 및 키 암호화 키를 사용 하 여 디스크 encryption.encryptionkey 래핑</span><span class="sxs-lookup"><span data-stu-id="f2903-125">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue
$ServicePrincipal = New-AzADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

$AADClientID = $AzureAdApplication.ApplicationId
$AADClientCertThumbprint= $Cert.Thumbprint

#Upload pfx to KeyVault 
$KeyVaultSecretName = "MyAADCert"
$FileContentBytes = get-content $CertPath -Encoding Byte
$FileContentEncoded = [System.Convert]::ToBase64String($FileContentBytes)
$JSONObject = @"
    { 
        "data" : "$filecontentencoded", 
        "dataType" : "pfx", 
        "password" : "$CertPassword" 
    } 
"@
$JSONObjectBytes = [System.Text.Encoding]::UTF8.GetBytes($JSONObject)
$JsonEncoded = [System.Convert]::ToBase64String($JSONObjectBytes)
$Secret = ConvertTo-SecureString -String $JSONEncoded -AsPlainText -Force
Set-AzKeyVaultSecret -VaultName $VaultName-Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl 
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="f2903-126">이 예제에서는 키 암호화 키를 사용 하 여 Azure AD 클라이언트 ID, 클라이언트 인증서 지문, 디스크 암호화 키 래핑 등을 사용 하 여 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-126">This example enables encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryption key by using key encryption key.</span></span>

## <span data-ttu-id="f2903-127">변수</span><span class="sxs-lookup"><span data-stu-id="f2903-127">PARAMETERS</span></span>

### <span data-ttu-id="f2903-128">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="f2903-128">-AadClientCertThumbprint</span></span>
<span data-ttu-id="f2903-129">**Keyvault** 에 비밀을 쓸 수 있는 권한이 있는 Azureactive Directory (Azure AD) 응용 프로그램 클라이언트 인증서의 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-129">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="f2903-130">필수 구성 요소는 Azure AD 클라이언트 인증서를 이전에 가상 컴퓨터의 로컬 컴퓨터 인증서 저장소에 배포 해야 합니다 `my` .</span><span class="sxs-lookup"><span data-stu-id="f2903-130">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="f2903-131">Add-AzVMSecret cmdlet은 Azure의 가상 컴퓨터에 인증서를 배포 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-131">The Add-AzVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="f2903-132">자세한 내용은 **AzVMSecret** cmdlet 도움말을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f2903-132">For more details, see the **Add-AzVMSecret** cmdlet help.</span></span>
<span data-ttu-id="f2903-133">인증서를 이전에 가상 컴퓨터 로컬 컴퓨터의 인증서 저장소에 배포 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-133">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientCertParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2903-134">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="f2903-134">-AadClientID</span></span>
<span data-ttu-id="f2903-135">**Keyvault** 에 비밀을 쓸 수 있는 권한이 있는 Azure AD 응용 프로그램의 클라이언트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-135">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientSecretParameterSet, AADClientCertParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2903-136">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="f2903-136">-AadClientSecret</span></span>
<span data-ttu-id="f2903-137">**Keyvault** 에 비밀을 쓸 수 있는 권한이 있는 Azure AD 응용 프로그램의 클라이언트 비밀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-137">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientSecretParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2903-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2903-138">-DefaultProfile</span></span>
<span data-ttu-id="f2903-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2903-140">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f2903-140">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="f2903-141">이 cmdlet이 확장의 부 버전에 대 한 자동 업그레이드를 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-141">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2903-142">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="f2903-142">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="f2903-143">가상 머신 암호화 키를 업로드 해야 하는 **Keyvault** 의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-143">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2903-144">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="f2903-144">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="f2903-145">가상 컴퓨터 암호화 키를 업로드 해야 하는 **Keyvault** URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-145">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2903-146">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="f2903-146">-EncryptFormatAll</span></span>
<span data-ttu-id="f2903-147">아직 암호화 되지 않은 모든 데이터 드라이브 Encrypt-Format</span><span class="sxs-lookup"><span data-stu-id="f2903-147">Encrypt-Format all data drives that are not already encrypted</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2903-148">-Extension# ername</span><span class="sxs-lookup"><span data-stu-id="f2903-148">-ExtensionPublisherName</span></span>
<span data-ttu-id="f2903-149">확장명 게시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-149">The extension publisher name.</span></span> <span data-ttu-id="f2903-150">"Microsoft. i i."의 기본값을 재정의 하려면이 매개 변수만 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-150">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2903-151">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="f2903-151">-ExtensionType</span></span>
<span data-ttu-id="f2903-152">확장 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-152">The extension type.</span></span> <span data-ttu-id="f2903-153">이 매개 변수를 지정 하면 Windows Vm에 대 한 "AzureDiskEncryption"의 기본값을 재정의 하 고 Linux 용으로 "Azurediskencryption Forlinux"를 재정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-153">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2903-154">-Force</span><span class="sxs-lookup"><span data-stu-id="f2903-154">-Force</span></span>
<span data-ttu-id="f2903-155">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-155">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2903-156">-Keya 알고리즘</span><span class="sxs-lookup"><span data-stu-id="f2903-156">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="f2903-157">가상 컴퓨터의 키 암호화 키를 래핑하고 래핑을 해제 하는 데 사용 되는 알고리즘을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-157">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="f2903-158">기본 값은 RSA-OAEP입니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-158">The default value is RSA-OAEP.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2903-159">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="f2903-159">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="f2903-160">가상 컴퓨터 암호화 키를 래핑하고 래핑 해제 하는 데 사용 되는 키 암호화 키의 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-160">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="f2903-161">정식 버전의 URL 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-161">This must be the full versioned URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2903-162">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="f2903-162">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="f2903-163">가상 컴퓨터 암호화 키를 래핑하고 래핑 해제 하는 데 사용 되는 키 암호화 키를 포함 하는 **Keyvault** 의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-163">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="f2903-164">정식 버전의 URL 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-164">This must be a full versioned URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2903-165">-이름</span><span class="sxs-lookup"><span data-stu-id="f2903-165">-Name</span></span>
<span data-ttu-id="f2903-166">확장을 나타내는 Azure Resource Manager 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-166">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="f2903-167">기본값은 Windows 운영 체제를 실행 하는 가상 컴퓨터에 대 한 AzureDiskEncryption (Linux 용 Azurediskencryption Linux 가상 머신의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-167">The default value is AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2903-168">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="f2903-168">-Passphrase</span></span>
<span data-ttu-id="f2903-169">Linux 가상 컴퓨터만 암호화 하는 데 사용 되는 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-169">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="f2903-170">이 매개 변수는 Windows 운영 체제를 실행 하는 가상 컴퓨터에는 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-170">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2903-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2903-171">-ResourceGroupName</span></span>
<span data-ttu-id="f2903-172">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-172">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2903-173">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="f2903-173">-SequenceVersion</span></span>
<span data-ttu-id="f2903-174">가상 컴퓨터에 대 한 암호화 작업의 시퀀스 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-174">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="f2903-175">이는 동일한 가상 컴퓨터에서 수행 하는 각 암호화 작업 마다 고유 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-175">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="f2903-176">Get-AzVMExtension cmdlet은 사용 된 이전 시퀀스 번호를 검색 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-176">The Get-AzVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2903-177">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="f2903-177">-SkipVmBackup</span></span>
<span data-ttu-id="f2903-178">Linux Vm에 대 한 백업 만들기 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="f2903-178">Skip backup creation for Linux VMs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2903-179">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f2903-179">-TypeHandlerVersion</span></span>
<span data-ttu-id="f2903-180">암호화 확장명의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-180">Specifies the version of the encryption extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2903-181">-VMName</span><span class="sxs-lookup"><span data-stu-id="f2903-181">-VMName</span></span>
<span data-ttu-id="f2903-182">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-182">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2903-183">-가이 Etype</span><span class="sxs-lookup"><span data-stu-id="f2903-183">-VolumeType</span></span>
<span data-ttu-id="f2903-184">암호화 작업을 수행할 가상 컴퓨터 볼륨의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-184">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="f2903-185">Windows 운영 체제를 실행 하는 가상 컴퓨터에 허용 되는 값은 모든, OS, 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-185">Allowed values for virtual machines that run the Windows operating system are as follows: All, OS, and Data.</span></span>
<span data-ttu-id="f2903-186">Linux 가상 머신에 허용 되는 값은 다음과 같습니다: 데이터에만 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-186">The allowed values for Linux virtual machines are as follows: Data only.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2903-187">-확인</span><span class="sxs-lookup"><span data-stu-id="f2903-187">-Confirm</span></span>
<span data-ttu-id="f2903-188">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-188">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2903-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2903-189">-WhatIf</span></span>
<span data-ttu-id="f2903-190">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2903-191">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-191">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2903-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2903-192">CommonParameters</span></span>
<span data-ttu-id="f2903-193">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2903-194">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2903-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2903-195">입력</span><span class="sxs-lookup"><span data-stu-id="f2903-195">INPUTS</span></span>

### <span data-ttu-id="f2903-196">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f2903-196">System.String</span></span>

### <span data-ttu-id="f2903-197">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f2903-197">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f2903-198">출력</span><span class="sxs-lookup"><span data-stu-id="f2903-198">OUTPUTS</span></span>

### <span data-ttu-id="f2903-199">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="f2903-199">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f2903-200">상속자</span><span class="sxs-lookup"><span data-stu-id="f2903-200">NOTES</span></span>

## <span data-ttu-id="f2903-201">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2903-201">RELATED LINKS</span></span>

[<span data-ttu-id="f2903-202">추가-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="f2903-202">Add-AzVMSecret</span></span>](./Add-AzVMSecret.md)

[<span data-ttu-id="f2903-203">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="f2903-203">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="f2903-204">제거-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="f2903-204">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)


