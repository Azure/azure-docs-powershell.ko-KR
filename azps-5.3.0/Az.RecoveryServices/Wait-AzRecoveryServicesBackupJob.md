---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: d494169c989096ce562858c500289527479d42dd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490759"
---
# <span data-ttu-id="2c3fd-101">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="2c3fd-101">Wait-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="2c3fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c3fd-102">SYNOPSIS</span></span>

<span data-ttu-id="2c3fd-103">Backup 작업이 완료될 때까지 기다릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2c3fd-103">Waits for a Backup job to finish.</span></span>

## <span data-ttu-id="2c3fd-104">구문</span><span class="sxs-lookup"><span data-stu-id="2c3fd-104">SYNTAX</span></span>

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c3fd-105">설명</span><span class="sxs-lookup"><span data-stu-id="2c3fd-105">DESCRIPTION</span></span>

<span data-ttu-id="2c3fd-106">**Wait-AzRecoveryServicesBackupJob** cmdlet은 Azure Backup 작업이 완료될 때까지 대기합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3fd-106">The **Wait-AzRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="2c3fd-107">백업 작업은 시간이 오래 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2c3fd-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="2c3fd-108">스크립트의 일부로 백업 작업을 실행하면 스크립트가 작업을 완료할 때까지 기다렸다가 다른 태스크로 계속 진행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2c3fd-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="2c3fd-109">이 cmdlet을 포함하는 스크립트는 작업 상태에 대한 Backup 서비스를 폴링하는 스크립트보다 간단할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2c3fd-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="2c3fd-110">-VaultId 매개 변수를 사용하여 자격 증명 모음 컨텍스트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3fd-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="2c3fd-111">예제</span><span class="sxs-lookup"><span data-stu-id="2c3fd-111">EXAMPLES</span></span>

### <span data-ttu-id="2c3fd-112">예제 1: 작업이 완료될 때까지 대기</span><span class="sxs-lookup"><span data-stu-id="2c3fd-112">Example 1: Wait for a job to finish</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> Wait-AzRecoveryServicesBackupJob -Job $Jobs[0] -VaultId $vault.ID -Timeout 3600
```

<span data-ttu-id="2c3fd-113">이 스크립트는 작업이 완료되거나 1시간의 시간 제한 기간이 만료될 때까지 현재 진행 중인 첫 번째 작업을 폴링합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3fd-113">This script polls the first job that is currently in progress until the job has completed or timeout period of 1 hour expired.</span></span>

## <span data-ttu-id="2c3fd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c3fd-114">PARAMETERS</span></span>

### <span data-ttu-id="2c3fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c3fd-115">-DefaultProfile</span></span>

<span data-ttu-id="2c3fd-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3fd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c3fd-117">-Job</span><span class="sxs-lookup"><span data-stu-id="2c3fd-117">-Job</span></span>

<span data-ttu-id="2c3fd-118">대기할 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3fd-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="2c3fd-119">**BackupJob 개체를 얻습니다.** **Get-AzRecoveryServicesBackupJob** cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3fd-119">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c3fd-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="2c3fd-120">-Timeout</span></span>

<span data-ttu-id="2c3fd-121">이 cmdlet이 작업이 완료될 때까지 대기하는 최대 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3fd-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="2c3fd-122">시간 시간 값을 지정하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="2c3fd-122">It is recommended to specify a time-out value.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c3fd-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2c3fd-123">-VaultId</span></span>

<span data-ttu-id="2c3fd-124">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3fd-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2c3fd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c3fd-125">CommonParameters</span></span>
<span data-ttu-id="2c3fd-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3fd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c3fd-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2c3fd-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c3fd-128">입력</span><span class="sxs-lookup"><span data-stu-id="2c3fd-128">INPUTS</span></span>

### <span data-ttu-id="2c3fd-129">System.Object</span><span class="sxs-lookup"><span data-stu-id="2c3fd-129">System.Object</span></span>

### <span data-ttu-id="2c3fd-130">System.String</span><span class="sxs-lookup"><span data-stu-id="2c3fd-130">System.String</span></span>

## <span data-ttu-id="2c3fd-131">출력</span><span class="sxs-lookup"><span data-stu-id="2c3fd-131">OUTPUTS</span></span>

### <span data-ttu-id="2c3fd-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="2c3fd-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="2c3fd-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2c3fd-133">NOTES</span></span>

## <span data-ttu-id="2c3fd-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c3fd-134">RELATED LINKS</span></span>

[<span data-ttu-id="2c3fd-135">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="2c3fd-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
