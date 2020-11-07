---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: 276cd57a51b6b457f2f4d205932cdbfabd7613b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876662"
---
# <span data-ttu-id="7502f-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7502f-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="7502f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7502f-102">SYNOPSIS</span></span>
<span data-ttu-id="7502f-103">네트워크 감시자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7502f-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="7502f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7502f-104">SYNTAX</span></span>

```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7502f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7502f-105">DESCRIPTION</span></span>
<span data-ttu-id="7502f-106">Remove-AzNetworkWatcher cmdlet은 네트워크 감시자 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7502f-106">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="7502f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7502f-107">EXAMPLES</span></span>

### <span data-ttu-id="7502f-108">--------------------------예제 1: 네트워크 감시자--------------------------만들기 및 삭제</span><span class="sxs-lookup"><span data-stu-id="7502f-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="7502f-109">이 예제에서는 리소스 그룹에 네트워크 감시자를 만든 다음 즉시 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7502f-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="7502f-110">구독 당 지역 당 하나의 네트워크 감시자만 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7502f-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="7502f-111">가상 네트워크를 삭제할 때 메시지가 표시 되지 않도록 하려면-Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7502f-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="7502f-112">변수</span><span class="sxs-lookup"><span data-stu-id="7502f-112">PARAMETERS</span></span>

### <span data-ttu-id="7502f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7502f-113">-AsJob</span></span>
<span data-ttu-id="7502f-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7502f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7502f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7502f-115">-DefaultProfile</span></span>
<span data-ttu-id="7502f-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7502f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7502f-117">-이름</span><span class="sxs-lookup"><span data-stu-id="7502f-117">-Name</span></span>
<span data-ttu-id="7502f-118">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7502f-118">The resource name.</span></span>

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

### <span data-ttu-id="7502f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7502f-119">-PassThru</span></span>
<span data-ttu-id="7502f-120">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="7502f-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7502f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7502f-121">-ResourceGroupName</span></span>
<span data-ttu-id="7502f-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7502f-122">The resource group name.</span></span>

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

### <span data-ttu-id="7502f-123">-확인</span><span class="sxs-lookup"><span data-stu-id="7502f-123">-Confirm</span></span>
<span data-ttu-id="7502f-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7502f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7502f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7502f-125">-WhatIf</span></span>
<span data-ttu-id="7502f-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7502f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7502f-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7502f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7502f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7502f-128">CommonParameters</span></span>
<span data-ttu-id="7502f-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7502f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7502f-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7502f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7502f-131">입력</span><span class="sxs-lookup"><span data-stu-id="7502f-131">INPUTS</span></span>

### <span data-ttu-id="7502f-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7502f-132">System.String</span></span>

## <span data-ttu-id="7502f-133">출력</span><span class="sxs-lookup"><span data-stu-id="7502f-133">OUTPUTS</span></span>

### <span data-ttu-id="7502f-134">System. 개체</span><span class="sxs-lookup"><span data-stu-id="7502f-134">System.Object</span></span>

## <span data-ttu-id="7502f-135">상속자</span><span class="sxs-lookup"><span data-stu-id="7502f-135">NOTES</span></span>
<span data-ttu-id="7502f-136">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자</span><span class="sxs-lookup"><span data-stu-id="7502f-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="7502f-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7502f-137">RELATED LINKS</span></span>

[<span data-ttu-id="7502f-138">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7502f-138">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="7502f-139">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7502f-139">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="7502f-140">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7502f-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7502f-141">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7502f-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="7502f-142">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7502f-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7502f-143">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7502f-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7502f-144">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7502f-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7502f-145">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7502f-145">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="7502f-146">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7502f-146">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="7502f-147">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7502f-147">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7502f-148">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7502f-148">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="7502f-149">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7502f-149">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
