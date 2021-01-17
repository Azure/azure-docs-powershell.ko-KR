---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 39e388fbdb809f136942749a0d0585189155e32b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371330"
---
# <span data-ttu-id="e2a9c-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e2a9c-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="e2a9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2a9c-102">SYNOPSIS</span></span>
<span data-ttu-id="e2a9c-103">백end 주소 풀 구성을 부하 균형 조정에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a9c-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="e2a9c-104">구문</span><span class="sxs-lookup"><span data-stu-id="e2a9c-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2a9c-105">설명</span><span class="sxs-lookup"><span data-stu-id="e2a9c-105">DESCRIPTION</span></span>
<span data-ttu-id="e2a9c-106">**Add-AzLoadBalancerBackend** cmdlet은 Azure Load Balancer에 백end 주소 풀을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a9c-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="e2a9c-107">예제</span><span class="sxs-lookup"><span data-stu-id="e2a9c-107">EXAMPLES</span></span>

### <span data-ttu-id="e2a9c-108">예제 1: 부하 균형 조정에 백end 주소 풀 구성 추가</span><span class="sxs-lookup"><span data-stu-id="e2a9c-108">Example 1: Add a backend address pool configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="e2a9c-109">이 명령은 MyLoadBalancer라는 부하 분산 기능을 다운로드하고 BackendAddressPool02라는 백end 주소 풀을 MyLoadBalancer에 추가한 다음 **Set-AzLoadBalancer** cmdlet을 사용하여 MyLoadBalancer를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a9c-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="e2a9c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2a9c-110">PARAMETERS</span></span>

### <span data-ttu-id="e2a9c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2a9c-111">-DefaultProfile</span></span>
<span data-ttu-id="e2a9c-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2a9c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2a9c-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e2a9c-113">-LoadBalancer</span></span>
<span data-ttu-id="e2a9c-114">**LoadBalancer** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a9c-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="e2a9c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e2a9c-115">-Name</span></span>
<span data-ttu-id="e2a9c-116">추가할 백end 주소 풀 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a9c-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="e2a9c-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2a9c-117">-Confirm</span></span>
<span data-ttu-id="e2a9c-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2a9c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2a9c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2a9c-119">-WhatIf</span></span>
<span data-ttu-id="e2a9c-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e2a9c-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2a9c-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2a9c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2a9c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2a9c-122">CommonParameters</span></span>
<span data-ttu-id="e2a9c-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a9c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2a9c-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e2a9c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2a9c-125">입력</span><span class="sxs-lookup"><span data-stu-id="e2a9c-125">INPUTS</span></span>

### <span data-ttu-id="e2a9c-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e2a9c-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e2a9c-127">출력</span><span class="sxs-lookup"><span data-stu-id="e2a9c-127">OUTPUTS</span></span>

### <span data-ttu-id="e2a9c-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e2a9c-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e2a9c-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e2a9c-129">NOTES</span></span>

## <span data-ttu-id="e2a9c-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2a9c-130">RELATED LINKS</span></span>

[<span data-ttu-id="e2a9c-131">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e2a9c-131">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="e2a9c-132">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e2a9c-132">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="e2a9c-133">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e2a9c-133">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="e2a9c-134">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e2a9c-134">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="e2a9c-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e2a9c-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


