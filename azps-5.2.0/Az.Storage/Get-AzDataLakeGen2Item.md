---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
ms.openlocfilehash: edd65cc10ca90592225b6b9deb04167202510a2e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325114"
---
# <span data-ttu-id="b05c6-101">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="b05c6-101">Get-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="b05c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b05c6-102">SYNOPSIS</span></span>
<span data-ttu-id="b05c6-103">파일 시스템으로 파일 또는 디렉터리의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b05c6-103">Gets the details of a file or directory in a filesystem.</span></span>

## <span data-ttu-id="b05c6-104">구문</span><span class="sxs-lookup"><span data-stu-id="b05c6-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b05c6-105">설명</span><span class="sxs-lookup"><span data-stu-id="b05c6-105">DESCRIPTION</span></span>
<span data-ttu-id="b05c6-106">**Get-AzDataLakeGen2Item** cmdlet은 Azure 저장소 계정의 파일 시스템으로 파일 또는 디렉터리의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b05c6-106">The **Get-AzDataLakeGen2Item** cmdlet gets the details of a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="b05c6-107">이 cmdlet은 저장소 계정에 대해 계층적 네임스페이스를 사용하도록 설정한 경우만 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="b05c6-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="b05c6-108">"-EnableHierarchicalNamespace $true"를 사용하여 "New-AzStorageAccount" cmdlet을 실행하여 이러한 종류의 계정을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b05c6-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="b05c6-109">예제</span><span class="sxs-lookup"><span data-stu-id="b05c6-109">EXAMPLES</span></span>

### <span data-ttu-id="b05c6-110">예제 1: 파일에서 디렉터리를 다운로드하고 세부 정보 표시</span><span class="sxs-lookup"><span data-stu-id="b05c6-110">Example 1: Get a directory from a Filesystem, and show the details</span></span>
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

<span data-ttu-id="b05c6-111">이 명령은 파일 파일에서 디렉터리를 다운로드하고 세부 정보를 보여 주며,</span><span class="sxs-lookup"><span data-stu-id="b05c6-111">This command gets a directory from a Filesystem, and show the details.</span></span>

### <span data-ttu-id="b05c6-112">예제 2: 파일 시스템에서 파일 다운로드</span><span class="sxs-lookup"><span data-stu-id="b05c6-112">Example 2: Get a file from a Filesystem</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:20:37Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="b05c6-113">이 명령은 파일 시스템으로부터 파일의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b05c6-113">This command gets the details of a file from a Filesystem.</span></span> 

## <span data-ttu-id="b05c6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b05c6-114">PARAMETERS</span></span>

### <span data-ttu-id="b05c6-115">-Context</span><span class="sxs-lookup"><span data-stu-id="b05c6-115">-Context</span></span>
<span data-ttu-id="b05c6-116">Azure Storage 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="b05c6-116">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="b05c6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b05c6-117">-DefaultProfile</span></span>
<span data-ttu-id="b05c6-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b05c6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b05c6-119">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="b05c6-119">-FileSystem</span></span>
<span data-ttu-id="b05c6-120">FileSystem 이름</span><span class="sxs-lookup"><span data-stu-id="b05c6-120">FileSystem name</span></span>

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

### <span data-ttu-id="b05c6-121">-Path</span><span class="sxs-lookup"><span data-stu-id="b05c6-121">-Path</span></span>
<span data-ttu-id="b05c6-122">검색해야 하는 지정된 파일 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="b05c6-122">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="b05c6-123">'directory/file.txt' 또는 'directory1/directory2/' 형식의 파일 또는 디렉터리일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b05c6-123">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="b05c6-124">파일 파일의 루트 디렉터리를 얻게 이 매개 변수를 지정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b05c6-124">Not specify this parameter to get the root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="b05c6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b05c6-125">CommonParameters</span></span>
<span data-ttu-id="b05c6-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b05c6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b05c6-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b05c6-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b05c6-128">입력</span><span class="sxs-lookup"><span data-stu-id="b05c6-128">INPUTS</span></span>

### <span data-ttu-id="b05c6-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b05c6-129">System.String</span></span>

### <span data-ttu-id="b05c6-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b05c6-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b05c6-131">출력</span><span class="sxs-lookup"><span data-stu-id="b05c6-131">OUTPUTS</span></span>

### <span data-ttu-id="b05c6-132">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="b05c6-132">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="b05c6-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b05c6-133">NOTES</span></span>

## <span data-ttu-id="b05c6-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b05c6-134">RELATED LINKS</span></span>
