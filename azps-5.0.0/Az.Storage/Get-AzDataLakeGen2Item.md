---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
ms.openlocfilehash: edd65cc10ca90592225b6b9deb04167202510a2e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226076"
---
# <span data-ttu-id="d3174-101">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="d3174-101">Get-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="d3174-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3174-102">SYNOPSIS</span></span>
<span data-ttu-id="d3174-103">Filesystem의 파일 또는 디렉터리에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3174-103">Gets the details of a file or directory in a filesystem.</span></span>

## <span data-ttu-id="d3174-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d3174-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3174-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d3174-105">DESCRIPTION</span></span>
<span data-ttu-id="d3174-106">**AzDataLakeGen2Item** Cmdlet은 Azure 저장소 계정에서 파일 시스템에 있는 파일이 나 디렉터리의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3174-106">The **Get-AzDataLakeGen2Item** cmdlet gets the details of a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="d3174-107">이 cmdlet은 저장소 계정에 대해 계층적 네임 스페이스를 사용 하는 경우에만 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3174-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="d3174-108">"-EnableHierarchicalNamespace $true"를 사용 하 여 "New-AzStorageAccount" cmdlet을 실행 하 여 이러한 종류의 계정을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3174-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="d3174-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d3174-109">EXAMPLES</span></span>

### <span data-ttu-id="d3174-110">예제 1: Filesystem에서 디렉터리 가져오기 및 세부 정보 표시</span><span class="sxs-lookup"><span data-stu-id="d3174-110">Example 1: Get a directory from a Filesystem, and show the details</span></span>
```
PS C:\> $dir1 = Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/"
PS C:\> $dir1

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser     
 
PS C:\WINDOWS\system32> $dir1.ACL

DefaultScope AccessControlType EntityId Permissions
------------ ----------------- -------- -----------
False        User                       rwx        
False        Group                      ---        
False        Other                      rwx      

PS C:\WINDOWS\system32> $dir1.Permissions

Owner        : Execute, Write, Read
Group        : None
Other        : Execute, Write, Read
StickyBit    : False
ExtendedAcls : False

PS C:\WINDOWS\system32> $dir1.Properties.Metadata

Key          Value 
---          ----- 
hdi_isfolder true  
tag1         value1
tag2         value2

PS C:\WINDOWS\system32> $dir1.Properties

LastModified          : 3/23/2020 9:15:56 AM +00:00
CreatedOn             : 3/23/2020 9:15:56 AM +00:00
Metadata              : {[hdi_isfolder, true], [tag1, value1], [tag2, value2]}
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
ContentLength         : 0
ContentType           : application/octet-stream
ETag                  : "0x8D7CF0ACBA35FA8"
ContentHash           : 
ContentEncoding       : UDF12
ContentDisposition    : 
ContentLanguage       : 
CacheControl          : READ
AcceptRanges          : bytes
IsServerEncrypted     : True
EncryptionKeySha256   : 
AccessTier            : Cool
ArchiveStatus         : 
AccessTierChangedOn   : 1/1/0001 12:00:00 AM +00:00
```

<span data-ttu-id="d3174-111">이 명령은 Filesystem에서 디렉터리를 가져오고 세부 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3174-111">This command gets a directory from a Filesystem, and show the details.</span></span>

### <span data-ttu-id="d3174-112">예제 2: Filesystem에서 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="d3174-112">Example 2: Get a file from a Filesystem</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:20:37Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="d3174-113">이 명령은 Filesystem의 파일에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3174-113">This command gets the details of a file from a Filesystem.</span></span> 

## <span data-ttu-id="d3174-114">변수</span><span class="sxs-lookup"><span data-stu-id="d3174-114">PARAMETERS</span></span>

### <span data-ttu-id="d3174-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="d3174-115">-Context</span></span>
<span data-ttu-id="d3174-116">Azure 저장소 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="d3174-116">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="d3174-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3174-117">-DefaultProfile</span></span>
<span data-ttu-id="d3174-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3174-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3174-119">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="d3174-119">-FileSystem</span></span>
<span data-ttu-id="d3174-120">파일 시스템 이름</span><span class="sxs-lookup"><span data-stu-id="d3174-120">FileSystem name</span></span>

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

### <span data-ttu-id="d3174-121">-Path</span><span class="sxs-lookup"><span data-stu-id="d3174-121">-Path</span></span>
<span data-ttu-id="d3174-122">지정 된 파일 시스템에서 검색 해야 하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="d3174-122">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="d3174-123">' Directory/file.txt ' 또는 ' directory1/directory2/' 형식의 파일 또는 디렉터리 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3174-123">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="d3174-124">이 매개 변수를 지정 하 여 파일 시스템의 루트 디렉터리를 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d3174-124">Not specify this parameter to get the root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3174-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3174-125">CommonParameters</span></span>
<span data-ttu-id="d3174-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3174-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3174-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3174-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3174-128">입력</span><span class="sxs-lookup"><span data-stu-id="d3174-128">INPUTS</span></span>

### <span data-ttu-id="d3174-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d3174-129">System.String</span></span>

### <span data-ttu-id="d3174-130">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d3174-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d3174-131">출력</span><span class="sxs-lookup"><span data-stu-id="d3174-131">OUTPUTS</span></span>

### <span data-ttu-id="d3174-132">WindowsAzure. ResourceModel를 AzureDataLakeGen2Item로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3174-132">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="d3174-133">상속자</span><span class="sxs-lookup"><span data-stu-id="d3174-133">NOTES</span></span>

## <span data-ttu-id="d3174-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3174-134">RELATED LINKS</span></span>
