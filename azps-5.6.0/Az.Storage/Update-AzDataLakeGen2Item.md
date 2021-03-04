---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
ms.openlocfilehash: fdcac32a925cad97c256af2db949a08268e0ac3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959328"
---
# <span data-ttu-id="e9af0-101">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="e9af0-101">Update-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="e9af0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9af0-102">SYNOPSIS</span></span>
<span data-ttu-id="e9af0-103">속성, 메타데이터, 권한, ACL 및 소유자에 대한 파일 또는 디렉터리를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-103">Update a file or directory on properties, metadata, permission, ACL, and owner.</span></span>

## <span data-ttu-id="e9af0-104">구문</span><span class="sxs-lookup"><span data-stu-id="e9af0-104">SYNTAX</span></span>

### <span data-ttu-id="e9af0-105">ReceiveManual(기본값)</span><span class="sxs-lookup"><span data-stu-id="e9af0-105">ReceiveManual (Default)</span></span>
```
Update-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9af0-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="e9af0-106">ItemPipeline</span></span>
```
Update-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9af0-107">설명</span><span class="sxs-lookup"><span data-stu-id="e9af0-107">DESCRIPTION</span></span>
<span data-ttu-id="e9af0-108">**Update-AzDataLakeGen2Item** cmdlet은 속성, 메타데이터, 권한, ACL 및 소유자에 대한 파일 또는 디렉터리를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-108">The **Update-AzDataLakeGen2Item** cmdlet updates a file or directory on properties, metadata, permission, ACL, and owner.</span></span>
<span data-ttu-id="e9af0-109">이 cmdlet은 저장소 계정에 대해 계층적 네임스페이스를 사용하도록 설정한 경우만 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="e9af0-110">이러한 종류의 계정은 "-EnableHierarchicalNamespace $true"를 사용하여 "New-AzStorageAccount" cmdlet을 실행하여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="e9af0-111">예제</span><span class="sxs-lookup"><span data-stu-id="e9af0-111">EXAMPLES</span></span>

