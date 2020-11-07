---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 97227c27e23c6283fd64e1660262bbec175cf0a7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882930"
---
# <span data-ttu-id="f73f8-101">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f73f8-101">Get-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="f73f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f73f8-102">SYNOPSIS</span></span>
<span data-ttu-id="f73f8-103">네트워크 감시자의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f73f8-103">Gets the properties of a Network Watcher</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f73f8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f73f8-104">SYNTAX</span></span>

### <span data-ttu-id="f73f8-105">가져오기</span><span class="sxs-lookup"><span data-stu-id="f73f8-105">Get</span></span>
```
Get-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f73f8-106">목록</span><span class="sxs-lookup"><span data-stu-id="f73f8-106">List</span></span>
```
Get-AzureRmNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f73f8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f73f8-107">DESCRIPTION</span></span>
<span data-ttu-id="f73f8-108">Get-AzureRmNetworkWatcher cmdlet은 하나 이상의 Azure 네트워크 감시자 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f73f8-108">The Get-AzureRmNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="f73f8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f73f8-109">EXAMPLES</span></span>

### <span data-ttu-id="f73f8-110">--------------------------예제 1: 네트워크 감시자를 가져옵니다--------------------------</span><span class="sxs-lookup"><span data-stu-id="f73f8-110">--------------------------  Example 1: Get a Network Watcher  --------------------------</span></span>
```
Get-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="f73f8-111">리소스 그룹 NetworkWatcherRG의 NetworkWatcher_westcentralus 라는 네트워크 감시자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f73f8-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="f73f8-112">변수</span><span class="sxs-lookup"><span data-stu-id="f73f8-112">PARAMETERS</span></span>

### <span data-ttu-id="f73f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f73f8-113">-DefaultProfile</span></span>
<span data-ttu-id="f73f8-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f73f8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f73f8-115">-이름</span><span class="sxs-lookup"><span data-stu-id="f73f8-115">-Name</span></span>
<span data-ttu-id="f73f8-116">네트워크 감시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f73f8-116">The network watcher name.</span></span>

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

### <span data-ttu-id="f73f8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f73f8-117">-ResourceGroupName</span></span>
<span data-ttu-id="f73f8-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f73f8-118">The resource group name.</span></span>

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

### <span data-ttu-id="f73f8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f73f8-119">CommonParameters</span></span>
<span data-ttu-id="f73f8-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f73f8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f73f8-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f73f8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f73f8-122">입력</span><span class="sxs-lookup"><span data-stu-id="f73f8-122">INPUTS</span></span>

### <span data-ttu-id="f73f8-123">않아야</span><span class="sxs-lookup"><span data-stu-id="f73f8-123">None</span></span>

## <span data-ttu-id="f73f8-124">출력</span><span class="sxs-lookup"><span data-stu-id="f73f8-124">OUTPUTS</span></span>

### <span data-ttu-id="f73f8-125">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f73f8-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="f73f8-126">상속자</span><span class="sxs-lookup"><span data-stu-id="f73f8-126">NOTES</span></span>
<span data-ttu-id="f73f8-127">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자</span><span class="sxs-lookup"><span data-stu-id="f73f8-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="f73f8-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f73f8-128">RELATED LINKS</span></span>

[<span data-ttu-id="f73f8-129">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f73f8-129">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f73f8-130">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f73f8-130">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f73f8-131">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f73f8-131">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f73f8-132">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f73f8-132">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="f73f8-133">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f73f8-133">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f73f8-134">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f73f8-134">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f73f8-135">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f73f8-135">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f73f8-136">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f73f8-136">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="f73f8-137">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f73f8-137">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="f73f8-138">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f73f8-138">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f73f8-139">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f73f8-139">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="f73f8-140">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f73f8-140">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
