---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: b320d8d938264700fdde320cad5844325f66b938
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870693"
---
# <span data-ttu-id="f7ab4-101">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f7ab4-101">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="f7ab4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7ab4-102">SYNOPSIS</span></span>
<span data-ttu-id="f7ab4-103">부하 분산 장치에 대 한 백 엔드 주소 풀 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f7ab4-103">Gets a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="f7ab4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f7ab4-104">SYNTAX</span></span>

```
Get-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7ab4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f7ab4-105">DESCRIPTION</span></span>
<span data-ttu-id="f7ab4-106">**AzLoadBalancerBackendAddressPoolConfig** cmdlet은 단일 백엔드 주소 풀 또는 부하 분산 장치 내의 백엔드 주소 풀 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f7ab4-106">The **Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="f7ab4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f7ab4-107">EXAMPLES</span></span>

### <span data-ttu-id="f7ab4-108">예제 1: 백 엔드 주소 풀 가져오기</span><span class="sxs-lookup"><span data-stu-id="f7ab4-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="f7ab4-109">첫 번째 명령은 Myloadbalancer 이라는 리소스 그룹에서 MyLoadBalancer 라는 기존 부하 분산 장치를 가져온 다음이를 $loadbalancer 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ab4-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="f7ab4-110">두 번째 명령은 $loadbalancer의 부하 분산 장치에 대 한 BackendAddressPool02 이라는 관련 백엔드 주소 풀 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f7ab4-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="f7ab4-111">변수</span><span class="sxs-lookup"><span data-stu-id="f7ab4-111">PARAMETERS</span></span>

### <span data-ttu-id="f7ab4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7ab4-112">-DefaultProfile</span></span>
<span data-ttu-id="f7ab4-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f7ab4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7ab4-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f7ab4-114">-LoadBalancer</span></span>
<span data-ttu-id="f7ab4-115">가져올 백 엔드 주소 풀과 연결 된 부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ab4-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

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

### <span data-ttu-id="f7ab4-116">-이름</span><span class="sxs-lookup"><span data-stu-id="f7ab4-116">-Name</span></span>
<span data-ttu-id="f7ab4-117">가져올 백 엔드 주소 풀이 포함 된 부하 분산 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ab4-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="f7ab4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7ab4-118">CommonParameters</span></span>
<span data-ttu-id="f7ab4-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7ab4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7ab4-120">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f7ab4-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7ab4-121">입력</span><span class="sxs-lookup"><span data-stu-id="f7ab4-121">INPUTS</span></span>

### <span data-ttu-id="f7ab4-122">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f7ab4-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f7ab4-123">출력</span><span class="sxs-lookup"><span data-stu-id="f7ab4-123">OUTPUTS</span></span>

### <span data-ttu-id="f7ab4-124">PSBackendAddressPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f7ab4-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="f7ab4-125">상속자</span><span class="sxs-lookup"><span data-stu-id="f7ab4-125">NOTES</span></span>

## <span data-ttu-id="f7ab4-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f7ab4-126">RELATED LINKS</span></span>

[<span data-ttu-id="f7ab4-127">추가-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f7ab4-127">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="f7ab4-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f7ab4-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f7ab4-129">새로운 AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f7ab4-129">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="f7ab4-130">제거-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f7ab4-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


