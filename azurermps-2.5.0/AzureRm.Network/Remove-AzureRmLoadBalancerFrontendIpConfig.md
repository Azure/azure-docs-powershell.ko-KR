---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: 192eb5ebfa21c97aa7043c4d4719831def08d93e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882878"
---
# <span data-ttu-id="0d926-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0d926-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="0d926-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d926-102">SYNOPSIS</span></span>
<span data-ttu-id="0d926-103">부하 분산 장치에서 프런트 엔드 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d926-103">Removes a front-end IP configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d926-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0d926-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d926-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0d926-105">DESCRIPTION</span></span>
<span data-ttu-id="0d926-106">**AzureRmLoadBalancerFrontendIpConfig** Cmdlet은 Azure 부하 분산 장치에서 프런트 엔드 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d926-106">The **Remove-AzureRmLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="0d926-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0d926-107">EXAMPLES</span></span>

### <span data-ttu-id="0d926-108">예제 1: 부하 분산 장치에서 프런트 엔드 IP 구성 제거</span><span class="sxs-lookup"><span data-stu-id="0d926-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="0d926-109">첫 번째 명령은 제거 하려는 프런트 엔드 IP 구성과 연결 된 부하 분산을 가져온 다음 $loadbalancer 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d926-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="0d926-110">두 번째 명령은 $loadbalancer의 부하 분산 장치에서 연결 된 프런트 엔드 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d926-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="0d926-111">변수</span><span class="sxs-lookup"><span data-stu-id="0d926-111">PARAMETERS</span></span>

### <span data-ttu-id="0d926-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d926-112">-DefaultProfile</span></span>
<span data-ttu-id="0d926-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d926-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d926-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0d926-114">-LoadBalancer</span></span>
<span data-ttu-id="0d926-115">제거할 프런트 엔드 IP 구성을 포함 하는 부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d926-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="0d926-116">-이름</span><span class="sxs-lookup"><span data-stu-id="0d926-116">-Name</span></span>
<span data-ttu-id="0d926-117">제거할 프런트 엔드 IP 주소 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d926-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="0d926-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d926-118">CommonParameters</span></span>
<span data-ttu-id="0d926-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d926-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d926-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d926-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d926-121">입력</span><span class="sxs-lookup"><span data-stu-id="0d926-121">INPUTS</span></span>

### <span data-ttu-id="0d926-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0d926-122">PSLoadBalancer</span></span>
<span data-ttu-id="0d926-123">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d926-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="0d926-124">출력</span><span class="sxs-lookup"><span data-stu-id="0d926-124">OUTPUTS</span></span>

### <span data-ttu-id="0d926-125">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0d926-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0d926-126">상속자</span><span class="sxs-lookup"><span data-stu-id="0d926-126">NOTES</span></span>

## <span data-ttu-id="0d926-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d926-127">RELATED LINKS</span></span>

[<span data-ttu-id="0d926-128">추가-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0d926-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="0d926-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0d926-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="0d926-130">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0d926-130">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="0d926-131">새로운 AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0d926-131">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="0d926-132">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0d926-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


