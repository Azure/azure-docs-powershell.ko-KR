---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
ms.openlocfilehash: 4fd6da3388b4058a3aa4bee2fe918fb063c8fd6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531004"
---
# <span data-ttu-id="d29bb-101">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d29bb-101">Remove-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="d29bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d29bb-102">SYNOPSIS</span></span>
<span data-ttu-id="d29bb-103">네트워크 감시자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d29bb-103">Removes a Network Watcher.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d29bb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d29bb-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d29bb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d29bb-105">DESCRIPTION</span></span>
<span data-ttu-id="d29bb-106">Remove-AzureRmNetworkWatcher cmdlet은 네트워크 감시자 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d29bb-106">The Remove-AzureRmNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="d29bb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d29bb-107">EXAMPLES</span></span>

### <span data-ttu-id="d29bb-108">--------------------------예제 1: 네트워크 감시자--------------------------만들기 및 삭제</span><span class="sxs-lookup"><span data-stu-id="d29bb-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="d29bb-109">이 예제에서는 리소스 그룹에 네트워크 감시자를 만든 다음 즉시 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d29bb-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="d29bb-110">구독 당 지역 당 하나의 네트워크 감시자만 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d29bb-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="d29bb-111">가상 네트워크를 삭제할 때 메시지가 표시 되지 않도록 하려면-Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d29bb-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="d29bb-112">변수</span><span class="sxs-lookup"><span data-stu-id="d29bb-112">PARAMETERS</span></span>

### <span data-ttu-id="d29bb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d29bb-113">-AsJob</span></span>
<span data-ttu-id="d29bb-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d29bb-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d29bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d29bb-115">-DefaultProfile</span></span>
<span data-ttu-id="d29bb-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d29bb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d29bb-117">-이름</span><span class="sxs-lookup"><span data-stu-id="d29bb-117">-Name</span></span>
<span data-ttu-id="d29bb-118">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d29bb-118">The resource name.</span></span>

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

### <span data-ttu-id="d29bb-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d29bb-119">-PassThru</span></span>
<span data-ttu-id="d29bb-120">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="d29bb-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d29bb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d29bb-121">-ResourceGroupName</span></span>
<span data-ttu-id="d29bb-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d29bb-122">The resource group name.</span></span>

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

### <span data-ttu-id="d29bb-123">-확인</span><span class="sxs-lookup"><span data-stu-id="d29bb-123">-Confirm</span></span>
<span data-ttu-id="d29bb-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d29bb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d29bb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d29bb-125">-WhatIf</span></span>
<span data-ttu-id="d29bb-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d29bb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d29bb-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d29bb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d29bb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d29bb-128">CommonParameters</span></span>
<span data-ttu-id="d29bb-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d29bb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d29bb-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d29bb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d29bb-131">입력</span><span class="sxs-lookup"><span data-stu-id="d29bb-131">INPUTS</span></span>

### <span data-ttu-id="d29bb-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d29bb-132">System.String</span></span>

## <span data-ttu-id="d29bb-133">출력</span><span class="sxs-lookup"><span data-stu-id="d29bb-133">OUTPUTS</span></span>

### <span data-ttu-id="d29bb-134">System. 개체</span><span class="sxs-lookup"><span data-stu-id="d29bb-134">System.Object</span></span>

## <span data-ttu-id="d29bb-135">상속자</span><span class="sxs-lookup"><span data-stu-id="d29bb-135">NOTES</span></span>
<span data-ttu-id="d29bb-136">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자</span><span class="sxs-lookup"><span data-stu-id="d29bb-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="d29bb-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d29bb-137">RELATED LINKS</span></span>

[<span data-ttu-id="d29bb-138">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d29bb-138">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d29bb-139">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d29bb-139">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d29bb-140">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d29bb-140">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d29bb-141">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d29bb-141">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="d29bb-142">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d29bb-142">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d29bb-143">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d29bb-143">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d29bb-144">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d29bb-144">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d29bb-145">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d29bb-145">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="d29bb-146">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d29bb-146">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="d29bb-147">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d29bb-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d29bb-148">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d29bb-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="d29bb-149">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d29bb-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
