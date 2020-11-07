---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: ce21b116ceb41bfdfb26008dd44c914f3198ab39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697883"
---
# <span data-ttu-id="46672-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="46672-101">New-AzAttestation</span></span>

## <span data-ttu-id="46672-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46672-102">SYNOPSIS</span></span>
<span data-ttu-id="46672-103">증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="46672-103">Creates an attestation</span></span>

## <span data-ttu-id="46672-104">구문과</span><span class="sxs-lookup"><span data-stu-id="46672-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> [-AttestationPolicy <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46672-105">설명은</span><span class="sxs-lookup"><span data-stu-id="46672-105">DESCRIPTION</span></span>
<span data-ttu-id="46672-106">New-AzAttestation cmdlet은 지정 된 리소스 그룹에 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="46672-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="46672-107">예제의</span><span class="sxs-lookup"><span data-stu-id="46672-107">EXAMPLES</span></span>

### <span data-ttu-id="46672-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="46672-108">Example 1</span></span>
```powershell
PS C:\> New-AzAttestation -Name example -ResourceGroupName rg1 
Id                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/rg1/providers/Microsoft.Attestation/attestationProviders/example
Name                : example
Type                : Microsoft.Attestation/attestationProviders
Status              : Ready
AttesUri            : https://example.us.attest.azure.net
ResoureGroupName    : rg1 
SubscriptionId      : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
```

<span data-ttu-id="46672-109">현재 구독, 리소스 그룹 "rg1"에서 새 증명 "예제"를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="46672-109">Create a new Attestation "example" in current Subscription, Resource Group "rg1"</span></span>

## <span data-ttu-id="46672-110">변수</span><span class="sxs-lookup"><span data-stu-id="46672-110">PARAMETERS</span></span>

### <span data-ttu-id="46672-111">-AttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="46672-111">-AttestationPolicy</span></span>
<span data-ttu-id="46672-112">증명을 만들 증명 정책을 통과 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46672-112">Specifies the attestation policy passed in which to create the attestation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46672-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46672-113">-DefaultProfile</span></span>
<span data-ttu-id="46672-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="46672-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46672-115">-이름</span><span class="sxs-lookup"><span data-stu-id="46672-115">-Name</span></span>
<span data-ttu-id="46672-116">만들 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46672-116">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="46672-117">이름은 문자, 숫자 또는 하이픈을 임의로 조합 하 여 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46672-117">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="46672-118">이름은 문자 또는 숫자로 시작 하 고 끝나야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46672-118">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="46672-119">이름은 범용으로 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46672-119">The name must be universally unique.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46672-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46672-120">-ResourceGroupName</span></span>
<span data-ttu-id="46672-121">증명을 만들 기존 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46672-121">Specifies the name of an existing resource group in which to create the attestation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46672-122">-확인</span><span class="sxs-lookup"><span data-stu-id="46672-122">-Confirm</span></span>
<span data-ttu-id="46672-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="46672-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46672-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46672-124">-WhatIf</span></span>
<span data-ttu-id="46672-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="46672-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46672-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46672-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46672-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46672-127">CommonParameters</span></span>
<span data-ttu-id="46672-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="46672-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46672-129">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="46672-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46672-130">입력</span><span class="sxs-lookup"><span data-stu-id="46672-130">INPUTS</span></span>

### <span data-ttu-id="46672-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="46672-131">System.String</span></span>

## <span data-ttu-id="46672-132">출력</span><span class="sxs-lookup"><span data-stu-id="46672-132">OUTPUTS</span></span>

### <span data-ttu-id="46672-133">Microsoft. Azure. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="46672-133">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="46672-134">상속자</span><span class="sxs-lookup"><span data-stu-id="46672-134">NOTES</span></span>

## <span data-ttu-id="46672-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46672-135">RELATED LINKS</span></span>
