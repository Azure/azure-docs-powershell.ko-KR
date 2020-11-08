---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
ms.openlocfilehash: 6af68da41e1d5ea212d23d0cbc2296a68a6fa7e5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034961"
---
# <span data-ttu-id="8cd61-101">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="8cd61-101">Update-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="8cd61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cd61-102">SYNOPSIS</span></span>
<span data-ttu-id="8cd61-103">속성, 메타 데이터, 사용 권한, ACL 및 owner에 대 한 파일 또는 디렉터리를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-103">Update a file or directory on properties, metadata, permission, ACL, and owner.</span></span>

## <span data-ttu-id="8cd61-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8cd61-104">SYNTAX</span></span>

### <span data-ttu-id="8cd61-105">ReceiveManual (기본값)</span><span class="sxs-lookup"><span data-stu-id="8cd61-105">ReceiveManual (Default)</span></span>
```
Update-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8cd61-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="8cd61-106">ItemPipeline</span></span>
```
Update-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8cd61-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8cd61-107">DESCRIPTION</span></span>
<span data-ttu-id="8cd61-108">**AzDataLakeGen2Item** cmdlet은 속성, 메타 데이터, 사용 권한, ACL 및 owner에 대 한 파일 또는 디렉터리를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-108">The **Update-AzDataLakeGen2Item** cmdlet updates a file or directory on properties, metadata, permission, ACL, and owner.</span></span>
<span data-ttu-id="8cd61-109">이 cmdlet은 저장소 계정에 대해 계층적 네임 스페이스를 사용 하는 경우에만 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="8cd61-110">"-EnableHierarchicalNamespace $true"를 사용 하 여 "New-AzStorageAccount" cmdlet을 실행 하 여 이러한 종류의 계정을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="8cd61-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8cd61-111">EXAMPLES</span></span>

### <span data-ttu-id="8cd61-112">예제 1: ACL 항목이 3 개 있는 ACL 개체를 만들고 파일 시스템의 모든 항목에 대 한 ACL을 재귀적으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-112">Example 1: Create an ACL object with 3 ACL entry, and update ACL to all items in a Filesystem recursively</span></span>
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

<span data-ttu-id="8cd61-113">이 명령은 먼저 3 개의 acl 항목이 있는 ACL 개체를 만들고 (-InputObject 매개 변수를 사용 하 여 기존 acl 개체에 acl 항목을 추가 하려면) filesystem의 모든 항목을 가져오고 항목의 ACL을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-113">This command first creates an ACL object with 3 acl entry (use -InputObject parameter to add acl entry to existing acl object), then get all items in a filesystem and update acl on the items.</span></span>

### <span data-ttu-id="8cd61-114">예제 2: 파일의 모든 속성 업데이트 및 표시</span><span class="sxs-lookup"><span data-stu-id="8cd61-114">Example 2: Update all properties on a file, and show them</span></span>
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

<span data-ttu-id="8cd61-115">이 명령은 파일의 모든 속성 (ACL, 사용 권한, 소유자, 그룹, 메타 데이터, 속성을 conbination으로 업데이트할 수 있음)을 업데이트 하 고 Powershell 콘솔에 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-115">This command updates all properties on a file (ACL, permission,owner, group, metadata, property can be updated with any conbination), and show them in Powershell console.</span></span>

### <span data-ttu-id="8cd61-116">예제 3: 디렉터리에 ACL 항목 추가</span><span class="sxs-lookup"><span data-stu-id="8cd61-116">Example 3: Add an ACL entry to a directory</span></span>
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

<span data-ttu-id="8cd61-117">이 명령은 디렉터리에서 ACL을 가져오고, ACL 항목을 업데이트/추가 하 고, 디렉터리로 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-117">This command gets ACL from a directory, updates/adds an ACL entry, and sets back to the directory.</span></span>
<span data-ttu-id="8cd61-118">AccessControlType/EntityId/DefaultScope가 같은 ACL 항목이 없는 경우 새 ACL 항목을 추가 하 고 기존 ACL 항목을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-118">If ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="8cd61-119">변수</span><span class="sxs-lookup"><span data-stu-id="8cd61-119">PARAMETERS</span></span>

### <span data-ttu-id="8cd61-120">-Acl</span><span class="sxs-lookup"><span data-stu-id="8cd61-120">-Acl</span></span>
<span data-ttu-id="8cd61-121">파일 및 디렉터리에 대 한 POSIX 액세스 제어 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-121">Sets POSIX access control rights on files and directories.</span></span>
<span data-ttu-id="8cd61-122">새 AzDataLakeGen2ItemAclObject를 사용 하 여이 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-122">Create this object with New-AzDataLakeGen2ItemAclObject.</span></span>

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

