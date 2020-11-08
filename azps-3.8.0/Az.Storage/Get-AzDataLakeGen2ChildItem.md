---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2childitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
ms.openlocfilehash: 9160eabf2492969ad7fa3916791854abd4ef6c44
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042303"
---
# <span data-ttu-id="948a5-101">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="948a5-101">Get-AzDataLakeGen2ChildItem</span></span>

## <span data-ttu-id="948a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="948a5-102">SYNOPSIS</span></span>
<span data-ttu-id="948a5-103">디렉터리 또는 파일 시스템 루트의 하위 항목 및 파일을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="948a5-103">Lists sub directorys and files from a directory or filesystem root.</span></span>

## <span data-ttu-id="948a5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="948a5-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2ChildItem [-FileSystem] <String> [[-Path] <String>] [-FetchProperty] [-Recurse]
 [-MaxCount <Int32>] [-ContinuationToken <String>] [-AsJob] [-OutputUserPrincipalName]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="948a5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="948a5-105">DESCRIPTION</span></span>
<span data-ttu-id="948a5-106">**AzDataLakeGen2ChildItem** cmdlet은 디렉터리 또는 파일 시스템의 Azure 저장소 계정에 하위 directorys를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="948a5-106">The **Get-AzDataLakeGen2ChildItem** cmdlet lists sub directorys and files in a directory or Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="948a5-107">이 cmdlet은 저장소 계정에 대해 계층적 네임 스페이스를 사용 하는 경우에만 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="948a5-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="948a5-108">"-EnableHierarchicalNamespace $true"를 사용 하 여 "New-AzStorageAccount" cmdlet을 실행 하 여 이러한 종류의 계정을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="948a5-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="948a5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="948a5-109">EXAMPLES</span></span>

