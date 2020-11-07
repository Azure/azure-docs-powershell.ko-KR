---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
ms.openlocfilehash: dd87a5b9abf6126fee71bbc308ec3a985c9da9de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711886"
---
# <span data-ttu-id="a95f4-101">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a95f4-101">Get-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="a95f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a95f4-102">SYNOPSIS</span></span>
<span data-ttu-id="a95f4-103">키 자격 증명 모음에서 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a95f4-103">Gets a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a95f4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a95f4-104">SYNTAX</span></span>

### <span data-ttu-id="a95f4-105">ByVaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="a95f4-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a95f4-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="a95f4-106">ByCertificateName</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a95f4-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="a95f4-107">ByCertificateVersions</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a95f4-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="a95f4-108">ByDeletedCertificates</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a95f4-109">설명은</span><span class="sxs-lookup"><span data-stu-id="a95f4-109">DESCRIPTION</span></span>
<span data-ttu-id="a95f4-110">**AzureKeyVaultCertificate** cmdlet은 지정 된 인증서 또는 Azure key vault의 키 자격 증명 모음에서 인증서의 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a95f4-110">The **Get-AzureKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="a95f4-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a95f4-111">EXAMPLES</span></span>

### <span data-ttu-id="a95f4-112">예제 1: 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="a95f4-112">Example 1: Get a certificate</span></span>
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

<span data-ttu-id="a95f4-113">이 명령은 ContosoKV01 이라는 키 보관소에서 TestCert01 라는 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a95f4-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="a95f4-114">예제 2: 삭제 했지만이 키 보관소에는 제거 되지 않은 모든 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a95f4-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="a95f4-115">이 명령은 Contoso 라는 키 보관소에서 이전에 삭제 했지만 제거 되지 않은 모든 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a95f4-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="a95f4-116">예제 3: 삭제 되었지만이 키 보관소에는 제거 되지 않은 인증서 MyCert 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a95f4-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="a95f4-117">이 명령은 Contoso 라는 키 보관소에서 이전에 삭제 되었지만 제거 되지 않은 ' MyCert ' 라는 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a95f4-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="a95f4-118">이 명령은 삭제 날짜 등의 메타 데이터와 해당 인증서의 예정 된 제거 날짜 등을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a95f4-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="a95f4-119">변수</span><span class="sxs-lookup"><span data-stu-id="a95f4-119">PARAMETERS</span></span>

### <span data-ttu-id="a95f4-120">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="a95f4-120">-IncludeVersions</span></span>
<span data-ttu-id="a95f4-121">이 작업이 모든 버전의 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a95f4-121">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByCertificateVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95f4-122">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="a95f4-122">-InRemovedState</span></span>
<span data-ttu-id="a95f4-123">이전에 삭제 된 인증서를 출력에 포함시킬지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a95f4-123">Specifies whether to include previously deleted certificates in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedCertificates
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95f4-124">-이름</span><span class="sxs-lookup"><span data-stu-id="a95f4-124">-Name</span></span>
<span data-ttu-id="a95f4-125">가져올 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a95f4-125">Specifies the name of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName, ByCertificateVersions
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedCertificates
Aliases: CertificateName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a95f4-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a95f4-126">-VaultName</span></span>
<span data-ttu-id="a95f4-127">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a95f4-127">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a95f4-128">-버전</span><span class="sxs-lookup"><span data-stu-id="a95f4-128">-Version</span></span>
<span data-ttu-id="a95f4-129">인증서의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a95f4-129">Specifies the version of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: CertificateVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a95f4-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a95f4-130">-DefaultProfile</span></span>
<span data-ttu-id="a95f4-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a95f4-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a95f4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a95f4-132">CommonParameters</span></span>
<span data-ttu-id="a95f4-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a95f4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a95f4-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a95f4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a95f4-135">입력</span><span class="sxs-lookup"><span data-stu-id="a95f4-135">INPUTS</span></span>

## <span data-ttu-id="a95f4-136">출력</span><span class="sxs-lookup"><span data-stu-id="a95f4-136">OUTPUTS</span></span>

### <span data-ttu-id="a95f4-137">CertificateIdentityItem의 ' 1 [Microsoft Azure.] 목록. List.</span><span class="sxs-lookup"><span data-stu-id="a95f4-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="a95f4-138">Microsoft. KeyVault. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a95f4-138">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="a95f4-139">상속자</span><span class="sxs-lookup"><span data-stu-id="a95f4-139">NOTES</span></span>

## <span data-ttu-id="a95f4-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a95f4-140">RELATED LINKS</span></span>

[<span data-ttu-id="a95f4-141">추가-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a95f4-141">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="a95f4-142">가져오기-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a95f4-142">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="a95f4-143">제거-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a95f4-143">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="a95f4-144">실행 취소-AzureKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="a95f4-144">Undo-AzureKeyVaultSecretCertificate</span></span>](./Undo-AzureKeyVaultSecretCertificate.md)
