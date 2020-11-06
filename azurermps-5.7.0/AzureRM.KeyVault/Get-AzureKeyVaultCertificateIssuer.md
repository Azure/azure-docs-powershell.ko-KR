---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: f19fa119bf307724fb318e0a1d9a390190523bd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528948"
---
# <span data-ttu-id="c93f8-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="c93f8-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="c93f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c93f8-102">SYNOPSIS</span></span>
<span data-ttu-id="c93f8-103">키 자격 증명 모음에 대 한 인증서 발급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c93f8-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c93f8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c93f8-104">SYNTAX</span></span>

### <span data-ttu-id="c93f8-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c93f8-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c93f8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c93f8-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c93f8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c93f8-107">DESCRIPTION</span></span>
<span data-ttu-id="c93f8-108">**AzureKeyVaultCertificateIssuer** cmdlet은 지정 된 인증서 발급자 또는 Azure key vault의 키 자격 증명에 대 한 모든 인증서 발급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c93f8-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="c93f8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c93f8-109">EXAMPLES</span></span>

### <span data-ttu-id="c93f8-110">예제 1: 인증서 발급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="c93f8-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="c93f8-111">이 명령은 TestIssuer01 이라는 인증서 발급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c93f8-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="c93f8-112">변수</span><span class="sxs-lookup"><span data-stu-id="c93f8-112">PARAMETERS</span></span>

### <span data-ttu-id="c93f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c93f8-113">-DefaultProfile</span></span>
<span data-ttu-id="c93f8-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c93f8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c93f8-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c93f8-115">-InputObject</span></span>
<span data-ttu-id="c93f8-116">KeyVault 개체.</span><span class="sxs-lookup"><span data-stu-id="c93f8-116">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c93f8-117">-이름</span><span class="sxs-lookup"><span data-stu-id="c93f8-117">-Name</span></span>
<span data-ttu-id="c93f8-118">가져올 인증서 발급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c93f8-118">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c93f8-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c93f8-119">-VaultName</span></span>
<span data-ttu-id="c93f8-120">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c93f8-120">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c93f8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c93f8-121">CommonParameters</span></span>
<span data-ttu-id="c93f8-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c93f8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c93f8-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c93f8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c93f8-124">입력</span><span class="sxs-lookup"><span data-stu-id="c93f8-124">INPUTS</span></span>

### <span data-ttu-id="c93f8-125">않아야</span><span class="sxs-lookup"><span data-stu-id="c93f8-125">None</span></span>
<span data-ttu-id="c93f8-126">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c93f8-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c93f8-127">출력</span><span class="sxs-lookup"><span data-stu-id="c93f8-127">OUTPUTS</span></span>

### <span data-ttu-id="c93f8-128"><를 나열 합니다. Keyvault>, PSKeyVaultCertificateIssuerIdentityItem,. KeyVault..</span><span class="sxs-lookup"><span data-stu-id="c93f8-128">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="c93f8-129">상속자</span><span class="sxs-lookup"><span data-stu-id="c93f8-129">NOTES</span></span>

## <span data-ttu-id="c93f8-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c93f8-130">RELATED LINKS</span></span>

[<span data-ttu-id="c93f8-131">제거-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="c93f8-131">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="c93f8-132">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="c93f8-132">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


