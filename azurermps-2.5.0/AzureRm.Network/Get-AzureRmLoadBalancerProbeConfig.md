---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerprobeconfig
schema: 2.0.0
ms.openlocfilehash: 30989d3b9c71821c2eae3cdfd97f9e4e5fc0cb15
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882958"
---
# <span data-ttu-id="5dd1c-101">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5dd1c-101">Get-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="5dd1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5dd1c-102">SYNOPSIS</span></span>
<span data-ttu-id="5dd1c-103">부하 분산 장치에 대 한 프로브 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5dd1c-103">Gets a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5dd1c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5dd1c-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5dd1c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5dd1c-105">DESCRIPTION</span></span>
<span data-ttu-id="5dd1c-106">**AzureRmLoadBalancerProbeConfig** cmdlet은 부하 분산 장치에 대 한 하나 이상의 프로브 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5dd1c-106">The **Get-AzureRmLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="5dd1c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5dd1c-107">EXAMPLES</span></span>

### <span data-ttu-id="5dd1c-108">예제 1: 부하 분산 장치에 대 한 프로브 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="5dd1c-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="5dd1c-109">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음이를 변수 $slb에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dd1c-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="5dd1c-110">두 번째 명령은 $slb의 부하 분산 장치에서 MyProbe 라는 연결 된 프로브 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5dd1c-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="5dd1c-111">변수</span><span class="sxs-lookup"><span data-stu-id="5dd1c-111">PARAMETERS</span></span>

### <span data-ttu-id="5dd1c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dd1c-112">-DefaultProfile</span></span>
<span data-ttu-id="5dd1c-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5dd1c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd1c-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5dd1c-114">-LoadBalancer</span></span>
<span data-ttu-id="5dd1c-115">가져올 프로브 구성과 연결 된 부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dd1c-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5dd1c-116">-이름</span><span class="sxs-lookup"><span data-stu-id="5dd1c-116">-Name</span></span>
<span data-ttu-id="5dd1c-117">가져올 프로브 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dd1c-117">Specifies the name of the probe configuration to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd1c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dd1c-118">CommonParameters</span></span>
<span data-ttu-id="5dd1c-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dd1c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dd1c-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dd1c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dd1c-121">입력</span><span class="sxs-lookup"><span data-stu-id="5dd1c-121">INPUTS</span></span>

### <span data-ttu-id="5dd1c-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5dd1c-122">PSLoadBalancer</span></span>
<span data-ttu-id="5dd1c-123">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dd1c-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="5dd1c-124">출력</span><span class="sxs-lookup"><span data-stu-id="5dd1c-124">OUTPUTS</span></span>

### <span data-ttu-id="5dd1c-125">Microsoft. 네트워크. PSProbe</span><span class="sxs-lookup"><span data-stu-id="5dd1c-125">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="5dd1c-126">상속자</span><span class="sxs-lookup"><span data-stu-id="5dd1c-126">NOTES</span></span>

## <span data-ttu-id="5dd1c-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5dd1c-127">RELATED LINKS</span></span>

[<span data-ttu-id="5dd1c-128">추가-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5dd1c-128">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="5dd1c-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5dd1c-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="5dd1c-130">새로운 AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5dd1c-130">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="5dd1c-131">제거-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5dd1c-131">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="5dd1c-132">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5dd1c-132">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


