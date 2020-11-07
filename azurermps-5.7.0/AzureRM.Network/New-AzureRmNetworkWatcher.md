---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
ms.openlocfilehash: e1e0714c070c47d4be2cff0893a4428bdf0949c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711154"
---
# <span data-ttu-id="7cdbb-101">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7cdbb-101">New-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="7cdbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cdbb-102">SYNOPSIS</span></span>
<span data-ttu-id="7cdbb-103">새 네트워크 감시자 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7cdbb-103">Creates a new Network Watcher resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cdbb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7cdbb-104">SYNTAX</span></span>

```
New-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cdbb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7cdbb-105">DESCRIPTION</span></span>
<span data-ttu-id="7cdbb-106">New-AzureRmNetworkWatcher cmdlet은 새 네트워크 감시자 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7cdbb-106">The New-AzureRmNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="7cdbb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7cdbb-107">EXAMPLES</span></span>

### <span data-ttu-id="7cdbb-108">예제 1: 네트워크 감시자 만들기</span><span class="sxs-lookup"><span data-stu-id="7cdbb-108">Example 1: Create a Network Watcher</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="7cdbb-109">이 예제에서는 새로 만든 리소스 그룹 내에 새 네트워크 감시자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7cdbb-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="7cdbb-110">구독 당 지역 당 하나의 네트워크 감시자만 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7cdbb-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="7cdbb-111">변수</span><span class="sxs-lookup"><span data-stu-id="7cdbb-111">PARAMETERS</span></span>

### <span data-ttu-id="7cdbb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cdbb-112">-DefaultProfile</span></span>
<span data-ttu-id="7cdbb-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7cdbb-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cdbb-114">-위치</span><span class="sxs-lookup"><span data-stu-id="7cdbb-114">-Location</span></span>
<span data-ttu-id="7cdbb-115">Location.</span><span class="sxs-lookup"><span data-stu-id="7cdbb-115">Location.</span></span>

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

### <span data-ttu-id="7cdbb-116">-이름</span><span class="sxs-lookup"><span data-stu-id="7cdbb-116">-Name</span></span>
<span data-ttu-id="7cdbb-117">네트워크 감시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7cdbb-117">The network watcher name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cdbb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cdbb-118">-ResourceGroupName</span></span>
<span data-ttu-id="7cdbb-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7cdbb-119">The resource group name.</span></span>

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

### <span data-ttu-id="7cdbb-120">태그</span><span class="sxs-lookup"><span data-stu-id="7cdbb-120">-Tag</span></span>
<span data-ttu-id="7cdbb-121">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="7cdbb-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7cdbb-122">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="7cdbb-122">For example:</span></span>

<span data-ttu-id="7cdbb-123">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7cdbb-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cdbb-124">-확인</span><span class="sxs-lookup"><span data-stu-id="7cdbb-124">-Confirm</span></span>
<span data-ttu-id="7cdbb-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cdbb-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cdbb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cdbb-126">-WhatIf</span></span>
<span data-ttu-id="7cdbb-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7cdbb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cdbb-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7cdbb-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cdbb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cdbb-129">CommonParameters</span></span>
<span data-ttu-id="7cdbb-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cdbb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cdbb-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cdbb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cdbb-132">입력</span><span class="sxs-lookup"><span data-stu-id="7cdbb-132">INPUTS</span></span>

### <span data-ttu-id="7cdbb-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7cdbb-133">System.String</span></span>
<span data-ttu-id="7cdbb-134">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="7cdbb-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7cdbb-135">출력</span><span class="sxs-lookup"><span data-stu-id="7cdbb-135">OUTPUTS</span></span>

### <span data-ttu-id="7cdbb-136">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7cdbb-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="7cdbb-137">상속자</span><span class="sxs-lookup"><span data-stu-id="7cdbb-137">NOTES</span></span>
<span data-ttu-id="7cdbb-138">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자</span><span class="sxs-lookup"><span data-stu-id="7cdbb-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="7cdbb-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7cdbb-139">RELATED LINKS</span></span>

[<span data-ttu-id="7cdbb-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7cdbb-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7cdbb-141">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7cdbb-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7cdbb-142">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7cdbb-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7cdbb-143">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7cdbb-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="7cdbb-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7cdbb-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7cdbb-145">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7cdbb-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7cdbb-146">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7cdbb-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7cdbb-147">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7cdbb-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="7cdbb-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7cdbb-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="7cdbb-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7cdbb-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7cdbb-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7cdbb-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="7cdbb-151">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7cdbb-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
