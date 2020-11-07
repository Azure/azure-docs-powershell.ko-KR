---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
ms.openlocfilehash: 2af05b60498fc83b74c00701794dba7f1b59e6a6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882866"
---
# <span data-ttu-id="86d8b-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86d8b-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="86d8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86d8b-102">SYNOPSIS</span></span>
<span data-ttu-id="86d8b-103">부하 분산 장치에서 인바운드 NAT 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="86d8b-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86d8b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="86d8b-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86d8b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="86d8b-105">DESCRIPTION</span></span>
<span data-ttu-id="86d8b-106">**AzureRmLoadBalancerInboundNatRuleConfig** Cmdlet은 Azure 부하 분산 장치에서 인바운드 NAT (network address translation) 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="86d8b-106">The **Remove-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="86d8b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="86d8b-107">EXAMPLES</span></span>

### <span data-ttu-id="86d8b-108">1: Azure 부하 분산 장치에서 인바운드 NAT 규칙 삭제</span><span class="sxs-lookup"><span data-stu-id="86d8b-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzureRmLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzureRmLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="86d8b-109">첫 번째 명령은 이미 "mylb" 라는 기존 부하 분산 장치를 로드 하 여 변수 $load 조정기에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="86d8b-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="86d8b-110">두 번째 명령은이 부하 분산 장치에 연결 된 인바운드 NAT 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="86d8b-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="86d8b-111">변수</span><span class="sxs-lookup"><span data-stu-id="86d8b-111">PARAMETERS</span></span>

### <span data-ttu-id="86d8b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86d8b-112">-DefaultProfile</span></span>
<span data-ttu-id="86d8b-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="86d8b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86d8b-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="86d8b-114">-LoadBalancer</span></span>
<span data-ttu-id="86d8b-115">이 cmdlet이 제거 하는 인바운드 NAT 규칙 구성을 포함 하는 **LoadBalancer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86d8b-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="86d8b-116">-이름</span><span class="sxs-lookup"><span data-stu-id="86d8b-116">-Name</span></span>
<span data-ttu-id="86d8b-117">이 cmdlet이 제거 하는 인바운드 NAT 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86d8b-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="86d8b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86d8b-118">CommonParameters</span></span>
<span data-ttu-id="86d8b-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="86d8b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86d8b-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86d8b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86d8b-121">입력</span><span class="sxs-lookup"><span data-stu-id="86d8b-121">INPUTS</span></span>

### <span data-ttu-id="86d8b-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="86d8b-122">PSLoadBalancer</span></span>
<span data-ttu-id="86d8b-123">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="86d8b-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="86d8b-124">출력</span><span class="sxs-lookup"><span data-stu-id="86d8b-124">OUTPUTS</span></span>

### <span data-ttu-id="86d8b-125">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="86d8b-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="86d8b-126">상속자</span><span class="sxs-lookup"><span data-stu-id="86d8b-126">NOTES</span></span>

## <span data-ttu-id="86d8b-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86d8b-127">RELATED LINKS</span></span>

[<span data-ttu-id="86d8b-128">추가-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86d8b-128">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="86d8b-129">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86d8b-129">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="86d8b-130">새로운 AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86d8b-130">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="86d8b-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86d8b-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


