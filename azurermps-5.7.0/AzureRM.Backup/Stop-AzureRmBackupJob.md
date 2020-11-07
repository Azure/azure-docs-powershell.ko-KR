---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 44C5AF58-ADC1-4BC6-9771-3FD8F0480106
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/stop-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
ms.openlocfilehash: d219f49bd3fa4660048bdf5108ca660344e2bc48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538043"
---
# <span data-ttu-id="f49cd-101">Stop-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="f49cd-101">Stop-AzureRmBackupJob</span></span>

## <span data-ttu-id="f49cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f49cd-102">SYNOPSIS</span></span>
<span data-ttu-id="f49cd-103">기존 백업 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49cd-103">Cancels an existing Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f49cd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f49cd-104">SYNTAX</span></span>

### <span data-ttu-id="f49cd-105">IdFiltersSet</span><span class="sxs-lookup"><span data-stu-id="f49cd-105">IdFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Vault <AzureRMBackupVault> -JobID <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f49cd-106">JobFiltersSet</span><span class="sxs-lookup"><span data-stu-id="f49cd-106">JobFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f49cd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f49cd-107">DESCRIPTION</span></span>
<span data-ttu-id="f49cd-108">**AzureRmBackupJob** cmdlet은 기존 Azure Backup 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49cd-108">The **Stop-AzureRmBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="f49cd-109">이 매개 변수를 사용 하 여 시간이 오래 걸리는 작업을 중지 하 고 다른 작업을 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49cd-109">Use this parameter to stop a job that takes too long and blocks other activities.</span></span>

<span data-ttu-id="f49cd-110">다음 유형의 작업만 취소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f49cd-110">You can cancel only the following types of jobs:</span></span> 

- <span data-ttu-id="f49cd-111">백업할</span><span class="sxs-lookup"><span data-stu-id="f49cd-111">Backup</span></span>
- <span data-ttu-id="f49cd-112">복원한</span><span class="sxs-lookup"><span data-stu-id="f49cd-112">Restore</span></span>

## <span data-ttu-id="f49cd-113">예제의</span><span class="sxs-lookup"><span data-stu-id="f49cd-113">EXAMPLES</span></span>

### <span data-ttu-id="f49cd-114">예제 1: 작업 ID를 사용 하 여 백업 작업 중지</span><span class="sxs-lookup"><span data-stu-id="f49cd-114">Example 1: Stop a backup job by using a job ID</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Job = Get-AzureRmBackupJob -Vault $Vault -Operation Backup
PS C:\> Stop-AzureRmBackupJob -Vault $Vault -JobID $Job.InstanceId
```

<span data-ttu-id="f49cd-115">첫 번째 명령은 **AzureRmBackupVault** cmdlet을 사용 하 여 Vault03 이라는 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f49cd-115">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="f49cd-116">명령이 $Vault 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49cd-116">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="f49cd-117">두 번째 명령은 **AzureRmBackupJob** cmdlet을 사용 하 여 $Vault의 자격 증명 모음에서 백업 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f49cd-117">The second command gets a backup job from the vault in $Vault by using the **Get-AzureRmBackupJob** cmdlet.</span></span>
<span data-ttu-id="f49cd-118">명령이 $Job 변수에 작업을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49cd-118">The command stores the job in the $Job variable.</span></span>
<span data-ttu-id="f49cd-119">이 예제에서는 지정 된 자격 증명 모음에 백업 작업이 하나만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f49cd-119">In this example, there is only one backup operation in the specified vault.</span></span>

<span data-ttu-id="f49cd-120">마지막 명령은 지정 된 ID를 가진 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49cd-120">The final command stops the job that has the specified ID.</span></span>

### <span data-ttu-id="f49cd-121">예제 2: 모든 복원 작업 중지</span><span class="sxs-lookup"><span data-stu-id="f49cd-121">Example 2: Stop all Restore operations</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Operation Restore | Stop-AzureRmBackupJob
```

<span data-ttu-id="f49cd-122">이 명령은 $Vault의 자격 증명 모음에 있는 모든 복원 작업을 가져온 다음 파이프라인 연산자를 사용 하 여 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49cd-122">This command gets all the restore operations in the vault in $Vault, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f49cd-123">현재 cmdlet은 각 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49cd-123">The current cmdlet stops each job.</span></span>

## <span data-ttu-id="f49cd-124">변수</span><span class="sxs-lookup"><span data-stu-id="f49cd-124">PARAMETERS</span></span>

### <span data-ttu-id="f49cd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f49cd-125">-DefaultProfile</span></span>
<span data-ttu-id="f49cd-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f49cd-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f49cd-127">-작업</span><span class="sxs-lookup"><span data-stu-id="f49cd-127">-Job</span></span>
<span data-ttu-id="f49cd-128">이 cmdlet이 취소 하는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49cd-128">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="f49cd-129">**AzureRmBackupJob** 개체를 가져오려면 Get-AzureRmBackupJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49cd-129">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: AzureRMBackupJob
Parameter Sets: JobFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f49cd-130">-JobID</span><span class="sxs-lookup"><span data-stu-id="f49cd-130">-JobID</span></span>
<span data-ttu-id="f49cd-131">이 cmdlet이 취소 하는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49cd-131">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="f49cd-132">**AzureRmBackupJob** 개체를 가져오려면 Get-AzureRmBackupJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49cd-132">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f49cd-133">-저장실</span><span class="sxs-lookup"><span data-stu-id="f49cd-133">-Vault</span></span>
<span data-ttu-id="f49cd-134">이 cmdlet이 작업을 취소 하는 백업 자격 증명 모음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49cd-134">Specifies the Backup vault in which this cmdlet cancels a job.</span></span>
<span data-ttu-id="f49cd-135">**AzureRmBackupVault** 개체를 가져오려면 Get-AzureRmBackupVault cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49cd-135">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f49cd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f49cd-136">CommonParameters</span></span>
<span data-ttu-id="f49cd-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49cd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f49cd-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f49cd-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f49cd-139">입력</span><span class="sxs-lookup"><span data-stu-id="f49cd-139">INPUTS</span></span>

### <span data-ttu-id="f49cd-140">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="f49cd-140">AzureRmBackupJob</span></span>

## <span data-ttu-id="f49cd-141">출력</span><span class="sxs-lookup"><span data-stu-id="f49cd-141">OUTPUTS</span></span>

### <span data-ttu-id="f49cd-142">않아야</span><span class="sxs-lookup"><span data-stu-id="f49cd-142">None</span></span>

## <span data-ttu-id="f49cd-143">상속자</span><span class="sxs-lookup"><span data-stu-id="f49cd-143">NOTES</span></span>

## <span data-ttu-id="f49cd-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f49cd-144">RELATED LINKS</span></span>

[<span data-ttu-id="f49cd-145">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="f49cd-145">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="f49cd-146">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="f49cd-146">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="f49cd-147">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="f49cd-147">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)

