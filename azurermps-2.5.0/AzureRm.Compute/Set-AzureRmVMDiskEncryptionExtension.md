---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdiskencryptionextension
schema: 2.0.0
ms.openlocfilehash: 76bdebc68f1fafef127863ef753c28fce7034fe0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882273"
---
# <span data-ttu-id="7e90f-101">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="7e90f-101">Set-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="7e90f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e90f-102">SYNOPSIS</span></span>
<span data-ttu-id="7e90f-103">Azure에서 실행 중인 IaaS 가상 컴퓨터에서 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e90f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7e90f-104">SYNTAX</span></span>

### <span data-ttu-id="7e90f-105">AADClientSecretParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7e90f-105">AADClientSecretParameterSet (Default)</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e90f-106">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e90f-106">AADClientCertParameterSet</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e90f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7e90f-107">DESCRIPTION</span></span>
<span data-ttu-id="7e90f-108">**AzureRmVMDiskEncryptionExtension** cmdlet은 실행 중인 인프라를 Azure의 IaaS (서비스) 가상 컴퓨터에서 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-108">The **Set-AzureRmVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>
<span data-ttu-id="7e90f-109">이 cmdlet은 가상 컴퓨터에 디스크 암호화 확장을 설치 하 여 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-109">This cmdlet enables encryption by installing the disk encryption extension on the virtual machine.</span></span>
<span data-ttu-id="7e90f-110">*Name* 매개 변수를 지정 하지 않으면 Windows 운영 체제를 실행 하는 가상 컴퓨터 또는 Linux 용 Azurediskencryption forlinux 가상 머신에 대 한 기본 이름 AzureDiskEncryption 확장자가 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-110">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>
<span data-ttu-id="7e90f-111">이 cmdlet은 암호화를 사용 하도록 설정 하는 단계 중 하나에서 가상 컴퓨터를 다시 시작 해야 하는 경우 사용자에 게 확인이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>
<span data-ttu-id="7e90f-112">이 cmdlet을 실행 하기 전에 가상 컴퓨터에 작업을 저장 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

## <span data-ttu-id="7e90f-113">예제의</span><span class="sxs-lookup"><span data-stu-id="7e90f-113">EXAMPLES</span></span>

### <span data-ttu-id="7e90f-114">예제 1: Azure AD 클라이언트 ID 및 클라이언트 암호를 사용 하 여 암호화 사용</span><span class="sxs-lookup"><span data-stu-id="7e90f-114">Example 1: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="7e90f-115">이 예제에서는 Azure AD 클라이언트 ID와 클라이언트 암호를 사용 하 여 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-115">This example enables encryption using Azure AD client ID, and client secret.</span></span>

### <span data-ttu-id="7e90f-116">예제 2: Azure AD 클라이언트 ID 및 클라이언트 인증 지문을 사용 하 여 암호화 사용</span><span class="sxs-lookup"><span data-stu-id="7e90f-116">Example 2: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$KeyValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzureRmADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -KeyValue $KeyValue -KeyType AsymmetricX509Cert 
$ServicePrincipal = New-AzureRmADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

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
Set-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName -SecretValue $Secret
Set-AzureRmKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzureRmVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzureRmVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzureRmVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="7e90f-117">이 예제에서는 Azure AD 클라이언트 ID 및 클라이언트 인증 지문을 사용 하 여 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-117">This example enables encryption using Azure AD client ID and client certification thumbprints.</span></span>

### <span data-ttu-id="7e90f-118">예제 3: Azure AD 클라이언트 ID, 클라이언트 비밀 번호를 사용 하 여 암호화 설정, 키 암호화 키를 사용 하 여 디스크 암호화 키 래핑</span><span class="sxs-lookup"><span data-stu-id="7e90f-118">Example 3: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="7e90f-119">이 예제에서는 키 암호화 키를 사용 하 여 Azure AD 클라이언트 ID, 클라이언트 암호 및 디스크 줄 바꿈 키를 사용 하 여 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-119">This example enables encryption using Azure AD client ID, client secret, and wrap disk encryption key by using the key encryption key.</span></span>

### <span data-ttu-id="7e90f-120">예제 4: Azure AD 클라이언트 ID를 사용 하 여 암호화 설정, 클라이언트 인증서 지문 및 키 암호화 키를 사용 하 여 디스크 encryption.encryptionkey 래핑</span><span class="sxs-lookup"><span data-stu-id="7e90f-120">Example 4: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$KeyValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzureRmADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -KeyValue $KeyValue -KeyType AsymmetricX509Cert 
$ServicePrincipal = New-AzureRmADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

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
Set-AzureKeyVaultSecret -VaultName $VaultName-Name $KeyVaultSecretName -SecretValue $Secret
Set-AzureRmKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzureRmVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzureRmVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl 
Update-AzureRmVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="7e90f-121">이 예제에서는 키 암호화 키를 사용 하 여 Azure AD 클라이언트 ID, 클라이언트 인증서 지문, 디스크 암호화 키 래핑 등을 사용 하 여 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-121">This example enables encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryption key by using key encryption key.</span></span>

