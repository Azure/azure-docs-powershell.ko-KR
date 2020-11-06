---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Stop-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Stop-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 63d90aa5f98f6710702a70e9609c7625626e34c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536223"
---
# <span data-ttu-id="a5ba9-101">Stop-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="a5ba9-101">Stop-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="a5ba9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5ba9-102">SYNOPSIS</span></span>
<span data-ttu-id="a5ba9-103">실행 중인 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-103">Cancels a running job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5ba9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5ba9-104">SYNTAX</span></span>

### <span data-ttu-id="a5ba9-105">JobFilterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a5ba9-105">JobFilterSet (Default)</span></span>
```
Stop-AzureRmRecoveryServicesBackupJob [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5ba9-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="a5ba9-106">IdFilterSet</span></span>
```
Stop-AzureRmRecoveryServicesBackupJob [-JobId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5ba9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a5ba9-107">DESCRIPTION</span></span>
<span data-ttu-id="a5ba9-108">**AzureRmRecoveryServicesBackupJob** cmdlet은 기존 Azure Backup 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-108">The **Stop-AzureRmRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="a5ba9-109">이 cmdlet을 사용 하 여 시간이 오래 걸리는 작업을 중지 하 고 다른 작업을 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>

<span data-ttu-id="a5ba9-110">백업 및 복원 작업 유형만 취소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-110">You can cancel only Backup and Restore job types.</span></span>

<span data-ttu-id="a5ba9-111">현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="a5ba9-112">예제의</span><span class="sxs-lookup"><span data-stu-id="a5ba9-112">EXAMPLES</span></span>

### <span data-ttu-id="a5ba9-113">예제 1: 백업 작업 중지</span><span class="sxs-lookup"><span data-stu-id="a5ba9-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzureRmRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzureRmRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="a5ba9-114">첫 번째 명령은 백업 작업을 가져온 다음 작업을 $Job 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>

<span data-ttu-id="a5ba9-115">마지막 명령은 $Job에서 백업 작업의 인스턴스 ID를 지정 하 여 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="a5ba9-116">변수</span><span class="sxs-lookup"><span data-stu-id="a5ba9-116">PARAMETERS</span></span>

### <span data-ttu-id="a5ba9-117">-작업</span><span class="sxs-lookup"><span data-stu-id="a5ba9-117">-Job</span></span>
<span data-ttu-id="a5ba9-118">이 cmdlet이 취소 하는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-118">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="a5ba9-119">**Backupjob** 개체를 가져오려면 Get-AzureRmRecoveryServicesBackupJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-119">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="a5ba9-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="a5ba9-120">-JobId</span></span>
<span data-ttu-id="a5ba9-121">취소할 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-121">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="a5ba9-122">ID는 **Backupjob** 개체의 InstanceId 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-122">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="a5ba9-123">**Backupjob** 개체를 가져오려면 Get-help를 AzureRmRecoveryServicesBackupJob를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-123">To obtain an **BackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="a5ba9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5ba9-124">-DefaultProfile</span></span>
<span data-ttu-id="a5ba9-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5ba9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5ba9-126">CommonParameters</span></span>
<span data-ttu-id="a5ba9-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5ba9-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5ba9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5ba9-129">입력</span><span class="sxs-lookup"><span data-stu-id="a5ba9-129">INPUTS</span></span>

## <span data-ttu-id="a5ba9-130">출력</span><span class="sxs-lookup"><span data-stu-id="a5ba9-130">OUTPUTS</span></span>

### <span data-ttu-id="a5ba9-131">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-131">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="a5ba9-132">상속자</span><span class="sxs-lookup"><span data-stu-id="a5ba9-132">NOTES</span></span>

## <span data-ttu-id="a5ba9-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5ba9-133">RELATED LINKS</span></span>

[<span data-ttu-id="a5ba9-134">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="a5ba9-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="a5ba9-135">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="a5ba9-135">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


