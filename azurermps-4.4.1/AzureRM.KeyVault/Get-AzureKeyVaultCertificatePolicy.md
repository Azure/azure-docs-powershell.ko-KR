---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: a6b8b4f07d4ac589a0bb700e6303c384e38966fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711271"
---
# <span data-ttu-id="196de-101">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="196de-101">Get-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="196de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="196de-102">SYNOPSIS</span></span>
<span data-ttu-id="196de-103">키 자격 증명 모음의 인증서에 대 한 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="196de-103">Gets the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="196de-104">구문과</span><span class="sxs-lookup"><span data-stu-id="196de-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="196de-105">설명은</span><span class="sxs-lookup"><span data-stu-id="196de-105">DESCRIPTION</span></span>
<span data-ttu-id="196de-106">**AzureKeyVaultCertificatePolicy** Cmdlet은 Azure key vault의 키 보관소에서 인증서에 대 한 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="196de-106">The **Get-AzureKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="196de-107">예제의</span><span class="sxs-lookup"><span data-stu-id="196de-107">EXAMPLES</span></span>

### <span data-ttu-id="196de-108">예제 1: 인증서 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="196de-108">Example 1: Get a certificate policy</span></span>
```
PS C:\>Get-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"
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
RenewAtNumberOfDaysBeforeExpiry : 
RenewAtPercentageLifetime       : 80
EmailOnly                       : False
Enabled                         : True
Created                         : 2/8/2016 11:10:29 PM
Updated                         : 2/8/2016 11:10:29 PM
```

<span data-ttu-id="196de-109">이 명령은 ContosoKV01 키 자격 증명 모음의 TestCert01 certificate에 대 한 인증서 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="196de-109">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="196de-110">변수</span><span class="sxs-lookup"><span data-stu-id="196de-110">PARAMETERS</span></span>

### <span data-ttu-id="196de-111">-이름</span><span class="sxs-lookup"><span data-stu-id="196de-111">-Name</span></span>
<span data-ttu-id="196de-112">인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="196de-112">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="196de-113">-VaultName</span><span class="sxs-lookup"><span data-stu-id="196de-113">-VaultName</span></span>
<span data-ttu-id="196de-114">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="196de-114">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="196de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="196de-115">-DefaultProfile</span></span>
<span data-ttu-id="196de-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="196de-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="196de-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="196de-117">CommonParameters</span></span>
<span data-ttu-id="196de-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="196de-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="196de-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="196de-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="196de-120">입력</span><span class="sxs-lookup"><span data-stu-id="196de-120">INPUTS</span></span>

## <span data-ttu-id="196de-121">출력</span><span class="sxs-lookup"><span data-stu-id="196de-121">OUTPUTS</span></span>

### <span data-ttu-id="196de-122">Microsoft. KeyVault. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="196de-122">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="196de-123">상속자</span><span class="sxs-lookup"><span data-stu-id="196de-123">NOTES</span></span>

## <span data-ttu-id="196de-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="196de-124">RELATED LINKS</span></span>

[<span data-ttu-id="196de-125">새로운 AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="196de-125">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="196de-126">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="196de-126">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

