---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: a67dde4b1e8f3f97038304086b63d02d75ff8fec
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880921"
---
# <span data-ttu-id="70892-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="70892-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="70892-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70892-102">SYNOPSIS</span></span>
<span data-ttu-id="70892-103">연결 모니터 중지</span><span class="sxs-lookup"><span data-stu-id="70892-103">Stop a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70892-104">구문과</span><span class="sxs-lookup"><span data-stu-id="70892-104">SYNTAX</span></span>

### <span data-ttu-id="70892-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="70892-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="70892-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="70892-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="70892-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="70892-107">SetByLocation</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="70892-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="70892-108">SetByResourceId</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="70892-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="70892-109">SetByInputObject</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="70892-110">설명은</span><span class="sxs-lookup"><span data-stu-id="70892-110">DESCRIPTION</span></span>
<span data-ttu-id="70892-111">Stop-AzureRmNetworkWatcherConnectionMonitor cmdlet은 지정 된 연결 모니터를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="70892-111">The Stop-AzureRmNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="70892-112">예제의</span><span class="sxs-lookup"><span data-stu-id="70892-112">EXAMPLES</span></span>

### <span data-ttu-id="70892-113">---------------예제 1: 연결 모니터 중지---------------</span><span class="sxs-lookup"><span data-stu-id="70892-113">---------------  Example 1: Stop a connection monitor ---------------</span></span>
```
PS C:\> Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="70892-114">이 예제에서는 이름 및 네트워크 감시자에 의해 지정 된 연결 모니터를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="70892-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="70892-115">변수</span><span class="sxs-lookup"><span data-stu-id="70892-115">PARAMETERS</span></span>

### <span data-ttu-id="70892-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70892-116">-AsJob</span></span>
<span data-ttu-id="70892-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="70892-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70892-118">-확인</span><span class="sxs-lookup"><span data-stu-id="70892-118">-Confirm</span></span>
<span data-ttu-id="70892-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="70892-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70892-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70892-120">-DefaultProfile</span></span>
<span data-ttu-id="70892-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="70892-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70892-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70892-122">-InputObject</span></span>
<span data-ttu-id="70892-123">연결 모니터 개체</span><span class="sxs-lookup"><span data-stu-id="70892-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="70892-124">-위치</span><span class="sxs-lookup"><span data-stu-id="70892-124">-Location</span></span>
<span data-ttu-id="70892-125">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="70892-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="70892-126">-이름</span><span class="sxs-lookup"><span data-stu-id="70892-126">-Name</span></span>
<span data-ttu-id="70892-127">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70892-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="70892-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="70892-128">-NetworkWatcher</span></span>
<span data-ttu-id="70892-129">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="70892-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="70892-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="70892-130">-NetworkWatcherName</span></span>
<span data-ttu-id="70892-131">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70892-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="70892-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70892-132">-PassThru</span></span>
<span data-ttu-id="70892-133">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="70892-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="70892-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70892-134">-ResourceGroupName</span></span>
<span data-ttu-id="70892-135">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70892-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="70892-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70892-136">-ResourceId</span></span>
<span data-ttu-id="70892-137">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="70892-137">Resource ID.</span></span>

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

### <span data-ttu-id="70892-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70892-138">-WhatIf</span></span>
<span data-ttu-id="70892-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="70892-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70892-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70892-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="70892-141">입력</span><span class="sxs-lookup"><span data-stu-id="70892-141">INPUTS</span></span>

### <span data-ttu-id="70892-142">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="70892-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="70892-143">Microsoft. Azure. PSConnectionMonitorResult.</span><span class="sxs-lookup"><span data-stu-id="70892-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="70892-144">출력</span><span class="sxs-lookup"><span data-stu-id="70892-144">OUTPUTS</span></span>

### <span data-ttu-id="70892-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="70892-145">System.Boolean</span></span>


## <span data-ttu-id="70892-146">상속자</span><span class="sxs-lookup"><span data-stu-id="70892-146">NOTES</span></span>
<span data-ttu-id="70892-147">키워드: azure, azurerm, arm, 리소스, 연결, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결 모니터</span><span class="sxs-lookup"><span data-stu-id="70892-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="70892-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70892-148">RELATED LINKS</span></span>
<span data-ttu-id="70892-149">[새로운 AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [제거-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="70892-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="70892-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="70892-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="70892-151">[새로운 AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [새로운 AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [제거-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [중지-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="70892-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="70892-152">[새로운 AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [제거-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md) 
 [시작-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="70892-152">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)
[Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md)
[Start-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>
