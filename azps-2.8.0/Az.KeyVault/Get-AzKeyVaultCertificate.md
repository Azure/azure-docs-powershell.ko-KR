---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: 5935706c341fac5f0b26d3e4965f226342c3dfc8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689668"
---
# <span data-ttu-id="84830-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="84830-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="84830-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84830-102">SYNOPSIS</span></span>
<span data-ttu-id="84830-103">키 자격 증명 모음에서 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="84830-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="84830-104">구문과</span><span class="sxs-lookup"><span data-stu-id="84830-104">SYNTAX</span></span>

### <span data-ttu-id="84830-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="84830-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84830-106">ByCertificateNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="84830-106">ByCertificateNameAndVersion</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84830-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="84830-107">ByCertificateAllVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84830-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="84830-108">ByNameInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84830-109">ByCertificateNameAndVersionInputObject</span><span class="sxs-lookup"><span data-stu-id="84830-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84830-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="84830-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84830-111">ByNameResourceId</span><span class="sxs-lookup"><span data-stu-id="84830-111">ByNameResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84830-112">ByCertificateNameAndVersionResourceId</span><span class="sxs-lookup"><span data-stu-id="84830-112">ByCertificateNameAndVersionResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84830-113">ByCertificateAllVersionsResourceId</span><span class="sxs-lookup"><span data-stu-id="84830-113">ByCertificateAllVersionsResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84830-114">설명은</span><span class="sxs-lookup"><span data-stu-id="84830-114">DESCRIPTION</span></span>
<span data-ttu-id="84830-115">**AzKeyVaultCertificate** cmdlet은 지정 된 인증서 또는 Azure key vault의 키 자격 증명 모음에서 인증서의 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="84830-115">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="84830-116">예제의</span><span class="sxs-lookup"><span data-stu-id="84830-116">EXAMPLES</span></span>

### <span data-ttu-id="84830-117">예제 1: 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="84830-117">Example 1: Get a certificate</span></span>
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

Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="84830-118">이 명령은 ContosoKV01 이라는 키 보관소에서 TestCert01 라는 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="84830-118">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="84830-119">예제 2: 삭제 했지만이 키 보관소에는 제거 되지 않은 모든 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="84830-119">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="84830-120">이 명령은 Contoso 라는 키 보관소에서 이전에 삭제 했지만 제거 되지 않은 모든 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="84830-120">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="84830-121">예제 3: 삭제 되었지만이 키 보관소에는 제거 되지 않은 인증서 MyCert 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="84830-121">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="84830-122">이 명령은 Contoso 라는 키 보관소에서 이전에 삭제 되었지만 제거 되지 않은 ' MyCert ' 라는 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="84830-122">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="84830-123">이 명령은 삭제 날짜 등의 메타 데이터와 해당 인증서의 예정 된 제거 날짜 등을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="84830-123">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

### <span data-ttu-id="84830-124">예제 4: 필터링을 사용 하 여 인증서 목록 표시</span><span class="sxs-lookup"><span data-stu-id="84830-124">Example 4: List certificates using filtering</span></span>
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

## <span data-ttu-id="84830-125">변수</span><span class="sxs-lookup"><span data-stu-id="84830-125">PARAMETERS</span></span>

### <span data-ttu-id="84830-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84830-126">-DefaultProfile</span></span>
<span data-ttu-id="84830-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="84830-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84830-128">-IncludePending</span><span class="sxs-lookup"><span data-stu-id="84830-128">-IncludePending</span></span>
<span data-ttu-id="84830-129">출력에 보류 중인 인증서를 포함할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84830-129">Specifies whether to include pending certificates in the output</span></span>

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

### <span data-ttu-id="84830-130">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="84830-130">-IncludeVersions</span></span>
<span data-ttu-id="84830-131">이 작업이 모든 버전의 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="84830-131">Indicates that this operation gets all versions of the certificate.</span></span>

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

### <span data-ttu-id="84830-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84830-132">-InputObject</span></span>
<span data-ttu-id="84830-133">KeyVault 개체.</span><span class="sxs-lookup"><span data-stu-id="84830-133">KeyVault object.</span></span>

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

### <span data-ttu-id="84830-134">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="84830-134">-InRemovedState</span></span>
<span data-ttu-id="84830-135">출력에 이전에 삭제 된 인증서를 포함할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84830-135">Specifies whether to include previously deleted certificates in the output</span></span>

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

### <span data-ttu-id="84830-136">-이름</span><span class="sxs-lookup"><span data-stu-id="84830-136">-Name</span></span>
<span data-ttu-id="84830-137">가져올 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84830-137">Specifies the name of the certificate to get.</span></span>

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

### <span data-ttu-id="84830-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84830-138">-ResourceId</span></span>
<span data-ttu-id="84830-139">KeyVault 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="84830-139">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="84830-140">-VaultName</span><span class="sxs-lookup"><span data-stu-id="84830-140">-VaultName</span></span>
<span data-ttu-id="84830-141">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84830-141">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="84830-142">-버전</span><span class="sxs-lookup"><span data-stu-id="84830-142">-Version</span></span>
<span data-ttu-id="84830-143">인증서의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84830-143">Specifies the version of a certificate.</span></span>

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

### <span data-ttu-id="84830-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84830-144">CommonParameters</span></span>
<span data-ttu-id="84830-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="84830-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84830-146">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="84830-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84830-147">입력</span><span class="sxs-lookup"><span data-stu-id="84830-147">INPUTS</span></span>

### <span data-ttu-id="84830-148">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="84830-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="84830-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="84830-149">System.String</span></span>

## <span data-ttu-id="84830-150">출력</span><span class="sxs-lookup"><span data-stu-id="84830-150">OUTPUTS</span></span>

### <span data-ttu-id="84830-151">Microsoft. KeyVault. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="84830-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

### <span data-ttu-id="84830-152">Microsoft. KeyVault. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="84830-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

### <span data-ttu-id="84830-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="84830-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

### <span data-ttu-id="84830-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="84830-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="84830-155">상속자</span><span class="sxs-lookup"><span data-stu-id="84830-155">NOTES</span></span>

## <span data-ttu-id="84830-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84830-156">RELATED LINKS</span></span>

[<span data-ttu-id="84830-157">추가-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="84830-157">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="84830-158">가져오기-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="84830-158">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="84830-159">제거-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="84830-159">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="84830-160">실행 취소-AzKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="84830-160">Undo-AzKeyVaultSecretCertificate</span></span>](./Undo-AzKeyVaultSecretCertificate.md)
