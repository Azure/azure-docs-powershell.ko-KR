---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 3e5853d99157fef87c2f02c2be9fab7bb983d1ae
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881806"
---
# <span data-ttu-id="a9eb1-101">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a9eb1-101">New-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="a9eb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9eb1-102">SYNOPSIS</span></span>
<span data-ttu-id="a9eb1-103">연결 모니터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb1-103">Creates a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9eb1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a9eb1-104">SYNTAX</span></span>

### <span data-ttu-id="a9eb1-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="a9eb1-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a9eb1-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a9eb1-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a9eb1-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a9eb1-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a9eb1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a9eb1-108">DESCRIPTION</span></span>
<span data-ttu-id="a9eb1-109">New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates 지정 된 원본 및 대상에 대 한 연결 모니터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb1-109">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="a9eb1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a9eb1-110">EXAMPLES</span></span>

### <span data-ttu-id="a9eb1-111">---------------예제 1: vm 및 인터넷 대상에 대 한 연결 모니터 만들기---------------</span><span class="sxs-lookup"><span data-stu-id="a9eb1-111">---------------  Example 1: Create a connection monitor for a vm and internet destination ---------------</span></span>
```
PS C:\> New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/t1
Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft
                                .Compute/virtualMachines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "bing.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:13:11 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {}
```

<span data-ttu-id="a9eb1-112">New-AzureRmNetworkWatcherConnectionMonitor cmdlet은 지정 된 원본 및 대상에 대 한 연결 모니터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb1-112">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="a9eb1-113">변수</span><span class="sxs-lookup"><span data-stu-id="a9eb1-113">PARAMETERS</span></span>

### <span data-ttu-id="a9eb1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9eb1-114">-AsJob</span></span>
<span data-ttu-id="a9eb1-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a9eb1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9eb1-116">-자동 시작</span><span class="sxs-lookup"><span data-stu-id="a9eb1-116">-AutoStart</span></span>
<span data-ttu-id="a9eb1-117">자동 시작</span><span class="sxs-lookup"><span data-stu-id="a9eb1-117">Auto start.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9eb1-118">-확인</span><span class="sxs-lookup"><span data-stu-id="a9eb1-118">-Confirm</span></span>
<span data-ttu-id="a9eb1-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb1-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9eb1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9eb1-120">-DefaultProfile</span></span>
<span data-ttu-id="a9eb1-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9eb1-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="a9eb1-122">-DestinationAddress</span></span>
<span data-ttu-id="a9eb1-123">연결 모니터 대상의 Ip 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb1-123">The Ip address of the connection monitor destination.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9eb1-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="a9eb1-124">-DestinationPort</span></span>
<span data-ttu-id="a9eb1-125">대상 포트.</span><span class="sxs-lookup"><span data-stu-id="a9eb1-125">Destination port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9eb1-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="a9eb1-126">-DestinationResourceId</span></span>
<span data-ttu-id="a9eb1-127">연결 모니터 대상의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb1-127">The ID of the connection monitor destination.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9eb1-128">-Force</span><span class="sxs-lookup"><span data-stu-id="a9eb1-128">-Force</span></span>
<span data-ttu-id="a9eb1-129">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="a9eb1-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a9eb1-130">-위치</span><span class="sxs-lookup"><span data-stu-id="a9eb1-130">-Location</span></span>
<span data-ttu-id="a9eb1-131">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb1-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a9eb1-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a9eb1-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="a9eb1-133">모니터링 간격 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb1-133">Monitoring interval in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9eb1-134">-이름</span><span class="sxs-lookup"><span data-stu-id="a9eb1-134">-Name</span></span>
<span data-ttu-id="a9eb1-135">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb1-135">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9eb1-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a9eb1-136">-NetworkWatcher</span></span>
<span data-ttu-id="a9eb1-137">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="a9eb1-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="a9eb1-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a9eb1-138">-NetworkWatcherName</span></span>
<span data-ttu-id="a9eb1-139">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb1-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="a9eb1-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9eb1-140">-ResourceGroupName</span></span>
<span data-ttu-id="a9eb1-141">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb1-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a9eb1-142">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="a9eb1-142">-SourcePort</span></span>
<span data-ttu-id="a9eb1-143">원본 포트.</span><span class="sxs-lookup"><span data-stu-id="a9eb1-143">Source port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9eb1-144">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="a9eb1-144">-SourceResourceId</span></span>
<span data-ttu-id="a9eb1-145">연결 모니터 원본의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb1-145">The ID of the connection monitor source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9eb1-146">태그</span><span class="sxs-lookup"><span data-stu-id="a9eb1-146">-Tag</span></span>
<span data-ttu-id="a9eb1-147">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb1-147">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9eb1-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9eb1-148">-WhatIf</span></span>
<span data-ttu-id="a9eb1-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb1-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9eb1-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb1-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="a9eb1-151">입력</span><span class="sxs-lookup"><span data-stu-id="a9eb1-151">INPUTS</span></span>

### <span data-ttu-id="a9eb1-152">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a9eb1-152">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a9eb1-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a9eb1-153">System.String</span></span>


## <span data-ttu-id="a9eb1-154">출력</span><span class="sxs-lookup"><span data-stu-id="a9eb1-154">OUTPUTS</span></span>

### <span data-ttu-id="a9eb1-155">Microsoft. 네트워크 모델. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="a9eb1-155">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="a9eb1-156">상속자</span><span class="sxs-lookup"><span data-stu-id="a9eb1-156">NOTES</span></span>
<span data-ttu-id="a9eb1-157">키워드: azure, azurerm, arm, 리소스, 연결, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결 모니터</span><span class="sxs-lookup"><span data-stu-id="a9eb1-157">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="a9eb1-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9eb1-158">RELATED LINKS</span></span>
<span data-ttu-id="a9eb1-159">[새로운 AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [제거-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="a9eb1-159">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="a9eb1-160">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="a9eb1-160">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="a9eb1-161">[새로운 AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [새로운 AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [제거-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [중지-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="a9eb1-161">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="a9eb1-162">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [제거-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="a9eb1-162">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>
