---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 44bba48f1d066c4a9006595092bd84c68252bbd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532222"
---
# <span data-ttu-id="495ef-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="495ef-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="495ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="495ef-102">SYNOPSIS</span></span>
<span data-ttu-id="495ef-103">VM에 적용 되는 구성 된 유효 네트워크 보안 그룹 규칙을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="495ef-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="495ef-104">구문과</span><span class="sxs-lookup"><span data-stu-id="495ef-104">SYNTAX</span></span>

### <span data-ttu-id="495ef-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="495ef-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="495ef-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="495ef-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="495ef-107">설명은</span><span class="sxs-lookup"><span data-stu-id="495ef-107">DESCRIPTION</span></span>
<span data-ttu-id="495ef-108">Get-AzureRmNetworkWatcherSecurityGroupView를 사용 하 여 VM에 적용 되는 구성 된 유효 네트워크 보안 그룹 규칙을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="495ef-108">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="495ef-109">예제의</span><span class="sxs-lookup"><span data-stu-id="495ef-109">EXAMPLES</span></span>

### <span data-ttu-id="495ef-110">---예제 1: VM---보안 그룹 보기 호출 하기</span><span class="sxs-lookup"><span data-stu-id="495ef-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="495ef-111">위 예제에서는 먼저 지역 네트워크 감시자를 얻은 다음 지역에서 VM을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="495ef-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="495ef-112">그런 다음 지정 된 VM에서 보안 그룹 보기 호출을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="495ef-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="495ef-113">변수</span><span class="sxs-lookup"><span data-stu-id="495ef-113">PARAMETERS</span></span>

### <span data-ttu-id="495ef-114">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="495ef-114">-NetworkWatcher</span></span>
<span data-ttu-id="495ef-115">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="495ef-115">The network watcher resource.</span></span>

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

### <span data-ttu-id="495ef-116">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="495ef-116">-NetworkWatcherName</span></span>
<span data-ttu-id="495ef-117">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="495ef-117">The name of network watcher.</span></span>

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

### <span data-ttu-id="495ef-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="495ef-118">-ResourceGroupName</span></span>
<span data-ttu-id="495ef-119">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="495ef-119">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="495ef-120">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="495ef-120">-TargetVirtualMachineId</span></span>
<span data-ttu-id="495ef-121">대상 VM Id</span><span class="sxs-lookup"><span data-stu-id="495ef-121">The target VM Id</span></span>

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

### <span data-ttu-id="495ef-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="495ef-122">-DefaultProfile</span></span>
<span data-ttu-id="495ef-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="495ef-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="495ef-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="495ef-124">CommonParameters</span></span>
<span data-ttu-id="495ef-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="495ef-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="495ef-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="495ef-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="495ef-127">입력</span><span class="sxs-lookup"><span data-stu-id="495ef-127">INPUTS</span></span>

### <span data-ttu-id="495ef-128">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="495ef-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="495ef-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="495ef-129">System.String</span></span>

## <span data-ttu-id="495ef-130">출력</span><span class="sxs-lookup"><span data-stu-id="495ef-130">OUTPUTS</span></span>

### <span data-ttu-id="495ef-131">PSViewNsgRules에 대 한.</span><span class="sxs-lookup"><span data-stu-id="495ef-131">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="495ef-132">상속자</span><span class="sxs-lookup"><span data-stu-id="495ef-132">NOTES</span></span>
<span data-ttu-id="495ef-133">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 흐름, ip</span><span class="sxs-lookup"><span data-stu-id="495ef-133">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="495ef-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="495ef-134">RELATED LINKS</span></span>

[<span data-ttu-id="495ef-135">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="495ef-135">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="495ef-136">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="495ef-136">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="495ef-137">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="495ef-137">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="495ef-138">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="495ef-138">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="495ef-139">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="495ef-139">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="495ef-140">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="495ef-140">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="495ef-141">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="495ef-141">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="495ef-142">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="495ef-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="495ef-143">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="495ef-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="495ef-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="495ef-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="495ef-145">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="495ef-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="495ef-146">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="495ef-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

