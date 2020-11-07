---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: b9782d56fb18f0f00c52e9ff37ef0d62a609f980
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875339"
---
# <span data-ttu-id="dde02-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dde02-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="dde02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dde02-102">SYNOPSIS</span></span>
<span data-ttu-id="dde02-103">부하 분산 장치에서 프런트 엔드 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde02-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="dde02-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dde02-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dde02-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dde02-105">DESCRIPTION</span></span>
<span data-ttu-id="dde02-106">**AzLoadBalancerFrontendIpConfig** Cmdlet은 Azure 부하 분산 장치에서 프런트 엔드 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde02-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="dde02-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dde02-107">EXAMPLES</span></span>

### <span data-ttu-id="dde02-108">예제 1: 부하 분산 장치에서 프런트 엔드 IP 구성 제거</span><span class="sxs-lookup"><span data-stu-id="dde02-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="dde02-109">첫 번째 명령은 제거 하려는 프런트 엔드 IP 구성과 연결 된 부하 분산을 가져온 다음 $loadbalancer 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde02-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="dde02-110">두 번째 명령은 $loadbalancer의 부하 분산 장치에서 연결 된 프런트 엔드 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde02-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="dde02-111">변수</span><span class="sxs-lookup"><span data-stu-id="dde02-111">PARAMETERS</span></span>

### <span data-ttu-id="dde02-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dde02-112">-DefaultProfile</span></span>
<span data-ttu-id="dde02-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dde02-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dde02-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dde02-114">-LoadBalancer</span></span>
<span data-ttu-id="dde02-115">제거할 프런트 엔드 IP 구성을 포함 하는 부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde02-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="dde02-116">-이름</span><span class="sxs-lookup"><span data-stu-id="dde02-116">-Name</span></span>
<span data-ttu-id="dde02-117">제거할 프런트 엔드 IP 주소 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde02-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="dde02-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dde02-118">CommonParameters</span></span>
<span data-ttu-id="dde02-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde02-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dde02-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dde02-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dde02-121">입력</span><span class="sxs-lookup"><span data-stu-id="dde02-121">INPUTS</span></span>

### <span data-ttu-id="dde02-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dde02-122">PSLoadBalancer</span></span>
<span data-ttu-id="dde02-123">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde02-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="dde02-124">출력</span><span class="sxs-lookup"><span data-stu-id="dde02-124">OUTPUTS</span></span>

### <span data-ttu-id="dde02-125">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dde02-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="dde02-126">상속자</span><span class="sxs-lookup"><span data-stu-id="dde02-126">NOTES</span></span>

## <span data-ttu-id="dde02-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dde02-127">RELATED LINKS</span></span>

[<span data-ttu-id="dde02-128">추가-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dde02-128">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="dde02-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dde02-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="dde02-130">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dde02-130">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="dde02-131">새로운 AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dde02-131">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="dde02-132">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dde02-132">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


