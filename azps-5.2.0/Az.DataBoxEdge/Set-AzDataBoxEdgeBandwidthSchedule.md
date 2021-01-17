---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 503f274b07b13bc19b4994f8b440ffc853f69bc5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366010"
---
# <span data-ttu-id="eea53-101">Set-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="eea53-101">Set-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="eea53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eea53-102">SYNOPSIS</span></span>
<span data-ttu-id="eea53-103">대역폭 일정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="eea53-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="eea53-104">구문</span><span class="sxs-lookup"><span data-stu-id="eea53-104">SYNTAX</span></span>

### <span data-ttu-id="eea53-105">UpdateByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="eea53-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eea53-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eea53-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eea53-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="eea53-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eea53-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="eea53-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eea53-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eea53-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eea53-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="eea53-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eea53-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="eea53-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eea53-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="eea53-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eea53-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="eea53-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eea53-114">설명</span><span class="sxs-lookup"><span data-stu-id="eea53-114">DESCRIPTION</span></span>
<span data-ttu-id="eea53-115">**Set-AzDataBoxEdgeBandwidthSchedule** cmdlet은 Data Box Edge 디바이스에 대한 대역폭 일정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="eea53-115">The **Set-AzDataBoxEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Data Box Edge device.</span></span>

## <span data-ttu-id="eea53-116">예제</span><span class="sxs-lookup"><span data-stu-id="eea53-116">EXAMPLES</span></span>

### <span data-ttu-id="eea53-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="eea53-117">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="eea53-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="eea53-118">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="eea53-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eea53-119">PARAMETERS</span></span>

### <span data-ttu-id="eea53-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eea53-120">-AsJob</span></span>
<span data-ttu-id="eea53-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="eea53-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eea53-122">-Bandwidth</span><span class="sxs-lookup"><span data-stu-id="eea53-122">-Bandwidth</span></span>
<span data-ttu-id="eea53-123">대역폭(Mbps)</span><span class="sxs-lookup"><span data-stu-id="eea53-123">Bandwidth in Mbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateByResourceIdParameterBandwidthSet, UpdateByInputObjectParameterBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea53-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="eea53-124">-DaysOfWeek</span></span>
<span data-ttu-id="eea53-125">Scheduled DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="eea53-125">Scheduled DaysOfWeek</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea53-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea53-126">-DefaultProfile</span></span>
<span data-ttu-id="eea53-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eea53-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eea53-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="eea53-128">-DeviceName</span></span>
<span data-ttu-id="eea53-129">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="eea53-129">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea53-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eea53-130">-InputObject</span></span>
<span data-ttu-id="eea53-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="eea53-131">Azure ResourceId</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule
Parameter Sets: UpdateByInputObjectParameterSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea53-132">-Name</span><span class="sxs-lookup"><span data-stu-id="eea53-132">-Name</span></span>
<span data-ttu-id="eea53-133">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="eea53-133">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea53-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eea53-134">-ResourceGroupName</span></span>
<span data-ttu-id="eea53-135">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="eea53-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea53-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eea53-136">-ResourceId</span></span>
<span data-ttu-id="eea53-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="eea53-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet, UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByResourceIdParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea53-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="eea53-138">-StartTime</span></span>
<span data-ttu-id="eea53-139">시작 시간 예약</span><span class="sxs-lookup"><span data-stu-id="eea53-139">Schedule Start Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea53-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="eea53-140">-StopTime</span></span>
<span data-ttu-id="eea53-141">일정 중지 시간</span><span class="sxs-lookup"><span data-stu-id="eea53-141">Schedule Stop Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea53-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="eea53-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="eea53-143">무제한 대역폭을 설정할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="eea53-143">Will Set Unlimited Bandwidth</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByNameParameterUnlimitedBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea53-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eea53-144">-Confirm</span></span>
<span data-ttu-id="eea53-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea53-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eea53-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eea53-146">-WhatIf</span></span>
<span data-ttu-id="eea53-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="eea53-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eea53-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eea53-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eea53-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea53-149">CommonParameters</span></span>
<span data-ttu-id="eea53-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eea53-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea53-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="eea53-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea53-152">입력</span><span class="sxs-lookup"><span data-stu-id="eea53-152">INPUTS</span></span>

### <span data-ttu-id="eea53-153">없음</span><span class="sxs-lookup"><span data-stu-id="eea53-153">None</span></span>

## <span data-ttu-id="eea53-154">출력</span><span class="sxs-lookup"><span data-stu-id="eea53-154">OUTPUTS</span></span>

### <span data-ttu-id="eea53-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="eea53-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="eea53-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="eea53-156">NOTES</span></span>

## <span data-ttu-id="eea53-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eea53-157">RELATED LINKS</span></span>
