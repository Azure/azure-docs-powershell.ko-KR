---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: a18222c40dc5c56bd2d67afb8d0df35b7aedc532
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042740"
---
# <span data-ttu-id="610d4-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="610d4-101">Get-AzAttestation</span></span>

## <span data-ttu-id="610d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="610d4-102">SYNOPSIS</span></span>
<span data-ttu-id="610d4-103">증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="610d4-103">Gets an attestation.</span></span>

## <span data-ttu-id="610d4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="610d4-104">SYNTAX</span></span>

### <span data-ttu-id="610d4-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="610d4-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="610d4-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="610d4-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="610d4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="610d4-107">DESCRIPTION</span></span>
<span data-ttu-id="610d4-108">Get-AzAttestation cmdlet은 구독의 증명에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="610d4-108">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="610d4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="610d4-109">EXAMPLES</span></span>

### <span data-ttu-id="610d4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="610d4-110">Example 1</span></span>
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

<span data-ttu-id="610d4-111">리소스 그룹 *psh-테스트-rg* 에서 증명 공급자 *pshtest* 를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="610d4-111">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

## <span data-ttu-id="610d4-112">변수</span><span class="sxs-lookup"><span data-stu-id="610d4-112">PARAMETERS</span></span>

### <span data-ttu-id="610d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="610d4-113">-DefaultProfile</span></span>
<span data-ttu-id="610d4-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="610d4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="610d4-115">-이름</span><span class="sxs-lookup"><span data-stu-id="610d4-115">-Name</span></span>
<span data-ttu-id="610d4-116">증명 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="610d4-116">Attestation Name.</span></span>

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

### <span data-ttu-id="610d4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="610d4-117">-ResourceGroupName</span></span>
<span data-ttu-id="610d4-118">쿼리 중인 증명에 연결 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="610d4-118">Specifies the name of the resource group associated with the attestation being queried.</span></span>

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

### <span data-ttu-id="610d4-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="610d4-119">-ResourceId</span></span>
<span data-ttu-id="610d4-120">쿼리 중인 증명에 연결 된 ResourceID의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="610d4-120">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

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

### <span data-ttu-id="610d4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="610d4-121">CommonParameters</span></span>
<span data-ttu-id="610d4-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="610d4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="610d4-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="610d4-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="610d4-124">입력</span><span class="sxs-lookup"><span data-stu-id="610d4-124">INPUTS</span></span>

### <span data-ttu-id="610d4-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="610d4-125">System.String</span></span>

## <span data-ttu-id="610d4-126">출력</span><span class="sxs-lookup"><span data-stu-id="610d4-126">OUTPUTS</span></span>

### <span data-ttu-id="610d4-127">Microsoft. Azure. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="610d4-127">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="610d4-128">상속자</span><span class="sxs-lookup"><span data-stu-id="610d4-128">NOTES</span></span>

## <span data-ttu-id="610d4-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="610d4-129">RELATED LINKS</span></span>
