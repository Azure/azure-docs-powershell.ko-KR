---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 503f274b07b13bc19b4994f8b440ffc853f69bc5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214588"
---
# <span data-ttu-id="34846-101">Set-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="34846-101">Set-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="34846-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34846-102">SYNOPSIS</span></span>
<span data-ttu-id="34846-103">대역폭 일정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="34846-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="34846-104">구문과</span><span class="sxs-lookup"><span data-stu-id="34846-104">SYNTAX</span></span>

### <span data-ttu-id="34846-105">UpdateByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="34846-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34846-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="34846-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34846-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="34846-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34846-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="34846-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34846-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34846-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34846-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="34846-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34846-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="34846-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34846-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="34846-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34846-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="34846-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34846-114">설명은</span><span class="sxs-lookup"><span data-stu-id="34846-114">DESCRIPTION</span></span>
<span data-ttu-id="34846-115">**AzDataBoxEdgeBandwidthSchedule** Cmdlet은 데이터 상자 가장자리 장치에 대 한 대역폭 일정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="34846-115">The **Set-AzDataBoxEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Data Box Edge device.</span></span>

## <span data-ttu-id="34846-116">예제의</span><span class="sxs-lookup"><span data-stu-id="34846-116">EXAMPLES</span></span>

### <span data-ttu-id="34846-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="34846-117">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="34846-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="34846-118">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="34846-119">변수</span><span class="sxs-lookup"><span data-stu-id="34846-119">PARAMETERS</span></span>

### <span data-ttu-id="34846-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34846-120">-AsJob</span></span>
<span data-ttu-id="34846-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="34846-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34846-122">-대역폭</span><span class="sxs-lookup"><span data-stu-id="34846-122">-Bandwidth</span></span>
<span data-ttu-id="34846-123">Mbps 단위 대역폭</span><span class="sxs-lookup"><span data-stu-id="34846-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="34846-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="34846-124">-DaysOfWeek</span></span>
<span data-ttu-id="34846-125">예정 된 DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="34846-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="34846-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34846-126">-DefaultProfile</span></span>
<span data-ttu-id="34846-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34846-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34846-128">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="34846-128">-DeviceName</span></span>
<span data-ttu-id="34846-129">장치 이름</span><span class="sxs-lookup"><span data-stu-id="34846-129">Device Name</span></span>

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

### <span data-ttu-id="34846-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34846-130">-InputObject</span></span>
<span data-ttu-id="34846-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="34846-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="34846-132">-이름</span><span class="sxs-lookup"><span data-stu-id="34846-132">-Name</span></span>
<span data-ttu-id="34846-133">자원 이름</span><span class="sxs-lookup"><span data-stu-id="34846-133">Resource Name</span></span>

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

### <span data-ttu-id="34846-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34846-134">-ResourceGroupName</span></span>
<span data-ttu-id="34846-135">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="34846-135">Resource Group Name</span></span>

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

### <span data-ttu-id="34846-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34846-136">-ResourceId</span></span>
<span data-ttu-id="34846-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="34846-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="34846-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="34846-138">-StartTime</span></span>
<span data-ttu-id="34846-139">일정 시작 시간</span><span class="sxs-lookup"><span data-stu-id="34846-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="34846-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="34846-140">-StopTime</span></span>
<span data-ttu-id="34846-141">일정 중지 시간</span><span class="sxs-lookup"><span data-stu-id="34846-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="34846-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="34846-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="34846-143">무제한 대역폭을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34846-143">Will Set Unlimited Bandwidth</span></span>

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

### <span data-ttu-id="34846-144">-확인</span><span class="sxs-lookup"><span data-stu-id="34846-144">-Confirm</span></span>
<span data-ttu-id="34846-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="34846-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34846-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34846-146">-WhatIf</span></span>
<span data-ttu-id="34846-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="34846-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34846-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34846-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34846-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34846-149">CommonParameters</span></span>
<span data-ttu-id="34846-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="34846-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34846-151">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="34846-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34846-152">입력</span><span class="sxs-lookup"><span data-stu-id="34846-152">INPUTS</span></span>

### <span data-ttu-id="34846-153">않아야</span><span class="sxs-lookup"><span data-stu-id="34846-153">None</span></span>

## <span data-ttu-id="34846-154">출력</span><span class="sxs-lookup"><span data-stu-id="34846-154">OUTPUTS</span></span>

### <span data-ttu-id="34846-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="34846-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="34846-156">상속자</span><span class="sxs-lookup"><span data-stu-id="34846-156">NOTES</span></span>

## <span data-ttu-id="34846-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34846-157">RELATED LINKS</span></span>
