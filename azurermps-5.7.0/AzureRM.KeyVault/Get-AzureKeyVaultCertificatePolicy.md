---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 1317b35e957b46e6f39bfb0866e0429c01d35533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528942"
---
# <span data-ttu-id="050d0-101">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="050d0-101">Get-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="050d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="050d0-102">SYNOPSIS</span></span>
<span data-ttu-id="050d0-103">키 자격 증명 모음의 인증서에 대 한 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="050d0-103">Gets the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="050d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="050d0-104">SYNTAX</span></span>

### <span data-ttu-id="050d0-105">VaultAndCertName (기본값)</span><span class="sxs-lookup"><span data-stu-id="050d0-105">VaultAndCertName (Default)</span></span>
```
Get-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="050d0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="050d0-106">InputObject</span></span>
```
Get-AzureKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="050d0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="050d0-107">DESCRIPTION</span></span>
<span data-ttu-id="050d0-108">**AzureKeyVaultCertificatePolicy** Cmdlet은 Azure key vault의 키 보관소에서 인증서에 대 한 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="050d0-108">The **Get-AzureKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="050d0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="050d0-109">EXAMPLES</span></span>

### <span data-ttu-id="050d0-110">예제 1: 인증서 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="050d0-110">Example 1: Get a certificate policy</span></span>
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

<span data-ttu-id="050d0-111">이 명령은 ContosoKV01 키 자격 증명 모음의 TestCert01 certificate에 대 한 인증서 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="050d0-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="050d0-112">변수</span><span class="sxs-lookup"><span data-stu-id="050d0-112">PARAMETERS</span></span>

### <span data-ttu-id="050d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="050d0-113">-DefaultProfile</span></span>
<span data-ttu-id="050d0-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="050d0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="050d0-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="050d0-115">-InputObject</span></span>
<span data-ttu-id="050d0-116">인증서 개체.</span><span class="sxs-lookup"><span data-stu-id="050d0-116">Certificate Object.</span></span>

```yaml
Type: PSKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="050d0-117">-이름</span><span class="sxs-lookup"><span data-stu-id="050d0-117">-Name</span></span>
<span data-ttu-id="050d0-118">인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="050d0-118">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: VaultAndCertName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="050d0-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="050d0-119">-VaultName</span></span>
<span data-ttu-id="050d0-120">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="050d0-120">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: VaultAndCertName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="050d0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="050d0-121">CommonParameters</span></span>
<span data-ttu-id="050d0-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="050d0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="050d0-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="050d0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="050d0-124">입력</span><span class="sxs-lookup"><span data-stu-id="050d0-124">INPUTS</span></span>

### <span data-ttu-id="050d0-125">않아야</span><span class="sxs-lookup"><span data-stu-id="050d0-125">None</span></span>
<span data-ttu-id="050d0-126">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="050d0-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="050d0-127">출력</span><span class="sxs-lookup"><span data-stu-id="050d0-127">OUTPUTS</span></span>

### <span data-ttu-id="050d0-128">Microsoft. KeyVault. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="050d0-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="050d0-129">상속자</span><span class="sxs-lookup"><span data-stu-id="050d0-129">NOTES</span></span>

## <span data-ttu-id="050d0-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="050d0-130">RELATED LINKS</span></span>

[<span data-ttu-id="050d0-131">새로운 AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="050d0-131">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="050d0-132">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="050d0-132">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

