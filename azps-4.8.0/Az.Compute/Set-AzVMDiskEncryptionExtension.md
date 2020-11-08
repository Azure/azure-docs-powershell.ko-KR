---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 1c69d79e148eae92307855ecfe308f5208a2f455
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056729"
---
# <span data-ttu-id="7c1fd-101">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="7c1fd-101">Set-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="7c1fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c1fd-102">SYNOPSIS</span></span>
<span data-ttu-id="7c1fd-103">Azure에서 실행 중인 IaaS 가상 컴퓨터에서 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

## <span data-ttu-id="7c1fd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c1fd-104">SYNTAX</span></span>

### <span data-ttu-id="7c1fd-105">SinglePassParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7c1fd-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c1fd-106">AADClientSecretParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c1fd-106">AADClientSecretParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c1fd-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c1fd-107">AADClientCertParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c1fd-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7c1fd-108">DESCRIPTION</span></span>
<span data-ttu-id="7c1fd-109">**AzVMDiskEncryptionExtension** cmdlet은 실행 중인 인프라를 Azure의 IaaS (서비스) 가상 컴퓨터에서 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-109">The **Set-AzVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>  <span data-ttu-id="7c1fd-110">가상 컴퓨터에 디스크 암호화 확장을 설치 하 여 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-110">It enables encryption by installing the disk encryption extension on the virtual machine.</span></span> 

<span data-ttu-id="7c1fd-111">이 cmdlet은 암호화를 사용 하도록 설정 하는 단계 중 하나에서 가상 컴퓨터를 다시 시작 해야 하는 경우 사용자에 게 확인이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>

<span data-ttu-id="7c1fd-112">이 cmdlet을 실행 하기 전에 가상 컴퓨터에 작업을 저장 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

<span data-ttu-id="7c1fd-113">Linux: Linux 가상 컴퓨터를 암호화 하는 경우는 데 필요한 **etype** 매개 변수가 필요 하며, linux 배포에서 지원 되는 값 ("Os", "Data" 또는 "All")으로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-113">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="7c1fd-114">Windows: 지 수 **etype** 매개 변수를 생략할 수 있으며,이 경우 작업은 기본적으로 모두 설정 됩니다. Windows 가상 컴퓨터에는 지 수 Etype 매개 변수가 있는 경우 모든 또는 OS 중 하나로 설정 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-114">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

## <span data-ttu-id="7c1fd-115">예제의</span><span class="sxs-lookup"><span data-stu-id="7c1fd-115">EXAMPLES</span></span>

### <span data-ttu-id="7c1fd-116">예제 1: 암호화 사용</span><span class="sxs-lookup"><span data-stu-id="7c1fd-116">Example 1: Enable encryption</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="7c1fd-117">이 예제에서는 광고 자격 증명을 지정 하지 않고 VM에서 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-117">This example enables encryption on a VM without specifying AD credentials.</span></span>

### <span data-ttu-id="7c1fd-118">예제 2: 파이프라인 입력으로 암호화 사용</span><span class="sxs-lookup"><span data-stu-id="7c1fd-118">Example 2: Enable encryption with pipelined input</span></span>
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

<span data-ttu-id="7c1fd-119">이 예제에서는 광고 자격 증명을 지정 하지 않고 파이프라인 입력을 사용 하 여 VM에서 암호화를 사용 하도록 매개 변수를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-119">This example sends parameters using pipelined input to enable encryption on a VM, without specifying AD credentials.</span></span>

### <span data-ttu-id="7c1fd-120">예제 3: Azure AD 클라이언트 ID 및 클라이언트 암호를 사용 하 여 암호화 사용</span><span class="sxs-lookup"><span data-stu-id="7c1fd-120">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="7c1fd-121">이 예제에서는 Azure AD 클라이언트 ID와 클라이언트 암호를 사용 하 여 VM에서 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-121">This example uses Azure AD client ID and client secret to enable encryption on a VM.</span></span>

