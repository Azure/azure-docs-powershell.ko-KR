---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: dd887874540a216cc826f807059e6534b99e28f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365555"
---
# <span data-ttu-id="95f36-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="95f36-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="95f36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95f36-102">SYNOPSIS</span></span>
<span data-ttu-id="95f36-103">부하 균형 조정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="95f36-103">Gets a load balancer.</span></span>

## <span data-ttu-id="95f36-104">구문</span><span class="sxs-lookup"><span data-stu-id="95f36-104">SYNTAX</span></span>

### <span data-ttu-id="95f36-105">NoExpand(기본값)</span><span class="sxs-lookup"><span data-stu-id="95f36-105">NoExpand (Default)</span></span>
```
Get-AzLoadBalancer [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95f36-106">확장</span><span class="sxs-lookup"><span data-stu-id="95f36-106">Expand</span></span>
```
Get-AzLoadBalancer -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95f36-107">설명</span><span class="sxs-lookup"><span data-stu-id="95f36-107">DESCRIPTION</span></span>
<span data-ttu-id="95f36-108">**Get-AzLoadBalancer** cmdlet은 리소스 그룹에 포함된 하나 이상의 Azure Load Balancers를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="95f36-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="95f36-109">예제</span><span class="sxs-lookup"><span data-stu-id="95f36-109">EXAMPLES</span></span>

### <span data-ttu-id="95f36-110">예제 1: 부하 균형 조정기</span><span class="sxs-lookup"><span data-stu-id="95f36-110">Example 1: Get a load balancer</span></span>
```
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer1" -ResourceGroupName "MyResourceGroup"

Name                     : MyLoadBalancer1
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }
```

<span data-ttu-id="95f36-111">이 명령은 MyLoadBalancer라는 부하 분산을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="95f36-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="95f36-112">이 cmdlet을 실행하려면 먼저 부하 균형 조정이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="95f36-112">A load balancer must exist before you can run this cmdlet.</span></span>

### <span data-ttu-id="95f36-113">예제 2: 필터링을 사용하여 부하 균형 조정기 나열</span><span class="sxs-lookup"><span data-stu-id="95f36-113">Example 2: List load balancers using filtering</span></span>
```
PS C:\> Get-AzLoadBalancer -Name MyLoadBalancer*

Name                     : MyLoadBalancer1
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }

Name                     : MyLoadBalancer2
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer2
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }
```

<span data-ttu-id="95f36-114">이 명령은 "MyLoadBalancer"로 시작하는 이름으로 모든 부하 분산을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="95f36-114">This command gets all load balancers with a name that starts with "MyLoadBalancer"</span></span>

## <span data-ttu-id="95f36-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95f36-115">PARAMETERS</span></span>

### <span data-ttu-id="95f36-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95f36-116">-DefaultProfile</span></span>
<span data-ttu-id="95f36-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95f36-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95f36-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="95f36-118">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95f36-119">-Name</span><span class="sxs-lookup"><span data-stu-id="95f36-119">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="95f36-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95f36-120">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="95f36-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95f36-121">CommonParameters</span></span>
<span data-ttu-id="95f36-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="95f36-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95f36-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="95f36-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95f36-124">입력</span><span class="sxs-lookup"><span data-stu-id="95f36-124">INPUTS</span></span>

### <span data-ttu-id="95f36-125">System.String</span><span class="sxs-lookup"><span data-stu-id="95f36-125">System.String</span></span>

## <span data-ttu-id="95f36-126">출력</span><span class="sxs-lookup"><span data-stu-id="95f36-126">OUTPUTS</span></span>

### <span data-ttu-id="95f36-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="95f36-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="95f36-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="95f36-128">NOTES</span></span>

## <span data-ttu-id="95f36-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95f36-129">RELATED LINKS</span></span>

[<span data-ttu-id="95f36-130">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="95f36-130">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="95f36-131">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="95f36-131">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="95f36-132">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="95f36-132">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


