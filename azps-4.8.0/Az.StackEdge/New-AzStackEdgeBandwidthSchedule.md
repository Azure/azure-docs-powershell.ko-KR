---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 27d1f77db385c04e50b67b9aa3a8d8d6bf921485
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204737"
---
# <span data-ttu-id="b4ec0-101">New-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="b4ec0-101">New-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="b4ec0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="b4ec0-103">새 대역폭 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b4ec0-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="b4ec0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b4ec0-104">SYNTAX</span></span>

### <span data-ttu-id="b4ec0-105">UnlimitedBandwidthParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b4ec0-105">UnlimitedBandwidthParameterSet (Default)</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4ec0-106">BandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4ec0-106">BandwidthParameterSet</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4ec0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b4ec0-107">DESCRIPTION</span></span>
<span data-ttu-id="b4ec0-108">**AzStackEdgeBandwidthSchedule** Cmdlet은 스택 경계 장치에 대 한 새 대역폭 일정을 만들어 대역폭 사용량을 관리 하는 데 도움을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b4ec0-108">The **New-AzStackEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Stack Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="b4ec0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b4ec0-109">EXAMPLES</span></span>

### <span data-ttu-id="b4ec0-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b4ec0-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="b4ec0-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="b4ec0-111">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="b4ec0-112">변수</span><span class="sxs-lookup"><span data-stu-id="b4ec0-112">PARAMETERS</span></span>

### <span data-ttu-id="b4ec0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4ec0-113">-AsJob</span></span>
<span data-ttu-id="b4ec0-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b4ec0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4ec0-115">-대역폭</span><span class="sxs-lookup"><span data-stu-id="b4ec0-115">-Bandwidth</span></span>
<span data-ttu-id="b4ec0-116">Mbps 단위 대역폭</span><span class="sxs-lookup"><span data-stu-id="b4ec0-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="b4ec0-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="b4ec0-117">-DaysOfWeek</span></span>
<span data-ttu-id="b4ec0-118">예정 된 DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="b4ec0-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="b4ec0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4ec0-119">-DefaultProfile</span></span>
<span data-ttu-id="b4ec0-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ec0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4ec0-121">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="b4ec0-121">-DeviceName</span></span>
<span data-ttu-id="b4ec0-122">장치 이름</span><span class="sxs-lookup"><span data-stu-id="b4ec0-122">Device Name</span></span>

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

### <span data-ttu-id="b4ec0-123">-이름</span><span class="sxs-lookup"><span data-stu-id="b4ec0-123">-Name</span></span>
<span data-ttu-id="b4ec0-124">자원 이름</span><span class="sxs-lookup"><span data-stu-id="b4ec0-124">Resource Name</span></span>

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

### <span data-ttu-id="b4ec0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4ec0-125">-ResourceGroupName</span></span>
<span data-ttu-id="b4ec0-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b4ec0-126">Resource Group Name</span></span>

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

### <span data-ttu-id="b4ec0-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b4ec0-127">-StartTime</span></span>
<span data-ttu-id="b4ec0-128">일정 시작 시간</span><span class="sxs-lookup"><span data-stu-id="b4ec0-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="b4ec0-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="b4ec0-129">-StopTime</span></span>
<span data-ttu-id="b4ec0-130">일정 중지 시간</span><span class="sxs-lookup"><span data-stu-id="b4ec0-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="b4ec0-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="b4ec0-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="b4ec0-132">대역폭을 무제한으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ec0-132">Will Set Bandwidth as Unlimited</span></span>

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

### <span data-ttu-id="b4ec0-133">-확인</span><span class="sxs-lookup"><span data-stu-id="b4ec0-133">-Confirm</span></span>
<span data-ttu-id="b4ec0-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ec0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4ec0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4ec0-135">-WhatIf</span></span>
<span data-ttu-id="b4ec0-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b4ec0-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4ec0-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4ec0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4ec0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4ec0-138">CommonParameters</span></span>
<span data-ttu-id="b4ec0-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ec0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4ec0-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b4ec0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4ec0-141">입력</span><span class="sxs-lookup"><span data-stu-id="b4ec0-141">INPUTS</span></span>

### <span data-ttu-id="b4ec0-142">않아야</span><span class="sxs-lookup"><span data-stu-id="b4ec0-142">None</span></span>

## <span data-ttu-id="b4ec0-143">출력</span><span class="sxs-lookup"><span data-stu-id="b4ec0-143">OUTPUTS</span></span>

### <span data-ttu-id="b4ec0-144">StackEdge. PSStackEdgeBandWidthSchedule에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="b4ec0-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="b4ec0-145">상속자</span><span class="sxs-lookup"><span data-stu-id="b4ec0-145">NOTES</span></span>

## <span data-ttu-id="b4ec0-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4ec0-146">RELATED LINKS</span></span>
