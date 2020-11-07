---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 3f380135cc6edde875c927dd9d640a10cdf14957
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703827"
---
# <span data-ttu-id="43d0b-101">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="43d0b-101">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="43d0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43d0b-102">SYNOPSIS</span></span>
<span data-ttu-id="43d0b-103">지정 된 이름 또는 연결 모니터 목록으로 연결 모니터를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="43d0b-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43d0b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="43d0b-104">SYNTAX</span></span>

### <span data-ttu-id="43d0b-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="43d0b-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43d0b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="43d0b-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43d0b-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="43d0b-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43d0b-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="43d0b-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43d0b-109">설명은</span><span class="sxs-lookup"><span data-stu-id="43d0b-109">DESCRIPTION</span></span>
<span data-ttu-id="43d0b-110">Get-AzureRmNetworkWatcherConnectionMonitor cmdlet은 지정 된 이름/resourceId를 갖는 연결 모니터 또는 지정 된 네트워크 감시자/위치에 해당 하는 연결 모니터링 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="43d0b-110">The Get-AzureRmNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="43d0b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="43d0b-111">EXAMPLES</span></span>

### <span data-ttu-id="43d0b-112">예제 1: 지정 된 위치에 이름으로 연결 모니터 가져오기</span><span class="sxs-lookup"><span data-stu-id="43d0b-112">Example 1: Get connection monitor by name in the specified location</span></span>
```
PS C:\> Get-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm


Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6
                              a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C
                              ompute/virtualMachines/irinavm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Stopped
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="43d0b-113">이 예제에서는 지정 된 위치에 이름으로 연결 모니터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="43d0b-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="43d0b-114">변수</span><span class="sxs-lookup"><span data-stu-id="43d0b-114">PARAMETERS</span></span>

### <span data-ttu-id="43d0b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43d0b-115">-DefaultProfile</span></span>
<span data-ttu-id="43d0b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="43d0b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43d0b-117">-위치</span><span class="sxs-lookup"><span data-stu-id="43d0b-117">-Location</span></span>
<span data-ttu-id="43d0b-118">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="43d0b-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="43d0b-119">-이름</span><span class="sxs-lookup"><span data-stu-id="43d0b-119">-Name</span></span>
<span data-ttu-id="43d0b-120">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43d0b-120">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d0b-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="43d0b-121">-NetworkWatcher</span></span>
<span data-ttu-id="43d0b-122">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="43d0b-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="43d0b-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="43d0b-123">-NetworkWatcherName</span></span>
<span data-ttu-id="43d0b-124">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43d0b-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="43d0b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43d0b-125">-ResourceGroupName</span></span>
<span data-ttu-id="43d0b-126">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43d0b-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="43d0b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43d0b-127">-ResourceId</span></span>
<span data-ttu-id="43d0b-128">연결 모니터의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="43d0b-128">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="43d0b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43d0b-129">CommonParameters</span></span>
<span data-ttu-id="43d0b-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="43d0b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43d0b-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43d0b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43d0b-132">입력</span><span class="sxs-lookup"><span data-stu-id="43d0b-132">INPUTS</span></span>

### <span data-ttu-id="43d0b-133">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="43d0b-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="43d0b-134">매개 변수: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="43d0b-134">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="43d0b-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="43d0b-135">System.String</span></span>

## <span data-ttu-id="43d0b-136">출력</span><span class="sxs-lookup"><span data-stu-id="43d0b-136">OUTPUTS</span></span>

### <span data-ttu-id="43d0b-137">Microsoft. 네트워크 모델. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="43d0b-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="43d0b-138">상속자</span><span class="sxs-lookup"><span data-stu-id="43d0b-138">NOTES</span></span>
<span data-ttu-id="43d0b-139">키워드: azure, azurerm, arm, 리소스, 연결, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결 모니터</span><span class="sxs-lookup"><span data-stu-id="43d0b-139">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="43d0b-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43d0b-140">RELATED LINKS</span></span>

[<span data-ttu-id="43d0b-141">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="43d0b-141">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="43d0b-142">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="43d0b-142">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="43d0b-143">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="43d0b-143">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="43d0b-144">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="43d0b-144">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="43d0b-145">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="43d0b-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="43d0b-146">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="43d0b-146">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="43d0b-147">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="43d0b-147">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="43d0b-148">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="43d0b-148">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="43d0b-149">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="43d0b-149">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="43d0b-150">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="43d0b-150">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="43d0b-151">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="43d0b-151">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="43d0b-152">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="43d0b-152">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="43d0b-153">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="43d0b-153">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="43d0b-154">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="43d0b-154">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="43d0b-155">제거-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="43d0b-155">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="43d0b-156">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="43d0b-156">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="43d0b-157">중지-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="43d0b-157">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="43d0b-158">새로운 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="43d0b-158">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="43d0b-159">새로운 AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="43d0b-159">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="43d0b-160">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="43d0b-160">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="43d0b-161">테스트-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="43d0b-161">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="43d0b-162">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="43d0b-162">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="43d0b-163">시작-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="43d0b-163">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="43d0b-164">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="43d0b-164">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="43d0b-165">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="43d0b-165">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="43d0b-166">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="43d0b-166">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="43d0b-167">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="43d0b-167">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
