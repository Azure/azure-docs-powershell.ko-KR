---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
ms.openlocfilehash: 133a779a1227c74830fdae69b52db321a63a12e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526715"
---
# <span data-ttu-id="faf7c-101">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="faf7c-101">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>

## <span data-ttu-id="faf7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faf7c-102">SYNOPSIS</span></span>
<span data-ttu-id="faf7c-103">백업 작업에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="faf7c-103">Gets details for a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="faf7c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="faf7c-104">SYNTAX</span></span>

### <span data-ttu-id="faf7c-105">JobFilterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="faf7c-105">JobFilterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="faf7c-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="faf7c-106">IdFilterSet</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-JobId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="faf7c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="faf7c-107">DESCRIPTION</span></span>
<span data-ttu-id="faf7c-108">**AzureRmRecoveryServicesBackupJobDetails** cmdlet은 지정 된 작업에 대 한 Azure 백업 작업 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="faf7c-108">The **Get-AzureRmRecoveryServicesBackupJobDetails** cmdlet gets Azure Backup job details for a specified job.</span></span>

<span data-ttu-id="faf7c-109">현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="faf7c-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="faf7c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="faf7c-110">EXAMPLES</span></span>

### <span data-ttu-id="faf7c-111">예제 1: 실패 한 작업에 대 한 백업 작업 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="faf7c-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzureRmRecoveryServicesBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="faf7c-112">첫 번째 명령은 자격 증명 모음에서 실패 한 작업의 배열을 가져온 다음 $Jobs 배열에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="faf7c-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>

<span data-ttu-id="faf7c-113">두 번째 명령은 $Jobs에서 실패 한 작업에 대 한 세부 정보를 가져온 다음 $JobDetails 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="faf7c-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>

<span data-ttu-id="faf7c-114">마지막 명령은 실패 한 작업에 대 한 오류 세부 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="faf7c-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="faf7c-115">변수</span><span class="sxs-lookup"><span data-stu-id="faf7c-115">PARAMETERS</span></span>

### <span data-ttu-id="faf7c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faf7c-116">-DefaultProfile</span></span>
<span data-ttu-id="faf7c-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="faf7c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf7c-118">-작업</span><span class="sxs-lookup"><span data-stu-id="faf7c-118">-Job</span></span>
<span data-ttu-id="faf7c-119">가져올 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="faf7c-119">Specifies the job to get.</span></span>
<span data-ttu-id="faf7c-120">**Backupjob** 개체를 가져오려면 Get-AzureRmRecoveryServicesBackupJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="faf7c-120">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: JobBase
Parameter Sets: JobFilterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf7c-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="faf7c-121">-JobId</span></span>
<span data-ttu-id="faf7c-122">백업 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="faf7c-122">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="faf7c-123">ID는 **Backupjob** 개체의 InstanceId 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="faf7c-123">The ID is the InstanceId property of a **BackupJob** object.</span></span>

```yaml
Type: String
Parameter Sets: IdFilterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf7c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faf7c-124">CommonParameters</span></span>
<span data-ttu-id="faf7c-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="faf7c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faf7c-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faf7c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faf7c-127">입력</span><span class="sxs-lookup"><span data-stu-id="faf7c-127">INPUTS</span></span>

### <span data-ttu-id="faf7c-128">않아야</span><span class="sxs-lookup"><span data-stu-id="faf7c-128">None</span></span>
<span data-ttu-id="faf7c-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="faf7c-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="faf7c-130">출력</span><span class="sxs-lookup"><span data-stu-id="faf7c-130">OUTPUTS</span></span>

### <span data-ttu-id="faf7c-131">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="faf7c-131">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="faf7c-132">상속자</span><span class="sxs-lookup"><span data-stu-id="faf7c-132">NOTES</span></span>

## <span data-ttu-id="faf7c-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="faf7c-133">RELATED LINKS</span></span>

[<span data-ttu-id="faf7c-134">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="faf7c-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


