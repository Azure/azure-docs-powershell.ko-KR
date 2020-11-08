---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218134"
---
# <span data-ttu-id="29882-101">New-AzBatchResourceFile</span><span class="sxs-lookup"><span data-stu-id="29882-101">New-AzBatchResourceFile</span></span>

## <span data-ttu-id="29882-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29882-102">SYNOPSIS</span></span>
<span data-ttu-id="29882-103">에서 사용 하도록 리소스 파일을 만듭니다 `New-AzBatchTask` .</span><span class="sxs-lookup"><span data-stu-id="29882-103">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="29882-104">구문과</span><span class="sxs-lookup"><span data-stu-id="29882-104">SYNTAX</span></span>

### <span data-ttu-id="29882-105">HttpUrl (기본값)</span><span class="sxs-lookup"><span data-stu-id="29882-105">HttpUrl (Default)</span></span>
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29882-106">StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="29882-106">StorageContainerUrl</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29882-107">AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="29882-107">AutoStorageContainerName</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29882-108">설명은</span><span class="sxs-lookup"><span data-stu-id="29882-108">DESCRIPTION</span></span>
<span data-ttu-id="29882-109">에서 사용 하도록 리소스 파일을 만듭니다 `New-AzBatchTask` .</span><span class="sxs-lookup"><span data-stu-id="29882-109">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="29882-110">예제의</span><span class="sxs-lookup"><span data-stu-id="29882-110">EXAMPLES</span></span>

### <span data-ttu-id="29882-111">예제 1: 단일 파일을 가리키는 HTTP URL에서 리소스 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="29882-111">Example 1: Create a resource file from an HTTP URL pointing at a single file</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="29882-112">`PSResourceFile`HTTP url 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="29882-112">Creates a `PSResourceFile` referencing an HTTP url.</span></span>

### <span data-ttu-id="29882-113">예제 2: Azure Storage 컨테이너 URL에서 리소스 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="29882-113">Example 2: Create a resource file from an Azure Storage container URL</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="29882-114">`PSResourceFile`Azure 저장소 컨테이너 URL 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="29882-114">Creates a `PSResourceFile` referencing an Azure Storage container URL.</span></span> <span data-ttu-id="29882-115">컨테이너의 모든 파일이 지정 된 폴더에 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="29882-115">All files in the container will be downloaded to the specified folder.</span></span>

### <span data-ttu-id="29882-116">예제 3: 자동 저장소 컨테이너 이름에서 리소스 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="29882-116">Example 3: Create a resource file from an Auto Storage container name</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="29882-117">`PSResourceFile`자동 저장소 컨테이너 이름을 참조 하 여 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="29882-117">Creates a `PSResourceFile` referencing an Auto Storage container name.</span></span> <span data-ttu-id="29882-118">컨테이너의 모든 파일이 지정 된 폴더에 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="29882-118">All files in the container will be downloaded to the specified folder.</span></span>

## <span data-ttu-id="29882-119">변수</span><span class="sxs-lookup"><span data-stu-id="29882-119">PARAMETERS</span></span>

### <span data-ttu-id="29882-120">-AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="29882-120">-AutoStorageContainerName</span></span>
<span data-ttu-id="29882-121">자동 저장소 계정의 저장소 컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29882-121">The storage container name in the auto storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AutoStorageContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29882-122">-BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="29882-122">-BlobPrefix</span></span>
<span data-ttu-id="29882-123">Azure Storage 컨테이너에서 blob을 다운로드할 때 사용할 blob 접두사를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="29882-123">Gets the blob prefix to use when downloading blobs from an Azure Storage container.</span></span>
<span data-ttu-id="29882-124">이름이 지정 된 접두사로 시작 하는 blob만 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="29882-124">Only the blobs whose names begin with the specified prefix will be downloaded.</span></span>
<span data-ttu-id="29882-125">이 접두사는 부분적인 파일 이름 또는 하위 디렉터리인 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="29882-125">This prefix can be a partial filename or a subdirectory.</span></span>
<span data-ttu-id="29882-126">접두사를 지정 하지 않으면 컨테이너의 모든 파일이 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="29882-126">If a prefix is not specified, all the files in the container will be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29882-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29882-127">-DefaultProfile</span></span>
<span data-ttu-id="29882-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="29882-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29882-129">-FileMode</span><span class="sxs-lookup"><span data-stu-id="29882-129">-FileMode</span></span>
<span data-ttu-id="29882-130">파일 사용 권한 모드 특성을 8 진수 형식으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="29882-130">Gets the file permission mode attribute in octal format.</span></span>
<span data-ttu-id="29882-131">이 속성은 리소스 파일이 Linux 노드에 다운로드 된 경우에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="29882-131">This property is applicable only if the resource file is downloaded to a Linux node.</span></span>
<span data-ttu-id="29882-132">이 속성이 Linux 노드에 대해 지정 되지 않은 경우 기본값은 0770입니다.</span><span class="sxs-lookup"><span data-stu-id="29882-132">If this property is not specified for a Linux node, then the default value is 0770.</span></span>

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