### <span data-ttu-id="948a5-110">예제 1: 파일 시스템의 직계 하위 항목 나열</span><span class="sxs-lookup"><span data-stu-id="948a5-110">Example 1: List the direct sub items from a Filesystem</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxr-x---    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxr-x---    $superuser           $superuser
```

<span data-ttu-id="948a5-111">이 명령은 Filesystem의 직계 하위 항목을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="948a5-111">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="948a5-112">예제 2: 디렉터리에서 재귀적으로 나열 하 고 속성/ACL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="948a5-112">Example 2: List recursively from a directory, and fetch Properties/ACL</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Path "dir1/" -Recurse -FetchProperty

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwx---rwx    $superuser           $superuser          
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser           
dir1/testfile_1K_0   False        1024            2020-03-23 09:29:21Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="948a5-113">이 명령은 Filesystem의 직계 하위 항목을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="948a5-113">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="948a5-114">예제 3: 여러 일괄 작업의 파일 시스템에서 재귀적으로 항목 목록 표시</span><span class="sxs-lookup"><span data-stu-id="948a5-114">Example 3: List items recursively from a Filesystem in multiple batches</span></span>
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

<span data-ttu-id="948a5-115">이 예제에서는 *MaxCount* 및 *ContinuationToken* 매개 변수를 사용 하 여 여러 일괄 처리의 파일 시스템에서 재귀적으로 항목을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="948a5-115">This example uses the *MaxCount* and *ContinuationToken* parameters to list items recursively from a Filesystem in multiple batches.</span></span>
<span data-ttu-id="948a5-116">처음 4 개의 명령은 예제에서 사용할 변수에 값을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="948a5-116">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="948a5-117">다섯 번째 명령은 **AzDataLakeGen2ChildItem** cmdlet을 사용 하 여 항목을 나열 하는 **Do While** 문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="948a5-117">The fifth command specifies a **Do-While** statement that uses the **Get-AzDataLakeGen2ChildItem** cmdlet to list items.</span></span>
<span data-ttu-id="948a5-118">이 문에는 $Token 변수에 저장 된 연속 토큰이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="948a5-118">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="948a5-119">루프가 실행 되는 동안 값이 변경 $Token.</span><span class="sxs-lookup"><span data-stu-id="948a5-119">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="948a5-120">마지막 명령은 **Echo** 명령을 사용 하 여 합계를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="948a5-120">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="948a5-121">변수</span><span class="sxs-lookup"><span data-stu-id="948a5-121">PARAMETERS</span></span>

### <span data-ttu-id="948a5-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="948a5-122">-AsJob</span></span>
<span data-ttu-id="948a5-123">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="948a5-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="948a5-124">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="948a5-124">-Context</span></span>
<span data-ttu-id="948a5-125">Azure 저장소 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="948a5-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="948a5-126">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="948a5-126">-ContinuationToken</span></span>
<span data-ttu-id="948a5-127">연속 토큰.</span><span class="sxs-lookup"><span data-stu-id="948a5-127">Continuation Token.</span></span>

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

### <span data-ttu-id="948a5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="948a5-128">-DefaultProfile</span></span>
<span data-ttu-id="948a5-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="948a5-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="948a5-130">-FetchProperty</span><span class="sxs-lookup"><span data-stu-id="948a5-130">-FetchProperty</span></span>
<span data-ttu-id="948a5-131">Datalake item 속성 및 ACL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="948a5-131">Fetch the datalake item properties and ACL.</span></span>

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

### <span data-ttu-id="948a5-132">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="948a5-132">-FileSystem</span></span>
<span data-ttu-id="948a5-133">파일 시스템 이름</span><span class="sxs-lookup"><span data-stu-id="948a5-133">FileSystem name</span></span>

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

### <span data-ttu-id="948a5-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="948a5-134">-MaxCount</span></span>
<span data-ttu-id="948a5-135">반환할 수 있는 blob의 최대 개수입니다.</span><span class="sxs-lookup"><span data-stu-id="948a5-135">The max count of the blobs that can return.</span></span>

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

### <span data-ttu-id="948a5-136">-OutputUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="948a5-136">-OutputUserPrincipalName</span></span>
<span data-ttu-id="948a5-137">이 매개 변수를 speicify 경우 각 목록 항목의 소유자 및 그룹 필드에 반환 된 사용자 id 값이 Azure Active Directory 개체 Id에서 사용자 주체 이름으로 변환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="948a5-137">If speicify this parameter, the user identity values returned in the owner and group fields of each list entry will be transformed from Azure Active Directory Object IDs to User Principal Names.</span></span> <span data-ttu-id="948a5-138">이 매개 변수를 speicify 하지 않으면 값이 Azure Active Directory 개체 Id로 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="948a5-138">If not speicify this parameter, the values will be returned as Azure Active Directory Object IDs.</span></span> <span data-ttu-id="948a5-139">그룹 및 응용 프로그램 개체 Id는 고유한 이름을 가지 지 않으므로 번역 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="948a5-139">Note that group and application Object IDs are not translated because they do not have unique friendly names.</span></span>

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

### <span data-ttu-id="948a5-140">-Path</span><span class="sxs-lookup"><span data-stu-id="948a5-140">-Path</span></span>
<span data-ttu-id="948a5-141">지정 된 파일 시스템에서 검색 해야 하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="948a5-141">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="948a5-142">' Directory1/directory2/' 형식의 디렉터리 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="948a5-142">Should be a directory, in the format 'directory1/directory2/'.</span></span>

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

### <span data-ttu-id="948a5-143">-재귀적으로</span><span class="sxs-lookup"><span data-stu-id="948a5-143">-Recurse</span></span>
<span data-ttu-id="948a5-144">이 재귀적으로 자식 항목을 가져올 것임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="948a5-144">Indicates if will recursively get the Child Item.</span></span>
<span data-ttu-id="948a5-145">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="948a5-145">The default is false.</span></span>

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

### <span data-ttu-id="948a5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="948a5-146">CommonParameters</span></span>
<span data-ttu-id="948a5-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="948a5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="948a5-148">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="948a5-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="948a5-149">입력</span><span class="sxs-lookup"><span data-stu-id="948a5-149">INPUTS</span></span>

### <span data-ttu-id="948a5-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="948a5-150">System.String</span></span>

### <span data-ttu-id="948a5-151">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="948a5-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="948a5-152">출력</span><span class="sxs-lookup"><span data-stu-id="948a5-152">OUTPUTS</span></span>

### <span data-ttu-id="948a5-153">WindowsAzure. ResourceModel를 AzureDataLakeGen2Item로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="948a5-153">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="948a5-154">상속자</span><span class="sxs-lookup"><span data-stu-id="948a5-154">NOTES</span></span>

## <span data-ttu-id="948a5-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="948a5-155">RELATED LINKS</span></span>
