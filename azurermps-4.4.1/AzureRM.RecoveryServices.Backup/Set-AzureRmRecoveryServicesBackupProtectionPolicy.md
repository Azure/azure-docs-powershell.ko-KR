---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: f17ce0a23c2b91cd00f2a12bb2451c4e235169ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536228"
---
# <span data-ttu-id="f5b5c-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f5b5c-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="f5b5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5b5c-102">SYNOPSIS</span></span>
<span data-ttu-id="f5b5c-103">백업 보호 정책을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b5c-103">Modifies a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5b5c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f5b5c-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase>
 [[-RetentionPolicy] <RetentionPolicyBase>] [[-SchedulePolicy] <SchedulePolicyBase>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5b5c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f5b5c-105">DESCRIPTION</span></span>
<span data-ttu-id="f5b5c-106">**Set-AzureRmBackupProtectionPolicy** cmdlet은 기존 Azure Backup 보호 정책을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b5c-106">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="f5b5c-107">백업 일정 및 보존 정책 구성 요소를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f5b5c-107">You can modify the Backup schedule and retention policy components.</span></span>

<span data-ttu-id="f5b5c-108">변경 사항은 정책과 관련 된 항목의 백업 및 보존에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f5b5c-108">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>

<span data-ttu-id="f5b5c-109">현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b5c-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="f5b5c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f5b5c-110">EXAMPLES</span></span>

### <span data-ttu-id="f5b5c-111">예제 1: 백업 보호 정책 수정</span><span class="sxs-lookup"><span data-stu-id="f5b5c-111">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="f5b5c-112">첫 번째 명령은 기본 SchedulePolicy 개체를 가져온 다음이를 $SchPol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b5c-112">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="f5b5c-113">두 번째 명령은 $SchPol의 일정 정책에서 예약 된 모든 실행 시간을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b5c-113">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>

<span data-ttu-id="f5b5c-114">세 번째 명령은 Get-Date cmdlet을 사용 하 여 현재 날짜와 시간을 얻은 다음 $DT 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b5c-114">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>

<span data-ttu-id="f5b5c-115">네 번째 명령은 일정 정책에 대 한 일정 실행 시간에 $DT 날짜와 시간을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b5c-115">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>

<span data-ttu-id="f5b5c-116">다섯 번째 명령은 기본 보존 정책 개체를 가져온 다음 $RetPol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b5c-116">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="f5b5c-117">여섯 번째 명령은 보존 기간을 365 일로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b5c-117">The sixth command sets the retention duration to 365 days.</span></span>

<span data-ttu-id="f5b5c-118">일곱째 명령에서는 NewPolicy 라는 백업 보호 정책을 가져온 다음 $Pol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b5c-118">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="f5b5c-119">마지막 명령은 $SchPol의 일정 정책과 $RetPol의 보존 정책을 사용 하 여 $Pol의 백업 보호 정책을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b5c-119">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="f5b5c-120">변수</span><span class="sxs-lookup"><span data-stu-id="f5b5c-120">PARAMETERS</span></span>

### <span data-ttu-id="f5b5c-121">-정책</span><span class="sxs-lookup"><span data-stu-id="f5b5c-121">-Policy</span></span>
<span data-ttu-id="f5b5c-122">이 cmdlet이 수정 하는 백업 보호 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b5c-122">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="f5b5c-123">**BackupProtectionPolicy** 개체를 가져오려면 Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b5c-123">To obtain a **BackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="f5b5c-124">-보존 정책</span><span class="sxs-lookup"><span data-stu-id="f5b5c-124">-RetentionPolicy</span></span>
<span data-ttu-id="f5b5c-125">기본 보존 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b5c-125">Specifies the base retention policy.</span></span>
<span data-ttu-id="f5b5c-126">**보존 정책** 개체를 얻으려면 Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b5c-126">To obtain a **RetentionPolicy** object, use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5b5c-127">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="f5b5c-127">-SchedulePolicy</span></span>
<span data-ttu-id="f5b5c-128">기본 일정 정책 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b5c-128">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="f5b5c-129">**SchedulePolicy** 개체를 가져오려면 Get-AzureRmRecoveryServicesBackupSchedulePolicyObject 개체를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b5c-129">To obtain a **SchedulePolicy** object, use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5b5c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5b5c-130">-DefaultProfile</span></span>
<span data-ttu-id="f5b5c-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5b5c-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5b5c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5b5c-132">CommonParameters</span></span>
<span data-ttu-id="f5b5c-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b5c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5b5c-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5b5c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5b5c-135">입력</span><span class="sxs-lookup"><span data-stu-id="f5b5c-135">INPUTS</span></span>

### <span data-ttu-id="f5b5c-136">PolicyBase</span><span class="sxs-lookup"><span data-stu-id="f5b5c-136">PolicyBase</span></span>
<span data-ttu-id="f5b5c-137">' Policy ' 매개 변수는 파이프라인에서 ' PolicyBase ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b5c-137">Parameter 'Policy' accepts value of type 'PolicyBase' from the pipeline</span></span>

## <span data-ttu-id="f5b5c-138">출력</span><span class="sxs-lookup"><span data-stu-id="f5b5c-138">OUTPUTS</span></span>

### <span data-ttu-id="f5b5c-139">System.webserver. List ' 1 [Microsoft Azure. e-유틸리티의 이름 '을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b5c-139">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="f5b5c-140">상속자</span><span class="sxs-lookup"><span data-stu-id="f5b5c-140">NOTES</span></span>

## <span data-ttu-id="f5b5c-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5b5c-141">RELATED LINKS</span></span>

[<span data-ttu-id="f5b5c-142">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f5b5c-142">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="f5b5c-143">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="f5b5c-143">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="f5b5c-144">새로운 AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f5b5c-144">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="f5b5c-145">제거-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f5b5c-145">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)