### <span data-ttu-id="7c1fd-122">예제 4: Azure AD 클라이언트 ID 및 클라이언트 인증 지문을 사용 하 여 암호화 사용</span><span class="sxs-lookup"><span data-stu-id="7c1fd-122">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"

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
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="7c1fd-123">이 예제에서는 Azure AD 클라이언트 ID 및 클라이언트 인증 지문을 사용 하 여 VM에서 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-123">This example uses Azure AD client ID and client certification thumbprints to enable encryption on a VM.</span></span>

### <span data-ttu-id="7c1fd-124">예제 5: Azure AD 클라이언트 ID를 사용 하 여 암호화 설정, 클라이언트 비밀 및 키 암호화 키를 사용 하 여 디스크 암호화 키 래핑</span><span class="sxs-lookup"><span data-stu-id="7c1fd-124">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"

$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="7c1fd-125">이 예제에서는 Azure AD 클라이언트 ID와 클라이언트 암호를 사용 하 여 VM에서 암호화를 사용 하도록 설정 하 고 키 암호화 키를 사용 하 여 디스크 암호화 키를 래핑합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-125">This example uses Azure AD client ID and client secret to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

### <span data-ttu-id="7c1fd-126">예제 6: Azure AD 클라이언트 ID를 사용 하 여 암호화 설정, 클라이언트 인증서 지문 및 키 암호화 키를 사용 하 여 디스크 encryption.encryptionkey 래핑</span><span class="sxs-lookup"><span data-stu-id="7c1fd-126">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
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
$VolumeType = "All"

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
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="7c1fd-127">이 예제에서는 Azure AD 클라이언트 ID 및 클라이언트 인증서 지문을 사용 하 여 VM에서 암호화를 사용 하도록 설정 하 고 키 암호화 키를 사용 하 여 디스크 암호화 키를 래핑합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-127">This example uses Azure AD client ID and client cert thumbprint to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

## <span data-ttu-id="7c1fd-128">변수</span><span class="sxs-lookup"><span data-stu-id="7c1fd-128">PARAMETERS</span></span>

### <span data-ttu-id="7c1fd-129">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="7c1fd-129">-AadClientCertThumbprint</span></span>
<span data-ttu-id="7c1fd-130">**Keyvault** 에 비밀을 쓸 수 있는 권한이 있는 Azureactive Directory (Azure AD) 응용 프로그램 클라이언트 인증서의 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-130">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="7c1fd-131">필수 구성 요소는 Azure AD 클라이언트 인증서를 이전에 가상 컴퓨터의 로컬 컴퓨터 인증서 저장소에 배포 해야 합니다 `my` .</span><span class="sxs-lookup"><span data-stu-id="7c1fd-131">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="7c1fd-132">Add-AzVMSecret cmdlet은 Azure의 가상 컴퓨터에 인증서를 배포 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-132">The Add-AzVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="7c1fd-133">자세한 내용은 **AzVMSecret** cmdlet 도움말을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-133">For more details, see the **Add-AzVMSecret** cmdlet help.</span></span>
<span data-ttu-id="7c1fd-134">인증서를 이전에 가상 컴퓨터 로컬 컴퓨터의 인증서 저장소에 배포 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-134">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

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

