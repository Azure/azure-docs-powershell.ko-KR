---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 66c5e949cca8a6f53fdbac89e2745ac7697e14ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534955"
---
# <span data-ttu-id="622a3-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="622a3-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="622a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="622a3-102">SYNOPSIS</span></span>
<span data-ttu-id="622a3-103">키 자격 증명 모음에 대 한 인증서 발급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="622a3-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="622a3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="622a3-104">SYNTAX</span></span>

### <span data-ttu-id="622a3-105">ByVaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="622a3-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="622a3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="622a3-106">ByName</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="622a3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="622a3-107">DESCRIPTION</span></span>
<span data-ttu-id="622a3-108">**AzureKeyVaultCertificateIssuer** cmdlet은 지정 된 인증서 발급자 또는 Azure key vault의 키 자격 증명에 대 한 모든 인증서 발급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="622a3-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="622a3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="622a3-109">EXAMPLES</span></span>

### <span data-ttu-id="622a3-110">예제 1: 인증서 발급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="622a3-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="622a3-111">이 명령은 TestIssuer01 이라는 인증서 발급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="622a3-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="622a3-112">변수</span><span class="sxs-lookup"><span data-stu-id="622a3-112">PARAMETERS</span></span>

### <span data-ttu-id="622a3-113">-이름</span><span class="sxs-lookup"><span data-stu-id="622a3-113">-Name</span></span>
<span data-ttu-id="622a3-114">가져올 인증서 발급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="622a3-114">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="622a3-115">-VaultName</span><span class="sxs-lookup"><span data-stu-id="622a3-115">-VaultName</span></span>
<span data-ttu-id="622a3-116">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="622a3-116">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="622a3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="622a3-117">-DefaultProfile</span></span>
<span data-ttu-id="622a3-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="622a3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="622a3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="622a3-119">CommonParameters</span></span>
<span data-ttu-id="622a3-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="622a3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="622a3-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="622a3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="622a3-122">입력</span><span class="sxs-lookup"><span data-stu-id="622a3-122">INPUTS</span></span>

## <span data-ttu-id="622a3-123">출력</span><span class="sxs-lookup"><span data-stu-id="622a3-123">OUTPUTS</span></span>

### <span data-ttu-id="622a3-124"><를 나열 합니다. Keyvault>, CertificateIssuerIdentityItem,. KeyVault..</span><span class="sxs-lookup"><span data-stu-id="622a3-124">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="622a3-125">상속자</span><span class="sxs-lookup"><span data-stu-id="622a3-125">NOTES</span></span>

## <span data-ttu-id="622a3-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="622a3-126">RELATED LINKS</span></span>

[<span data-ttu-id="622a3-127">제거-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="622a3-127">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="622a3-128">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="622a3-128">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


