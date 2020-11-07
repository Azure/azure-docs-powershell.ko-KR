---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 01e8a41c8d8854527037c447545f3d0601d4daf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711050"
---
# <span data-ttu-id="8661f-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8661f-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="8661f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8661f-102">SYNOPSIS</span></span>
<span data-ttu-id="8661f-103">연결 모니터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8661f-103">Remove connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8661f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8661f-104">SYNTAX</span></span>

### <span data-ttu-id="8661f-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="8661f-105">SetByName (Default)</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8661f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8661f-106">SetByResource</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8661f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="8661f-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8661f-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8661f-108">SetByResourceId</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8661f-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="8661f-109">SetByInputObject</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8661f-110">설명은</span><span class="sxs-lookup"><span data-stu-id="8661f-110">DESCRIPTION</span></span>
<span data-ttu-id="8661f-111">AzureRmNetworkWatcherConnectionMonitor cmdlet은 지정 된 연결 모니터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8661f-111">The remove-AzureRmNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="8661f-112">예제의</span><span class="sxs-lookup"><span data-stu-id="8661f-112">EXAMPLES</span></span>

### <span data-ttu-id="8661f-113">예제 1: 지정 된 연결 모니터 제거</span><span class="sxs-lookup"><span data-stu-id="8661f-113">Example 1: Remove the specified connection monitor</span></span>
```
PS C:\> Remove-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="8661f-114">이 예제에서는 위치 및 이름으로 지정 된 연결 모니터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8661f-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="8661f-115">변수</span><span class="sxs-lookup"><span data-stu-id="8661f-115">PARAMETERS</span></span>

### <span data-ttu-id="8661f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8661f-116">-AsJob</span></span>
<span data-ttu-id="8661f-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8661f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8661f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8661f-118">-DefaultProfile</span></span>
<span data-ttu-id="8661f-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8661f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8661f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8661f-120">-InputObject</span></span>
<span data-ttu-id="8661f-121">연결 모니터 개체</span><span class="sxs-lookup"><span data-stu-id="8661f-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="8661f-122">-위치</span><span class="sxs-lookup"><span data-stu-id="8661f-122">-Location</span></span>
<span data-ttu-id="8661f-123">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="8661f-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="8661f-124">-이름</span><span class="sxs-lookup"><span data-stu-id="8661f-124">-Name</span></span>
<span data-ttu-id="8661f-125">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8661f-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="8661f-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8661f-126">-NetworkWatcher</span></span>
<span data-ttu-id="8661f-127">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="8661f-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="8661f-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8661f-128">-NetworkWatcherName</span></span>
<span data-ttu-id="8661f-129">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8661f-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="8661f-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8661f-130">-PassThru</span></span>
<span data-ttu-id="8661f-131">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="8661f-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8661f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8661f-132">-ResourceGroupName</span></span>
<span data-ttu-id="8661f-133">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8661f-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="8661f-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8661f-134">-ResourceId</span></span>
<span data-ttu-id="8661f-135">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8661f-135">Resource ID.</span></span>

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

### <span data-ttu-id="8661f-136">-확인</span><span class="sxs-lookup"><span data-stu-id="8661f-136">-Confirm</span></span>
<span data-ttu-id="8661f-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8661f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8661f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8661f-138">-WhatIf</span></span>
<span data-ttu-id="8661f-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8661f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8661f-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8661f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8661f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8661f-141">CommonParameters</span></span>
<span data-ttu-id="8661f-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8661f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8661f-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8661f-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8661f-144">입력</span><span class="sxs-lookup"><span data-stu-id="8661f-144">INPUTS</span></span>

### <span data-ttu-id="8661f-145">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8661f-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="8661f-146">매개 변수: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8661f-146">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="8661f-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8661f-147">System.String</span></span>

### <span data-ttu-id="8661f-148">Microsoft. 네트워크 모델. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="8661f-148">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="8661f-149">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8661f-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="8661f-150">출력</span><span class="sxs-lookup"><span data-stu-id="8661f-150">OUTPUTS</span></span>

### <span data-ttu-id="8661f-151">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8661f-151">System.Boolean</span></span>

## <span data-ttu-id="8661f-152">상속자</span><span class="sxs-lookup"><span data-stu-id="8661f-152">NOTES</span></span>
<span data-ttu-id="8661f-153">키워드: azure, azurerm, arm, 리소스, 연결, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결 모니터</span><span class="sxs-lookup"><span data-stu-id="8661f-153">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="8661f-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8661f-154">RELATED LINKS</span></span>

[<span data-ttu-id="8661f-155">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8661f-155">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="8661f-156">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8661f-156">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="8661f-157">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8661f-157">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="8661f-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8661f-158">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="8661f-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8661f-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="8661f-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8661f-160">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="8661f-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8661f-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="8661f-162">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8661f-162">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="8661f-163">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8661f-163">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="8661f-164">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8661f-164">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="8661f-165">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8661f-165">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="8661f-166">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8661f-166">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="8661f-167">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8661f-167">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="8661f-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="8661f-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="8661f-169">제거-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8661f-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="8661f-170">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8661f-170">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="8661f-171">중지-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8661f-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="8661f-172">새로운 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8661f-172">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="8661f-173">새로운 AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8661f-173">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="8661f-174">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8661f-174">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="8661f-175">테스트-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="8661f-175">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="8661f-176">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8661f-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="8661f-177">시작-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8661f-177">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="8661f-178">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="8661f-178">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="8661f-179">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8661f-179">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="8661f-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="8661f-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="8661f-181">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="8661f-181">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
