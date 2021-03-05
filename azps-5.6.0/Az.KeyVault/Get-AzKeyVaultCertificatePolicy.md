---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: cace261f300dc63b9568413fb8a709c323349531
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991139"
---
# <span data-ttu-id="57f60-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="57f60-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="57f60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57f60-102">SYNOPSIS</span></span>
<span data-ttu-id="57f60-103">키 자격 증명 모음에서 인증서에 대한 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="57f60-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="57f60-104">구문</span><span class="sxs-lookup"><span data-stu-id="57f60-104">SYNTAX</span></span>

### <span data-ttu-id="57f60-105">VaultAndCertName(기본값)</span><span class="sxs-lookup"><span data-stu-id="57f60-105">VaultAndCertName (Default)</span></span>
```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57f60-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="57f60-106">InputObject</span></span>
```
Get-AzKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57f60-107">설명</span><span class="sxs-lookup"><span data-stu-id="57f60-107">DESCRIPTION</span></span>
<span data-ttu-id="57f60-108">**Get-AzKeyVaultCertificatePolicy** cmdlet은 Azure Key Vault의 키 자격 증명 모음에서 인증서에 대한 정책을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="57f60-108">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="57f60-109">예제</span><span class="sxs-lookup"><span data-stu-id="57f60-109">EXAMPLES</span></span>

### <span data-ttu-id="57f60-110">예제 1: 인증서 정책 얻기</span><span class="sxs-lookup"><span data-stu-id="57f60-110">Example 1: Get a certificate policy</span></span>
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

<span data-ttu-id="57f60-111">이 명령은 ContosoKV01 키 자격 증명 모음에서 TestCert01 인증서에 대한 인증서 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="57f60-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="57f60-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="57f60-112">PARAMETERS</span></span>

### <span data-ttu-id="57f60-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57f60-113">-DefaultProfile</span></span>
<span data-ttu-id="57f60-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="57f60-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57f60-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57f60-115">-InputObject</span></span>
<span data-ttu-id="57f60-116">인증서 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="57f60-116">Certificate Object.</span></span>

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

### <span data-ttu-id="57f60-117">-Name</span><span class="sxs-lookup"><span data-stu-id="57f60-117">-Name</span></span>
<span data-ttu-id="57f60-118">인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="57f60-118">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="57f60-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="57f60-119">-VaultName</span></span>
<span data-ttu-id="57f60-120">키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="57f60-120">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="57f60-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57f60-121">CommonParameters</span></span>
<span data-ttu-id="57f60-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="57f60-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57f60-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57f60-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57f60-124">입력</span><span class="sxs-lookup"><span data-stu-id="57f60-124">INPUTS</span></span>

### <span data-ttu-id="57f60-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="57f60-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="57f60-126">출력</span><span class="sxs-lookup"><span data-stu-id="57f60-126">OUTPUTS</span></span>

### <span data-ttu-id="57f60-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="57f60-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="57f60-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="57f60-128">NOTES</span></span>

## <span data-ttu-id="57f60-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57f60-129">RELATED LINKS</span></span>

[<span data-ttu-id="57f60-130">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="57f60-130">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="57f60-131">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="57f60-131">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

