---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 4b880e98a2b0352591e4a4e8840500ba2d25e431
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870161"
---
# <span data-ttu-id="783d0-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="783d0-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="783d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="783d0-102">SYNOPSIS</span></span>
<span data-ttu-id="783d0-103">부하 분산 장치에 대 한 프로브 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="783d0-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="783d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="783d0-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="783d0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="783d0-105">DESCRIPTION</span></span>
<span data-ttu-id="783d0-106">**AzLoadBalancerProbeConfig** cmdlet은 부하 분산 장치에 대 한 하나 이상의 프로브 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="783d0-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="783d0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="783d0-107">EXAMPLES</span></span>

### <span data-ttu-id="783d0-108">예제 1: 부하 분산 장치에 대 한 프로브 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="783d0-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="783d0-109">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음이를 변수 $slb에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="783d0-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="783d0-110">두 번째 명령은 $slb의 부하 분산 장치에서 MyProbe 라는 연결 된 프로브 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="783d0-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="783d0-111">변수</span><span class="sxs-lookup"><span data-stu-id="783d0-111">PARAMETERS</span></span>

### <span data-ttu-id="783d0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="783d0-112">-DefaultProfile</span></span>
<span data-ttu-id="783d0-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="783d0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="783d0-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="783d0-114">-LoadBalancer</span></span>
<span data-ttu-id="783d0-115">가져올 프로브 구성과 연결 된 부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="783d0-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="783d0-116">-이름</span><span class="sxs-lookup"><span data-stu-id="783d0-116">-Name</span></span>
<span data-ttu-id="783d0-117">가져올 프로브 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="783d0-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="783d0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="783d0-118">CommonParameters</span></span>
<span data-ttu-id="783d0-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="783d0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="783d0-120">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="783d0-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="783d0-121">입력</span><span class="sxs-lookup"><span data-stu-id="783d0-121">INPUTS</span></span>

### <span data-ttu-id="783d0-122">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="783d0-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="783d0-123">출력</span><span class="sxs-lookup"><span data-stu-id="783d0-123">OUTPUTS</span></span>

### <span data-ttu-id="783d0-124">Microsoft. 네트워크. PSProbe</span><span class="sxs-lookup"><span data-stu-id="783d0-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="783d0-125">상속자</span><span class="sxs-lookup"><span data-stu-id="783d0-125">NOTES</span></span>

## <span data-ttu-id="783d0-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="783d0-126">RELATED LINKS</span></span>

[<span data-ttu-id="783d0-127">추가-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="783d0-127">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="783d0-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="783d0-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="783d0-129">새로운 AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="783d0-129">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="783d0-130">제거-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="783d0-130">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="783d0-131">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="783d0-131">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


