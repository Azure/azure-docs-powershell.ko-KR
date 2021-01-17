---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361327"
---
# <span data-ttu-id="e1f77-101">New-AzBatchResourceFile</span><span class="sxs-lookup"><span data-stu-id="e1f77-101">New-AzBatchResourceFile</span></span>

## <span data-ttu-id="e1f77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1f77-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f77-103">에서 사용할 리소스 파일을 `New-AzBatchTask` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-103">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="e1f77-104">구문</span><span class="sxs-lookup"><span data-stu-id="e1f77-104">SYNTAX</span></span>

### <span data-ttu-id="e1f77-105">HttpUrl(기본값)</span><span class="sxs-lookup"><span data-stu-id="e1f77-105">HttpUrl (Default)</span></span>
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1f77-106">StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="e1f77-106">StorageContainerUrl</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1f77-107">AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="e1f77-107">AutoStorageContainerName</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1f77-108">설명</span><span class="sxs-lookup"><span data-stu-id="e1f77-108">DESCRIPTION</span></span>
<span data-ttu-id="e1f77-109">에서 사용할 리소스 파일을 `New-AzBatchTask` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-109">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="e1f77-110">예제</span><span class="sxs-lookup"><span data-stu-id="e1f77-110">EXAMPLES</span></span>

### <span data-ttu-id="e1f77-111">예제 1: 단일 파일을 포인터로 하는 HTTP URL에서 리소스 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="e1f77-111">Example 1: Create a resource file from an HTTP URL pointing at a single file</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="e1f77-112">HTTP URL `PSResourceFile` 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-112">Creates a `PSResourceFile` referencing an HTTP url.</span></span>

### <span data-ttu-id="e1f77-113">예제 2: Azure Storage 컨테이너 URL에서 리소스 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="e1f77-113">Example 2: Create a resource file from an Azure Storage container URL</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="e1f77-114">Azure `PSResourceFile` Storage 컨테이너 URL을 참조하는 것을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-114">Creates a `PSResourceFile` referencing an Azure Storage container URL.</span></span> <span data-ttu-id="e1f77-115">컨테이너의 모든 파일은 지정된 폴더에 다운로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-115">All files in the container will be downloaded to the specified folder.</span></span>

### <span data-ttu-id="e1f77-116">예제 3: 자동 저장소 컨테이너 이름에서 리소스 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="e1f77-116">Example 3: Create a resource file from an Auto Storage container name</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="e1f77-117">자동 저장소 `PSResourceFile` 컨테이너 이름을 참조하는 이름을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-117">Creates a `PSResourceFile` referencing an Auto Storage container name.</span></span> <span data-ttu-id="e1f77-118">컨테이너의 모든 파일은 지정된 폴더에 다운로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-118">All files in the container will be downloaded to the specified folder.</span></span>

## <span data-ttu-id="e1f77-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1f77-119">PARAMETERS</span></span>

### <span data-ttu-id="e1f77-120">-AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="e1f77-120">-AutoStorageContainerName</span></span>
<span data-ttu-id="e1f77-121">자동 저장소 계정의 저장소 컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-121">The storage container name in the auto storage account.</span></span>

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

### <span data-ttu-id="e1f77-122">-BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="e1f77-122">-BlobPrefix</span></span>
<span data-ttu-id="e1f77-123">Azure Storage 컨테이너에서 Blob을 다운로드할 때 사용할 Blob prefix를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-123">Gets the blob prefix to use when downloading blobs from an Azure Storage container.</span></span>
<span data-ttu-id="e1f77-124">이름이 지정된 prefix로 시작하는 Blob만 다운로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-124">Only the blobs whose names begin with the specified prefix will be downloaded.</span></span>
<span data-ttu-id="e1f77-125">이 prefix는 부분 파일 이름 또는 하위디렉트일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-125">This prefix can be a partial filename or a subdirectory.</span></span>
<span data-ttu-id="e1f77-126">지정하지 않은 경우 컨테이너의 모든 파일이 다운로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-126">If a prefix is not specified, all the files in the container will be downloaded.</span></span>

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

### <span data-ttu-id="e1f77-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1f77-127">-DefaultProfile</span></span>
<span data-ttu-id="e1f77-128">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1f77-129">-FileMode</span><span class="sxs-lookup"><span data-stu-id="e1f77-129">-FileMode</span></span>
<span data-ttu-id="e1f77-130">8진수 형식의 파일 사용 권한 모드 특성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-130">Gets the file permission mode attribute in octal format.</span></span>
<span data-ttu-id="e1f77-131">이 속성은 리소스 파일이 Linux 노드에 다운로드된 경우만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-131">This property is applicable only if the resource file is downloaded to a Linux node.</span></span>
<span data-ttu-id="e1f77-132">Linux 노드에 대해 이 속성을 지정하지 않으면 기본값은 0770입니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-132">If this property is not specified for a Linux node, then the default value is 0770.</span></span>

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

