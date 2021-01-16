---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: e9f89a39b283f073c0fe826f22157570be29e74b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493324"
---
# <span data-ttu-id="c1121-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c1121-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="c1121-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1121-102">SYNOPSIS</span></span>
<span data-ttu-id="c1121-103">Backup 보호 정책을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="c1121-104">구문</span><span class="sxs-lookup"><span data-stu-id="c1121-104">SYNTAX</span></span>

### <span data-ttu-id="c1121-105">ModifyPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="c1121-105">ModifyPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1121-106">FixPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="c1121-106">FixPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-FixForInconsistentItems]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1121-107">설명</span><span class="sxs-lookup"><span data-stu-id="c1121-107">DESCRIPTION</span></span>
<span data-ttu-id="c1121-108">**Set-AzRecoveryServicesBackupProtectionPolicy** cmdlet은 기존 Azure Backup 보호 정책을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-108">The **Set-AzRecoveryServicesBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="c1121-109">Backup 일정 및 보존 정책 구성 요소를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-109">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="c1121-110">변경한 내용은 정책과 연결된 항목의 백업 및 보존에 영향을 미치게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-110">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="c1121-111">현재 cmdlet을 사용하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용하여 자격 증명 모음 컨텍스트를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="c1121-112">예제</span><span class="sxs-lookup"><span data-stu-id="c1121-112">EXAMPLES</span></span>

### <span data-ttu-id="c1121-113">예제 1: Backup 보호 정책 수정</span><span class="sxs-lookup"><span data-stu-id="c1121-113">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Time = Get-Date
PS C:\> $Time1 = Get-Date -Year $Time.Year -Month $Time.Month -Day $Time.Day -Hour $Time.Hour -Minute 0 -Second 0 -Millisecond 0
PS C:\> $Time1 = $Time1.ToUniversalTime()
PS C:\> $SchPol.ScheduleRunTimes.Add($Time1)
PS C:\> $SchPol.ScheduleRunFrequency.Clear
PS C:\> $SchPol.ScheduleRunDays.Add("Monday")
PS C:\> $SchPol.ScheduleRunFrequency="Weekly"
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.IsDailyScheduleEnabled=$false
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 0
PS C:\> $RetPol.IsWeeklyScheduleEnabled=$true 
PS C:\> $RetPol.WeeklySchedule.DaysOfTheWeek.Add("Monday")
PS C:\> $RetPol.WeeklySchedule.DurationCountInWeeks = 365
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "azurefiles" -Name "azurefilesvault"
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "TestPolicy" -VaultId $vault.ID
PS C:\> $Pol.SnapshotRetentionInDays=5
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="c1121-114">보호 정책을 수정하기 위해 따라야 하는 단계에 대한 개략적인 설명은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-114">Here is the high-level description of the steps to be followed for modifying a protection policy:</span></span> 
1.  <span data-ttu-id="c1121-115">기본 SchedulePolicyObject 및 기본 RetentionPolicyObject를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-115">Get a base SchedulePolicyObject and base RetentionPolicyObject.</span></span> <span data-ttu-id="c1121-116">일부 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-116">Store them in some variable.</span></span>
2.  <span data-ttu-id="c1121-117">요구 사항에 따라 일정 및 보존 정책 개체의 다른 매개 변수를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-117">Set the different parameters of schedule and retention policy object as per your requirement.</span></span> <span data-ttu-id="c1121-118">예를 들어 위의 샘플 스크립트에서는 주간 보호 정책을 설정하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-118">For example- In the above sample script, we are trying to set a weekly protection policy.</span></span> <span data-ttu-id="c1121-119">따라서 일정 빈도를 "매주"로 변경하고 일정 실행 시간도 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-119">Hence, we changed the schedule frequency to "Weekly" and also updated the schedule run time.</span></span> <span data-ttu-id="c1121-120">보존 정책 개체에서 주간 보존 기간을 업데이트하고 올바른 "주간 일정 사용" 플래그를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-120">In the retention policy object, we updated the weekly retention duration and set the correct "weekly schedule enabled" flag.</span></span> <span data-ttu-id="c1121-121">일일 정책을 설정하려는 경우 "일일 일정 사용" 플래그를 true로 설정하고 다른 개체 매개 변수에 적절한 값을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-121">In case you want to set a Daily policy, set the "daily schedule enabled" flag to true and assign appropriate values for other object parameters.</span></span>
3.  <span data-ttu-id="c1121-122">수정하려는 백업 보호 정책을 다운로드하고 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-122">Get the backup protection policy that you want to modify and store it in a variable.</span></span> <span data-ttu-id="c1121-123">위의 예제에서는 수정하려고 하는 "TestPolicy"라는 이름의 백업 정책을 검색했습니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-123">In the above example, we retrieved the backup policy with the name "TestPolicy" that we wanted to modify.</span></span>
4.  <span data-ttu-id="c1121-124">수정된 일정 정책 개체 및 보존 정책 개체를 사용하여 3단계에서 검색된 백업 보호 정책을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-124">Modify the backup protection policy retrieved in step 3 using the modified schedule policy object and retention policy object.</span></span>

