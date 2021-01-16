---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: d089cf44e14e70be8b377de310ab4a332ae2d1a1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367417"
---
# <span data-ttu-id="335aa-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="335aa-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="335aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="335aa-102">SYNOPSIS</span></span>
<span data-ttu-id="335aa-103">키 자격 증명 모음에 대한 인증서 발급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="335aa-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="335aa-104">구문</span><span class="sxs-lookup"><span data-stu-id="335aa-104">SYNTAX</span></span>

### <span data-ttu-id="335aa-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="335aa-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="335aa-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="335aa-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="335aa-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="335aa-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="335aa-108">설명</span><span class="sxs-lookup"><span data-stu-id="335aa-108">DESCRIPTION</span></span>
<span data-ttu-id="335aa-109">**Get-AzKeyVaultCertificateIssuer** cmdlet은 Azure Key Vault의 키 자격 증명 모음에 대해 지정된 인증서 발급자 또는 모든 인증서 발급서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="335aa-109">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="335aa-110">예제</span><span class="sxs-lookup"><span data-stu-id="335aa-110">EXAMPLES</span></span>

### <span data-ttu-id="335aa-111">예제 1: 인증서 발급자 얻기</span><span class="sxs-lookup"><span data-stu-id="335aa-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="335aa-112">이 명령은 TestIssuer01이라는 인증서 발급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="335aa-112">This command gets the certificate issuer named TestIssuer01.</span></span>

### <span data-ttu-id="335aa-113">예제 2: 필터링을 사용하여 인증서 발급자 나열</span><span class="sxs-lookup"><span data-stu-id="335aa-113">Example 2: List certificate issuers using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "test*"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer02
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="335aa-114">이 명령은 "test"로 시작하는 인증서 발급자입니다.</span><span class="sxs-lookup"><span data-stu-id="335aa-114">This command gets the certificate issuers that start with "test".</span></span>

## <span data-ttu-id="335aa-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="335aa-115">PARAMETERS</span></span>

### <span data-ttu-id="335aa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="335aa-116">-DefaultProfile</span></span>
<span data-ttu-id="335aa-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="335aa-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="335aa-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="335aa-118">-InputObject</span></span>
<span data-ttu-id="335aa-119">KeyVault 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="335aa-119">KeyVault object.</span></span>

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

### <span data-ttu-id="335aa-120">-Name</span><span class="sxs-lookup"><span data-stu-id="335aa-120">-Name</span></span>
<span data-ttu-id="335aa-121">얻을 인증서 발급자 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="335aa-121">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="335aa-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="335aa-122">-ResourceId</span></span>
<span data-ttu-id="335aa-123">KeyVault 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="335aa-123">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="335aa-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="335aa-124">-VaultName</span></span>
<span data-ttu-id="335aa-125">키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="335aa-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="335aa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="335aa-126">CommonParameters</span></span>
<span data-ttu-id="335aa-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="335aa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="335aa-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="335aa-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="335aa-129">입력</span><span class="sxs-lookup"><span data-stu-id="335aa-129">INPUTS</span></span>

### <span data-ttu-id="335aa-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="335aa-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="335aa-131">System.String</span><span class="sxs-lookup"><span data-stu-id="335aa-131">System.String</span></span>

## <span data-ttu-id="335aa-132">출력</span><span class="sxs-lookup"><span data-stu-id="335aa-132">OUTPUTS</span></span>

### <span data-ttu-id="335aa-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="335aa-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="335aa-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="335aa-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="335aa-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="335aa-135">NOTES</span></span>

## <span data-ttu-id="335aa-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="335aa-136">RELATED LINKS</span></span>

[<span data-ttu-id="335aa-137">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="335aa-137">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="335aa-138">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="335aa-138">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