### <span data-ttu-id="8cd61-123">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="8cd61-123">-Context</span></span>
<span data-ttu-id="8cd61-124">Azure 저장소 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="8cd61-124">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="8cd61-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cd61-125">-DefaultProfile</span></span>
<span data-ttu-id="8cd61-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cd61-127">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="8cd61-127">-FileSystem</span></span>
<span data-ttu-id="8cd61-128">파일 시스템 이름</span><span class="sxs-lookup"><span data-stu-id="8cd61-128">FileSystem name</span></span>

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

### <span data-ttu-id="8cd61-129">-그룹</span><span class="sxs-lookup"><span data-stu-id="8cd61-129">-Group</span></span>
<span data-ttu-id="8cd61-130">Blob의 소유 그룹을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-130">Sets the owning group of the blob.</span></span>

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

### <span data-ttu-id="8cd61-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cd61-131">-InputObject</span></span>
<span data-ttu-id="8cd61-132">업데이트할 Azure Datalake Gen2 Item 개체</span><span class="sxs-lookup"><span data-stu-id="8cd61-132">Azure Datalake Gen2 Item Object to update</span></span>

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

### <span data-ttu-id="8cd61-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="8cd61-133">-Metadata</span></span>
<span data-ttu-id="8cd61-134">디렉터리 또는 파일에 대 한 메타 데이터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-134">Specifies metadata for the directory or file.</span></span>

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

### <span data-ttu-id="8cd61-135">-소유자</span><span class="sxs-lookup"><span data-stu-id="8cd61-135">-Owner</span></span>
<span data-ttu-id="8cd61-136">Blob의 소유자를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-136">Sets the owner of the blob.</span></span>

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

### <span data-ttu-id="8cd61-137">-Path</span><span class="sxs-lookup"><span data-stu-id="8cd61-137">-Path</span></span>
<span data-ttu-id="8cd61-138">지정 된 파일 시스템에서 업데이트 해야 하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-138">The path in the specified Filesystem that should be updated.</span></span>
<span data-ttu-id="8cd61-139">' Directory/file.txt ' 또는 ' directory1/directory2/' 형식의 파일 또는 디렉터리 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-139">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="8cd61-140">이 매개 변수를 지정 하지 않으면 파일 시스템의 루트 디렉터리가 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-140">Not specify this parameter will update the root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="8cd61-141">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="8cd61-141">-Permission</span></span>
<span data-ttu-id="8cd61-142">파일 소유자, 소유 하는 그룹 및 다른 사용자에 대 한 POSIX 액세스 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-142">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="8cd61-143">각 클래스에는 읽기, 쓰기 또는 실행 권한이 부여 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-143">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="8cd61-144">기호 (rwxrw)가 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-144">Symbolic (rwxrw-rw-) is supported.</span></span>
<span data-ttu-id="8cd61-145">Acl과 함께 사용할 올바르지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-145">Invalid in conjunction with Acl.</span></span>

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

### <span data-ttu-id="8cd61-146">-속성</span><span class="sxs-lookup"><span data-stu-id="8cd61-146">-Property</span></span>
<span data-ttu-id="8cd61-147">디렉터리 또는 파일의 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-147">Specifies properties for the directory or file.</span></span> <span data-ttu-id="8cd61-148">파일에 대해 지원 되는 속성은 CacheControl, ContentDisposition, Contentdisposition, Contentdisposition, ContentMD5, ContentType입니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-148">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="8cd61-149">디렉터리에 대해 지원 되는 속성은 CacheControl, ContentDisposition, Contentdisposition, Contentdisposition입니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-149">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="8cd61-150">-확인</span><span class="sxs-lookup"><span data-stu-id="8cd61-150">-Confirm</span></span>
<span data-ttu-id="8cd61-151">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cd61-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cd61-152">-WhatIf</span></span>
<span data-ttu-id="8cd61-153">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cd61-154">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cd61-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cd61-155">CommonParameters</span></span>
<span data-ttu-id="8cd61-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cd61-157">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cd61-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cd61-158">입력</span><span class="sxs-lookup"><span data-stu-id="8cd61-158">INPUTS</span></span>

### <span data-ttu-id="8cd61-159">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8cd61-159">System.String</span></span>

### <span data-ttu-id="8cd61-160">WindowsAzure. ResourceModel를 AzureDataLakeGen2Item로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="8cd61-161">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8cd61-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8cd61-162">출력</span><span class="sxs-lookup"><span data-stu-id="8cd61-162">OUTPUTS</span></span>

### <span data-ttu-id="8cd61-163">WindowsAzure. ResourceModel를 AzureDataLakeGen2Item로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd61-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="8cd61-164">상속자</span><span class="sxs-lookup"><span data-stu-id="8cd61-164">NOTES</span></span>

## <span data-ttu-id="8cd61-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8cd61-165">RELATED LINKS</span></span>
