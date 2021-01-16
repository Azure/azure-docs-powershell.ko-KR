---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: d6e2225cc7441d4c370d990aa45c9b2c2bb40457
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367382"
---
# <span data-ttu-id="3beed-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3beed-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="3beed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3beed-102">SYNOPSIS</span></span>
<span data-ttu-id="3beed-103">키 자격 증명 모음에서 인증서에 대한 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3beed-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="3beed-104">구문</span><span class="sxs-lookup"><span data-stu-id="3beed-104">SYNTAX</span></span>

### <span data-ttu-id="3beed-105">VaultAndCertName(기본값)</span><span class="sxs-lookup"><span data-stu-id="3beed-105">VaultAndCertName (Default)</span></span>
```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3beed-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3beed-106">InputObject</span></span>
```
Get-AzKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3beed-107">설명</span><span class="sxs-lookup"><span data-stu-id="3beed-107">DESCRIPTION</span></span>
<span data-ttu-id="3beed-108">**Get-AzKeyVaultCertificatePolicy** cmdlet은 Azure Key Vault의 키 자격 증명 모음에서 인증서에 대한 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3beed-108">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="3beed-109">예제</span><span class="sxs-lookup"><span data-stu-id="3beed-109">EXAMPLES</span></span>

### <span data-ttu-id="3beed-110">예제 1: 인증서 정책 얻기</span><span class="sxs-lookup"><span data-stu-id="3beed-110">Example 1: Get a certificate policy</span></span>
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

<span data-ttu-id="3beed-111">이 명령은 ContosoKV01 키 자격 증명 모음에서 TestCert01 인증서에 대한 인증서 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3beed-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="3beed-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3beed-112">PARAMETERS</span></span>

### <span data-ttu-id="3beed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3beed-113">-DefaultProfile</span></span>
<span data-ttu-id="3beed-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3beed-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3beed-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3beed-115">-InputObject</span></span>
<span data-ttu-id="3beed-116">인증서 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3beed-116">Certificate Object.</span></span>

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

### <span data-ttu-id="3beed-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3beed-117">-Name</span></span>
<span data-ttu-id="3beed-118">인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3beed-118">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="3beed-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3beed-119">-VaultName</span></span>
<span data-ttu-id="3beed-120">키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3beed-120">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="3beed-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3beed-121">CommonParameters</span></span>
<span data-ttu-id="3beed-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3beed-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3beed-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3beed-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3beed-124">입력</span><span class="sxs-lookup"><span data-stu-id="3beed-124">INPUTS</span></span>

### <span data-ttu-id="3beed-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="3beed-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="3beed-126">출력</span><span class="sxs-lookup"><span data-stu-id="3beed-126">OUTPUTS</span></span>

### <span data-ttu-id="3beed-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3beed-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="3beed-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3beed-128">NOTES</span></span>

## <span data-ttu-id="3beed-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3beed-129">RELATED LINKS</span></span>

[<span data-ttu-id="3beed-130">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3beed-130">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="3beed-131">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3beed-131">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

