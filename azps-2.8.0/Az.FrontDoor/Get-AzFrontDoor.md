---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
ms.openlocfilehash: 6dd40ff6bdf94d95b9fe31ead7ce6bde53c7042b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689898"
---
# <span data-ttu-id="68c32-101">Get-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="68c32-101">Get-AzFrontDoor</span></span>

## <span data-ttu-id="68c32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68c32-102">SYNOPSIS</span></span>
<span data-ttu-id="68c32-103">전방 도어 부하 분산 장치 가져오기</span><span class="sxs-lookup"><span data-stu-id="68c32-103">Get Front Door load balancer</span></span>

## <span data-ttu-id="68c32-104">구문과</span><span class="sxs-lookup"><span data-stu-id="68c32-104">SYNTAX</span></span>

```
Get-AzFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="68c32-105">설명은</span><span class="sxs-lookup"><span data-stu-id="68c32-105">DESCRIPTION</span></span>
<span data-ttu-id="68c32-106">**AzFrontDoor** cmdletget은 제공 된 정보와 일치 하는 현재 구독의 모든 기존 전방 도어를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68c32-106">The **Get-AzFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="68c32-107">예제의</span><span class="sxs-lookup"><span data-stu-id="68c32-107">EXAMPLES</span></span>

### <span data-ttu-id="68c32-108">예제 1: 현재 구독에 있는 모든 FrontDoors를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68c32-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid1}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid2}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="68c32-109">현재 플랜의 모든 FrontDoors을 받으세요.</span><span class="sxs-lookup"><span data-stu-id="68c32-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="68c32-110">예제 2: 현재 구독에서 리소스 그룹 "rg1"의 모든 FrontDoors를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68c32-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1"

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor2
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="68c32-111">현재 구독에서 리소스 그룹 "rg1"의 모든 FrontDoors를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68c32-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="68c32-112">예제 3: 현재 구독에서 이름이 "frontDoor1" 인 리소스 그룹 "rg1"의 FrontDoors를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68c32-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="68c32-113">현재 구독에서 이름이 "frontDoor1" 인 리소스 그룹 "rg1"의 FrontDoors를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68c32-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="68c32-114">변수</span><span class="sxs-lookup"><span data-stu-id="68c32-114">PARAMETERS</span></span>

### <span data-ttu-id="68c32-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68c32-115">-DefaultProfile</span></span>
<span data-ttu-id="68c32-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68c32-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68c32-117">-이름</span><span class="sxs-lookup"><span data-stu-id="68c32-117">-Name</span></span>
<span data-ttu-id="68c32-118">전방 문 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68c32-118">Front Door name.</span></span>

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

### <span data-ttu-id="68c32-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68c32-119">-ResourceGroupName</span></span>
<span data-ttu-id="68c32-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68c32-120">The resource group name.</span></span>

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

### <span data-ttu-id="68c32-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68c32-121">CommonParameters</span></span>
<span data-ttu-id="68c32-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68c32-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68c32-123">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="68c32-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68c32-124">입력</span><span class="sxs-lookup"><span data-stu-id="68c32-124">INPUTS</span></span>

### <span data-ttu-id="68c32-125">않아야</span><span class="sxs-lookup"><span data-stu-id="68c32-125">None</span></span>

## <span data-ttu-id="68c32-126">출력</span><span class="sxs-lookup"><span data-stu-id="68c32-126">OUTPUTS</span></span>

### <span data-ttu-id="68c32-127">FrontDoor. PSFrontDoor/.</span><span class="sxs-lookup"><span data-stu-id="68c32-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="68c32-128">상속자</span><span class="sxs-lookup"><span data-stu-id="68c32-128">NOTES</span></span>

## <span data-ttu-id="68c32-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68c32-129">RELATED LINKS</span></span>

<span data-ttu-id="68c32-130">[새로운 AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [제거-AzFrontDoor](./Remove-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="68c32-130">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span></span>