### <span data-ttu-id="7c1fd-135">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="7c1fd-135">-AadClientID</span></span>
<span data-ttu-id="7c1fd-136">**Keyvault** 에 비밀을 쓸 수 있는 권한이 있는 Azure AD 응용 프로그램의 클라이언트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-136">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="7c1fd-137">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="7c1fd-137">-AadClientSecret</span></span>
<span data-ttu-id="7c1fd-138">**Keyvault** 에 비밀을 쓸 수 있는 권한이 있는 Azure AD 응용 프로그램의 클라이언트 비밀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-138">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="7c1fd-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c1fd-139">-DefaultProfile</span></span>
<span data-ttu-id="7c1fd-140">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c1fd-141">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="7c1fd-141">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="7c1fd-142">이 cmdlet이 확장의 부 버전에 대 한 자동 업그레이드를 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-142">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="7c1fd-143">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="7c1fd-143">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="7c1fd-144">가상 머신 암호화 키를 업로드 해야 하는 **Keyvault** 의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-144">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="7c1fd-145">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="7c1fd-145">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="7c1fd-146">가상 컴퓨터 암호화 키를 업로드 해야 하는 **Keyvault** URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-146">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="7c1fd-147">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="7c1fd-147">-EncryptFormatAll</span></span>
<span data-ttu-id="7c1fd-148">아직 암호화 되지 않은 모든 데이터 드라이브 Encrypt-Format</span><span class="sxs-lookup"><span data-stu-id="7c1fd-148">Encrypt-Format all data drives that are not already encrypted</span></span>

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

### <span data-ttu-id="7c1fd-149">-Extension# ername</span><span class="sxs-lookup"><span data-stu-id="7c1fd-149">-ExtensionPublisherName</span></span>
<span data-ttu-id="7c1fd-150">확장명 게시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-150">The extension publisher name.</span></span> <span data-ttu-id="7c1fd-151">"Microsoft. i i."의 기본값을 재정의 하려면이 매개 변수만 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-151">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="7c1fd-152">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="7c1fd-152">-ExtensionType</span></span>
<span data-ttu-id="7c1fd-153">확장 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-153">The extension type.</span></span> <span data-ttu-id="7c1fd-154">이 매개 변수를 지정 하면 Windows Vm에 대 한 "AzureDiskEncryption"의 기본값을 재정의 하 고 Linux 용으로 "Azurediskencryption Forlinux"를 재정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-154">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="7c1fd-155">-Force</span><span class="sxs-lookup"><span data-stu-id="7c1fd-155">-Force</span></span>
<span data-ttu-id="7c1fd-156">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-156">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7c1fd-157">-Keya 알고리즘</span><span class="sxs-lookup"><span data-stu-id="7c1fd-157">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="7c1fd-158">가상 컴퓨터의 키 암호화 키를 래핑하고 래핑을 해제 하는 데 사용 되는 알고리즘을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-158">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="7c1fd-159">기본 값은 RSA-OAEP입니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-159">The default value is RSA-OAEP.</span></span>

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

### <span data-ttu-id="7c1fd-160">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="7c1fd-160">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="7c1fd-161">가상 컴퓨터 암호화 키를 래핑하고 래핑 해제 하는 데 사용 되는 키 암호화 키의 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-161">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="7c1fd-162">정식 버전의 URL 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-162">This must be the full versioned URL.</span></span>

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

### <span data-ttu-id="7c1fd-163">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="7c1fd-163">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="7c1fd-164">가상 컴퓨터 암호화 키를 래핑하고 래핑 해제 하는 데 사용 되는 키 암호화 키를 포함 하는 **Keyvault** 의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-164">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="7c1fd-165">정식 버전의 URL 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-165">This must be a full versioned URL.</span></span>

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

### <span data-ttu-id="7c1fd-166">-이름</span><span class="sxs-lookup"><span data-stu-id="7c1fd-166">-Name</span></span>
<span data-ttu-id="7c1fd-167">확장을 나타내는 Azure Resource Manager 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-167">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span> <span data-ttu-id="7c1fd-168">*Name* 매개 변수를 생략 하면 설치 된 확장이 Windows 가상 머신에서 AzureDiskEncryption으로 명명 되 고 linux 가상 머신에는 Azurediskencryption forlinux가 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-168">If the *Name* parameter is omitted, the installed extension will be named AzureDiskEncryption on Windows virtual machines and AzureDiskEncryptionForLinux on Linux virtual machines.</span></span>


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

