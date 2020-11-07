---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: 71650d36c319536db5ad96aa142e2712e229d712
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699685"
---
# <span data-ttu-id="0c09d-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="0c09d-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="0c09d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c09d-102">SYNOPSIS</span></span>
<span data-ttu-id="0c09d-103">기본 일정 정책 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0c09d-103">Gets a base schedule policy object.</span></span>

## <span data-ttu-id="0c09d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0c09d-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c09d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0c09d-105">DESCRIPTION</span></span>
<span data-ttu-id="0c09d-106">**AzRecoveryServicesBackupSchedulePolicyObject** cmdlet은 기본 **AzureRMRecoveryServicesSchedulePolicyObject** 를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0c09d-106">The **Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="0c09d-107">이 개체는 시스템에 유지 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c09d-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="0c09d-108">새 백업 보호 정책을 만들기 위해 New-AzRecoveryServicesBackupProtectionPolicy cmdlet을 조작 하 고 사용할 수 있는 임시 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0c09d-108">It is temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="0c09d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0c09d-109">EXAMPLES</span></span>

### <span data-ttu-id="0c09d-110">예제 1: 일정 주기를 매주로 설정</span><span class="sxs-lookup"><span data-stu-id="0c09d-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="0c09d-111">첫 번째 명령은 보존 정책 개체를 가져온 다음 $RetPol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c09d-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="0c09d-112">두 번째 명령은 일정 정책 개체를 가져온 다음 $SchPol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c09d-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="0c09d-113">세 번째 명령은 일정 정책의 빈도를 매주로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c09d-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="0c09d-114">마지막 명령은 업데이트 된 일정으로 백업 보호 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0c09d-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="0c09d-115">예제 2: 백업 시간 설정</span><span class="sxs-lookup"><span data-stu-id="0c09d-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="0c09d-116">첫 번째 명령은 일정 정책 개체를 가져온 다음 $SchPol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c09d-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="0c09d-117">두 번째 명령은 $SchPol에서 예약 된 모든 실행 시간을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c09d-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="0c09d-118">세 번째 명령은 현재 날짜와 시간을 가져온 다음이를 $DT 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c09d-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="0c09d-119">네 번째 명령은 예약 된 실행 시간을 현재 시간으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="0c09d-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="0c09d-120">1 일에 한 명만을 한 번만 백업할 수 있으므로 백업 시간을 다시 설정 하려면 원래 일정을 바꿔야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c09d-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="0c09d-121">마지막 명령은 새 일정을 사용 하 여 백업 보호 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0c09d-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="0c09d-122">변수</span><span class="sxs-lookup"><span data-stu-id="0c09d-122">PARAMETERS</span></span>

### <span data-ttu-id="0c09d-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="0c09d-123">-BackupManagementType</span></span>
<span data-ttu-id="0c09d-124">백업 관리 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c09d-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="0c09d-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0c09d-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0c09d-126">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="0c09d-126">AzureVM</span></span> 
- <span data-ttu-id="0c09d-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="0c09d-127">AzureSQLDatabase</span></span>
- <span data-ttu-id="0c09d-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="0c09d-128">AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c09d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c09d-129">-DefaultProfile</span></span>
<span data-ttu-id="0c09d-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0c09d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c09d-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="0c09d-131">-WorkloadType</span></span>
<span data-ttu-id="0c09d-132">작업 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c09d-132">Specifies the workload type.</span></span>
<span data-ttu-id="0c09d-133">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0c09d-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0c09d-134">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="0c09d-134">AzureVM</span></span> 
- <span data-ttu-id="0c09d-135">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="0c09d-135">AzureSQLDatabase</span></span>
- <span data-ttu-id="0c09d-136">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="0c09d-136">AzureFiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c09d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c09d-137">CommonParameters</span></span>
<span data-ttu-id="0c09d-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c09d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c09d-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c09d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c09d-140">입력</span><span class="sxs-lookup"><span data-stu-id="0c09d-140">INPUTS</span></span>

### <span data-ttu-id="0c09d-141">않아야</span><span class="sxs-lookup"><span data-stu-id="0c09d-141">None</span></span>

## <span data-ttu-id="0c09d-142">출력</span><span class="sxs-lookup"><span data-stu-id="0c09d-142">OUTPUTS</span></span>

### <span data-ttu-id="0c09d-143">SchedulePolicyBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="0c09d-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="0c09d-144">상속자</span><span class="sxs-lookup"><span data-stu-id="0c09d-144">NOTES</span></span>

## <span data-ttu-id="0c09d-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c09d-145">RELATED LINKS</span></span>

[<span data-ttu-id="0c09d-146">새로운 AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0c09d-146">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="0c09d-147">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0c09d-147">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


