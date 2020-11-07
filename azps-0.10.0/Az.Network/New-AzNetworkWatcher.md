---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: cace33dd9831dcfcc01f2a57eefb5f28367966d9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875411"
---
# <span data-ttu-id="c229a-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c229a-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="c229a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c229a-102">SYNOPSIS</span></span>
<span data-ttu-id="c229a-103">새 네트워크 감시자 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c229a-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="c229a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c229a-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c229a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c229a-105">DESCRIPTION</span></span>
<span data-ttu-id="c229a-106">New-AzNetworkWatcher cmdlet은 새 네트워크 감시자 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c229a-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="c229a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c229a-107">EXAMPLES</span></span>

### <span data-ttu-id="c229a-108">예제 1: 네트워크 감시자 만들기</span><span class="sxs-lookup"><span data-stu-id="c229a-108">Example 1: Create a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="c229a-109">이 예제에서는 새로 만든 리소스 그룹 내에 새 네트워크 감시자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c229a-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="c229a-110">구독 당 지역 당 하나의 네트워크 감시자만 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c229a-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="c229a-111">변수</span><span class="sxs-lookup"><span data-stu-id="c229a-111">PARAMETERS</span></span>

### <span data-ttu-id="c229a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c229a-112">-DefaultProfile</span></span>
<span data-ttu-id="c229a-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c229a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c229a-114">-위치</span><span class="sxs-lookup"><span data-stu-id="c229a-114">-Location</span></span>
<span data-ttu-id="c229a-115">Location.</span><span class="sxs-lookup"><span data-stu-id="c229a-115">Location.</span></span>

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

### <span data-ttu-id="c229a-116">-이름</span><span class="sxs-lookup"><span data-stu-id="c229a-116">-Name</span></span>
<span data-ttu-id="c229a-117">네트워크 감시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c229a-117">The network watcher name.</span></span>

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

### <span data-ttu-id="c229a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c229a-118">-ResourceGroupName</span></span>
<span data-ttu-id="c229a-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c229a-119">The resource group name.</span></span>

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

### <span data-ttu-id="c229a-120">태그</span><span class="sxs-lookup"><span data-stu-id="c229a-120">-Tag</span></span>
<span data-ttu-id="c229a-121">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="c229a-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c229a-122">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="c229a-122">For example:</span></span>

<span data-ttu-id="c229a-123">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c229a-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c229a-124">-확인</span><span class="sxs-lookup"><span data-stu-id="c229a-124">-Confirm</span></span>
<span data-ttu-id="c229a-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c229a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c229a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c229a-126">-WhatIf</span></span>
<span data-ttu-id="c229a-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c229a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c229a-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c229a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c229a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c229a-129">CommonParameters</span></span>
<span data-ttu-id="c229a-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c229a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c229a-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c229a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c229a-132">입력</span><span class="sxs-lookup"><span data-stu-id="c229a-132">INPUTS</span></span>

### <span data-ttu-id="c229a-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c229a-133">System.String</span></span>
<span data-ttu-id="c229a-134">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="c229a-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c229a-135">출력</span><span class="sxs-lookup"><span data-stu-id="c229a-135">OUTPUTS</span></span>

### <span data-ttu-id="c229a-136">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c229a-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="c229a-137">상속자</span><span class="sxs-lookup"><span data-stu-id="c229a-137">NOTES</span></span>
<span data-ttu-id="c229a-138">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자</span><span class="sxs-lookup"><span data-stu-id="c229a-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="c229a-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c229a-139">RELATED LINKS</span></span>

[<span data-ttu-id="c229a-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c229a-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c229a-141">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c229a-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c229a-142">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c229a-142">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c229a-143">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c229a-143">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c229a-144">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c229a-144">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c229a-145">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c229a-145">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c229a-146">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c229a-146">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c229a-147">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c229a-147">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c229a-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c229a-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c229a-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c229a-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c229a-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c229a-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c229a-151">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c229a-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
