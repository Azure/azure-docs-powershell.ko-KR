---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 30ab203f50df9e712792e216a1b4ecf1c5378b2e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954432"
---
# <span data-ttu-id="3cbaf-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3cbaf-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="3cbaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cbaf-102">SYNOPSIS</span></span>
<span data-ttu-id="3cbaf-103">지정된 이름 또는 연결 모니터 목록이 있는 연결 모니터를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3cbaf-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="3cbaf-104">구문</span><span class="sxs-lookup"><span data-stu-id="3cbaf-104">SYNTAX</span></span>

### <span data-ttu-id="3cbaf-105">SetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="3cbaf-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3cbaf-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3cbaf-106">SetByResource</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3cbaf-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3cbaf-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3cbaf-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3cbaf-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3cbaf-109">설명</span><span class="sxs-lookup"><span data-stu-id="3cbaf-109">DESCRIPTION</span></span>
<span data-ttu-id="3cbaf-110">Get-AzNetworkWatcherConnectionMonitor cmdlet은 지정된 이름/resourceId 또는 지정된 네트워크 감시자/위치에 해당하는 연결 모니터 목록을 사용하여 연결 모니터를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3cbaf-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="3cbaf-111">예제</span><span class="sxs-lookup"><span data-stu-id="3cbaf-111">EXAMPLES</span></span>

### <span data-ttu-id="3cbaf-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="3cbaf-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="3cbaf-113">이름 : cm Id : /subscriptions/0000000-0000-0000-000000000/resourceGro ups/NetworkWatcherRG/providers /Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm Etag : W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState : 성공한 원본 : { "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C ompute/virtualMachines/irinavm", "Port": 0 } Destination : { "address": "google.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart : True StartTime : 1/19:28 PM MonitoringStatus : stopped location : centraluseuap Type : Microsoft.Network/networkWatchers/connectionMonitors Tags : { "key1": "value1" }</span><span class="sxs-lookup"><span data-stu-id="3cbaf-113">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C ompute/virtualMachines/irinavm", "Port": 0 } Destination                 : { "Address": "google.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:19:28 PM MonitoringStatus            : Stopped Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : { "key1": "value1" }</span></span>

## <span data-ttu-id="3cbaf-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3cbaf-114">PARAMETERS</span></span>

### <span data-ttu-id="3cbaf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cbaf-115">-DefaultProfile</span></span>
<span data-ttu-id="3cbaf-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3cbaf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cbaf-117">-Location</span><span class="sxs-lookup"><span data-stu-id="3cbaf-117">-Location</span></span>
<span data-ttu-id="3cbaf-118">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="3cbaf-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="3cbaf-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3cbaf-119">-Name</span></span>
<span data-ttu-id="3cbaf-120">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3cbaf-120">The connection monitor name.</span></span>

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

### <span data-ttu-id="3cbaf-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3cbaf-121">-NetworkWatcher</span></span>
<span data-ttu-id="3cbaf-122">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="3cbaf-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="3cbaf-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3cbaf-123">-NetworkWatcherName</span></span>
<span data-ttu-id="3cbaf-124">네트워크 감시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3cbaf-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="3cbaf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cbaf-125">-ResourceGroupName</span></span>
<span data-ttu-id="3cbaf-126">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3cbaf-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3cbaf-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3cbaf-127">-ResourceId</span></span>
<span data-ttu-id="3cbaf-128">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3cbaf-128">Resource ID.</span></span>

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

### <span data-ttu-id="3cbaf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cbaf-129">CommonParameters</span></span>
<span data-ttu-id="3cbaf-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3cbaf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cbaf-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3cbaf-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cbaf-132">입력</span><span class="sxs-lookup"><span data-stu-id="3cbaf-132">INPUTS</span></span>

### <span data-ttu-id="3cbaf-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3cbaf-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="3cbaf-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3cbaf-134">System.String</span></span>

## <span data-ttu-id="3cbaf-135">출력</span><span class="sxs-lookup"><span data-stu-id="3cbaf-135">OUTPUTS</span></span>

### <span data-ttu-id="3cbaf-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="3cbaf-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="3cbaf-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="3cbaf-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="3cbaf-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3cbaf-138">NOTES</span></span>

## <span data-ttu-id="3cbaf-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3cbaf-139">RELATED LINKS</span></span>
