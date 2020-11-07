---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: fe315ac4b6c29b8ffd1c82c8045ba9b7a7aab4a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875542"
---
# <span data-ttu-id="f6e74-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f6e74-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="f6e74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6e74-102">SYNOPSIS</span></span>
<span data-ttu-id="f6e74-103">VM에 적용 되는 구성 된 유효 네트워크 보안 그룹 규칙을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="f6e74-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="f6e74-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f6e74-104">SYNTAX</span></span>

### <span data-ttu-id="f6e74-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="f6e74-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6e74-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f6e74-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6e74-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f6e74-107">DESCRIPTION</span></span>
<span data-ttu-id="f6e74-108">Get-AzNetworkWatcherSecurityGroupView를 사용 하 여 VM에 적용 되는 구성 된 유효 네트워크 보안 그룹 규칙을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6e74-108">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="f6e74-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f6e74-109">EXAMPLES</span></span>

### <span data-ttu-id="f6e74-110">---예제 1: VM---보안 그룹 보기 호출 하기</span><span class="sxs-lookup"><span data-stu-id="f6e74-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="f6e74-111">위 예제에서는 먼저 지역 네트워크 감시자를 얻은 다음 지역에서 VM을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f6e74-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="f6e74-112">그런 다음 지정 된 VM에서 보안 그룹 보기 호출을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6e74-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="f6e74-113">변수</span><span class="sxs-lookup"><span data-stu-id="f6e74-113">PARAMETERS</span></span>

### <span data-ttu-id="f6e74-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6e74-114">-AsJob</span></span>
<span data-ttu-id="f6e74-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f6e74-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f6e74-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6e74-116">-DefaultProfile</span></span>
<span data-ttu-id="f6e74-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f6e74-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6e74-118">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f6e74-118">-NetworkWatcher</span></span>
<span data-ttu-id="f6e74-119">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="f6e74-119">The network watcher resource.</span></span>

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

### <span data-ttu-id="f6e74-120">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f6e74-120">-NetworkWatcherName</span></span>
<span data-ttu-id="f6e74-121">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f6e74-121">The name of network watcher.</span></span>

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

### <span data-ttu-id="f6e74-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6e74-122">-ResourceGroupName</span></span>
<span data-ttu-id="f6e74-123">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f6e74-123">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f6e74-124">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="f6e74-124">-TargetVirtualMachineId</span></span>
<span data-ttu-id="f6e74-125">대상 VM Id</span><span class="sxs-lookup"><span data-stu-id="f6e74-125">The target VM Id</span></span>

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

### <span data-ttu-id="f6e74-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6e74-126">CommonParameters</span></span>
<span data-ttu-id="f6e74-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6e74-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6e74-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6e74-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6e74-129">입력</span><span class="sxs-lookup"><span data-stu-id="f6e74-129">INPUTS</span></span>

### <span data-ttu-id="f6e74-130">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f6e74-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f6e74-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f6e74-131">System.String</span></span>

## <span data-ttu-id="f6e74-132">출력</span><span class="sxs-lookup"><span data-stu-id="f6e74-132">OUTPUTS</span></span>

### <span data-ttu-id="f6e74-133">PSViewNsgRules에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f6e74-133">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="f6e74-134">상속자</span><span class="sxs-lookup"><span data-stu-id="f6e74-134">NOTES</span></span>
<span data-ttu-id="f6e74-135">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 흐름, ip</span><span class="sxs-lookup"><span data-stu-id="f6e74-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="f6e74-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6e74-136">RELATED LINKS</span></span>

[<span data-ttu-id="f6e74-137">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f6e74-137">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f6e74-138">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f6e74-138">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f6e74-139">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f6e74-139">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f6e74-140">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f6e74-140">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f6e74-141">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f6e74-141">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="f6e74-142">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f6e74-142">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f6e74-143">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f6e74-143">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f6e74-144">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f6e74-144">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f6e74-145">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f6e74-145">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f6e74-146">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f6e74-146">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f6e74-147">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f6e74-147">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f6e74-148">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f6e74-148">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