### <span data-ttu-id="7c1fd-169">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="7c1fd-169">-Passphrase</span></span>
<span data-ttu-id="7c1fd-170">Linux 가상 컴퓨터만 암호화 하는 데 사용 되는 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-170">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="7c1fd-171">이 매개 변수는 Windows 운영 체제를 실행 하는 가상 컴퓨터에는 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-171">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="7c1fd-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c1fd-172">-ResourceGroupName</span></span>
<span data-ttu-id="7c1fd-173">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-173">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7c1fd-174">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="7c1fd-174">-SequenceVersion</span></span>
<span data-ttu-id="7c1fd-175">가상 컴퓨터에 대 한 암호화 작업의 시퀀스 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-175">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="7c1fd-176">이는 동일한 가상 컴퓨터에서 수행 하는 각 암호화 작업 마다 고유 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-176">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="7c1fd-177">Get-AzVMExtension cmdlet은 사용 된 이전 시퀀스 번호를 검색 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-177">The Get-AzVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

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

### <span data-ttu-id="7c1fd-178">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="7c1fd-178">-SkipVmBackup</span></span>
<span data-ttu-id="7c1fd-179">Linux Vm에 대 한 백업 만들기 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="7c1fd-179">Skip backup creation for Linux VMs</span></span>

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

### <span data-ttu-id="7c1fd-180">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="7c1fd-180">-TypeHandlerVersion</span></span>
<span data-ttu-id="7c1fd-181">암호화 확장명의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-181">Specifies the version of the encryption extension.</span></span>

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

### <span data-ttu-id="7c1fd-182">-VMName</span><span class="sxs-lookup"><span data-stu-id="7c1fd-182">-VMName</span></span>
<span data-ttu-id="7c1fd-183">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-183">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="7c1fd-184">-가이 Etype</span><span class="sxs-lookup"><span data-stu-id="7c1fd-184">-VolumeType</span></span>
<span data-ttu-id="7c1fd-185">암호화 작업을 수행할 가상 컴퓨터 볼륨의 유형 (OS, 데이터 또는 모두)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-185">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="7c1fd-186">Linux: Linux 가상 컴퓨터를 암호화 하는 경우는 데 필요한 **etype** 매개 변수가 필요 하며, linux 배포에서 지원 되는 값 ("Os", "Data" 또는 "All")으로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-186">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="7c1fd-187">Windows: 지 수 **etype** 매개 변수를 생략할 수 있으며,이 경우 작업은 기본적으로 모두 설정 됩니다. Windows 가상 컴퓨터에는 지 수 Etype 매개 변수가 있는 경우 모든 또는 OS 중 하나로 설정 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-187">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

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

### <span data-ttu-id="7c1fd-188">-확인</span><span class="sxs-lookup"><span data-stu-id="7c1fd-188">-Confirm</span></span>
<span data-ttu-id="7c1fd-189">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c1fd-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c1fd-190">-WhatIf</span></span>
<span data-ttu-id="7c1fd-191">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c1fd-192">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c1fd-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c1fd-193">CommonParameters</span></span>
<span data-ttu-id="7c1fd-194">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c1fd-195">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c1fd-196">입력</span><span class="sxs-lookup"><span data-stu-id="7c1fd-196">INPUTS</span></span>

### <span data-ttu-id="7c1fd-197">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c1fd-197">System.String</span></span>

### <span data-ttu-id="7c1fd-198">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7c1fd-198">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7c1fd-199">출력</span><span class="sxs-lookup"><span data-stu-id="7c1fd-199">OUTPUTS</span></span>

### <span data-ttu-id="7c1fd-200">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-200">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7c1fd-201">상속자</span><span class="sxs-lookup"><span data-stu-id="7c1fd-201">NOTES</span></span>

## <span data-ttu-id="7c1fd-202">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c1fd-202">RELATED LINKS</span></span>

[<span data-ttu-id="7c1fd-203">추가-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="7c1fd-203">Add-AzVMSecret</span></span>](./Add-AzVMSecret.md)

[<span data-ttu-id="7c1fd-204">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="7c1fd-204">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="7c1fd-205">제거-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="7c1fd-205">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)


