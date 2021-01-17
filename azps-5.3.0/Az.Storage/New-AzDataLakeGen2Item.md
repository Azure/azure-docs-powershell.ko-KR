---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
ms.openlocfilehash: 26f3dbc3462688458647e2e9676916063ffa3586
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492089"
---
# <span data-ttu-id="06d88-101">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="06d88-101">New-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="06d88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06d88-102">SYNOPSIS</span></span>
<span data-ttu-id="06d88-103">파일 시스템으로 파일 또는 디렉터리를 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="06d88-103">Create a file or directory in a filesystem.</span></span>

## <span data-ttu-id="06d88-104">구문</span><span class="sxs-lookup"><span data-stu-id="06d88-104">SYNTAX</span></span>

### <span data-ttu-id="06d88-105">파일(기본값)</span><span class="sxs-lookup"><span data-stu-id="06d88-105">File (Default)</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -Source <String> [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06d88-106">디렉터리</span><span class="sxs-lookup"><span data-stu-id="06d88-106">Directory</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Directory] [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06d88-107">설명</span><span class="sxs-lookup"><span data-stu-id="06d88-107">DESCRIPTION</span></span>
<span data-ttu-id="06d88-108">**New-AzDataLakeGen2Item** cmdlet은 Azure 저장소 계정의 파일 시스템으로 파일 또는 디렉터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-108">The **New-AzDataLakeGen2Item** cmdlet creates a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="06d88-109">이 cmdlet은 저장소 계정에 대해 계층적 네임스페이스를 사용하도록 설정한 경우만 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="06d88-110">"-EnableHierarchicalNamespace $true"를 사용하여 "New-AzStorageAccount" cmdlet을 실행하여 이러한 종류의 계정을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="06d88-111">예제</span><span class="sxs-lookup"><span data-stu-id="06d88-111">EXAMPLES</span></span>

### <span data-ttu-id="06d88-112">예제 1: 지정된 권한, Umask, 속성 및 메타데이터가 있는 디렉터리 만들기</span><span class="sxs-lookup"><span data-stu-id="06d88-112">Example 1: Create a directory with specified permission, Umask, properties, and metadata</span></span>
```
PS C:\>New-AzDataLakeGen2Item -FileSystem "testfilesystem" -Path "dir1/dir2/" -Directory -Permission rwxrwxrwx -Umask ---rw---- -Property @{"CacheControl" = "READ"; "ContentDisposition" = "True"} -Metadata  @{"tag1" = "value1"; "tag2" = "value2" }

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2            True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="06d88-113">이 명령은 지정된 권한, Umask, 속성 및 메타데이터를 사용하여 디렉터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-113">This command creates a directory with specified Permission, Umask, properties, and metadata</span></span>

### <span data-ttu-id="06d88-114">예제 2: 로컬 원본 파일에서 Data Lake 파일 만들기(업로드)를 실행하고 cmdlet이 백그라운드에서 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-114">Example 2: Create(upload) a data lake file from a local source file, and the cmdlet runs in background</span></span>
```
PS C:\> $task = New-AzDataLakeGen2Item  -FileSystem "testfilesystem" -Path "dir1/dir2/file1" -Source "c:\sourcefile.txt" -Force -asjob
PS C:\> $task | Wait-Job
PS C:\> $task.Output

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group                
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2/file1      False        14400000        2020-03-23 09:19:13Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="06d88-115">이 명령은 로컬 원본 파일에서 Data Lake 파일을 만들고(업로드) cmdlet이 백그라운드에서 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-115">This command creates(upload) a data lake file from a local source file, and the cmdlet runs in background.</span></span>

## <span data-ttu-id="06d88-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06d88-116">PARAMETERS</span></span>

### <span data-ttu-id="06d88-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06d88-117">-AsJob</span></span>
<span data-ttu-id="06d88-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="06d88-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06d88-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="06d88-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="06d88-120">동시 비동기 작업의 총 양입니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-120">The total amount of concurrent async tasks.</span></span> <span data-ttu-id="06d88-121">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-121">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d88-122">-Context</span><span class="sxs-lookup"><span data-stu-id="06d88-122">-Context</span></span>
<span data-ttu-id="06d88-123">Azure Storage 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="06d88-123">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="06d88-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d88-124">-DefaultProfile</span></span>
<span data-ttu-id="06d88-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06d88-126">-Directory</span><span class="sxs-lookup"><span data-stu-id="06d88-126">-Directory</span></span>
<span data-ttu-id="06d88-127">이 새 항목이 파일이 아닌 디렉터리를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-127">Indicates that this new item is a directory and not a file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Directory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d88-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="06d88-128">-FileSystem</span></span>
<span data-ttu-id="06d88-129">FileSystem 이름</span><span class="sxs-lookup"><span data-stu-id="06d88-129">FileSystem name</span></span>

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

