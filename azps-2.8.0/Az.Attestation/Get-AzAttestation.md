---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: cd6181ffb2bba8d71d8a0bf7cbe96d2f8038efc5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697884"
---
# <span data-ttu-id="4a6f8-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="4a6f8-101">Get-AzAttestation</span></span>

## <span data-ttu-id="4a6f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a6f8-102">SYNOPSIS</span></span>
<span data-ttu-id="4a6f8-103">증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-103">Gets an attestation.</span></span>

## <span data-ttu-id="4a6f8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4a6f8-104">SYNTAX</span></span>

### <span data-ttu-id="4a6f8-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4a6f8-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a6f8-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a6f8-106">ResourceGroupParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a6f8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4a6f8-107">DESCRIPTION</span></span>
<span data-ttu-id="4a6f8-108">Get-AzAttestation cmdlet은 구독의 증명에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-108">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="4a6f8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4a6f8-109">EXAMPLES</span></span>

### <span data-ttu-id="4a6f8-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4a6f8-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestation -Name example -ResourceGroupName rg1 
Id                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/rg1/providers/Microsoft.Attestation/attestationProviders/example
Name                : example
Type                : Microsoft.Attestation/attestationProviders
Status              : Ready
AttesUri            : https://example.us.attest.azure.net
ResoureGroupName    : rg1 
SubscriptionId      : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
```
<span data-ttu-id="4a6f8-111">리소스 그룹 "rg1"의 증명 "예제"를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-111">Get Attestation "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="4a6f8-112">변수</span><span class="sxs-lookup"><span data-stu-id="4a6f8-112">PARAMETERS</span></span>

### <span data-ttu-id="4a6f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a6f8-113">-DefaultProfile</span></span>
<span data-ttu-id="4a6f8-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6f8-115">-이름</span><span class="sxs-lookup"><span data-stu-id="4a6f8-115">-Name</span></span>
<span data-ttu-id="4a6f8-116">증명 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-116">Attestation Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6f8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a6f8-117">-ResourceGroupName</span></span>
<span data-ttu-id="4a6f8-118">쿼리 중인 증명에 연결 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-118">Specifies the name of the resource group associated with the attestation being queried.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6f8-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a6f8-119">-ResourceId</span></span>
<span data-ttu-id="4a6f8-120">쿼리 중인 증명에 연결 된 ResourceID의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-120">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a6f8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a6f8-121">CommonParameters</span></span>
<span data-ttu-id="4a6f8-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a6f8-123">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a6f8-124">입력</span><span class="sxs-lookup"><span data-stu-id="4a6f8-124">INPUTS</span></span>

### <span data-ttu-id="4a6f8-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4a6f8-125">System.String</span></span>

## <span data-ttu-id="4a6f8-126">출력</span><span class="sxs-lookup"><span data-stu-id="4a6f8-126">OUTPUTS</span></span>

### <span data-ttu-id="4a6f8-127">Microsoft. Azure. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="4a6f8-127">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="4a6f8-128">상속자</span><span class="sxs-lookup"><span data-stu-id="4a6f8-128">NOTES</span></span>

## <span data-ttu-id="4a6f8-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a6f8-129">RELATED LINKS</span></span>
