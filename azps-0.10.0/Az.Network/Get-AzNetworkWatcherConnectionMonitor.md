---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: d8ab2ce24db9c6ab07989dc5a4a45b8bfca8fc78
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875549"
---
# <span data-ttu-id="42cf4-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="42cf4-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="42cf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42cf4-102">SYNOPSIS</span></span>
<span data-ttu-id="42cf4-103">지정 된 이름 또는 연결 모니터 목록으로 연결 모니터를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="42cf4-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="42cf4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="42cf4-104">SYNTAX</span></span>

### <span data-ttu-id="42cf4-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="42cf4-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="42cf4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="42cf4-106">SetByName</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="42cf4-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="42cf4-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="42cf4-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="42cf4-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="42cf4-109">설명은</span><span class="sxs-lookup"><span data-stu-id="42cf4-109">DESCRIPTION</span></span>
<span data-ttu-id="42cf4-110">Get-AzNetworkWatcherConnectionMonitor cmdlet은 지정 된 이름/resourceId를 갖는 연결 모니터 또는 지정 된 네트워크 감시자/위치에 해당 하는 연결 모니터링 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="42cf4-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="42cf4-111">예제의</span><span class="sxs-lookup"><span data-stu-id="42cf4-111">EXAMPLES</span></span>

### <span data-ttu-id="42cf4-112">---------------예제 1: 지정 된 위치에서 이름으로 연결 모니터 가져오기---------------</span><span class="sxs-lookup"><span data-stu-id="42cf4-112">---------------  Example 1: Get connection monitor by name in the specified location ---------------</span></span>
```
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm


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

<span data-ttu-id="42cf4-113">이 예제에서는 지정 된 위치에 이름으로 연결 모니터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="42cf4-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="42cf4-114">변수</span><span class="sxs-lookup"><span data-stu-id="42cf4-114">PARAMETERS</span></span>

### <span data-ttu-id="42cf4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42cf4-115">-AsJob</span></span>
<span data-ttu-id="42cf4-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="42cf4-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42cf4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42cf4-117">-DefaultProfile</span></span>
<span data-ttu-id="42cf4-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42cf4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42cf4-119">-위치</span><span class="sxs-lookup"><span data-stu-id="42cf4-119">-Location</span></span>
<span data-ttu-id="42cf4-120">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="42cf4-120">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42cf4-121">-이름</span><span class="sxs-lookup"><span data-stu-id="42cf4-121">-Name</span></span>
<span data-ttu-id="42cf4-122">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42cf4-122">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42cf4-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="42cf4-123">-NetworkWatcher</span></span>
<span data-ttu-id="42cf4-124">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="42cf4-124">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42cf4-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="42cf4-125">-NetworkWatcherName</span></span>
<span data-ttu-id="42cf4-126">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42cf4-126">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42cf4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42cf4-127">-ResourceGroupName</span></span>
<span data-ttu-id="42cf4-128">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42cf4-128">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42cf4-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42cf4-129">-ResourceId</span></span>
<span data-ttu-id="42cf4-130">연결 모니터의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="42cf4-130">Resource ID of the connection monitor.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42cf4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42cf4-131">CommonParameters</span></span>
<span data-ttu-id="42cf4-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="42cf4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42cf4-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42cf4-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42cf4-134">입력</span><span class="sxs-lookup"><span data-stu-id="42cf4-134">INPUTS</span></span>

### <span data-ttu-id="42cf4-135">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="42cf4-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="42cf4-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="42cf4-136">System.String</span></span>


## <span data-ttu-id="42cf4-137">출력</span><span class="sxs-lookup"><span data-stu-id="42cf4-137">OUTPUTS</span></span>

### <span data-ttu-id="42cf4-138">Microsoft. 네트워크 모델. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="42cf4-138">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="42cf4-139">상속자</span><span class="sxs-lookup"><span data-stu-id="42cf4-139">NOTES</span></span>
<span data-ttu-id="42cf4-140">키워드: azure, azurerm, arm, 리소스, 연결, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결 모니터</span><span class="sxs-lookup"><span data-stu-id="42cf4-140">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="42cf4-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42cf4-141">RELATED LINKS</span></span>
<span data-ttu-id="42cf4-142">[새로운 AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [제거-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="42cf4-142">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="42cf4-143">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="42cf4-143">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="42cf4-144">[새로운 AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [새로운 AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [제거-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [중지-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="42cf4-144">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="42cf4-145">[새로운 AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="42cf4-145">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)</span></span>