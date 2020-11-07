---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitorReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitorReport.md
ms.openlocfilehash: a1bdb9a1e77793622d0c23793701b9d3119b4f1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702258"
---
# <span data-ttu-id="e20a0-101">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e20a0-101">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>

## <span data-ttu-id="e20a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e20a0-102">SYNOPSIS</span></span>
<span data-ttu-id="e20a0-103">최신 연결 상태의 스냅숏을 쿼리 합니다.</span><span class="sxs-lookup"><span data-stu-id="e20a0-103">Query a snapshot of the most recent connection states.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e20a0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e20a0-104">SYNTAX</span></span>

### <span data-ttu-id="e20a0-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="e20a0-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e20a0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e20a0-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -NetworkWatcher <PSNetworkWatcher> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e20a0-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e20a0-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -Location <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e20a0-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e20a0-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e20a0-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="e20a0-109">SetByInputObject</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -InputObject <PSConnectionMonitorResult> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e20a0-110">설명은</span><span class="sxs-lookup"><span data-stu-id="e20a0-110">DESCRIPTION</span></span>
<span data-ttu-id="e20a0-111">Get-AzureRmNetworkWatcherConnectionMonitorReport cmdlet은 최신 연결 상태에 대 한 보고서를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e20a0-111">The Get-AzureRmNetworkWatcherConnectionMonitorReport cmdlet returns the report on the most recent connection states.</span></span>

## <span data-ttu-id="e20a0-112">예제의</span><span class="sxs-lookup"><span data-stu-id="e20a0-112">EXAMPLES</span></span>

### <span data-ttu-id="e20a0-113">예제 1: 지정 된 위치에서 연결 모니터의 이름에 대 한 최신 연결 스냅숏 가져오기</span><span class="sxs-lookup"><span data-stu-id="e20a0-113">Example 1: Get the most recent connection snapshot of the connection monitor by name in the specified location</span></span>
```
PS C:\> Get-AzureRmNetworkWatcherConnectionMonitorReport -Location centraluseuap -Name cm


States : [
           {
             "ConnectionState": "Reachable",
             "StartTime": "2018-01-12T01:18:20Z",
             "EvaluationState": "Completed",
             "Hops": [
               {
                 "Type": "Source",
                 "Id": "1530e0f2-c9b7-4bc0-a205-cf7332cd8983",
                 "Address": "10.1.1.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "b19b74b1-423d-4f0b-99cd-bcaed4d0b8a2"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "b19b74b1-423d-4f0b-99cd-bcaed4d0b8a2",
                 "Address": "10.1.2.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/fwNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "80e46c56-2cf9-4106-8602-608a74832d41"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "80e46c56-2cf9-4106-8602-608a74832d41",
                 "Address": "10.1.3.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/auNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "e17cf884-69db-43b8-9cd5-f920770a0dbe"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualNetwork",
                 "Id": "e17cf884-69db-43b8-9cd5-f920770a0dbe",
                 "Address": "10.1.4.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/dbNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [],
                 "Issues": []
               }
             ]
           },
           {
             "ConnectionState": "Unreachable",
             "StartTime": "2018-01-12T01:14:11Z",
             "EvaluationState": "Completed",
             "Hops": [
               {
                 "Type": "Source",
                 "Id": "b6251ff8-3d07-4fdf-98f8-04b168e1cf90",
                 "Address": "10.1.1.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "de6d463b-47fb-4beb-afc4-d77782755313"
                 ],
                 "Issues": [
                   {
                     "Origin": "Local",
                     "Severity": "Error",
                     "Type": "NetworkError",
                     "Context": []
                   }
                 ]
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "de6d463b-47fb-4beb-afc4-d77782755313",
                 "Address": "10.1.2.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/fwNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "0cbadb7e-cd99-4fa9-a832-eb4e0d112293"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "0cbadb7e-cd99-4fa9-a832-eb4e0d112293",
                 "Address": "10.1.3.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/auNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "538005d1-994a-4350-9866-6985385beecf"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualNetwork",
                 "Id": "538005d1-994a-4350-9866-6985385beecf",
                 "Address": "10.1.4.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/dbNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [],
                 "Issues": []
               }
             ]
           },
           {
             "ConnectionState": "Reachable",
             "StartTime": "2018-01-11T23:54:05Z",
             "EvaluationState": "Completed",
             "Hops": [
               {
                 "Type": "Source",
                 "Id": "3dbec7e8-a37f-4acd-bc5f-86918fffba0e",
                 "Address": "10.1.1.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "1a87cf61-1be6-4add-bba7-f84afbcf3726"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "1a87cf61-1be6-4add-bba7-f84afbcf3726",
                 "Address": "10.1.2.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/fwNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "070c0740-308e-43ba-b72f-5d8d5a6537ec"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "070c0740-308e-43ba-b72f-5d8d5a6537ec",
                 "Address": "10.1.3.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/auNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "760182e1-c88d-4cfc-a711-65e7e622a67a"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualNetwork",
                 "Id": "760182e1-c88d-4cfc-a711-65e7e622a67a",
                 "Address": "10.1.4.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/dbNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [],
                 "Issues": []
               }
             ]
           }
         ]
```

