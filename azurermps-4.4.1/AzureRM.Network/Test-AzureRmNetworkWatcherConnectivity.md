---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherConnectivity.md
ms.openlocfilehash: 4e9c99f2985be335f2750e500ee0c01394195c39
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710974"
---
# <span data-ttu-id="0f1ce-101">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="0f1ce-101">Test-AzureRmNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="0f1ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f1ce-102">SYNOPSIS</span></span>
<span data-ttu-id="0f1ce-103">지정 된 원본 VM 및 대상에 대 한 연결 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f1ce-103">Returns connectivity information for a specified source VM and a destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f1ce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0f1ce-104">SYNTAX</span></span>

### <span data-ttu-id="0f1ce-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="0f1ce-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f1ce-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="0f1ce-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String>
 -SourceId <String> [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>]
 [-DestinationPort <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f1ce-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0f1ce-107">DESCRIPTION</span></span>
<span data-ttu-id="0f1ce-108">Test-AzureRmNetworkWatcherConnectivity cmdlet은 지정 된 원본 VM 및 대상에 대 한 연결 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f1ce-108">The Test-AzureRmNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="0f1ce-109">원본과 대상 간의 연결을 설정할 수 없는 경우 cmdlet은 문제에 대 한 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f1ce-109">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="0f1ce-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0f1ce-110">EXAMPLES</span></span>

### <span data-ttu-id="0f1ce-111">---------------예제 1: VM에서 웹 사이트로 네트워크 감시자 연결 테스트---------------</span><span class="sxs-lookup"><span data-stu-id="0f1ce-111">---------------  Example 1: Test Network Watcher Connectivity from a VM to a website  ---------------</span></span>
<span data-ttu-id="0f1ce-112">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="0f1ce-112">@{paragraph=PS C:\\\>}</span></span>










```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80


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

<span data-ttu-id="0f1ce-113">이 예제에서는 Azure의 VM에서 www.bing.com에 대 한 연결을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f1ce-113">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="0f1ce-114">변수</span><span class="sxs-lookup"><span data-stu-id="0f1ce-114">PARAMETERS</span></span>

### <span data-ttu-id="0f1ce-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="0f1ce-115">-DestinationAddress</span></span>
<span data-ttu-id="0f1ce-116">연결을 시도 하는 데 사용할 리소스의 IP 주소 또는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="0f1ce-116">The IP address or URI the resource to which a connection attempt will be made.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f1ce-117">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="0f1ce-117">-DestinationId</span></span>
<span data-ttu-id="0f1ce-118">연결 시도가 수행 될 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0f1ce-118">The ID of the resource to which a connection attempt will be made.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f1ce-119">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="0f1ce-119">-DestinationPort</span></span>
<span data-ttu-id="0f1ce-120">확인 연결을 수행할 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="0f1ce-120">Port on which check connectivity will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f1ce-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0f1ce-121">-NetworkWatcher</span></span>
<span data-ttu-id="0f1ce-122">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="0f1ce-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="0f1ce-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0f1ce-123">-NetworkWatcherName</span></span>
<span data-ttu-id="0f1ce-124">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0f1ce-124">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f1ce-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f1ce-125">-ResourceGroupName</span></span>
<span data-ttu-id="0f1ce-126">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0f1ce-126">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f1ce-127">-SourceId</span><span class="sxs-lookup"><span data-stu-id="0f1ce-127">-SourceId</span></span>
<span data-ttu-id="0f1ce-128">연결 검사가 시작 되는 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0f1ce-128">The ID of the resource from which a connectivity check will be initiated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f1ce-129">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="0f1ce-129">-SourcePort</span></span>
<span data-ttu-id="0f1ce-130">연결 검사가 수행 되는 원본 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="0f1ce-130">The source port from which a connectivity check will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f1ce-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f1ce-131">-DefaultProfile</span></span>
<span data-ttu-id="0f1ce-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0f1ce-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f1ce-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f1ce-133">CommonParameters</span></span>
<span data-ttu-id="0f1ce-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f1ce-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f1ce-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f1ce-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f1ce-136">입력</span><span class="sxs-lookup"><span data-stu-id="0f1ce-136">INPUTS</span></span>

### <span data-ttu-id="0f1ce-137">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0f1ce-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="0f1ce-138">시스템. i i a 시스템. Int32</span><span class="sxs-lookup"><span data-stu-id="0f1ce-138">System.String System.Int32</span></span>

## <span data-ttu-id="0f1ce-139">출력</span><span class="sxs-lookup"><span data-stu-id="0f1ce-139">OUTPUTS</span></span>

### <span data-ttu-id="0f1ce-140">PSConnectivityInformation에 대 한.</span><span class="sxs-lookup"><span data-stu-id="0f1ce-140">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="0f1ce-141">상속자</span><span class="sxs-lookup"><span data-stu-id="0f1ce-141">NOTES</span></span>
<span data-ttu-id="0f1ce-142">키워드: azure, azurerm, arm, 리소스, 연결, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자</span><span class="sxs-lookup"><span data-stu-id="0f1ce-142">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="0f1ce-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f1ce-143">RELATED LINKS</span></span>

<span data-ttu-id="0f1ce-144">[새로운 AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [제거-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="0f1ce-144">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="0f1ce-145">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="0f1ce-145">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="0f1ce-146">[새로운 AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [새로운 AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [제거-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [중지-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="0f1ce-146">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>
