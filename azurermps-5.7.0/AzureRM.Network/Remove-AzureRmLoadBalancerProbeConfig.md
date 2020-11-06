---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 9840476e64c78293b747f96d1a689a3ce5099bff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526759"
---
# <span data-ttu-id="16491-101">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="16491-101">Remove-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="16491-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16491-102">SYNOPSIS</span></span>
<span data-ttu-id="16491-103">부하 분산 장치에서 프로브 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="16491-103">Removes a probe configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16491-104">구문과</span><span class="sxs-lookup"><span data-stu-id="16491-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16491-105">설명은</span><span class="sxs-lookup"><span data-stu-id="16491-105">DESCRIPTION</span></span>
<span data-ttu-id="16491-106">**AzureRmLoadBalancerProbeConfig** cmdlet은 부하 분산 장치에서 프로브 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="16491-106">The **Remove-AzureRmLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="16491-107">예제의</span><span class="sxs-lookup"><span data-stu-id="16491-107">EXAMPLES</span></span>

### <span data-ttu-id="16491-108">예제 1: 부하 분산 장치에서 프로브 구성 제거</span><span class="sxs-lookup"><span data-stu-id="16491-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="16491-109">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음 $loadbalancer 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="16491-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="16491-110">두 번째 명령은 $loadbalancer의 부하 분산 장치에서 MyProbe 구성을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="16491-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="16491-111">변수</span><span class="sxs-lookup"><span data-stu-id="16491-111">PARAMETERS</span></span>

### <span data-ttu-id="16491-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16491-112">-DefaultProfile</span></span>
<span data-ttu-id="16491-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16491-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16491-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="16491-114">-LoadBalancer</span></span>
<span data-ttu-id="16491-115">이 cmdlet이 제거 하는 프로브 구성을 포함 하는 부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16491-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="16491-116">-이름</span><span class="sxs-lookup"><span data-stu-id="16491-116">-Name</span></span>
<span data-ttu-id="16491-117">이 cmdlet이 제거 하는 프로브 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16491-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="16491-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16491-118">CommonParameters</span></span>
<span data-ttu-id="16491-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="16491-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16491-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16491-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16491-121">입력</span><span class="sxs-lookup"><span data-stu-id="16491-121">INPUTS</span></span>

### <span data-ttu-id="16491-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="16491-122">PSLoadBalancer</span></span>
<span data-ttu-id="16491-123">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="16491-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="16491-124">출력</span><span class="sxs-lookup"><span data-stu-id="16491-124">OUTPUTS</span></span>

### <span data-ttu-id="16491-125">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="16491-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="16491-126">상속자</span><span class="sxs-lookup"><span data-stu-id="16491-126">NOTES</span></span>

## <span data-ttu-id="16491-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16491-127">RELATED LINKS</span></span>

[<span data-ttu-id="16491-128">추가-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="16491-128">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="16491-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="16491-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="16491-130">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="16491-130">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="16491-131">새로운 AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="16491-131">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="16491-132">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="16491-132">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


