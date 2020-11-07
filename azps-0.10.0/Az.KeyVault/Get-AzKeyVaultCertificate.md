---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: 40514bdd6ed8d37679d3002f80146e622a0614e9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875843"
---
# <span data-ttu-id="2bef2-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2bef2-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="2bef2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bef2-102">SYNOPSIS</span></span>
<span data-ttu-id="2bef2-103">키 자격 증명 모음에서 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2bef2-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="2bef2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2bef2-104">SYNTAX</span></span>

### <span data-ttu-id="2bef2-105">ByVaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="2bef2-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2bef2-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="2bef2-106">ByCertificateName</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bef2-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="2bef2-107">ByCertificateVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bef2-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="2bef2-108">ByDeletedCertificates</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bef2-109">설명은</span><span class="sxs-lookup"><span data-stu-id="2bef2-109">DESCRIPTION</span></span>
<span data-ttu-id="2bef2-110">**AzKeyVaultCertificate** cmdlet은 지정 된 인증서 또는 Azure key vault의 키 자격 증명 모음에서 인증서의 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2bef2-110">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="2bef2-111">예제의</span><span class="sxs-lookup"><span data-stu-id="2bef2-111">EXAMPLES</span></span>

### <span data-ttu-id="2bef2-112">예제 1: 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="2bef2-112">Example 1: Get a certificate</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
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

<span data-ttu-id="2bef2-113">이 명령은 ContosoKV01 이라는 키 보관소에서 TestCert01 라는 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2bef2-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="2bef2-114">예제 2: 삭제 했지만이 키 보관소에는 제거 되지 않은 모든 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2bef2-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="2bef2-115">이 명령은 Contoso 라는 키 보관소에서 이전에 삭제 했지만 제거 되지 않은 모든 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2bef2-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="2bef2-116">예제 3: 삭제 되었지만이 키 보관소에는 제거 되지 않은 인증서 MyCert 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2bef2-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="2bef2-117">이 명령은 Contoso 라는 키 보관소에서 이전에 삭제 되었지만 제거 되지 않은 ' MyCert ' 라는 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2bef2-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="2bef2-118">이 명령은 삭제 날짜 등의 메타 데이터와 해당 인증서의 예정 된 제거 날짜 등을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bef2-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="2bef2-119">변수</span><span class="sxs-lookup"><span data-stu-id="2bef2-119">PARAMETERS</span></span>

### <span data-ttu-id="2bef2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bef2-120">-DefaultProfile</span></span>
<span data-ttu-id="2bef2-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2bef2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef2-122">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="2bef2-122">-IncludeVersions</span></span>
<span data-ttu-id="2bef2-123">이 작업이 모든 버전의 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2bef2-123">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByCertificateVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef2-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="2bef2-124">-InRemovedState</span></span>
<span data-ttu-id="2bef2-125">출력에 이전에 삭제 된 인증서를 포함할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bef2-125">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedCertificates
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef2-126">-이름</span><span class="sxs-lookup"><span data-stu-id="2bef2-126">-Name</span></span>
<span data-ttu-id="2bef2-127">가져올 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bef2-127">Specifies the name of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName, ByCertificateVersions
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedCertificates
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bef2-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2bef2-128">-VaultName</span></span>
<span data-ttu-id="2bef2-129">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bef2-129">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="2bef2-130">-버전</span><span class="sxs-lookup"><span data-stu-id="2bef2-130">-Version</span></span>
<span data-ttu-id="2bef2-131">인증서의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bef2-131">Specifies the version of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bef2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bef2-132">CommonParameters</span></span>
<span data-ttu-id="2bef2-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bef2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bef2-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bef2-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bef2-135">입력</span><span class="sxs-lookup"><span data-stu-id="2bef2-135">INPUTS</span></span>

### <span data-ttu-id="2bef2-136">않아야</span><span class="sxs-lookup"><span data-stu-id="2bef2-136">None</span></span>
<span data-ttu-id="2bef2-137">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2bef2-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2bef2-138">출력</span><span class="sxs-lookup"><span data-stu-id="2bef2-138">OUTPUTS</span></span>

### <span data-ttu-id="2bef2-139">CertificateIdentityItem의 ' 1 [Microsoft Azure.] 목록. List.</span><span class="sxs-lookup"><span data-stu-id="2bef2-139">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="2bef2-140">Microsoft. KeyVault. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2bef2-140">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="2bef2-141">상속자</span><span class="sxs-lookup"><span data-stu-id="2bef2-141">NOTES</span></span>

## <span data-ttu-id="2bef2-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2bef2-142">RELATED LINKS</span></span>

[<span data-ttu-id="2bef2-143">추가-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2bef2-143">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="2bef2-144">가져오기-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2bef2-144">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="2bef2-145">제거-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2bef2-145">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="2bef2-146">실행 취소-AzKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="2bef2-146">Undo-AzKeyVaultSecretCertificate</span></span>](./Undo-AzKeyVaultSecretCertificate.md)
