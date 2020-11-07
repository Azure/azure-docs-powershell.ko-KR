---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 83e81e479807c3eada25456d53521dfcecd81f40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703852"
---
# <span data-ttu-id="204f5-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="204f5-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="204f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="204f5-102">SYNOPSIS</span></span>
<span data-ttu-id="204f5-103">키 자격 증명 모음에 대 한 인증서 발급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="204f5-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="204f5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="204f5-104">SYNTAX</span></span>

### <span data-ttu-id="204f5-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="204f5-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="204f5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="204f5-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="204f5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="204f5-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="204f5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="204f5-108">DESCRIPTION</span></span>
<span data-ttu-id="204f5-109">**AzureKeyVaultCertificateIssuer** cmdlet은 지정 된 인증서 발급자 또는 Azure key vault의 키 자격 증명에 대 한 모든 인증서 발급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="204f5-109">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="204f5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="204f5-110">EXAMPLES</span></span>

### <span data-ttu-id="204f5-111">예제 1: 인증서 발급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="204f5-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="204f5-112">이 명령은 TestIssuer01 이라는 인증서 발급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="204f5-112">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="204f5-113">변수</span><span class="sxs-lookup"><span data-stu-id="204f5-113">PARAMETERS</span></span>

### <span data-ttu-id="204f5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="204f5-114">-DefaultProfile</span></span>
<span data-ttu-id="204f5-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="204f5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="204f5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="204f5-116">-InputObject</span></span>
<span data-ttu-id="204f5-117">KeyVault 개체.</span><span class="sxs-lookup"><span data-stu-id="204f5-117">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="204f5-118">-이름</span><span class="sxs-lookup"><span data-stu-id="204f5-118">-Name</span></span>
<span data-ttu-id="204f5-119">가져올 인증서 발급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="204f5-119">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="204f5-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="204f5-120">-ResourceId</span></span>
<span data-ttu-id="204f5-121">KeyVault 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="204f5-121">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="204f5-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="204f5-122">-VaultName</span></span>
<span data-ttu-id="204f5-123">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="204f5-123">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="204f5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="204f5-124">CommonParameters</span></span>
<span data-ttu-id="204f5-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="204f5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="204f5-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="204f5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="204f5-127">입력</span><span class="sxs-lookup"><span data-stu-id="204f5-127">INPUTS</span></span>

### <span data-ttu-id="204f5-128">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="204f5-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="204f5-129">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="204f5-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="204f5-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="204f5-130">System.String</span></span>

## <span data-ttu-id="204f5-131">출력</span><span class="sxs-lookup"><span data-stu-id="204f5-131">OUTPUTS</span></span>

### <span data-ttu-id="204f5-132">Microsoft. KeyVault. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="204f5-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="204f5-133">Microsoft. KeyVault. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="204f5-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="204f5-134">상속자</span><span class="sxs-lookup"><span data-stu-id="204f5-134">NOTES</span></span>

## <span data-ttu-id="204f5-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="204f5-135">RELATED LINKS</span></span>

[<span data-ttu-id="204f5-136">제거-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="204f5-136">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="204f5-137">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="204f5-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


