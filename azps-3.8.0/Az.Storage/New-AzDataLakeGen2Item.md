---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
ms.openlocfilehash: 26f3dbc3462688458647e2e9676916063ffa3586
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043154"
---
# <span data-ttu-id="11adb-101">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="11adb-101">New-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="11adb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11adb-102">SYNOPSIS</span></span>
<span data-ttu-id="11adb-103">파일 또는 디렉터리를 filesystem에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-103">Create a file or directory in a filesystem.</span></span>

## <span data-ttu-id="11adb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11adb-104">SYNTAX</span></span>

### <span data-ttu-id="11adb-105">파일 (기본값)</span><span class="sxs-lookup"><span data-stu-id="11adb-105">File (Default)</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -Source <String> [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11adb-106">디렉토리로</span><span class="sxs-lookup"><span data-stu-id="11adb-106">Directory</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Directory] [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11adb-107">설명은</span><span class="sxs-lookup"><span data-stu-id="11adb-107">DESCRIPTION</span></span>
<span data-ttu-id="11adb-108">**AzDataLakeGen2Item** Cmdlet은 Azure 저장소 계정의 Filesystem에 파일 또는 디렉터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-108">The **New-AzDataLakeGen2Item** cmdlet creates a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="11adb-109">이 cmdlet은 저장소 계정에 대해 계층적 네임 스페이스를 사용 하는 경우에만 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="11adb-110">"-EnableHierarchicalNamespace $true"를 사용 하 여 "New-AzStorageAccount" cmdlet을 실행 하 여 이러한 종류의 계정을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="11adb-111">예제의</span><span class="sxs-lookup"><span data-stu-id="11adb-111">EXAMPLES</span></span>

### <span data-ttu-id="11adb-112">예제 1: 지정 된 사용 권한, Umask, 속성 및 메타 데이터를 사용 하 여 디렉터리 만들기</span><span class="sxs-lookup"><span data-stu-id="11adb-112">Example 1: Create a directory with specified permission, Umask, properties, and metadata</span></span>
```
PS C:\>New-AzDataLakeGen2Item -FileSystem "testfilesystem" -Path "dir1/dir2/" -Directory -Permission rwxrwxrwx -Umask ---rw---- -Property @{"CacheControl" = "READ"; "ContentDisposition" = "True"} -Metadata  @{"tag1" = "value1"; "tag2" = "value2" }

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2            True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="11adb-113">이 명령은 지정 된 사용 권한, Umask, 속성 및 메타 데이터로 디렉터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-113">This command creates a directory with specified Permission, Umask, properties, and metadata</span></span>

### <span data-ttu-id="11adb-114">예제 2: 로컬 원본 파일에서 데이터 호수 파일을 만들고 (업로드) 백그라운드에서 실행 되는 cmdlet</span><span class="sxs-lookup"><span data-stu-id="11adb-114">Example 2: Create(upload) a data lake file from a local source file, and the cmdlet runs in background</span></span>
```
PS C:\> $task = New-AzDataLakeGen2Item  -FileSystem "testfilesystem" -Path "dir1/dir2/file1" -Source "c:\sourcefile.txt" -Force -asjob
PS C:\> $task | Wait-Job
PS C:\> $task.Output

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group                
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2/file1      False        14400000        2020-03-23 09:19:13Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="11adb-115">이 명령은 로컬 원본 파일에서 데이터 호수 파일을 생성 (업로드) 하 고 cmdlet은 백그라운드에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-115">This command creates(upload) a data lake file from a local source file, and the cmdlet runs in background.</span></span>

## <span data-ttu-id="11adb-116">변수</span><span class="sxs-lookup"><span data-stu-id="11adb-116">PARAMETERS</span></span>

### <span data-ttu-id="11adb-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11adb-117">-AsJob</span></span>
<span data-ttu-id="11adb-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="11adb-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11adb-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="11adb-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="11adb-120">동시 비동기 작업의 전체 양입니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-120">The total amount of concurrent async tasks.</span></span> <span data-ttu-id="11adb-121">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-121">The default value is 10.</span></span>

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

### <span data-ttu-id="11adb-122">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="11adb-122">-Context</span></span>
<span data-ttu-id="11adb-123">Azure 저장소 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="11adb-123">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="11adb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11adb-124">-DefaultProfile</span></span>
<span data-ttu-id="11adb-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11adb-126">-디렉터리</span><span class="sxs-lookup"><span data-stu-id="11adb-126">-Directory</span></span>
<span data-ttu-id="11adb-127">이 새 항목이 파일이 아니라 디렉터리 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-127">Indicates that this new item is a directory and not a file.</span></span>

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

