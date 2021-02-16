---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 41234c91d5c833f15a4914d2af2de93c9c5bf288
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202012"
---
# <span data-ttu-id="f8645-101">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f8645-101">Stop-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="f8645-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8645-102">SYNOPSIS</span></span>
<span data-ttu-id="f8645-103">실행 중인 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="f8645-103">Cancels a running job.</span></span>

## <span data-ttu-id="f8645-104">구문</span><span class="sxs-lookup"><span data-stu-id="f8645-104">SYNTAX</span></span>

### <span data-ttu-id="f8645-105">JobFilterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f8645-105">JobFilterSet (Default)</span></span>
```
Stop-AzRecoveryServicesBackupJob [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8645-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="f8645-106">IdFilterSet</span></span>
```
Stop-AzRecoveryServicesBackupJob [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8645-107">설명</span><span class="sxs-lookup"><span data-stu-id="f8645-107">DESCRIPTION</span></span>
<span data-ttu-id="f8645-108">**Stop-AzRecoveryServicesBackupJob** cmdlet은 기존 Azure Backup 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="f8645-108">The **Stop-AzRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="f8645-109">이 cmdlet을 사용하여 너무 오래 걸리고 다른 활동을 차단하는 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="f8645-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="f8645-110">Backup 및 복원 작업 유형만 취소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8645-110">You can cancel only Backup and Restore job types.</span></span>
<span data-ttu-id="f8645-111">현재 cmdlet을 사용하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용하여 자격 증명 모음 컨텍스트를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8645-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="f8645-112">예제</span><span class="sxs-lookup"><span data-stu-id="f8645-112">EXAMPLES</span></span>

### <span data-ttu-id="f8645-113">예제 1: 백업 작업 중지</span><span class="sxs-lookup"><span data-stu-id="f8645-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="f8645-114">첫 번째 명령은 백업 작업을 구한 다음, 백업 $Job 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f8645-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>
<span data-ttu-id="f8645-115">마지막 명령은 백업 작업의 인스턴스 ID를 지정하여 작업을 $Job.</span><span class="sxs-lookup"><span data-stu-id="f8645-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="f8645-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8645-116">PARAMETERS</span></span>

### <span data-ttu-id="f8645-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8645-117">-DefaultProfile</span></span>
<span data-ttu-id="f8645-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f8645-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8645-119">-Job</span><span class="sxs-lookup"><span data-stu-id="f8645-119">-Job</span></span>
<span data-ttu-id="f8645-120">이 cmdlet이 취소하는 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8645-120">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="f8645-121">**BackupJob** 개체를 얻으면 Get-AzRecoveryServicesBackupJob cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f8645-121">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="f8645-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="f8645-122">-JobId</span></span>
<span data-ttu-id="f8645-123">취소할 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8645-123">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="f8645-124">ID는 **BackupJob** 개체의 InstanceId 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="f8645-124">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="f8645-125">**BackupJob 개체를 얻습니다.** Get-AzRecoveryServicesBackupJob을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f8645-125">To obtain an **BackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="f8645-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="f8645-126">-VaultId</span></span>
<span data-ttu-id="f8645-127">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f8645-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f8645-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8645-128">-Confirm</span></span>
<span data-ttu-id="f8645-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8645-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8645-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8645-130">-WhatIf</span></span>
<span data-ttu-id="f8645-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f8645-131">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="f8645-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8645-132">CommonParameters</span></span>
<span data-ttu-id="f8645-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f8645-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8645-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f8645-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8645-135">입력</span><span class="sxs-lookup"><span data-stu-id="f8645-135">INPUTS</span></span>

### <span data-ttu-id="f8645-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f8645-136">System.String</span></span>

## <span data-ttu-id="f8645-137">출력</span><span class="sxs-lookup"><span data-stu-id="f8645-137">OUTPUTS</span></span>

### <span data-ttu-id="f8645-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="f8645-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="f8645-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f8645-139">NOTES</span></span>

## <span data-ttu-id="f8645-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8645-140">RELATED LINKS</span></span>

[<span data-ttu-id="f8645-141">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f8645-141">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="f8645-142">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f8645-142">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


