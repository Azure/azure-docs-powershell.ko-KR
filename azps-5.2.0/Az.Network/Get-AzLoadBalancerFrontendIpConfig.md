---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 776ff53573fa68d1757ea7c0422579e253661968
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358912"
---
# <span data-ttu-id="cc7ec-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cc7ec-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="cc7ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc7ec-102">SYNOPSIS</span></span>
<span data-ttu-id="cc7ec-103">부하 균형 조정기에서 프런트 엔드 IP 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cc7ec-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="cc7ec-104">구문</span><span class="sxs-lookup"><span data-stu-id="cc7ec-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc7ec-105">설명</span><span class="sxs-lookup"><span data-stu-id="cc7ec-105">DESCRIPTION</span></span>
<span data-ttu-id="cc7ec-106">**Get-AzLoadBalancerFrontendIpConfig** cmdlet은 부하 분산의 프런트 엔드 IP 구성 또는 프런트 엔드 IP 구성 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cc7ec-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="cc7ec-107">예제</span><span class="sxs-lookup"><span data-stu-id="cc7ec-107">EXAMPLES</span></span>

### <span data-ttu-id="cc7ec-108">예제 1: 부하 균형 조정기에서 프런트 엔드 IP 구성을 얻게</span><span class="sxs-lookup"><span data-stu-id="cc7ec-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="cc7ec-109">첫 번째 명령은 MyLoadBalancer라는 부하 분산을 하여 변수에 $slb.</span><span class="sxs-lookup"><span data-stu-id="cc7ec-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="cc7ec-110">두 번째 명령은 해당 부하 균형 조정과 연결된 프런트 엔드 IP 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cc7ec-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="cc7ec-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc7ec-111">PARAMETERS</span></span>

### <span data-ttu-id="cc7ec-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc7ec-112">-DefaultProfile</span></span>
<span data-ttu-id="cc7ec-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cc7ec-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc7ec-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cc7ec-114">-LoadBalancer</span></span>
<span data-ttu-id="cc7ec-115">얻을 프런트 엔드 IP 구성과 연결된 부하 균형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cc7ec-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc7ec-116">-Name</span><span class="sxs-lookup"><span data-stu-id="cc7ec-116">-Name</span></span>
<span data-ttu-id="cc7ec-117">얻을 프런트 엔드 IP 구성을 포함하는 부하 균형 조정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cc7ec-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="cc7ec-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc7ec-118">CommonParameters</span></span>
<span data-ttu-id="cc7ec-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cc7ec-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc7ec-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cc7ec-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc7ec-121">입력</span><span class="sxs-lookup"><span data-stu-id="cc7ec-121">INPUTS</span></span>

### <span data-ttu-id="cc7ec-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cc7ec-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="cc7ec-123">출력</span><span class="sxs-lookup"><span data-stu-id="cc7ec-123">OUTPUTS</span></span>

### <span data-ttu-id="cc7ec-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc7ec-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="cc7ec-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cc7ec-125">NOTES</span></span>

## <span data-ttu-id="cc7ec-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cc7ec-126">RELATED LINKS</span></span>

[<span data-ttu-id="cc7ec-127">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cc7ec-127">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="cc7ec-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cc7ec-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="cc7ec-129">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cc7ec-129">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="cc7ec-130">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cc7ec-130">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="cc7ec-131">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cc7ec-131">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


