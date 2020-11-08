---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: 767f725633560d79cb19e1caad61c08772107b42
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214137"
---
# <span data-ttu-id="4384b-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4384b-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="4384b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4384b-102">SYNOPSIS</span></span>
<span data-ttu-id="4384b-103">부하 분산 장치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4384b-103">Gets a load balancer.</span></span>

## <span data-ttu-id="4384b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4384b-104">SYNTAX</span></span>

### <span data-ttu-id="4384b-105">NoExpand (기본값)</span><span class="sxs-lookup"><span data-stu-id="4384b-105">NoExpand (Default)</span></span>
```
Get-AzLoadBalancer [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4384b-106">확장</span><span class="sxs-lookup"><span data-stu-id="4384b-106">Expand</span></span>
```
Get-AzLoadBalancer -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4384b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4384b-107">DESCRIPTION</span></span>
<span data-ttu-id="4384b-108">**AzLoadBalancer** cmdlet은 리소스 그룹에 포함 된 하나 이상의 Azure 부하 분산 장치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4384b-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="4384b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4384b-109">EXAMPLES</span></span>

### <span data-ttu-id="4384b-110">예제 1: 부하 분산 장치 가져오기</span><span class="sxs-lookup"><span data-stu-id="4384b-110">Example 1: Get a load balancer</span></span>
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
                             "Name": "Basic"
                           }
```

<span data-ttu-id="4384b-111">이 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4384b-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="4384b-112">이 cmdlet을 실행 하려면 로드 균형 조정기가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4384b-112">A load balancer must exist before you can run this cmdlet.</span></span>

### <span data-ttu-id="4384b-113">예제 2: 필터링을 사용 하 여 부하 분산 장치 나열</span><span class="sxs-lookup"><span data-stu-id="4384b-113">Example 2: List load balancers using filtering</span></span>
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
                             "Name": "Basic"
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
                             "Name": "Basic"
                           }
```

<span data-ttu-id="4384b-114">이 명령은 "MyLoadBalancer"로 시작 하는 이름을 사용 하 여 모든 부하 분산 장치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4384b-114">This command gets all load balancers with a name that starts with "MyLoadBalancer"</span></span>

## <span data-ttu-id="4384b-115">변수</span><span class="sxs-lookup"><span data-stu-id="4384b-115">PARAMETERS</span></span>

### <span data-ttu-id="4384b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4384b-116">-DefaultProfile</span></span>
<span data-ttu-id="4384b-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4384b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4384b-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="4384b-118">-ExpandResource</span></span>
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

### <span data-ttu-id="4384b-119">-이름</span><span class="sxs-lookup"><span data-stu-id="4384b-119">-Name</span></span>
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

### <span data-ttu-id="4384b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4384b-120">-ResourceGroupName</span></span>
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

### <span data-ttu-id="4384b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4384b-121">CommonParameters</span></span>
<span data-ttu-id="4384b-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4384b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4384b-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4384b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4384b-124">입력</span><span class="sxs-lookup"><span data-stu-id="4384b-124">INPUTS</span></span>

### <span data-ttu-id="4384b-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4384b-125">System.String</span></span>

## <span data-ttu-id="4384b-126">출력</span><span class="sxs-lookup"><span data-stu-id="4384b-126">OUTPUTS</span></span>

### <span data-ttu-id="4384b-127">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4384b-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4384b-128">상속자</span><span class="sxs-lookup"><span data-stu-id="4384b-128">NOTES</span></span>

## <span data-ttu-id="4384b-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4384b-129">RELATED LINKS</span></span>

[<span data-ttu-id="4384b-130">새로운 AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4384b-130">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="4384b-131">제거-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4384b-131">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="4384b-132">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4384b-132">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


