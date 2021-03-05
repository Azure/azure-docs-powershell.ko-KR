---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: 1f8b68ac04a563dbec44b0ed43bca0a54015154d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968432"
---
# <span data-ttu-id="af960-101">New-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="af960-101">New-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="af960-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af960-102">SYNOPSIS</span></span>
<span data-ttu-id="af960-103">ANF 계정에 대한 ANF(새 Azure NetApp Files) 스냅숏 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="af960-103">Creates a new Azure NetApp Files (ANF) snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="af960-104">구문</span><span class="sxs-lookup"><span data-stu-id="af960-104">SYNTAX</span></span>

### <span data-ttu-id="af960-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="af960-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af960-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af960-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af960-107">설명</span><span class="sxs-lookup"><span data-stu-id="af960-107">DESCRIPTION</span></span>
<span data-ttu-id="af960-108">**New-AzNetAppFilesActiveDirectory** cmdlet은 ANF 계정에 대한 새 스냅숏 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="af960-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="af960-109">예제</span><span class="sxs-lookup"><span data-stu-id="af960-109">EXAMPLES</span></span>

### <span data-ttu-id="af960-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="af960-110">Example 1</span></span>
```powershell
$hourlySchedule = @{        
        Minute = 2
        SnapshotsToKeep = 6
    }
    $dailySchedule = @{
        Hour = 1
        Minute = 2
        SnapshotsToKeep = 6
    }
    $weeklySchedule = @{
        Minute = 2    
        Hour = 1                
        Day = "Sunday,Monday"
        SnapshotsToKeep = 6
    }
    $monthlySchedule = @{
        Minute = 2    
        Hour = 1        
        DaysOfMonth = "2,11,21"
        SnapshotsToKeep = 6
    }
PS C:\> New-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MySnapshotPolicy" -Enabled -HourlySchedule $hourlySchedule -DailySchedule $dailySchedule -WeeklySchedule $weeklySchedule -MonthlySchedule $monthlySchedule
```

<span data-ttu-id="af960-111">이 명령은 "MyAccount"라는 ANF 계정에 대한 새 ANF 스냅숏 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="af960-111">This command creates the new ANF snapshot policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="af960-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="af960-112">PARAMETERS</span></span>

### <span data-ttu-id="af960-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="af960-113">-AccountName</span></span>
<span data-ttu-id="af960-114">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="af960-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af960-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="af960-115">-AccountObject</span></span>
<span data-ttu-id="af960-116">새 스냅숏 정책 개체에 대한 계정</span><span class="sxs-lookup"><span data-stu-id="af960-116">The Account for the new Snapshot Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af960-117">-DailySchedule</span><span class="sxs-lookup"><span data-stu-id="af960-117">-DailySchedule</span></span>
<span data-ttu-id="af960-118">일별 일정을 나타내는 해시테이블 배열</span><span class="sxs-lookup"><span data-stu-id="af960-118">A hashtable array which represents the daily Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesDailySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af960-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af960-119">-DefaultProfile</span></span>
<span data-ttu-id="af960-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="af960-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af960-121">-사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="af960-121">-Enabled</span></span>
<span data-ttu-id="af960-122">정책을 사용할지 여부를 결정하는 속성</span><span class="sxs-lookup"><span data-stu-id="af960-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="af960-123">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="af960-123">-HourlySchedule</span></span>
<span data-ttu-id="af960-124">시간당 일정을 나타내는 해시테이블 배열</span><span class="sxs-lookup"><span data-stu-id="af960-124">A hashtable array which represents the hourly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesHourlySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af960-125">-Location</span><span class="sxs-lookup"><span data-stu-id="af960-125">-Location</span></span>
<span data-ttu-id="af960-126">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="af960-126">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af960-127">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="af960-127">-MonthlySchedule</span></span>
<span data-ttu-id="af960-128">몽블리 일정을 나타내는 해시테이블 배열</span><span class="sxs-lookup"><span data-stu-id="af960-128">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesMonthlySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af960-129">-Name</span><span class="sxs-lookup"><span data-stu-id="af960-129">-Name</span></span>
<span data-ttu-id="af960-130">ANF 스냅숏 정책의 이름</span><span class="sxs-lookup"><span data-stu-id="af960-130">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af960-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af960-131">-ResourceGroupName</span></span>
<span data-ttu-id="af960-132">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="af960-132">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af960-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="af960-133">-Tag</span></span>
<span data-ttu-id="af960-134">리소스 태그를 나타내는 해시테이블 배열</span><span class="sxs-lookup"><span data-stu-id="af960-134">A hashtable array which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af960-135">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="af960-135">-WeeklySchedule</span></span>
<span data-ttu-id="af960-136">몽블리 일정을 나타내는 해시테이블 배열</span><span class="sxs-lookup"><span data-stu-id="af960-136">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesWeeklySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af960-137">-확인</span><span class="sxs-lookup"><span data-stu-id="af960-137">-Confirm</span></span>
<span data-ttu-id="af960-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="af960-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af960-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af960-139">-WhatIf</span></span>
<span data-ttu-id="af960-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="af960-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af960-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af960-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af960-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af960-142">CommonParameters</span></span>
<span data-ttu-id="af960-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="af960-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af960-144">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af960-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af960-145">입력</span><span class="sxs-lookup"><span data-stu-id="af960-145">INPUTS</span></span>

### <span data-ttu-id="af960-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="af960-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="af960-147">출력</span><span class="sxs-lookup"><span data-stu-id="af960-147">OUTPUTS</span></span>

### <span data-ttu-id="af960-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="af960-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="af960-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="af960-149">NOTES</span></span>

## <span data-ttu-id="af960-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af960-150">RELATED LINKS</span></span>
