---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: 689336bb7fbb7ef59be96a5bd6bcbfe49ddb64c0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495905"
---
# <span data-ttu-id="06ff8-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="06ff8-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="06ff8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="06ff8-103">가용성 집합을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="06ff8-103">Updates an availability set.</span></span>

## <span data-ttu-id="06ff8-104">구문</span><span class="sxs-lookup"><span data-stu-id="06ff8-104">SYNTAX</span></span>

```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06ff8-105">설명</span><span class="sxs-lookup"><span data-stu-id="06ff8-105">DESCRIPTION</span></span>
<span data-ttu-id="06ff8-106">**Update-AzAvailabilitySet** cmdlet은 가용성 집합을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="06ff8-106">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="06ff8-107">예제</span><span class="sxs-lookup"><span data-stu-id="06ff8-107">EXAMPLES</span></span>

### <span data-ttu-id="06ff8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="06ff8-108">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="06ff8-109">이 명령은 'ResourceGroup01'이라는 리소스 그룹의 'AvSet01'이라는 가용성 집합을 관리되는 가용성 집합으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="06ff8-109">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="06ff8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06ff8-110">PARAMETERS</span></span>

### <span data-ttu-id="06ff8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06ff8-111">-AsJob</span></span>
<span data-ttu-id="06ff8-112">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="06ff8-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06ff8-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="06ff8-113">-AvailabilitySet</span></span>
<span data-ttu-id="06ff8-114">업데이트할 가용성 집합 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="06ff8-114">Specifies the availability set object to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06ff8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06ff8-115">-DefaultProfile</span></span>
<span data-ttu-id="06ff8-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="06ff8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06ff8-117">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="06ff8-117">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="06ff8-118">이 가용성 집합에 사용할 근접 배치 그룹의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="06ff8-118">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06ff8-119">-Sku</span><span class="sxs-lookup"><span data-stu-id="06ff8-119">-Sku</span></span>
<span data-ttu-id="06ff8-120">SKU의 이름</span><span class="sxs-lookup"><span data-stu-id="06ff8-120">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06ff8-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="06ff8-121">-Tag</span></span>
<span data-ttu-id="06ff8-122">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="06ff8-122">Key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06ff8-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06ff8-123">-Confirm</span></span>
<span data-ttu-id="06ff8-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="06ff8-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06ff8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06ff8-125">-WhatIf</span></span>
<span data-ttu-id="06ff8-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="06ff8-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06ff8-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06ff8-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06ff8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06ff8-128">CommonParameters</span></span>
<span data-ttu-id="06ff8-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="06ff8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06ff8-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="06ff8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06ff8-131">입력</span><span class="sxs-lookup"><span data-stu-id="06ff8-131">INPUTS</span></span>

### <span data-ttu-id="06ff8-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="06ff8-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="06ff8-133">출력</span><span class="sxs-lookup"><span data-stu-id="06ff8-133">OUTPUTS</span></span>

### <span data-ttu-id="06ff8-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="06ff8-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="06ff8-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="06ff8-135">NOTES</span></span>

## <span data-ttu-id="06ff8-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06ff8-136">RELATED LINKS</span></span>
