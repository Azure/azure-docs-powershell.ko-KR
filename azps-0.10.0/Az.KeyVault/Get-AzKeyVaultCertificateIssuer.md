---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: b9188e1bb4d5de4896bf0ca3b2844c7718593ca2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875840"
---
# <span data-ttu-id="1b955-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="1b955-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="1b955-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b955-102">SYNOPSIS</span></span>
<span data-ttu-id="1b955-103">키 자격 증명 모음에 대 한 인증서 발급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1b955-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="1b955-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1b955-104">SYNTAX</span></span>

### <span data-ttu-id="1b955-105">ByVaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="1b955-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b955-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1b955-106">ByName</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b955-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1b955-107">DESCRIPTION</span></span>
<span data-ttu-id="1b955-108">**AzKeyVaultCertificateIssuer** cmdlet은 지정 된 인증서 발급자 또는 Azure key vault의 키 자격 증명에 대 한 모든 인증서 발급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1b955-108">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="1b955-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1b955-109">EXAMPLES</span></span>

### <span data-ttu-id="1b955-110">예제 1: 인증서 발급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="1b955-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="1b955-111">이 명령은 TestIssuer01 이라는 인증서 발급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1b955-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="1b955-112">변수</span><span class="sxs-lookup"><span data-stu-id="1b955-112">PARAMETERS</span></span>

### <span data-ttu-id="1b955-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b955-113">-DefaultProfile</span></span>
<span data-ttu-id="1b955-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1b955-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b955-115">-이름</span><span class="sxs-lookup"><span data-stu-id="1b955-115">-Name</span></span>
<span data-ttu-id="1b955-116">가져올 인증서 발급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b955-116">Specifies the name of the certificate issuer to get.</span></span>

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

### <span data-ttu-id="1b955-117">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1b955-117">-VaultName</span></span>
<span data-ttu-id="1b955-118">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b955-118">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="1b955-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b955-119">CommonParameters</span></span>
<span data-ttu-id="1b955-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b955-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b955-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b955-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b955-122">입력</span><span class="sxs-lookup"><span data-stu-id="1b955-122">INPUTS</span></span>

### <span data-ttu-id="1b955-123">않아야</span><span class="sxs-lookup"><span data-stu-id="1b955-123">None</span></span>
<span data-ttu-id="1b955-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b955-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1b955-125">출력</span><span class="sxs-lookup"><span data-stu-id="1b955-125">OUTPUTS</span></span>

### <span data-ttu-id="1b955-126"><를 나열 합니다. Keyvault>, CertificateIssuerIdentityItem,. KeyVault..</span><span class="sxs-lookup"><span data-stu-id="1b955-126">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="1b955-127">상속자</span><span class="sxs-lookup"><span data-stu-id="1b955-127">NOTES</span></span>

## <span data-ttu-id="1b955-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1b955-128">RELATED LINKS</span></span>

[<span data-ttu-id="1b955-129">제거-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="1b955-129">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="1b955-130">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="1b955-130">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


