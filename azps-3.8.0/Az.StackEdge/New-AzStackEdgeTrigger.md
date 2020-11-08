---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeTrigger.md
ms.openlocfilehash: d13498df4c91c8d31b8bfe2e19e9f7fa23f99998
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034206"
---
# <span data-ttu-id="dbf3f-101">New-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="dbf3f-101">New-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="dbf3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbf3f-102">SYNOPSIS</span></span>
<span data-ttu-id="dbf3f-103">장치에서 트리거를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbf3f-103">Configures a trigger on the device.</span></span>

## <span data-ttu-id="dbf3f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dbf3f-104">SYNTAX</span></span>

### <span data-ttu-id="dbf3f-105">FileEventTriggerParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="dbf3f-105">FileEventTriggerParameterSet (Default)</span></span>
```
New-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -RoleName <String>
 [-FileEvent] -ShareName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dbf3f-106">PeriodicTimerTriggerParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbf3f-106">PeriodicTimerTriggerParameterSet</span></span>
```
New-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -RoleName <String>
 [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>] -Schedule <String>
 -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbf3f-107">FileEventTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbf3f-107">FileEventTriggerResourceIdParameterSet</span></span>
```
New-AzStackEdgeTrigger [-FileEvent] -ShareId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbf3f-108">PeriodicTimerTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbf3f-108">PeriodicTimerTriggerResourceIdParameterSet</span></span>
```
New-AzStackEdgeTrigger [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbf3f-109">설명은</span><span class="sxs-lookup"><span data-stu-id="dbf3f-109">DESCRIPTION</span></span>
<span data-ttu-id="dbf3f-110">**AzStackEdgeTrigger** Cmdlet은 스택 가장자리 장치에서 트리거를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbf3f-110">The **New-AzStackEdgeTrigger** cmdlet configures a trigger on the Stack Edge device.</span></span> 

## <span data-ttu-id="dbf3f-111">예제의</span><span class="sxs-lookup"><span data-stu-id="dbf3f-111">EXAMPLES</span></span>

### <span data-ttu-id="dbf3f-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="dbf3f-112">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -PeriodicTimerEvent -Name periodic-trigger -RoleName IOTRole -Schedule "00:00" -StartTime "2019-10-28 12:00:00" -Topic sample-topic
Name                  Kind               
----                  ----               
periodic-trigger      PeriodicTimerEvent
```

## <span data-ttu-id="dbf3f-113">변수</span><span class="sxs-lookup"><span data-stu-id="dbf3f-113">PARAMETERS</span></span>

### <span data-ttu-id="dbf3f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dbf3f-114">-AsJob</span></span>
<span data-ttu-id="dbf3f-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="dbf3f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dbf3f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbf3f-116">-DefaultProfile</span></span>
<span data-ttu-id="dbf3f-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf3f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbf3f-118">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="dbf3f-118">-DeviceName</span></span>
<span data-ttu-id="dbf3f-119">장치 이름</span><span class="sxs-lookup"><span data-stu-id="dbf3f-119">Device Name</span></span>

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

### <span data-ttu-id="dbf3f-120">-FileEvent</span><span class="sxs-lookup"><span data-stu-id="dbf3f-120">-FileEvent</span></span>
<span data-ttu-id="dbf3f-121">이 스위치 매개 변수를 전달 하 여 FileEvent 트리거 구성</span><span class="sxs-lookup"><span data-stu-id="dbf3f-121">Pass this switch parameter to configure FileEvent Trigger</span></span>

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

### <span data-ttu-id="dbf3f-122">-이름</span><span class="sxs-lookup"><span data-stu-id="dbf3f-122">-Name</span></span>
<span data-ttu-id="dbf3f-123">자원 이름</span><span class="sxs-lookup"><span data-stu-id="dbf3f-123">Resource Name</span></span>

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

### <span data-ttu-id="dbf3f-124">-PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="dbf3f-124">-PeriodicTimerEvent</span></span>
<span data-ttu-id="dbf3f-125">이 스위치 매개 변수를 전달 하 여 PeriodicTimerEvent 트리거 구성</span><span class="sxs-lookup"><span data-stu-id="dbf3f-125">Pass this switch parameter to configure PeriodicTimerEvent Trigger</span></span>

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

### <span data-ttu-id="dbf3f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbf3f-126">-ResourceGroupName</span></span>
<span data-ttu-id="dbf3f-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="dbf3f-127">Resource Group Name</span></span>

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

### <span data-ttu-id="dbf3f-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="dbf3f-128">-RoleName</span></span>
<span data-ttu-id="dbf3f-129">이벤트를 발생 시킬 역할을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbf3f-129">Compute role against which events will be raised.</span></span>

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

### <span data-ttu-id="dbf3f-130">-일정</span><span class="sxs-lookup"><span data-stu-id="dbf3f-130">-Schedule</span></span>
<span data-ttu-id="dbf3f-131">타이머 이벤트를 발생 시켜야 하는 정기 빈도입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf3f-131">Periodic frequency at which timer event needs to be raised.</span></span> <span data-ttu-id="dbf3f-132">일정을 일 단위 (1 ~ 365), 시간 (1 ~ 23) 또는 분 (1 ~ 59) 중에서 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbf3f-132">Specify a schedule in either days (between 1 and 365) , hours (between 1 and 23), or minutes (between 1 and 59).</span></span>

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

### <span data-ttu-id="dbf3f-133">-ShareId</span><span class="sxs-lookup"><span data-stu-id="dbf3f-133">-ShareId</span></span>
<span data-ttu-id="dbf3f-134">FileEvent Trigger에 전달 될 파일 공유 ID</span><span class="sxs-lookup"><span data-stu-id="dbf3f-134">File share ID to be passed in FileEvent Trigger</span></span>

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

### <span data-ttu-id="dbf3f-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="dbf3f-135">-ShareName</span></span>
<span data-ttu-id="dbf3f-136">FileEvent Trigger에 전달 될 파일 공유 ID</span><span class="sxs-lookup"><span data-stu-id="dbf3f-136">File share ID to be passed in FileEvent Trigger</span></span>

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

### <span data-ttu-id="dbf3f-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="dbf3f-137">-StartTime</span></span>
<span data-ttu-id="dbf3f-138">일이 유효한 트리거를 반환 하는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf3f-138">The time of the day that results in a valid trigger.</span></span> <span data-ttu-id="dbf3f-139">일정은 지정 된 시간에 대 한 참조를 사용 하 여 초 단위로 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dbf3f-139">Schedule is computed with reference to the time specified up to seconds.</span></span> <span data-ttu-id="dbf3f-140">Timezone가 지정 되지 않은 경우 시간은 장치 표준 시간대로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dbf3f-140">If timezone is not specified the time will considered to be in device timezone.</span></span> <span data-ttu-id="dbf3f-141">값은 항상 UTC 시간으로 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dbf3f-141">The value will always be returned as UTC time.</span></span>

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

### <span data-ttu-id="dbf3f-142">-주제</span><span class="sxs-lookup"><span data-stu-id="dbf3f-142">-Topic</span></span>
<span data-ttu-id="dbf3f-143">IoT 장치에 정기 이벤트가 게시 되는 주제입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf3f-143">Topic where periodic events are published to IoT device.</span></span>

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

### <span data-ttu-id="dbf3f-144">-확인</span><span class="sxs-lookup"><span data-stu-id="dbf3f-144">-Confirm</span></span>
<span data-ttu-id="dbf3f-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbf3f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbf3f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbf3f-146">-WhatIf</span></span>
<span data-ttu-id="dbf3f-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dbf3f-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dbf3f-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dbf3f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbf3f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbf3f-149">CommonParameters</span></span>
<span data-ttu-id="dbf3f-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbf3f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbf3f-151">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dbf3f-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbf3f-152">입력</span><span class="sxs-lookup"><span data-stu-id="dbf3f-152">INPUTS</span></span>

### <span data-ttu-id="dbf3f-153">않아야</span><span class="sxs-lookup"><span data-stu-id="dbf3f-153">None</span></span>

## <span data-ttu-id="dbf3f-154">출력</span><span class="sxs-lookup"><span data-stu-id="dbf3f-154">OUTPUTS</span></span>

### <span data-ttu-id="dbf3f-155">StackEdge. PSStackEdgeTrigger에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="dbf3f-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="dbf3f-156">상속자</span><span class="sxs-lookup"><span data-stu-id="dbf3f-156">NOTES</span></span>

## <span data-ttu-id="dbf3f-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dbf3f-157">RELATED LINKS</span></span>
