---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 2f2ca6c4b9174248074cb3863c7be7de45c170c6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876664"
---
# <span data-ttu-id="4bbaa-101">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4bbaa-101">Remove-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="4bbaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bbaa-102">SYNOPSIS</span></span>
<span data-ttu-id="4bbaa-103">연결 모니터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbaa-103">Remove connection monitor.</span></span>

## <span data-ttu-id="4bbaa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4bbaa-104">SYNTAX</span></span>

### <span data-ttu-id="4bbaa-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="4bbaa-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4bbaa-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4bbaa-106">SetByName</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4bbaa-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4bbaa-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4bbaa-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4bbaa-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4bbaa-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="4bbaa-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="4bbaa-110">설명은</span><span class="sxs-lookup"><span data-stu-id="4bbaa-110">DESCRIPTION</span></span>
<span data-ttu-id="4bbaa-111">AzNetworkWatcherConnectionMonitor cmdlet은 지정 된 연결 모니터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbaa-111">The remove-AzNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="4bbaa-112">예제의</span><span class="sxs-lookup"><span data-stu-id="4bbaa-112">EXAMPLES</span></span>

### <span data-ttu-id="4bbaa-113">---------------예제 1: 지정 된 연결 모니터 제거---------------</span><span class="sxs-lookup"><span data-stu-id="4bbaa-113">---------------  Example 1: Remove the specified connection monitor ---------------</span></span>
```
PS C:\> Remove-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="4bbaa-114">이 예제에서는 위치 및 이름으로 지정 된 연결 모니터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbaa-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="4bbaa-115">변수</span><span class="sxs-lookup"><span data-stu-id="4bbaa-115">PARAMETERS</span></span>

### <span data-ttu-id="4bbaa-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bbaa-116">-AsJob</span></span>
<span data-ttu-id="4bbaa-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4bbaa-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4bbaa-118">-확인</span><span class="sxs-lookup"><span data-stu-id="4bbaa-118">-Confirm</span></span>
<span data-ttu-id="4bbaa-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbaa-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbaa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bbaa-120">-DefaultProfile</span></span>
<span data-ttu-id="4bbaa-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4bbaa-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bbaa-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bbaa-122">-InputObject</span></span>
<span data-ttu-id="4bbaa-123">연결 모니터 개체</span><span class="sxs-lookup"><span data-stu-id="4bbaa-123">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bbaa-124">-위치</span><span class="sxs-lookup"><span data-stu-id="4bbaa-124">-Location</span></span>
<span data-ttu-id="4bbaa-125">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4bbaa-125">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bbaa-126">-이름</span><span class="sxs-lookup"><span data-stu-id="4bbaa-126">-Name</span></span>
<span data-ttu-id="4bbaa-127">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bbaa-127">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bbaa-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4bbaa-128">-NetworkWatcher</span></span>
<span data-ttu-id="4bbaa-129">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="4bbaa-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="4bbaa-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4bbaa-130">-NetworkWatcherName</span></span>
<span data-ttu-id="4bbaa-131">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bbaa-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="4bbaa-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4bbaa-132">-PassThru</span></span>
<span data-ttu-id="4bbaa-133">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="4bbaa-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4bbaa-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bbaa-134">-ResourceGroupName</span></span>
<span data-ttu-id="4bbaa-135">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bbaa-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4bbaa-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bbaa-136">-ResourceId</span></span>
<span data-ttu-id="4bbaa-137">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4bbaa-137">Resource ID.</span></span>

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

### <span data-ttu-id="4bbaa-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bbaa-138">-WhatIf</span></span>
<span data-ttu-id="4bbaa-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4bbaa-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bbaa-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4bbaa-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="4bbaa-141">입력</span><span class="sxs-lookup"><span data-stu-id="4bbaa-141">INPUTS</span></span>

### <span data-ttu-id="4bbaa-142">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4bbaa-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="4bbaa-143">Microsoft. Azure. PSConnectionMonitorResult.</span><span class="sxs-lookup"><span data-stu-id="4bbaa-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="4bbaa-144">출력</span><span class="sxs-lookup"><span data-stu-id="4bbaa-144">OUTPUTS</span></span>

### <span data-ttu-id="4bbaa-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="4bbaa-145">System.Boolean</span></span>


## <span data-ttu-id="4bbaa-146">상속자</span><span class="sxs-lookup"><span data-stu-id="4bbaa-146">NOTES</span></span>
<span data-ttu-id="4bbaa-147">키워드: azure, azurerm, arm, 리소스, 연결, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결 모니터</span><span class="sxs-lookup"><span data-stu-id="4bbaa-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="4bbaa-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4bbaa-148">RELATED LINKS</span></span>
<span data-ttu-id="4bbaa-149">[새로운 AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [제거-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="4bbaa-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="4bbaa-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="4bbaa-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="4bbaa-151">[새로운 AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [새로운 AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [제거-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [중지-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="4bbaa-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="4bbaa-152">[새로운 AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="4bbaa-152">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)</span></span>

