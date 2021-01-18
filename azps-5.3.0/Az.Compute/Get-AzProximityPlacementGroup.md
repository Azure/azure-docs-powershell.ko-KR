---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
ms.openlocfilehash: a6308120303684a8e87280ef903056361fbaf848
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493889"
---
# <span data-ttu-id="204e2-101">Get-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="204e2-101">Get-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="204e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="204e2-102">SYNOPSIS</span></span>
<span data-ttu-id="204e2-103">근접 배치 그룹 리소스를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="204e2-103">Get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="204e2-104">구문</span><span class="sxs-lookup"><span data-stu-id="204e2-104">SYNTAX</span></span>

### <span data-ttu-id="204e2-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="204e2-105">DefaultParameter (Default)</span></span>
```
Get-AzProximityPlacementGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-ColocationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="204e2-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="204e2-106">ResourceIdParameter</span></span>
```
Get-AzProximityPlacementGroup [-ColocationStatus] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="204e2-107">설명</span><span class="sxs-lookup"><span data-stu-id="204e2-107">DESCRIPTION</span></span>
<span data-ttu-id="204e2-108">이 cmdlet은 근접 배치 그룹 리소스를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="204e2-108">This cmdlet will get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="204e2-109">예제</span><span class="sxs-lookup"><span data-stu-id="204e2-109">EXAMPLES</span></span>

### <span data-ttu-id="204e2-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="204e2-110">Example 1</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName

ResourceGroupName           : rg0
ProximityPlacementGroupType : Standard
VirtualMachines             : {}
VirtualMachineScaleSets     : {}
AvailabilitySets            : {}
Id                          : /subscriptions/5393f919-a68a-43d0-9063-4b2bda6bffdf/resourceGroups/rg0/providers/Microsoft.Compute/proximityPlacementGroups/ppg0
Name                        : ppg0
Type                        : Microsoft.Compute/proximityPlacementGroups
Location                    : westcentralus
Tags                        : {[key1, val1]}
```

<span data-ttu-id="204e2-111">이 명령은 근접 배치 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="204e2-111">This command gets the proximity placement group</span></span>

### <span data-ttu-id="204e2-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="204e2-112">Example 2</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
```

<span data-ttu-id="204e2-113">이 명령은 주어진 리소스 그룹 아래에 있는 모든 근접 배치 그룹을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="204e2-113">This command list all proximity placement groups under the given resource group.</span></span>

### <span data-ttu-id="204e2-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="204e2-114">Example 3</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
rg1                          ppg2     centralus Standard
```

<span data-ttu-id="204e2-115">이 명령은 구독의 모든 근접 배치 그룹을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="204e2-115">This command list all proximity placement groups under the subscription.</span></span>

## <span data-ttu-id="204e2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="204e2-116">PARAMETERS</span></span>

### <span data-ttu-id="204e2-117">-ColocationStatus</span><span class="sxs-lookup"><span data-stu-id="204e2-117">-ColocationStatus</span></span>
<span data-ttu-id="204e2-118">근접 배치 그룹에 있는 리소스의 공동 배치 상태를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="204e2-118">Shows the colocation status of a resource in the proximity placement group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="204e2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="204e2-119">-DefaultProfile</span></span>
<span data-ttu-id="204e2-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="204e2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="204e2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="204e2-121">-Name</span></span>
<span data-ttu-id="204e2-122">근접 배치 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="204e2-122">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: ProximityPlacementGroupName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="204e2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="204e2-123">-ResourceGroupName</span></span>
<span data-ttu-id="204e2-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="204e2-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="204e2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="204e2-125">-ResourceId</span></span>
<span data-ttu-id="204e2-126">근접 배치 그룹에 대한 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="204e2-126">The resource id for the proximity placement group.</span></span>

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

### <span data-ttu-id="204e2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="204e2-127">CommonParameters</span></span>
<span data-ttu-id="204e2-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="204e2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="204e2-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="204e2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="204e2-130">입력</span><span class="sxs-lookup"><span data-stu-id="204e2-130">INPUTS</span></span>

### <span data-ttu-id="204e2-131">System.String</span><span class="sxs-lookup"><span data-stu-id="204e2-131">System.String</span></span>

## <span data-ttu-id="204e2-132">출력</span><span class="sxs-lookup"><span data-stu-id="204e2-132">OUTPUTS</span></span>

### <span data-ttu-id="204e2-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="204e2-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="204e2-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="204e2-134">NOTES</span></span>

## <span data-ttu-id="204e2-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="204e2-135">RELATED LINKS</span></span>
