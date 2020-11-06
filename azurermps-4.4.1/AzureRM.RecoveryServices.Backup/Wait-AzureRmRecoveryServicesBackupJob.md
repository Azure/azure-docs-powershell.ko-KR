---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: c4678cfb29d366c5ad855ea86313ea36be35e10b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530711"
---
# <span data-ttu-id="57832-101">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="57832-101">Wait-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="57832-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57832-102">SYNOPSIS</span></span>
<span data-ttu-id="57832-103">백업 작업이 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="57832-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57832-104">구문과</span><span class="sxs-lookup"><span data-stu-id="57832-104">SYNTAX</span></span>

```
Wait-AzureRmRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57832-105">설명은</span><span class="sxs-lookup"><span data-stu-id="57832-105">DESCRIPTION</span></span>
<span data-ttu-id="57832-106">**AzureRmRecoveryServicesBackupJob** Cmdlet은 Azure Backup 작업이 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="57832-106">The **Wait-AzureRmRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="57832-107">백업 작업에는 시간이 오래 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57832-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="57832-108">스크립트의 일부로 백업 작업을 실행 하는 경우 스크립트에서 작업이 완료 될 때까지 기다렸다가 다른 작업을 계속 하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57832-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>

<span data-ttu-id="57832-109">이 cmdlet을 포함 하는 스크립트는 작업 상태에 대 한 백업 서비스를 폴링하는 것 보다 더 간단 하 게 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57832-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>

<span data-ttu-id="57832-110">현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57832-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="57832-111">예제의</span><span class="sxs-lookup"><span data-stu-id="57832-111">EXAMPLES</span></span>

### <span data-ttu-id="57832-112">예제 1: 작업이 완료 될 때까지 대기</span><span class="sxs-lookup"><span data-stu-id="57832-112">Example 1: Wait for a job to finish</span></span>
```
PS C:\>
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
    $Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $Job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob -Job $Job
    }
   Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="57832-113">이 스크립트는 작업이 완료 될 때까지 현재 진행 중인 첫 번째 작업을 폴링합니다.</span><span class="sxs-lookup"><span data-stu-id="57832-113">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="57832-114">변수</span><span class="sxs-lookup"><span data-stu-id="57832-114">PARAMETERS</span></span>

### <span data-ttu-id="57832-115">-작업</span><span class="sxs-lookup"><span data-stu-id="57832-115">-Job</span></span>
<span data-ttu-id="57832-116">대기할 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57832-116">Specifies the job to wait for.</span></span>
<span data-ttu-id="57832-117">**Backupjob** 개체를 가져오려면 Get-AzureRmRecoveryServicesBackupJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="57832-117">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="57832-118">-시간 제한</span><span class="sxs-lookup"><span data-stu-id="57832-118">-Timeout</span></span>
<span data-ttu-id="57832-119">작업이 완료 될 때까지이 cmdlet이 대기 하는 최대 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57832-119">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="57832-120">시간 초과 값을 지정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="57832-120">It is recommended to specify a time-out value.</span></span>

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

### <span data-ttu-id="57832-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57832-121">-DefaultProfile</span></span>
<span data-ttu-id="57832-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57832-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57832-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57832-123">CommonParameters</span></span>
<span data-ttu-id="57832-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57832-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57832-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57832-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57832-126">입력</span><span class="sxs-lookup"><span data-stu-id="57832-126">INPUTS</span></span>

### <span data-ttu-id="57832-127">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="57832-127">Object</span></span>
<span data-ttu-id="57832-128">' Job ' 매개 변수는 파이프라인에서 ' Object ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="57832-128">Parameter 'Job' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="57832-129">출력</span><span class="sxs-lookup"><span data-stu-id="57832-129">OUTPUTS</span></span>

### <span data-ttu-id="57832-130">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="57832-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

### <span data-ttu-id="57832-131">System.webserver. IList ' 1 [Microsoft Azure. Commands. e-유틸리티의 JobBase]</span><span class="sxs-lookup"><span data-stu-id="57832-131">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="57832-132">상속자</span><span class="sxs-lookup"><span data-stu-id="57832-132">NOTES</span></span>

## <span data-ttu-id="57832-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57832-133">RELATED LINKS</span></span>

[<span data-ttu-id="57832-134">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="57832-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


