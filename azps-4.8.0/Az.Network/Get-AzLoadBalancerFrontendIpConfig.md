---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 776ff53573fa68d1757ea7c0422579e253661968
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204042"
---
# <span data-ttu-id="54e6c-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="54e6c-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="54e6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54e6c-102">SYNOPSIS</span></span>
<span data-ttu-id="54e6c-103">부하 분산 장치에서 프런트 엔드 IP 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="54e6c-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="54e6c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="54e6c-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54e6c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="54e6c-105">DESCRIPTION</span></span>
<span data-ttu-id="54e6c-106">**AzLoadBalancerFrontendIpConfig** cmdlet은 부하 분산 장치에서 프런트 엔드 ip 구성 또는 프런트 엔드 ip 구성 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="54e6c-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="54e6c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="54e6c-107">EXAMPLES</span></span>

### <span data-ttu-id="54e6c-108">예제 1: 부하 분산 장치에서 프런트 엔드 IP 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="54e6c-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="54e6c-109">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음이를 변수 $slb에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="54e6c-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="54e6c-110">두 번째 명령은 해당 부하 분산 장치에 연결 된 프런트 엔드 IP 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="54e6c-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="54e6c-111">변수</span><span class="sxs-lookup"><span data-stu-id="54e6c-111">PARAMETERS</span></span>

### <span data-ttu-id="54e6c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54e6c-112">-DefaultProfile</span></span>
<span data-ttu-id="54e6c-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="54e6c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54e6c-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="54e6c-114">-LoadBalancer</span></span>
<span data-ttu-id="54e6c-115">가져올 프런트 엔드 IP 구성에 연결 된 부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54e6c-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="54e6c-116">-이름</span><span class="sxs-lookup"><span data-stu-id="54e6c-116">-Name</span></span>
<span data-ttu-id="54e6c-117">가져올 프런트 엔드 IP 구성을 포함 하는 부하 분산 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54e6c-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="54e6c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54e6c-118">CommonParameters</span></span>
<span data-ttu-id="54e6c-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="54e6c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54e6c-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="54e6c-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54e6c-121">입력</span><span class="sxs-lookup"><span data-stu-id="54e6c-121">INPUTS</span></span>

### <span data-ttu-id="54e6c-122">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="54e6c-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="54e6c-123">출력</span><span class="sxs-lookup"><span data-stu-id="54e6c-123">OUTPUTS</span></span>

### <span data-ttu-id="54e6c-124">PSFrontendIPConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="54e6c-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="54e6c-125">상속자</span><span class="sxs-lookup"><span data-stu-id="54e6c-125">NOTES</span></span>

## <span data-ttu-id="54e6c-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54e6c-126">RELATED LINKS</span></span>

[<span data-ttu-id="54e6c-127">추가-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="54e6c-127">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="54e6c-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="54e6c-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="54e6c-129">새로운 AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="54e6c-129">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="54e6c-130">제거-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="54e6c-130">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="54e6c-131">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="54e6c-131">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


