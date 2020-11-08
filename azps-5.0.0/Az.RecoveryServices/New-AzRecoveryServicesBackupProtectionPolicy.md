---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 0a60e3bd7f07f69687766b95eb3d56be3ef1d56f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226200"
---
# <span data-ttu-id="0be0e-101">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0be0e-101">New-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="0be0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0be0e-102">SYNOPSIS</span></span>
<span data-ttu-id="0be0e-103">백업 보호 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-103">Creates a Backup protection policy.</span></span>

## <span data-ttu-id="0be0e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0be0e-104">SYNTAX</span></span>

```
New-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0be0e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0be0e-105">DESCRIPTION</span></span>
<span data-ttu-id="0be0e-106">**AzRecoveryServicesBackupProtectionPolicy** cmdlet은 자격 증명 모음에 백업 보호 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-106">The **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="0be0e-107">보호 정책은 하나 이상의 보존 정책에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="0be0e-108">보존 정책은 복구 지점이 Azure Backup으로 유지 되는 기간을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>
<span data-ttu-id="0be0e-109">Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet을 사용 하 여 기본 보존 정책을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-109">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="0be0e-110">Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet을 사용 하 여 기본 일정 정책을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-110">And you can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="0be0e-111">**SchedulePolicy** 및 **보존 정책** 개체는 **새로운 AzRecoveryServicesBackupProtectionPolicy** cmdlet에 대 한 입력으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="0be0e-112">현재 cmdlet을 사용 하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="0be0e-113">예제의</span><span class="sxs-lookup"><span data-stu-id="0be0e-113">EXAMPLES</span></span>

### <span data-ttu-id="0be0e-114">예제 1: 백업 보호 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="0be0e-114">Example 1: Create a Backup protection policy</span></span>
```powershell
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="0be0e-115">첫 번째 명령은 기본 **SchedulePolicyObject** 를 가져온 다음이를 $SchPol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-115">The first command gets a base **SchedulePolicyObject** , and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="0be0e-116">두 번째 명령은 $SchPol의 일정 정책에서 예약 된 모든 실행 시간을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="0be0e-117">세 번째 명령은 Get-Date cmdlet을 사용 하 여 현재 날짜와 시간을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>
<span data-ttu-id="0be0e-118">네 번째 명령은 예약 된 실행 시간에 $Dt의 현재 날짜 및 시간을 일정 정책에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>
<span data-ttu-id="0be0e-119">다섯 번째 명령은 기본 **보존 정책** 개체를 가져온 다음 $RetPol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="0be0e-120">여섯 번째 명령은 보존 기간 정책을 365 days로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-120">The sixth command sets the retention duration policy to 365 days.</span></span>
<span data-ttu-id="0be0e-121">마지막 명령은 이전 명령으로 만든 일정 및 보존 정책에 따라 **BackupProtectionPolicy** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

### <span data-ttu-id="0be0e-122">예제 2</span><span class="sxs-lookup"><span data-stu-id="0be0e-122">Example 2</span></span>

<span data-ttu-id="0be0e-123">백업 보호 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-123">Creates a Backup protection policy.</span></span> <span data-ttu-id="0be0e-124">생성</span><span class="sxs-lookup"><span data-stu-id="0be0e-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzRecoveryServicesBackupProtectionPolicy -Name 'NewPolicy' -RetentionPolicy $RetPol -SchedulePolicy $SchPol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="0be0e-125">변수</span><span class="sxs-lookup"><span data-stu-id="0be0e-125">PARAMETERS</span></span>

### <span data-ttu-id="0be0e-126">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="0be0e-126">-BackupManagementType</span></span>
<span data-ttu-id="0be0e-127">보호 되는 리소스의 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-127">The class of resources being protected.</span></span> <span data-ttu-id="0be0e-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0be0e-129">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="0be0e-129">AzureVM</span></span> 
- <span data-ttu-id="0be0e-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="0be0e-130">AzureStorage</span></span>
- <span data-ttu-id="0be0e-131">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="0be0e-131">AzureWorkload</span></span>

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

