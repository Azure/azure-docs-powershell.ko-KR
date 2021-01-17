---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeTrigger.md
ms.openlocfilehash: d13498df4c91c8d31b8bfe2e19e9f7fa23f99998
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350037"
---
# <span data-ttu-id="ecf2d-101">New-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="ecf2d-101">New-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="ecf2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecf2d-102">SYNOPSIS</span></span>
<span data-ttu-id="ecf2d-103">디바이스에서 트리거를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-103">Configures a trigger on the device.</span></span>

## <span data-ttu-id="ecf2d-104">구문</span><span class="sxs-lookup"><span data-stu-id="ecf2d-104">SYNTAX</span></span>

### <span data-ttu-id="ecf2d-105">FileEventTriggerParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ecf2d-105">FileEventTriggerParameterSet (Default)</span></span>
```
New-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -RoleName <String>
 [-FileEvent] -ShareName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ecf2d-106">PeriodicTimerTriggerParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecf2d-106">PeriodicTimerTriggerParameterSet</span></span>
```
New-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -RoleName <String>
 [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>] -Schedule <String>
 -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecf2d-107">FileEventTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecf2d-107">FileEventTriggerResourceIdParameterSet</span></span>
```
New-AzStackEdgeTrigger [-FileEvent] -ShareId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecf2d-108">PeriodicTimerTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecf2d-108">PeriodicTimerTriggerResourceIdParameterSet</span></span>
```
New-AzStackEdgeTrigger [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecf2d-109">설명</span><span class="sxs-lookup"><span data-stu-id="ecf2d-109">DESCRIPTION</span></span>
<span data-ttu-id="ecf2d-110">**New-AzStackEdgeTrigger** cmdlet은 Stack Edge 디바이스에서 트리거를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-110">The **New-AzStackEdgeTrigger** cmdlet configures a trigger on the Stack Edge device.</span></span> 

## <span data-ttu-id="ecf2d-111">예제</span><span class="sxs-lookup"><span data-stu-id="ecf2d-111">EXAMPLES</span></span>

### <span data-ttu-id="ecf2d-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="ecf2d-112">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -PeriodicTimerEvent -Name periodic-trigger -RoleName IOTRole -Schedule "00:00" -StartTime "2019-10-28 12:00:00" -Topic sample-topic
Name                  Kind               
----                  ----               
periodic-trigger      PeriodicTimerEvent
```

## <span data-ttu-id="ecf2d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecf2d-113">PARAMETERS</span></span>

### <span data-ttu-id="ecf2d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ecf2d-114">-AsJob</span></span>
<span data-ttu-id="ecf2d-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ecf2d-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecf2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecf2d-116">-DefaultProfile</span></span>
<span data-ttu-id="ecf2d-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecf2d-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ecf2d-118">-DeviceName</span></span>
<span data-ttu-id="ecf2d-119">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="ecf2d-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf2d-120">-FileEvent</span><span class="sxs-lookup"><span data-stu-id="ecf2d-120">-FileEvent</span></span>
<span data-ttu-id="ecf2d-121">이 스위치 매개 변수를 전달하여 FileEvent 트리거 구성</span><span class="sxs-lookup"><span data-stu-id="ecf2d-121">Pass this switch parameter to configure FileEvent Trigger</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FileEventTriggerParameterSet, FileEventTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecf2d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ecf2d-122">-Name</span></span>
<span data-ttu-id="ecf2d-123">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="ecf2d-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf2d-124">-PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="ecf2d-124">-PeriodicTimerEvent</span></span>
<span data-ttu-id="ecf2d-125">이 스위치 매개 변수를 전달하여 PeriodicTimerEvent 트리거를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-125">Pass this switch parameter to configure PeriodicTimerEvent Trigger</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecf2d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecf2d-126">-ResourceGroupName</span></span>
<span data-ttu-id="ecf2d-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ecf2d-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf2d-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="ecf2d-128">-RoleName</span></span>
<span data-ttu-id="ecf2d-129">이벤트가 발생될 계산 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-129">Compute role against which events will be raised.</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecf2d-130">-Schedule</span><span class="sxs-lookup"><span data-stu-id="ecf2d-130">-Schedule</span></span>
<span data-ttu-id="ecf2d-131">Timer 이벤트를 발생해야 하는 주기적 빈도입니다.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-131">Periodic frequency at which timer event needs to be raised.</span></span> <span data-ttu-id="ecf2d-132">일(1~365 사이), 시간(1~23 사이) 또는 분(1~59 사이)으로 일정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-132">Specify a schedule in either days (between 1 and 365) , hours (between 1 and 23), or minutes (between 1 and 59).</span></span>

```yaml
Type: System.String
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecf2d-133">-ShareId</span><span class="sxs-lookup"><span data-stu-id="ecf2d-133">-ShareId</span></span>
<span data-ttu-id="ecf2d-134">FileEvent 트리거에 전달할 파일 공유 ID</span><span class="sxs-lookup"><span data-stu-id="ecf2d-134">File share ID to be passed in FileEvent Trigger</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecf2d-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="ecf2d-135">-ShareName</span></span>
<span data-ttu-id="ecf2d-136">FileEvent 트리거에 전달할 파일 공유 ID</span><span class="sxs-lookup"><span data-stu-id="ecf2d-136">File share ID to be passed in FileEvent Trigger</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecf2d-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ecf2d-137">-StartTime</span></span>
<span data-ttu-id="ecf2d-138">유효한 트리거를 유발하는 하루의 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-138">The time of the day that results in a valid trigger.</span></span> <span data-ttu-id="ecf2d-139">일정은 최대 초까지 지정된 시간을 참조하여 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-139">Schedule is computed with reference to the time specified up to seconds.</span></span> <span data-ttu-id="ecf2d-140">timezone이 지정되지 않은 경우 시간은 디바이스 시간제에 있는 것으로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-140">If timezone is not specified the time will considered to be in device timezone.</span></span> <span data-ttu-id="ecf2d-141">값은 항상 UTC 시간으로 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-141">The value will always be returned as UTC time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecf2d-142">-Topic</span><span class="sxs-lookup"><span data-stu-id="ecf2d-142">-Topic</span></span>
<span data-ttu-id="ecf2d-143">IoT 디바이스에 주기적 이벤트가 게시되는 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-143">Topic where periodic events are published to IoT device.</span></span>

```yaml
Type: System.String
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecf2d-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ecf2d-144">-Confirm</span></span>
<span data-ttu-id="ecf2d-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecf2d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecf2d-146">-WhatIf</span></span>
<span data-ttu-id="ecf2d-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ecf2d-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ecf2d-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecf2d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecf2d-149">CommonParameters</span></span>
<span data-ttu-id="ecf2d-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecf2d-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecf2d-152">입력</span><span class="sxs-lookup"><span data-stu-id="ecf2d-152">INPUTS</span></span>

### <span data-ttu-id="ecf2d-153">없음</span><span class="sxs-lookup"><span data-stu-id="ecf2d-153">None</span></span>

## <span data-ttu-id="ecf2d-154">출력</span><span class="sxs-lookup"><span data-stu-id="ecf2d-154">OUTPUTS</span></span>

### <span data-ttu-id="ecf2d-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="ecf2d-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="ecf2d-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ecf2d-156">NOTES</span></span>

## <span data-ttu-id="ecf2d-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecf2d-157">RELATED LINKS</span></span>
