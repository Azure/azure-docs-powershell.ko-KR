---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: d24344392682e04f2eecc34f491e6048ca543d4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957520"
---
# <span data-ttu-id="fd4ad-101">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="fd4ad-101">Set-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="fd4ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd4ad-102">SYNOPSIS</span></span>
<span data-ttu-id="fd4ad-103">Azure에서 실행 중인 IaaS 가상 머신에서 암호화를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

## <span data-ttu-id="fd4ad-104">구문</span><span class="sxs-lookup"><span data-stu-id="fd4ad-104">SYNTAX</span></span>

### <span data-ttu-id="fd4ad-105">SinglePassParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="fd4ad-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd4ad-106">AADClientSecretParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd4ad-106">AADClientSecretParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd4ad-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd4ad-107">AADClientCertParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd4ad-108">설명</span><span class="sxs-lookup"><span data-stu-id="fd4ad-108">DESCRIPTION</span></span>
<span data-ttu-id="fd4ad-109">**Set-AzVMDiskEncryptionExtension** cmdlet을 사용하면 Azure에서 실행 중인 인프라에서 IaaS(서비스) 가상 머신으로 암호화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-109">The **Set-AzVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>  <span data-ttu-id="fd4ad-110">가상 머신에 디스크 암호화 확장을 설치하여 암호화를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-110">It enables encryption by installing the disk encryption extension on the virtual machine.</span></span> 

<span data-ttu-id="fd4ad-111">이 cmdlet은 암호화를 사용하도록 설정하는 단계 중 하나인 사용자로부터 확인을 요구하고 가상 머신을 다시 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>

<span data-ttu-id="fd4ad-112">이 cmdlet을 실행하기 전에 가상 머신에 작업을 저장하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

<span data-ttu-id="fd4ad-113">Linux: **VolumeType** 매개 변수는 Linux 가상 머신을 암호화할 때 필요하며 Linux 배포에서 지원하는 값("Os", "Data" 또는 "All")으로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-113">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="fd4ad-114">Windows: **VolumeType** 매개 변수를 생략할 수 있습니다. 이 경우 작업은 모두로 기본값입니다. Windows 가상 머신에 대해 VolumeType 매개 변수가 있는 경우 전체 또는 OS로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-114">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

## <span data-ttu-id="fd4ad-115">예제</span><span class="sxs-lookup"><span data-stu-id="fd4ad-115">EXAMPLES</span></span>

### <span data-ttu-id="fd4ad-116">예제 1: 암호화 사용</span><span class="sxs-lookup"><span data-stu-id="fd4ad-116">Example 1: Enable encryption</span></span>
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

<span data-ttu-id="fd4ad-117">이 예제에서는 AD 자격 증명을 지정하지 않고 VM에서 암호화를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-117">This example enables encryption on a VM without specifying AD credentials.</span></span>

### <span data-ttu-id="fd4ad-118">예제 2: 파이프라인 입력을 사용하여 암호화 사용</span><span class="sxs-lookup"><span data-stu-id="fd4ad-118">Example 2: Enable encryption with pipelined input</span></span>
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

<span data-ttu-id="fd4ad-119">이 예제에서는 AD 자격 증명을 지정하지 않고 파이프라인 입력을 사용하여 VM에서 암호화를 사용하도록 설정하는 매개 변수를 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-119">This example sends parameters using pipelined input to enable encryption on a VM, without specifying AD credentials.</span></span>

### <span data-ttu-id="fd4ad-120">예제 3: Azure AD 클라이언트 ID 및 클라이언트 비밀을 사용하여 암호화 사용</span><span class="sxs-lookup"><span data-stu-id="fd4ad-120">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
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

<span data-ttu-id="fd4ad-121">이 예제에서는 Azure AD 클라이언트 ID 및 클라이언트 비밀을 사용하여 VM에서 암호화를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-121">This example uses Azure AD client ID and client secret to enable encryption on a VM.</span></span>

### <span data-ttu-id="fd4ad-122">예제 4: Azure AD 클라이언트 ID 및 클라이언트 인증 지문을 사용하여 암호화 사용</span><span class="sxs-lookup"><span data-stu-id="fd4ad-122">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
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

<span data-ttu-id="fd4ad-123">이 예제에서는 Azure AD 클라이언트 ID 및 클라이언트 인증 지문을 사용하여 VM에서 암호화를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-123">This example uses Azure AD client ID and client certification thumbprints to enable encryption on a VM.</span></span>

### <span data-ttu-id="fd4ad-124">예제 5: 키 암호화 키를 사용하여 Azure AD 클라이언트 ID, 클라이언트 비밀 및 래핑 디스크 암호화 키를 사용하여 암호화 사용</span><span class="sxs-lookup"><span data-stu-id="fd4ad-124">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
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

<span data-ttu-id="fd4ad-125">이 예제에서는 Azure AD 클라이언트 ID 및 클라이언트 비밀을 사용하여 VM에서 암호화를 사용하도록 설정하고 키 암호화 키를 사용하여 디스크 암호화 키를 래핑합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-125">This example uses Azure AD client ID and client secret to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

