---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: 650ac7c478f1c27ca3ba925c4d767f02c79fa781
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199689"
---
# <span data-ttu-id="8b8a7-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="8b8a7-101">Get-AzAttestation</span></span>

## <span data-ttu-id="8b8a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b8a7-102">SYNOPSIS</span></span>
<span data-ttu-id="8b8a7-103">Attestation을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-103">Gets an attestation.</span></span>

## <span data-ttu-id="8b8a7-104">구문</span><span class="sxs-lookup"><span data-stu-id="8b8a7-104">SYNTAX</span></span>

### <span data-ttu-id="8b8a7-105">NameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="8b8a7-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b8a7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b8a7-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b8a7-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b8a7-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestation [[-Location] <String>] [-DefaultProvider] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b8a7-108">설명</span><span class="sxs-lookup"><span data-stu-id="8b8a7-108">DESCRIPTION</span></span>
<span data-ttu-id="8b8a7-109">Get-AzAttestation cmdlet은 구독의 등록에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-109">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="8b8a7-110">예제</span><span class="sxs-lookup"><span data-stu-id="8b8a7-110">EXAMPLES</span></span>

### <span data-ttu-id="8b8a7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8b8a7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestation -Name pshtest -ResourceGroupName psh-test-rg                                                                                                                                                                                                                                                       
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest
Status            : Ready
TrustModel        : AAD
AttestUri         : https://pshtest.us.attest.azure.net
Tags              : {Production, Example}
TagsTable         :
                    Name        Value
                    ==========  =====
                    Production  False
                    Example     True
```

<span data-ttu-id="8b8a7-112">리소스 그룹 *psh-test-rg에서* Attestation Provider *pshtest를* 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-112">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

### <span data-ttu-id="8b8a7-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="8b8a7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAttestation -DefaultProvider
Id                : /providers/Microsoft.Attestation/attestationProviders/sharedeus2
Location          : East US 2
ResourceGroupName :
Name              : sharedeus2
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedeus2.eus2.attest.azure.net
Tags              :
TagsTable         :

Id                : /providers/Microsoft.Attestation/attestationProviders/sharedcus
Location          : Central US
ResourceGroupName :
Name              : sharedcus
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedcus.cus.attest.azure.net
Tags              :
TagsTable         :

Id                : /providers/Microsoft.Attestation/attestationProviders/shareduks
Location          : UK South
ResourceGroupName :
Name              : shareduks
Status            : Ready
TrustModel        : AAD
AttestUri         : https://shareduks.uks.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="8b8a7-114">사용 가능한 모든 사용 가능한 기본 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-114">Get all available Attestation Default Providers</span></span>

### <span data-ttu-id="8b8a7-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="8b8a7-115">Example 3</span></span>
```powershell
PS C:\> Get-AzAttestation -DefaultProvider -Location "East US 2"
Id                : /providers/Microsoft.Attestation/attestationProviders/sharedeus2
Location          : East US 2
ResourceGroupName :
Name              : sharedeus2
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedeus2.eus2.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="8b8a7-116">미국 동부 2 위치에서 Attestation 기본 *공급자를 얻습니다.*</span><span class="sxs-lookup"><span data-stu-id="8b8a7-116">Get Attestation Default Provider from Location *East US 2*</span></span>

## <span data-ttu-id="8b8a7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b8a7-117">PARAMETERS</span></span>

### <span data-ttu-id="8b8a7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b8a7-118">-DefaultProfile</span></span>
<span data-ttu-id="8b8a7-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b8a7-120">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="8b8a7-120">-DefaultProvider</span></span>
<span data-ttu-id="8b8a7-121">기본 등록 공급자에 대한 요청으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-121">Specifies this is the request to a default attestation provider.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b8a7-122">-Location</span><span class="sxs-lookup"><span data-stu-id="8b8a7-122">-Location</span></span>
<span data-ttu-id="8b8a7-123">기본 등록 공급자의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-123">Specifies the Location of the default attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b8a7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8b8a7-124">-Name</span></span>
<span data-ttu-id="8b8a7-125">Attestation Name.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-125">Attestation Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b8a7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b8a7-126">-ResourceGroupName</span></span>
<span data-ttu-id="8b8a7-127">Queriation과 연결된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-127">Specifies the name of the resource group associated with the attestation being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b8a7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b8a7-128">-ResourceId</span></span>
<span data-ttu-id="8b8a7-129">Queriation과 연결된 ResourceID의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-129">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b8a7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b8a7-130">CommonParameters</span></span>
<span data-ttu-id="8b8a7-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b8a7-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8b8a7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b8a7-133">입력</span><span class="sxs-lookup"><span data-stu-id="8b8a7-133">INPUTS</span></span>

### <span data-ttu-id="8b8a7-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8b8a7-134">System.String</span></span>

## <span data-ttu-id="8b8a7-135">출력</span><span class="sxs-lookup"><span data-stu-id="8b8a7-135">OUTPUTS</span></span>

### <span data-ttu-id="8b8a7-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="8b8a7-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="8b8a7-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8b8a7-137">NOTES</span></span>

## <span data-ttu-id="8b8a7-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b8a7-138">RELATED LINKS</span></span>
