---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: bde16a6f3ecd68307574ae5eac7760a177101cc1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342722"
---
# <span data-ttu-id="27b37-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="27b37-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="27b37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27b37-102">SYNOPSIS</span></span>
<span data-ttu-id="27b37-103">부하 균형 조정기에서 프런트 엔드 IP 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="27b37-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="27b37-104">구문</span><span class="sxs-lookup"><span data-stu-id="27b37-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27b37-105">설명</span><span class="sxs-lookup"><span data-stu-id="27b37-105">DESCRIPTION</span></span>
<span data-ttu-id="27b37-106">**Remove-AzLoadBalancerFrontendIpConfig** cmdlet은 Azure Load Balancer에서 프런트 엔드 IP 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="27b37-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="27b37-107">예제</span><span class="sxs-lookup"><span data-stu-id="27b37-107">EXAMPLES</span></span>

### <span data-ttu-id="27b37-108">예제 1: 부하 균형 조정기에서 프런트 엔드 IP 구성 제거</span><span class="sxs-lookup"><span data-stu-id="27b37-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="27b37-109">첫 번째 명령은 제거하려는 프런트 엔드 IP 구성과 연결된 부하 $loadbalancer 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="27b37-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="27b37-110">두 번째 명령은 연결된 프런트 엔드 IP 구성을 네트워크의 부하 $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="27b37-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="27b37-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27b37-111">PARAMETERS</span></span>

### <span data-ttu-id="27b37-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27b37-112">-DefaultProfile</span></span>
<span data-ttu-id="27b37-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27b37-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27b37-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27b37-114">-LoadBalancer</span></span>
<span data-ttu-id="27b37-115">제거할 프런트 엔드 IP 구성을 포함하는 부하 균형 조정기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27b37-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="27b37-116">-Name</span><span class="sxs-lookup"><span data-stu-id="27b37-116">-Name</span></span>
<span data-ttu-id="27b37-117">제거할 프런트 엔드 IP 주소 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27b37-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="27b37-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27b37-118">-Confirm</span></span>
<span data-ttu-id="27b37-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="27b37-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27b37-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27b37-120">-WhatIf</span></span>
<span data-ttu-id="27b37-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="27b37-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27b37-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27b37-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27b37-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27b37-123">CommonParameters</span></span>
<span data-ttu-id="27b37-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="27b37-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27b37-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="27b37-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27b37-126">입력</span><span class="sxs-lookup"><span data-stu-id="27b37-126">INPUTS</span></span>

### <span data-ttu-id="27b37-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27b37-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="27b37-128">출력</span><span class="sxs-lookup"><span data-stu-id="27b37-128">OUTPUTS</span></span>

### <span data-ttu-id="27b37-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27b37-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="27b37-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="27b37-130">NOTES</span></span>

## <span data-ttu-id="27b37-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27b37-131">RELATED LINKS</span></span>

[<span data-ttu-id="27b37-132">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="27b37-132">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="27b37-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27b37-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="27b37-134">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="27b37-134">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="27b37-135">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="27b37-135">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="27b37-136">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="27b37-136">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


