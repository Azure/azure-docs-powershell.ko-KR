---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: d494169c989096ce562858c500289527479d42dd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219166"
---
# <span data-ttu-id="57c3d-101">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="57c3d-101">Wait-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="57c3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57c3d-102">SYNOPSIS</span></span>

<span data-ttu-id="57c3d-103">백업 작업이 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="57c3d-103">Waits for a Backup job to finish.</span></span>

## <span data-ttu-id="57c3d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="57c3d-104">SYNTAX</span></span>

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57c3d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="57c3d-105">DESCRIPTION</span></span>

<span data-ttu-id="57c3d-106">**AzRecoveryServicesBackupJob** Cmdlet은 Azure Backup 작업이 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="57c3d-106">The **Wait-AzRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="57c3d-107">백업 작업에는 시간이 오래 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57c3d-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="57c3d-108">스크립트의 일부로 백업 작업을 실행 하는 경우 스크립트에서 작업이 완료 될 때까지 기다렸다가 다른 작업을 계속 하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57c3d-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="57c3d-109">이 cmdlet을 포함 하는 스크립트는 작업 상태에 대 한 백업 서비스를 폴링하는 것 보다 더 간단 하 게 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57c3d-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="57c3d-110">-VaultId 매개 변수를 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57c3d-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="57c3d-111">예제의</span><span class="sxs-lookup"><span data-stu-id="57c3d-111">EXAMPLES</span></span>

### <span data-ttu-id="57c3d-112">예제 1: 작업이 완료 될 때까지 대기</span><span class="sxs-lookup"><span data-stu-id="57c3d-112">Example 1: Wait for a job to finish</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> Wait-AzRecoveryServicesBackupJob -Job $Jobs[0] -VaultId $vault.ID -Timeout 3600
```

<span data-ttu-id="57c3d-113">이 스크립트는 작업이 완료 되거나 시간 초과 기간이 1 시간인 만료 될 때까지 현재 진행 중인 첫 번째 작업을 폴링합니다.</span><span class="sxs-lookup"><span data-stu-id="57c3d-113">This script polls the first job that is currently in progress until the job has completed or timeout period of 1 hour expired.</span></span>

## <span data-ttu-id="57c3d-114">변수</span><span class="sxs-lookup"><span data-stu-id="57c3d-114">PARAMETERS</span></span>

### <span data-ttu-id="57c3d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57c3d-115">-DefaultProfile</span></span>

<span data-ttu-id="57c3d-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57c3d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57c3d-117">-작업</span><span class="sxs-lookup"><span data-stu-id="57c3d-117">-Job</span></span>

<span data-ttu-id="57c3d-118">대기할 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57c3d-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="57c3d-119">**Backupjob** 개체를 가져오려면 **AzRecoveryServicesBackupJob** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="57c3d-119">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="57c3d-120">-시간 제한</span><span class="sxs-lookup"><span data-stu-id="57c3d-120">-Timeout</span></span>

<span data-ttu-id="57c3d-121">작업이 완료 될 때까지이 cmdlet이 대기 하는 최대 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57c3d-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="57c3d-122">시간 초과 값을 지정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="57c3d-122">It is recommended to specify a time-out value.</span></span>

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

### <span data-ttu-id="57c3d-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="57c3d-123">-VaultId</span></span>

<span data-ttu-id="57c3d-124">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="57c3d-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="57c3d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57c3d-125">CommonParameters</span></span>
<span data-ttu-id="57c3d-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57c3d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57c3d-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="57c3d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57c3d-128">입력</span><span class="sxs-lookup"><span data-stu-id="57c3d-128">INPUTS</span></span>

### <span data-ttu-id="57c3d-129">System. 개체</span><span class="sxs-lookup"><span data-stu-id="57c3d-129">System.Object</span></span>

### <span data-ttu-id="57c3d-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="57c3d-130">System.String</span></span>

## <span data-ttu-id="57c3d-131">출력</span><span class="sxs-lookup"><span data-stu-id="57c3d-131">OUTPUTS</span></span>

### <span data-ttu-id="57c3d-132">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="57c3d-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="57c3d-133">상속자</span><span class="sxs-lookup"><span data-stu-id="57c3d-133">NOTES</span></span>

## <span data-ttu-id="57c3d-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57c3d-134">RELATED LINKS</span></span>

[<span data-ttu-id="57c3d-135">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="57c3d-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
