---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: ee831cf3f2b6441bde55dc458d6b9af33f4b42e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525507"
---
# <span data-ttu-id="9acb0-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9acb0-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="9acb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9acb0-102">SYNOPSIS</span></span>
<span data-ttu-id="9acb0-103">부하 분산 장치에서 인바운드 NAT 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9acb0-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9acb0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9acb0-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9acb0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9acb0-105">DESCRIPTION</span></span>
<span data-ttu-id="9acb0-106">**AzureRmLoadBalancerInboundNatRuleConfig** Cmdlet은 Azure 부하 분산 장치에서 인바운드 NAT (network address translation) 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9acb0-106">The **Remove-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="9acb0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9acb0-107">EXAMPLES</span></span>

### <span data-ttu-id="9acb0-108">1: Azure 부하 분산 장치에서 인바운드 NAT 규칙 삭제</span><span class="sxs-lookup"><span data-stu-id="9acb0-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzureRmLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzureRmLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="9acb0-109">첫 번째 명령은 이미 "mylb" 라는 기존 부하 분산 장치를 로드 하 여 변수 $load 조정기에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9acb0-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="9acb0-110">두 번째 명령은이 부하 분산 장치에 연결 된 인바운드 NAT 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9acb0-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="9acb0-111">변수</span><span class="sxs-lookup"><span data-stu-id="9acb0-111">PARAMETERS</span></span>

### <span data-ttu-id="9acb0-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9acb0-112">-LoadBalancer</span></span>
<span data-ttu-id="9acb0-113">이 cmdlet이 제거 하는 인바운드 NAT 규칙 구성을 포함 하는 **LoadBalancer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9acb0-113">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9acb0-114">-이름</span><span class="sxs-lookup"><span data-stu-id="9acb0-114">-Name</span></span>
<span data-ttu-id="9acb0-115">이 cmdlet이 제거 하는 인바운드 NAT 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9acb0-115">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9acb0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9acb0-116">-DefaultProfile</span></span>
<span data-ttu-id="9acb0-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9acb0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9acb0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9acb0-118">CommonParameters</span></span>
<span data-ttu-id="9acb0-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9acb0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9acb0-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9acb0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9acb0-121">입력</span><span class="sxs-lookup"><span data-stu-id="9acb0-121">INPUTS</span></span>

### <span data-ttu-id="9acb0-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9acb0-122">PSLoadBalancer</span></span>
<span data-ttu-id="9acb0-123">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9acb0-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="9acb0-124">출력</span><span class="sxs-lookup"><span data-stu-id="9acb0-124">OUTPUTS</span></span>

### <span data-ttu-id="9acb0-125">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9acb0-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9acb0-126">상속자</span><span class="sxs-lookup"><span data-stu-id="9acb0-126">NOTES</span></span>

## <span data-ttu-id="9acb0-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9acb0-127">RELATED LINKS</span></span>

[<span data-ttu-id="9acb0-128">추가-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9acb0-128">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9acb0-129">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9acb0-129">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9acb0-130">새로운 AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9acb0-130">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9acb0-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9acb0-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)

