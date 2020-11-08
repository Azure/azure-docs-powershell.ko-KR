---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: db54799f13ca7524ccf42ade8b7e33c61a134ae9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217208"
---
# <span data-ttu-id="b0e4e-101">Set-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="b0e4e-101">Set-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="b0e4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0e4e-102">SYNOPSIS</span></span>
<span data-ttu-id="b0e4e-103">대역폭 일정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e4e-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="b0e4e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0e4e-104">SYNTAX</span></span>

### <span data-ttu-id="b0e4e-105">UpdateByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b0e4e-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0e4e-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0e4e-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0e4e-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="b0e4e-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0e4e-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="b0e4e-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0e4e-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0e4e-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0e4e-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="b0e4e-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0e4e-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="b0e4e-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0e4e-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="b0e4e-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0e4e-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="b0e4e-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0e4e-114">설명은</span><span class="sxs-lookup"><span data-stu-id="b0e4e-114">DESCRIPTION</span></span>
<span data-ttu-id="b0e4e-115">**AzStackEdgeBandwidthSchedule** Cmdlet은 스택 경계 장치에 대 한 대역폭 일정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e4e-115">The **Set-AzStackEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Stack Edge device.</span></span>

## <span data-ttu-id="b0e4e-116">예제의</span><span class="sxs-lookup"><span data-stu-id="b0e4e-116">EXAMPLES</span></span>

### <span data-ttu-id="b0e4e-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="b0e4e-117">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="b0e4e-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="b0e4e-118">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="b0e4e-119">변수</span><span class="sxs-lookup"><span data-stu-id="b0e4e-119">PARAMETERS</span></span>

### <span data-ttu-id="b0e4e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0e4e-120">-AsJob</span></span>
<span data-ttu-id="b0e4e-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b0e4e-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0e4e-122">-대역폭</span><span class="sxs-lookup"><span data-stu-id="b0e4e-122">-Bandwidth</span></span>
<span data-ttu-id="b0e4e-123">Mbps 단위 대역폭</span><span class="sxs-lookup"><span data-stu-id="b0e4e-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="b0e4e-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="b0e4e-124">-DaysOfWeek</span></span>
<span data-ttu-id="b0e4e-125">예정 된 DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="b0e4e-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="b0e4e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0e4e-126">-DefaultProfile</span></span>
<span data-ttu-id="b0e4e-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0e4e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0e4e-128">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="b0e4e-128">-DeviceName</span></span>
<span data-ttu-id="b0e4e-129">장치 이름</span><span class="sxs-lookup"><span data-stu-id="b0e4e-129">Device Name</span></span>

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

### <span data-ttu-id="b0e4e-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0e4e-130">-InputObject</span></span>
<span data-ttu-id="b0e4e-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0e4e-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="b0e4e-132">-이름</span><span class="sxs-lookup"><span data-stu-id="b0e4e-132">-Name</span></span>
<span data-ttu-id="b0e4e-133">자원 이름</span><span class="sxs-lookup"><span data-stu-id="b0e4e-133">Resource Name</span></span>

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

### <span data-ttu-id="b0e4e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0e4e-134">-ResourceGroupName</span></span>
<span data-ttu-id="b0e4e-135">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b0e4e-135">Resource Group Name</span></span>

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

### <span data-ttu-id="b0e4e-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0e4e-136">-ResourceId</span></span>
<span data-ttu-id="b0e4e-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0e4e-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="b0e4e-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b0e4e-138">-StartTime</span></span>
<span data-ttu-id="b0e4e-139">일정 시작 시간</span><span class="sxs-lookup"><span data-stu-id="b0e4e-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="b0e4e-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="b0e4e-140">-StopTime</span></span>
<span data-ttu-id="b0e4e-141">일정 중지 시간</span><span class="sxs-lookup"><span data-stu-id="b0e4e-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="b0e4e-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="b0e4e-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="b0e4e-143">무제한 대역폭을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e4e-143">Will Set Unlimited Bandwidth</span></span>

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

### <span data-ttu-id="b0e4e-144">-확인</span><span class="sxs-lookup"><span data-stu-id="b0e4e-144">-Confirm</span></span>
<span data-ttu-id="b0e4e-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e4e-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0e4e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0e4e-146">-WhatIf</span></span>
<span data-ttu-id="b0e4e-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b0e4e-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0e4e-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0e4e-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0e4e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0e4e-149">CommonParameters</span></span>
<span data-ttu-id="b0e4e-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e4e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0e4e-151">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b0e4e-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0e4e-152">입력</span><span class="sxs-lookup"><span data-stu-id="b0e4e-152">INPUTS</span></span>

### <span data-ttu-id="b0e4e-153">않아야</span><span class="sxs-lookup"><span data-stu-id="b0e4e-153">None</span></span>

## <span data-ttu-id="b0e4e-154">출력</span><span class="sxs-lookup"><span data-stu-id="b0e4e-154">OUTPUTS</span></span>

### <span data-ttu-id="b0e4e-155">StackEdge. PSStackEdgeBandWidthSchedule에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="b0e4e-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="b0e4e-156">상속자</span><span class="sxs-lookup"><span data-stu-id="b0e4e-156">NOTES</span></span>

## <span data-ttu-id="b0e4e-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0e4e-157">RELATED LINKS</span></span>
