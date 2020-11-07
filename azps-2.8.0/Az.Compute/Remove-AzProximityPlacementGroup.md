---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
ms.openlocfilehash: 2a3f4a6d386f37334908efde31332ed6137ecb74
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697312"
---
# <span data-ttu-id="68c51-101">Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="68c51-101">Remove-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="68c51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68c51-102">SYNOPSIS</span></span>
<span data-ttu-id="68c51-103">근접 배치 그룹 리소스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="68c51-103">Delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="68c51-104">구문과</span><span class="sxs-lookup"><span data-stu-id="68c51-104">SYNTAX</span></span>

### <span data-ttu-id="68c51-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="68c51-105">DefaultParameter (Default)</span></span>
```
Remove-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68c51-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="68c51-106">ResourceIdParameter</span></span>
```
Remove-AzProximityPlacementGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68c51-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="68c51-107">ObjectParameter</span></span>
```
Remove-AzProximityPlacementGroup [-InputObject] <PSProximityPlacementGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68c51-108">설명은</span><span class="sxs-lookup"><span data-stu-id="68c51-108">DESCRIPTION</span></span>
<span data-ttu-id="68c51-109">이 cmdlet은 근접 배치 그룹 리소스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="68c51-109">This cmdlet will delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="68c51-110">예제의</span><span class="sxs-lookup"><span data-stu-id="68c51-110">EXAMPLES</span></span>

### <span data-ttu-id="68c51-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="68c51-111">Example 1</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup  -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName  | Remove-AzureRmProximityPlacementGroup
```

<span data-ttu-id="68c51-112">이 명령은 지정 된 근접 배치 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="68c51-112">This command removes the given proximity placement group.</span></span>

## <span data-ttu-id="68c51-113">변수</span><span class="sxs-lookup"><span data-stu-id="68c51-113">PARAMETERS</span></span>

### <span data-ttu-id="68c51-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68c51-114">-AsJob</span></span>
<span data-ttu-id="68c51-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="68c51-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="68c51-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68c51-116">-DefaultProfile</span></span>
<span data-ttu-id="68c51-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68c51-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68c51-118">-Force</span><span class="sxs-lookup"><span data-stu-id="68c51-118">-Force</span></span>
<span data-ttu-id="68c51-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="68c51-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68c51-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68c51-120">-InputObject</span></span>
<span data-ttu-id="68c51-121">PS 근사 배치 그룹 개체</span><span class="sxs-lookup"><span data-stu-id="68c51-121">The PS Proximity Placement Group Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup
Parameter Sets: ObjectParameter
Aliases: ProximityPlacementGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68c51-122">-이름</span><span class="sxs-lookup"><span data-stu-id="68c51-122">-Name</span></span>
<span data-ttu-id="68c51-123">근접 배치 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68c51-123">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: ProximityPlacementGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68c51-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68c51-124">-ResourceGroupName</span></span>
<span data-ttu-id="68c51-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68c51-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68c51-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68c51-126">-ResourceId</span></span>
<span data-ttu-id="68c51-127">근접 배치 그룹의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="68c51-127">The resource id for the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68c51-128">-확인</span><span class="sxs-lookup"><span data-stu-id="68c51-128">-Confirm</span></span>
<span data-ttu-id="68c51-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="68c51-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68c51-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68c51-130">-WhatIf</span></span>
<span data-ttu-id="68c51-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="68c51-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68c51-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68c51-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68c51-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68c51-133">CommonParameters</span></span>
<span data-ttu-id="68c51-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68c51-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68c51-135">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="68c51-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68c51-136">입력</span><span class="sxs-lookup"><span data-stu-id="68c51-136">INPUTS</span></span>

### <span data-ttu-id="68c51-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="68c51-137">System.String</span></span>

### <span data-ttu-id="68c51-138">PSProximityPlacementGroup의. m a.</span><span class="sxs-lookup"><span data-stu-id="68c51-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="68c51-139">출력</span><span class="sxs-lookup"><span data-stu-id="68c51-139">OUTPUTS</span></span>

### <span data-ttu-id="68c51-140">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="68c51-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="68c51-141">상속자</span><span class="sxs-lookup"><span data-stu-id="68c51-141">NOTES</span></span>

## <span data-ttu-id="68c51-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68c51-142">RELATED LINKS</span></span>
