---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: c7b213fd041718de1f4f8a6c21979a6c0e7af964
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984224"
---
# <span data-ttu-id="ed249-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="ed249-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="ed249-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed249-102">SYNOPSIS</span></span>

<span data-ttu-id="ed249-103">Backup 작업의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ed249-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="ed249-104">구문</span><span class="sxs-lookup"><span data-stu-id="ed249-104">SYNTAX</span></span>

### <span data-ttu-id="ed249-105">JobFilterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ed249-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-UseSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed249-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="ed249-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-UseSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed249-107">설명</span><span class="sxs-lookup"><span data-stu-id="ed249-107">DESCRIPTION</span></span>

<span data-ttu-id="ed249-108">**Get-AzRecoveryServicesBackupJobDetail** cmdlet은 지정된 작업의 Azure Backup 작업 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ed249-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="ed249-109">-VaultId 매개 변수를 사용하여 자격 증명 모음 컨텍스트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ed249-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="ed249-110">경고: **Get-AzRecoveryServicesBackupJobDetails** 별칭은 향후 중단되는 변경 릴리스에서 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed249-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="ed249-111">예제</span><span class="sxs-lookup"><span data-stu-id="ed249-111">EXAMPLES</span></span>

### <span data-ttu-id="ed249-112">예제 1: 실패한 작업의 백업 작업 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="ed249-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="ed249-113">첫 번째 명령은 관련 자격 증명 모음을 인치합니다.</span><span class="sxs-lookup"><span data-stu-id="ed249-113">The first command fetches the relevant vault.</span></span> <span data-ttu-id="ed249-114">두 번째 명령은 자격 증명 모음에 실패한 작업의 배열을 얻은 다음, 해당 작업을 $Jobs 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ed249-114">The second command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="ed249-115">세 번째 명령은 실패한 첫 번째 작업의 작업 세부 정보를 $Jobs 다음, $JobDetails 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ed249-115">The third command gets the job details for the 1st failed job in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="ed249-116">마지막 명령은 실패한 작업의 오류 세부 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="ed249-116">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="ed249-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ed249-117">PARAMETERS</span></span>

### <span data-ttu-id="ed249-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed249-118">-DefaultProfile</span></span>

<span data-ttu-id="ed249-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ed249-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed249-120">-Job</span><span class="sxs-lookup"><span data-stu-id="ed249-120">-Job</span></span>

<span data-ttu-id="ed249-121">얻을 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ed249-121">Specifies the job to get.</span></span>
<span data-ttu-id="ed249-122">**BackupJob** 개체를 얻은 경우 **Get-AzRecoveryServicesBackupJob** cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ed249-122">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="ed249-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="ed249-123">-JobId</span></span>

<span data-ttu-id="ed249-124">Backup 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ed249-124">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="ed249-125">ID는 **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** 개체의 JobId 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="ed249-125">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="ed249-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ed249-126">-VaultId</span></span>

<span data-ttu-id="ed249-127">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ed249-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ed249-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed249-128">CommonParameters</span></span>
<span data-ttu-id="ed249-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ed249-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed249-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed249-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed249-131">입력</span><span class="sxs-lookup"><span data-stu-id="ed249-131">INPUTS</span></span>

### <span data-ttu-id="ed249-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ed249-132">System.String</span></span>

## <span data-ttu-id="ed249-133">출력</span><span class="sxs-lookup"><span data-stu-id="ed249-133">OUTPUTS</span></span>

### <span data-ttu-id="ed249-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="ed249-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="ed249-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ed249-135">NOTES</span></span>

## <span data-ttu-id="ed249-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed249-136">RELATED LINKS</span></span>

[<span data-ttu-id="ed249-137">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="ed249-137">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