### <span data-ttu-id="e1f77-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="e1f77-133">-FilePath</span></span>
<span data-ttu-id="e1f77-134">태스크의 작업 디렉터리를 상대로 파일을 다운로드할 계산 노드의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-134">The location on the compute node to which to download the file(s), relative to the task's working directory.</span></span> <span data-ttu-id="e1f77-135">HttpUrl 매개 변수를 지정하는 경우 FilePath가 필요하며 파일 이름을 포함하여 파일을 다운로드할 경로를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-135">If the HttpUrl parameter is specified, the FilePath is required and describes the path which the file will be downloaded to, including the filename.</span></span> <span data-ttu-id="e1f77-136">그렇지 않은 경우 AutoStorageContainerName 또는 StorageContainerUrl 매개 변수가 지정된 경우 FilePath는 선택 사항이며 파일을 다운로드할 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-136">Otherwise, if the AutoStorageContainerName or StorageContainerUrl parameters are specified, FilePath is optional and is the directory to download the files to.</span></span> <span data-ttu-id="e1f77-137">FilePath가 디렉터리로 사용되는 경우 입력 데이터와 연결된 모든 디렉터리 구조가 전체로 유지되고 지정된 FilePath 디렉터리에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-137">In the case where FilePath is used as a directory, any directory structure already associated with the input data will be retained in full and appended to the specified FilePath directory.</span></span> <span data-ttu-id="e1f77-138">지정된 상대 경로는 작업의 작업 디렉터리를 끊을 수 없습니다(예: '..'를 사용하여).</span><span class="sxs-lookup"><span data-stu-id="e1f77-138">The specified relative path cannot break out of the task's working directory (for example by using '..').</span></span>

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

### <span data-ttu-id="e1f77-139">-HttpUrl</span><span class="sxs-lookup"><span data-stu-id="e1f77-139">-HttpUrl</span></span>
<span data-ttu-id="e1f77-140">다운로드할 파일의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-140">The URL of the file to download.</span></span>
<span data-ttu-id="e1f77-141">URL이 Azure Blob Storage인 경우 익명 액세스를 사용하여 읽을 수 있어야 합니다. 즉, Batch 서비스는 Blob을 다운로드할 때 자격 증명을 제시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-141">If the URL is Azure Blob Storage, it must be readable using anonymous access; that is, the Batch service does not present any credentials when downloading the blob.</span></span>
<span data-ttu-id="e1f77-142">Azure Storage에서 Blob에 대한 이러한 URL을 얻을 수 있는 두 가지 방법은 Blob에 대한 읽기 권한을 부여하는 SAS(공유 액세스 서명)를 포함하거나 Blob 또는 해당 컨테이너에 대한 ACL을 설정하여 공용 액세스를 허용하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-142">There are two ways to get such a URL for a blob in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the blob, or set the ACL for the blob or its container to allow public access.</span></span>

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

### <span data-ttu-id="e1f77-143">-StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="e1f77-143">-StorageContainerUrl</span></span>
<span data-ttu-id="e1f77-144">Azure Blob Storage 내의 Blob 컨테이너의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-144">The URL of the blob container within Azure Blob Storage.</span></span>
<span data-ttu-id="e1f77-145">이 URL은 익명 액세스를 사용하여 읽을 수 있어야 합니다. 즉, Batch 서비스는 컨테이너에서 Blob을 다운로드할 때 자격 증명을 제시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-145">This URL must be readable and listable using anonymous access; that is, the Batch service does not present any credentials when downloading blobs from the container.</span></span>
<span data-ttu-id="e1f77-146">Azure Storage에서 컨테이너에 대한 이러한 URL을 얻을 수 있는 두 가지 방법은 컨테이너에 대한 읽기 권한을 부여하는 SAS(공유 액세스 서명)를 포함하거나 공용 액세스를 허용하도록 컨테이너에 대한 ACL을 설정하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-146">There are two ways to get such a URL for a container in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the container, or set the ACL for the container to allow public access.</span></span>

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

### <span data-ttu-id="e1f77-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f77-147">CommonParameters</span></span>
<span data-ttu-id="e1f77-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e1f77-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f77-149">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e1f77-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f77-150">입력</span><span class="sxs-lookup"><span data-stu-id="e1f77-150">INPUTS</span></span>

### <span data-ttu-id="e1f77-151">없음</span><span class="sxs-lookup"><span data-stu-id="e1f77-151">None</span></span>

## <span data-ttu-id="e1f77-152">출력</span><span class="sxs-lookup"><span data-stu-id="e1f77-152">OUTPUTS</span></span>

### <span data-ttu-id="e1f77-153">Microsoft.Azure.Commands.Batch. Models.PSResourceFile</span><span class="sxs-lookup"><span data-stu-id="e1f77-153">Microsoft.Azure.Commands.Batch.Models.PSResourceFile</span></span>

## <span data-ttu-id="e1f77-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e1f77-154">NOTES</span></span>

## <span data-ttu-id="e1f77-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1f77-155">RELATED LINKS</span></span>

[<span data-ttu-id="e1f77-156">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="e1f77-156">New-AzBatchTask</span></span>](./New-AzBatchTask.md)