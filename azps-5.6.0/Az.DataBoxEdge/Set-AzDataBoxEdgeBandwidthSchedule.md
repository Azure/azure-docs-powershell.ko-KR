---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/set-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: d0f5d0d71f35df5bb36ea86a1ec20ca009256f67
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983184"
---
# <span data-ttu-id="4c20c-101">Set-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="4c20c-101">Set-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="4c20c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c20c-102">SYNOPSIS</span></span>
<span data-ttu-id="4c20c-103">대역폭 일정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4c20c-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="4c20c-104">구문</span><span class="sxs-lookup"><span data-stu-id="4c20c-104">SYNTAX</span></span>

### <span data-ttu-id="4c20c-105">UpdateByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4c20c-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c20c-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c20c-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c20c-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="4c20c-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c20c-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="4c20c-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c20c-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c20c-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c20c-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="4c20c-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c20c-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="4c20c-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c20c-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="4c20c-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c20c-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="4c20c-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c20c-114">설명</span><span class="sxs-lookup"><span data-stu-id="4c20c-114">DESCRIPTION</span></span>
<span data-ttu-id="4c20c-115">**Set-AzDataBoxEdgeBandwidthSchedule** cmdlet은 Data Box Edge 디바이스에 대한 대역폭 일정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4c20c-115">The **Set-AzDataBoxEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Data Box Edge device.</span></span>

## <span data-ttu-id="4c20c-116">예제</span><span class="sxs-lookup"><span data-stu-id="4c20c-116">EXAMPLES</span></span>

### <span data-ttu-id="4c20c-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="4c20c-117">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="4c20c-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="4c20c-118">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="4c20c-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4c20c-119">PARAMETERS</span></span>

### <span data-ttu-id="4c20c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c20c-120">-AsJob</span></span>
<span data-ttu-id="4c20c-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4c20c-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c20c-122">-대역폭</span><span class="sxs-lookup"><span data-stu-id="4c20c-122">-Bandwidth</span></span>
<span data-ttu-id="4c20c-123">Mbps의 대역폭</span><span class="sxs-lookup"><span data-stu-id="4c20c-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="4c20c-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="4c20c-124">-DaysOfWeek</span></span>
<span data-ttu-id="4c20c-125">예약된 DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="4c20c-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="4c20c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c20c-126">-DefaultProfile</span></span>
<span data-ttu-id="4c20c-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4c20c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c20c-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="4c20c-128">-DeviceName</span></span>
<span data-ttu-id="4c20c-129">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="4c20c-129">Device Name</span></span>

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

### <span data-ttu-id="4c20c-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c20c-130">-InputObject</span></span>
<span data-ttu-id="4c20c-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c20c-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="4c20c-132">-Name</span><span class="sxs-lookup"><span data-stu-id="4c20c-132">-Name</span></span>
<span data-ttu-id="4c20c-133">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="4c20c-133">Resource Name</span></span>

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

### <span data-ttu-id="4c20c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c20c-134">-ResourceGroupName</span></span>
<span data-ttu-id="4c20c-135">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4c20c-135">Resource Group Name</span></span>

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

### <span data-ttu-id="4c20c-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c20c-136">-ResourceId</span></span>
<span data-ttu-id="4c20c-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c20c-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="4c20c-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4c20c-138">-StartTime</span></span>
<span data-ttu-id="4c20c-139">시작 시간 예약</span><span class="sxs-lookup"><span data-stu-id="4c20c-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="4c20c-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="4c20c-140">-StopTime</span></span>
<span data-ttu-id="4c20c-141">일정 중지 시간</span><span class="sxs-lookup"><span data-stu-id="4c20c-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="4c20c-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="4c20c-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="4c20c-143">무제한 대역폭을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4c20c-143">Will Set Unlimited Bandwidth</span></span>

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

### <span data-ttu-id="4c20c-144">-확인</span><span class="sxs-lookup"><span data-stu-id="4c20c-144">-Confirm</span></span>
<span data-ttu-id="4c20c-145">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c20c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c20c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c20c-146">-WhatIf</span></span>
<span data-ttu-id="4c20c-147">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4c20c-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c20c-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c20c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c20c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c20c-149">CommonParameters</span></span>
<span data-ttu-id="4c20c-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4c20c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c20c-151">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c20c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c20c-152">입력</span><span class="sxs-lookup"><span data-stu-id="4c20c-152">INPUTS</span></span>

### <span data-ttu-id="4c20c-153">없음</span><span class="sxs-lookup"><span data-stu-id="4c20c-153">None</span></span>

## <span data-ttu-id="4c20c-154">출력</span><span class="sxs-lookup"><span data-stu-id="4c20c-154">OUTPUTS</span></span>

### <span data-ttu-id="4c20c-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="4c20c-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="4c20c-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4c20c-156">NOTES</span></span>

## <span data-ttu-id="4c20c-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4c20c-157">RELATED LINKS</span></span>
