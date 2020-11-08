---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: d6e2225cc7441d4c370d990aa45c9b2c2bb40457
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034154"
---
# <span data-ttu-id="c2686-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c2686-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="c2686-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2686-102">SYNOPSIS</span></span>
<span data-ttu-id="c2686-103">키 자격 증명 모음의 인증서에 대 한 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c2686-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="c2686-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c2686-104">SYNTAX</span></span>

### <span data-ttu-id="c2686-105">VaultAndCertName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c2686-105">VaultAndCertName (Default)</span></span>
```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2686-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c2686-106">InputObject</span></span>
```
Get-AzKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2686-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c2686-107">DESCRIPTION</span></span>
<span data-ttu-id="c2686-108">**AzKeyVaultCertificatePolicy** Cmdlet은 Azure key vault의 키 보관소에서 인증서에 대 한 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c2686-108">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="c2686-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c2686-109">EXAMPLES</span></span>

### <span data-ttu-id="c2686-110">예제 1: 인증서 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="c2686-110">Example 1: Get a certificate policy</span></span>
```powershell
PS C:\ >Get-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"

SecretContentType               : application/x-pkcs12
Kty                             : RSA
KeySize                         : 2048
Exportable                      : True
ReuseKeyOnRenewal               : True
SubjectName                     : CN=contoso.com
DnsNames                        : 
Ekus                            : {1.3.6.1.5.5.7.3.1, 1.3.6.1.5.5.7.3.2}
ValidityInMonths                : 6
IssuerName                      : Self
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry : 
RenewAtPercentageLifetime       : 80
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
Enabled                         : True
Created                         : 2/8/2016 11:10:29 PM
Updated                         : 2/8/2016 11:10:29 PM
```

<span data-ttu-id="c2686-111">이 명령은 ContosoKV01 키 자격 증명 모음의 TestCert01 certificate에 대 한 인증서 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c2686-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="c2686-112">변수</span><span class="sxs-lookup"><span data-stu-id="c2686-112">PARAMETERS</span></span>

### <span data-ttu-id="c2686-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2686-113">-DefaultProfile</span></span>
<span data-ttu-id="c2686-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c2686-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2686-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2686-115">-InputObject</span></span>
<span data-ttu-id="c2686-116">인증서 개체.</span><span class="sxs-lookup"><span data-stu-id="c2686-116">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2686-117">-이름</span><span class="sxs-lookup"><span data-stu-id="c2686-117">-Name</span></span>
<span data-ttu-id="c2686-118">인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2686-118">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultAndCertName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2686-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c2686-119">-VaultName</span></span>
<span data-ttu-id="c2686-120">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2686-120">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultAndCertName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2686-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2686-121">CommonParameters</span></span>
<span data-ttu-id="c2686-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2686-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2686-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2686-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2686-124">입력</span><span class="sxs-lookup"><span data-stu-id="c2686-124">INPUTS</span></span>

### <span data-ttu-id="c2686-125">Microsoft. KeyVault. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c2686-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="c2686-126">출력</span><span class="sxs-lookup"><span data-stu-id="c2686-126">OUTPUTS</span></span>

### <span data-ttu-id="c2686-127">Microsoft. KeyVault. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c2686-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="c2686-128">상속자</span><span class="sxs-lookup"><span data-stu-id="c2686-128">NOTES</span></span>

## <span data-ttu-id="c2686-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2686-129">RELATED LINKS</span></span>

[<span data-ttu-id="c2686-130">새로운 AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c2686-130">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="c2686-131">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c2686-131">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

