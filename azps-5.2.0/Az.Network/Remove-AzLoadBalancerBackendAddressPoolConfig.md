---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 26f7e0dde825305e888d598a23af0b2fbaff81cd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331502"
---
# <span data-ttu-id="4d55a-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4d55a-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="4d55a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d55a-102">SYNOPSIS</span></span>
<span data-ttu-id="4d55a-103">부하 균형 조정기에서 백end 주소 풀 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4d55a-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="4d55a-104">구문</span><span class="sxs-lookup"><span data-stu-id="4d55a-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d55a-105">설명</span><span class="sxs-lookup"><span data-stu-id="4d55a-105">DESCRIPTION</span></span>
<span data-ttu-id="4d55a-106">**Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet은 부하 분산기에서 백end 주소 풀을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4d55a-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="4d55a-107">예제</span><span class="sxs-lookup"><span data-stu-id="4d55a-107">EXAMPLES</span></span>

### <span data-ttu-id="4d55a-108">예제 1: 부하 균형 조정기에서 백end 주소 풀 구성 제거</span><span class="sxs-lookup"><span data-stu-id="4d55a-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="4d55a-109">이 명령은 MyLoadBalancer라는 부하 분산기를 사용하여 **Remove-AzLoadBalancerBackendAddressPoolConfig에** 전달합니다. 그러면 MyLoadBalancer에서 BackendAddressPool02 구성이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d55a-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig**, which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="4d55a-110">마지막으로, Set-AzLoadBalancer cmdlet이 MyLoadBalancer를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4d55a-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="4d55a-111">삭제하려면 먼저 백end 주소 풀 구성이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d55a-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="4d55a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d55a-112">PARAMETERS</span></span>

### <span data-ttu-id="4d55a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d55a-113">-DefaultProfile</span></span>
<span data-ttu-id="4d55a-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d55a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d55a-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4d55a-115">-LoadBalancer</span></span>
<span data-ttu-id="4d55a-116">제거할 백end 주소 풀을 포함하는 부하 균형 조정기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d55a-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="4d55a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4d55a-117">-Name</span></span>
<span data-ttu-id="4d55a-118">이 cmdlet에서 제거하는 백end 주소 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d55a-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4d55a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d55a-119">-Confirm</span></span>
<span data-ttu-id="4d55a-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d55a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d55a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d55a-121">-WhatIf</span></span>
<span data-ttu-id="4d55a-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4d55a-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d55a-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4d55a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d55a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d55a-124">CommonParameters</span></span>
<span data-ttu-id="4d55a-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4d55a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d55a-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4d55a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d55a-127">입력</span><span class="sxs-lookup"><span data-stu-id="4d55a-127">INPUTS</span></span>

### <span data-ttu-id="4d55a-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4d55a-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4d55a-129">출력</span><span class="sxs-lookup"><span data-stu-id="4d55a-129">OUTPUTS</span></span>

### <span data-ttu-id="4d55a-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4d55a-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4d55a-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4d55a-131">NOTES</span></span>

## <span data-ttu-id="4d55a-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d55a-132">RELATED LINKS</span></span>

[<span data-ttu-id="4d55a-133">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4d55a-133">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="4d55a-134">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4d55a-134">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="4d55a-135">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4d55a-135">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="4d55a-136">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4d55a-136">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


