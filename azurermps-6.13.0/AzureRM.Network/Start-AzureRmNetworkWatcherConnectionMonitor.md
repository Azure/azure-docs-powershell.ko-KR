---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 7c32c58167336fc032e543261e237430de36653c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531378"
---
# <span data-ttu-id="3d2f2-101">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d2f2-101">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="3d2f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d2f2-102">SYNOPSIS</span></span>
<span data-ttu-id="3d2f2-103">연결 모니터 시작</span><span class="sxs-lookup"><span data-stu-id="3d2f2-103">Start a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d2f2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3d2f2-104">SYNTAX</span></span>

### <span data-ttu-id="3d2f2-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="3d2f2-105">SetByName (Default)</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d2f2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3d2f2-106">SetByResource</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d2f2-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3d2f2-107">SetByLocation</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d2f2-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3d2f2-108">SetByResourceId</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d2f2-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="3d2f2-109">SetByInputObject</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d2f2-110">설명은</span><span class="sxs-lookup"><span data-stu-id="3d2f2-110">DESCRIPTION</span></span>
<span data-ttu-id="3d2f2-111">Start-AzureRmNetworkWatcherConnectionMonitor cmdlet은 지정 된 연결 모니터를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d2f2-111">The Start-AzureRmNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="3d2f2-112">예제의</span><span class="sxs-lookup"><span data-stu-id="3d2f2-112">EXAMPLES</span></span>

### <span data-ttu-id="3d2f2-113">예제 1: 연결 모니터 시작</span><span class="sxs-lookup"><span data-stu-id="3d2f2-113">Example 1: Start a connection monitor</span></span>
```
PS C:\> Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="3d2f2-114">이 예제에서는 이름 및 네트워크 감시자에 의해 지정 된 연결 모니터를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d2f2-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="3d2f2-115">변수</span><span class="sxs-lookup"><span data-stu-id="3d2f2-115">PARAMETERS</span></span>

### <span data-ttu-id="3d2f2-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d2f2-116">-AsJob</span></span>
<span data-ttu-id="3d2f2-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3d2f2-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d2f2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d2f2-118">-DefaultProfile</span></span>
<span data-ttu-id="3d2f2-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3d2f2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d2f2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d2f2-120">-InputObject</span></span>
<span data-ttu-id="3d2f2-121">연결 모니터 개체</span><span class="sxs-lookup"><span data-stu-id="3d2f2-121">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d2f2-122">-위치</span><span class="sxs-lookup"><span data-stu-id="3d2f2-122">-Location</span></span>
<span data-ttu-id="3d2f2-123">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="3d2f2-123">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d2f2-124">-이름</span><span class="sxs-lookup"><span data-stu-id="3d2f2-124">-Name</span></span>
<span data-ttu-id="3d2f2-125">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d2f2-125">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d2f2-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d2f2-126">-NetworkWatcher</span></span>
<span data-ttu-id="3d2f2-127">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="3d2f2-127">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d2f2-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3d2f2-128">-NetworkWatcherName</span></span>
<span data-ttu-id="3d2f2-129">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d2f2-129">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d2f2-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d2f2-130">-PassThru</span></span>
<span data-ttu-id="3d2f2-131">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="3d2f2-131">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d2f2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d2f2-132">-ResourceGroupName</span></span>
<span data-ttu-id="3d2f2-133">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d2f2-133">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d2f2-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d2f2-134">-ResourceId</span></span>
<span data-ttu-id="3d2f2-135">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3d2f2-135">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d2f2-136">-확인</span><span class="sxs-lookup"><span data-stu-id="3d2f2-136">-Confirm</span></span>
<span data-ttu-id="3d2f2-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d2f2-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d2f2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d2f2-138">-WhatIf</span></span>
<span data-ttu-id="3d2f2-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3d2f2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d2f2-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d2f2-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d2f2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d2f2-141">CommonParameters</span></span>
<span data-ttu-id="3d2f2-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d2f2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d2f2-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d2f2-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d2f2-144">입력</span><span class="sxs-lookup"><span data-stu-id="3d2f2-144">INPUTS</span></span>

### <span data-ttu-id="3d2f2-145">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d2f2-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="3d2f2-146">매개 변수: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3d2f2-146">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="3d2f2-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3d2f2-147">System.String</span></span>

### <span data-ttu-id="3d2f2-148">Microsoft. 네트워크 모델. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="3d2f2-148">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="3d2f2-149">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3d2f2-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="3d2f2-150">출력</span><span class="sxs-lookup"><span data-stu-id="3d2f2-150">OUTPUTS</span></span>

### <span data-ttu-id="3d2f2-151">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="3d2f2-151">System.Boolean</span></span>

## <span data-ttu-id="3d2f2-152">상속자</span><span class="sxs-lookup"><span data-stu-id="3d2f2-152">NOTES</span></span>
<span data-ttu-id="3d2f2-153">키워드: azure, azurerm, arm, 리소스, 연결, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결 모니터</span><span class="sxs-lookup"><span data-stu-id="3d2f2-153">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="3d2f2-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d2f2-154">RELATED LINKS</span></span>

[<span data-ttu-id="3d2f2-155">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d2f2-155">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="3d2f2-156">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d2f2-156">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="3d2f2-157">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d2f2-157">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="3d2f2-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3d2f2-158">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="3d2f2-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3d2f2-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="3d2f2-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3d2f2-160">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="3d2f2-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3d2f2-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="3d2f2-162">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d2f2-162">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="3d2f2-163">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3d2f2-163">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="3d2f2-164">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d2f2-164">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="3d2f2-165">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d2f2-165">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="3d2f2-166">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d2f2-166">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="3d2f2-167">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d2f2-167">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="3d2f2-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="3d2f2-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="3d2f2-169">제거-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d2f2-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="3d2f2-170">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d2f2-170">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="3d2f2-171">중지-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d2f2-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="3d2f2-172">새로운 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d2f2-172">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="3d2f2-173">새로운 AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d2f2-173">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="3d2f2-174">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3d2f2-174">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="3d2f2-175">테스트-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="3d2f2-175">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="3d2f2-176">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3d2f2-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="3d2f2-177">시작-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d2f2-177">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="3d2f2-178">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="3d2f2-178">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="3d2f2-179">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3d2f2-179">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="3d2f2-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="3d2f2-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="3d2f2-181">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="3d2f2-181">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
