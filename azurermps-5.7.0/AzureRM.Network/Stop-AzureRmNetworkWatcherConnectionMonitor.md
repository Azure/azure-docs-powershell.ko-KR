---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: e49245fabd4387c48def797168e1d572a43d6bfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528899"
---
# <span data-ttu-id="7f8f3-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7f8f3-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="7f8f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f8f3-102">SYNOPSIS</span></span>
<span data-ttu-id="7f8f3-103">연결 모니터 중지</span><span class="sxs-lookup"><span data-stu-id="7f8f3-103">Stop a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f8f3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7f8f3-104">SYNTAX</span></span>

### <span data-ttu-id="7f8f3-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="7f8f3-105">SetByName (Default)</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f8f3-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7f8f3-106">SetByResource</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f8f3-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="7f8f3-107">SetByLocation</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f8f3-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7f8f3-108">SetByResourceId</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f8f3-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="7f8f3-109">SetByInputObject</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f8f3-110">설명은</span><span class="sxs-lookup"><span data-stu-id="7f8f3-110">DESCRIPTION</span></span>
<span data-ttu-id="7f8f3-111">Stop-AzureRmNetworkWatcherConnectionMonitor cmdlet은 지정 된 연결 모니터를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-111">The Stop-AzureRmNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="7f8f3-112">예제의</span><span class="sxs-lookup"><span data-stu-id="7f8f3-112">EXAMPLES</span></span>

### <span data-ttu-id="7f8f3-113">예제 1: 연결 모니터 중지</span><span class="sxs-lookup"><span data-stu-id="7f8f3-113">Example 1: Stop a connection monitor</span></span>
```
PS C:\> Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="7f8f3-114">이 예제에서는 이름 및 네트워크 감시자에 의해 지정 된 연결 모니터를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="7f8f3-115">변수</span><span class="sxs-lookup"><span data-stu-id="7f8f3-115">PARAMETERS</span></span>

### <span data-ttu-id="7f8f3-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f8f3-116">-AsJob</span></span>
<span data-ttu-id="7f8f3-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7f8f3-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7f8f3-118">-확인</span><span class="sxs-lookup"><span data-stu-id="7f8f3-118">-Confirm</span></span>
<span data-ttu-id="7f8f3-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f8f3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f8f3-120">-DefaultProfile</span></span>
<span data-ttu-id="7f8f3-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f8f3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f8f3-122">-InputObject</span></span>
<span data-ttu-id="7f8f3-123">연결 모니터 개체</span><span class="sxs-lookup"><span data-stu-id="7f8f3-123">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f8f3-124">-위치</span><span class="sxs-lookup"><span data-stu-id="7f8f3-124">-Location</span></span>
<span data-ttu-id="7f8f3-125">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-125">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f8f3-126">-이름</span><span class="sxs-lookup"><span data-stu-id="7f8f3-126">-Name</span></span>
<span data-ttu-id="7f8f3-127">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-127">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f8f3-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7f8f3-128">-NetworkWatcher</span></span>
<span data-ttu-id="7f8f3-129">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="7f8f3-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7f8f3-130">-NetworkWatcherName</span></span>
<span data-ttu-id="7f8f3-131">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-131">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f8f3-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f8f3-132">-PassThru</span></span>
<span data-ttu-id="7f8f3-133">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="7f8f3-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7f8f3-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f8f3-134">-ResourceGroupName</span></span>
<span data-ttu-id="7f8f3-135">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-135">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f8f3-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f8f3-136">-ResourceId</span></span>
<span data-ttu-id="7f8f3-137">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-137">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f8f3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f8f3-138">-WhatIf</span></span>
<span data-ttu-id="7f8f3-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f8f3-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f8f3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f8f3-141">CommonParameters</span></span>
<span data-ttu-id="7f8f3-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7f8f3-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f8f3-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f8f3-144">입력</span><span class="sxs-lookup"><span data-stu-id="7f8f3-144">INPUTS</span></span>

### <span data-ttu-id="7f8f3-145">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7f8f3-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="7f8f3-146">Microsoft. Azure. PSConnectionMonitorResult.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-146">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="7f8f3-147">출력</span><span class="sxs-lookup"><span data-stu-id="7f8f3-147">OUTPUTS</span></span>

### <span data-ttu-id="7f8f3-148">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="7f8f3-148">System.Boolean</span></span>

## <span data-ttu-id="7f8f3-149">상속자</span><span class="sxs-lookup"><span data-stu-id="7f8f3-149">NOTES</span></span>
<span data-ttu-id="7f8f3-150">키워드: azure, azurerm, arm, 리소스, 연결, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결 모니터</span><span class="sxs-lookup"><span data-stu-id="7f8f3-150">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="7f8f3-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f8f3-151">RELATED LINKS</span></span>

[<span data-ttu-id="7f8f3-152">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7f8f3-152">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="7f8f3-153">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7f8f3-153">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="7f8f3-154">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7f8f3-154">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="7f8f3-155">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7f8f3-155">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="7f8f3-156">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7f8f3-156">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="7f8f3-157">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7f8f3-157">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="7f8f3-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7f8f3-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="7f8f3-159">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7f8f3-159">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="7f8f3-160">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7f8f3-160">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="7f8f3-161">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7f8f3-161">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="7f8f3-162">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7f8f3-162">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="7f8f3-163">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7f8f3-163">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="7f8f3-164">새로운 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7f8f3-164">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="7f8f3-165">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7f8f3-165">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="7f8f3-166">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="7f8f3-166">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="7f8f3-167">제거-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7f8f3-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="7f8f3-168">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7f8f3-168">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="7f8f3-169">시작-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7f8f3-169">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
