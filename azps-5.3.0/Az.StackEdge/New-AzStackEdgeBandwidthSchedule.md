---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 27d1f77db385c04e50b67b9aa3a8d8d6bf921485
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374417"
---
# <span data-ttu-id="ffa12-101">New-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="ffa12-101">New-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="ffa12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffa12-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa12-103">새 대역폭 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ffa12-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="ffa12-104">구문</span><span class="sxs-lookup"><span data-stu-id="ffa12-104">SYNTAX</span></span>

### <span data-ttu-id="ffa12-105">UnlimitedBandwidthParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ffa12-105">UnlimitedBandwidthParameterSet (Default)</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffa12-106">BandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffa12-106">BandwidthParameterSet</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffa12-107">설명</span><span class="sxs-lookup"><span data-stu-id="ffa12-107">DESCRIPTION</span></span>
<span data-ttu-id="ffa12-108">**New-AzStackEdgeBandwidthSchedule** cmdlet은 대역폭 사용량을 관리하는 데 도움이 되는 Stack Edge 디바이스에 대한 새 대역폭 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ffa12-108">The **New-AzStackEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Stack Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="ffa12-109">예제</span><span class="sxs-lookup"><span data-stu-id="ffa12-109">EXAMPLES</span></span>

### <span data-ttu-id="ffa12-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ffa12-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="ffa12-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="ffa12-111">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="ffa12-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffa12-112">PARAMETERS</span></span>

### <span data-ttu-id="ffa12-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ffa12-113">-AsJob</span></span>
<span data-ttu-id="ffa12-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ffa12-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ffa12-115">-Bandwidth</span><span class="sxs-lookup"><span data-stu-id="ffa12-115">-Bandwidth</span></span>
<span data-ttu-id="ffa12-116">대역폭(Mbps)</span><span class="sxs-lookup"><span data-stu-id="ffa12-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="ffa12-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="ffa12-117">-DaysOfWeek</span></span>
<span data-ttu-id="ffa12-118">Scheduled DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="ffa12-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="ffa12-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffa12-119">-DefaultProfile</span></span>
<span data-ttu-id="ffa12-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ffa12-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffa12-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ffa12-121">-DeviceName</span></span>
<span data-ttu-id="ffa12-122">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="ffa12-122">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa12-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ffa12-123">-Name</span></span>
<span data-ttu-id="ffa12-124">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="ffa12-124">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa12-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffa12-125">-ResourceGroupName</span></span>
<span data-ttu-id="ffa12-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ffa12-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa12-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ffa12-127">-StartTime</span></span>
<span data-ttu-id="ffa12-128">시작 시간 예약</span><span class="sxs-lookup"><span data-stu-id="ffa12-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="ffa12-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="ffa12-129">-StopTime</span></span>
<span data-ttu-id="ffa12-130">일정 중지 시간</span><span class="sxs-lookup"><span data-stu-id="ffa12-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="ffa12-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="ffa12-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="ffa12-132">대역폭을 무제한으로 설정</span><span class="sxs-lookup"><span data-stu-id="ffa12-132">Will Set Bandwidth as Unlimited</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UnlimitedBandwidthParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa12-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffa12-133">-Confirm</span></span>
<span data-ttu-id="ffa12-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffa12-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffa12-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffa12-135">-WhatIf</span></span>
<span data-ttu-id="ffa12-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ffa12-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ffa12-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffa12-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffa12-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa12-138">CommonParameters</span></span>
<span data-ttu-id="ffa12-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ffa12-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa12-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ffa12-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa12-141">입력</span><span class="sxs-lookup"><span data-stu-id="ffa12-141">INPUTS</span></span>

### <span data-ttu-id="ffa12-142">없음</span><span class="sxs-lookup"><span data-stu-id="ffa12-142">None</span></span>

## <span data-ttu-id="ffa12-143">출력</span><span class="sxs-lookup"><span data-stu-id="ffa12-143">OUTPUTS</span></span>

### <span data-ttu-id="ffa12-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="ffa12-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="ffa12-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ffa12-145">NOTES</span></span>

## <span data-ttu-id="ffa12-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ffa12-146">RELATED LINKS</span></span>
