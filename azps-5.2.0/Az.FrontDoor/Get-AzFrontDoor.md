---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
ms.openlocfilehash: 8c378d7f0b1ac7a753f7f270fd3969eb881c7aec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354369"
---
# <span data-ttu-id="76b97-101">Get-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="76b97-101">Get-AzFrontDoor</span></span>

## <span data-ttu-id="76b97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76b97-102">SYNOPSIS</span></span>
<span data-ttu-id="76b97-103">Front Door 부하 균형 조정기</span><span class="sxs-lookup"><span data-stu-id="76b97-103">Get Front Door load balancer</span></span>

## <span data-ttu-id="76b97-104">구문</span><span class="sxs-lookup"><span data-stu-id="76b97-104">SYNTAX</span></span>

```
Get-AzFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76b97-105">설명</span><span class="sxs-lookup"><span data-stu-id="76b97-105">DESCRIPTION</span></span>
<span data-ttu-id="76b97-106">**Get-AzFrontDoor** cmdletGet은 제공된 정보와 일치하는 현재 구독의 모든 기존 Front Door를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="76b97-106">The **Get-AzFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="76b97-107">예제</span><span class="sxs-lookup"><span data-stu-id="76b97-107">EXAMPLES</span></span>

### <span data-ttu-id="76b97-108">예제 1: 현재 구독의 모든 FrontDoors를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="76b97-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
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

<span data-ttu-id="76b97-109">현재 구독의 모든 FrontDoors를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="76b97-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="76b97-110">예제 2: 현재 구독의 리소스 그룹 "rg1"에 있는 모든 FrontDoors를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="76b97-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
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

<span data-ttu-id="76b97-111">현재 구독의 리소스 그룹 "rg1"에 있는 모든 FrontDoors를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="76b97-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="76b97-112">예제 3: 현재 구독에서 이름이 "frontDoor1"인 리소스 그룹 "rg1"의 FrontDoors를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="76b97-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
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

<span data-ttu-id="76b97-113">현재 구독에서 이름이 "frontDoor1"인 리소스 그룹 "rg1"의 FrontDoors를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="76b97-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="76b97-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76b97-114">PARAMETERS</span></span>

### <span data-ttu-id="76b97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76b97-115">-DefaultProfile</span></span>
<span data-ttu-id="76b97-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="76b97-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76b97-117">-Name</span><span class="sxs-lookup"><span data-stu-id="76b97-117">-Name</span></span>
<span data-ttu-id="76b97-118">Front Door 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="76b97-118">Front Door name.</span></span>

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

### <span data-ttu-id="76b97-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76b97-119">-ResourceGroupName</span></span>
<span data-ttu-id="76b97-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="76b97-120">The resource group name.</span></span>

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

### <span data-ttu-id="76b97-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76b97-121">CommonParameters</span></span>
<span data-ttu-id="76b97-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76b97-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76b97-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="76b97-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76b97-124">입력</span><span class="sxs-lookup"><span data-stu-id="76b97-124">INPUTS</span></span>

### <span data-ttu-id="76b97-125">없음</span><span class="sxs-lookup"><span data-stu-id="76b97-125">None</span></span>

## <span data-ttu-id="76b97-126">출력</span><span class="sxs-lookup"><span data-stu-id="76b97-126">OUTPUTS</span></span>

### <span data-ttu-id="76b97-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="76b97-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="76b97-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="76b97-128">NOTES</span></span>

## <span data-ttu-id="76b97-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76b97-129">RELATED LINKS</span></span>

<span data-ttu-id="76b97-130">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="76b97-130">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span></span>
