---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: c3d1e7e3a76a2561c77c8d580b7365f8fd2e6fee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875540"
---
# <span data-ttu-id="9b036-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9b036-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="9b036-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b036-102">SYNOPSIS</span></span>
<span data-ttu-id="9b036-103">이전에 실행 되었거나 현재 실행 중인 문제 해결 작업의 문제 해결 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b036-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="9b036-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b036-104">SYNTAX</span></span>

### <span data-ttu-id="9b036-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="9b036-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b036-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="9b036-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b036-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9b036-107">DESCRIPTION</span></span>
<span data-ttu-id="9b036-108">Get-AzNetworkWatcherTroubleshootingResult cmdlet은 이전에 실행 되거나 현재 실행 중인 Start-AzNetworkWatcherResourceTroubleshooting 작업의 문제 해결 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b036-108">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="9b036-109">현재 문제 해결 작업이 진행 중인 경우이 작업을 완료 하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b036-109">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="9b036-110">현재 가상 네트워크 게이트웨이 및 연결이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b036-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="9b036-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9b036-111">EXAMPLES</span></span>

### <span data-ttu-id="9b036-112">---예제 1: 가상 네트워크 게이트웨이에서 문제 해결을 시작 하 고 결과 검색---</span><span class="sxs-lookup"><span data-stu-id="9b036-112">--- Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="9b036-113">위의 샘플에서는 가상 네트워크 게이트웨이에서 문제 해결을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b036-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="9b036-114">작업을 완료 하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b036-114">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="9b036-115">문제 해결이 시작 된 후에는이 통화의 결과를 검색 하기 위해 리소스에 대 한 Get-AzNetworkWatcherTroubleshootingResult 호출이 이루어집니다.</span><span class="sxs-lookup"><span data-stu-id="9b036-115">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="9b036-116">변수</span><span class="sxs-lookup"><span data-stu-id="9b036-116">PARAMETERS</span></span>

### <span data-ttu-id="9b036-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b036-117">-DefaultProfile</span></span>
<span data-ttu-id="9b036-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b036-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b036-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9b036-119">-NetworkWatcher</span></span>
<span data-ttu-id="9b036-120">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="9b036-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="9b036-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9b036-121">-NetworkWatcherName</span></span>
<span data-ttu-id="9b036-122">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b036-122">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b036-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b036-123">-ResourceGroupName</span></span>
<span data-ttu-id="9b036-124">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b036-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9b036-125">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="9b036-125">-TargetResourceId</span></span>
<span data-ttu-id="9b036-126">대상 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9b036-126">The target resource ID.</span></span>

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

### <span data-ttu-id="9b036-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b036-127">CommonParameters</span></span>
<span data-ttu-id="9b036-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b036-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b036-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b036-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b036-130">입력</span><span class="sxs-lookup"><span data-stu-id="9b036-130">INPUTS</span></span>

### <span data-ttu-id="9b036-131">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9b036-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="9b036-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9b036-132">System.String</span></span>

## <span data-ttu-id="9b036-133">출력</span><span class="sxs-lookup"><span data-stu-id="9b036-133">OUTPUTS</span></span>

### <span data-ttu-id="9b036-134">PSViewNsgRules에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9b036-134">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="9b036-135">상속자</span><span class="sxs-lookup"><span data-stu-id="9b036-135">NOTES</span></span>
<span data-ttu-id="9b036-136">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 문제 해결, VPN, 연결</span><span class="sxs-lookup"><span data-stu-id="9b036-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="9b036-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b036-137">RELATED LINKS</span></span>

[<span data-ttu-id="9b036-138">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9b036-138">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="9b036-139">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9b036-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="9b036-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9b036-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="9b036-141">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9b036-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="9b036-142">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9b036-142">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9b036-143">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9b036-143">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="9b036-144">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9b036-144">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9b036-145">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9b036-145">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9b036-146">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9b036-146">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9b036-147">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9b036-147">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="9b036-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9b036-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="9b036-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9b036-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9b036-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9b036-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)
