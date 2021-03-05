---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: 4f268ae4278712e16e8efc126702d0130dc225cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964955"
---
# <span data-ttu-id="c7bdd-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c7bdd-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="c7bdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7bdd-102">SYNOPSIS</span></span>
<span data-ttu-id="c7bdd-103">가용성 집합을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c7bdd-103">Updates an availability set.</span></span>

## <span data-ttu-id="c7bdd-104">구문</span><span class="sxs-lookup"><span data-stu-id="c7bdd-104">SYNTAX</span></span>

```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7bdd-105">설명</span><span class="sxs-lookup"><span data-stu-id="c7bdd-105">DESCRIPTION</span></span>
<span data-ttu-id="c7bdd-106">**Update-AzAvailabilitySet** cmdlet은 가용성 집합을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c7bdd-106">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="c7bdd-107">예제</span><span class="sxs-lookup"><span data-stu-id="c7bdd-107">EXAMPLES</span></span>

### <span data-ttu-id="c7bdd-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c7bdd-108">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="c7bdd-109">이 명령은 'ResourceGroup01'이라는 리소스 그룹의 'AvSet01'이라는 가용성 집합을 관리되는 가용성 집합으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c7bdd-109">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="c7bdd-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c7bdd-110">PARAMETERS</span></span>

### <span data-ttu-id="c7bdd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7bdd-111">-AsJob</span></span>
<span data-ttu-id="c7bdd-112">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="c7bdd-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c7bdd-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c7bdd-113">-AvailabilitySet</span></span>
<span data-ttu-id="c7bdd-114">업데이트할 가용성 집합 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c7bdd-114">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="c7bdd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7bdd-115">-DefaultProfile</span></span>
<span data-ttu-id="c7bdd-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c7bdd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7bdd-117">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="c7bdd-117">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="c7bdd-118">이 가용성 집합과 함께 사용할 근접 배치 그룹의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c7bdd-118">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

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

### <span data-ttu-id="c7bdd-119">-Sku</span><span class="sxs-lookup"><span data-stu-id="c7bdd-119">-Sku</span></span>
<span data-ttu-id="c7bdd-120">Sku의 이름</span><span class="sxs-lookup"><span data-stu-id="c7bdd-120">The Name of Sku</span></span>

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

### <span data-ttu-id="c7bdd-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="c7bdd-121">-Tag</span></span>
<span data-ttu-id="c7bdd-122">해시 테이블의 형태로 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="c7bdd-122">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="c7bdd-123">-확인</span><span class="sxs-lookup"><span data-stu-id="c7bdd-123">-Confirm</span></span>
<span data-ttu-id="c7bdd-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c7bdd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7bdd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7bdd-125">-WhatIf</span></span>
<span data-ttu-id="c7bdd-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c7bdd-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7bdd-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7bdd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7bdd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7bdd-128">CommonParameters</span></span>
<span data-ttu-id="c7bdd-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c7bdd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7bdd-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7bdd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7bdd-131">입력</span><span class="sxs-lookup"><span data-stu-id="c7bdd-131">INPUTS</span></span>

### <span data-ttu-id="c7bdd-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c7bdd-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="c7bdd-133">출력</span><span class="sxs-lookup"><span data-stu-id="c7bdd-133">OUTPUTS</span></span>

### <span data-ttu-id="c7bdd-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c7bdd-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="c7bdd-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c7bdd-135">NOTES</span></span>

## <span data-ttu-id="c7bdd-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7bdd-136">RELATED LINKS</span></span>
