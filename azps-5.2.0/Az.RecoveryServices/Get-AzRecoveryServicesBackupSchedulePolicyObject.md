---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: d66b8515c6b2c3782c6f6c2b49d462dbb7bd1660
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342129"
---
# <span data-ttu-id="05341-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="05341-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="05341-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05341-102">SYNOPSIS</span></span>
<span data-ttu-id="05341-103">기본 일정 정책 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="05341-103">Gets a base schedule policy object.</span></span>

## <span data-ttu-id="05341-104">구문</span><span class="sxs-lookup"><span data-stu-id="05341-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05341-105">설명</span><span class="sxs-lookup"><span data-stu-id="05341-105">DESCRIPTION</span></span>
<span data-ttu-id="05341-106">**Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet은 기본 **AzureRMRecoveryServicesSchedulePolicyObject를** 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="05341-106">The **Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="05341-107">이 개체는 시스템에서 유지되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05341-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="05341-108">새 백업 보호 정책을 만들기 위해 New-AzRecoveryServicesBackupProtectionPolicy cmdlet을 조작하고 사용할 수 있는 임시 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="05341-108">It is temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="05341-109">예제</span><span class="sxs-lookup"><span data-stu-id="05341-109">EXAMPLES</span></span>

### <span data-ttu-id="05341-110">예제 1: 일정 빈도를 매주로 설정</span><span class="sxs-lookup"><span data-stu-id="05341-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="05341-111">첫 번째 명령은 보존 정책 개체를 구한 다음 $RetPol 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="05341-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="05341-112">두 번째 명령은 일정 정책 개체를 끈 다음, $SchPol 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="05341-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="05341-113">세 번째 명령은 일정 정책의 빈도를 매주로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="05341-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="05341-114">마지막 명령은 업데이트된 일정을 사용하여 백업 보호 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="05341-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="05341-115">예제 2: 백업 시간 설정</span><span class="sxs-lookup"><span data-stu-id="05341-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="05341-116">첫 번째 명령은 일정 정책 개체를 인용한 다음 $SchPol 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="05341-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="05341-117">두 번째 명령은 모든 예약된 실행 시간을 $SchPol.</span><span class="sxs-lookup"><span data-stu-id="05341-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="05341-118">세 번째 명령은 현재 날짜 및 시간을 인용한 다음, $DT 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="05341-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="05341-119">네 번째 명령은 예약된 실행 시간을 현재 시간으로 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="05341-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="05341-120">AzureVM을 매일 한 번만 백업할 수 있으므로 백업 시간을 다시 설정하려면 원래 일정을 대체해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="05341-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="05341-121">마지막 명령은 새 일정을 사용하여 백업 보호 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="05341-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="05341-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05341-122">PARAMETERS</span></span>

### <span data-ttu-id="05341-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="05341-123">-BackupManagementType</span></span>
<span data-ttu-id="05341-124">보호되는 리소스의 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="05341-124">The class of resources being protected.</span></span> <span data-ttu-id="05341-125">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="05341-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="05341-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="05341-126">AzureVM</span></span> 
- <span data-ttu-id="05341-127">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="05341-127">AzureStorage</span></span>
- <span data-ttu-id="05341-128">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="05341-128">AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05341-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05341-129">-DefaultProfile</span></span>
<span data-ttu-id="05341-130">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="05341-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05341-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="05341-131">-WorkloadType</span></span>
<span data-ttu-id="05341-132">리소스의 워크로드 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="05341-132">Workload type of the resource.</span></span> <span data-ttu-id="05341-133">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="05341-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="05341-134">AzureVM</span><span class="sxs-lookup"><span data-stu-id="05341-134">AzureVM</span></span> 
- <span data-ttu-id="05341-135">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="05341-135">AzureFiles</span></span>
- <span data-ttu-id="05341-136">MSSQL</span><span class="sxs-lookup"><span data-stu-id="05341-136">MSSQL</span></span>


```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05341-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05341-137">CommonParameters</span></span>
<span data-ttu-id="05341-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="05341-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05341-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="05341-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05341-140">입력</span><span class="sxs-lookup"><span data-stu-id="05341-140">INPUTS</span></span>

### <span data-ttu-id="05341-141">없음</span><span class="sxs-lookup"><span data-stu-id="05341-141">None</span></span>

## <span data-ttu-id="05341-142">출력</span><span class="sxs-lookup"><span data-stu-id="05341-142">OUTPUTS</span></span>

### <span data-ttu-id="05341-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="05341-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="05341-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="05341-144">NOTES</span></span>

## <span data-ttu-id="05341-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05341-145">RELATED LINKS</span></span>

[<span data-ttu-id="05341-146">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="05341-146">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="05341-147">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="05341-147">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


