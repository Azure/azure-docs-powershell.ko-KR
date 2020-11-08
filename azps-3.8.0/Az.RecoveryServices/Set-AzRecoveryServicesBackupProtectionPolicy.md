---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 16bb97fdfab6d890f67bef209acaa584b5a67487
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043522"
---
# <span data-ttu-id="33234-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="33234-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="33234-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33234-102">SYNOPSIS</span></span>
<span data-ttu-id="33234-103">백업 보호 정책을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33234-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="33234-104">구문과</span><span class="sxs-lookup"><span data-stu-id="33234-104">SYNTAX</span></span>

### <span data-ttu-id="33234-105">ModifyPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="33234-105">ModifyPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33234-106">FixPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="33234-106">FixPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-FixForInconsistentItems]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33234-107">설명은</span><span class="sxs-lookup"><span data-stu-id="33234-107">DESCRIPTION</span></span>
<span data-ttu-id="33234-108">**Set-AzBackupProtectionPolicy** cmdlet은 기존 Azure Backup 보호 정책을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33234-108">The **Set-AzBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="33234-109">백업 일정 및 보존 정책 구성 요소를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33234-109">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="33234-110">변경 사항은 정책과 관련 된 항목의 백업 및 보존에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="33234-110">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="33234-111">현재 cmdlet을 사용 하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33234-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="33234-112">예제의</span><span class="sxs-lookup"><span data-stu-id="33234-112">EXAMPLES</span></span>

### <span data-ttu-id="33234-113">예제 1: 백업 보호 정책 수정</span><span class="sxs-lookup"><span data-stu-id="33234-113">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> $Pol.AzureBackupRGName = "RG_prefix"
PS C:\> $Pol.AzureBackupRGNameSuffix = "RG_suffix"
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="33234-114">첫 번째 명령은 기본 SchedulePolicy 개체를 가져온 다음이를 $SchPol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="33234-114">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="33234-115">두 번째 명령은 $SchPol의 일정 정책에서 예약 된 모든 실행 시간을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33234-115">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="33234-116">세 번째 명령은 Get-Date cmdlet을 사용 하 여 현재 날짜와 시간을 얻은 다음 $DT 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="33234-116">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="33234-117">네 번째 명령은 일정 정책에 대 한 일정 실행 시간에 $DT 날짜와 시간을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="33234-117">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>
<span data-ttu-id="33234-118">다섯 번째 명령은 기본 보존 정책 개체를 가져온 다음 $RetPol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="33234-118">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="33234-119">여섯 번째 명령은 보존 기간을 365 일로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33234-119">The sixth command sets the retention duration to 365 days.</span></span>
<span data-ttu-id="33234-120">일곱째 명령에서는 NewPolicy 라는 백업 보호 정책을 가져온 다음 $Pol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="33234-120">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="33234-121">여덟 번째 및 9 번째는 복원 지점을 저장 하는 정책과 연결 된 리소스 그룹 매개 변수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33234-121">The eighth and ninth sets the resource group parameters associated with policy which stores the restore points.</span></span>
<span data-ttu-id="33234-122">마지막 명령은 $SchPol의 일정 정책과 $RetPol의 보존 정책을 사용 하 여 $Pol의 백업 보호 정책을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33234-122">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="33234-123">변수</span><span class="sxs-lookup"><span data-stu-id="33234-123">PARAMETERS</span></span>

### <span data-ttu-id="33234-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33234-124">-DefaultProfile</span></span>
<span data-ttu-id="33234-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33234-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33234-126">-FixForInconsistentItems</span><span class="sxs-lookup"><span data-stu-id="33234-126">-FixForInconsistentItems</span></span>
<span data-ttu-id="33234-127">실패 한 항목에 대 한 정책 업데이트 재시도 여부를 나타내는 Switch 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="33234-127">Switch Parameter indicating whether or not to retry Policy Update for failed items.</span></span>

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

### <span data-ttu-id="33234-128">-정책</span><span class="sxs-lookup"><span data-stu-id="33234-128">-Policy</span></span>
<span data-ttu-id="33234-129">이 cmdlet이 수정 하는 백업 보호 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33234-129">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="33234-130">**BackupProtectionPolicy** 개체를 가져오려면 Get-AzRecoveryServicesBackupProtectionPolicy cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="33234-130">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="33234-131">-보존 정책</span><span class="sxs-lookup"><span data-stu-id="33234-131">-RetentionPolicy</span></span>
<span data-ttu-id="33234-132">기본 보존 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33234-132">Specifies the base retention policy.</span></span>
<span data-ttu-id="33234-133">**보존 정책** 개체를 얻으려면 Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="33234-133">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

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

### <span data-ttu-id="33234-134">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="33234-134">-SchedulePolicy</span></span>
<span data-ttu-id="33234-135">기본 일정 정책 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33234-135">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="33234-136">**SchedulePolicy** 개체를 가져오려면 Get-AzRecoveryServicesBackupSchedulePolicyObject 개체를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="33234-136">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

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

### <span data-ttu-id="33234-137">-VaultId</span><span class="sxs-lookup"><span data-stu-id="33234-137">-VaultId</span></span>
<span data-ttu-id="33234-138">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="33234-138">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="33234-139">-확인</span><span class="sxs-lookup"><span data-stu-id="33234-139">-Confirm</span></span>
<span data-ttu-id="33234-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="33234-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33234-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33234-141">-WhatIf</span></span>
<span data-ttu-id="33234-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="33234-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33234-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33234-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33234-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33234-144">CommonParameters</span></span>
<span data-ttu-id="33234-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="33234-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33234-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="33234-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33234-147">입력</span><span class="sxs-lookup"><span data-stu-id="33234-147">INPUTS</span></span>

### <span data-ttu-id="33234-148">Microsoft. \*. i i m.. i i m.</span><span class="sxs-lookup"><span data-stu-id="33234-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="33234-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="33234-149">System.String</span></span>

## <span data-ttu-id="33234-150">출력</span><span class="sxs-lookup"><span data-stu-id="33234-150">OUTPUTS</span></span>

### <span data-ttu-id="33234-151">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="33234-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="33234-152">상속자</span><span class="sxs-lookup"><span data-stu-id="33234-152">NOTES</span></span>

## <span data-ttu-id="33234-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33234-153">RELATED LINKS</span></span>

[<span data-ttu-id="33234-154">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="33234-154">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="33234-155">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="33234-155">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="33234-156">새로운 AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="33234-156">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="33234-157">제거-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="33234-157">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


