---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 93c54df5cb0976aa0bd8f73881208c1966bbe9d0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876561"
---
# <span data-ttu-id="6f136-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6f136-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="6f136-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f136-102">SYNOPSIS</span></span>
<span data-ttu-id="6f136-103">연결 모니터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f136-103">Update a connection monitor.</span></span>

## <span data-ttu-id="6f136-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f136-104">SYNTAX</span></span>

### <span data-ttu-id="6f136-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="6f136-105">SetByResource (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6f136-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="6f136-106">SetByName</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6f136-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="6f136-107">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6f136-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6f136-108">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6f136-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="6f136-109">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="6f136-110">설명은</span><span class="sxs-lookup"><span data-stu-id="6f136-110">DESCRIPTION</span></span>
<span data-ttu-id="6f136-111">Set-AzNetworkWatcherConnectionMonitor cmdlet은 지정 된 연결 모니터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f136-111">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="6f136-112">예제의</span><span class="sxs-lookup"><span data-stu-id="6f136-112">EXAMPLES</span></span>

### <span data-ttu-id="6f136-113">---------------예제 1: 연결 모니터 업데이트---------------</span><span class="sxs-lookup"><span data-stu-id="6f136-113">---------------  Example 1: Update a connection monitor ---------------</span></span>
```
PS C:\> Set-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm 
-DestinationAddress google.com -DestinationPort 80 -Tag @{"key1" = "value1"}

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"5b2b20e8-0ce0-417e-9607-76208149bb67"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMach
                                ines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="6f136-114">이 예제에서는 destinationAddress를 변경 하 고 태그를 추가 하 여 기존 연결 모니터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f136-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="6f136-115">변수</span><span class="sxs-lookup"><span data-stu-id="6f136-115">PARAMETERS</span></span>

### <span data-ttu-id="6f136-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f136-116">-AsJob</span></span>
<span data-ttu-id="6f136-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6f136-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f136-118">-자동 시작</span><span class="sxs-lookup"><span data-stu-id="6f136-118">-AutoStart</span></span>
<span data-ttu-id="6f136-119">자동 시작</span><span class="sxs-lookup"><span data-stu-id="6f136-119">Auto start.</span></span>

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

### <span data-ttu-id="6f136-120">-확인</span><span class="sxs-lookup"><span data-stu-id="6f136-120">-Confirm</span></span>
<span data-ttu-id="6f136-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f136-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f136-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f136-122">-DefaultProfile</span></span>
<span data-ttu-id="6f136-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f136-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f136-124">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="6f136-124">-DestinationAddress</span></span>
<span data-ttu-id="6f136-125">연결 모니터 대상의 Ip 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="6f136-125">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="6f136-126">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="6f136-126">-DestinationPort</span></span>
<span data-ttu-id="6f136-127">대상 포트.</span><span class="sxs-lookup"><span data-stu-id="6f136-127">Destination port.</span></span>

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

### <span data-ttu-id="6f136-128">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="6f136-128">-DestinationResourceId</span></span>
<span data-ttu-id="6f136-129">연결 모니터 대상의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6f136-129">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="6f136-130">-Force</span><span class="sxs-lookup"><span data-stu-id="6f136-130">-Force</span></span>
<span data-ttu-id="6f136-131">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="6f136-131">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="6f136-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f136-132">-InputObject</span></span>
<span data-ttu-id="6f136-133">연결 모니터 개체</span><span class="sxs-lookup"><span data-stu-id="6f136-133">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f136-134">-위치</span><span class="sxs-lookup"><span data-stu-id="6f136-134">-Location</span></span>
<span data-ttu-id="6f136-135">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6f136-135">Location of the network watcher.</span></span>

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

### <span data-ttu-id="6f136-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="6f136-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="6f136-137">모니터링 간격 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="6f136-137">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="6f136-138">-이름</span><span class="sxs-lookup"><span data-stu-id="6f136-138">-Name</span></span>
<span data-ttu-id="6f136-139">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f136-139">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f136-140">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6f136-140">-NetworkWatcher</span></span>
<span data-ttu-id="6f136-141">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="6f136-141">The network watcher resource.</span></span>

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

### <span data-ttu-id="6f136-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6f136-142">-NetworkWatcherName</span></span>
<span data-ttu-id="6f136-143">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f136-143">The name of network watcher.</span></span>

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

### <span data-ttu-id="6f136-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f136-144">-ResourceGroupName</span></span>
<span data-ttu-id="6f136-145">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f136-145">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="6f136-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f136-146">-ResourceId</span></span>
<span data-ttu-id="6f136-147">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6f136-147">Resource ID.</span></span>

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

### <span data-ttu-id="6f136-148">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="6f136-148">-SourcePort</span></span>
<span data-ttu-id="6f136-149">원본 포트.</span><span class="sxs-lookup"><span data-stu-id="6f136-149">Source port.</span></span>

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

### <span data-ttu-id="6f136-150">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="6f136-150">-SourceResourceId</span></span>
<span data-ttu-id="6f136-151">연결 모니터 원본의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6f136-151">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="6f136-152">태그</span><span class="sxs-lookup"><span data-stu-id="6f136-152">-Tag</span></span>
<span data-ttu-id="6f136-153">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="6f136-153">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6f136-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f136-154">-WhatIf</span></span>
<span data-ttu-id="6f136-155">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6f136-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f136-156">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f136-156">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="6f136-157">입력</span><span class="sxs-lookup"><span data-stu-id="6f136-157">INPUTS</span></span>

### <span data-ttu-id="6f136-158">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6f136-158">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="6f136-159">Microsoft. Azure. PSConnectionMonitorResult.</span><span class="sxs-lookup"><span data-stu-id="6f136-159">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="6f136-160">출력</span><span class="sxs-lookup"><span data-stu-id="6f136-160">OUTPUTS</span></span>

### <span data-ttu-id="6f136-161">Microsoft. 네트워크 모델. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="6f136-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="6f136-162">상속자</span><span class="sxs-lookup"><span data-stu-id="6f136-162">NOTES</span></span>
<span data-ttu-id="6f136-163">키워드: azure, azurerm, arm, 리소스, 연결, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결 모니터</span><span class="sxs-lookup"><span data-stu-id="6f136-163">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="6f136-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f136-164">RELATED LINKS</span></span>
<span data-ttu-id="6f136-165">[새로운 AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [제거-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="6f136-165">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="6f136-166">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="6f136-166">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="6f136-167">[새로운 AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [새로운 AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [제거-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [중지-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="6f136-167">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="6f136-168">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [제거-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [시작-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="6f136-168">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span></span>

