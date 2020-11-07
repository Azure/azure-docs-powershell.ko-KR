---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 10582a0e81fdb9c86902c7a2580ad31fe84f3bb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704180"
---
# <span data-ttu-id="d9bab-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d9bab-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="d9bab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9bab-102">SYNOPSIS</span></span>
<span data-ttu-id="d9bab-103">연결 모니터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9bab-103">Remove connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9bab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d9bab-104">SYNTAX</span></span>

### <span data-ttu-id="d9bab-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d9bab-105">SetByName (Default)</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9bab-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d9bab-106">SetByResource</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9bab-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d9bab-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9bab-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d9bab-108">SetByResourceId</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9bab-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="d9bab-109">SetByInputObject</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9bab-110">설명은</span><span class="sxs-lookup"><span data-stu-id="d9bab-110">DESCRIPTION</span></span>
<span data-ttu-id="d9bab-111">AzureRmNetworkWatcherConnectionMonitor cmdlet은 지정 된 연결 모니터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9bab-111">The remove-AzureRmNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="d9bab-112">예제의</span><span class="sxs-lookup"><span data-stu-id="d9bab-112">EXAMPLES</span></span>

### <span data-ttu-id="d9bab-113">예제 1: 지정 된 연결 모니터 제거</span><span class="sxs-lookup"><span data-stu-id="d9bab-113">Example 1: Remove the specified connection monitor</span></span>
```
PS C:\> Remove-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="d9bab-114">이 예제에서는 위치 및 이름으로 지정 된 연결 모니터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9bab-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="d9bab-115">변수</span><span class="sxs-lookup"><span data-stu-id="d9bab-115">PARAMETERS</span></span>

### <span data-ttu-id="d9bab-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9bab-116">-AsJob</span></span>
<span data-ttu-id="d9bab-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d9bab-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9bab-118">-확인</span><span class="sxs-lookup"><span data-stu-id="d9bab-118">-Confirm</span></span>
<span data-ttu-id="d9bab-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9bab-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9bab-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9bab-120">-DefaultProfile</span></span>
<span data-ttu-id="d9bab-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d9bab-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9bab-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9bab-122">-InputObject</span></span>
<span data-ttu-id="d9bab-123">연결 모니터 개체</span><span class="sxs-lookup"><span data-stu-id="d9bab-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="d9bab-124">-위치</span><span class="sxs-lookup"><span data-stu-id="d9bab-124">-Location</span></span>
<span data-ttu-id="d9bab-125">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d9bab-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d9bab-126">-이름</span><span class="sxs-lookup"><span data-stu-id="d9bab-126">-Name</span></span>
<span data-ttu-id="d9bab-127">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d9bab-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="d9bab-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d9bab-128">-NetworkWatcher</span></span>
<span data-ttu-id="d9bab-129">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="d9bab-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="d9bab-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d9bab-130">-NetworkWatcherName</span></span>
<span data-ttu-id="d9bab-131">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d9bab-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="d9bab-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9bab-132">-PassThru</span></span>
<span data-ttu-id="d9bab-133">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="d9bab-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d9bab-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9bab-134">-ResourceGroupName</span></span>
<span data-ttu-id="d9bab-135">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d9bab-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d9bab-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9bab-136">-ResourceId</span></span>
<span data-ttu-id="d9bab-137">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d9bab-137">Resource ID.</span></span>

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

### <span data-ttu-id="d9bab-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9bab-138">-WhatIf</span></span>
<span data-ttu-id="d9bab-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d9bab-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9bab-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9bab-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9bab-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9bab-141">CommonParameters</span></span>
<span data-ttu-id="d9bab-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9bab-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d9bab-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9bab-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9bab-144">입력</span><span class="sxs-lookup"><span data-stu-id="d9bab-144">INPUTS</span></span>

### <span data-ttu-id="d9bab-145">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d9bab-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="d9bab-146">Microsoft. Azure. PSConnectionMonitorResult.</span><span class="sxs-lookup"><span data-stu-id="d9bab-146">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="d9bab-147">출력</span><span class="sxs-lookup"><span data-stu-id="d9bab-147">OUTPUTS</span></span>

### <span data-ttu-id="d9bab-148">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d9bab-148">System.Boolean</span></span>

## <span data-ttu-id="d9bab-149">상속자</span><span class="sxs-lookup"><span data-stu-id="d9bab-149">NOTES</span></span>
<span data-ttu-id="d9bab-150">키워드: azure, azurerm, arm, 리소스, 연결, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결 모니터</span><span class="sxs-lookup"><span data-stu-id="d9bab-150">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="d9bab-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9bab-151">RELATED LINKS</span></span>

[<span data-ttu-id="d9bab-152">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d9bab-152">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="d9bab-153">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d9bab-153">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="d9bab-154">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d9bab-154">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="d9bab-155">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d9bab-155">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="d9bab-156">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d9bab-156">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="d9bab-157">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d9bab-157">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="d9bab-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d9bab-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="d9bab-159">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d9bab-159">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="d9bab-160">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d9bab-160">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="d9bab-161">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d9bab-161">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="d9bab-162">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d9bab-162">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="d9bab-163">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d9bab-163">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="d9bab-164">새로운 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d9bab-164">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="d9bab-165">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d9bab-165">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="d9bab-166">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d9bab-166">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

