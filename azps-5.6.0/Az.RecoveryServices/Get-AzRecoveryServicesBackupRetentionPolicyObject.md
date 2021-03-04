---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: bb1c63b41d27f92991a3504cdd5c2fd8fe547298
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958048"
---
# <span data-ttu-id="173c3-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="173c3-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="173c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="173c3-102">SYNOPSIS</span></span>
<span data-ttu-id="173c3-103">기본 보존 정책 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="173c3-103">Gets a base retention policy object.</span></span>

## <span data-ttu-id="173c3-104">구문</span><span class="sxs-lookup"><span data-stu-id="173c3-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="173c3-105">설명</span><span class="sxs-lookup"><span data-stu-id="173c3-105">DESCRIPTION</span></span>
<span data-ttu-id="173c3-106">**Get-AzRecoveryServicesBackupRetentionPolicyObject** cmdlet은 기본 **AzureRMRecoveryServicesRetentionPolicyObject를 얻습니다.**</span><span class="sxs-lookup"><span data-stu-id="173c3-106">The **Get-AzRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="173c3-107">이 개체는 시스템에 유지되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="173c3-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="173c3-108">새 백업 정책을 만들기 위해 New-AzRecoveryServicesBackupProtectionPolicy cmdlet과 함께 조작하고 사용할 수 있는 임시 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="173c3-108">It is a temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="173c3-109">예제</span><span class="sxs-lookup"><span data-stu-id="173c3-109">EXAMPLES</span></span>

### <span data-ttu-id="173c3-110">예제 1: 백업 보호 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="173c3-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="173c3-111">첫 번째 명령은 보존 정책 개체를 구한 다음, $RetPol 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="173c3-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="173c3-112">두 번째 명령은 보존 정책 개체의 기간을 365일로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="173c3-112">The second command sets the duration for the retention policy object to 365 days.</span></span>
<span data-ttu-id="173c3-113">세 번째 명령은 일정 정책 개체를 얻은 다음, $SchPol 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="173c3-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="173c3-114">마지막 명령은 보존 정책을 사용하여 백업 보호 정책을 만들고 이전 명령으로 만든 예약 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="173c3-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="173c3-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="173c3-115">PARAMETERS</span></span>

### <span data-ttu-id="173c3-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="173c3-116">-BackupManagementType</span></span>
<span data-ttu-id="173c3-117">보호되는 리소스의 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="173c3-117">The class of resources being protected.</span></span> <span data-ttu-id="173c3-118">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="173c3-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="173c3-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="173c3-119">AzureVM</span></span> 
- <span data-ttu-id="173c3-120">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="173c3-120">AzureWorkload</span></span>
- <span data-ttu-id="173c3-121">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="173c3-121">AzureStorage</span></span>

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

### <span data-ttu-id="173c3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="173c3-122">-DefaultProfile</span></span>
<span data-ttu-id="173c3-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="173c3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="173c3-124">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="173c3-124">-WorkloadType</span></span>
<span data-ttu-id="173c3-125">리소스의 워크로드 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="173c3-125">Workload type of the resource.</span></span> <span data-ttu-id="173c3-126">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="173c3-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="173c3-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="173c3-127">AzureVM</span></span> 
- <span data-ttu-id="173c3-128">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="173c3-128">AzureFiles</span></span>
- <span data-ttu-id="173c3-129">MSSQL</span><span class="sxs-lookup"><span data-stu-id="173c3-129">MSSQL</span></span>

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

### <span data-ttu-id="173c3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="173c3-130">CommonParameters</span></span>
<span data-ttu-id="173c3-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="173c3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="173c3-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="173c3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="173c3-133">입력</span><span class="sxs-lookup"><span data-stu-id="173c3-133">INPUTS</span></span>

### <span data-ttu-id="173c3-134">없음</span><span class="sxs-lookup"><span data-stu-id="173c3-134">None</span></span>

## <span data-ttu-id="173c3-135">출력</span><span class="sxs-lookup"><span data-stu-id="173c3-135">OUTPUTS</span></span>

### <span data-ttu-id="173c3-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="173c3-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="173c3-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="173c3-137">NOTES</span></span>

## <span data-ttu-id="173c3-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="173c3-138">RELATED LINKS</span></span>

[<span data-ttu-id="173c3-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="173c3-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="173c3-140">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="173c3-140">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)


