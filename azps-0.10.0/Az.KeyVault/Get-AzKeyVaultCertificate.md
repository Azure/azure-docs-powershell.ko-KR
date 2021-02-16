---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: babd3d8a42ddbd740c8189a41de76c78170ecae5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398821"
---
# <span data-ttu-id="e5a35-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e5a35-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="e5a35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5a35-102">SYNOPSIS</span></span>
<span data-ttu-id="e5a35-103">키 자격 증명 모음에서 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e5a35-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="e5a35-104">구문</span><span class="sxs-lookup"><span data-stu-id="e5a35-104">SYNTAX</span></span>

### <span data-ttu-id="e5a35-105">ByVaultName(기본값)</span><span class="sxs-lookup"><span data-stu-id="e5a35-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5a35-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="e5a35-106">ByCertificateName</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5a35-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="e5a35-107">ByCertificateVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5a35-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="e5a35-108">ByDeletedCertificates</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5a35-109">설명</span><span class="sxs-lookup"><span data-stu-id="e5a35-109">DESCRIPTION</span></span>
<span data-ttu-id="e5a35-110">**Get-AzKeyVaultCertificate** cmdlet은 Azure Key Vault의 키 자격 증명 모음에서 지정된 인증서 또는 인증서 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e5a35-110">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="e5a35-111">예제</span><span class="sxs-lookup"><span data-stu-id="e5a35-111">EXAMPLES</span></span>

### <span data-ttu-id="e5a35-112">예제 1: 인증서를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5a35-112">Example 1: Get a certificate</span></span>
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

<span data-ttu-id="e5a35-113">이 명령은 ContosoKV01이라는 키 자격 증명 모음에서 TestCert01이라는 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e5a35-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="e5a35-114">예제 2: 이 키 자격 증명 모음에 대해 삭제했지만 제거되지 않은 모든 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e5a35-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="e5a35-115">이 명령은 Contoso라는 키 자격 증명 모음에서 이전에 삭제했지만 제거되지 않은 모든 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e5a35-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="e5a35-116">예제 3: 이 키 자격 증명 모음에 대해 삭제했지만 제거되지 않은 인증서 MyCert를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e5a35-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="e5a35-117">이 명령은 Contoso라는 키 자격 증명 모음에서 이전에 삭제했지만 제거되지 않은 'MyCert'라는 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e5a35-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="e5a35-118">이 명령은 삭제 날짜 및 이 삭제된 인증서의 예약된 제거 날짜와 같은 메타데이터를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e5a35-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="e5a35-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5a35-119">PARAMETERS</span></span>

### <span data-ttu-id="e5a35-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5a35-120">-DefaultProfile</span></span>
<span data-ttu-id="e5a35-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e5a35-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5a35-122">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="e5a35-122">-IncludeVersions</span></span>
<span data-ttu-id="e5a35-123">이 작업이 모든 버전의 인증서를 얻게 됐습니다.</span><span class="sxs-lookup"><span data-stu-id="e5a35-123">Indicates that this operation gets all versions of the certificate.</span></span>

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

### <span data-ttu-id="e5a35-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="e5a35-124">-InRemovedState</span></span>
<span data-ttu-id="e5a35-125">출력에 이전에 삭제된 인증서를 포함할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e5a35-125">Specifies whether to include previously deleted certificates in the output</span></span>

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

### <span data-ttu-id="e5a35-126">-Name</span><span class="sxs-lookup"><span data-stu-id="e5a35-126">-Name</span></span>
<span data-ttu-id="e5a35-127">얻을 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e5a35-127">Specifies the name of the certificate to get.</span></span>

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

### <span data-ttu-id="e5a35-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e5a35-128">-VaultName</span></span>
<span data-ttu-id="e5a35-129">키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e5a35-129">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="e5a35-130">-Version</span><span class="sxs-lookup"><span data-stu-id="e5a35-130">-Version</span></span>
<span data-ttu-id="e5a35-131">인증서의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e5a35-131">Specifies the version of a certificate.</span></span>

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

### <span data-ttu-id="e5a35-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5a35-132">CommonParameters</span></span>
<span data-ttu-id="e5a35-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e5a35-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5a35-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e5a35-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5a35-135">입력</span><span class="sxs-lookup"><span data-stu-id="e5a35-135">INPUTS</span></span>

### <span data-ttu-id="e5a35-136">없음</span><span class="sxs-lookup"><span data-stu-id="e5a35-136">None</span></span>
<span data-ttu-id="e5a35-137">이 cmdlet은 입력을 허용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5a35-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e5a35-138">출력</span><span class="sxs-lookup"><span data-stu-id="e5a35-138">OUTPUTS</span></span>

### <span data-ttu-id="e5a35-139">System.Collections.Generic.List'1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="e5a35-139">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="e5a35-140">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e5a35-140">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="e5a35-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e5a35-141">NOTES</span></span>

## <span data-ttu-id="e5a35-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5a35-142">RELATED LINKS</span></span>

[<span data-ttu-id="e5a35-143">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e5a35-143">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="e5a35-144">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e5a35-144">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="e5a35-145">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e5a35-145">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

