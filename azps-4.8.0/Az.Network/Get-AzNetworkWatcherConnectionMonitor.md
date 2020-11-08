---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: c2da2b9173b3977a606699fd8e1def3dae2a68d9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204546"
---
# <span data-ttu-id="d9594-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d9594-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="d9594-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9594-102">SYNOPSIS</span></span>
<span data-ttu-id="d9594-103">지정 된 이름 또는 연결 모니터 목록으로 연결 모니터를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9594-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="d9594-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d9594-104">SYNTAX</span></span>

### <span data-ttu-id="d9594-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d9594-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9594-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d9594-106">SetByResource</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9594-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d9594-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9594-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d9594-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9594-109">설명은</span><span class="sxs-lookup"><span data-stu-id="d9594-109">DESCRIPTION</span></span>
<span data-ttu-id="d9594-110">Get-AzNetworkWatcherConnectionMonitor cmdlet은 지정 된 이름/resourceId를 갖는 연결 모니터 또는 지정 된 네트워크 감시자/위치에 해당 하는 연결 모니터링 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9594-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="d9594-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d9594-111">EXAMPLES</span></span>

### <span data-ttu-id="d9594-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="d9594-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="d9594-113">Name: cm Id:/subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/공급자/Microsoft/connectionMonitors/cm Etag: W o s NetworkWatcher_centraluseuap/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState: 성공 원본: {"ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/공급자/Microsoft. C ompute/virtualMachines/irinavm", "Port": 0} 대상: {"주소": "google.com", "포트": 80} MonitoringIntervalInSeconds: 60 자동 시작: 실제 StartTime: 1/12/2018 7:19:28 PM MonitoringStatus: 중지 된 위치: centraluseuap 형식: Microsoft. Network/networkWatchers/connectionMonitors 태그: {"key1": "value1"}</span><span class="sxs-lookup"><span data-stu-id="d9594-113">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C ompute/virtualMachines/irinavm", "Port": 0 } Destination                 : { "Address": "google.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:19:28 PM MonitoringStatus            : Stopped Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : { "key1": "value1" }</span></span>

## <span data-ttu-id="d9594-114">변수</span><span class="sxs-lookup"><span data-stu-id="d9594-114">PARAMETERS</span></span>

### <span data-ttu-id="d9594-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9594-115">-DefaultProfile</span></span>
<span data-ttu-id="d9594-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d9594-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9594-117">-위치</span><span class="sxs-lookup"><span data-stu-id="d9594-117">-Location</span></span>
<span data-ttu-id="d9594-118">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d9594-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d9594-119">-이름</span><span class="sxs-lookup"><span data-stu-id="d9594-119">-Name</span></span>
<span data-ttu-id="d9594-120">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d9594-120">The connection monitor name.</span></span>

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

### <span data-ttu-id="d9594-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d9594-121">-NetworkWatcher</span></span>
<span data-ttu-id="d9594-122">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="d9594-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="d9594-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d9594-123">-NetworkWatcherName</span></span>
<span data-ttu-id="d9594-124">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d9594-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="d9594-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9594-125">-ResourceGroupName</span></span>
<span data-ttu-id="d9594-126">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d9594-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d9594-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9594-127">-ResourceId</span></span>
<span data-ttu-id="d9594-128">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d9594-128">Resource ID.</span></span>

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

### <span data-ttu-id="d9594-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9594-129">CommonParameters</span></span>
<span data-ttu-id="d9594-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9594-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9594-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d9594-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9594-132">입력</span><span class="sxs-lookup"><span data-stu-id="d9594-132">INPUTS</span></span>

### <span data-ttu-id="d9594-133">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d9594-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d9594-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d9594-134">System.String</span></span>

## <span data-ttu-id="d9594-135">출력</span><span class="sxs-lookup"><span data-stu-id="d9594-135">OUTPUTS</span></span>

### <span data-ttu-id="d9594-136">PSConnectionMonitorResultV1에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d9594-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="d9594-137">PSConnectionMonitorResultV2에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d9594-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="d9594-138">상속자</span><span class="sxs-lookup"><span data-stu-id="d9594-138">NOTES</span></span>

## <span data-ttu-id="d9594-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9594-139">RELATED LINKS</span></span>
