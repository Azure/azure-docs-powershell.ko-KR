---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: 80b1816dff686db7e84bf876fd74f9642389b42f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375992"
---
# <span data-ttu-id="5f9d9-101">Update-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="5f9d9-101">Update-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="5f9d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f9d9-102">SYNOPSIS</span></span>
<span data-ttu-id="5f9d9-103">지정된 경로에서 ACL을 재발적으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-103">Update ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="5f9d9-104">구문</span><span class="sxs-lookup"><span data-stu-id="5f9d9-104">SYNTAX</span></span>

```
Update-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f9d9-105">설명</span><span class="sxs-lookup"><span data-stu-id="5f9d9-105">DESCRIPTION</span></span>
<span data-ttu-id="5f9d9-106">**Update-AzDataLakeGen2AclRecursive** cmdlet은 지정된 경로에서 ACL을 재발적으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-106">The **Update-AzDataLakeGen2AclRecursive** cmdlet updates ACL recursively on the specified path.</span></span> <span data-ttu-id="5f9d9-107">입력 ACL은 원래 ACL을 병합합니다. AccessControlType/EntityId/DefaultScope가 동일한 ACL 항목이 있는 경우 권한 업데이트; 또는 새 ACL 항목을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-107">The input ACL will merge the the original ACL: If ACL entry with same AccessControlType/EntityId/DefaultScope exist, update permission; else add a new ACL entry.</span></span>

## <span data-ttu-id="5f9d9-108">예제</span><span class="sxs-lookup"><span data-stu-id="5f9d9-108">EXAMPLES</span></span>

### <span data-ttu-id="5f9d9-109">예제 1: 파일 파일의 루트 지시문에서 ACL 재발 업데이트</span><span class="sxs-lookup"><span data-stu-id="5f9d9-109">Example 1: Update ACL recursively on a root directiry of filesystem</span></span>
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\> Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl -Context $ctx

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 7
TotalFilesSuccessfulCount       : 5
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="5f9d9-110">이 명령은 먼저 ACL 항목이 3개인 ACL 개체를 만든 다음 파일 시스템의 루트 디렉터리에서 ACL을 재발적으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-110">This command first creates an ACL object with 3 acl entries, then updates ACL recursively on a root directory of a file system.</span></span>

### <span data-ttu-id="5f9d9-111">예제 2: 디렉터리에서 ACL을 재발적으로 업데이트하고 ContinuationToken을 통해 실패로부터 다시 시작</span><span class="sxs-lookup"><span data-stu-id="5f9d9-111">Example 2: Update ACL recursively on a directory, and resume from failure with ContinuationToken</span></span>
```
PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -Context $ctx

PS C:\> $result

FailedEntries                   : {dir1/dir2/file4}
TotalDirectoriesSuccessfulCount : 500
TotalFilesSuccessfulCount       : 2500
TotalFailureCount               : 1
ContinuationToken               : VBaHi5TfyO2ai1wYTRhIL2FjbGNibjA2c3RmATAxRDVEN0UzRENFQzZCRTAvYWRsc3Rlc3QyATAxRDY2M0ZCQTZBN0JGQTkvZGlyMC9kaXIxL2ZpbGUzFgAAAA==

PS C:\> $result.FailedEntries

Name            IsDirectory ErrorMessage                                                                   
----            ----------- ------------                                                                   
dir0/dir2/file4       False This request is not authorized to perform this operation using this permission.

# user need fix the failed item , then can resume with ContinuationToken

PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinuationToken $result.ContinuationToken -Context $ctx

PS C:\> $result

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 1000
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="5f9d9-112">이 명령은 먼저 ACL을 디렉터리에 재발적으로 업데이트하고 실패한 다음, 사용자가 실패한 파일을 수정한 후 ContinuationToken으로 다시 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-112">This command first updateds ACL recursively to a directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="5f9d9-113">예제 3: ACL을 재발적으로 청크로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5f9d9-113">Example 3: Update ACL recursively chunk by chunk</span></span>
```
$ContinueOnFailure = $true # Set it to $false if want to terminate the operation quickly on encountering failures
$token = $null
$TotalDirectoriesSuccess = 0
$TotalFilesSuccess = 0
$totalFailure = 0
$FailedEntries = New-Object System.Collections.Generic.List[System.Object]
do
{
    
    if ($ContinueOnFailure)
    {
        $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 100 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx -ContinueOnFailure
    }
    else
    {
        $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 100 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx
    }

    # echo $result
    $TotalFilesSuccess += $result.TotalFilesSuccessfulCount
    $TotalDirectoriesSuccess += $result.TotalDirectoriesSuccessfulCount
    $totalFailure += $result.TotalFailureCount
    $FailedEntries += $result.FailedEntries
    $token = $result.ContinuationToken
}while (($token -ne $null) -and (($ContinueOnFailure) -or ($result.TotalFailureCount -eq 0)))
echo ""
echo "[Result Summary]"
echo "TotalDirectoriesSuccessfulCount: `t$($TotalDirectoriesSuccess)"
echo "TotalFilesSuccessfulCount: `t`t`t$($TotalFilesSuccess)"
echo "TotalFailureCount: `t`t`t`t`t$($totalFailure)"
echo "ContinuationToken: `t`t`t`t`t$($token)"
echo "FailedEntries:"$($FailedEntries | ft)
```

<span data-ttu-id="5f9d9-114">이 스크립트는 디렉터리 청크에서 청크를 BatchSize \* MaxBatchCount로 청크 크기로 다시 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-114">This script will update ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="5f9d9-115">청크 크기는 이 스크립트에서 5000입니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-115">Chunk size is 5000 in this script.</span></span>

### <span data-ttu-id="5f9d9-116">예제 4: 디렉터리 및 ContinueOnFailure에서 ACL을 재발적으로 업데이트한 다음, 오류에서 하나씩 다시 시작</span><span class="sxs-lookup"><span data-stu-id="5f9d9-116">Example 4: Update ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
```
PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinueOnFailure -Context $ctx

