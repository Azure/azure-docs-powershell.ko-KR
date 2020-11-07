---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchersecuritygroupview
schema: 2.0.0
ms.openlocfilehash: fad852ff589b2929df83775a2fa955e72663cfa2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880682"
---
# <span data-ttu-id="efeb4-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="efeb4-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="efeb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efeb4-102">SYNOPSIS</span></span>
<span data-ttu-id="efeb4-103">VM에 적용 되는 구성 된 유효 네트워크 보안 그룹 규칙을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="efeb4-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efeb4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="efeb4-104">SYNTAX</span></span>

### <span data-ttu-id="efeb4-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="efeb4-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efeb4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="efeb4-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efeb4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="efeb4-107">DESCRIPTION</span></span>
<span data-ttu-id="efeb4-108">Get-AzureRmNetworkWatcherSecurityGroupView를 사용 하 여 VM에 적용 되는 구성 된 유효 네트워크 보안 그룹 규칙을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efeb4-108">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="efeb4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="efeb4-109">EXAMPLES</span></span>

### <span data-ttu-id="efeb4-110">---예제 1: VM---보안 그룹 보기 호출 하기</span><span class="sxs-lookup"><span data-stu-id="efeb4-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="efeb4-111">위 예제에서는 먼저 지역 네트워크 감시자를 얻은 다음 지역에서 VM을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="efeb4-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="efeb4-112">그런 다음 지정 된 VM에서 보안 그룹 보기 호출을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="efeb4-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="efeb4-113">변수</span><span class="sxs-lookup"><span data-stu-id="efeb4-113">PARAMETERS</span></span>

### <span data-ttu-id="efeb4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="efeb4-114">-AsJob</span></span>
<span data-ttu-id="efeb4-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="efeb4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="efeb4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efeb4-116">-DefaultProfile</span></span>
<span data-ttu-id="efeb4-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="efeb4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efeb4-118">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="efeb4-118">-NetworkWatcher</span></span>
<span data-ttu-id="efeb4-119">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="efeb4-119">The network watcher resource.</span></span>

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

### <span data-ttu-id="efeb4-120">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="efeb4-120">-NetworkWatcherName</span></span>
<span data-ttu-id="efeb4-121">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efeb4-121">The name of network watcher.</span></span>

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

### <span data-ttu-id="efeb4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efeb4-122">-ResourceGroupName</span></span>
<span data-ttu-id="efeb4-123">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efeb4-123">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="efeb4-124">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="efeb4-124">-TargetVirtualMachineId</span></span>
<span data-ttu-id="efeb4-125">대상 VM Id</span><span class="sxs-lookup"><span data-stu-id="efeb4-125">The target VM Id</span></span>

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

### <span data-ttu-id="efeb4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efeb4-126">CommonParameters</span></span>
<span data-ttu-id="efeb4-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="efeb4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efeb4-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efeb4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efeb4-129">입력</span><span class="sxs-lookup"><span data-stu-id="efeb4-129">INPUTS</span></span>

### <span data-ttu-id="efeb4-130">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="efeb4-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="efeb4-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="efeb4-131">System.String</span></span>

## <span data-ttu-id="efeb4-132">출력</span><span class="sxs-lookup"><span data-stu-id="efeb4-132">OUTPUTS</span></span>

### <span data-ttu-id="efeb4-133">PSViewNsgRules에 대 한.</span><span class="sxs-lookup"><span data-stu-id="efeb4-133">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="efeb4-134">상속자</span><span class="sxs-lookup"><span data-stu-id="efeb4-134">NOTES</span></span>
<span data-ttu-id="efeb4-135">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 흐름, ip</span><span class="sxs-lookup"><span data-stu-id="efeb4-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="efeb4-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="efeb4-136">RELATED LINKS</span></span>

[<span data-ttu-id="efeb4-137">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="efeb4-137">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="efeb4-138">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="efeb4-138">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="efeb4-139">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="efeb4-139">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="efeb4-140">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="efeb4-140">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="efeb4-141">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="efeb4-141">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="efeb4-142">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="efeb4-142">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="efeb4-143">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="efeb4-143">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="efeb4-144">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="efeb4-144">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="efeb4-145">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="efeb4-145">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="efeb4-146">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="efeb4-146">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="efeb4-147">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="efeb4-147">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="efeb4-148">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="efeb4-148">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

