---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: f220f029b25963fa07d582b6ddd70b572791924a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535459"
---
# <span data-ttu-id="f6ec6-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f6ec6-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="f6ec6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6ec6-102">SYNOPSIS</span></span>
<span data-ttu-id="f6ec6-103">Azure에서 네트워킹 리소스에 대 한 문제 해결을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6ec6-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6ec6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f6ec6-104">SYNTAX</span></span>

### <span data-ttu-id="f6ec6-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="f6ec6-105">SetByResource (Default)</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6ec6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f6ec6-106">SetByName</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6ec6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f6ec6-107">DESCRIPTION</span></span>
<span data-ttu-id="f6ec6-108">Start-AzureRmNetworkWatcherResourceTroubleshooting cmdlet은 Azure에서 네트워킹 리소스에 대 한 문제 해결을 시작 하 고 잠재적인 문제 및 완화에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6ec6-108">The Start-AzureRmNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="f6ec6-109">현재 가상 네트워크 게이트웨이 및 연결이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6ec6-109">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="f6ec6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f6ec6-110">EXAMPLES</span></span>

### <span data-ttu-id="f6ec6-111">---예제 1: 가상 네트워크 게이트웨이에서 문제 해결 시작---</span><span class="sxs-lookup"><span data-stu-id="f6ec6-111">--- Example 1: Start Troubleshooting on a Virtual Network Gateway ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="f6ec6-112">위의 샘플에서는 가상 네트워크 게이트웨이에서 문제 해결을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6ec6-112">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="f6ec6-113">작업을 완료 하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6ec6-113">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="f6ec6-114">변수</span><span class="sxs-lookup"><span data-stu-id="f6ec6-114">PARAMETERS</span></span>

### <span data-ttu-id="f6ec6-115">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f6ec6-115">-NetworkWatcher</span></span>
<span data-ttu-id="f6ec6-116">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="f6ec6-116">The network watcher resource.</span></span>

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

### <span data-ttu-id="f6ec6-117">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f6ec6-117">-NetworkWatcherName</span></span>
<span data-ttu-id="f6ec6-118">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f6ec6-118">The name of network watcher.</span></span>

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

### <span data-ttu-id="f6ec6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6ec6-119">-ResourceGroupName</span></span>
<span data-ttu-id="f6ec6-120">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f6ec6-120">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f6ec6-121">-StorageId</span><span class="sxs-lookup"><span data-stu-id="f6ec6-121">-StorageId</span></span>
<span data-ttu-id="f6ec6-122">저장소 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f6ec6-122">The storage ID.</span></span>

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

### <span data-ttu-id="f6ec6-123">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="f6ec6-123">-StoragePath</span></span>
<span data-ttu-id="f6ec6-124">저장소 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="f6ec6-124">The storage path.</span></span>

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

### <span data-ttu-id="f6ec6-125">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f6ec6-125">-TargetResourceId</span></span>
<span data-ttu-id="f6ec6-126">문제를 해결할 리소스의 리소스 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6ec6-126">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="f6ec6-127">예제 형식: "/subscriptions/$ {subscriptionId}/resourceGroups//$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {connectionName}"</span><span class="sxs-lookup"><span data-stu-id="f6ec6-127">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="f6ec6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6ec6-128">-DefaultProfile</span></span>
<span data-ttu-id="f6ec6-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f6ec6-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6ec6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6ec6-130">CommonParameters</span></span>
<span data-ttu-id="f6ec6-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6ec6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6ec6-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6ec6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6ec6-133">입력</span><span class="sxs-lookup"><span data-stu-id="f6ec6-133">INPUTS</span></span>

### <span data-ttu-id="f6ec6-134">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f6ec6-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f6ec6-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f6ec6-135">System.String</span></span>

## <span data-ttu-id="f6ec6-136">출력</span><span class="sxs-lookup"><span data-stu-id="f6ec6-136">OUTPUTS</span></span>

### <span data-ttu-id="f6ec6-137">PSViewNsgRules에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f6ec6-137">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="f6ec6-138">상속자</span><span class="sxs-lookup"><span data-stu-id="f6ec6-138">NOTES</span></span>
<span data-ttu-id="f6ec6-139">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 문제 해결, VPN, 연결</span><span class="sxs-lookup"><span data-stu-id="f6ec6-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="f6ec6-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6ec6-140">RELATED LINKS</span></span>

[<span data-ttu-id="f6ec6-141">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f6ec6-141">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="f6ec6-142">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f6ec6-142">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f6ec6-143">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f6ec6-143">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f6ec6-144">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f6ec6-144">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f6ec6-145">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f6ec6-145">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f6ec6-146">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f6ec6-146">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="f6ec6-147">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f6ec6-147">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f6ec6-148">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f6ec6-148">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f6ec6-149">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f6ec6-149">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f6ec6-150">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f6ec6-150">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="f6ec6-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f6ec6-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="f6ec6-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f6ec6-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f6ec6-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f6ec6-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)
