---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: 650ac7c478f1c27ca3ba925c4d767f02c79fa781
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216141"
---
# <span data-ttu-id="31f03-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="31f03-101">Get-AzAttestation</span></span>

## <span data-ttu-id="31f03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31f03-102">SYNOPSIS</span></span>
<span data-ttu-id="31f03-103">증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31f03-103">Gets an attestation.</span></span>

## <span data-ttu-id="31f03-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31f03-104">SYNTAX</span></span>

### <span data-ttu-id="31f03-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="31f03-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31f03-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31f03-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31f03-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="31f03-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestation [[-Location] <String>] [-DefaultProvider] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31f03-108">설명은</span><span class="sxs-lookup"><span data-stu-id="31f03-108">DESCRIPTION</span></span>
<span data-ttu-id="31f03-109">Get-AzAttestation cmdlet은 구독의 증명에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31f03-109">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="31f03-110">예제의</span><span class="sxs-lookup"><span data-stu-id="31f03-110">EXAMPLES</span></span>

### <span data-ttu-id="31f03-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="31f03-111">Example 1</span></span>
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

<span data-ttu-id="31f03-112">리소스 그룹 *psh-테스트-rg* 에서 증명 공급자 *pshtest* 를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31f03-112">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

### <span data-ttu-id="31f03-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="31f03-113">Example 2</span></span>
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

<span data-ttu-id="31f03-114">모든 사용 가능한 증명 기본 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="31f03-114">Get all available Attestation Default Providers</span></span>

### <span data-ttu-id="31f03-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="31f03-115">Example 3</span></span>
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

<span data-ttu-id="31f03-116">지역/ *미국 2* 에서 증명 기본 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="31f03-116">Get Attestation Default Provider from Location *East US 2*</span></span>

## <span data-ttu-id="31f03-117">변수</span><span class="sxs-lookup"><span data-stu-id="31f03-117">PARAMETERS</span></span>

### <span data-ttu-id="31f03-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31f03-118">-DefaultProfile</span></span>
<span data-ttu-id="31f03-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31f03-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31f03-120">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="31f03-120">-DefaultProvider</span></span>
<span data-ttu-id="31f03-121">기본 증명 공급자에 대 한 요청 임을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31f03-121">Specifies this is the request to a default attestation provider.</span></span>

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

### <span data-ttu-id="31f03-122">-위치</span><span class="sxs-lookup"><span data-stu-id="31f03-122">-Location</span></span>
<span data-ttu-id="31f03-123">기본 증명 공급자의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31f03-123">Specifies the Location of the default attestation provider.</span></span>

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

### <span data-ttu-id="31f03-124">-이름</span><span class="sxs-lookup"><span data-stu-id="31f03-124">-Name</span></span>
<span data-ttu-id="31f03-125">증명 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31f03-125">Attestation Name.</span></span>

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

### <span data-ttu-id="31f03-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31f03-126">-ResourceGroupName</span></span>
<span data-ttu-id="31f03-127">쿼리 중인 증명에 연결 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31f03-127">Specifies the name of the resource group associated with the attestation being queried.</span></span>

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

### <span data-ttu-id="31f03-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31f03-128">-ResourceId</span></span>
<span data-ttu-id="31f03-129">쿼리 중인 증명에 연결 된 ResourceID의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31f03-129">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

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

### <span data-ttu-id="31f03-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f03-130">CommonParameters</span></span>
<span data-ttu-id="31f03-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31f03-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f03-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="31f03-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f03-133">입력</span><span class="sxs-lookup"><span data-stu-id="31f03-133">INPUTS</span></span>

### <span data-ttu-id="31f03-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="31f03-134">System.String</span></span>

## <span data-ttu-id="31f03-135">출력</span><span class="sxs-lookup"><span data-stu-id="31f03-135">OUTPUTS</span></span>

### <span data-ttu-id="31f03-136">Microsoft. Azure. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="31f03-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="31f03-137">상속자</span><span class="sxs-lookup"><span data-stu-id="31f03-137">NOTES</span></span>

## <span data-ttu-id="31f03-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31f03-138">RELATED LINKS</span></span>
