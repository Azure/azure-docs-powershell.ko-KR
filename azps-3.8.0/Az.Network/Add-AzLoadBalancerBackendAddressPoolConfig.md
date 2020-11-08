---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: a1e0f8abdc8951155ab56b85f516145c9b6b1d1a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042069"
---
# <span data-ttu-id="1bc84-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1bc84-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="1bc84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bc84-102">SYNOPSIS</span></span>
<span data-ttu-id="1bc84-103">부하 분산 장치에 백 엔드 주소 풀 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bc84-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="1bc84-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1bc84-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bc84-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1bc84-105">DESCRIPTION</span></span>
<span data-ttu-id="1bc84-106">**추가-AzLoadBalancerBackend** Cmdlet은 Azure 부하 분산 장치에 백 엔드 주소 풀을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bc84-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="1bc84-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1bc84-107">EXAMPLES</span></span>

### <span data-ttu-id="1bc84-108">예제 1 부하 분산 장치에 백 엔드 주소 풀 구성 추가</span><span class="sxs-lookup"><span data-stu-id="1bc84-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="1bc84-109">이 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져오고 BackendAddressPool02 이라는 이름의 백엔드 주소 풀을 MyLoadBalancer에 추가한 다음 **Set-AzLoadBalancer** cmdlet을 사용 하 여 myloadbalancer를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bc84-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="1bc84-110">변수</span><span class="sxs-lookup"><span data-stu-id="1bc84-110">PARAMETERS</span></span>

### <span data-ttu-id="1bc84-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bc84-111">-DefaultProfile</span></span>
<span data-ttu-id="1bc84-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1bc84-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bc84-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1bc84-113">-LoadBalancer</span></span>
<span data-ttu-id="1bc84-114">**LoadBalancer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bc84-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="1bc84-115">-이름</span><span class="sxs-lookup"><span data-stu-id="1bc84-115">-Name</span></span>
<span data-ttu-id="1bc84-116">추가할 백 엔드 주소 풀 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bc84-116">Specifies the name of the backend address pool configuration to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bc84-117">-확인</span><span class="sxs-lookup"><span data-stu-id="1bc84-117">-Confirm</span></span>
<span data-ttu-id="1bc84-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bc84-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bc84-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bc84-119">-WhatIf</span></span>
<span data-ttu-id="1bc84-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1bc84-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1bc84-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1bc84-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bc84-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bc84-122">CommonParameters</span></span>
<span data-ttu-id="1bc84-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bc84-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bc84-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bc84-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bc84-125">입력</span><span class="sxs-lookup"><span data-stu-id="1bc84-125">INPUTS</span></span>

### <span data-ttu-id="1bc84-126">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1bc84-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1bc84-127">출력</span><span class="sxs-lookup"><span data-stu-id="1bc84-127">OUTPUTS</span></span>

### <span data-ttu-id="1bc84-128">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1bc84-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1bc84-129">상속자</span><span class="sxs-lookup"><span data-stu-id="1bc84-129">NOTES</span></span>

## <span data-ttu-id="1bc84-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1bc84-130">RELATED LINKS</span></span>

[<span data-ttu-id="1bc84-131">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1bc84-131">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="1bc84-132">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1bc84-132">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="1bc84-133">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1bc84-133">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="1bc84-134">새로운 AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1bc84-134">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="1bc84-135">제거-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1bc84-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


