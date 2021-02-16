---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2childitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
ms.openlocfilehash: 9160eabf2492969ad7fa3916791854abd4ef6c44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187836"
---
# <span data-ttu-id="9a540-101">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="9a540-101">Get-AzDataLakeGen2ChildItem</span></span>

## <span data-ttu-id="9a540-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a540-102">SYNOPSIS</span></span>
<span data-ttu-id="9a540-103">디렉터리 또는 파일 파일 루트의 하위 디렉터리 및 파일을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-103">Lists sub directorys and files from a directory or filesystem root.</span></span>

## <span data-ttu-id="9a540-104">구문</span><span class="sxs-lookup"><span data-stu-id="9a540-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2ChildItem [-FileSystem] <String> [[-Path] <String>] [-FetchProperty] [-Recurse]
 [-MaxCount <Int32>] [-ContinuationToken <String>] [-AsJob] [-OutputUserPrincipalName]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a540-105">설명</span><span class="sxs-lookup"><span data-stu-id="9a540-105">DESCRIPTION</span></span>
<span data-ttu-id="9a540-106">**Get-AzDataLakeGen2ChildItem** cmdlet은 Azure 저장소 계정의 디렉터리 또는 파일 시스템에서 하위 디렉터리 및 파일을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-106">The **Get-AzDataLakeGen2ChildItem** cmdlet lists sub directorys and files in a directory or Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="9a540-107">이 cmdlet은 저장소 계정에 대해 계층적 네임스페이스를 사용하도록 설정한 경우만 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="9a540-108">"-EnableHierarchicalNamespace $true"를 사용하여 "New-AzStorageAccount" cmdlet을 실행하여 이러한 종류의 계정을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="9a540-109">예제</span><span class="sxs-lookup"><span data-stu-id="9a540-109">EXAMPLES</span></span>