### <span data-ttu-id="fd4ad-126">예제 6: 키 암호화 키를 사용하여 Azure AD 클라이언트 ID, 클라이언트 인증 지문 및 래핑 디스크 암호화 키를 사용하여 암호화 사용</span><span class="sxs-lookup"><span data-stu-id="fd4ad-126">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
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

<span data-ttu-id="fd4ad-127">이 예제에서는 Azure AD 클라이언트 ID 및 클라이언트 인증 지문을 사용하여 VM에서 암호화를 사용하도록 설정하고 키 암호화 키를 사용하여 디스크 암호화 키를 래핑합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-127">This example uses Azure AD client ID and client cert thumbprint to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

## <span data-ttu-id="fd4ad-128">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fd4ad-128">PARAMETERS</span></span>

### <span data-ttu-id="fd4ad-129">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="fd4ad-129">-AadClientCertThumbprint</span></span>
<span data-ttu-id="fd4ad-130">**KeyVault에** 비밀을 쓸 수 있는 권한이 있는 Azure AD(Azure AD) 애플리케이션 클라이언트 인증서의 지문을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-130">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="fd4ad-131">반드시 Azure AD 클라이언트 인증서를 가상 머신의 로컬 컴퓨터 인증서 저장소에 `my` 배포해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-131">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="fd4ad-132">Add-AzVMSecret cmdlet을 사용하여 Azure의 가상 머신에 인증서를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-132">The Add-AzVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="fd4ad-133">자세한 내용은 **Add-AzVMSecret cmdlet** 도움말을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-133">For more details, see the **Add-AzVMSecret** cmdlet help.</span></span>
<span data-ttu-id="fd4ad-134">인증서는 이전에 내 인증서 저장소의 가상 머신 로컬 컴퓨터에 배포되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-134">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

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

### <span data-ttu-id="fd4ad-135">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="fd4ad-135">-AadClientID</span></span>
<span data-ttu-id="fd4ad-136">KeyVault에 비밀을 쓸 수 있는 권한이 있는 Azure AD 애플리케이션의 **클라이언트 ID를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="fd4ad-136">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="fd4ad-137">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="fd4ad-137">-AadClientSecret</span></span>
<span data-ttu-id="fd4ad-138">KeyVault에 비밀을 쓸 수 있는 권한이 있는 Azure AD 애플리케이션의 클라이언트 **비밀을 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="fd4ad-138">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="fd4ad-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd4ad-139">-DefaultProfile</span></span>
<span data-ttu-id="fd4ad-140">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd4ad-141">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="fd4ad-141">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="fd4ad-142">이 cmdlet은 확장의 부 버전 자동 업그레이드를 사용하지 않도록 설정하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-142">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="fd4ad-143">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="fd4ad-143">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="fd4ad-144">가상 머신 암호화 키를 업로드해야 하는 **KeyVault의** 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-144">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="fd4ad-145">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="fd4ad-145">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="fd4ad-146">가상 머신 암호화 키를 업로드해야 하는 **KeyVault** URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-146">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="fd4ad-147">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="fd4ad-147">-EncryptFormatAll</span></span>
<span data-ttu-id="fd4ad-148">Encrypt-Format 암호화되지 않은 모든 데이터 드라이브를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-148">Encrypt-Format all data drives that are not already encrypted</span></span>

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

### <span data-ttu-id="fd4ad-149">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="fd4ad-149">-ExtensionPublisherName</span></span>
<span data-ttu-id="fd4ad-150">확장 게시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-150">The extension publisher name.</span></span> <span data-ttu-id="fd4ad-151">이 매개 변수를 지정하여 "Microsoft.Azure.Security"의 기본값을 오버라이드합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-151">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="fd4ad-152">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="fd4ad-152">-ExtensionType</span></span>
<span data-ttu-id="fd4ad-153">확장 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-153">The extension type.</span></span> <span data-ttu-id="fd4ad-154">이 매개 변수를 지정하여 Windows VM에 대한 "AzureDiskEncryption" 및 Linux VM에 대한 "AzureDiskEncryptionForLinux"의 기본값을 오버라이드합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-154">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="fd4ad-155">-Force</span><span class="sxs-lookup"><span data-stu-id="fd4ad-155">-Force</span></span>
<span data-ttu-id="fd4ad-156">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-156">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fd4ad-157">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="fd4ad-157">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="fd4ad-158">가상 머신의 키 암호화 키를 래핑하고 래핑하는 데 사용되는 알고리즘을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-158">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="fd4ad-159">기본값은 RSA-OAEP입니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-159">The default value is RSA-OAEP.</span></span>

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

### <span data-ttu-id="fd4ad-160">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="fd4ad-160">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="fd4ad-161">가상 머신 암호화 키를 래핑하고 래핑하는 데 사용되는 키 암호화 키의 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-161">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="fd4ad-162">정식 버전 URL이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-162">This must be the full versioned URL.</span></span>

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

