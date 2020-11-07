---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
ms.openlocfilehash: 1e8288b8e580b8ce4b23a54f5bef3d351f832862
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703854"
---
# <span data-ttu-id="a29b4-101">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a29b4-101">Get-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="a29b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a29b4-102">SYNOPSIS</span></span>
<span data-ttu-id="a29b4-103">키 자격 증명 모음에서 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a29b4-103">Gets a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a29b4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a29b4-104">SYNTAX</span></span>

### <span data-ttu-id="a29b4-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="a29b4-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-IncludePending] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a29b4-106">ByCertificateNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="a29b4-106">ByCertificateNameAndVersion</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a29b4-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="a29b4-107">ByCertificateAllVersions</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a29b4-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="a29b4-108">ByNameInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-IncludePending] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a29b4-109">ByCertificateNameAndVersionInputObject</span><span class="sxs-lookup"><span data-stu-id="a29b4-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a29b4-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="a29b4-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a29b4-111">ByNameResourceId</span><span class="sxs-lookup"><span data-stu-id="a29b4-111">ByNameResourceId</span></span>
```
Get-AzureKeyVaultCertificate [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-IncludePending] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a29b4-112">ByCertificateNameAndVersionResourceId</span><span class="sxs-lookup"><span data-stu-id="a29b4-112">ByCertificateNameAndVersionResourceId</span></span>
```
Get-AzureKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a29b4-113">ByCertificateAllVersionsResourceId</span><span class="sxs-lookup"><span data-stu-id="a29b4-113">ByCertificateAllVersionsResourceId</span></span>
```
Get-AzureKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a29b4-114">설명은</span><span class="sxs-lookup"><span data-stu-id="a29b4-114">DESCRIPTION</span></span>
<span data-ttu-id="a29b4-115">**AzureKeyVaultCertificate** cmdlet은 지정 된 인증서 또는 Azure key vault의 키 자격 증명 모음에서 인증서의 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a29b4-115">The **Get-AzureKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="a29b4-116">예제의</span><span class="sxs-lookup"><span data-stu-id="a29b4-116">EXAMPLES</span></span>

### <span data-ttu-id="a29b4-117">예제 1: 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="a29b4-117">Example 1: Get a certificate</span></span>
```powershell
PS C:\> Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
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

<span data-ttu-id="a29b4-118">이 명령은 ContosoKV01 이라는 키 보관소에서 TestCert01 라는 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a29b4-118">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="a29b4-119">예제 2: 삭제 했지만이 키 보관소에는 제거 되지 않은 모든 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a29b4-119">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzureKeyVaultCertificate -VaultName 'contoso' -InRemovedState

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

<span data-ttu-id="a29b4-120">이 명령은 Contoso 라는 키 보관소에서 이전에 삭제 했지만 제거 되지 않은 모든 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a29b4-120">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="a29b4-121">예제 3: 삭제 되었지만이 키 보관소에는 제거 되지 않은 인증서 MyCert 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a29b4-121">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzureKeyVaultCertificate -VaultName 'contoso' -Name 'test1' -InRemovedState

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

<span data-ttu-id="a29b4-122">이 명령은 Contoso 라는 키 보관소에서 이전에 삭제 되었지만 제거 되지 않은 ' MyCert ' 라는 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a29b4-122">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="a29b4-123">이 명령은 삭제 날짜 등의 메타 데이터와 해당 인증서의 예정 된 제거 날짜 등을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a29b4-123">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="a29b4-124">변수</span><span class="sxs-lookup"><span data-stu-id="a29b4-124">PARAMETERS</span></span>

### <span data-ttu-id="a29b4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a29b4-125">-DefaultProfile</span></span>
<span data-ttu-id="a29b4-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a29b4-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a29b4-127">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="a29b4-127">-IncludeVersions</span></span>
<span data-ttu-id="a29b4-128">이 작업이 모든 버전의 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a29b4-128">Indicates that this operation gets all versions of the certificate.</span></span>

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

### <span data-ttu-id="a29b4-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a29b4-129">-InputObject</span></span>
<span data-ttu-id="a29b4-130">KeyVault 개체.</span><span class="sxs-lookup"><span data-stu-id="a29b4-130">KeyVault object.</span></span>

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

### <span data-ttu-id="a29b4-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="a29b4-131">-InRemovedState</span></span>
<span data-ttu-id="a29b4-132">출력에 이전에 삭제 된 인증서를 포함할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a29b4-132">Specifies whether to include previously deleted certificates in the output</span></span>

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

### <span data-ttu-id="a29b4-133">-이름</span><span class="sxs-lookup"><span data-stu-id="a29b4-133">-Name</span></span>
<span data-ttu-id="a29b4-134">가져올 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a29b4-134">Specifies the name of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a29b4-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a29b4-135">-ResourceId</span></span>
<span data-ttu-id="a29b4-136">KeyVault 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="a29b4-136">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="a29b4-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a29b4-137">-VaultName</span></span>
<span data-ttu-id="a29b4-138">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a29b4-138">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="a29b4-139">-버전</span><span class="sxs-lookup"><span data-stu-id="a29b4-139">-Version</span></span>
<span data-ttu-id="a29b4-140">인증서의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a29b4-140">Specifies the version of a certificate.</span></span>

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

### <span data-ttu-id="a29b4-141">-IncludePending</span><span class="sxs-lookup"><span data-stu-id="a29b4-141">-IncludePending</span></span>
<span data-ttu-id="a29b4-142">출력에 보류 중인 인증서를 포함할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a29b4-142">Specifies whether to include pending certificates in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a29b4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a29b4-143">CommonParameters</span></span>
<span data-ttu-id="a29b4-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a29b4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a29b4-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a29b4-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a29b4-146">입력</span><span class="sxs-lookup"><span data-stu-id="a29b4-146">INPUTS</span></span>

### <span data-ttu-id="a29b4-147">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a29b4-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="a29b4-148">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a29b4-148">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="a29b4-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a29b4-149">System.String</span></span>

## <span data-ttu-id="a29b4-150">출력</span><span class="sxs-lookup"><span data-stu-id="a29b4-150">OUTPUTS</span></span>

### <span data-ttu-id="a29b4-151">Microsoft. KeyVault. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a29b4-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

### <span data-ttu-id="a29b4-152">Microsoft. KeyVault. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a29b4-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

### <span data-ttu-id="a29b4-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a29b4-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

### <span data-ttu-id="a29b4-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a29b4-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="a29b4-155">상속자</span><span class="sxs-lookup"><span data-stu-id="a29b4-155">NOTES</span></span>

## <span data-ttu-id="a29b4-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a29b4-156">RELATED LINKS</span></span>

[<span data-ttu-id="a29b4-157">추가-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a29b4-157">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="a29b4-158">가져오기-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a29b4-158">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="a29b4-159">제거-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a29b4-159">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="a29b4-160">실행 취소-AzureKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="a29b4-160">Undo-AzureKeyVaultSecretCertificate</span></span>](./Undo-AzureKeyVaultSecretCertificate.md)
