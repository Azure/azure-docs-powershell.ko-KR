---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azstorageblobrange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
ms.openlocfilehash: ee8a8bd6a12d3f4aa1dc1624d0dc5c11de972b11
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047505"
---
# <span data-ttu-id="4848b-101">Restore-AzStorageBlobRange</span><span class="sxs-lookup"><span data-stu-id="4848b-101">Restore-AzStorageBlobRange</span></span>

## <span data-ttu-id="4848b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4848b-102">SYNOPSIS</span></span>
<span data-ttu-id="4848b-103">특정 blob 범위에 대해 저장소 계정을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4848b-103">Restores a Storage account for specific blob ranges.</span></span>

## <span data-ttu-id="4848b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4848b-104">SYNTAX</span></span>

### <span data-ttu-id="4848b-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="4848b-105">AccountName (Default)</span></span>
```
Restore-AzStorageBlobRange [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -TimeToRestore <DateTime> [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4848b-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="4848b-106">AccountResourceId</span></span>
```
Restore-AzStorageBlobRange [-ResourceId] <String> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4848b-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="4848b-107">AccountObject</span></span>
```
Restore-AzStorageBlobRange -StorageAccount <PSStorageAccount> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4848b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4848b-108">DESCRIPTION</span></span>
<span data-ttu-id="4848b-109">**AzStorageBlobRange** cmdlet은 특정 blob 범위에 대해 저장소 계정에 blob을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4848b-109">The **Restore-AzStorageBlobRange** cmdlet restores blobs in a Storage account for specific blob ranges.</span></span>
<span data-ttu-id="4848b-110">시작 범위가 포함 되며, 끝 범위가 blob restore에서 제외 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4848b-110">The start range is included, and the end range is excluded in blob restore.</span></span>

## <span data-ttu-id="4848b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="4848b-111">EXAMPLES</span></span>

### <span data-ttu-id="4848b-112">예제 1: 시작 특정 blob 범위를 사용 하 여 저장소 계정에 blob 복원</span><span class="sxs-lookup"><span data-stu-id="4848b-112">Example 1: Start restores blobs in a Storage account with specific blob ranges</span></span>
```powershell
PS C:\> $range1 = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
PS C:\> $range2 = New-AzStorageBlobRangeToRestore -StartRange container3/blob3 -EndRange container4/blob4
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddDays(-1) -BlobRestoreRange $range1,$range2

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                     
------     ---------                            ------------- ------------------------     ---------------------                     
InProgress 6ca55a8b-fca0-461a-8e4c-13927a9707e6               2020-02-10T13:58:44.6841810Z ["container1/blob1" -> "container2/blob2",...]

PS C:\> (Get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName -IncludeBlobRestoreStatus).BlobRestoreStatus 

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                     
------   ---------                            ------------- ------------------------     ---------------------                     
Complete 6ca55a8b-fca0-461a-8e4c-13927a9707e6               2020-02-10T13:58:44.6841810Z ["container1/blob1" -> "container2/blob2",...]
```

<span data-ttu-id="4848b-113">이 명령은 먼저 2 개의 blob 범위를 만든 다음 start는 1 일 전 2 개의 blob 범위를 사용 하 여 저장소 계정에 blob을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4848b-113">This command first creates 2 blob ranges, then start restores blobs in a Storage account with the 2 blob ranges from 1 day ago.</span></span> <span data-ttu-id="4848b-114">사용자는 Get-AzStorageAccount를 사용 하 여 나중에 복원 상태를 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4848b-114">User can use Get-AzStorageAccount to trace the restore status later.</span></span>

### <span data-ttu-id="4848b-115">예제 2: 백엔드의 저장소 계정에 있는 모든 blob 복원</span><span class="sxs-lookup"><span data-stu-id="4848b-115">Example 2: Restores all blobs in a Storage account in the backend</span></span>
```powershell
PS C:\> $job = Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddMinutes(-30) -WaitForComplete -asjob

PS C:\> $job | Wait-Job

