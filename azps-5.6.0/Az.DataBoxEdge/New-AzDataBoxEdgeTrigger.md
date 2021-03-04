---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 195be7fb51e947888c7c22911f4fb5177454731e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977147"
---
# <span data-ttu-id="fb28c-101">New-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="fb28c-101">New-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="fb28c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb28c-102">SYNOPSIS</span></span>
<span data-ttu-id="fb28c-103">디바이스에서 트리거를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="fb28c-103">Configures a trigger on the device.</span></span>

## <span data-ttu-id="fb28c-104">구문</span><span class="sxs-lookup"><span data-stu-id="fb28c-104">SYNTAX</span></span>

### <span data-ttu-id="fb28c-105">FileEventTriggerParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="fb28c-105">FileEventTriggerParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-FileEvent] -ShareName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb28c-106">PeriodicTimerTriggerParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb28c-106">PeriodicTimerTriggerParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb28c-107">FileEventTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb28c-107">FileEventTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-FileEvent] -ShareId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb28c-108">PeriodicTimerTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb28c-108">PeriodicTimerTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb28c-109">설명</span><span class="sxs-lookup"><span data-stu-id="fb28c-109">DESCRIPTION</span></span>
<span data-ttu-id="fb28c-110">**New-AzDataBoxEdgeTrigger** cmdlet은 Data Box Edge 디바이스에서 트리거를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="fb28c-110">The **New-AzDataBoxEdgeTrigger** cmdlet configures a trigger on the Data Box Edge device.</span></span> 

## <span data-ttu-id="fb28c-111">예제</span><span class="sxs-lookup"><span data-stu-id="fb28c-111">EXAMPLES</span></span>

### <span data-ttu-id="fb28c-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="fb28c-112">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -PeriodicTimerEvent -Name periodic-trigger -RoleName IOTRole -Schedule "00:00" -StartTime "2019-10-28 12:00:00" -Topic sample-topic
Name                  Kind               
----                  ----               
periodic-trigger      PeriodicTimerEvent
```

## <span data-ttu-id="fb28c-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fb28c-113">PARAMETERS</span></span>

### <span data-ttu-id="fb28c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb28c-114">-AsJob</span></span>
<span data-ttu-id="fb28c-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fb28c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb28c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb28c-116">-DefaultProfile</span></span>
<span data-ttu-id="fb28c-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb28c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb28c-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="fb28c-118">-DeviceName</span></span>
<span data-ttu-id="fb28c-119">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="fb28c-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb28c-120">-FileEvent</span><span class="sxs-lookup"><span data-stu-id="fb28c-120">-FileEvent</span></span>
<span data-ttu-id="fb28c-121">이 스위치 매개 변수를 전달하여 FileEvent Trigger를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="fb28c-121">Pass this switch parameter to configure FileEvent Trigger</span></span>

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

### <span data-ttu-id="fb28c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fb28c-122">-Name</span></span>
<span data-ttu-id="fb28c-123">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="fb28c-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb28c-124">-PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="fb28c-124">-PeriodicTimerEvent</span></span>
<span data-ttu-id="fb28c-125">이 스위치 매개 변수를 전달하여 PeriodicTimerEvent 트리거를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="fb28c-125">Pass this switch parameter to configure PeriodicTimerEvent Trigger</span></span>

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

### <span data-ttu-id="fb28c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb28c-126">-ResourceGroupName</span></span>
<span data-ttu-id="fb28c-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="fb28c-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb28c-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="fb28c-128">-RoleName</span></span>
<span data-ttu-id="fb28c-129">어떤 이벤트가 발생될지 계산 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="fb28c-129">Compute role against which events will be raised.</span></span>

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

### <span data-ttu-id="fb28c-130">-Schedule</span><span class="sxs-lookup"><span data-stu-id="fb28c-130">-Schedule</span></span>
<span data-ttu-id="fb28c-131">시간 이벤트가 발생해야 하는 주기적 빈도입니다.</span><span class="sxs-lookup"><span data-stu-id="fb28c-131">Periodic frequency at which timer event needs to be raised.</span></span> <span data-ttu-id="fb28c-132">일정을 일(1~365 사이) 또는 시간(1~23 사이) 또는 분(1~59 사이)으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fb28c-132">Specify a schedule in either days (between 1 and 365) , hours (between 1 and 23), or minutes (between 1 and 59).</span></span>

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

### <span data-ttu-id="fb28c-133">-ShareId</span><span class="sxs-lookup"><span data-stu-id="fb28c-133">-ShareId</span></span>
<span data-ttu-id="fb28c-134">FileEvent Trigger에서 전달할 파일 공유 ID</span><span class="sxs-lookup"><span data-stu-id="fb28c-134">File share ID to be passed in FileEvent Trigger</span></span>

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

### <span data-ttu-id="fb28c-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="fb28c-135">-ShareName</span></span>
<span data-ttu-id="fb28c-136">FileEvent Trigger에서 전달할 파일 공유 ID</span><span class="sxs-lookup"><span data-stu-id="fb28c-136">File share ID to be passed in FileEvent Trigger</span></span>

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

### <span data-ttu-id="fb28c-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="fb28c-137">-StartTime</span></span>
<span data-ttu-id="fb28c-138">유효한 트리거가 발생되는 하루의 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="fb28c-138">The time of the day that results in a valid trigger.</span></span> <span data-ttu-id="fb28c-139">일정은 최대 초까지 지정된 시간을 참조하여 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb28c-139">Schedule is computed with reference to the time specified up to seconds.</span></span> <span data-ttu-id="fb28c-140">타임존이 지정되지 않은 경우 디바이스 타임존에 있는 것으로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb28c-140">If timezone is not specified the time will considered to be in device timezone.</span></span> <span data-ttu-id="fb28c-141">값은 항상 UTC 시간으로 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb28c-141">The value will always be returned as UTC time.</span></span>

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

### <span data-ttu-id="fb28c-142">-Topic</span><span class="sxs-lookup"><span data-stu-id="fb28c-142">-Topic</span></span>
<span data-ttu-id="fb28c-143">주기적인 이벤트가 IoT 디바이스에 게시되는 토픽입니다.</span><span class="sxs-lookup"><span data-stu-id="fb28c-143">Topic where periodic events are published to IoT device.</span></span>

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

### <span data-ttu-id="fb28c-144">-확인</span><span class="sxs-lookup"><span data-stu-id="fb28c-144">-Confirm</span></span>
<span data-ttu-id="fb28c-145">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb28c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb28c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb28c-146">-WhatIf</span></span>
<span data-ttu-id="fb28c-147">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="fb28c-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb28c-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb28c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb28c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb28c-149">CommonParameters</span></span>
<span data-ttu-id="fb28c-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fb28c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb28c-151">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb28c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb28c-152">입력</span><span class="sxs-lookup"><span data-stu-id="fb28c-152">INPUTS</span></span>

### <span data-ttu-id="fb28c-153">없음</span><span class="sxs-lookup"><span data-stu-id="fb28c-153">None</span></span>

## <span data-ttu-id="fb28c-154">출력</span><span class="sxs-lookup"><span data-stu-id="fb28c-154">OUTPUTS</span></span>

### <span data-ttu-id="fb28c-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="fb28c-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="fb28c-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fb28c-156">NOTES</span></span>

## <span data-ttu-id="fb28c-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb28c-157">RELATED LINKS</span></span>
