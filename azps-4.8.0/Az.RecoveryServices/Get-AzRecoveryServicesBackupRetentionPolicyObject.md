---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: d426cd18aaf3382939e55668b1c19938319a3c51
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213361"
---
# <span data-ttu-id="b2249-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="b2249-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="b2249-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2249-102">SYNOPSIS</span></span>
<span data-ttu-id="b2249-103">기본 보존 정책 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2249-103">Gets a base retention policy object.</span></span>

## <span data-ttu-id="b2249-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b2249-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2249-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b2249-105">DESCRIPTION</span></span>
<span data-ttu-id="b2249-106">**AzRecoveryServicesBackupRetentionPolicyObject** cmdlet은 기본 **AzureRMRecoveryServicesRetentionPolicyObject** 를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2249-106">The **Get-AzRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="b2249-107">이 개체는 시스템에 유지 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b2249-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="b2249-108">새 백업 정책을 만들기 위해 New-AzRecoveryServicesBackupProtectionPolicy cmdlet을 조작 하 고 사용할 수 있는 임시 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b2249-108">It is a temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="b2249-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b2249-109">EXAMPLES</span></span>

### <span data-ttu-id="b2249-110">예제 1: 백업 보호 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="b2249-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="b2249-111">첫 번째 명령은 보존 정책 개체를 가져온 다음 $RetPol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2249-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="b2249-112">두 번째 명령은 보존 정책 개체의 기간을 365 일로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2249-112">The second command sets the duration for the retention policy object to 365 days.</span></span>
<span data-ttu-id="b2249-113">세 번째 명령은 일정 정책 개체를 가져온 다음 $SchPol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2249-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="b2249-114">마지막 명령은 이전 명령으로 만든 보존 정책 및 예약 정책을 사용 하 여 백업 보호 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2249-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="b2249-115">변수</span><span class="sxs-lookup"><span data-stu-id="b2249-115">PARAMETERS</span></span>

### <span data-ttu-id="b2249-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="b2249-116">-BackupManagementType</span></span>
<span data-ttu-id="b2249-117">보호 되는 리소스의 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="b2249-117">The class of resources being protected.</span></span> <span data-ttu-id="b2249-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b2249-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b2249-119">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="b2249-119">AzureVM</span></span> 
- <span data-ttu-id="b2249-120">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="b2249-120">AzureWorkload</span></span>
- <span data-ttu-id="b2249-121">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="b2249-121">AzureStorage</span></span>

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

### <span data-ttu-id="b2249-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2249-122">-DefaultProfile</span></span>
<span data-ttu-id="b2249-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b2249-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2249-124">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="b2249-124">-WorkloadType</span></span>
<span data-ttu-id="b2249-125">리소스의 작업 부하 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="b2249-125">Workload type of the resource.</span></span> <span data-ttu-id="b2249-126">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b2249-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b2249-127">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="b2249-127">AzureVM</span></span> 
- <span data-ttu-id="b2249-128">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="b2249-128">AzureFiles</span></span>
- <span data-ttu-id="b2249-129">원인은</span><span class="sxs-lookup"><span data-stu-id="b2249-129">MSSQL</span></span>

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

### <span data-ttu-id="b2249-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2249-130">CommonParameters</span></span>
<span data-ttu-id="b2249-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2249-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2249-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b2249-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2249-133">입력</span><span class="sxs-lookup"><span data-stu-id="b2249-133">INPUTS</span></span>

### <span data-ttu-id="b2249-134">않아야</span><span class="sxs-lookup"><span data-stu-id="b2249-134">None</span></span>

## <span data-ttu-id="b2249-135">출력</span><span class="sxs-lookup"><span data-stu-id="b2249-135">OUTPUTS</span></span>

### <span data-ttu-id="b2249-136">Microsoft Azure.. i 0. a 0 유틸리티.</span><span class="sxs-lookup"><span data-stu-id="b2249-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="b2249-137">상속자</span><span class="sxs-lookup"><span data-stu-id="b2249-137">NOTES</span></span>

## <span data-ttu-id="b2249-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2249-138">RELATED LINKS</span></span>

[<span data-ttu-id="b2249-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="b2249-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="b2249-140">새로운 AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b2249-140">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)


