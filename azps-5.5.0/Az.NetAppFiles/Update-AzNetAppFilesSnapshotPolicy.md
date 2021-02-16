---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: edb22cc9945ca665b2e24a4488bf3335faac4f50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194025"
---
# <span data-ttu-id="322c1-101">Update-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="322c1-101">Update-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="322c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="322c1-102">SYNOPSIS</span></span>
<span data-ttu-id="322c1-103">제공된 선택적 수정자에 ANF(Azure NetApp Files) 스냅숏 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="322c1-103">Updates an Azure NetApp Files (ANF) snapshot policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="322c1-104">구문</span><span class="sxs-lookup"><span data-stu-id="322c1-104">SYNTAX</span></span>

### <span data-ttu-id="322c1-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="322c1-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="322c1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="322c1-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled <Boolean>]
 [-HourlySchedule <PSNetAppFilesHourlySchedule>] [-DailySchedule <PSNetAppFilesDailySchedule>]
 [-WeeklySchedule <PSNetAppFilesWeeklySchedule>] [-MonthlySchedule <PSNetAppFilesMonthlySchedule>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="322c1-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="322c1-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="322c1-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="322c1-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesSnapshotPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="322c1-109">설명</span><span class="sxs-lookup"><span data-stu-id="322c1-109">DESCRIPTION</span></span>
<span data-ttu-id="322c1-110">**Update-AzNetAppFilesSnapshotPolicy** cmdlet은 ANF 스냅숏 정책을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="322c1-110">The **Update-AzNetAppFilesSnapshotPolicy** cmdlet modifies an ANF snapshot policy.</span></span>

## <span data-ttu-id="322c1-111">예제</span><span class="sxs-lookup"><span data-stu-id="322c1-111">EXAMPLES</span></span>

### <span data-ttu-id="322c1-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="322c1-112">Example 1</span></span>
```powershell
$hourlySchedule = @{
        Minute = 1
        SnapshotsToKeep = 3
    }
PS C:\> Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy" -HourlySchedule $hourlySchedule
```

<span data-ttu-id="322c1-113">이 명령은 ANF 백업 정책 "MySnapshotPolicy"를 지정한 HourlySchedule로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="322c1-113">This command changes the ANF backup policy "MySnapshotPolicy" to have the given HourlySchedule.</span></span>

## <span data-ttu-id="322c1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="322c1-114">PARAMETERS</span></span>

### <span data-ttu-id="322c1-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="322c1-115">-AccountName</span></span>
<span data-ttu-id="322c1-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="322c1-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="322c1-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="322c1-117">-AccountObject</span></span>
<span data-ttu-id="322c1-118">새 스냅숏 정책 개체의 계정</span><span class="sxs-lookup"><span data-stu-id="322c1-118">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="322c1-119">-DailySchedule</span><span class="sxs-lookup"><span data-stu-id="322c1-119">-DailySchedule</span></span>
<span data-ttu-id="322c1-120">일별 일정을 나타내는 해시테이블 배열</span><span class="sxs-lookup"><span data-stu-id="322c1-120">A hashtable array which represents the daily Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesDailySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="322c1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="322c1-121">-DefaultProfile</span></span>
<span data-ttu-id="322c1-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="322c1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="322c1-123">-Enabled</span><span class="sxs-lookup"><span data-stu-id="322c1-123">-Enabled</span></span>
<span data-ttu-id="322c1-124">정책을 사용할지 여부를 결정하는 속성</span><span class="sxs-lookup"><span data-stu-id="322c1-124">The property to decide policy is enabled or not</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="322c1-125">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="322c1-125">-HourlySchedule</span></span>
<span data-ttu-id="322c1-126">시간당 일정을 나타내는 해시테이블 배열</span><span class="sxs-lookup"><span data-stu-id="322c1-126">A hashtable array which represents the hourly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesHourlySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="322c1-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="322c1-127">-InputObject</span></span>
<span data-ttu-id="322c1-128">제거할 스냅숏 개체</span><span class="sxs-lookup"><span data-stu-id="322c1-128">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="322c1-129">-Location</span><span class="sxs-lookup"><span data-stu-id="322c1-129">-Location</span></span>
<span data-ttu-id="322c1-130">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="322c1-130">The location of the resource</span></span>

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

### <span data-ttu-id="322c1-131">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="322c1-131">-MonthlySchedule</span></span>
<span data-ttu-id="322c1-132">montly Schedule을 나타내는 해시테이블 배열</span><span class="sxs-lookup"><span data-stu-id="322c1-132">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesMonthlySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="322c1-133">-Name</span><span class="sxs-lookup"><span data-stu-id="322c1-133">-Name</span></span>
<span data-ttu-id="322c1-134">ANF 스냅숏 정책의 이름</span><span class="sxs-lookup"><span data-stu-id="322c1-134">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="322c1-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="322c1-135">-ResourceGroupName</span></span>
<span data-ttu-id="322c1-136">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="322c1-136">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="322c1-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="322c1-137">-ResourceId</span></span>
<span data-ttu-id="322c1-138">ANF 스냅숏 정책의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="322c1-138">The resource id of the ANF Snapshot Policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="322c1-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="322c1-139">-Tag</span></span>
<span data-ttu-id="322c1-140">리소스 태그를 나타내는 해시테이블 배열</span><span class="sxs-lookup"><span data-stu-id="322c1-140">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="322c1-141">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="322c1-141">-WeeklySchedule</span></span>
<span data-ttu-id="322c1-142">montly Schedule을 나타내는 해시테이블 배열</span><span class="sxs-lookup"><span data-stu-id="322c1-142">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesWeeklySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="322c1-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="322c1-143">-Confirm</span></span>
<span data-ttu-id="322c1-144">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="322c1-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="322c1-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="322c1-145">-WhatIf</span></span>
<span data-ttu-id="322c1-146">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="322c1-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="322c1-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="322c1-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="322c1-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="322c1-148">CommonParameters</span></span>
<span data-ttu-id="322c1-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="322c1-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="322c1-150">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="322c1-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="322c1-151">입력</span><span class="sxs-lookup"><span data-stu-id="322c1-151">INPUTS</span></span>

### <span data-ttu-id="322c1-152">System.String</span><span class="sxs-lookup"><span data-stu-id="322c1-152">System.String</span></span>

### <span data-ttu-id="322c1-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="322c1-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="322c1-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="322c1-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="322c1-155">출력</span><span class="sxs-lookup"><span data-stu-id="322c1-155">OUTPUTS</span></span>

### <span data-ttu-id="322c1-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="322c1-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="322c1-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="322c1-157">NOTES</span></span>

## <span data-ttu-id="322c1-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="322c1-158">RELATED LINKS</span></span>
