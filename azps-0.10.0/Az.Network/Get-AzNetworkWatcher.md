---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: d312eaa9f75fc13ecba0b00aa0fea64b5d3ea2e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875559"
---
# <span data-ttu-id="76d09-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="76d09-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="76d09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76d09-102">SYNOPSIS</span></span>
<span data-ttu-id="76d09-103">네트워크 감시자의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76d09-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="76d09-104">구문과</span><span class="sxs-lookup"><span data-stu-id="76d09-104">SYNTAX</span></span>

### <span data-ttu-id="76d09-105">가져오기</span><span class="sxs-lookup"><span data-stu-id="76d09-105">Get</span></span>
```
Get-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="76d09-106">목록</span><span class="sxs-lookup"><span data-stu-id="76d09-106">List</span></span>
```
Get-AzNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76d09-107">설명은</span><span class="sxs-lookup"><span data-stu-id="76d09-107">DESCRIPTION</span></span>
<span data-ttu-id="76d09-108">Get-AzNetworkWatcher cmdlet은 하나 이상의 Azure 네트워크 감시자 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76d09-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="76d09-109">예제의</span><span class="sxs-lookup"><span data-stu-id="76d09-109">EXAMPLES</span></span>

### <span data-ttu-id="76d09-110">--------------------------예제 1: 네트워크 감시자를 가져옵니다--------------------------</span><span class="sxs-lookup"><span data-stu-id="76d09-110">--------------------------  Example 1: Get a Network Watcher  --------------------------</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="76d09-111">리소스 그룹 NetworkWatcherRG의 NetworkWatcher_westcentralus 라는 네트워크 감시자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76d09-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="76d09-112">변수</span><span class="sxs-lookup"><span data-stu-id="76d09-112">PARAMETERS</span></span>

### <span data-ttu-id="76d09-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76d09-113">-DefaultProfile</span></span>
<span data-ttu-id="76d09-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="76d09-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76d09-115">-이름</span><span class="sxs-lookup"><span data-stu-id="76d09-115">-Name</span></span>
<span data-ttu-id="76d09-116">네트워크 감시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="76d09-116">The network watcher name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76d09-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76d09-117">-ResourceGroupName</span></span>
<span data-ttu-id="76d09-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="76d09-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76d09-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76d09-119">CommonParameters</span></span>
<span data-ttu-id="76d09-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="76d09-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76d09-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76d09-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76d09-122">입력</span><span class="sxs-lookup"><span data-stu-id="76d09-122">INPUTS</span></span>

### <span data-ttu-id="76d09-123">않아야</span><span class="sxs-lookup"><span data-stu-id="76d09-123">None</span></span>

## <span data-ttu-id="76d09-124">출력</span><span class="sxs-lookup"><span data-stu-id="76d09-124">OUTPUTS</span></span>

### <span data-ttu-id="76d09-125">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="76d09-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="76d09-126">상속자</span><span class="sxs-lookup"><span data-stu-id="76d09-126">NOTES</span></span>
<span data-ttu-id="76d09-127">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자</span><span class="sxs-lookup"><span data-stu-id="76d09-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="76d09-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76d09-128">RELATED LINKS</span></span>

[<span data-ttu-id="76d09-129">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="76d09-129">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="76d09-130">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="76d09-130">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="76d09-131">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="76d09-131">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="76d09-132">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="76d09-132">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="76d09-133">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="76d09-133">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="76d09-134">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="76d09-134">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="76d09-135">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="76d09-135">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="76d09-136">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="76d09-136">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="76d09-137">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="76d09-137">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="76d09-138">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="76d09-138">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="76d09-139">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="76d09-139">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="76d09-140">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="76d09-140">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