### <span data-ttu-id="29882-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="29882-133">-FilePath</span></span>
<span data-ttu-id="29882-134">작업의 작업 디렉터리를 기준으로 파일을 다운로드할 계산 노드의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="29882-134">The location on the compute node to which to download the file(s), relative to the task's working directory.</span></span> <span data-ttu-id="29882-135">HttpUrl 매개 변수를 지정 하면 FilePath가 필요 하며 파일 이름을 포함 하 여 파일이 다운로드 되는 경로를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="29882-135">If the HttpUrl parameter is specified, the FilePath is required and describes the path which the file will be downloaded to, including the filename.</span></span> <span data-ttu-id="29882-136">그렇지 않고 AutoStorageContainerName 또는 StorageContainerUrl 매개 변수를 지정 하는 경우 FilePath는 선택 사항이 며 파일을 다운로드할 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="29882-136">Otherwise, if the AutoStorageContainerName or StorageContainerUrl parameters are specified, FilePath is optional and is the directory to download the files to.</span></span> <span data-ttu-id="29882-137">FilePath가 디렉터리로 사용 되는 경우 입력 데이터와 이미 연결 된 디렉터리 구조는 full에 유지 되 고 지정 된 FilePath 디렉터리에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="29882-137">In the case where FilePath is used as a directory, any directory structure already associated with the input data will be retained in full and appended to the specified FilePath directory.</span></span> <span data-ttu-id="29882-138">지정 된 상대 경로는 작업의 작업 디렉터리를 분리할 수 없습니다 (예: '. ' 사용).</span><span class="sxs-lookup"><span data-stu-id="29882-138">The specified relative path cannot break out of the task's working directory (for example by using '..').</span></span>

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29882-139">-HttpUrl</span><span class="sxs-lookup"><span data-stu-id="29882-139">-HttpUrl</span></span>
<span data-ttu-id="29882-140">다운로드할 파일의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="29882-140">The URL of the file to download.</span></span>
<span data-ttu-id="29882-141">URL이 Azure Blob Storage 인 경우 익명 액세스를 사용 하 여 읽을 수 있어야 합니다. 즉, 일괄 처리 서비스는 blob을 다운로드할 때 자격 증명을 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="29882-141">If the URL is Azure Blob Storage, it must be readable using anonymous access; that is, the Batch service does not present any credentials when downloading the blob.</span></span>
<span data-ttu-id="29882-142">Azure storage에서 blob에 대 한 이러한 URL을 가져오는 데는 다음 두 가지 방법이 있습니다. blob에 대 한 읽기 권한을 부여 하는 SA (공유 액세스 서명)를 포함 하거나 blob 또는 해당 컨테이너의 ACL을 설정 하 여 공용 액세스를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="29882-142">There are two ways to get such a URL for a blob in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the blob, or set the ACL for the blob or its container to allow public access.</span></span>

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29882-143">-StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="29882-143">-StorageContainerUrl</span></span>
<span data-ttu-id="29882-144">Azure Blob Storage 내의 blob 컨테이너에 대 한 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="29882-144">The URL of the blob container within Azure Blob Storage.</span></span>
<span data-ttu-id="29882-145">이 URL은 읽기 가능 하 고 익명 액세스를 사용 하 여 목록에 표시할 수 있어야 합니다. 즉, 일괄 처리 서비스는 컨테이너에서 blob을 다운로드할 때 자격 증명을 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="29882-145">This URL must be readable and listable using anonymous access; that is, the Batch service does not present any credentials when downloading blobs from the container.</span></span>
<span data-ttu-id="29882-146">Azure storage에서 컨테이너에 대 한 URL을 가져오는 데 사용할 수 있는 두 가지 방법이 있습니다. 컨테이너에 대 한 읽기 권한을 부여 하는 SA (공유 액세스 서명)를 포함 하거나 컨테이너에 대 한 ACL을 설정 하 여 공용 액세스를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="29882-146">There are two ways to get such a URL for a container in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the container, or set the ACL for the container to allow public access.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29882-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29882-147">CommonParameters</span></span>
<span data-ttu-id="29882-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="29882-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29882-149">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="29882-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29882-150">입력</span><span class="sxs-lookup"><span data-stu-id="29882-150">INPUTS</span></span>

### <span data-ttu-id="29882-151">않아야</span><span class="sxs-lookup"><span data-stu-id="29882-151">None</span></span>

## <span data-ttu-id="29882-152">출력</span><span class="sxs-lookup"><span data-stu-id="29882-152">OUTPUTS</span></span>

### <span data-ttu-id="29882-153">Microsoft.Azure.Commands.Batch. PSResourceFile</span><span class="sxs-lookup"><span data-stu-id="29882-153">Microsoft.Azure.Commands.Batch.Models.PSResourceFile</span></span>

## <span data-ttu-id="29882-154">상속자</span><span class="sxs-lookup"><span data-stu-id="29882-154">NOTES</span></span>

## <span data-ttu-id="29882-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29882-155">RELATED LINKS</span></span>

[<span data-ttu-id="29882-156">새로운 AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="29882-156">New-AzBatchTask</span></span>](./New-AzBatchTask.md)