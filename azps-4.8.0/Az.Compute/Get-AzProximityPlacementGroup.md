---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
ms.openlocfilehash: a6308120303684a8e87280ef903056361fbaf848
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048449"
---
# <span data-ttu-id="c5af9-101">Get-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="c5af9-101">Get-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="c5af9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5af9-102">SYNOPSIS</span></span>
<span data-ttu-id="c5af9-103">근접 배치 그룹 리소스를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5af9-103">Get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="c5af9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c5af9-104">SYNTAX</span></span>

### <span data-ttu-id="c5af9-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="c5af9-105">DefaultParameter (Default)</span></span>
```
Get-AzProximityPlacementGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-ColocationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5af9-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="c5af9-106">ResourceIdParameter</span></span>
```
Get-AzProximityPlacementGroup [-ColocationStatus] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5af9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c5af9-107">DESCRIPTION</span></span>
<span data-ttu-id="c5af9-108">이 cmdlet은 근접 배치 그룹 리소스를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5af9-108">This cmdlet will get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="c5af9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c5af9-109">EXAMPLES</span></span>

### <span data-ttu-id="c5af9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c5af9-110">Example 1</span></span>
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

<span data-ttu-id="c5af9-111">이 명령은 근접 배치 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c5af9-111">This command gets the proximity placement group</span></span>

### <span data-ttu-id="c5af9-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="c5af9-112">Example 2</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
```

<span data-ttu-id="c5af9-113">이 명령은 지정 된 리소스 그룹 아래의 모든 근접 배치 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5af9-113">This command list all proximity placement groups under the given resource group.</span></span>

### <span data-ttu-id="c5af9-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="c5af9-114">Example 3</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
rg1                          ppg2     centralus Standard
```

<span data-ttu-id="c5af9-115">이 명령은 구독 아래의 모든 근접 배치 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5af9-115">This command list all proximity placement groups under the subscription.</span></span>

## <span data-ttu-id="c5af9-116">변수</span><span class="sxs-lookup"><span data-stu-id="c5af9-116">PARAMETERS</span></span>

### <span data-ttu-id="c5af9-117">-ColocationStatus</span><span class="sxs-lookup"><span data-stu-id="c5af9-117">-ColocationStatus</span></span>
<span data-ttu-id="c5af9-118">근접 배치 그룹에 있는 리소스의 공동 위치 상태를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c5af9-118">Shows the colocation status of a resource in the proximity placement group.</span></span>

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

### <span data-ttu-id="c5af9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5af9-119">-DefaultProfile</span></span>
<span data-ttu-id="c5af9-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c5af9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5af9-121">-이름</span><span class="sxs-lookup"><span data-stu-id="c5af9-121">-Name</span></span>
<span data-ttu-id="c5af9-122">근접 배치 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5af9-122">The name of the proximity placement group.</span></span>

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

### <span data-ttu-id="c5af9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5af9-123">-ResourceGroupName</span></span>
<span data-ttu-id="c5af9-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5af9-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="c5af9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5af9-125">-ResourceId</span></span>
<span data-ttu-id="c5af9-126">근접 배치 그룹의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="c5af9-126">The resource id for the proximity placement group.</span></span>

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

### <span data-ttu-id="c5af9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5af9-127">CommonParameters</span></span>
<span data-ttu-id="c5af9-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5af9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5af9-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c5af9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5af9-130">입력</span><span class="sxs-lookup"><span data-stu-id="c5af9-130">INPUTS</span></span>

### <span data-ttu-id="c5af9-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c5af9-131">System.String</span></span>

## <span data-ttu-id="c5af9-132">출력</span><span class="sxs-lookup"><span data-stu-id="c5af9-132">OUTPUTS</span></span>

### <span data-ttu-id="c5af9-133">PSProximityPlacementGroup의. m a.</span><span class="sxs-lookup"><span data-stu-id="c5af9-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="c5af9-134">상속자</span><span class="sxs-lookup"><span data-stu-id="c5af9-134">NOTES</span></span>

## <span data-ttu-id="c5af9-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5af9-135">RELATED LINKS</span></span>
