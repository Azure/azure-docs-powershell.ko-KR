---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: 20d350bec1e344ed359a62f0026c490361140fcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530013"
---
# <span data-ttu-id="4d6bc-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4d6bc-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="4d6bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d6bc-102">SYNOPSIS</span></span>
<span data-ttu-id="4d6bc-103">이전에 실행 되었거나 현재 실행 중인 문제 해결 작업의 문제 해결 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d6bc-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d6bc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4d6bc-104">SYNTAX</span></span>

### <span data-ttu-id="4d6bc-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="4d6bc-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d6bc-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4d6bc-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d6bc-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4d6bc-107">DESCRIPTION</span></span>
<span data-ttu-id="4d6bc-108">Get-AzureRmNetworkWatcherTroubleshootingResult cmdlet은 이전에 실행 되거나 현재 실행 중인 Start-AzureRmNetworkWatcherResourceTroubleshooting 작업의 문제 해결 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d6bc-108">The Get-AzureRmNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzureRmNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="4d6bc-109">현재 문제 해결 작업이 진행 중인 경우이 작업을 완료 하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d6bc-109">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="4d6bc-110">현재 가상 네트워크 게이트웨이 및 연결이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d6bc-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="4d6bc-111">예제의</span><span class="sxs-lookup"><span data-stu-id="4d6bc-111">EXAMPLES</span></span>

### <span data-ttu-id="4d6bc-112">---예제 1: 가상 네트워크 게이트웨이에서 문제 해결을 시작 하 고 결과 검색---</span><span class="sxs-lookup"><span data-stu-id="4d6bc-112">--- Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="4d6bc-113">위의 샘플에서는 가상 네트워크 게이트웨이에서 문제 해결을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d6bc-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="4d6bc-114">작업을 완료 하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d6bc-114">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="4d6bc-115">문제 해결이 시작 된 후에는이 통화의 결과를 검색 하기 위해 리소스에 대 한 Get-AzureRmNetworkWatcherTroubleshootingResult 호출이 이루어집니다.</span><span class="sxs-lookup"><span data-stu-id="4d6bc-115">After troubleshooting has started, a Get-AzureRmNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="4d6bc-116">변수</span><span class="sxs-lookup"><span data-stu-id="4d6bc-116">PARAMETERS</span></span>

### <span data-ttu-id="4d6bc-117">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4d6bc-117">-NetworkWatcher</span></span>
<span data-ttu-id="4d6bc-118">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="4d6bc-118">The network watcher resource.</span></span>

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

### <span data-ttu-id="4d6bc-119">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4d6bc-119">-NetworkWatcherName</span></span>
<span data-ttu-id="4d6bc-120">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d6bc-120">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d6bc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d6bc-121">-ResourceGroupName</span></span>
<span data-ttu-id="4d6bc-122">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d6bc-122">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4d6bc-123">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="4d6bc-123">-TargetResourceId</span></span>
<span data-ttu-id="4d6bc-124">대상 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4d6bc-124">The target resource ID.</span></span>

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

### <span data-ttu-id="4d6bc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d6bc-125">-DefaultProfile</span></span>
<span data-ttu-id="4d6bc-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d6bc-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d6bc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d6bc-127">CommonParameters</span></span>
<span data-ttu-id="4d6bc-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d6bc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d6bc-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d6bc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d6bc-130">입력</span><span class="sxs-lookup"><span data-stu-id="4d6bc-130">INPUTS</span></span>

### <span data-ttu-id="4d6bc-131">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4d6bc-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="4d6bc-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4d6bc-132">System.String</span></span>

## <span data-ttu-id="4d6bc-133">출력</span><span class="sxs-lookup"><span data-stu-id="4d6bc-133">OUTPUTS</span></span>

### <span data-ttu-id="4d6bc-134">PSViewNsgRules에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4d6bc-134">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="4d6bc-135">상속자</span><span class="sxs-lookup"><span data-stu-id="4d6bc-135">NOTES</span></span>
<span data-ttu-id="4d6bc-136">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 문제 해결, VPN, 연결</span><span class="sxs-lookup"><span data-stu-id="4d6bc-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="4d6bc-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d6bc-137">RELATED LINKS</span></span>

[<span data-ttu-id="4d6bc-138">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4d6bc-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4d6bc-139">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4d6bc-139">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4d6bc-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4d6bc-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4d6bc-141">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4d6bc-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4d6bc-142">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4d6bc-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4d6bc-143">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4d6bc-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="4d6bc-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4d6bc-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4d6bc-145">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4d6bc-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4d6bc-146">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4d6bc-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4d6bc-147">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4d6bc-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="4d6bc-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4d6bc-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="4d6bc-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4d6bc-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4d6bc-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4d6bc-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)
