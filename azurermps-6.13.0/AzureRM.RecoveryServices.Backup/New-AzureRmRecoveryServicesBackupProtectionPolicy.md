---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/new-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 1a9eb2ef731e7ce555fbac1a08cd8468de83ebc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534211"
---
# <span data-ttu-id="d1af1-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d1af1-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="d1af1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1af1-102">SYNOPSIS</span></span>
<span data-ttu-id="d1af1-103">백업 보호 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-103">Creates a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1af1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d1af1-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1af1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d1af1-105">DESCRIPTION</span></span>
<span data-ttu-id="d1af1-106">**AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet은 자격 증명 모음에 백업 보호 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-106">The **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="d1af1-107">보호 정책은 하나 이상의 보존 정책에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="d1af1-108">보존 정책은 복구 지점이 Azure Backup으로 유지 되는 기간을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>
<span data-ttu-id="d1af1-109">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet을 사용 하 여 기본 보존 정책을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-109">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="d1af1-110">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet을 사용 하 여 기본 일정 정책을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-110">And you can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="d1af1-111">**SchedulePolicy** 및 **보존 정책** 개체는 **새로운 AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet에 대 한 입력으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="d1af1-112">현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d1af1-113">예제의</span><span class="sxs-lookup"><span data-stu-id="d1af1-113">EXAMPLES</span></span>

### <span data-ttu-id="d1af1-114">예제 1: 백업 보호 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="d1af1-114">Example 1: Create a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="d1af1-115">첫 번째 명령은 기본 **SchedulePolicyObject** 를 가져온 다음이를 $SchPol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-115">The first command gets a base **SchedulePolicyObject** , and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="d1af1-116">두 번째 명령은 $SchPol의 일정 정책에서 예약 된 모든 실행 시간을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="d1af1-117">세 번째 명령은 Get-Date cmdlet을 사용 하 여 현재 날짜와 시간을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>
<span data-ttu-id="d1af1-118">네 번째 명령은 예약 된 실행 시간에 $Dt의 현재 날짜 및 시간을 일정 정책에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>
<span data-ttu-id="d1af1-119">다섯 번째 명령은 기본 **보존 정책** 개체를 가져온 다음 $RetPol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="d1af1-120">여섯 번째 명령은 보존 기간 정책을 365 days로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-120">The sixth command sets the retention duration policy to 365 days.</span></span>
<span data-ttu-id="d1af1-121">마지막 명령은 이전 명령으로 만든 일정 및 보존 정책에 따라 **BackupProtectionPolicy** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

## <span data-ttu-id="d1af1-122">변수</span><span class="sxs-lookup"><span data-stu-id="d1af1-122">PARAMETERS</span></span>

### <span data-ttu-id="d1af1-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="d1af1-123">-BackupManagementType</span></span>
<span data-ttu-id="d1af1-124">백업 관리 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="d1af1-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d1af1-126">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="d1af1-126">AzureVM</span></span> 
- <span data-ttu-id="d1af1-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="d1af1-127">AzureSQLDatabase</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1af1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1af1-128">-DefaultProfile</span></span>
<span data-ttu-id="d1af1-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1af1-130">-이름</span><span class="sxs-lookup"><span data-stu-id="d1af1-130">-Name</span></span>
<span data-ttu-id="d1af1-131">정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-131">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="d1af1-132">-보존 정책</span><span class="sxs-lookup"><span data-stu-id="d1af1-132">-RetentionPolicy</span></span>
<span data-ttu-id="d1af1-133">기본 **보존 정책** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-133">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="d1af1-134">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet을 사용 하 여 **보존 정책** 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-134">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

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

### <span data-ttu-id="d1af1-135">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="d1af1-135">-SchedulePolicy</span></span>
<span data-ttu-id="d1af1-136">기본 **SchedulePolicy** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-136">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="d1af1-137">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet을 사용 하 여 **SchedulePolicy** 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-137">You can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

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

### <span data-ttu-id="d1af1-138">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d1af1-138">-VaultId</span></span>
<span data-ttu-id="d1af1-139">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-139">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d1af1-140">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="d1af1-140">-WorkloadType</span></span>
<span data-ttu-id="d1af1-141">작업 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-141">Specifies the workload type.</span></span>
<span data-ttu-id="d1af1-142">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d1af1-143">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="d1af1-143">AzureVM</span></span> 
- <span data-ttu-id="d1af1-144">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="d1af1-144">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1af1-145">-확인</span><span class="sxs-lookup"><span data-stu-id="d1af1-145">-Confirm</span></span>
<span data-ttu-id="d1af1-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1af1-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1af1-147">-WhatIf</span></span>
<span data-ttu-id="d1af1-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1af1-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1af1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1af1-150">CommonParameters</span></span>
<span data-ttu-id="d1af1-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1af1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1af1-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1af1-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1af1-153">입력</span><span class="sxs-lookup"><span data-stu-id="d1af1-153">INPUTS</span></span>

### <span data-ttu-id="d1af1-154">WorkloadType에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="d1af1-154">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span></span>

### <span data-ttu-id="d1af1-155">시스템 Null 허용 ' 1 [[4.3.1.0 관리]. e-유틸리티의 BackupManagementType, Microsoft Azure. 명령. e 1.-모델, Version =, Culture = 중립, PublicKeyToken = null]</span><span class="sxs-lookup"><span data-stu-id="d1af1-155">System.Nullable\`1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.Commands.RecoveryServices.Backup.Models, Version=4.3.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d1af1-156">Microsoft Azure.. i 0. a 0 유틸리티.</span><span class="sxs-lookup"><span data-stu-id="d1af1-156">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

### <span data-ttu-id="d1af1-157">SchedulePolicyBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="d1af1-157">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

### <span data-ttu-id="d1af1-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d1af1-158">System.String</span></span>
<span data-ttu-id="d1af1-159">매개 변수: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d1af1-159">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="d1af1-160">출력</span><span class="sxs-lookup"><span data-stu-id="d1af1-160">OUTPUTS</span></span>

### <span data-ttu-id="d1af1-161">Microsoft. \*. i i m.. i i m.</span><span class="sxs-lookup"><span data-stu-id="d1af1-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="d1af1-162">상속자</span><span class="sxs-lookup"><span data-stu-id="d1af1-162">NOTES</span></span>

## <span data-ttu-id="d1af1-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1af1-163">RELATED LINKS</span></span>

[<span data-ttu-id="d1af1-164">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="d1af1-164">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="d1af1-165">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d1af1-165">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="d1af1-166">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="d1af1-166">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="d1af1-167">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="d1af1-167">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="d1af1-168">제거-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d1af1-168">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="d1af1-169">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d1af1-169">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


