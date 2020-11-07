---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
ms.openlocfilehash: 9ec2760ba50d4ed97ebf36f5bab7c02d110d77ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697468"
---
# <span data-ttu-id="c31e4-101">Get-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="c31e4-101">Get-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="c31e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c31e4-102">SYNOPSIS</span></span>
<span data-ttu-id="c31e4-103">근접 배치 그룹 리소스를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c31e4-103">Get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="c31e4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c31e4-104">SYNTAX</span></span>

### <span data-ttu-id="c31e4-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="c31e4-105">DefaultParameter (Default)</span></span>
```
Get-AzProximityPlacementGroup [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c31e4-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="c31e4-106">ResourceIdParameter</span></span>
```
Get-AzProximityPlacementGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c31e4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c31e4-107">DESCRIPTION</span></span>
<span data-ttu-id="c31e4-108">이 cmdlet은 근접 배치 그룹 리소스를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c31e4-108">This cmdlet will get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="c31e4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c31e4-109">EXAMPLES</span></span>

### <span data-ttu-id="c31e4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c31e4-110">Example 1</span></span>
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

<span data-ttu-id="c31e4-111">이 명령은 근접 배치 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c31e4-111">This command gets the proximity placement group</span></span>

### <span data-ttu-id="c31e4-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="c31e4-112">Example 2</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
```

<span data-ttu-id="c31e4-113">이 명령은 지정 된 리소스 그룹 아래의 모든 근접 배치 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c31e4-113">This command list all proximity placement groups under the given resource group.</span></span>

### <span data-ttu-id="c31e4-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="c31e4-114">Example 3</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
rg1                          ppg2     centralus Standard
```

<span data-ttu-id="c31e4-115">이 명령은 구독 아래의 모든 근접 배치 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c31e4-115">This command list all proximity placement groups under the subscription.</span></span>

## <span data-ttu-id="c31e4-116">변수</span><span class="sxs-lookup"><span data-stu-id="c31e4-116">PARAMETERS</span></span>

### <span data-ttu-id="c31e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c31e4-117">-DefaultProfile</span></span>
<span data-ttu-id="c31e4-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c31e4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c31e4-119">-이름</span><span class="sxs-lookup"><span data-stu-id="c31e4-119">-Name</span></span>
<span data-ttu-id="c31e4-120">근접 배치 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c31e4-120">The name of the proximity placement group.</span></span>

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

### <span data-ttu-id="c31e4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c31e4-121">-ResourceGroupName</span></span>
<span data-ttu-id="c31e4-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c31e4-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="c31e4-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c31e4-123">-ResourceId</span></span>
<span data-ttu-id="c31e4-124">근접 배치 그룹의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="c31e4-124">The resource id for the proximity placement group.</span></span>

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

### <span data-ttu-id="c31e4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c31e4-125">CommonParameters</span></span>
<span data-ttu-id="c31e4-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c31e4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c31e4-127">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c31e4-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c31e4-128">입력</span><span class="sxs-lookup"><span data-stu-id="c31e4-128">INPUTS</span></span>

### <span data-ttu-id="c31e4-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c31e4-129">System.String</span></span>

## <span data-ttu-id="c31e4-130">출력</span><span class="sxs-lookup"><span data-stu-id="c31e4-130">OUTPUTS</span></span>

### <span data-ttu-id="c31e4-131">PSProximityPlacementGroup의. m a.</span><span class="sxs-lookup"><span data-stu-id="c31e4-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="c31e4-132">상속자</span><span class="sxs-lookup"><span data-stu-id="c31e4-132">NOTES</span></span>

## <span data-ttu-id="c31e4-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c31e4-133">RELATED LINKS</span></span>
