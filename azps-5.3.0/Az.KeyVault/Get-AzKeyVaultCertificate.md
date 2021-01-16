---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: 002cfba4a5660fa8996c30ff83a1011da669539b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386380"
---
# <span data-ttu-id="90abe-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="90abe-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="90abe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90abe-102">SYNOPSIS</span></span>
<span data-ttu-id="90abe-103">키 자격 증명 모음에서 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90abe-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="90abe-104">구문</span><span class="sxs-lookup"><span data-stu-id="90abe-104">SYNTAX</span></span>

### <span data-ttu-id="90abe-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="90abe-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90abe-106">ByCertificateNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="90abe-106">ByCertificateNameAndVersion</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90abe-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="90abe-107">ByCertificateAllVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90abe-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="90abe-108">ByNameInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90abe-109">ByCertificateNameAndVersionInputObject</span><span class="sxs-lookup"><span data-stu-id="90abe-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90abe-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="90abe-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90abe-111">ByNameResourceId</span><span class="sxs-lookup"><span data-stu-id="90abe-111">ByNameResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90abe-112">ByCertificateNameAndVersionResourceId</span><span class="sxs-lookup"><span data-stu-id="90abe-112">ByCertificateNameAndVersionResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90abe-113">ByCertificateAllVersionsResourceId</span><span class="sxs-lookup"><span data-stu-id="90abe-113">ByCertificateAllVersionsResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90abe-114">설명</span><span class="sxs-lookup"><span data-stu-id="90abe-114">DESCRIPTION</span></span>
<span data-ttu-id="90abe-115">**Get-AzKeyVaultCertificate** cmdlet은 Azure Key Vault의 키 자격 증명 모음에서 지정된 인증서 또는 인증서 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90abe-115">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="90abe-116">예제</span><span class="sxs-lookup"><span data-stu-id="90abe-116">EXAMPLES</span></span>

### <span data-ttu-id="90abe-117">예제 1: 인증서 얻기</span><span class="sxs-lookup"><span data-stu-id="90abe-117">Example 1: Get a certificate</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject] 
                CN=contoso.com

              [Issuer] 
                CN=contoso.com

              [Serial Number] 
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before] 
                2/8/2016 3:11:45 PM

              [Not After] 
                8/8/2016 4:21:45 PM

              [Thumbprint] 
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId       : https://contoso.vault.azure.net:443/keys/TestCert01/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
SecretId    : https://contoso.vault.azure.net:443/secrets/TestCert01/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

### <span data-ttu-id="90abe-118">예제 2: 인증을 구하고 pfx로 저장</span><span class="sxs-lookup"><span data-stu-id="90abe-118">Example 2: Get cert and save it as pfx</span></span>
<span data-ttu-id="90abe-119">이 명령은 ContosoKV01이라는 키 자격 증명 모음에서 TestCert01이라는 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90abe-119">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span> <span data-ttu-id="90abe-120">인증서를 pfx 파일로 다운로드하려면 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="90abe-120">To download the certificate as pfx file, run following command.</span></span> <span data-ttu-id="90abe-121">이러한 명령은 SecretId에 액세스한 다음 콘텐츠를 pfx 파일로 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="90abe-121">These commands access SecretId and then save the content as a pfx file.</span></span>

```powershell
$cert = Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
$secret = Get-AzKeyVaultSecret -VaultName $vaultName -Name $cert.Name -AsPlainText
$secretByte = [Convert]::FromBase64String($secret)
$x509Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($secretByte, "", "Exportable,PersistKeySet")
$type = [System.Security.Cryptography.X509Certificates.X509ContentType]::Pfx
$pfxFileByte = $x509Cert.Export($type, $password)

# Write to a file
[System.IO.File]::WriteAllBytes("KeyVault.pfx", $pfxFileByte)
```

### <span data-ttu-id="90abe-122">예제 3: 이 키 자격 증명 모음에 대해 삭제했지만 제거되지 않은 모든 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90abe-122">Example 3: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName 'contoso' -InRemovedState

DeletedDate        : 5/24/2018 6:08:32 PM
Enabled            : True
Expires            : 11/24/2018 6:08:13 PM
NotBefore          : 5/24/2018 5:58:13 PM
Created            : 5/24/2018 6:08:13 PM
Updated            : 5/24/2018 6:08:13 PM
Tags               :
VaultName          : contoso
Name               : test1
Version            :
Id                 : https://contoso.vault.azure.net:443/certificates/test1

ScheduledPurgeDate : 8/22/2018 6:10:47 PM
DeletedDate        : 5/24/2018 6:10:47 PM
Enabled            : True
Expires            : 11/24/2018 6:09:44 PM
NotBefore          : 5/24/2018 5:59:44 PM
Created            : 5/24/2018 6:09:44 PM
Updated            : 5/24/2018 6:09:44 PM
Tags               :
VaultName          : contoso
Name               : test2
Version            :
Id                 : https://contoso.vault.azure.net:443/certificates/test2
```

<span data-ttu-id="90abe-123">이 명령은 Contoso라는 키 자격 증명 모음에서 이전에 삭제했지만 제거되지 않은 모든 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90abe-123">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="90abe-124">예제 4: 이 키 자격 증명 모음에 대해 삭제했지만 제거되지 않은 인증서 MyCert를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90abe-124">Example 4: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName 'contoso' -Name 'test1' -InRemovedState

Certificate        : [Subject]
                       CN=contoso.com

                     [Issuer]
                       CN=contoso.com

                     [Serial Number]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                     [Not Before]
                       5/24/2018 10:58:13 AM

                     [Not After]
                       11/24/2018 10:08:13 AM

                     [Thumbprint]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId              : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
SecretId           : https://contoso.vault.azure.net:443/secrets/test1/7fe415d5518240c1a6fce89986b8d334
Thumbprint         : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel      : Recoverable+Purgeable
ScheduledPurgeDate : 8/22/2018 6:08:32 PM
DeletedDate        : 5/24/2018 6:08:32 PM
Enabled            : True
Expires            : 11/24/2018 6:08:13 PM
NotBefore          : 5/24/2018 5:58:13 PM
Created            : 5/24/2018 6:08:13 PM
Updated            : 5/24/2018 6:08:13 PM
Tags               :
VaultName          : contoso
Name               : test1
Version            : 7fe415d5518240c1a6fce89986b8d334
Id                 : https://contoso.vault.azure.net:443/certificates/test1/7fe415d5518240c1a6fce89986b8d334
```