## <span data-ttu-id="7e90f-122">변수</span><span class="sxs-lookup"><span data-stu-id="7e90f-122">PARAMETERS</span></span>

### <span data-ttu-id="7e90f-123">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="7e90f-123">-AadClientCertThumbprint</span></span>
<span data-ttu-id="7e90f-124">**Keyvault** 에 비밀을 쓸 수 있는 권한이 있는 Azureactive Directory (Azure AD) 응용 프로그램 클라이언트 인증서의 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-124">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="7e90f-125">필수 구성 요소는 Azure AD 클라이언트 인증서를 이전에 가상 컴퓨터의 로컬 컴퓨터 인증서 저장소에 배포 해야 합니다 `my` .</span><span class="sxs-lookup"><span data-stu-id="7e90f-125">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="7e90f-126">Add-AzureRmVMSecret cmdlet은 Azure의 가상 컴퓨터에 인증서를 배포 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-126">The Add-AzureRmVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="7e90f-127">자세한 내용은 **AzureRmVMSecret** cmdlet 도움말을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7e90f-127">For more details, see the **Add-AzureRmVMSecret** cmdlet help.</span></span>
<span data-ttu-id="7e90f-128">인증서를 이전에 가상 컴퓨터 로컬 컴퓨터의 인증서 저장소에 배포 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-128">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: String
Parameter Sets: AADClientCertParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e90f-129">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="7e90f-129">-AadClientID</span></span>
<span data-ttu-id="7e90f-130">**Keyvault** 에 비밀을 쓸 수 있는 권한이 있는 Azure AD 응용 프로그램의 클라이언트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-130">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e90f-131">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="7e90f-131">-AadClientSecret</span></span>
<span data-ttu-id="7e90f-132">**Keyvault** 에 비밀을 쓸 수 있는 권한이 있는 Azure AD 응용 프로그램의 클라이언트 비밀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-132">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: String
Parameter Sets: AADClientSecretParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e90f-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e90f-133">-DefaultProfile</span></span>
<span data-ttu-id="7e90f-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e90f-135">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="7e90f-135">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="7e90f-136">이 cmdlet이 확장의 부 버전에 대 한 자동 업그레이드를 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-136">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e90f-137">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="7e90f-137">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="7e90f-138">가상 머신 암호화 키를 업로드 해야 하는 **Keyvault** 의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-138">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e90f-139">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="7e90f-139">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="7e90f-140">가상 컴퓨터 암호화 키를 업로드 해야 하는 **Keyvault** URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-140">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e90f-141">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="7e90f-141">-EncryptFormatAll</span></span>
<span data-ttu-id="7e90f-142">아직 암호화 되지 않은 모든 데이터 드라이브 Encrypt-Format</span><span class="sxs-lookup"><span data-stu-id="7e90f-142">Encrypt-Format all data drives that are not already encrypted</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e90f-143">-Extension# ername</span><span class="sxs-lookup"><span data-stu-id="7e90f-143">-ExtensionPublisherName</span></span>
<span data-ttu-id="7e90f-144">확장명 게시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-144">The extension publisher name.</span></span> <span data-ttu-id="7e90f-145">"Microsoft. i i."의 기본값을 재정의 하려면이 매개 변수만 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-145">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e90f-146">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="7e90f-146">-ExtensionType</span></span>
<span data-ttu-id="7e90f-147">확장 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-147">The extension type.</span></span> <span data-ttu-id="7e90f-148">이 매개 변수를 지정 하면 Windows Vm에 대 한 "AzureDiskEncryption"의 기본값을 재정의 하 고 Linux 용으로 "Azurediskencryption Forlinux"를 재정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-148">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e90f-149">-Force</span><span class="sxs-lookup"><span data-stu-id="7e90f-149">-Force</span></span>
<span data-ttu-id="7e90f-150">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-150">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e90f-151">-Keya 알고리즘</span><span class="sxs-lookup"><span data-stu-id="7e90f-151">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="7e90f-152">가상 컴퓨터의 키 암호화 키를 래핑하고 래핑을 해제 하는 데 사용 되는 알고리즘을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-152">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="7e90f-153">기본 값은 RSA-OAEP입니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-153">The default value is RSA-OAEP.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e90f-154">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="7e90f-154">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="7e90f-155">가상 컴퓨터 암호화 키를 래핑하고 래핑 해제 하는 데 사용 되는 키 암호화 키의 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-155">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="7e90f-156">정식 버전의 URL 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-156">This must be the full versioned URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e90f-157">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="7e90f-157">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="7e90f-158">가상 컴퓨터 암호화 키를 래핑하고 래핑 해제 하는 데 사용 되는 키 암호화 키를 포함 하는 **Keyvault** 의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-158">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="7e90f-159">정식 버전의 URL 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-159">This must be a full versioned URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e90f-160">-이름</span><span class="sxs-lookup"><span data-stu-id="7e90f-160">-Name</span></span>
<span data-ttu-id="7e90f-161">확장을 나타내는 Azure Resource Manager 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-161">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="7e90f-162">기본값은 Windows 운영 체제를 실행 하는 가상 컴퓨터에 대 한 AzureDiskEncryption (Linux 용 Azurediskencryption Linux 가상 머신의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-162">The default value is AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e90f-163">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="7e90f-163">-Passphrase</span></span>
<span data-ttu-id="7e90f-164">Linux 가상 컴퓨터만 암호화 하는 데 사용 되는 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-164">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="7e90f-165">이 매개 변수는 Windows 운영 체제를 실행 하는 가상 컴퓨터에는 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-165">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e90f-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e90f-166">-ResourceGroupName</span></span>
<span data-ttu-id="7e90f-167">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-167">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e90f-168">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="7e90f-168">-SequenceVersion</span></span>
<span data-ttu-id="7e90f-169">가상 컴퓨터에 대 한 암호화 작업의 시퀀스 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-169">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="7e90f-170">이는 동일한 가상 컴퓨터에서 수행 하는 각 암호화 작업 마다 고유 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-170">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="7e90f-171">Get-AzureRmVMExtension cmdlet은 사용 된 이전 시퀀스 번호를 검색 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-171">The Get-AzureRmVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e90f-172">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="7e90f-172">-SkipVmBackup</span></span>
<span data-ttu-id="7e90f-173">Linux Vm에 대 한 백업 만들기 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="7e90f-173">Skip backup creation for Linux VMs</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e90f-174">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="7e90f-174">-TypeHandlerVersion</span></span>
<span data-ttu-id="7e90f-175">암호화 확장명의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-175">Specifies the version of the encryption extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e90f-176">-VMName</span><span class="sxs-lookup"><span data-stu-id="7e90f-176">-VMName</span></span>
<span data-ttu-id="7e90f-177">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-177">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e90f-178">-가이 Etype</span><span class="sxs-lookup"><span data-stu-id="7e90f-178">-VolumeType</span></span>
<span data-ttu-id="7e90f-179">암호화 작업을 수행할 가상 컴퓨터 볼륨의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-179">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="7e90f-180">Windows 운영 체제를 실행 하는 가상 컴퓨터에 허용 되는 값은 모든, OS, 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-180">Allowed values for virtual machines that run the Windows operating system are as follows: All, OS, and Data.</span></span>
<span data-ttu-id="7e90f-181">Linux 가상 머신에 허용 되는 값은 다음과 같습니다: 데이터에만 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-181">The allowed values for Linux virtual machines are as follows: Data only.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e90f-182">-확인</span><span class="sxs-lookup"><span data-stu-id="7e90f-182">-Confirm</span></span>
<span data-ttu-id="7e90f-183">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-183">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e90f-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e90f-184">-WhatIf</span></span>
<span data-ttu-id="7e90f-185">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-185">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="7e90f-186">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-186">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e90f-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e90f-187">CommonParameters</span></span>
<span data-ttu-id="7e90f-188">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e90f-189">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e90f-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e90f-190">입력</span><span class="sxs-lookup"><span data-stu-id="7e90f-190">INPUTS</span></span>

### <span data-ttu-id="7e90f-191">않아야</span><span class="sxs-lookup"><span data-stu-id="7e90f-191">None</span></span>
<span data-ttu-id="7e90f-192">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-192">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7e90f-193">출력</span><span class="sxs-lookup"><span data-stu-id="7e90f-193">OUTPUTS</span></span>

### <span data-ttu-id="7e90f-194">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="7e90f-194">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7e90f-195">상속자</span><span class="sxs-lookup"><span data-stu-id="7e90f-195">NOTES</span></span>

## <span data-ttu-id="7e90f-196">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e90f-196">RELATED LINKS</span></span>

[<span data-ttu-id="7e90f-197">추가-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="7e90f-197">Add-AzureRmVMSecret</span></span>](./Add-AzureRmVMSecret.md)

[<span data-ttu-id="7e90f-198">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="7e90f-198">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="7e90f-199">제거-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="7e90f-199">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)


