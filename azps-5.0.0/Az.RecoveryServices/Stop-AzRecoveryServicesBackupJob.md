---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 41234c91d5c833f15a4914d2af2de93c9c5bf288
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216847"
---
# <span data-ttu-id="d2f5e-101">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="d2f5e-101">Stop-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="d2f5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2f5e-102">SYNOPSIS</span></span>
<span data-ttu-id="d2f5e-103">실행 중인 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-103">Cancels a running job.</span></span>

## <span data-ttu-id="d2f5e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d2f5e-104">SYNTAX</span></span>

### <span data-ttu-id="d2f5e-105">JobFilterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d2f5e-105">JobFilterSet (Default)</span></span>
```
Stop-AzRecoveryServicesBackupJob [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2f5e-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="d2f5e-106">IdFilterSet</span></span>
```
Stop-AzRecoveryServicesBackupJob [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2f5e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d2f5e-107">DESCRIPTION</span></span>
<span data-ttu-id="d2f5e-108">**AzRecoveryServicesBackupJob** cmdlet은 기존 Azure Backup 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-108">The **Stop-AzRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="d2f5e-109">이 cmdlet을 사용 하 여 시간이 오래 걸리는 작업을 중지 하 고 다른 작업을 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="d2f5e-110">백업 및 복원 작업 유형만 취소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-110">You can cancel only Backup and Restore job types.</span></span>
<span data-ttu-id="d2f5e-111">현재 cmdlet을 사용 하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d2f5e-112">예제의</span><span class="sxs-lookup"><span data-stu-id="d2f5e-112">EXAMPLES</span></span>

### <span data-ttu-id="d2f5e-113">예제 1: 백업 작업 중지</span><span class="sxs-lookup"><span data-stu-id="d2f5e-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="d2f5e-114">첫 번째 명령은 백업 작업을 가져온 다음 작업을 $Job 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>
<span data-ttu-id="d2f5e-115">마지막 명령은 $Job에서 백업 작업의 인스턴스 ID를 지정 하 여 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="d2f5e-116">변수</span><span class="sxs-lookup"><span data-stu-id="d2f5e-116">PARAMETERS</span></span>

### <span data-ttu-id="d2f5e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2f5e-117">-DefaultProfile</span></span>
<span data-ttu-id="d2f5e-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2f5e-119">-작업</span><span class="sxs-lookup"><span data-stu-id="d2f5e-119">-Job</span></span>
<span data-ttu-id="d2f5e-120">이 cmdlet이 취소 하는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-120">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="d2f5e-121">**Backupjob** 개체를 가져오려면 Get-AzRecoveryServicesBackupJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-121">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: JobFilterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2f5e-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="d2f5e-122">-JobId</span></span>
<span data-ttu-id="d2f5e-123">취소할 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-123">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="d2f5e-124">ID는 **Backupjob** 개체의 InstanceId 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-124">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="d2f5e-125">**Backupjob** 개체를 가져오려면 Get-help를 AzRecoveryServicesBackupJob를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-125">To obtain an **BackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFilterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2f5e-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d2f5e-126">-VaultId</span></span>
<span data-ttu-id="d2f5e-127">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d2f5e-128">-확인</span><span class="sxs-lookup"><span data-stu-id="d2f5e-128">-Confirm</span></span>
<span data-ttu-id="d2f5e-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2f5e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2f5e-130">-WhatIf</span></span>
<span data-ttu-id="d2f5e-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-131">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="d2f5e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2f5e-132">CommonParameters</span></span>
<span data-ttu-id="d2f5e-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2f5e-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2f5e-135">입력</span><span class="sxs-lookup"><span data-stu-id="d2f5e-135">INPUTS</span></span>

### <span data-ttu-id="d2f5e-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d2f5e-136">System.String</span></span>

## <span data-ttu-id="d2f5e-137">출력</span><span class="sxs-lookup"><span data-stu-id="d2f5e-137">OUTPUTS</span></span>

### <span data-ttu-id="d2f5e-138">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="d2f5e-139">상속자</span><span class="sxs-lookup"><span data-stu-id="d2f5e-139">NOTES</span></span>

## <span data-ttu-id="d2f5e-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2f5e-140">RELATED LINKS</span></span>

[<span data-ttu-id="d2f5e-141">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="d2f5e-141">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="d2f5e-142">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="d2f5e-142">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