<span data-ttu-id="90abe-125">이 명령은 Contoso라는 키 자격 증명 모음에서 이전에 삭제했지만 제거되지 않은 'MyCert'라는 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90abe-125">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="90abe-126">이 명령은 삭제 날짜 및 이 삭제된 인증서의 예약된 제거 날짜와 같은 메타데이터를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="90abe-126">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

### <span data-ttu-id="90abe-127">예제 5: 필터링을 사용하여 인증서 나열</span><span class="sxs-lookup"><span data-stu-id="90abe-127">Example 5: List certificates using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "test*"

Enabled   : True
Expires   : 8/5/2019 2:39:25 AM
NotBefore : 2/5/2019 2:29:25 AM
Created   : 2/5/2019 2:39:25 AM
Updated   : 2/5/2019 2:39:25 AM
Tags      :
VaultName : ContosoKV01
Name      : test1
Version   :
Id        : https://ContosoKV01.vault.azure.net:443/certificates/test1

Enabled   : True
Expires   : 8/5/2019 2:39:25 AM
NotBefore : 2/5/2019 2:29:25 AM
Created   : 2/5/2019 2:39:25 AM
Updated   : 2/5/2019 2:39:25 AM
Tags      :
VaultName : ContosoKV01
Name      : test2
Version   :
Id        : https://ContosoKV01.vault.azure.net:443/certificates/test2

This command gets all certificates starting with "test" from the key vault named ContosoKV01.
```

## <span data-ttu-id="90abe-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90abe-128">PARAMETERS</span></span>

### <span data-ttu-id="90abe-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90abe-129">-DefaultProfile</span></span>
<span data-ttu-id="90abe-130">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="90abe-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90abe-131">-IncludePending</span><span class="sxs-lookup"><span data-stu-id="90abe-131">-IncludePending</span></span>
<span data-ttu-id="90abe-132">출력에 보류 중인 인증서를 포함할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90abe-132">Specifies whether to include pending certificates in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90abe-133">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="90abe-133">-IncludeVersions</span></span>
<span data-ttu-id="90abe-134">이 작업에서 모든 버전의 인증서를 얻게 됐습니다.</span><span class="sxs-lookup"><span data-stu-id="90abe-134">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByCertificateAllVersions, ByCertificateAllVersionsInputObject, ByCertificateAllVersionsResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90abe-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90abe-135">-InputObject</span></span>
<span data-ttu-id="90abe-136">KeyVault 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="90abe-136">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByNameInputObject, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90abe-137">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="90abe-137">-InRemovedState</span></span>
<span data-ttu-id="90abe-138">출력에 이전에 삭제된 인증서를 포함할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90abe-138">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90abe-139">-Name</span><span class="sxs-lookup"><span data-stu-id="90abe-139">-Name</span></span>
<span data-ttu-id="90abe-140">얻을 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90abe-140">Specifies the name of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="90abe-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90abe-141">-ResourceId</span></span>
<span data-ttu-id="90abe-142">KeyVault 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="90abe-142">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameResourceId, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90abe-143">-VaultName</span><span class="sxs-lookup"><span data-stu-id="90abe-143">-VaultName</span></span>
<span data-ttu-id="90abe-144">키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90abe-144">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByCertificateNameAndVersion, ByCertificateAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90abe-145">-Version</span><span class="sxs-lookup"><span data-stu-id="90abe-145">-Version</span></span>
<span data-ttu-id="90abe-146">인증서의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90abe-146">Specifies the version of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateNameAndVersionInputObject, ByCertificateNameAndVersionResourceId
Aliases: CertificateVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90abe-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90abe-147">CommonParameters</span></span>
<span data-ttu-id="90abe-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="90abe-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90abe-149">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="90abe-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90abe-150">입력</span><span class="sxs-lookup"><span data-stu-id="90abe-150">INPUTS</span></span>

### <span data-ttu-id="90abe-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="90abe-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="90abe-152">System.String</span><span class="sxs-lookup"><span data-stu-id="90abe-152">System.String</span></span>

## <span data-ttu-id="90abe-153">출력</span><span class="sxs-lookup"><span data-stu-id="90abe-153">OUTPUTS</span></span>

### <span data-ttu-id="90abe-154">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="90abe-154">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

### <span data-ttu-id="90abe-155">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="90abe-155">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

### <span data-ttu-id="90abe-156">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="90abe-156">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

### <span data-ttu-id="90abe-157">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="90abe-157">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="90abe-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="90abe-158">NOTES</span></span>

## <span data-ttu-id="90abe-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90abe-159">RELATED LINKS</span></span>

[<span data-ttu-id="90abe-160">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="90abe-160">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="90abe-161">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="90abe-161">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="90abe-162">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="90abe-162">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="90abe-163">Undo-AzKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="90abe-163">Undo-AzKeyVaultSecretCertificate</span></span>](./Undo-AzKeyVaultSecretCertificate.md)