### <span data-ttu-id="0be0e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0be0e-132">-DefaultProfile</span></span>
<span data-ttu-id="0be0e-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0be0e-134">-이름</span><span class="sxs-lookup"><span data-stu-id="0be0e-134">-Name</span></span>
<span data-ttu-id="0be0e-135">정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-135">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="0be0e-136">-보존 정책</span><span class="sxs-lookup"><span data-stu-id="0be0e-136">-RetentionPolicy</span></span>
<span data-ttu-id="0be0e-137">기본 **보존 정책** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-137">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="0be0e-138">Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet을 사용 하 여 **보존 정책** 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-138">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

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

### <span data-ttu-id="0be0e-139">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="0be0e-139">-SchedulePolicy</span></span>
<span data-ttu-id="0be0e-140">기본 **SchedulePolicy** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-140">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="0be0e-141">Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet을 사용 하 여 **SchedulePolicy** 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-141">You can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

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

### <span data-ttu-id="0be0e-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0be0e-142">-VaultId</span></span>
<span data-ttu-id="0be0e-143">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0be0e-144">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="0be0e-144">-WorkloadType</span></span>
<span data-ttu-id="0be0e-145">리소스의 작업 부하 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-145">Workload type of the resource.</span></span> <span data-ttu-id="0be0e-146">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0be0e-147">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="0be0e-147">AzureVM</span></span> 
- <span data-ttu-id="0be0e-148">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="0be0e-148">AzureFiles</span></span>
- <span data-ttu-id="0be0e-149">원인은</span><span class="sxs-lookup"><span data-stu-id="0be0e-149">MSSQL</span></span>

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

### <span data-ttu-id="0be0e-150">-확인</span><span class="sxs-lookup"><span data-stu-id="0be0e-150">-Confirm</span></span>
<span data-ttu-id="0be0e-151">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0be0e-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0be0e-152">-WhatIf</span></span>
<span data-ttu-id="0be0e-153">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-153">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="0be0e-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0be0e-154">CommonParameters</span></span>
<span data-ttu-id="0be0e-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0be0e-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0be0e-156">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0be0e-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0be0e-157">입력</span><span class="sxs-lookup"><span data-stu-id="0be0e-157">INPUTS</span></span>

### <span data-ttu-id="0be0e-158">WorkloadType에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="0be0e-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span></span>

### <span data-ttu-id="0be0e-159">시스템 Null 허용 ' 1 [[Microsoft Azure. e-유틸리티]. system.webserver 관리 형식, Microsoft Azure. PowerShell, 버전 = 1.0.0.0, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="0be0e-159">System.Nullable\`1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0be0e-160">Microsoft Azure.. i 0. a 0 유틸리티.</span><span class="sxs-lookup"><span data-stu-id="0be0e-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

### <span data-ttu-id="0be0e-161">SchedulePolicyBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="0be0e-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

### <span data-ttu-id="0be0e-162">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0be0e-162">System.String</span></span>

## <span data-ttu-id="0be0e-163">출력</span><span class="sxs-lookup"><span data-stu-id="0be0e-163">OUTPUTS</span></span>

### <span data-ttu-id="0be0e-164">Microsoft. \*. i i m.. i i m.</span><span class="sxs-lookup"><span data-stu-id="0be0e-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="0be0e-165">상속자</span><span class="sxs-lookup"><span data-stu-id="0be0e-165">NOTES</span></span>

## <span data-ttu-id="0be0e-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0be0e-166">RELATED LINKS</span></span>

[<span data-ttu-id="0be0e-167">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="0be0e-167">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="0be0e-168">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0be0e-168">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="0be0e-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="0be0e-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="0be0e-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="0be0e-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="0be0e-171">제거-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0be0e-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="0be0e-172">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0be0e-172">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


