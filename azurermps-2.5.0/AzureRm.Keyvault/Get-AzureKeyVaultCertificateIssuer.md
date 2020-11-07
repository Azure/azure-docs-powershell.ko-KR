---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
ms.openlocfilehash: fcbb19936bb9924f95aa3a20fa026a9c8c723033
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881910"
---
# <span data-ttu-id="319f0-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="319f0-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="319f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="319f0-102">SYNOPSIS</span></span>
<span data-ttu-id="319f0-103">키 자격 증명 모음에 대 한 인증서 발급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="319f0-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="319f0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="319f0-104">SYNTAX</span></span>

### <span data-ttu-id="319f0-105">ByVaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="319f0-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="319f0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="319f0-106">ByName</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="319f0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="319f0-107">DESCRIPTION</span></span>
<span data-ttu-id="319f0-108">**AzureKeyVaultCertificateIssuer** cmdlet은 지정 된 인증서 발급자 또는 Azure key vault의 키 자격 증명에 대 한 모든 인증서 발급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="319f0-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="319f0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="319f0-109">EXAMPLES</span></span>

### <span data-ttu-id="319f0-110">예제 1: 인증서 발급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="319f0-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="319f0-111">이 명령은 TestIssuer01 이라는 인증서 발급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="319f0-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="319f0-112">변수</span><span class="sxs-lookup"><span data-stu-id="319f0-112">PARAMETERS</span></span>

### <span data-ttu-id="319f0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="319f0-113">-DefaultProfile</span></span>
<span data-ttu-id="319f0-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="319f0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="319f0-115">-이름</span><span class="sxs-lookup"><span data-stu-id="319f0-115">-Name</span></span>
<span data-ttu-id="319f0-116">가져올 인증서 발급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="319f0-116">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319f0-117">-VaultName</span><span class="sxs-lookup"><span data-stu-id="319f0-117">-VaultName</span></span>
<span data-ttu-id="319f0-118">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="319f0-118">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="319f0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="319f0-119">CommonParameters</span></span>
<span data-ttu-id="319f0-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="319f0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="319f0-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="319f0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="319f0-122">입력</span><span class="sxs-lookup"><span data-stu-id="319f0-122">INPUTS</span></span>

## <span data-ttu-id="319f0-123">출력</span><span class="sxs-lookup"><span data-stu-id="319f0-123">OUTPUTS</span></span>

### <span data-ttu-id="319f0-124"><를 나열 합니다. Keyvault>, CertificateIssuerIdentityItem,. KeyVault..</span><span class="sxs-lookup"><span data-stu-id="319f0-124">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="319f0-125">상속자</span><span class="sxs-lookup"><span data-stu-id="319f0-125">NOTES</span></span>

## <span data-ttu-id="319f0-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="319f0-126">RELATED LINKS</span></span>

[<span data-ttu-id="319f0-127">제거-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="319f0-127">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="319f0-128">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="319f0-128">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