<span data-ttu-id="e20a0-114">이 예제에서는 지정 된 연결 모니터의 최신 연결 상태를 쿼리 합니다.</span><span class="sxs-lookup"><span data-stu-id="e20a0-114">In this example we query the most recent connection states of the specified connection monitor.</span></span>

## <span data-ttu-id="e20a0-115">변수</span><span class="sxs-lookup"><span data-stu-id="e20a0-115">PARAMETERS</span></span>

### <span data-ttu-id="e20a0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e20a0-116">-AsJob</span></span>
<span data-ttu-id="e20a0-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e20a0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e20a0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e20a0-118">-DefaultProfile</span></span>
<span data-ttu-id="e20a0-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e20a0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e20a0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e20a0-120">-InputObject</span></span>
<span data-ttu-id="e20a0-121">연결 모니터 개체</span><span class="sxs-lookup"><span data-stu-id="e20a0-121">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e20a0-122">-위치</span><span class="sxs-lookup"><span data-stu-id="e20a0-122">-Location</span></span>
<span data-ttu-id="e20a0-123">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e20a0-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="e20a0-124">-이름</span><span class="sxs-lookup"><span data-stu-id="e20a0-124">-Name</span></span>
<span data-ttu-id="e20a0-125">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e20a0-125">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e20a0-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e20a0-126">-NetworkWatcher</span></span>
<span data-ttu-id="e20a0-127">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="e20a0-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="e20a0-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e20a0-128">-NetworkWatcherName</span></span>
<span data-ttu-id="e20a0-129">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e20a0-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="e20a0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e20a0-130">-ResourceGroupName</span></span>
<span data-ttu-id="e20a0-131">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e20a0-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e20a0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e20a0-132">-ResourceId</span></span>
<span data-ttu-id="e20a0-133">연결 모니터의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e20a0-133">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="e20a0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e20a0-134">CommonParameters</span></span>
<span data-ttu-id="e20a0-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e20a0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e20a0-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e20a0-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e20a0-137">입력</span><span class="sxs-lookup"><span data-stu-id="e20a0-137">INPUTS</span></span>

### <span data-ttu-id="e20a0-138">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e20a0-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="e20a0-139">Microsoft. Azure. PSConnectionMonitorResult.</span><span class="sxs-lookup"><span data-stu-id="e20a0-139">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="e20a0-140">출력</span><span class="sxs-lookup"><span data-stu-id="e20a0-140">OUTPUTS</span></span>

### <span data-ttu-id="e20a0-141">Microsoft. 네트워크. PSConnectionMonitorQueryResult</span><span class="sxs-lookup"><span data-stu-id="e20a0-141">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorQueryResult</span></span>

## <span data-ttu-id="e20a0-142">상속자</span><span class="sxs-lookup"><span data-stu-id="e20a0-142">NOTES</span></span>
<span data-ttu-id="e20a0-143">키워드: azure, azurerm, arm, 리소스, 연결, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결 모니터</span><span class="sxs-lookup"><span data-stu-id="e20a0-143">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="e20a0-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e20a0-144">RELATED LINKS</span></span>

[<span data-ttu-id="e20a0-145">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e20a0-145">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="e20a0-146">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e20a0-146">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="e20a0-147">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e20a0-147">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="e20a0-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e20a0-148">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="e20a0-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e20a0-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="e20a0-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e20a0-150">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="e20a0-151">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e20a0-151">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="e20a0-152">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e20a0-152">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="e20a0-153">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e20a0-153">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="e20a0-154">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e20a0-154">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="e20a0-155">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e20a0-155">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="e20a0-156">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e20a0-156">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="e20a0-157">새로운 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e20a0-157">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="e20a0-158">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e20a0-158">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="e20a0-159">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e20a0-159">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="e20a0-160">시작-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e20a0-160">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="e20a0-161">중지-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e20a0-161">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="e20a0-162">제거-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e20a0-162">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
