---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 81c1aeded9b4bb40998448d61a5edbf35742bfcc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034349"
---
# <span data-ttu-id="0265e-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="0265e-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="0265e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0265e-102">SYNOPSIS</span></span>

<span data-ttu-id="0265e-103">백업 작업에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0265e-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="0265e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0265e-104">SYNTAX</span></span>

### <span data-ttu-id="0265e-105">JobFilterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0265e-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0265e-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="0265e-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0265e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0265e-107">DESCRIPTION</span></span>

<span data-ttu-id="0265e-108">**AzRecoveryServicesBackupJobDetail** cmdlet은 지정 된 작업에 대 한 Azure 백업 작업 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0265e-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="0265e-109">-VaultId 매개 변수를 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0265e-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="0265e-110">경고: **AzRecoveryServicesBackupJobDetails** alias는 향후 주요 변경 릴리스에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0265e-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="0265e-111">예제의</span><span class="sxs-lookup"><span data-stu-id="0265e-111">EXAMPLES</span></span>

### <span data-ttu-id="0265e-112">예제 1: 실패 한 작업에 대 한 백업 작업 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="0265e-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="0265e-113">첫 번째 명령은 자격 증명 모음에서 실패 한 작업의 배열을 가져온 다음 $Jobs 배열에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0265e-113">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="0265e-114">두 번째 명령은 $Jobs에서 실패 한 작업에 대 한 세부 정보를 가져온 다음 $JobDetails 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0265e-114">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="0265e-115">마지막 명령은 실패 한 작업에 대 한 오류 세부 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0265e-115">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="0265e-116">변수</span><span class="sxs-lookup"><span data-stu-id="0265e-116">PARAMETERS</span></span>

### <span data-ttu-id="0265e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0265e-117">-DefaultProfile</span></span>

<span data-ttu-id="0265e-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0265e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0265e-119">-작업</span><span class="sxs-lookup"><span data-stu-id="0265e-119">-Job</span></span>

<span data-ttu-id="0265e-120">가져올 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0265e-120">Specifies the job to get.</span></span>
<span data-ttu-id="0265e-121">**Backupjob** 개체를 가져오려면 **AzRecoveryServicesBackupJob** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0265e-121">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="0265e-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="0265e-122">-JobId</span></span>

<span data-ttu-id="0265e-123">백업 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0265e-123">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="0265e-124">이 ID는 **Microsoft Azure.** . d m.-To-Commands 기본 개체의 JobId 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="0265e-124">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="0265e-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0265e-125">-VaultId</span></span>

<span data-ttu-id="0265e-126">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0265e-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0265e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0265e-127">CommonParameters</span></span>
<span data-ttu-id="0265e-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0265e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0265e-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0265e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0265e-130">입력</span><span class="sxs-lookup"><span data-stu-id="0265e-130">INPUTS</span></span>

### <span data-ttu-id="0265e-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0265e-131">System.String</span></span>

## <span data-ttu-id="0265e-132">출력</span><span class="sxs-lookup"><span data-stu-id="0265e-132">OUTPUTS</span></span>

### <span data-ttu-id="0265e-133">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="0265e-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="0265e-134">상속자</span><span class="sxs-lookup"><span data-stu-id="0265e-134">NOTES</span></span>

## <span data-ttu-id="0265e-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0265e-135">RELATED LINKS</span></span>

[<span data-ttu-id="0265e-136">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="0265e-136">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
