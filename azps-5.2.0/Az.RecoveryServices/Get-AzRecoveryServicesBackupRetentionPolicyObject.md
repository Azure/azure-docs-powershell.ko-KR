---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: d426cd18aaf3382939e55668b1c19938319a3c51
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334082"
---
# <span data-ttu-id="38fdd-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="38fdd-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="38fdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38fdd-102">SYNOPSIS</span></span>
<span data-ttu-id="38fdd-103">기본 보존 정책 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="38fdd-103">Gets a base retention policy object.</span></span>

## <span data-ttu-id="38fdd-104">구문</span><span class="sxs-lookup"><span data-stu-id="38fdd-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38fdd-105">설명</span><span class="sxs-lookup"><span data-stu-id="38fdd-105">DESCRIPTION</span></span>
<span data-ttu-id="38fdd-106">**Get-AzRecoveryServicesBackupRetentionPolicyObject** cmdlet은 기본 **AzureRMRecoveryServicesRetentionPolicyObject를** 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="38fdd-106">The **Get-AzRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="38fdd-107">이 개체는 시스템에서 유지되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="38fdd-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="38fdd-108">새 백업 정책을 만들기 위해 New-AzRecoveryServicesBackupProtectionPolicy cmdlet과 함께 조작하고 사용할 수 있는 임시 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="38fdd-108">It is a temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="38fdd-109">예제</span><span class="sxs-lookup"><span data-stu-id="38fdd-109">EXAMPLES</span></span>

### <span data-ttu-id="38fdd-110">예제 1: 백업 보호 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="38fdd-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="38fdd-111">첫 번째 명령은 보존 정책 개체를 구한 다음 $RetPol 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="38fdd-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="38fdd-112">두 번째 명령은 보존 정책 개체의 기간을 365일로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="38fdd-112">The second command sets the duration for the retention policy object to 365 days.</span></span>
<span data-ttu-id="38fdd-113">세 번째 명령은 일정 정책 개체를 인용한 다음, 일정 변수에 $SchPol 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="38fdd-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="38fdd-114">마지막 명령은 보존 정책을 사용하여 백업 보호 정책을 만들고 이전 명령으로 만든 일정 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="38fdd-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="38fdd-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38fdd-115">PARAMETERS</span></span>

### <span data-ttu-id="38fdd-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="38fdd-116">-BackupManagementType</span></span>
<span data-ttu-id="38fdd-117">보호되는 리소스의 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="38fdd-117">The class of resources being protected.</span></span> <span data-ttu-id="38fdd-118">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="38fdd-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="38fdd-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="38fdd-119">AzureVM</span></span> 
- <span data-ttu-id="38fdd-120">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="38fdd-120">AzureWorkload</span></span>
- <span data-ttu-id="38fdd-121">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="38fdd-121">AzureStorage</span></span>

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

### <span data-ttu-id="38fdd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38fdd-122">-DefaultProfile</span></span>
<span data-ttu-id="38fdd-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="38fdd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38fdd-124">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="38fdd-124">-WorkloadType</span></span>
<span data-ttu-id="38fdd-125">리소스의 워크로드 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="38fdd-125">Workload type of the resource.</span></span> <span data-ttu-id="38fdd-126">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="38fdd-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="38fdd-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="38fdd-127">AzureVM</span></span> 
- <span data-ttu-id="38fdd-128">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="38fdd-128">AzureFiles</span></span>
- <span data-ttu-id="38fdd-129">MSSQL</span><span class="sxs-lookup"><span data-stu-id="38fdd-129">MSSQL</span></span>

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

### <span data-ttu-id="38fdd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38fdd-130">CommonParameters</span></span>
<span data-ttu-id="38fdd-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="38fdd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38fdd-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="38fdd-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38fdd-133">입력</span><span class="sxs-lookup"><span data-stu-id="38fdd-133">INPUTS</span></span>

### <span data-ttu-id="38fdd-134">없음</span><span class="sxs-lookup"><span data-stu-id="38fdd-134">None</span></span>

## <span data-ttu-id="38fdd-135">출력</span><span class="sxs-lookup"><span data-stu-id="38fdd-135">OUTPUTS</span></span>

### <span data-ttu-id="38fdd-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="38fdd-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="38fdd-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="38fdd-137">NOTES</span></span>

## <span data-ttu-id="38fdd-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="38fdd-138">RELATED LINKS</span></span>

[<span data-ttu-id="38fdd-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="38fdd-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="38fdd-140">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="38fdd-140">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)


