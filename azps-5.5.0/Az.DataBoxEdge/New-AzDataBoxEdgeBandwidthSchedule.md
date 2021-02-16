---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 68522dbd90593bdbc37afe333144431b997cc70c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188665"
---
# <span data-ttu-id="a3c10-101">New-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="a3c10-101">New-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="a3c10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3c10-102">SYNOPSIS</span></span>
<span data-ttu-id="a3c10-103">새 대역폭 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a3c10-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="a3c10-104">구문</span><span class="sxs-lookup"><span data-stu-id="a3c10-104">SYNTAX</span></span>

### <span data-ttu-id="a3c10-105">BandwidthParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a3c10-105">BandwidthParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3c10-106">UnlimitedBandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3c10-106">UnlimitedBandwidthParameterSet</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3c10-107">설명</span><span class="sxs-lookup"><span data-stu-id="a3c10-107">DESCRIPTION</span></span>
<span data-ttu-id="a3c10-108">**New-AzDataBoxEdgeBandwidthSchedule** cmdlet은 대역폭 사용량을 관리하는 데 도움이 되는 Data Box Edge 디바이스에 대한 새 대역폭 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a3c10-108">The **New-AzDataBoxEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Data Box Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="a3c10-109">예제</span><span class="sxs-lookup"><span data-stu-id="a3c10-109">EXAMPLES</span></span>

### <span data-ttu-id="a3c10-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a3c10-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="a3c10-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="a3c10-111">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="a3c10-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3c10-112">PARAMETERS</span></span>

### <span data-ttu-id="a3c10-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3c10-113">-AsJob</span></span>
<span data-ttu-id="a3c10-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a3c10-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3c10-115">-Bandwidth</span><span class="sxs-lookup"><span data-stu-id="a3c10-115">-Bandwidth</span></span>
<span data-ttu-id="a3c10-116">대역폭(Mbps)</span><span class="sxs-lookup"><span data-stu-id="a3c10-116">Bandwidth in Mbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: BandwidthParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c10-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="a3c10-117">-DaysOfWeek</span></span>
<span data-ttu-id="a3c10-118">Scheduled DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="a3c10-118">Scheduled DaysOfWeek</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c10-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3c10-119">-DefaultProfile</span></span>
<span data-ttu-id="a3c10-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a3c10-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3c10-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a3c10-121">-DeviceName</span></span>
<span data-ttu-id="a3c10-122">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="a3c10-122">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c10-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a3c10-123">-Name</span></span>
<span data-ttu-id="a3c10-124">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="a3c10-124">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c10-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3c10-125">-ResourceGroupName</span></span>
<span data-ttu-id="a3c10-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="a3c10-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c10-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a3c10-127">-StartTime</span></span>
<span data-ttu-id="a3c10-128">시작 시간 예약</span><span class="sxs-lookup"><span data-stu-id="a3c10-128">Schedule Start Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c10-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="a3c10-129">-StopTime</span></span>
<span data-ttu-id="a3c10-130">일정 중지 시간</span><span class="sxs-lookup"><span data-stu-id="a3c10-130">Schedule Stop Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c10-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="a3c10-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="a3c10-132">무제한 대역폭을 설정합니다. false로 설정하면 기본값이 20Mbps로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3c10-132">Will Set Unlimited Bandwidth, if set to false will set default value as 20 Mbps</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UnlimitedBandwidthParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c10-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3c10-133">-Confirm</span></span>
<span data-ttu-id="a3c10-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3c10-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3c10-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3c10-135">-WhatIf</span></span>
<span data-ttu-id="a3c10-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a3c10-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3c10-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c10-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3c10-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3c10-138">CommonParameters</span></span>
<span data-ttu-id="a3c10-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c10-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3c10-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a3c10-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3c10-141">입력</span><span class="sxs-lookup"><span data-stu-id="a3c10-141">INPUTS</span></span>

### <span data-ttu-id="a3c10-142">없음</span><span class="sxs-lookup"><span data-stu-id="a3c10-142">None</span></span>

## <span data-ttu-id="a3c10-143">출력</span><span class="sxs-lookup"><span data-stu-id="a3c10-143">OUTPUTS</span></span>

### <span data-ttu-id="a3c10-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="a3c10-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="a3c10-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a3c10-145">NOTES</span></span>

## <span data-ttu-id="a3c10-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3c10-146">RELATED LINKS</span></span>
