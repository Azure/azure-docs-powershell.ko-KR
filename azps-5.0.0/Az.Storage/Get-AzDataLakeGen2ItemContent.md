---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2itemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
ms.openlocfilehash: 9721305494ffd9b1d6a6f260008f050c9600437a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226075"
---
# <span data-ttu-id="d1275-101">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="d1275-101">Get-AzDataLakeGen2ItemContent</span></span>

## <span data-ttu-id="d1275-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1275-102">SYNOPSIS</span></span>
<span data-ttu-id="d1275-103">파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1275-103">Download a file.</span></span>

## <span data-ttu-id="d1275-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d1275-104">SYNTAX</span></span>

### <span data-ttu-id="d1275-105">ReceiveManual (기본값)</span><span class="sxs-lookup"><span data-stu-id="d1275-105">ReceiveManual (Default)</span></span>
```
Get-AzDataLakeGen2ItemContent [-FileSystem] <String> [-Path] <String> [-Destination <String>] [-CheckMd5]
 [-Force] [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1275-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="d1275-106">ItemPipeline</span></span>
```
Get-AzDataLakeGen2ItemContent -InputObject <AzureDataLakeGen2Item> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1275-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d1275-107">DESCRIPTION</span></span>
<span data-ttu-id="d1275-108">**AzDataLakeGen2ItemContent** Cmdlet은 Azure 저장소 계정에서 파일 시스템에 있는 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1275-108">The **Get-AzDataLakeGen2ItemContent** cmdlet download a file in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="d1275-109">이 cmdlet은 저장소 계정에 대해 계층적 네임 스페이스를 사용 하는 경우에만 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1275-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="d1275-110">"-EnableHierarchicalNamespace $true"를 사용 하 여 "New-AzStorageAccount" cmdlet을 실행 하 여 이러한 종류의 계정을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1275-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="d1275-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d1275-111">EXAMPLES</span></span>

### <span data-ttu-id="d1275-112">예제 1: 메시지를 표시 하지 않고 파일 다운로드</span><span class="sxs-lookup"><span data-stu-id="d1275-112">Example 1: Download a file without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2ItemContent -FileSystem "filesystem1" -Path "dir1/file1" -Destination $localDestFile -Force

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="d1275-113">이 명령은 메시지를 표시 하지 않고 로컬 파일에 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1275-113">This command downloads a file to a local file without prompt.</span></span>

### <span data-ttu-id="d1275-114">예제 2: 파일을 가져오고 파이프라인을 통해 로컬 파일로 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1275-114">Example 2: Get a file, then pipeline to download the file to a local file</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" |  Get-AzDataLakeGen2ItemContent -Destination $localDestFile 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="d1275-115">이 명령은 먼저 파일을 가져온 다음 파이프라인을 통해 로컬 파일에 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1275-115">This command first gets a file, then pipeline to download the file to a local file.</span></span>

## <span data-ttu-id="d1275-116">변수</span><span class="sxs-lookup"><span data-stu-id="d1275-116">PARAMETERS</span></span>

### <span data-ttu-id="d1275-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1275-117">-AsJob</span></span>
<span data-ttu-id="d1275-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d1275-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d1275-119">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="d1275-119">-CheckMd5</span></span>
<span data-ttu-id="d1275-120">md5sum 확인</span><span class="sxs-lookup"><span data-stu-id="d1275-120">check the md5sum</span></span>

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

### <span data-ttu-id="d1275-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d1275-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d1275-122">동시 비동기 작업의 전체 양입니다.</span><span class="sxs-lookup"><span data-stu-id="d1275-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="d1275-123">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="d1275-123">The default value is 10.</span></span>

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

### <span data-ttu-id="d1275-124">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="d1275-124">-Context</span></span>
<span data-ttu-id="d1275-125">Azure 저장소 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="d1275-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="d1275-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1275-126">-DefaultProfile</span></span>
<span data-ttu-id="d1275-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1275-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1275-128">-대상</span><span class="sxs-lookup"><span data-stu-id="d1275-128">-Destination</span></span>
<span data-ttu-id="d1275-129">대상 로컬 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="d1275-129">Destination local file path.</span></span>

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

### <span data-ttu-id="d1275-130">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="d1275-130">-FileSystem</span></span>
<span data-ttu-id="d1275-131">파일 시스템 이름</span><span class="sxs-lookup"><span data-stu-id="d1275-131">FileSystem name</span></span>

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

### <span data-ttu-id="d1275-132">-Force</span><span class="sxs-lookup"><span data-stu-id="d1275-132">-Force</span></span>
<span data-ttu-id="d1275-133">기존 blob 또는 파일 강제 덮어쓰기</span><span class="sxs-lookup"><span data-stu-id="d1275-133">Force to overwrite the existing blob or file</span></span>

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

### <span data-ttu-id="d1275-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1275-134">-InputObject</span></span>
<span data-ttu-id="d1275-135">Azure Datalake Gen2 Item 개체를 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1275-135">Azure Datalake Gen2 Item Object to download.</span></span>

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

### <span data-ttu-id="d1275-136">-Path</span><span class="sxs-lookup"><span data-stu-id="d1275-136">-Path</span></span>
<span data-ttu-id="d1275-137">지정 된 파일 시스템에서 제거 해야 하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="d1275-137">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="d1275-138">' Directory/file.txt ' 또는 ' directory1/directory2/' 형식의 파일 또는 디렉터리만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1275-138">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1275-139">-확인</span><span class="sxs-lookup"><span data-stu-id="d1275-139">-Confirm</span></span>
<span data-ttu-id="d1275-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1275-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1275-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1275-141">-WhatIf</span></span>
<span data-ttu-id="d1275-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d1275-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1275-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1275-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1275-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1275-144">CommonParameters</span></span>
<span data-ttu-id="d1275-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1275-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1275-146">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1275-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1275-147">입력</span><span class="sxs-lookup"><span data-stu-id="d1275-147">INPUTS</span></span>

### <span data-ttu-id="d1275-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d1275-148">System.String</span></span>

### <span data-ttu-id="d1275-149">WindowsAzure. ResourceModel를 AzureDataLakeGen2Item로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1275-149">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="d1275-150">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d1275-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d1275-151">출력</span><span class="sxs-lookup"><span data-stu-id="d1275-151">OUTPUTS</span></span>

### <span data-ttu-id="d1275-152">WindowsAzure. ResourceModel를 AzureDataLakeGen2Item로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1275-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="d1275-153">상속자</span><span class="sxs-lookup"><span data-stu-id="d1275-153">NOTES</span></span>

## <span data-ttu-id="d1275-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1275-154">RELATED LINKS</span></span>
