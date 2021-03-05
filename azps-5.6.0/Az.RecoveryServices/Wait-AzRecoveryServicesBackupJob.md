---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: e0b3dc87ffdfc86f39f201b6384f38ce8ca1c70a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960144"
---
# <span data-ttu-id="3264f-101">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="3264f-101">Wait-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="3264f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3264f-102">SYNOPSIS</span></span>

<span data-ttu-id="3264f-103">백업 작업이 완료될 때까지 기다렸다.</span><span class="sxs-lookup"><span data-stu-id="3264f-103">Waits for a Backup job to finish.</span></span>

## <span data-ttu-id="3264f-104">구문</span><span class="sxs-lookup"><span data-stu-id="3264f-104">SYNTAX</span></span>

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3264f-105">설명</span><span class="sxs-lookup"><span data-stu-id="3264f-105">DESCRIPTION</span></span>

<span data-ttu-id="3264f-106">**Wait-AzRecoveryServicesBackupJob** cmdlet은 Azure Backup 작업이 완료될 때까지 기다렸다.</span><span class="sxs-lookup"><span data-stu-id="3264f-106">The **Wait-AzRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="3264f-107">백업 작업은 시간이 오래 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3264f-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="3264f-108">스크립트의 일부로 백업 작업을 실행하는 경우 다른 작업으로 계속하기 전에 작업이 완료될 때까지 스크립트가 대기해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3264f-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="3264f-109">이 cmdlet을 포함하는 스크립트는 작업 상태에 대한 Backup 서비스를 폴링하는 스크립트보다 간단할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3264f-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="3264f-110">-VaultId 매개 변수를 사용하여 자격 증명 모음 컨텍스트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3264f-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="3264f-111">예제</span><span class="sxs-lookup"><span data-stu-id="3264f-111">EXAMPLES</span></span>

### <span data-ttu-id="3264f-112">예제 1: 작업이 완료될 때까지 기다림</span><span class="sxs-lookup"><span data-stu-id="3264f-112">Example 1: Wait for a job to finish</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> Wait-AzRecoveryServicesBackupJob -Job $Jobs[0] -VaultId $vault.ID -Timeout 3600
```

<span data-ttu-id="3264f-113">이 스크립트는 작업이 완료되거나 1시간의 제한 기간이 만료될 때까지 현재 진행 중인 첫 번째 작업을 폴링합니다.</span><span class="sxs-lookup"><span data-stu-id="3264f-113">This script polls the first job that is currently in progress until the job has completed or timeout period of 1 hour expired.</span></span>

## <span data-ttu-id="3264f-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3264f-114">PARAMETERS</span></span>

### <span data-ttu-id="3264f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3264f-115">-DefaultProfile</span></span>

<span data-ttu-id="3264f-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3264f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3264f-117">-Job</span><span class="sxs-lookup"><span data-stu-id="3264f-117">-Job</span></span>

<span data-ttu-id="3264f-118">대기할 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3264f-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="3264f-119">**BackupJob** 개체를 얻은 경우 **Get-AzRecoveryServicesBackupJob** cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="3264f-119">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="3264f-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="3264f-120">-Timeout</span></span>

<span data-ttu-id="3264f-121">작업이 완료될 때까지 이 cmdlet이 대기하는 최대 시간을 초로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3264f-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="3264f-122">시간 지정 값을 지정하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="3264f-122">It is recommended to specify a time-out value.</span></span>

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

### <span data-ttu-id="3264f-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="3264f-123">-VaultId</span></span>

<span data-ttu-id="3264f-124">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3264f-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3264f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3264f-125">CommonParameters</span></span>
<span data-ttu-id="3264f-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3264f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3264f-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3264f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3264f-128">입력</span><span class="sxs-lookup"><span data-stu-id="3264f-128">INPUTS</span></span>

### <span data-ttu-id="3264f-129">System.Object</span><span class="sxs-lookup"><span data-stu-id="3264f-129">System.Object</span></span>

### <span data-ttu-id="3264f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3264f-130">System.String</span></span>

## <span data-ttu-id="3264f-131">출력</span><span class="sxs-lookup"><span data-stu-id="3264f-131">OUTPUTS</span></span>

### <span data-ttu-id="3264f-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="3264f-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="3264f-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3264f-133">NOTES</span></span>

## <span data-ttu-id="3264f-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3264f-134">RELATED LINKS</span></span>

[<span data-ttu-id="3264f-135">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="3264f-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