### <span data-ttu-id="06d88-130">-Force</span><span class="sxs-lookup"><span data-stu-id="06d88-130">-Force</span></span>
<span data-ttu-id="06d88-131">전달된 경우 프롬프트 없이 새 항목이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-131">If passed then new item is created without any prompt</span></span>

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

### <span data-ttu-id="06d88-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="06d88-132">-Metadata</span></span>
<span data-ttu-id="06d88-133">만든 디렉터리 또는 파일에 대한 메타데이터를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-133">Specifies metadata for the created directory or file.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d88-134">-Path</span><span class="sxs-lookup"><span data-stu-id="06d88-134">-Path</span></span>
<span data-ttu-id="06d88-135">만들어야 하는 지정된 파일 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-135">The path in the specified Filesystem that should be create.</span></span>
<span data-ttu-id="06d88-136">'directory/file.txt' 또는 'directory1/directory2/' 형식의 파일 또는 디렉터리일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-136">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06d88-137">-Permission</span><span class="sxs-lookup"><span data-stu-id="06d88-137">-Permission</span></span>
<span data-ttu-id="06d88-138">파일 소유자, 파일 소유 그룹 및 기타 사용자에 대한 POSIX 액세스 권한을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-138">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="06d88-139">각 클래스에는 읽기, 쓰기 또는 실행 권한이 부여될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-139">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="06d88-140">기호(rwxrw-rw-)가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-140">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="06d88-141">-Property</span><span class="sxs-lookup"><span data-stu-id="06d88-141">-Property</span></span>
<span data-ttu-id="06d88-142">만든 디렉터리 또는 파일에 대한 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-142">Specifies properties for the created directory or file.</span></span> <span data-ttu-id="06d88-143">파일에 지원되는 속성은 CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType입니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-143">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="06d88-144">디렉터리에 지원되는 속성은 CacheControl, ContentDisposition, ContentEncoding, ContentLanguage입니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-144">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d88-145">-Source</span><span class="sxs-lookup"><span data-stu-id="06d88-145">-Source</span></span>
<span data-ttu-id="06d88-146">Datalake Gen2 파일에 업로드할 로컬 원본 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-146">Specify the local source file path which will be upload to a Datalake Gen2 file.</span></span>

```yaml
Type: System.String
Parameter Sets: File
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06d88-147">-Umask</span><span class="sxs-lookup"><span data-stu-id="06d88-147">-Umask</span></span>
<span data-ttu-id="06d88-148">새 항목을 만들고 부모 디렉터리에 기본 ACL이 없는 경우 umask는 만들 파일 또는 디렉터리의 사용 권한을 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-148">When creating New Item and the parent directory does not have a default ACL, the umask restricts the permissions of the file or directory to be created.</span></span>
<span data-ttu-id="06d88-149">결과 사용 권한은 p & ^u에 의해 부여됩니다. 여기서 p는 권한이고 umask입니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-149">The resulting permission is given by p & ^u, where p is the permission and u is the umask.</span></span>
<span data-ttu-id="06d88-150">기호(rwxrw-rw-)가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-150">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="06d88-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06d88-151">-Confirm</span></span>
<span data-ttu-id="06d88-152">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06d88-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06d88-153">-WhatIf</span></span>
<span data-ttu-id="06d88-154">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="06d88-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06d88-155">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06d88-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d88-156">CommonParameters</span></span>
<span data-ttu-id="06d88-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="06d88-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d88-158">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="06d88-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d88-159">입력</span><span class="sxs-lookup"><span data-stu-id="06d88-159">INPUTS</span></span>

### <span data-ttu-id="06d88-160">System.String</span><span class="sxs-lookup"><span data-stu-id="06d88-160">System.String</span></span>

### <span data-ttu-id="06d88-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="06d88-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="06d88-162">출력</span><span class="sxs-lookup"><span data-stu-id="06d88-162">OUTPUTS</span></span>

### <span data-ttu-id="06d88-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="06d88-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="06d88-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="06d88-164">NOTES</span></span>

## <span data-ttu-id="06d88-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06d88-165">RELATED LINKS</span></span>
