---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
ms.openlocfilehash: 7d39ce49a76d8519f2eacf0649c52051290274f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526160"
---
# <span data-ttu-id="59eee-101">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="59eee-101">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>

## <span data-ttu-id="59eee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59eee-102">SYNOPSIS</span></span>
<span data-ttu-id="59eee-103">백업 작업에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="59eee-103">Gets details for a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59eee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59eee-104">SYNTAX</span></span>

### <span data-ttu-id="59eee-105">JobFilterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="59eee-105">JobFilterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59eee-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="59eee-106">IdFilterSet</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59eee-107">설명은</span><span class="sxs-lookup"><span data-stu-id="59eee-107">DESCRIPTION</span></span>
<span data-ttu-id="59eee-108">**AzureRmRecoveryServicesBackupJobDetails** cmdlet은 지정 된 작업에 대 한 Azure 백업 작업 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="59eee-108">The **Get-AzureRmRecoveryServicesBackupJobDetails** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="59eee-109">현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59eee-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="59eee-110">예제의</span><span class="sxs-lookup"><span data-stu-id="59eee-110">EXAMPLES</span></span>

### <span data-ttu-id="59eee-111">예제 1: 실패 한 작업에 대 한 백업 작업 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="59eee-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzureRmRecoveryServicesBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="59eee-112">첫 번째 명령은 자격 증명 모음에서 실패 한 작업의 배열을 가져온 다음 $Jobs 배열에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="59eee-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="59eee-113">두 번째 명령은 $Jobs에서 실패 한 작업에 대 한 세부 정보를 가져온 다음 $JobDetails 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="59eee-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="59eee-114">마지막 명령은 실패 한 작업에 대 한 오류 세부 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="59eee-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="59eee-115">변수</span><span class="sxs-lookup"><span data-stu-id="59eee-115">PARAMETERS</span></span>

### <span data-ttu-id="59eee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59eee-116">-DefaultProfile</span></span>
<span data-ttu-id="59eee-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59eee-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59eee-118">-작업</span><span class="sxs-lookup"><span data-stu-id="59eee-118">-Job</span></span>
<span data-ttu-id="59eee-119">가져올 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59eee-119">Specifies the job to get.</span></span>
<span data-ttu-id="59eee-120">**Backupjob** 개체를 가져오려면 Get-AzureRmRecoveryServicesBackupJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="59eee-120">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="59eee-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="59eee-121">-JobId</span></span>
<span data-ttu-id="59eee-122">백업 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59eee-122">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="59eee-123">ID는 **Backupjob** 개체의 InstanceId 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="59eee-123">The ID is the InstanceId property of a **BackupJob** object.</span></span>

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

### <span data-ttu-id="59eee-124">-VaultId</span><span class="sxs-lookup"><span data-stu-id="59eee-124">-VaultId</span></span>
<span data-ttu-id="59eee-125">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="59eee-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="59eee-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59eee-126">CommonParameters</span></span>
<span data-ttu-id="59eee-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59eee-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59eee-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59eee-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59eee-129">입력</span><span class="sxs-lookup"><span data-stu-id="59eee-129">INPUTS</span></span>

### <span data-ttu-id="59eee-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="59eee-130">System.String</span></span>
<span data-ttu-id="59eee-131">매개 변수: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="59eee-131">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="59eee-132">출력</span><span class="sxs-lookup"><span data-stu-id="59eee-132">OUTPUTS</span></span>

### <span data-ttu-id="59eee-133">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="59eee-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="59eee-134">상속자</span><span class="sxs-lookup"><span data-stu-id="59eee-134">NOTES</span></span>

## <span data-ttu-id="59eee-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59eee-135">RELATED LINKS</span></span>

[<span data-ttu-id="59eee-136">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="59eee-136">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


