---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: a72f494518b3a511eac3e4b1a92330f666bbca64
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876526"
---
# <span data-ttu-id="93d3b-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="93d3b-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="93d3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="93d3b-103">Azure에서 네트워킹 리소스에 대 한 문제 해결을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d3b-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="93d3b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="93d3b-104">SYNTAX</span></span>

### <span data-ttu-id="93d3b-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="93d3b-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93d3b-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="93d3b-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93d3b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="93d3b-107">DESCRIPTION</span></span>
<span data-ttu-id="93d3b-108">Start-AzNetworkWatcherResourceTroubleshooting cmdlet은 Azure에서 네트워킹 리소스에 대 한 문제 해결을 시작 하 고 잠재적인 문제 및 완화에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d3b-108">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="93d3b-109">현재 가상 네트워크 게이트웨이 및 연결이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="93d3b-109">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="93d3b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="93d3b-110">EXAMPLES</span></span>

### <span data-ttu-id="93d3b-111">---예제 1: 가상 네트워크 게이트웨이에서 문제 해결 시작---</span><span class="sxs-lookup"><span data-stu-id="93d3b-111">--- Example 1: Start Troubleshooting on a Virtual Network Gateway ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="93d3b-112">위의 샘플에서는 가상 네트워크 게이트웨이에서 문제 해결을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d3b-112">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="93d3b-113">작업을 완료 하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93d3b-113">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="93d3b-114">변수</span><span class="sxs-lookup"><span data-stu-id="93d3b-114">PARAMETERS</span></span>

### <span data-ttu-id="93d3b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93d3b-115">-DefaultProfile</span></span>
<span data-ttu-id="93d3b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="93d3b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93d3b-117">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="93d3b-117">-NetworkWatcher</span></span>
<span data-ttu-id="93d3b-118">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="93d3b-118">The network watcher resource.</span></span>

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

### <span data-ttu-id="93d3b-119">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="93d3b-119">-NetworkWatcherName</span></span>
<span data-ttu-id="93d3b-120">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93d3b-120">The name of network watcher.</span></span>

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

### <span data-ttu-id="93d3b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93d3b-121">-ResourceGroupName</span></span>
<span data-ttu-id="93d3b-122">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93d3b-122">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="93d3b-123">-StorageId</span><span class="sxs-lookup"><span data-stu-id="93d3b-123">-StorageId</span></span>
<span data-ttu-id="93d3b-124">저장소 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="93d3b-124">The storage ID.</span></span>

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

### <span data-ttu-id="93d3b-125">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="93d3b-125">-StoragePath</span></span>
<span data-ttu-id="93d3b-126">저장소 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="93d3b-126">The storage path.</span></span>

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

### <span data-ttu-id="93d3b-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="93d3b-127">-TargetResourceId</span></span>
<span data-ttu-id="93d3b-128">문제를 해결할 리소스의 리소스 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d3b-128">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="93d3b-129">예제 형식: "/subscriptions/$ {subscriptionId}/resourceGroups//$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {connectionName}"</span><span class="sxs-lookup"><span data-stu-id="93d3b-129">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="93d3b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93d3b-130">CommonParameters</span></span>
<span data-ttu-id="93d3b-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="93d3b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93d3b-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93d3b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93d3b-133">입력</span><span class="sxs-lookup"><span data-stu-id="93d3b-133">INPUTS</span></span>

### <span data-ttu-id="93d3b-134">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="93d3b-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="93d3b-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="93d3b-135">System.String</span></span>

## <span data-ttu-id="93d3b-136">출력</span><span class="sxs-lookup"><span data-stu-id="93d3b-136">OUTPUTS</span></span>

### <span data-ttu-id="93d3b-137">PSViewNsgRules에 대 한.</span><span class="sxs-lookup"><span data-stu-id="93d3b-137">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="93d3b-138">상속자</span><span class="sxs-lookup"><span data-stu-id="93d3b-138">NOTES</span></span>
<span data-ttu-id="93d3b-139">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 문제 해결, VPN, 연결</span><span class="sxs-lookup"><span data-stu-id="93d3b-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="93d3b-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93d3b-140">RELATED LINKS</span></span>

[<span data-ttu-id="93d3b-141">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="93d3b-141">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="93d3b-142">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="93d3b-142">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="93d3b-143">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="93d3b-143">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="93d3b-144">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="93d3b-144">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="93d3b-145">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="93d3b-145">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="93d3b-146">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="93d3b-146">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="93d3b-147">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="93d3b-147">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="93d3b-148">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="93d3b-148">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="93d3b-149">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="93d3b-149">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="93d3b-150">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="93d3b-150">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="93d3b-151">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="93d3b-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="93d3b-152">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="93d3b-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="93d3b-153">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="93d3b-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)
