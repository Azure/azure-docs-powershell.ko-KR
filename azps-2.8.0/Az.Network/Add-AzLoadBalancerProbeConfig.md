---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 071a6db22f6788f76a6c4323c26247c070f164b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870850"
---
# <span data-ttu-id="b0082-101">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b0082-101">Add-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="b0082-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0082-102">SYNOPSIS</span></span>
<span data-ttu-id="b0082-103">부하 분산 장치에 프로브 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0082-103">Adds a probe configuration to a load balancer.</span></span>

## <span data-ttu-id="b0082-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0082-104">SYNTAX</span></span>

```
Add-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0082-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b0082-105">DESCRIPTION</span></span>
<span data-ttu-id="b0082-106">**Add-AzLoadBalancerProbeConfig** Cmdlet은 Azure 부하 분산 장치에 프로브 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0082-106">The **Add-AzLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="b0082-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b0082-107">EXAMPLES</span></span>

### <span data-ttu-id="b0082-108">예제 1 부하 분산 장치에 프로브 구성 추가</span><span class="sxs-lookup"><span data-stu-id="b0082-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzLoadBalancer
```

<span data-ttu-id="b0082-109">이 명령은 myLb 라는 로드 균형 조정기를 가져와 지정 된 프로브 구성을이에 추가한 다음 **AzLoadBalancer** cmdlet을 사용 하 여 부하 분산 장치를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0082-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="b0082-110">변수</span><span class="sxs-lookup"><span data-stu-id="b0082-110">PARAMETERS</span></span>

### <span data-ttu-id="b0082-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0082-111">-DefaultProfile</span></span>
<span data-ttu-id="b0082-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0082-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0082-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="b0082-113">-IntervalInSeconds</span></span>
<span data-ttu-id="b0082-114">부하 분산 서비스의 각 인스턴스에 대 한 프로브 사이의 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0082-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0082-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b0082-115">-LoadBalancer</span></span>
<span data-ttu-id="b0082-116">**LoadBalancer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0082-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="b0082-117">이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 프로브 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0082-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="b0082-118">-이름</span><span class="sxs-lookup"><span data-stu-id="b0082-118">-Name</span></span>
<span data-ttu-id="b0082-119">추가할 프로브 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0082-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="b0082-120">-포트</span><span class="sxs-lookup"><span data-stu-id="b0082-120">-Port</span></span>
<span data-ttu-id="b0082-121">프로브가 부하 분산 서비스에 연결할 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0082-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0082-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="b0082-122">-ProbeCount</span></span>
<span data-ttu-id="b0082-123">비정상으로 간주 되는 인스턴스에 대 한 인스턴스 별 연속 된 실패의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0082-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0082-124">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="b0082-124">-Protocol</span></span>
<span data-ttu-id="b0082-125">프로브에 사용할 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0082-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="b0082-126">이 매개 변수에 허용 되는 값은 Tcp 또는 Http입니다.</span><span class="sxs-lookup"><span data-stu-id="b0082-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0082-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="b0082-127">-RequestPath</span></span>
<span data-ttu-id="b0082-128">부하 분산 서비스에서 상태를 확인 하기 위해 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0082-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0082-129">-확인</span><span class="sxs-lookup"><span data-stu-id="b0082-129">-Confirm</span></span>
<span data-ttu-id="b0082-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0082-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0082-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0082-131">-WhatIf</span></span>
<span data-ttu-id="b0082-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b0082-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0082-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0082-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0082-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0082-134">CommonParameters</span></span>
<span data-ttu-id="b0082-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0082-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0082-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0082-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0082-137">입력</span><span class="sxs-lookup"><span data-stu-id="b0082-137">INPUTS</span></span>

### <span data-ttu-id="b0082-138">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b0082-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="b0082-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b0082-139">System.String</span></span>

### <span data-ttu-id="b0082-140">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="b0082-140">System.Int32</span></span>

## <span data-ttu-id="b0082-141">출력</span><span class="sxs-lookup"><span data-stu-id="b0082-141">OUTPUTS</span></span>

### <span data-ttu-id="b0082-142">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b0082-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b0082-143">상속자</span><span class="sxs-lookup"><span data-stu-id="b0082-143">NOTES</span></span>

## <span data-ttu-id="b0082-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0082-144">RELATED LINKS</span></span>

[<span data-ttu-id="b0082-145">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b0082-145">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="b0082-146">새로운 AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b0082-146">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="b0082-147">제거-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b0082-147">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="b0082-148">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b0082-148">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="b0082-149">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b0082-149">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