### <span data-ttu-id="11adb-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="11adb-128">-FileSystem</span></span>
<span data-ttu-id="11adb-129">파일 시스템 이름</span><span class="sxs-lookup"><span data-stu-id="11adb-129">FileSystem name</span></span>

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

### <span data-ttu-id="11adb-130">-Force</span><span class="sxs-lookup"><span data-stu-id="11adb-130">-Force</span></span>
<span data-ttu-id="11adb-131">전달 되 면 메시지를 표시 하지 않고 새 항목이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-131">If passed then new item is created without any prompt</span></span>

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

### <span data-ttu-id="11adb-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="11adb-132">-Metadata</span></span>
<span data-ttu-id="11adb-133">생성 된 디렉터리 또는 파일에 대 한 메타 데이터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-133">Specifies metadata for the created directory or file.</span></span>

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

### <span data-ttu-id="11adb-134">-Path</span><span class="sxs-lookup"><span data-stu-id="11adb-134">-Path</span></span>
<span data-ttu-id="11adb-135">지정 된 파일 시스템에서 만들어야 하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-135">The path in the specified Filesystem that should be create.</span></span>
<span data-ttu-id="11adb-136">' Directory/file.txt ' 또는 ' directory1/directory2/' 형식의 파일 또는 디렉터리만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-136">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="11adb-137">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="11adb-137">-Permission</span></span>
<span data-ttu-id="11adb-138">파일 소유자, 소유 하는 그룹 및 다른 사용자에 대 한 POSIX 액세스 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-138">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="11adb-139">각 클래스에는 읽기, 쓰기 또는 실행 권한이 부여 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-139">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="11adb-140">기호 (rwxrw)가 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-140">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="11adb-141">-속성</span><span class="sxs-lookup"><span data-stu-id="11adb-141">-Property</span></span>
<span data-ttu-id="11adb-142">생성 된 디렉터리 또는 파일의 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-142">Specifies properties for the created directory or file.</span></span> <span data-ttu-id="11adb-143">파일에 대해 지원 되는 속성은 CacheControl, ContentDisposition, Contentdisposition, Contentdisposition, ContentMD5, ContentType입니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-143">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="11adb-144">디렉터리에 대해 지원 되는 속성은 CacheControl, ContentDisposition, Contentdisposition, Contentdisposition입니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-144">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="11adb-145">-원본</span><span class="sxs-lookup"><span data-stu-id="11adb-145">-Source</span></span>
<span data-ttu-id="11adb-146">Datalake Gen2 파일에 업로드 될 로컬 원본 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-146">Specify the local source file path which will be upload to a Datalake Gen2 file.</span></span>

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

### <span data-ttu-id="11adb-147">-Umask</span><span class="sxs-lookup"><span data-stu-id="11adb-147">-Umask</span></span>
<span data-ttu-id="11adb-148">새 항목을 만들 때 부모 디렉터리에 기본 ACL이 없는 경우 umask는 만들 파일 또는 디렉터리의 사용 권한을 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-148">When creating New Item and the parent directory does not have a default ACL, the umask restricts the permissions of the file or directory to be created.</span></span>
<span data-ttu-id="11adb-149">결과 권한은 p & ^ u에 게 제공 되며, 여기서 p는 권한이 고 umask.</span><span class="sxs-lookup"><span data-stu-id="11adb-149">The resulting permission is given by p & ^u, where p is the permission and u is the umask.</span></span>
<span data-ttu-id="11adb-150">기호 (rwxrw)가 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-150">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="11adb-151">-확인</span><span class="sxs-lookup"><span data-stu-id="11adb-151">-Confirm</span></span>
<span data-ttu-id="11adb-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11adb-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11adb-153">-WhatIf</span></span>
<span data-ttu-id="11adb-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11adb-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11adb-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11adb-156">CommonParameters</span></span>
<span data-ttu-id="11adb-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11adb-158">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11adb-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11adb-159">입력</span><span class="sxs-lookup"><span data-stu-id="11adb-159">INPUTS</span></span>

### <span data-ttu-id="11adb-160">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="11adb-160">System.String</span></span>

### <span data-ttu-id="11adb-161">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="11adb-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="11adb-162">출력</span><span class="sxs-lookup"><span data-stu-id="11adb-162">OUTPUTS</span></span>

### <span data-ttu-id="11adb-163">WindowsAzure. ResourceModel를 AzureDataLakeGen2Item로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="11adb-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="11adb-164">상속자</span><span class="sxs-lookup"><span data-stu-id="11adb-164">NOTES</span></span>

## <span data-ttu-id="11adb-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11adb-165">RELATED LINKS</span></span>