## <span data-ttu-id="c1121-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1121-125">PARAMETERS</span></span>

### <span data-ttu-id="c1121-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1121-126">-DefaultProfile</span></span>
<span data-ttu-id="c1121-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1121-128">-FixForInconsistentItems</span><span class="sxs-lookup"><span data-stu-id="c1121-128">-FixForInconsistentItems</span></span>
<span data-ttu-id="c1121-129">실패한 항목에 대한 정책 업데이트를 다시 시도할지 여부를 나타내는 매개 변수를 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-129">Switch Parameter indicating whether or not to retry Policy Update for failed items.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FixPolicyParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1121-130">-Policy</span><span class="sxs-lookup"><span data-stu-id="c1121-130">-Policy</span></span>
<span data-ttu-id="c1121-131">이 cmdlet이 수정하는 Backup 보호 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-131">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="c1121-132">**BackupProtectionPolicy** 개체를 얻으면 Get-AzRecoveryServicesBackupProtectionPolicy cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-132">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1121-133">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c1121-133">-RetentionPolicy</span></span>
<span data-ttu-id="c1121-134">기본 보존 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-134">Specifies the base retention policy.</span></span>
<span data-ttu-id="c1121-135">**RetentionPolicy** 개체를 얻으면 Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-135">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: ModifyPolicyParamSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1121-136">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="c1121-136">-SchedulePolicy</span></span>
<span data-ttu-id="c1121-137">기본 일정 정책 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-137">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="c1121-138">**SchedulePolicy** 개체를 얻으면 Get-AzRecoveryServicesBackupSchedulePolicyObject 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-138">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: ModifyPolicyParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1121-139">-VaultId</span><span class="sxs-lookup"><span data-stu-id="c1121-139">-VaultId</span></span>
<span data-ttu-id="c1121-140">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-140">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1121-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1121-141">-Confirm</span></span>
<span data-ttu-id="c1121-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1121-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1121-143">-WhatIf</span></span>
<span data-ttu-id="c1121-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c1121-144">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="c1121-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1121-145">CommonParameters</span></span>
<span data-ttu-id="c1121-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c1121-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1121-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c1121-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1121-148">입력</span><span class="sxs-lookup"><span data-stu-id="c1121-148">INPUTS</span></span>

### <span data-ttu-id="c1121-149">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="c1121-149">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="c1121-150">System.String</span><span class="sxs-lookup"><span data-stu-id="c1121-150">System.String</span></span>

## <span data-ttu-id="c1121-151">출력</span><span class="sxs-lookup"><span data-stu-id="c1121-151">OUTPUTS</span></span>

### <span data-ttu-id="c1121-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="c1121-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="c1121-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c1121-153">NOTES</span></span>

## <span data-ttu-id="c1121-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1121-154">RELATED LINKS</span></span>

[<span data-ttu-id="c1121-155">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c1121-155">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="c1121-156">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="c1121-156">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="c1121-157">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c1121-157">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="c1121-158">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c1121-158">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


