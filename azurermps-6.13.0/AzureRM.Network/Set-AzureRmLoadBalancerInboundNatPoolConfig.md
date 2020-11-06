---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 3d2110b4d8f4caf75751745ef996cb18094ae7e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534228"
---
# <span data-ttu-id="7b13f-101">Set-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7b13f-101">Set-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="7b13f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b13f-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b13f-103">구문과</span><span class="sxs-lookup"><span data-stu-id="7b13f-103">SYNTAX</span></span>

### <span data-ttu-id="7b13f-104">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="7b13f-104">SetByResource (Default)</span></span>
```
Set-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b13f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7b13f-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b13f-106">설명은</span><span class="sxs-lookup"><span data-stu-id="7b13f-106">DESCRIPTION</span></span>

## <span data-ttu-id="7b13f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7b13f-107">EXAMPLES</span></span>

### <span data-ttu-id="7b13f-108">1: 설정</span><span class="sxs-lookup"><span data-stu-id="7b13f-108">1: Set</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -LoadBalancer $slb
PS C:\> Set-AzureRmLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -LoadBalancer $slb -FrontendIpConfigurationId $inboundNatPoolConfig.FrontendIPConfiguration -Protocol TCP -FrontendPortRangeStart 2001 -FrontendPortRangeEnd 3000 -BackendPort 2001
```

## <span data-ttu-id="7b13f-109">변수</span><span class="sxs-lookup"><span data-stu-id="7b13f-109">PARAMETERS</span></span>

### <span data-ttu-id="7b13f-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="7b13f-110">-BackendPort</span></span>
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

### <span data-ttu-id="7b13f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b13f-111">-DefaultProfile</span></span>
<span data-ttu-id="7b13f-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b13f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b13f-113">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="7b13f-113">-EnableFloatingIP</span></span>
<span data-ttu-id="7b13f-114">SQL AlwaysOn 가용성 그룹을 구성 하는 데 필요한 부동 IP 접근 권한 값에 대 한 가상 컴퓨터의 끝점을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b13f-114">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="7b13f-115">SQL server에서 SQL AlwaysOn 가용성 그룹을 사용 하는 경우이 설정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b13f-115">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="7b13f-116">끝점을 만든 후에는이 설정을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7b13f-116">This setting can't be changed after you create the endpoint.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b13f-117">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="7b13f-117">-EnableTcpReset</span></span>
<span data-ttu-id="7b13f-118">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b13f-118">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="7b13f-119">이 요소는 프로토콜이 TCP로 설정 된 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7b13f-119">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b13f-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b13f-120">-FrontendIpConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b13f-121">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7b13f-121">-FrontendIpConfigurationId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b13f-122">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="7b13f-122">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="7b13f-123">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="7b13f-123">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="7b13f-124">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="7b13f-124">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="7b13f-125">TCP 유휴 연결에 대 한 제한 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="7b13f-125">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="7b13f-126">값을 4 ~ 30 분 사이로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b13f-126">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="7b13f-127">기본값은 4 분입니다.</span><span class="sxs-lookup"><span data-stu-id="7b13f-127">The default value is 4 minutes.</span></span> <span data-ttu-id="7b13f-128">이 요소는 프로토콜이 TCP로 설정 된 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7b13f-128">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b13f-129">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b13f-129">-LoadBalancer</span></span>
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

### <span data-ttu-id="7b13f-130">-이름</span><span class="sxs-lookup"><span data-stu-id="7b13f-130">-Name</span></span>
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

### <span data-ttu-id="7b13f-131">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="7b13f-131">-Protocol</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b13f-132">-확인</span><span class="sxs-lookup"><span data-stu-id="7b13f-132">-Confirm</span></span>
<span data-ttu-id="7b13f-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b13f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b13f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b13f-134">-WhatIf</span></span>
<span data-ttu-id="7b13f-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7b13f-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b13f-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b13f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b13f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b13f-137">CommonParameters</span></span>
<span data-ttu-id="7b13f-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b13f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b13f-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b13f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b13f-140">입력</span><span class="sxs-lookup"><span data-stu-id="7b13f-140">INPUTS</span></span>

### <span data-ttu-id="7b13f-141">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b13f-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="7b13f-142">매개 변수: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7b13f-142">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="7b13f-143">출력</span><span class="sxs-lookup"><span data-stu-id="7b13f-143">OUTPUTS</span></span>

### <span data-ttu-id="7b13f-144">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b13f-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7b13f-145">상속자</span><span class="sxs-lookup"><span data-stu-id="7b13f-145">NOTES</span></span>

## <span data-ttu-id="7b13f-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b13f-146">RELATED LINKS</span></span>

[<span data-ttu-id="7b13f-147">추가-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7b13f-147">Add-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="7b13f-148">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7b13f-148">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="7b13f-149">새로운 AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7b13f-149">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./New-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="7b13f-150">제거-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7b13f-150">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatPoolConfig.md)


