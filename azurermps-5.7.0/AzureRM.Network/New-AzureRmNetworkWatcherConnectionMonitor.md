---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: b8dd04fa4727465ee9b3be3eaf5e5e06a2243338
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711153"
---
# <span data-ttu-id="722a3-101">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="722a3-101">New-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="722a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="722a3-102">SYNOPSIS</span></span>
<span data-ttu-id="722a3-103">연결 모니터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="722a3-103">Creates a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="722a3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="722a3-104">SYNTAX</span></span>

### <span data-ttu-id="722a3-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="722a3-105">SetByName (Default)</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="722a3-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="722a3-106">SetByResource</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="722a3-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="722a3-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="722a3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="722a3-108">DESCRIPTION</span></span>
<span data-ttu-id="722a3-109">New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates 지정 된 원본 및 대상에 대 한 연결 모니터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="722a3-109">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="722a3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="722a3-110">EXAMPLES</span></span>

### <span data-ttu-id="722a3-111">예제 1: vm 및 인터넷 대상에 대 한 연결 모니터 만들기</span><span class="sxs-lookup"><span data-stu-id="722a3-111">Example 1: Create a connection monitor for a vm and internet destination</span></span>
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

<span data-ttu-id="722a3-112">New-AzureRmNetworkWatcherConnectionMonitor cmdlet은 지정 된 원본 및 대상에 대 한 연결 모니터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="722a3-112">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="722a3-113">변수</span><span class="sxs-lookup"><span data-stu-id="722a3-113">PARAMETERS</span></span>

### <span data-ttu-id="722a3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="722a3-114">-AsJob</span></span>
<span data-ttu-id="722a3-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="722a3-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="722a3-116">-확인</span><span class="sxs-lookup"><span data-stu-id="722a3-116">-Confirm</span></span>
<span data-ttu-id="722a3-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="722a3-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="722a3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="722a3-118">-DefaultProfile</span></span>
<span data-ttu-id="722a3-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="722a3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="722a3-120">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="722a3-120">-DestinationAddress</span></span>
<span data-ttu-id="722a3-121">연결 모니터 대상의 Ip 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="722a3-121">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="722a3-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="722a3-122">-DestinationPort</span></span>
<span data-ttu-id="722a3-123">대상 포트.</span><span class="sxs-lookup"><span data-stu-id="722a3-123">Destination port.</span></span>

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

### <span data-ttu-id="722a3-124">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="722a3-124">-DestinationResourceId</span></span>
<span data-ttu-id="722a3-125">연결 모니터 대상의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="722a3-125">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="722a3-126">-Force</span><span class="sxs-lookup"><span data-stu-id="722a3-126">-Force</span></span>
<span data-ttu-id="722a3-127">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="722a3-127">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="722a3-128">-위치</span><span class="sxs-lookup"><span data-stu-id="722a3-128">-Location</span></span>
<span data-ttu-id="722a3-129">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="722a3-129">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="722a3-130">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="722a3-130">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="722a3-131">모니터링 간격 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="722a3-131">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="722a3-132">-이름</span><span class="sxs-lookup"><span data-stu-id="722a3-132">-Name</span></span>
<span data-ttu-id="722a3-133">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="722a3-133">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="722a3-134">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="722a3-134">-NetworkWatcher</span></span>
<span data-ttu-id="722a3-135">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="722a3-135">The network watcher resource.</span></span>

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

### <span data-ttu-id="722a3-136">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="722a3-136">-NetworkWatcherName</span></span>
<span data-ttu-id="722a3-137">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="722a3-137">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="722a3-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="722a3-138">-ResourceGroupName</span></span>
<span data-ttu-id="722a3-139">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="722a3-139">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="722a3-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="722a3-140">-SourcePort</span></span>
<span data-ttu-id="722a3-141">원본 포트.</span><span class="sxs-lookup"><span data-stu-id="722a3-141">Source port.</span></span>

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

### <span data-ttu-id="722a3-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="722a3-142">-SourceResourceId</span></span>
<span data-ttu-id="722a3-143">연결 모니터 원본의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="722a3-143">The ID of the connection monitor source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="722a3-144">태그</span><span class="sxs-lookup"><span data-stu-id="722a3-144">-Tag</span></span>
<span data-ttu-id="722a3-145">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="722a3-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="722a3-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="722a3-146">-WhatIf</span></span>
<span data-ttu-id="722a3-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="722a3-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="722a3-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="722a3-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="722a3-149">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="722a3-149">-ConfigureOnly</span></span>
<span data-ttu-id="722a3-150">연결 모니터를 구성 하지만 시작 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="722a3-150">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="722a3-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="722a3-151">CommonParameters</span></span>
<span data-ttu-id="722a3-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="722a3-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="722a3-153">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="722a3-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="722a3-154">입력</span><span class="sxs-lookup"><span data-stu-id="722a3-154">INPUTS</span></span>

### <span data-ttu-id="722a3-155">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="722a3-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="722a3-156">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="722a3-156">System.String</span></span>

## <span data-ttu-id="722a3-157">출력</span><span class="sxs-lookup"><span data-stu-id="722a3-157">OUTPUTS</span></span>

### <span data-ttu-id="722a3-158">Microsoft. 네트워크 모델. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="722a3-158">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="722a3-159">상속자</span><span class="sxs-lookup"><span data-stu-id="722a3-159">NOTES</span></span>
<span data-ttu-id="722a3-160">키워드: azure, azurerm, arm, 리소스, 연결, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결 모니터</span><span class="sxs-lookup"><span data-stu-id="722a3-160">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="722a3-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="722a3-161">RELATED LINKS</span></span>

[<span data-ttu-id="722a3-162">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="722a3-162">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="722a3-163">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="722a3-163">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="722a3-164">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="722a3-164">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="722a3-165">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="722a3-165">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="722a3-166">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="722a3-166">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="722a3-167">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="722a3-167">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="722a3-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="722a3-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="722a3-169">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="722a3-169">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="722a3-170">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="722a3-170">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="722a3-171">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="722a3-171">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="722a3-172">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="722a3-172">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="722a3-173">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="722a3-173">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="722a3-174">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="722a3-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="722a3-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="722a3-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="722a3-176">제거-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="722a3-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="722a3-177">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="722a3-177">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="722a3-178">시작-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="722a3-178">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="722a3-179">중지-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="722a3-179">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
