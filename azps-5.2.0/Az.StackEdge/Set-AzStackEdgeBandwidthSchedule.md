---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: db54799f13ca7524ccf42ade8b7e33c61a134ae9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358681"
---
# <span data-ttu-id="25bbf-101">Set-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="25bbf-101">Set-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="25bbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25bbf-102">SYNOPSIS</span></span>
<span data-ttu-id="25bbf-103">대역폭 일정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="25bbf-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="25bbf-104">구문</span><span class="sxs-lookup"><span data-stu-id="25bbf-104">SYNTAX</span></span>

### <span data-ttu-id="25bbf-105">UpdateByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="25bbf-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25bbf-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25bbf-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25bbf-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="25bbf-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25bbf-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="25bbf-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25bbf-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25bbf-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25bbf-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="25bbf-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25bbf-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="25bbf-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25bbf-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="25bbf-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25bbf-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="25bbf-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25bbf-114">설명</span><span class="sxs-lookup"><span data-stu-id="25bbf-114">DESCRIPTION</span></span>
<span data-ttu-id="25bbf-115">**Set-AzStackEdgeBandwidthSchedule** cmdlet은 Stack Edge 디바이스에 대한 대역폭 일정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="25bbf-115">The **Set-AzStackEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Stack Edge device.</span></span>

## <span data-ttu-id="25bbf-116">예제</span><span class="sxs-lookup"><span data-stu-id="25bbf-116">EXAMPLES</span></span>

### <span data-ttu-id="25bbf-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="25bbf-117">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="25bbf-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="25bbf-118">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="25bbf-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25bbf-119">PARAMETERS</span></span>

### <span data-ttu-id="25bbf-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25bbf-120">-AsJob</span></span>
<span data-ttu-id="25bbf-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="25bbf-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25bbf-122">-Bandwidth</span><span class="sxs-lookup"><span data-stu-id="25bbf-122">-Bandwidth</span></span>
<span data-ttu-id="25bbf-123">대역폭(Mbps)</span><span class="sxs-lookup"><span data-stu-id="25bbf-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="25bbf-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="25bbf-124">-DaysOfWeek</span></span>
<span data-ttu-id="25bbf-125">Scheduled DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="25bbf-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="25bbf-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25bbf-126">-DefaultProfile</span></span>
<span data-ttu-id="25bbf-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="25bbf-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25bbf-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="25bbf-128">-DeviceName</span></span>
<span data-ttu-id="25bbf-129">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="25bbf-129">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25bbf-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25bbf-130">-InputObject</span></span>
<span data-ttu-id="25bbf-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="25bbf-131">Azure ResourceId</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule
Parameter Sets: UpdateByInputObjectParameterSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterBandwidthSet
Aliases: BandwidthSchedule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25bbf-132">-Name</span><span class="sxs-lookup"><span data-stu-id="25bbf-132">-Name</span></span>
<span data-ttu-id="25bbf-133">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="25bbf-133">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25bbf-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25bbf-134">-ResourceGroupName</span></span>
<span data-ttu-id="25bbf-135">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="25bbf-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25bbf-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25bbf-136">-ResourceId</span></span>
<span data-ttu-id="25bbf-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="25bbf-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet, UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByResourceIdParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25bbf-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="25bbf-138">-StartTime</span></span>
<span data-ttu-id="25bbf-139">시작 시간 예약</span><span class="sxs-lookup"><span data-stu-id="25bbf-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="25bbf-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="25bbf-140">-StopTime</span></span>
<span data-ttu-id="25bbf-141">일정 중지 시간</span><span class="sxs-lookup"><span data-stu-id="25bbf-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="25bbf-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="25bbf-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="25bbf-143">무제한 대역폭을 설정할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="25bbf-143">Will Set Unlimited Bandwidth</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByNameParameterUnlimitedBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25bbf-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25bbf-144">-Confirm</span></span>
<span data-ttu-id="25bbf-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="25bbf-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25bbf-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25bbf-146">-WhatIf</span></span>
<span data-ttu-id="25bbf-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="25bbf-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25bbf-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25bbf-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25bbf-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25bbf-149">CommonParameters</span></span>
<span data-ttu-id="25bbf-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="25bbf-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25bbf-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="25bbf-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25bbf-152">입력</span><span class="sxs-lookup"><span data-stu-id="25bbf-152">INPUTS</span></span>

### <span data-ttu-id="25bbf-153">없음</span><span class="sxs-lookup"><span data-stu-id="25bbf-153">None</span></span>

## <span data-ttu-id="25bbf-154">출력</span><span class="sxs-lookup"><span data-stu-id="25bbf-154">OUTPUTS</span></span>

### <span data-ttu-id="25bbf-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="25bbf-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="25bbf-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="25bbf-156">NOTES</span></span>

## <span data-ttu-id="25bbf-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25bbf-157">RELATED LINKS</span></span>
