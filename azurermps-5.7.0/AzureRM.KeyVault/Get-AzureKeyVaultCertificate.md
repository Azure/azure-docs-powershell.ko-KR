---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
ms.openlocfilehash: 87b030229eb2a1f4bb91122aaec8a119134d27fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528949"
---
# <span data-ttu-id="14e4d-101">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="14e4d-101">Get-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="14e4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14e4d-102">SYNOPSIS</span></span>
<span data-ttu-id="14e4d-103">키 자격 증명 모음에서 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14e4d-103">Gets a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14e4d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="14e4d-104">SYNTAX</span></span>

### <span data-ttu-id="14e4d-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="14e4d-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14e4d-106">ByCertificateNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="14e4d-106">ByCertificateNameAndVersion</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14e4d-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="14e4d-107">ByCertificateAllVersions</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14e4d-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="14e4d-108">ByNameInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14e4d-109">ByCertificateNameAndVersionInputObject</span><span class="sxs-lookup"><span data-stu-id="14e4d-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14e4d-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="14e4d-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14e4d-111">설명은</span><span class="sxs-lookup"><span data-stu-id="14e4d-111">DESCRIPTION</span></span>
<span data-ttu-id="14e4d-112">**AzureKeyVaultCertificate** cmdlet은 지정 된 인증서 또는 Azure key vault의 키 자격 증명 모음에서 인증서의 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14e4d-112">The **Get-AzureKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="14e4d-113">예제의</span><span class="sxs-lookup"><span data-stu-id="14e4d-113">EXAMPLES</span></span>

### <span data-ttu-id="14e4d-114">예제 1: 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="14e4d-114">Example 1: Get a certificate</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject] 
                CN=contoso.com

              [Issuer] 
                CN=contoso.com

              [Serial Number] 
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before] 
                2/8/2016 3:11:45 PM

              [Not After] 
                8/8/2016 4:21:45 PM

              [Thumbprint] 
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="14e4d-115">이 명령은 ContosoKV01 이라는 키 보관소에서 TestCert01 라는 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14e4d-115">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="14e4d-116">예제 2: 삭제 했지만이 키 보관소에는 제거 되지 않은 모든 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14e4d-116">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="14e4d-117">이 명령은 Contoso 라는 키 보관소에서 이전에 삭제 했지만 제거 되지 않은 모든 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14e4d-117">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="14e4d-118">예제 3: 삭제 되었지만이 키 보관소에는 제거 되지 않은 인증서 MyCert 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14e4d-118">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="14e4d-119">이 명령은 Contoso 라는 키 보관소에서 이전에 삭제 되었지만 제거 되지 않은 ' MyCert ' 라는 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14e4d-119">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="14e4d-120">이 명령은 삭제 날짜 등의 메타 데이터와 해당 인증서의 예정 된 제거 날짜 등을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="14e4d-120">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="14e4d-121">변수</span><span class="sxs-lookup"><span data-stu-id="14e4d-121">PARAMETERS</span></span>

### <span data-ttu-id="14e4d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14e4d-122">-DefaultProfile</span></span>
<span data-ttu-id="14e4d-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="14e4d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14e4d-124">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="14e4d-124">-IncludeVersions</span></span>
<span data-ttu-id="14e4d-125">이 작업이 모든 버전의 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14e4d-125">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByCertificateAllVersions, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e4d-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14e4d-126">-InputObject</span></span>
<span data-ttu-id="14e4d-127">KeyVault 개체.</span><span class="sxs-lookup"><span data-stu-id="14e4d-127">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByNameInputObject, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14e4d-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="14e4d-128">-InRemovedState</span></span>
<span data-ttu-id="14e4d-129">출력에 이전에 삭제 된 인증서를 포함할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14e4d-129">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByName, ByNameInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e4d-130">-이름</span><span class="sxs-lookup"><span data-stu-id="14e4d-130">-Name</span></span>
<span data-ttu-id="14e4d-131">가져올 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14e4d-131">Specifies the name of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByNameInputObject
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14e4d-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="14e4d-132">-VaultName</span></span>
<span data-ttu-id="14e4d-133">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14e4d-133">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByCertificateNameAndVersion, ByCertificateAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14e4d-134">-버전</span><span class="sxs-lookup"><span data-stu-id="14e4d-134">-Version</span></span>
<span data-ttu-id="14e4d-135">인증서의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14e4d-135">Specifies the version of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateNameAndVersionInputObject
Aliases: CertificateVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14e4d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14e4d-136">CommonParameters</span></span>
<span data-ttu-id="14e4d-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="14e4d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14e4d-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14e4d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14e4d-139">입력</span><span class="sxs-lookup"><span data-stu-id="14e4d-139">INPUTS</span></span>

### <span data-ttu-id="14e4d-140">않아야</span><span class="sxs-lookup"><span data-stu-id="14e4d-140">None</span></span>
<span data-ttu-id="14e4d-141">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="14e4d-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="14e4d-142">출력</span><span class="sxs-lookup"><span data-stu-id="14e4d-142">OUTPUTS</span></span>

### <span data-ttu-id="14e4d-143">PSKeyVaultCertificateIdentityItem의 ' 1 [Microsoft Azure.] 목록. List.</span><span class="sxs-lookup"><span data-stu-id="14e4d-143">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem]</span></span>

### <span data-ttu-id="14e4d-144">Microsoft. KeyVault. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="14e4d-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="14e4d-145">상속자</span><span class="sxs-lookup"><span data-stu-id="14e4d-145">NOTES</span></span>

## <span data-ttu-id="14e4d-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14e4d-146">RELATED LINKS</span></span>

[<span data-ttu-id="14e4d-147">추가-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="14e4d-147">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="14e4d-148">가져오기-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="14e4d-148">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="14e4d-149">제거-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="14e4d-149">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="14e4d-150">실행 취소-AzureKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="14e4d-150">Undo-AzureKeyVaultSecretCertificate</span></span>](./Undo-AzureKeyVaultSecretCertificate.md)
