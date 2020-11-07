---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 014942f38abf0caae01463d07343b5ad473a24d7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881014"
---
# <span data-ttu-id="2c79f-101">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2c79f-101">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="2c79f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c79f-102">SYNOPSIS</span></span>
<span data-ttu-id="2c79f-103">지정 된 이름 또는 연결 모니터 목록으로 연결 모니터를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c79f-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c79f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2c79f-104">SYNTAX</span></span>

### <span data-ttu-id="2c79f-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="2c79f-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="2c79f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2c79f-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="2c79f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2c79f-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="2c79f-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2c79f-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="2c79f-109">설명은</span><span class="sxs-lookup"><span data-stu-id="2c79f-109">DESCRIPTION</span></span>
<span data-ttu-id="2c79f-110">Get-AzureRmNetworkWatcherConnectionMonitor cmdlet은 지정 된 이름/resourceId를 갖는 연결 모니터 또는 지정 된 네트워크 감시자/위치에 해당 하는 연결 모니터링 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c79f-110">The Get-AzureRmNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="2c79f-111">예제의</span><span class="sxs-lookup"><span data-stu-id="2c79f-111">EXAMPLES</span></span>

### <span data-ttu-id="2c79f-112">---------------예제 1: 지정 된 위치에서 이름으로 연결 모니터 가져오기---------------</span><span class="sxs-lookup"><span data-stu-id="2c79f-112">---------------  Example 1: Get connection monitor by name in the specified location ---------------</span></span>
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

<span data-ttu-id="2c79f-113">이 예제에서는 지정 된 위치에 이름으로 연결 모니터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c79f-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="2c79f-114">변수</span><span class="sxs-lookup"><span data-stu-id="2c79f-114">PARAMETERS</span></span>

### <span data-ttu-id="2c79f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c79f-115">-AsJob</span></span>
<span data-ttu-id="2c79f-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2c79f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2c79f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c79f-117">-DefaultProfile</span></span>
<span data-ttu-id="2c79f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c79f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c79f-119">-위치</span><span class="sxs-lookup"><span data-stu-id="2c79f-119">-Location</span></span>
<span data-ttu-id="2c79f-120">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="2c79f-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2c79f-121">-이름</span><span class="sxs-lookup"><span data-stu-id="2c79f-121">-Name</span></span>
<span data-ttu-id="2c79f-122">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c79f-122">The connection monitor name.</span></span>

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

### <span data-ttu-id="2c79f-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2c79f-123">-NetworkWatcher</span></span>
<span data-ttu-id="2c79f-124">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="2c79f-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="2c79f-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2c79f-125">-NetworkWatcherName</span></span>
<span data-ttu-id="2c79f-126">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c79f-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="2c79f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c79f-127">-ResourceGroupName</span></span>
<span data-ttu-id="2c79f-128">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c79f-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2c79f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c79f-129">-ResourceId</span></span>
<span data-ttu-id="2c79f-130">연결 모니터의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2c79f-130">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="2c79f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c79f-131">CommonParameters</span></span>
<span data-ttu-id="2c79f-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c79f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c79f-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c79f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c79f-134">입력</span><span class="sxs-lookup"><span data-stu-id="2c79f-134">INPUTS</span></span>

### <span data-ttu-id="2c79f-135">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2c79f-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="2c79f-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2c79f-136">System.String</span></span>


## <span data-ttu-id="2c79f-137">출력</span><span class="sxs-lookup"><span data-stu-id="2c79f-137">OUTPUTS</span></span>

### <span data-ttu-id="2c79f-138">Microsoft. 네트워크 모델. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="2c79f-138">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="2c79f-139">상속자</span><span class="sxs-lookup"><span data-stu-id="2c79f-139">NOTES</span></span>
<span data-ttu-id="2c79f-140">키워드: azure, azurerm, arm, 리소스, 연결, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결 모니터</span><span class="sxs-lookup"><span data-stu-id="2c79f-140">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="2c79f-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c79f-141">RELATED LINKS</span></span>
<span data-ttu-id="2c79f-142">[새로운 AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [제거-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="2c79f-142">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="2c79f-143">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="2c79f-143">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="2c79f-144">[새로운 AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [새로운 AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [제거-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [중지-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="2c79f-144">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="2c79f-145">[새로운 AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="2c79f-145">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span></span>
