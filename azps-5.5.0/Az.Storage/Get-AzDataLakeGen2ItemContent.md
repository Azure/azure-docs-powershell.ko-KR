---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2itemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
ms.openlocfilehash: 9721305494ffd9b1d6a6f260008f050c9600437a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178268"
---
# <span data-ttu-id="320aa-101">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="320aa-101">Get-AzDataLakeGen2ItemContent</span></span>

## <span data-ttu-id="320aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="320aa-102">SYNOPSIS</span></span>
<span data-ttu-id="320aa-103">파일을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="320aa-103">Download a file.</span></span>

## <span data-ttu-id="320aa-104">구문</span><span class="sxs-lookup"><span data-stu-id="320aa-104">SYNTAX</span></span>

### <span data-ttu-id="320aa-105">ReceiveManual(기본값)</span><span class="sxs-lookup"><span data-stu-id="320aa-105">ReceiveManual (Default)</span></span>
```
Get-AzDataLakeGen2ItemContent [-FileSystem] <String> [-Path] <String> [-Destination <String>] [-CheckMd5]
 [-Force] [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="320aa-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="320aa-106">ItemPipeline</span></span>
```
Get-AzDataLakeGen2ItemContent -InputObject <AzureDataLakeGen2Item> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="320aa-107">설명</span><span class="sxs-lookup"><span data-stu-id="320aa-107">DESCRIPTION</span></span>
<span data-ttu-id="320aa-108">**Get-AzDataLakeGen2ItemContent** cmdlet은 Azure 저장소 계정의 파일 시스템으로 파일을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="320aa-108">The **Get-AzDataLakeGen2ItemContent** cmdlet download a file in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="320aa-109">이 cmdlet은 저장소 계정에 대해 계층적 네임스페이스를 사용하도록 설정한 경우만 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="320aa-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="320aa-110">"-EnableHierarchicalNamespace $true"를 사용하여 "New-AzStorageAccount" cmdlet을 실행하여 이러한 종류의 계정을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="320aa-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="320aa-111">예제</span><span class="sxs-lookup"><span data-stu-id="320aa-111">EXAMPLES</span></span>

### <span data-ttu-id="320aa-112">예제 1: 프롬프트 없이 파일 다운로드</span><span class="sxs-lookup"><span data-stu-id="320aa-112">Example 1: Download a file without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2ItemContent -FileSystem "filesystem1" -Path "dir1/file1" -Destination $localDestFile -Force

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="320aa-113">이 명령은 프롬프트 없이 파일을 로컬 파일에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="320aa-113">This command downloads a file to a local file without prompt.</span></span>

### <span data-ttu-id="320aa-114">예제 2: 파일을 다운로드한 다음, 파일을 로컬 파일에 다운로드하는 파이프라인</span><span class="sxs-lookup"><span data-stu-id="320aa-114">Example 2: Get a file, then pipeline to download the file to a local file</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" |  Get-AzDataLakeGen2ItemContent -Destination $localDestFile 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="320aa-115">이 명령은 먼저 파일을 다운로드한 다음, 파일을 로컬 파일에 다운로드하는 파이프라인을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="320aa-115">This command first gets a file, then pipeline to download the file to a local file.</span></span>

## <span data-ttu-id="320aa-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="320aa-116">PARAMETERS</span></span>

### <span data-ttu-id="320aa-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="320aa-117">-AsJob</span></span>
<span data-ttu-id="320aa-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="320aa-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="320aa-119">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="320aa-119">-CheckMd5</span></span>
<span data-ttu-id="320aa-120">md5sum 확인</span><span class="sxs-lookup"><span data-stu-id="320aa-120">check the md5sum</span></span>

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

### <span data-ttu-id="320aa-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="320aa-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="320aa-122">동시 비동기 작업의 총 양입니다.</span><span class="sxs-lookup"><span data-stu-id="320aa-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="320aa-123">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="320aa-123">The default value is 10.</span></span>

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

### <span data-ttu-id="320aa-124">-Context</span><span class="sxs-lookup"><span data-stu-id="320aa-124">-Context</span></span>
<span data-ttu-id="320aa-125">Azure Storage 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="320aa-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="320aa-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="320aa-126">-DefaultProfile</span></span>
<span data-ttu-id="320aa-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="320aa-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="320aa-128">-Destination</span><span class="sxs-lookup"><span data-stu-id="320aa-128">-Destination</span></span>
<span data-ttu-id="320aa-129">대상 로컬 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="320aa-129">Destination local file path.</span></span>

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

### <span data-ttu-id="320aa-130">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="320aa-130">-FileSystem</span></span>
<span data-ttu-id="320aa-131">FileSystem 이름</span><span class="sxs-lookup"><span data-stu-id="320aa-131">FileSystem name</span></span>

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

### <span data-ttu-id="320aa-132">-Force</span><span class="sxs-lookup"><span data-stu-id="320aa-132">-Force</span></span>
<span data-ttu-id="320aa-133">기존 Blob 또는 파일을 강제로 덮어 덮어 사용</span><span class="sxs-lookup"><span data-stu-id="320aa-133">Force to overwrite the existing blob or file</span></span>

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

### <span data-ttu-id="320aa-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="320aa-134">-InputObject</span></span>
<span data-ttu-id="320aa-135">다운로드할 Azure Datalake Gen2 항목 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="320aa-135">Azure Datalake Gen2 Item Object to download.</span></span>

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

### <span data-ttu-id="320aa-136">-Path</span><span class="sxs-lookup"><span data-stu-id="320aa-136">-Path</span></span>
<span data-ttu-id="320aa-137">제거해야 하는 지정된 파일 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="320aa-137">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="320aa-138">'directory/file.txt' 또는 'directory1/directory2/' 형식의 파일 또는 디렉터리일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="320aa-138">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="320aa-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="320aa-139">-Confirm</span></span>
<span data-ttu-id="320aa-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="320aa-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="320aa-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="320aa-141">-WhatIf</span></span>
<span data-ttu-id="320aa-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="320aa-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="320aa-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="320aa-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="320aa-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="320aa-144">CommonParameters</span></span>
<span data-ttu-id="320aa-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="320aa-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="320aa-146">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="320aa-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="320aa-147">입력</span><span class="sxs-lookup"><span data-stu-id="320aa-147">INPUTS</span></span>

### <span data-ttu-id="320aa-148">System.String</span><span class="sxs-lookup"><span data-stu-id="320aa-148">System.String</span></span>

### <span data-ttu-id="320aa-149">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="320aa-149">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="320aa-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="320aa-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="320aa-151">출력</span><span class="sxs-lookup"><span data-stu-id="320aa-151">OUTPUTS</span></span>

### <span data-ttu-id="320aa-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="320aa-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="320aa-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="320aa-153">NOTES</span></span>

## <span data-ttu-id="320aa-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="320aa-154">RELATED LINKS</span></span>
