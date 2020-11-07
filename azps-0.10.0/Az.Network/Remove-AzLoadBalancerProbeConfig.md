---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 11de4e8966b5e57e817b6c5d829536deacf229f8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875330"
---
# <span data-ttu-id="22762-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="22762-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="22762-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22762-102">SYNOPSIS</span></span>
<span data-ttu-id="22762-103">부하 분산 장치에서 프로브 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="22762-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="22762-104">구문과</span><span class="sxs-lookup"><span data-stu-id="22762-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22762-105">설명은</span><span class="sxs-lookup"><span data-stu-id="22762-105">DESCRIPTION</span></span>
<span data-ttu-id="22762-106">**AzLoadBalancerProbeConfig** cmdlet은 부하 분산 장치에서 프로브 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="22762-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="22762-107">예제의</span><span class="sxs-lookup"><span data-stu-id="22762-107">EXAMPLES</span></span>

### <span data-ttu-id="22762-108">예제 1: 부하 분산 장치에서 프로브 구성 제거</span><span class="sxs-lookup"><span data-stu-id="22762-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="22762-109">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음 $loadbalancer 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="22762-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="22762-110">두 번째 명령은 $loadbalancer의 부하 분산 장치에서 MyProbe 구성을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="22762-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="22762-111">변수</span><span class="sxs-lookup"><span data-stu-id="22762-111">PARAMETERS</span></span>

### <span data-ttu-id="22762-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22762-112">-DefaultProfile</span></span>
<span data-ttu-id="22762-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="22762-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22762-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="22762-114">-LoadBalancer</span></span>
<span data-ttu-id="22762-115">이 cmdlet이 제거 하는 프로브 구성을 포함 하는 부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22762-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="22762-116">-이름</span><span class="sxs-lookup"><span data-stu-id="22762-116">-Name</span></span>
<span data-ttu-id="22762-117">이 cmdlet이 제거 하는 프로브 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22762-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="22762-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22762-118">CommonParameters</span></span>
<span data-ttu-id="22762-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="22762-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22762-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22762-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22762-121">입력</span><span class="sxs-lookup"><span data-stu-id="22762-121">INPUTS</span></span>

### <span data-ttu-id="22762-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="22762-122">PSLoadBalancer</span></span>
<span data-ttu-id="22762-123">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="22762-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="22762-124">출력</span><span class="sxs-lookup"><span data-stu-id="22762-124">OUTPUTS</span></span>

### <span data-ttu-id="22762-125">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="22762-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="22762-126">상속자</span><span class="sxs-lookup"><span data-stu-id="22762-126">NOTES</span></span>

## <span data-ttu-id="22762-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22762-127">RELATED LINKS</span></span>

[<span data-ttu-id="22762-128">추가-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="22762-128">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="22762-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="22762-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="22762-130">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="22762-130">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="22762-131">새로운 AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="22762-131">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="22762-132">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="22762-132">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