### <span data-ttu-id="9a540-110">예제 1: 파일 파일의 직접 하위 항목 나열</span><span class="sxs-lookup"><span data-stu-id="9a540-110">Example 1: List the direct sub items from a Filesystem</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxr-x---    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxr-x---    $superuser           $superuser
```

<span data-ttu-id="9a540-111">이 명령은 파일 파일의 직접 하위 항목을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-111">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="9a540-112">예제 2: 디렉터리에서 재발적으로 나열하고 속성/ACL을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-112">Example 2: List recursively from a directory, and fetch Properties/ACL</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Path "dir1/" -Recurse -FetchProperty

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwx---rwx    $superuser           $superuser          
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser           
dir1/testfile_1K_0   False        1024            2020-03-23 09:29:21Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="9a540-113">이 명령은 파일 파일의 직접 하위 항목을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-113">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="9a540-114">예제 3: 여러 일괄 처리로 파일 파일의 항목을 재발적으로 나열</span><span class="sxs-lookup"><span data-stu-id="9a540-114">Example 3: List items recursively from a Filesystem in multiple batches</span></span>
```
PS C:\> $MaxReturn = 10000
PS C:\> $FileSystemName = "filesystem1"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $items = Get-AzDataLakeGen2ChildItem -FileSystem $FileSystemName -Recurse -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $items.Count
     if($items.Length -le 0) { Break;}
     $Token = $items[$items.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total items in Filesystem $FileSystemName"
```

<span data-ttu-id="9a540-115">이 예제에서는 *MaxCount* 및 *ContinuationToken* 매개 변수를 사용하여 파일 파일의 항목을 여러 일괄 처리로 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-115">This example uses the *MaxCount* and *ContinuationToken* parameters to list items recursively from a Filesystem in multiple batches.</span></span>
<span data-ttu-id="9a540-116">처음 4개의 명령은 예제에서 사용할 변수에 값을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-116">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="9a540-117">다섯 번째 명령은 **Get-AzDataLakeGen2ChildItem** cmdlet을 사용하여 항목을 나열하는 **Do-While** 문을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-117">The fifth command specifies a **Do-While** statement that uses the **Get-AzDataLakeGen2ChildItem** cmdlet to list items.</span></span>
<span data-ttu-id="9a540-118">이 문은 $Token 변수에 저장된 연속 토큰을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-118">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="9a540-119">$Token 실행될 때 값을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-119">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="9a540-120">마지막 명령은 **Echo** 명령을 사용하여 합계를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-120">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="9a540-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a540-121">PARAMETERS</span></span>

### <span data-ttu-id="9a540-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a540-122">-AsJob</span></span>
<span data-ttu-id="9a540-123">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9a540-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a540-124">-Context</span><span class="sxs-lookup"><span data-stu-id="9a540-124">-Context</span></span>
<span data-ttu-id="9a540-125">Azure Storage 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="9a540-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="9a540-126">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="9a540-126">-ContinuationToken</span></span>
<span data-ttu-id="9a540-127">연속 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-127">Continuation Token.</span></span>

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

### <span data-ttu-id="9a540-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a540-128">-DefaultProfile</span></span>
<span data-ttu-id="9a540-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a540-130">-FetchProperty</span><span class="sxs-lookup"><span data-stu-id="9a540-130">-FetchProperty</span></span>
<span data-ttu-id="9a540-131">datalake 항목 속성 및 ACL을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-131">Fetch the datalake item properties and ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: FetchPermission

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a540-132">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="9a540-132">-FileSystem</span></span>
<span data-ttu-id="9a540-133">FileSystem 이름</span><span class="sxs-lookup"><span data-stu-id="9a540-133">FileSystem name</span></span>

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

### <span data-ttu-id="9a540-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="9a540-134">-MaxCount</span></span>
<span data-ttu-id="9a540-135">반환할 수 있는 Blob의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-135">The max count of the blobs that can return.</span></span>

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

### <span data-ttu-id="9a540-136">-OutputUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="9a540-136">-OutputUserPrincipalName</span></span>
<span data-ttu-id="9a540-137">이 매개 변수를 지정하면 각 목록 항목의 소유자 및 그룹 필드에 반환된 사용자 ID 값이 Azure Active Directory 개체 ID에서 사용자 계정 이름으로 변환됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-137">If speicify this parameter, the user identity values returned in the owner and group fields of each list entry will be transformed from Azure Active Directory Object IDs to User Principal Names.</span></span> <span data-ttu-id="9a540-138">이 매개 변수를 지정하지 않는 경우 값은 Azure Active Directory 개체 ID로 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-138">If not speicify this parameter, the values will be returned as Azure Active Directory Object IDs.</span></span> <span data-ttu-id="9a540-139">그룹 및 애플리케이션 개체는 고유한 친숙한 이름이 아니기 때문에 번역되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-139">Note that group and application Object IDs are not translated because they do not have unique friendly names.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a540-140">-Path</span><span class="sxs-lookup"><span data-stu-id="9a540-140">-Path</span></span>
<span data-ttu-id="9a540-141">검색해야 하는 지정된 파일 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-141">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="9a540-142">디렉터리('directory1/directory2/' 형식)입니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-142">Should be a directory, in the format 'directory1/directory2/'.</span></span>

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

### <span data-ttu-id="9a540-143">-Recurse</span><span class="sxs-lookup"><span data-stu-id="9a540-143">-Recurse</span></span>
<span data-ttu-id="9a540-144">재발적으로 자식 항목을 받을지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-144">Indicates if will recursively get the Child Item.</span></span>
<span data-ttu-id="9a540-145">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-145">The default is false.</span></span>

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

### <span data-ttu-id="9a540-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a540-146">CommonParameters</span></span>
<span data-ttu-id="9a540-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9a540-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a540-148">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9a540-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a540-149">입력</span><span class="sxs-lookup"><span data-stu-id="9a540-149">INPUTS</span></span>

### <span data-ttu-id="9a540-150">System.String</span><span class="sxs-lookup"><span data-stu-id="9a540-150">System.String</span></span>

### <span data-ttu-id="9a540-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9a540-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9a540-152">출력</span><span class="sxs-lookup"><span data-stu-id="9a540-152">OUTPUTS</span></span>

### <span data-ttu-id="9a540-153">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="9a540-153">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="9a540-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9a540-154">NOTES</span></span>

## <span data-ttu-id="9a540-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a540-155">RELATED LINKS</span></span>