### <span data-ttu-id="fd4ad-163">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="fd4ad-163">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="fd4ad-164">가상 머신 암호화 키를 래핑하고 래핑하는 데 사용되는 키 암호화 키가 포함된 **KeyVault의** 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-164">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="fd4ad-165">전체 버전 URL이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-165">This must be a full versioned URL.</span></span>

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

### <span data-ttu-id="fd4ad-166">-Name</span><span class="sxs-lookup"><span data-stu-id="fd4ad-166">-Name</span></span>
<span data-ttu-id="fd4ad-167">확장을 나타내는 Azure Resource Manager 리소스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-167">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span> <span data-ttu-id="fd4ad-168">이름 *매개* 변수를 생략하면 설치된 확장은 Windows 가상 머신의 AzureDiskEncryption 및 Linux 가상 머신의 AzureDiskEncryptionForLinux로 명명됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-168">If the *Name* parameter is omitted, the installed extension will be named AzureDiskEncryption on Windows virtual machines and AzureDiskEncryptionForLinux on Linux virtual machines.</span></span>


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

### <span data-ttu-id="fd4ad-169">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="fd4ad-169">-Passphrase</span></span>
<span data-ttu-id="fd4ad-170">Linux 가상 머신을 암호화하는 데 사용되는 암호만 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-170">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="fd4ad-171">이 매개 변수는 Windows 운영 체제를 실행하는 가상 머신에 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-171">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="fd4ad-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd4ad-172">-ResourceGroupName</span></span>
<span data-ttu-id="fd4ad-173">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-173">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="fd4ad-174">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="fd4ad-174">-SequenceVersion</span></span>
<span data-ttu-id="fd4ad-175">가상 머신에 대한 암호화 작업의 시퀀스 번호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-175">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="fd4ad-176">이는 동일한 가상 머신에서 수행되는 각 암호화 작업에 따라 고유합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-176">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="fd4ad-177">Get-AzVMExtension cmdlet을 사용하여 사용된 이전 시퀀스 번호를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-177">The Get-AzVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

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

### <span data-ttu-id="fd4ad-178">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="fd4ad-178">-SkipVmBackup</span></span>
<span data-ttu-id="fd4ad-179">Linux VM에 대한 백업 만들기 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="fd4ad-179">Skip backup creation for Linux VMs</span></span>

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

### <span data-ttu-id="fd4ad-180">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="fd4ad-180">-TypeHandlerVersion</span></span>
<span data-ttu-id="fd4ad-181">암호화 확장의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-181">Specifies the version of the encryption extension.</span></span>

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

### <span data-ttu-id="fd4ad-182">-VMName</span><span class="sxs-lookup"><span data-stu-id="fd4ad-182">-VMName</span></span>
<span data-ttu-id="fd4ad-183">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-183">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="fd4ad-184">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="fd4ad-184">-VolumeType</span></span>
<span data-ttu-id="fd4ad-185">암호화 작업을 수행할 가상 머신 볼륨 유형(OS, 데이터 또는 모두)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-185">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="fd4ad-186">Linux: **VolumeType** 매개 변수는 Linux 가상 머신을 암호화할 때 필요하며 Linux 배포에서 지원하는 값("Os", "Data" 또는 "All")으로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-186">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="fd4ad-187">Windows: **VolumeType** 매개 변수를 생략할 수 있습니다. 이 경우 작업은 모두로 기본값입니다. Windows 가상 머신에 대해 VolumeType 매개 변수가 있는 경우 전체 또는 OS로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-187">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

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

### <span data-ttu-id="fd4ad-188">-확인</span><span class="sxs-lookup"><span data-stu-id="fd4ad-188">-Confirm</span></span>
<span data-ttu-id="fd4ad-189">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd4ad-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd4ad-190">-WhatIf</span></span>
<span data-ttu-id="fd4ad-191">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd4ad-192">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd4ad-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd4ad-193">CommonParameters</span></span>
<span data-ttu-id="fd4ad-194">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fd4ad-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd4ad-195">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd4ad-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd4ad-196">입력</span><span class="sxs-lookup"><span data-stu-id="fd4ad-196">INPUTS</span></span>

### <span data-ttu-id="fd4ad-197">System.String</span><span class="sxs-lookup"><span data-stu-id="fd4ad-197">System.String</span></span>

### <span data-ttu-id="fd4ad-198">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fd4ad-198">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fd4ad-199">출력</span><span class="sxs-lookup"><span data-stu-id="fd4ad-199">OUTPUTS</span></span>

### <span data-ttu-id="fd4ad-200">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="fd4ad-200">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="fd4ad-201">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fd4ad-201">NOTES</span></span>

## <span data-ttu-id="fd4ad-202">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd4ad-202">RELATED LINKS</span></span>

[<span data-ttu-id="fd4ad-203">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="fd4ad-203">Add-AzVMSecret</span></span>](./Add-AzVMSecret.md)

[<span data-ttu-id="fd4ad-204">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="fd4ad-204">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="fd4ad-205">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="fd4ad-205">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)


