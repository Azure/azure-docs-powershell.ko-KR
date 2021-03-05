---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 08644bd8b9846b0eb7d647b3df9c12008070c059
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993687"
---
# <span data-ttu-id="c310e-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c310e-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="c310e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c310e-102">SYNOPSIS</span></span>
<span data-ttu-id="c310e-103">부하 균형기에서 백던드 주소 풀 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c310e-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="c310e-104">구문</span><span class="sxs-lookup"><span data-stu-id="c310e-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c310e-105">설명</span><span class="sxs-lookup"><span data-stu-id="c310e-105">DESCRIPTION</span></span>
<span data-ttu-id="c310e-106">**Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet은 부하 분산기에서 백end 주소 풀을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c310e-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="c310e-107">예제</span><span class="sxs-lookup"><span data-stu-id="c310e-107">EXAMPLES</span></span>

### <span data-ttu-id="c310e-108">예제 1: 부하 균형 조정기에서 백던드 주소 풀 구성 제거</span><span class="sxs-lookup"><span data-stu-id="c310e-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="c310e-109">이 명령은 MyLoadBalancer라는 부하 분산기를 얻게 하여 **Remove-AzLoadBalancerBackendAddressPoolConfig로** 전달하여 MyLoadBalancer에서 BackendAddressPool02 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c310e-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig**, which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="c310e-110">마지막으로, Set-AzLoadBalancer cmdlet은 MyLoadBalancer를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c310e-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="c310e-111">삭제하려면 먼저 백던드 주소 풀 구성이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c310e-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="c310e-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c310e-112">PARAMETERS</span></span>

### <span data-ttu-id="c310e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c310e-113">-DefaultProfile</span></span>
<span data-ttu-id="c310e-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c310e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c310e-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c310e-115">-LoadBalancer</span></span>
<span data-ttu-id="c310e-116">제거할 백던드 주소 풀을 포함하는 부하 균형 조정기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c310e-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="c310e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c310e-117">-Name</span></span>
<span data-ttu-id="c310e-118">이 cmdlet이 제거하는 백던드 주소 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c310e-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c310e-119">-확인</span><span class="sxs-lookup"><span data-stu-id="c310e-119">-Confirm</span></span>
<span data-ttu-id="c310e-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c310e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c310e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c310e-121">-WhatIf</span></span>
<span data-ttu-id="c310e-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c310e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c310e-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c310e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c310e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c310e-124">CommonParameters</span></span>
<span data-ttu-id="c310e-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c310e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c310e-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c310e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c310e-127">입력</span><span class="sxs-lookup"><span data-stu-id="c310e-127">INPUTS</span></span>

### <span data-ttu-id="c310e-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c310e-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c310e-129">출력</span><span class="sxs-lookup"><span data-stu-id="c310e-129">OUTPUTS</span></span>

### <span data-ttu-id="c310e-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c310e-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c310e-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c310e-131">NOTES</span></span>

## <span data-ttu-id="c310e-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c310e-132">RELATED LINKS</span></span>

[<span data-ttu-id="c310e-133">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c310e-133">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="c310e-134">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c310e-134">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="c310e-135">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c310e-135">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="c310e-136">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c310e-136">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