PS C:\> $job.Output

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges
------   ---------                            ------------- ------------------------     ---------------------
Complete 0387953a-bbe6-4602-818d-e661581ee44b               2020-08-28T07:11:33.9843100Z ["" -> ""]
```

<span data-ttu-id="4848b-116">이 명령은 저장소 계정의 모든 blob을 30 분 전에 복원 하 고 복원이 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="4848b-116">This command restores all blobs in a Storage account from 30 minutes ago, and wait for the restore complete.</span></span> <span data-ttu-id="4848b-117">Blob 복원에 시간이 오래 걸릴 수 있으므로-Asjob 매개 변수를 사용 하 여 백엔드에서 실행 한 다음 작업이 완료 될 때까지 기다렸다가 결과를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4848b-117">Since restore blobs might take a long time, run it in the backend with -Asjob parameter, and then wait for the job complete and show the result.</span></span>

### <span data-ttu-id="4848b-118">예제 3: 입력 blob 범위를 기준으로 blob을 직접 복원 하 고 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="4848b-118">Example 3: Restores blobs by input blob ranges directly, and wait for complete</span></span>
```powershell
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -WaitForComplete `
    -TimeToRestore (Get-Date).AddSeconds(-1) `
    -BlobRestoreRange @{StartRange="aaa/abc";EndRange="bbb/abc"},@{StartRange="bbb/acc";EndRange=""}
WARNING: Restore blob rang with Id 'd66d1d02-6e48-47ef-b516-0155dd8319c6' started. Restore blob ranges time to complete is dependent on the size of the restore.

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges   
------   ---------                            ------------- ------------------------     ---------------------   
Complete d66d1d02-6e48-47ef-b516-0155dd8319c6               2020-02-10T14:17:46.8189116Z ["aaa/abc" -> "bbb/abc",...]
```

<span data-ttu-id="4848b-119">이 명령은 1 일 전부터 저장소 계정의 blob을 복원 하 고, 입력 2 blob는 Restore-AzStorageBlobRange cmdlet으로 직접 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4848b-119">This command restores blobs in a Storage account from 1 day ago, by input 2 blob ranges directly to the Restore-AzStorageBlobRange cmdlet.</span></span> <span data-ttu-id="4848b-120">이 명령은 복원이 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="4848b-120">This command will wait for the restore complete.</span></span>

## <span data-ttu-id="4848b-121">변수</span><span class="sxs-lookup"><span data-stu-id="4848b-121">PARAMETERS</span></span>

### <span data-ttu-id="4848b-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4848b-122">-AsJob</span></span>
<span data-ttu-id="4848b-123">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4848b-123">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4848b-124">-BlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="4848b-124">-BlobRestoreRange</span></span>
<span data-ttu-id="4848b-125">복원할 blob 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="4848b-125">The blob range to Restore.</span></span>
<span data-ttu-id="4848b-126">이 매개 변수를 지정 하지 않으면 모든 blob이 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4848b-126">If not specify this parameter, will restore all blobs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4848b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4848b-127">-DefaultProfile</span></span>
<span data-ttu-id="4848b-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4848b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4848b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4848b-129">-ResourceGroupName</span></span>
<span data-ttu-id="4848b-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4848b-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4848b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4848b-131">-ResourceId</span></span>
<span data-ttu-id="4848b-132">저장소 계정 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="4848b-132">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4848b-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="4848b-133">-StorageAccount</span></span>
<span data-ttu-id="4848b-134">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="4848b-134">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4848b-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4848b-135">-StorageAccountName</span></span>
<span data-ttu-id="4848b-136">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4848b-136">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4848b-137">-TimeToRestore</span><span class="sxs-lookup"><span data-stu-id="4848b-137">-TimeToRestore</span></span>
<span data-ttu-id="4848b-138">Blob을 복원할 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="4848b-138">The Time to Restore Blob.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4848b-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="4848b-139">-WaitForComplete</span></span>
<span data-ttu-id="4848b-140">복원 대기 작업 완료</span><span class="sxs-lookup"><span data-stu-id="4848b-140">Wait for Restore task complete</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4848b-141">-확인</span><span class="sxs-lookup"><span data-stu-id="4848b-141">-Confirm</span></span>
<span data-ttu-id="4848b-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4848b-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4848b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4848b-143">-WhatIf</span></span>
<span data-ttu-id="4848b-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4848b-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4848b-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4848b-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4848b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4848b-146">CommonParameters</span></span>
<span data-ttu-id="4848b-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4848b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4848b-148">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4848b-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4848b-149">입력</span><span class="sxs-lookup"><span data-stu-id="4848b-149">INPUTS</span></span>

### <span data-ttu-id="4848b-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4848b-150">System.String</span></span>

### <span data-ttu-id="4848b-151">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4848b-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="4848b-152">출력</span><span class="sxs-lookup"><span data-stu-id="4848b-152">OUTPUTS</span></span>

### <span data-ttu-id="4848b-153">PSBlobRestoreStatus를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="4848b-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span></span>

## <span data-ttu-id="4848b-154">상속자</span><span class="sxs-lookup"><span data-stu-id="4848b-154">NOTES</span></span>

## <span data-ttu-id="4848b-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4848b-155">RELATED LINKS</span></span>
