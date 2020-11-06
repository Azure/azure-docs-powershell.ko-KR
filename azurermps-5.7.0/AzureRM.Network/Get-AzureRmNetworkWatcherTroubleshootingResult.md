---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: ef730b8ee6e6c35408b9d57d9dc23b0ab51a63d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528083"
---
# <span data-ttu-id="c0186-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c0186-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="c0186-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0186-102">SYNOPSIS</span></span>
<span data-ttu-id="c0186-103">이전에 실행 되었거나 현재 실행 중인 문제 해결 작업의 문제 해결 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c0186-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0186-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c0186-104">SYNTAX</span></span>

### <span data-ttu-id="c0186-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="c0186-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0186-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c0186-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0186-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c0186-107">DESCRIPTION</span></span>
<span data-ttu-id="c0186-108">Get-AzureRmNetworkWatcherTroubleshootingResult cmdlet은 이전에 실행 되거나 현재 실행 중인 Start-AzureRmNetworkWatcherResourceTroubleshooting 작업의 문제 해결 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c0186-108">The Get-AzureRmNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzureRmNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="c0186-109">현재 문제 해결 작업이 진행 중인 경우이 작업을 완료 하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0186-109">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="c0186-110">현재 가상 네트워크 게이트웨이 및 연결이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0186-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="c0186-111">예제의</span><span class="sxs-lookup"><span data-stu-id="c0186-111">EXAMPLES</span></span>

### <span data-ttu-id="c0186-112">---예제 1: 가상 네트워크 게이트웨이에서 문제 해결을 시작 하 고 결과 검색---</span><span class="sxs-lookup"><span data-stu-id="c0186-112">--- Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="c0186-113">위의 샘플에서는 가상 네트워크 게이트웨이에서 문제 해결을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0186-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="c0186-114">작업을 완료 하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0186-114">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="c0186-115">문제 해결이 시작 된 후에는이 통화의 결과를 검색 하기 위해 리소스에 대 한 Get-AzureRmNetworkWatcherTroubleshootingResult 호출이 이루어집니다.</span><span class="sxs-lookup"><span data-stu-id="c0186-115">After troubleshooting has started, a Get-AzureRmNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="c0186-116">변수</span><span class="sxs-lookup"><span data-stu-id="c0186-116">PARAMETERS</span></span>

### <span data-ttu-id="c0186-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0186-117">-DefaultProfile</span></span>
<span data-ttu-id="c0186-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c0186-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0186-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0186-119">-NetworkWatcher</span></span>
<span data-ttu-id="c0186-120">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="c0186-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="c0186-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c0186-121">-NetworkWatcherName</span></span>
<span data-ttu-id="c0186-122">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0186-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="c0186-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0186-123">-ResourceGroupName</span></span>
<span data-ttu-id="c0186-124">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0186-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c0186-125">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c0186-125">-TargetResourceId</span></span>
<span data-ttu-id="c0186-126">대상 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c0186-126">The target resource ID.</span></span>

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

### <span data-ttu-id="c0186-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0186-127">CommonParameters</span></span>
<span data-ttu-id="c0186-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0186-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0186-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0186-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0186-130">입력</span><span class="sxs-lookup"><span data-stu-id="c0186-130">INPUTS</span></span>

### <span data-ttu-id="c0186-131">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0186-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="c0186-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c0186-132">System.String</span></span>

## <span data-ttu-id="c0186-133">출력</span><span class="sxs-lookup"><span data-stu-id="c0186-133">OUTPUTS</span></span>

### <span data-ttu-id="c0186-134">PSViewNsgRules에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c0186-134">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="c0186-135">상속자</span><span class="sxs-lookup"><span data-stu-id="c0186-135">NOTES</span></span>
<span data-ttu-id="c0186-136">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 문제 해결, VPN, 연결</span><span class="sxs-lookup"><span data-stu-id="c0186-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="c0186-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0186-137">RELATED LINKS</span></span>

[<span data-ttu-id="c0186-138">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c0186-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c0186-139">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0186-139">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c0186-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0186-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c0186-141">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0186-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c0186-142">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0186-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c0186-143">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c0186-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="c0186-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0186-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c0186-145">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0186-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c0186-146">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0186-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c0186-147">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c0186-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="c0186-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c0186-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="c0186-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c0186-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c0186-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c0186-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)
