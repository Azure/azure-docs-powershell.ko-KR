---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 7ebbb3cf53c422a3a4d5c73f156cd3890eaa41e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343094"
---
# <span data-ttu-id="c3f88-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="c3f88-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="c3f88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3f88-102">SYNOPSIS</span></span>

<span data-ttu-id="c3f88-103">Backup 작업의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c3f88-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="c3f88-104">구문</span><span class="sxs-lookup"><span data-stu-id="c3f88-104">SYNTAX</span></span>

### <span data-ttu-id="c3f88-105">JobFilterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c3f88-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3f88-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="c3f88-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3f88-107">설명</span><span class="sxs-lookup"><span data-stu-id="c3f88-107">DESCRIPTION</span></span>

<span data-ttu-id="c3f88-108">**Get-AzRecoveryServicesBackupJobDetail** cmdlet은 지정된 작업의 Azure Backup 작업 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c3f88-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="c3f88-109">-VaultId 매개 변수를 사용하여 자격 증명 모음 컨텍스트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c3f88-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="c3f88-110">경고: **Get-AzRecoveryServicesBackupJobDetails** 별칭은 향후의 새로운 변경 릴리스에서 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3f88-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="c3f88-111">예제</span><span class="sxs-lookup"><span data-stu-id="c3f88-111">EXAMPLES</span></span>

### <span data-ttu-id="c3f88-112">예제 1: 실패한 작업의 Backup 작업 세부 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="c3f88-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="c3f88-113">첫 번째 명령은 관련 자격 증명 모음을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="c3f88-113">The first command fetches the relevant vault.</span></span> <span data-ttu-id="c3f88-114">두 번째 명령은 자격 증명 모음에 실패한 작업의 배열을 구한 다음, $Jobs 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c3f88-114">The second command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="c3f88-115">세 번째 명령은 실패한 첫 번째 작업의 작업 세부 정보를 $Jobs 다음 $JobDetails 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c3f88-115">The third command gets the job details for the 1st failed job in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="c3f88-116">마지막 명령은 실패한 작업의 오류 세부 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="c3f88-116">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="c3f88-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3f88-117">PARAMETERS</span></span>

### <span data-ttu-id="c3f88-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3f88-118">-DefaultProfile</span></span>

<span data-ttu-id="c3f88-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c3f88-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3f88-120">-Job</span><span class="sxs-lookup"><span data-stu-id="c3f88-120">-Job</span></span>

<span data-ttu-id="c3f88-121">얻을 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c3f88-121">Specifies the job to get.</span></span>
<span data-ttu-id="c3f88-122">**BackupJob 개체를 얻습니다.** **Get-AzRecoveryServicesBackupJob** cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c3f88-122">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="c3f88-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="c3f88-123">-JobId</span></span>

<span data-ttu-id="c3f88-124">Backup 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c3f88-124">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="c3f88-125">ID는 **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** 개체의 JobId 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="c3f88-125">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="c3f88-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="c3f88-126">-VaultId</span></span>

<span data-ttu-id="c3f88-127">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c3f88-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="c3f88-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3f88-128">CommonParameters</span></span>
<span data-ttu-id="c3f88-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c3f88-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3f88-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c3f88-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3f88-131">입력</span><span class="sxs-lookup"><span data-stu-id="c3f88-131">INPUTS</span></span>

### <span data-ttu-id="c3f88-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c3f88-132">System.String</span></span>

## <span data-ttu-id="c3f88-133">출력</span><span class="sxs-lookup"><span data-stu-id="c3f88-133">OUTPUTS</span></span>

### <span data-ttu-id="c3f88-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="c3f88-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="c3f88-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c3f88-135">NOTES</span></span>

## <span data-ttu-id="c3f88-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3f88-136">RELATED LINKS</span></span>

[<span data-ttu-id="c3f88-137">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="c3f88-137">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
