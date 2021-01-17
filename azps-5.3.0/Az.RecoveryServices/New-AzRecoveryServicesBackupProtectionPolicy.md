---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 0a60e3bd7f07f69687766b95eb3d56be3ef1d56f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492442"
---
# <span data-ttu-id="d2f4c-101">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d2f4c-101">New-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="d2f4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2f4c-102">SYNOPSIS</span></span>
<span data-ttu-id="d2f4c-103">Backup 보호 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-103">Creates a Backup protection policy.</span></span>

## <span data-ttu-id="d2f4c-104">구문</span><span class="sxs-lookup"><span data-stu-id="d2f4c-104">SYNTAX</span></span>

```
New-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2f4c-105">설명</span><span class="sxs-lookup"><span data-stu-id="d2f4c-105">DESCRIPTION</span></span>
<span data-ttu-id="d2f4c-106">**New-AzRecoveryServicesBackupProtectionPolicy** cmdlet은 자격 증명 모음에 Backup 보호 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-106">The **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="d2f4c-107">보호 정책은 하나 이상의 보존 정책과 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="d2f4c-108">보존 정책은 Azure Backup을 사용하여 복구 지점을 보관하는 기간을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>
<span data-ttu-id="d2f4c-109">기본 보존 정책을 Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-109">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="d2f4c-110">또한 기본 일정 정책을 Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-110">And you can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="d2f4c-111">**SchedulePolicy** 및 **RetentionPolicy** 개체는 **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet에 대한 입력으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="d2f4c-112">현재 cmdlet을 사용하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용하여 자격 증명 모음 컨텍스트를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d2f4c-113">예제</span><span class="sxs-lookup"><span data-stu-id="d2f4c-113">EXAMPLES</span></span>

### <span data-ttu-id="d2f4c-114">예제 1: Backup 보호 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="d2f4c-114">Example 1: Create a Backup protection policy</span></span>
```powershell
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="d2f4c-115">첫 번째 명령은 **기본 SchedulePolicyObject를** 얻은 다음, $SchPol 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-115">The first command gets a base **SchedulePolicyObject**, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="d2f4c-116">두 번째 명령은 일정 정책에서 예약된 모든 실행 시간을 $SchPol.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="d2f4c-117">세 번째 명령은 Get-Date cmdlet을 사용하여 현재 날짜 및 시간을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>
<span data-ttu-id="d2f4c-118">네 번째 명령은 예약된 실행 시간으로 $Dt 시간의 현재 날짜 및 시간을 일정 정책에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>
<span data-ttu-id="d2f4c-119">다섯 번째 명령은 기본 **RetentionPolicy** 개체를 구한 다음, $RetPol 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="d2f4c-120">여섯 번째 명령은 보존 기간 정책을 365일로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-120">The sixth command sets the retention duration policy to 365 days.</span></span>
<span data-ttu-id="d2f4c-121">마지막 명령은 이전 명령에서 만든 일정 및 보존 정책에 따라 **BackupProtectionPolicy** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

### <span data-ttu-id="d2f4c-122">예제 2</span><span class="sxs-lookup"><span data-stu-id="d2f4c-122">Example 2</span></span>

<span data-ttu-id="d2f4c-123">Backup 보호 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-123">Creates a Backup protection policy.</span></span> <span data-ttu-id="d2f4c-124">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="d2f4c-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzRecoveryServicesBackupProtectionPolicy -Name 'NewPolicy' -RetentionPolicy $RetPol -SchedulePolicy $SchPol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="d2f4c-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2f4c-125">PARAMETERS</span></span>

### <span data-ttu-id="d2f4c-126">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="d2f4c-126">-BackupManagementType</span></span>
<span data-ttu-id="d2f4c-127">보호되는 리소스의 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-127">The class of resources being protected.</span></span> <span data-ttu-id="d2f4c-128">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="d2f4c-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d2f4c-129">AzureVM</span><span class="sxs-lookup"><span data-stu-id="d2f4c-129">AzureVM</span></span> 
- <span data-ttu-id="d2f4c-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="d2f4c-130">AzureStorage</span></span>
- <span data-ttu-id="d2f4c-131">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="d2f4c-131">AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2f4c-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2f4c-132">-DefaultProfile</span></span>
<span data-ttu-id="d2f4c-133">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2f4c-134">-Name</span><span class="sxs-lookup"><span data-stu-id="d2f4c-134">-Name</span></span>
<span data-ttu-id="d2f4c-135">정책의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-135">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="d2f4c-136">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d2f4c-136">-RetentionPolicy</span></span>
<span data-ttu-id="d2f4c-137">기본 **RetentionPolicy 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="d2f4c-137">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="d2f4c-138">Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet을 사용하여 **RetentionPolicy** 개체를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-138">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2f4c-139">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="d2f4c-139">-SchedulePolicy</span></span>
<span data-ttu-id="d2f4c-140">기본 **SchedulePolicy 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="d2f4c-140">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="d2f4c-141">Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet을 사용하여 **SchedulePolicy 개체를 얻을 수** 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-141">You can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2f4c-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d2f4c-142">-VaultId</span></span>
<span data-ttu-id="d2f4c-143">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d2f4c-144">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="d2f4c-144">-WorkloadType</span></span>
<span data-ttu-id="d2f4c-145">리소스의 워크로드 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-145">Workload type of the resource.</span></span> <span data-ttu-id="d2f4c-146">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="d2f4c-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d2f4c-147">AzureVM</span><span class="sxs-lookup"><span data-stu-id="d2f4c-147">AzureVM</span></span> 
- <span data-ttu-id="d2f4c-148">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="d2f4c-148">AzureFiles</span></span>
- <span data-ttu-id="d2f4c-149">MSSQL</span><span class="sxs-lookup"><span data-stu-id="d2f4c-149">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2f4c-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2f4c-150">-Confirm</span></span>
<span data-ttu-id="d2f4c-151">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2f4c-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2f4c-152">-WhatIf</span></span>
<span data-ttu-id="d2f4c-153">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d2f4c-153">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="d2f4c-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2f4c-154">CommonParameters</span></span>
<span data-ttu-id="d2f4c-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2f4c-156">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d2f4c-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2f4c-157">입력</span><span class="sxs-lookup"><span data-stu-id="d2f4c-157">INPUTS</span></span>

### <span data-ttu-id="d2f4c-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span><span class="sxs-lookup"><span data-stu-id="d2f4c-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span></span>

### <span data-ttu-id="d2f4c-159">System.Nullable'1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="d2f4c-159">System.Nullable\`1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d2f4c-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="d2f4c-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

### <span data-ttu-id="d2f4c-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="d2f4c-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

### <span data-ttu-id="d2f4c-162">System.String</span><span class="sxs-lookup"><span data-stu-id="d2f4c-162">System.String</span></span>

## <span data-ttu-id="d2f4c-163">출력</span><span class="sxs-lookup"><span data-stu-id="d2f4c-163">OUTPUTS</span></span>

### <span data-ttu-id="d2f4c-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="d2f4c-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="d2f4c-165">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d2f4c-165">NOTES</span></span>

## <span data-ttu-id="d2f4c-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2f4c-166">RELATED LINKS</span></span>

[<span data-ttu-id="d2f4c-167">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="d2f4c-167">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="d2f4c-168">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d2f4c-168">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="d2f4c-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="d2f4c-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="d2f4c-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="d2f4c-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="d2f4c-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d2f4c-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="d2f4c-172">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d2f4c-172">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


