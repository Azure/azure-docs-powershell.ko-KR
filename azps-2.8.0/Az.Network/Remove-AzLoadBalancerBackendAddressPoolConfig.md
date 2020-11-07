---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: ba4251615bd732526ca88f085cf2c7f2d2bf284d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871246"
---
# <span data-ttu-id="8dcf0-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8dcf0-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="8dcf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dcf0-102">SYNOPSIS</span></span>
<span data-ttu-id="8dcf0-103">부하 분산 장치에서 백 엔드 주소 풀 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="8dcf0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8dcf0-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dcf0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8dcf0-105">DESCRIPTION</span></span>
<span data-ttu-id="8dcf0-106">**AzLoadBalancerBackendAddressPoolConfig** cmdlet은 부하 분산 장치에서 백 엔드 주소 풀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="8dcf0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8dcf0-107">EXAMPLES</span></span>

### <span data-ttu-id="8dcf0-108">예제 1: 부하 분산 장치에서 백 엔드 주소 풀 구성 제거</span><span class="sxs-lookup"><span data-stu-id="8dcf0-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="8dcf0-109">이 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져오고 **AzLoadBalancerBackendAddressPoolConfig** 에 전달 하 여 Myloadbalancer의 BackendAddressPool02 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="8dcf0-110">마지막으로, Set-AzLoadBalancer cmdlet은 MyLoadBalancer를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="8dcf0-111">백 엔드 주소 풀 구성은 반드시 있어야 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="8dcf0-112">변수</span><span class="sxs-lookup"><span data-stu-id="8dcf0-112">PARAMETERS</span></span>

### <span data-ttu-id="8dcf0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dcf0-113">-DefaultProfile</span></span>
<span data-ttu-id="8dcf0-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8dcf0-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8dcf0-115">-LoadBalancer</span></span>
<span data-ttu-id="8dcf0-116">제거할 백 엔드 주소 풀을 포함 하는 부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="8dcf0-117">-이름</span><span class="sxs-lookup"><span data-stu-id="8dcf0-117">-Name</span></span>
<span data-ttu-id="8dcf0-118">이 cmdlet이 제거 하는 백 엔드 주소 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8dcf0-119">-확인</span><span class="sxs-lookup"><span data-stu-id="8dcf0-119">-Confirm</span></span>
<span data-ttu-id="8dcf0-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dcf0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dcf0-121">-WhatIf</span></span>
<span data-ttu-id="8dcf0-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8dcf0-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dcf0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dcf0-124">CommonParameters</span></span>
<span data-ttu-id="8dcf0-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dcf0-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dcf0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dcf0-127">입력</span><span class="sxs-lookup"><span data-stu-id="8dcf0-127">INPUTS</span></span>

### <span data-ttu-id="8dcf0-128">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8dcf0-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8dcf0-129">출력</span><span class="sxs-lookup"><span data-stu-id="8dcf0-129">OUTPUTS</span></span>

### <span data-ttu-id="8dcf0-130">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8dcf0-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8dcf0-131">상속자</span><span class="sxs-lookup"><span data-stu-id="8dcf0-131">NOTES</span></span>

## <span data-ttu-id="8dcf0-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8dcf0-132">RELATED LINKS</span></span>

[<span data-ttu-id="8dcf0-133">추가-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8dcf0-133">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="8dcf0-134">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8dcf0-134">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="8dcf0-135">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8dcf0-135">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="8dcf0-136">새로운 AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8dcf0-136">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