### <span data-ttu-id="e9af0-112">예제 1: ACL 항목 3개가 있는 ACL 개체 만들기 및 파일체의 모든 항목으로 ACL을 재구성적으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-112">Example 1: Create an ACL object with 3 ACL entry, and update ACL to all items in a Filesystem recursively</span></span>
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Recurse | Update-AzDataLakeGen2Item -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser           
dir1/file1           False        1024            2020-03-23 09:29:18Z rwxrw-rw-    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="e9af0-113">이 명령은 먼저 3 acl 항목이 있는 ACL 개체를 만듭니다(-InputObject 매개 변수를 사용하여 기존 acl 개체에 acl 항목을 추가한 다음 파일계의 모든 항목을 얻은 다음 항목의 acl을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-113">This command first creates an ACL object with 3 acl entry (use -InputObject parameter to add acl entry to existing acl object), then get all items in a filesystem and update acl on the items.</span></span>

### <span data-ttu-id="e9af0-114">예제 2: 파일의 모든 속성을 업데이트하고 표시</span><span class="sxs-lookup"><span data-stu-id="e9af0-114">Example 2: Update all properties on a file, and show them</span></span>
```
PS C:\> $file = Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" `
                 -Acl $acl `
                 -Property @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="; "ContentEncoding" = "UDF8"; "CacheControl" = "READ"; "ContentDisposition" = "True"; "ContentLanguage" = "EN-US"} `
                 -Metadata  @{"tag1" = "value1"; "tag2" = "value2" } `
                 -Permission rw-rw-rwx `
                 -Owner '$superuser' `
                 -Group '$superuser'

PS C:\> $file

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser          

PS C:\> $file.ACL

DefaultScope AccessControlType EntityId Permissions
------------ ----------------- -------- -----------
False        User                       rwx        
False        Group                      rw-        
False        Other                      rw-        

PS C:\> $file.Permissions

Owner        : Execute, Write, Read
Group        : Write, Read
Other        : Write, Read
StickyBit    : False
ExtendedAcls : False

PS C:\> $file.Properties.Metadata

Key  Value 
---  ----- 
tag2 value2
tag1 value1

PS C:\> $file.Properties


LastModified          : 3/23/2020 9:57:33 AM +00:00
CreatedOn             : 3/23/2020 9:29:18 AM +00:00
Metadata              : {[tag2, value2], [tag1, value1]}
CopyCompletedOn       : 1/1/0001 12:00:00 AM +00:00
CopyStatusDescription : 
CopyId                : 
CopyProgress          : 
CopySource            : 
CopyStatus            : Pending
IsIncrementalCopy     : False
LeaseDuration         : Infinite
LeaseState            : Available
LeaseStatus           : Unlocked
ContentLength         : 1024
ContentType           : image/jpeg
ETag                  : "0x8D7CF109B9878CC"
ContentHash           : {139, 189, 187, 176...}
ContentEncoding       : UDF8
ContentDisposition    : True
ContentLanguage       : EN-US
CacheControl          : READ
AcceptRanges          : bytes
IsServerEncrypted     : True
EncryptionKeySha256   : 
AccessTier            : Cool
ArchiveStatus         : 
AccessTierChangedOn   : 1/1/0001 12:00:00 AM +00:00
```

<span data-ttu-id="e9af0-115">이 명령은 파일의 모든 속성(ACL, 권한, 소유자, 그룹, 메타데이터, 속성은 모든 연결로 업데이트할 수 있습니다)을 업데이트하고 Powershell 콘솔에 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-115">This command updates all properties on a file (ACL, permission,owner, group, metadata, property can be updated with any conbination), and show them in Powershell console.</span></span>

### <span data-ttu-id="e9af0-116">예제 3: 디렉터리에 ACL 항목 추가</span><span class="sxs-lookup"><span data-stu-id="e9af0-116">Example 3: Add an ACL entry to a directory</span></span>
```
## Get the origin ACL
PS C:\> $acl = (Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path 'dir1/dir3/').ACL

# Update permission of a new ACL entry (if ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry)
PS C:\> $acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rw- -InputObject $acl  

# set the new acl to the directory
PS C:\> update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path 'dir1/dir3/' -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

<span data-ttu-id="e9af0-117">이 명령은 디렉터리에서 ACL을 얻게 하여 ACL 항목을 업데이트/추가하고 디렉터리로 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-117">This command gets ACL from a directory, updates/adds an ACL entry, and sets back to the directory.</span></span>
<span data-ttu-id="e9af0-118">동일한 AccessControlType/EntityId/DefaultScope가 있는 ACL 항목이 없는 경우 새 ACL 항목을 추가하고 기존 ACL 항목의 업데이트 권한을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-118">If ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="e9af0-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e9af0-119">PARAMETERS</span></span>

### <span data-ttu-id="e9af0-120">-Acl</span><span class="sxs-lookup"><span data-stu-id="e9af0-120">-Acl</span></span>
<span data-ttu-id="e9af0-121">파일 및 감독에 대한 POSIX 액세스 제어 권한을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-121">Sets POSIX access control rights on files and directories.</span></span>
<span data-ttu-id="e9af0-122">New-AzDataLakeGen2ItemAclObject를 사용하여 이 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-122">Create this object with New-AzDataLakeGen2ItemAclObject.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9af0-123">-Context</span><span class="sxs-lookup"><span data-stu-id="e9af0-123">-Context</span></span>
<span data-ttu-id="e9af0-124">Azure Storage 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="e9af0-124">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="e9af0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9af0-125">-DefaultProfile</span></span>
<span data-ttu-id="e9af0-126">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9af0-127">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="e9af0-127">-FileSystem</span></span>
<span data-ttu-id="e9af0-128">FileSystem 이름</span><span class="sxs-lookup"><span data-stu-id="e9af0-128">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9af0-129">-Group</span><span class="sxs-lookup"><span data-stu-id="e9af0-129">-Group</span></span>
<span data-ttu-id="e9af0-130">Blob의 소유 그룹을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-130">Sets the owning group of the blob.</span></span>

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

### <span data-ttu-id="e9af0-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9af0-131">-InputObject</span></span>
<span data-ttu-id="e9af0-132">업데이트할 Azure Datalake Gen2 항목 개체</span><span class="sxs-lookup"><span data-stu-id="e9af0-132">Azure Datalake Gen2 Item Object to update</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item
Parameter Sets: ItemPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9af0-133">-메타데이터</span><span class="sxs-lookup"><span data-stu-id="e9af0-133">-Metadata</span></span>
<span data-ttu-id="e9af0-134">디렉터리 또는 파일에 대한 메타데이터를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-134">Specifies metadata for the directory or file.</span></span>

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

### <span data-ttu-id="e9af0-135">-소유자</span><span class="sxs-lookup"><span data-stu-id="e9af0-135">-Owner</span></span>
<span data-ttu-id="e9af0-136">Blob의 소유자를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-136">Sets the owner of the blob.</span></span>

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

### <span data-ttu-id="e9af0-137">-Path</span><span class="sxs-lookup"><span data-stu-id="e9af0-137">-Path</span></span>
<span data-ttu-id="e9af0-138">업데이트해야 하는 지정된 Filesystem의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-138">The path in the specified Filesystem that should be updated.</span></span>
<span data-ttu-id="e9af0-139">파일 또는 디렉터리 형식의 'directory/file.txt' 또는 'directory1/directory2/'일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-139">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="e9af0-140">이 매개 변수를 지정하지 않으면 Filesystem의 루트 디렉터리가 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-140">Not specify this parameter will update the root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9af0-141">-권한</span><span class="sxs-lookup"><span data-stu-id="e9af0-141">-Permission</span></span>
<span data-ttu-id="e9af0-142">파일 소유자, 파일 소유 그룹 및 기타 사용자에 대한 POSIX 액세스 권한을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-142">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="e9af0-143">각 클래스는 읽기, 쓰기 또는 실행 권한을 부여할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-143">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="e9af0-144">기호(rwxrw-rw-)가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-144">Symbolic (rwxrw-rw-) is supported.</span></span>
<span data-ttu-id="e9af0-145">Acl과 함께 유효하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-145">Invalid in conjunction with Acl.</span></span>

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

### <span data-ttu-id="e9af0-146">-속성</span><span class="sxs-lookup"><span data-stu-id="e9af0-146">-Property</span></span>
<span data-ttu-id="e9af0-147">디렉터리 또는 파일에 대한 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-147">Specifies properties for the directory or file.</span></span> <span data-ttu-id="e9af0-148">파일에 지원되는 속성은 CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType입니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-148">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="e9af0-149">디렉터리에 지원되는 속성은 CacheControl, ContentDisposition, ContentEncoding, ContentLanguage입니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-149">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="e9af0-150">-확인</span><span class="sxs-lookup"><span data-stu-id="e9af0-150">-Confirm</span></span>
<span data-ttu-id="e9af0-151">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9af0-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9af0-152">-WhatIf</span></span>
<span data-ttu-id="e9af0-153">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9af0-154">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9af0-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9af0-155">CommonParameters</span></span>
<span data-ttu-id="e9af0-156">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e9af0-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9af0-157">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e9af0-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9af0-158">입력</span><span class="sxs-lookup"><span data-stu-id="e9af0-158">INPUTS</span></span>

### <span data-ttu-id="e9af0-159">System.String</span><span class="sxs-lookup"><span data-stu-id="e9af0-159">System.String</span></span>

### <span data-ttu-id="e9af0-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="e9af0-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="e9af0-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e9af0-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e9af0-162">출력</span><span class="sxs-lookup"><span data-stu-id="e9af0-162">OUTPUTS</span></span>

### <span data-ttu-id="e9af0-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="e9af0-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="e9af0-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e9af0-164">NOTES</span></span>

## <span data-ttu-id="e9af0-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9af0-165">RELATED LINKS</span></span>
