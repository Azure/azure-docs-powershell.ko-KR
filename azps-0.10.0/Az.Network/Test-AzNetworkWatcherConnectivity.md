---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
ms.openlocfilehash: f6c25d58588d0b75f67163c50cfa91a6f8e982da
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876516"
---
# <span data-ttu-id="3c7c6-101">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="3c7c6-101">Test-AzNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="3c7c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c7c6-102">SYNOPSIS</span></span>
<span data-ttu-id="3c7c6-103">지정 된 원본 VM 및 대상에 대 한 연결 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c6-103">Returns connectivity information for a specified source VM and a destination.</span></span>

## <span data-ttu-id="3c7c6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3c7c6-104">SYNTAX</span></span>

### <span data-ttu-id="3c7c6-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="3c7c6-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c7c6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="3c7c6-106">SetByName</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String>
 -SourceId <String> [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>]
 [-DestinationPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c7c6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3c7c6-107">DESCRIPTION</span></span>
<span data-ttu-id="3c7c6-108">Test-AzNetworkWatcherConnectivity cmdlet은 지정 된 원본 VM 및 대상에 대 한 연결 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c6-108">The Test-AzNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="3c7c6-109">원본과 대상 간의 연결을 설정할 수 없는 경우 cmdlet은 문제에 대 한 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c6-109">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="3c7c6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3c7c6-110">EXAMPLES</span></span>

### <span data-ttu-id="3c7c6-111">---------------예제 1: VM에서 웹 사이트로 네트워크 감시자 연결 테스트---------------</span><span class="sxs-lookup"><span data-stu-id="3c7c6-111">---------------  Example 1: Test Network Watcher Connectivity from a VM to a website  ---------------</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="3c7c6-112">이 예제에서는 Azure의 VM에서 www.bing.com에 대 한 연결을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c6-112">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="3c7c6-113">변수</span><span class="sxs-lookup"><span data-stu-id="3c7c6-113">PARAMETERS</span></span>

### <span data-ttu-id="3c7c6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c7c6-114">-AsJob</span></span>
<span data-ttu-id="3c7c6-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3c7c6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c7c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c7c6-116">-DefaultProfile</span></span>
<span data-ttu-id="3c7c6-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c7c6-118">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="3c7c6-118">-DestinationAddress</span></span>
<span data-ttu-id="3c7c6-119">연결을 시도 하는 데 사용할 리소스의 IP 주소 또는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c6-119">The IP address or URI the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="3c7c6-120">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="3c7c6-120">-DestinationId</span></span>
<span data-ttu-id="3c7c6-121">연결 시도가 수행 될 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c6-121">The ID of the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="3c7c6-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="3c7c6-122">-DestinationPort</span></span>
<span data-ttu-id="3c7c6-123">확인 연결을 수행할 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c6-123">Port on which check connectivity will be performed.</span></span>

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

### <span data-ttu-id="3c7c6-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3c7c6-124">-NetworkWatcher</span></span>
<span data-ttu-id="3c7c6-125">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="3c7c6-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="3c7c6-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3c7c6-126">-NetworkWatcherName</span></span>
<span data-ttu-id="3c7c6-127">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c6-127">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7c6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c7c6-128">-ResourceGroupName</span></span>
<span data-ttu-id="3c7c6-129">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c6-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3c7c6-130">-SourceId</span><span class="sxs-lookup"><span data-stu-id="3c7c6-130">-SourceId</span></span>
<span data-ttu-id="3c7c6-131">연결 검사가 시작 되는 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c6-131">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="3c7c6-132">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="3c7c6-132">-SourcePort</span></span>
<span data-ttu-id="3c7c6-133">연결 검사가 수행 되는 원본 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c6-133">The source port from which a connectivity check will be performed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7c6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c7c6-134">CommonParameters</span></span>
<span data-ttu-id="3c7c6-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c7c6-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c7c6-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c7c6-137">입력</span><span class="sxs-lookup"><span data-stu-id="3c7c6-137">INPUTS</span></span>

### <span data-ttu-id="3c7c6-138">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3c7c6-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="3c7c6-139">시스템. i i a 시스템. Int32</span><span class="sxs-lookup"><span data-stu-id="3c7c6-139">System.String System.Int32</span></span>

## <span data-ttu-id="3c7c6-140">출력</span><span class="sxs-lookup"><span data-stu-id="3c7c6-140">OUTPUTS</span></span>

### <span data-ttu-id="3c7c6-141">PSConnectivityInformation에 대 한.</span><span class="sxs-lookup"><span data-stu-id="3c7c6-141">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="3c7c6-142">상속자</span><span class="sxs-lookup"><span data-stu-id="3c7c6-142">NOTES</span></span>
<span data-ttu-id="3c7c6-143">키워드: azure, azurerm, arm, 리소스, 연결, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자</span><span class="sxs-lookup"><span data-stu-id="3c7c6-143">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="3c7c6-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3c7c6-144">RELATED LINKS</span></span>

<span data-ttu-id="3c7c6-145">[새로운 AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [제거-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="3c7c6-145">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="3c7c6-146">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="3c7c6-146">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="3c7c6-147">[새로운 AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [새로운 AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [제거-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [중지-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="3c7c6-147">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>