PS C:\> $result

FailedEntries                   : {dir0/dir1/file1, dir0/dir2/file4}
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 500
TotalFailureCount               : 2
ContinuationToken               : VBaHi5TfyO2ai1wYTRhIL2FjbGNibjA2c3RmATAxRDVEN0UzRENFQzZCRTAvYWRsc3Rlc3QyATAxRDY2M0ZCQTZBN0JGQTkvZGlyMC9kaXIxL2ZpbGUzFgAAAA==

PS C:\> $result.FailedEntries

Name            IsDirectory ErrorMessage                                                                   
----            ----------- ------------                                                                   
dir0/dir1/file1       False This request is not authorized to perform this operation using this permission.
dir0/dir2/file4       False This request is not authorized to perform this operation using this permission.

# user need fix the failed item , then can resume with ContinuationToken

PS C:\> foreach ($path in $result.FailedEntries.Name)
        {
            # user code to fix failed entry in $path
            
            #set ACL again
            Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path $path -Acl $acl -Context $ctx
        }
```

<span data-ttu-id="5f9d9-117">이 명령은 먼저 ContinueOnFailure를 사용하여 ACL을 디렉터리에 재발적으로 업데이트하고 일부 항목이 실패한 다음 실패한 항목을 하나씩 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-117">This command first updateds ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="5f9d9-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f9d9-118">PARAMETERS</span></span>

### <span data-ttu-id="5f9d9-119">-Acl</span><span class="sxs-lookup"><span data-stu-id="5f9d9-119">-Acl</span></span>
<span data-ttu-id="5f9d9-120">파일 또는 디렉터리에 대해 재발적으로 설정할 POSIX 액세스 제어 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-120">The POSIX access control list to set recursively for the file or directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f9d9-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f9d9-121">-AsJob</span></span>
<span data-ttu-id="5f9d9-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5f9d9-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5f9d9-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="5f9d9-123">-BatchSize</span></span>
<span data-ttu-id="5f9d9-124">데이터 집합 크기가 일괄 처리 크기를 초과하면 진행률을 추적할 수 있도록 작업이 여러 요청으로 분할됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="5f9d9-125">일괄 처리 크기는 1~2000 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="5f9d9-126">기본값은 2000입니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-126">Default is 2000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f9d9-127">-Context</span><span class="sxs-lookup"><span data-stu-id="5f9d9-127">-Context</span></span>
<span data-ttu-id="5f9d9-128">Azure Storage 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="5f9d9-128">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f9d9-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="5f9d9-129">-ContinuationToken</span></span>
<span data-ttu-id="5f9d9-130">연속 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-130">Continuation Token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f9d9-131">-ContinueOnFailure</span><span class="sxs-lookup"><span data-stu-id="5f9d9-131">-ContinueOnFailure</span></span>
<span data-ttu-id="5f9d9-132">이 매개 변수를 설정하여 실패를 무시하고 디렉터리의 다른 하위 엔터티에 대한 작업을 계속 진행합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="5f9d9-133">기본적으로 오류가 발생하면 작업이 신속하게 종료됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="5f9d9-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f9d9-134">-DefaultProfile</span></span>
<span data-ttu-id="5f9d9-135">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f9d9-136">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="5f9d9-136">-FileSystem</span></span>
<span data-ttu-id="5f9d9-137">FileSystem 이름</span><span class="sxs-lookup"><span data-stu-id="5f9d9-137">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f9d9-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="5f9d9-138">-MaxBatchCount</span></span>
<span data-ttu-id="5f9d9-139">단일 변경 Access Control 작업을 실행할 수 있는 최대 일괄 처리 수입니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="5f9d9-140">데이터 집합 크기가 MaxBatchCount BatchSize를 곱하면 연속 토큰이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f9d9-141">-Path</span><span class="sxs-lookup"><span data-stu-id="5f9d9-141">-Path</span></span>
<span data-ttu-id="5f9d9-142">Acl을 재발적으로 변경할 지정된 FileSystem의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="5f9d9-143">파일 또는 디렉터리일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-143">Can be a file or directory.</span></span>
<span data-ttu-id="5f9d9-144">'directory/file.txt' 또는 'directory1/directory2/' 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="5f9d9-145">이 매개 변수를 건너뛰어 파일 파일의 루트 디렉터리에서 Acl을 재발적으로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f9d9-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f9d9-146">-Confirm</span></span>
<span data-ttu-id="5f9d9-147">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f9d9-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f9d9-148">-WhatIf</span></span>
<span data-ttu-id="5f9d9-149">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5f9d9-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f9d9-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f9d9-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f9d9-151">CommonParameters</span></span>
<span data-ttu-id="5f9d9-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f9d9-153">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f9d9-154">입력</span><span class="sxs-lookup"><span data-stu-id="5f9d9-154">INPUTS</span></span>

### <span data-ttu-id="5f9d9-155">System.String</span><span class="sxs-lookup"><span data-stu-id="5f9d9-155">System.String</span></span>

### <span data-ttu-id="5f9d9-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5f9d9-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5f9d9-157">출력</span><span class="sxs-lookup"><span data-stu-id="5f9d9-157">OUTPUTS</span></span>

### <span data-ttu-id="5f9d9-158">System.String</span><span class="sxs-lookup"><span data-stu-id="5f9d9-158">System.String</span></span>

## <span data-ttu-id="5f9d9-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5f9d9-159">NOTES</span></span>

## <span data-ttu-id="5f9d9-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f9d9-160">RELATED LINKS</span></span>
